---
title: 보안 스트리밍을 위해 IIS 구성
description: 보안 스트리밍을 위해 IIS 구성
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821883"
---
# 보안 스트리밍을 위해 IIS 구성


Microsoft App-v (Application Virtualization) 버전 4.5에서 HTTP 및 HTTPS를 사용 하 여 응용 프로그램 패키지를 App-v 클라이언트에 스트리밍하는 프로토콜을 사용할 수 있습니다. 이 옵션을 사용 하면 조직에서 IIS가 일반적으로 제공 하는 추가 확장성을 활용할 수 있습니다. IIS를 스트리밍 서버로 사용할 때 HTTP 대신 HTTPS를 사용 하 여 클라이언트와 서버 간의 통신을 보호할 수 있습니다.

**참고**  파일 서버에서 응용 프로그램을 스트림할 경우 응용 프로그램 패키지에 대 한 통신의 보안을 강화 해야 합니다. 이는 IPsec을 사용 하 여 달성할 수 있습니다. 자세한 내용은 TechNet 라이브러리의 다음 항목을 참조 하세요.

-   Windows Server2003의 경우 <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Windows Server 2008의 경우 <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## MIME 형식


IIS를 사용 하 여 가상 응용 프로그램을 HTTP 또는 HTTPS로 스트리밍할 때 App-v를 지원 하려면 다음 MIME 형식을 IIS 서버에 추가 해야 합니다.

-   . OSD = TXT

-   . SFT = Binary

MIME 형식 추가에 대 한 지침으로 다음 KB 문서를 사용 합니다.

IIS 6.0: <https://go.microsoft.com/fwlink/?LinkId=151973>

IIS 7.0: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Kerberos 인증


HTTP 또는 HTTPS 및 Kerberos 인증을 사용 하 여 .ICO, OSD 또는 SFT 파일을 스트리밍하는 경우 사용자 환경의 보안이 향상 됩니다. 그러나 IIS에서 Kerberos 인증을 지원 하려면 올바른 SPN (서비스 사용자 이름)을 구성 해야 합니다. 이 `setspn.exe` 도구는 Windows Server2003에서 설치 CD의 지원 도구를 통해 사용할 수 있으며 Windows Server2008에 기본으로 제공 됩니다.

SPN을 만들려면 `setspn.exe` 도메인 관리자의 구성원으로 로그인 한 상태에서 명령 프롬프트에서 실행 합니다 (예:) `setspn.exe –A HTTP/FQDN of Server ServerName` .

## 관련 항목


[보안 통신 사후 설치를 위해 Management Server 또는 Streaming Server 구성](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





