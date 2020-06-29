---
title: App-V 사후 설치 검사 목록
description: App-V 사후 설치 검사 목록
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819803"
---
# <span data-ttu-id="0413b-103">App-V 사후 설치 검사 목록</span><span class="sxs-lookup"><span data-stu-id="0413b-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="0413b-104">다음 검사 목록에서는 Microsoft App-v 데스크톱 클라이언트의 설치를 완료 한 후에 고려해 야 할 항목의 상위 수준 목록을 제공 하 고이를 수행 하는 단계를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0413b-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0413b-105">단계</span><span class="sxs-lookup"><span data-stu-id="0413b-105">Step</span></span></th>
<th align="left"><span data-ttu-id="0413b-106">참고자료</span><span class="sxs-lookup"><span data-stu-id="0413b-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0413b-107">App-v 관리 서버 또는 스트리밍 서버 서비스에 대 한 방화벽 예외를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0413b-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="0413b-108">App-V Server용 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="0413b-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0413b-109">기본 응용 프로그램을 게시, 스트리밍 및 테스트 하 여 App-v 시스템이 제대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0413b-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="0413b-110">기본 응용 프로그램을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0413b-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0413b-111"><strong>ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> 및 <strong> OSDSourceRoot 설정을 통해 스트리밍할 수 있도록 app-v 스트리밍 서버 또는 다른 서버를 사용 하도록 app-v 클라이언트를 구성 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="0413b-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="0413b-112">응용 프로그램 패키지 검색에 대한 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0413b-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0413b-113">오프 라인 배포를 위해 시퀀싱 된 응용 프로그램 패키지의 .msi 파일 버전을 사용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0413b-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="0413b-114">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="0413b-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0413b-115">) App-v 데이터베이스에 대 한 SQL Server 데이터베이스 미러링을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0413b-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="0413b-116">App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0413b-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0413b-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0413b-117">Related topics</span></span>


[<span data-ttu-id="0413b-118">Application Virtualization 배포 및 업그레이드 검사 목록</span><span class="sxs-lookup"><span data-stu-id="0413b-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





