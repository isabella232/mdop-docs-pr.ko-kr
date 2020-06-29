---
title: 서버 보안 계획
description: 서버 보안 계획
author: dansimp
ms.assetid: c7cd8227-b359-41e7-a8ae-d0d5718a76a2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bea1bd8287a15385200bbfb425ed8e00fbcdb02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815903"
---
# 서버 보안 계획


환경의 보안을 강화 하려면 환경에서 발생할 수 있는 위협에 대 한 노출을 확인 해야 합니다. App-v 인프라에 대 한 보안을 제공 하려면 특정 App-v 보안 기능 뿐만 아니라 기본 인프라에 대 한 보안 방법 및 기능을 사용 해야 합니다. IIS (인터넷 정보 서비스), Active Directory 도메인 서비스 및 SQL Server와 같은 서비스에 대 한 기본 인프라를 보호 하면 App-v 시스템의 전체 보안이 향상 됩니다.

서버 설치의 기본 설정은 가장 높은 수준의 보안을 제공 합니다. 그러나 일부 구성 요소는 설치의 일부로 구성 되지 않은 기본 인프라를 사용 합니다. 설치 후 단계에 따라 App-v 인프라의 보안을 향상 시킬 수 있습니다.

콘텐츠 디렉터리에는 클라이언트로 스트리밍할 모든 패키지가 포함 됩니다. 이러한 리소스는 최대한 많은 보안 위험을 방지 하기 위해 최대한 안전 해야 합니다. 다음 목록에서는 몇 가지 추가 지침을 제공 합니다.

-   UNC 기반 게시 및/또는 스트리밍 —이 항목에 대 한 사용 권한은 환경에서 가장 제한적 이어야 합니다. NTFS 권한을 사용 하 여 콘텐츠 디렉터리에 대 한 가장 제한적인 Acl (액세스 제어 목록)을 구현 합니다 (사용자 = 읽기, 관리자 = 읽기 및 쓰기).

-   게시 및/또는 스트리밍을 위해 사용 되는 IIS-Windows 통합 인증만 지원 하도록 IIS를 구성 합니다. IIS 서버에 대 한 익명 액세스를 제거 하 고 NTFS 권한을 사용 하 여 디렉터리에 대 한 액세스를 제한 합니다.

-   RTSP/RTSPS for stream 응용 프로그램 패키지-인증을 요구 하도록 App-v 공급자 정책을 구성 하 고, 액세스 권한을 적용 하 고, 필요한 그룹만 공급자 정책에 액세스할 수 있도록 설정 합니다. 데이터베이스에서 적절 한 사용 권한을 사용 하 여 응용 프로그램을 구성 합니다.

관리자 권한을 가진 사용자 수를 최소로 유지 하 여 데이터 저장소의 데이터에 대 한 위협 가능성을 줄이고 악의적인 응용 프로그램을 인프라에 게시 하지 않도록 합니다.

## Application Virtualization 보안


App-v는 인프라의 다양 한 구성 요소 간에 여러 통신 방법을 사용 합니다. App-v 인프라 계획을 수립할 때 서버 간 통신을 보호 하면 기존 네트워크에 이미 존재 하는 보안 위험을 줄일 수 있습니다.

### 데이터 저장소

응용 프로그램 가상화 관리 서버 및 응용 프로그램 가상화 관리 서비스는 TCP 포트 1433를 통해 SQL 연결을 사용 하 여 데이터 저장소와 통신 합니다. 관리 서버는 데이터 저장소를 사용 하 여 응용 프로그램 및 구성 데이터를 검색 하 고 데이터베이스에 사용 정보를 기록 합니다. 관리 서비스는 App-v 인프라를 구성 하는 관리자를 대신 하 여 데이터 저장소와 통신 합니다. 데이터 저장소에 중요 한 정보가 포함 되어 있기 때문에이 데이터에 대 한 위협을 최소화 하는 것이 중요 합니다.

