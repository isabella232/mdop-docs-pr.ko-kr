---
title: HTTP를 통한 클라이언트 보고 지원
description: HTTP를 통한 클라이언트 보고 지원
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815288"
---
# <span data-ttu-id="3a62d-103">HTTP를 통한 클라이언트 보고 지원</span><span class="sxs-lookup"><span data-stu-id="3a62d-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="3a62d-104">현재 App-v 클라이언트의 버전 4.6에서는 클라이언트 보고 데이터를 게시 서버로 전송할 때 HTTP 통신을 사용 하도록 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="3a62d-105">이 기능은 고객이 클라이언트 데이터를 수집 하 고 처리 하도록 구성 된 사용자 지정 HTTP (S) 게시 서버를 구현한 시나리오를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="3a62d-106">HTTP 게시 서버에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a62d-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="3a62d-107">HTTP를 통한 클라이언트 보고</span><span class="sxs-lookup"><span data-stu-id="3a62d-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="3a62d-108">클라이언트는 게시 서버에서 게시 새로 고침 응답 XML의 "보고 =" TRUE "" 특성을 수신 하는 경우 데이터 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="3a62d-109">이 특성이 수신 되 면 클라이언트는 게시 새로 고침을 보낸 게시 서버로 누적 된 데이터를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="3a62d-110">이 프로세스에 대 한 세부 정보는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="3a62d-111">클라이언트가 게시 새로 고침을 위해 게시 서버로 HTTP GET 요청을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="3a62d-112">이 메시지의 헤더에는 사용자 지정 HTTP (S) 게시 서버에서 메시지 유형을 식별 하는 데 사용 하는 "AppV Op: Refresh" 사용자 지정 헤더가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="3a62d-113">그런 다음 게시 서버는 "보고 =" TRUE "" 값이 포함 된 게시 새로 고침 응답 XML을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="3a62d-114">그러면 클라이언트는 이전 새로 고침 이후 수집 된 보고 데이터와 함께 HTTP POST 요청을 게시 서버에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="3a62d-115">이 메시지의 머리글에는 사용자 지정 HTTP (S) 게시 서버에서 메시지 유형을 식별 하는 데 사용 하는 "AppV Op: Report" 사용자 지정 헤더가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="3a62d-116">다음 스키마는 패키지 및 서버에 전송 되는 응용 프로그램 데이터에 대 한 구체적인 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a62d-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