앱-V 관리 서버, 관리 서비스 및 데이터 저장소 간 통신은 IPsec (인터넷 프로토콜 보안)을 사용 하 여 보호 하는 것이 좋습니다. 특히 데이터 저장소 (SQL)와 관리 서버 및 데이터 저장소와 관리 서비스 간의 통신 채널을 보호 하는 정책을 만듭니다. IPsec으로 서버 및 도메인 격리를 배포 하 여 모든 App-v 인프라 구성 요소가 보안 채널을 통해서만 통신 하도록 할 수도 있습니다. IPsec을 구현 하는 방법에 대 한 자세한 내용은 다음 문서를 참조 하세요.

-   Windows Server2003의 경우 <https://go.microsoft.com/fwlink/?LinkId=133226> (()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=133226) .

-   Windows Server2008의 경우 <https://go.microsoft.com/fwlink/?LinkId=133227> (()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=133227) .

### 콘텐츠 디렉터리

App-v 관리 서버 설치는 콘텐츠 디렉터리의 위치를 구성 합니다. 이 디렉터리는 가상화 된 응용 프로그램 패키지의 저장소 위치입니다. 이 위치를 서버에 로컬로 설정 하거나 원격 네트워크 공유에 배치할 수 있습니다. 따라서 콘텐츠 디렉터리에 대 한 원격 위치와의 통신을 보호 하기 위해 IPsec을 구현 합니다.

IIS 서버의 가상 디렉터리를 사용 하 여 패키지를 클라이언트로 스트리밍할 수도 있습니다. 콘텐츠에 대해 만든 가상 디렉터리가 원격 원본에 있는 경우 IPsec을 사용 하 여 IIS 서버와 원격 저장소 위치 간의 통신을 보호할 수 있습니다.

콘텐츠 디렉터리에는 클라이언트로 스트리밍된 모든 패키지가 포함 됩니다. 이러한 리소스는 최대한 많은 보안 위험을 방지 하기 위해 최대한 안전 해야 합니다.

### 보안 프로토콜

향상 된 보안 통신을 위해 RTSPS 또는 HTTPS를 사용할 수 있습니다. RTSPS는 App-v 서버에서 사용 되는 프로토콜 이며, HTTPS는 IIS 서버에서 사용 하는 프로토콜입니다. 이러한 프로토콜은 서버에서 응용 프로그램 가상화 데스크톱 클라이언트로 응용 프로그램을 게시할 때 사용 됩니다. 원하는 프로토콜을 확인 한 후 해당 프로토콜을 사용 하는 게시 서버를 추가 합니다.

### <a href="" id="configuring-app-v-servers-for-rtsps-"></a>RTSPS 용 App-v 서버 구성

향상 된 보안을 사용 하도록 App-v 관리 서버 또는 스트리밍 서버를 설치 또는 구성 (예: TLS) 하려면 x.509 V3 인증서가 App-v Server에 프로비저닝 되어야 합니다. 서버에 대 한 보안을 설치 하거나 구성 하려고 준비 하는 경우 몇 가지 특정 요구 사항을 충족 해야 합니다. 더욱 안전한 App-v 관리 서버 또는 스트리밍 서버에 대 한 인증서를 배포 하 고 구성 하는 데 필요한 기술 요구 사항은 다음과 같습니다.

-   인증서가 유효 해야 합니다. 그렇지 않으면 클라이언트가 연결을 종료 합니다.

-   인증서에는 올바른 EKU (확장 된 키 사용)-서버 인증 (OID 1.3.6.1.5.5.7.3.1)이 포함 되어야 합니다. 그렇지 않으면 클라이언트가 연결을 종료 합니다.

-   인증서의 FQDN (정규화 된 도메인 이름)이 설치 된 서버와 일치 해야 합니다. 예를 들어 클라이언트가 호출 `RTSPS://Myserver.mycompany.com/content/MyApp.sft` 되지만 인증서 **발급 대상** 필드에는 `Myserver1.mycompany.com` 클라이언트가 서버에 연결 되지 않고 `Myserver.mycompany.com` `Myserver1.mycompany.com` 동일한 IP 주소를 확인 하는 경우에도 세션이 종료 됩니다.

    **참고**  네트워크 부하 분산 클러스터에서 App-v를 사용 하는 경우 RTSPS를 지원 하기 위해 *주체 대체 이름* (san)으로 인증서를 구성 해야 합니다. CA (인증 기관)를 구성 하 고 San을 사용 하 여 인증서를 만드는 방법에 대 한 자세한 내용은 (을 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=133228> https://go.microsoft.com/fwlink/?LinkId=133228) .

     

-   인증서를 App-v 서버에 발급 하는 CA는 서버에 연결 하는 클라이언트가 신뢰 해야 합니다. 그렇지 않으면 클라이언트가 연결을 종료 합니다.

-   서버 App-v 서비스에서 액세스를 사용 하도록 *인증서 개인 키* 에 대 한 사용 권한을 변경 해야 합니다. 기본적으로 App-v 관리 서버와 스트리밍 서버 서비스는 네트워크 서비스 계정으로 실행 됩니다. 서버에서 PKCS \ #10이 생성 되 면 개인 키가 만들어집니다. 로컬 시스템 및 관리자 그룹만이 키에 액세스할 수 있습니다. 이러한 기본 Acl을 통해 App-v 서버는 보안 연결을 수락 하지 않습니다.

    **참고**  PKI (공개 키 인프라)를 구성 하는 방법에 대 한 자세한 내용은 (을 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=133229> https://go.microsoft.com/fwlink/?LinkId=133229) .

     

### HTTPS를 사용 하 여 IIS 서버 구성

앱-V는 특정 인프라 구성에서 IIS 서버를 사용할 가능성이 있습니다. IIS 서버를 구성 하는 방법에 대 한 자세한 내용은 <https://go.microsoft.com/fwlink/?LinkId=133230> (()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=133230) .

**참고**  IIS를 사용 하 여 .ICO 및 OSD 파일을 게시 하는 경우 OSD = TXT에 대 한 MIME 형식을 구성 합니다. 그렇지 않은 경우에는 IIS가 .ICO 및 OSD 파일을 클라이언트에 제공 하는 것을 거부 합니다.

 

### 응용 프로그램 수준 보안

특정 응용 프로그램을 사용자의 데스크톱에 스트리밍하는 서버를 구성할 수 있습니다. 그러나 access 권한은 응용 프로그램 수준이 아니라 패키지 수준에서 부여 됩니다. 특정 응용 프로그램은 사용자의 데스크톱에 게시 되지 않을 수 있지만, 사용자가 응용 프로그램을 추가할 수 있는 권한이 있거나 클라이언트 컴퓨터의 관리자 인 경우 사용자는 클라이언트의 바로 가기를 만들고 사용 하 여 패키지의 모든 응용 프로그램을 실행할 수 있습니다.

## 분산된 환경에 대한 App-V 관리 구성


특정 조직의 인프라를 설계할 때 app-v 관리 서버를 설치 하는 컴퓨터 이외의 컴퓨터에 App-v 관리 웹 서비스를 설치할 수 있습니다. 이러한 App-v 구성 요소를 구분 하는 일반적인 이유는 다음과 같습니다.

-   성능

-   안정성

-   가용성

-   확장성

App-v 관리 콘솔, 관리 서버 및 관리 웹 서비스를 분리 하 여 인프라가 올바르게 작동 하 게 하려면 추가 구성이 필요 합니다. 서버를 구성 하는 방법에 대 한 자세한 내용은 [위임용으로 트러스트 되도록 서버를 구성 하는 방법을](how-to-configure-the-server-to-be-trusted-for-delegation.md)참조 하세요.

## 관련 항목


[보안 및 보호 계획](planning-for-security-and-protection.md)

 

 




