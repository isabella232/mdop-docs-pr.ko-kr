---
title: App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)
description: App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817943"
---
# App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)


Microsoft Application Virtualization (App-v) 4.6에서 클라이언트가 공유 읽기 전용 캐시 사용을 지원 합니다. 공유 읽기 전용 캐시는 클라이언트가 VDI (가상 데스크톱 인프라) 시스템에서 디스크 공간을 효율적으로 사용할 수 있도록 하며,이는 사용자가 데이터 센터 서버 환경에서 호스트 되는 VM (가상 컴퓨터)에서 응용 프로그램을 실행 하 고 SAN (저장 영역 네트워크)에서 네트워크 저장소를 공유 하는 것입니다. 다음 절차에서는 "풀링된 VM" 또는 "정적 VM" 이라고 하는 기본 VDI 아키텍처 중 하나에서 App-v 클라이언트를 구현 하는 데 필요한 프로세스의 개요를 제공 합니다. 이는 App-v 시스템 및 해당 구성 요소에 대 한 계획, 배포 및 운영 및 VDI 서버의 작업 및 관리에 익숙한 것으로 가정 합니다. App-v에 대 한 자세한 내용은 [응용 프로그램 가상화](https://go.microsoft.com/fwlink/?LinkId=122939) 를 참조 하세요 (https://go.microsoft.com/fwlink/?LinkId=122939)

**참고**  이 절차에 설명 된 세부 정보는 예제로만 제공 됩니다. 다른 방법을 사용 하 여 전체 프로세스를 완료할 수 있습니다.

 

## VDI 시나리오에서 App-v 클라이언트 배포


모든 사용자에 게 필요한 모든 응용 프로그램으로 채워진 공유 읽기 전용 캐시를 사용 하 여 VDI 시나리오에서 App-v 클라이언트를 배포할 수 있습니다. 그런 다음 모든 App-v 클라이언트가 동일한 캐시 파일을 사용 하도록 VDI 마스터 VM 이미지를 구성 합니다. 사용자에 게 App-v 게시 프로세스를 사용 하 여 특정 응용 프로그램에 대 한 액세스 권한이 부여 됩니다. 캐시가 이미 모든 응용 프로그램을 사용 하 여 미리 로드 되었으므로 사용자가 응용 프로그램을 시작할 때 스트리밍이 발생 하지 않습니다. 그러나 캐시를 미리 채우는 데 사용 되는 패키지는 RTSP (실시간 스트리밍 프로토콜) 스트리밍을 지 원하는 App-v 서버에 보관 하 고 App-v 클라이언트에 대 한 액세스 권한을 부여 해야 합니다. App-v 관리 서버를 사용 하 여 응용 프로그램을 게시 하는 경우이 스트리밍 함수를 제공 하는 데 사용할 수 있습니다.

배포 프로세스는 네 가지 주요 작업으로 구성 됩니다.

-   마스터 공유 캐시 파일 만들기 및 채우기

-   VDI server 저장소에 공유 캐시 파일 복사

-   VDI 마스터 이미지에서 App-v 클라이언트 소프트웨어 구성

-   초기 배포 후 공유 캐시 파일의 업데이트 배포 주기 관리

이러한 작업에는 신중한 계획이 필요 합니다. 조직에서 팔 로우 하는 체계적이 고 재현할 수 있는 프로세스를 준비 하 고 문서화 하는 것이 좋습니다. 이는 마스터 공유 캐시 파일의 초기 준비 및 배포, 각각 마스터 공유 캐시에 대 한 업데이트를 필요로 하는 응용 프로그램 업데이트의 지속적인 관리에 특히 중요 합니다. 다음 절차를 사용 하 여 이러한 기본 작업을 완료할 수 있습니다.

**참고**  여러 가지 메서드를 사용 하 여 응용 프로그램을 게시할 수 있지만, 다음 절차는 게시를 위한 App-v Management Server의 사용에 기반을 둔 것입니다.

 

**풀링된 VM VDI 또는 정적 VM VDI 시나리오에서 초기 배포에 대 한 읽기 전용 캐시를 구성 하려면**

1. VDI 서버의 VM에서 앱 V 관리 서버를 설정 하 고 구성 하 여 사용자 인증 및 게시 지원을 제공 합니다.

2. 모든 사용자에 게 필요한 모든 응용 프로그램 패키지를 사용 하 여이 관리 서버의 콘텐츠 폴더를 채웁니다.

3. App-v 클라이언트가 설치 된 준비 컴퓨터를 설정 합니다. 모든 응용 프로그램에 대 한 액세스 권한이 있는 계정을 사용 하 여 스테이징 컴퓨터에 로그온 한 다음 전체 응용 프로그램 집합을 컴퓨터에 게시 하 고 응용 프로그램을 스트리밍 하 여 캐시 하 여 완전히 로드 되도록 합니다.

   **중요**  
   준비 컴퓨터는 App-v 클라이언트가 실행 되는 Vm에서 사용 하는 것과 동일한 운영 체제 유형 및 시스템 아키텍처를 사용 해야 합니다.

     

4. 안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않도록 하 여 캐시 파일을 잠급니다.

   **참고**  
   또는 응용 프로그램 가상화 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다. 파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.

     

5. 모든 Vm이 액세스할 수 있는 VDI 서버의 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더). 폴더 액세스 권한을 모든 사용자 그룹에 대해 읽기 전용으로 설정 하 고 캐시 파일 업데이트를 관리 하는 관리자에 대해 모든 권한으로 제어 합니다. 캐시 파일의 위치는 registry AppFS\\FileName.에서 얻을 수 있습니다.

   **중요**  
   FSD 파일은 로컬에 연결 된 저장소 성능 (예: SAN)과 응답성과 신뢰도가 같은 위치에 두어야 합니다.

     

6. VDI 마스터 VM 이미지에 App-v 데스크톱 클라이언트를 설치한 다음, 클라이언트의 AppFS 키에 다음 레지스트리 키 값을 추가 하 여 읽기 전용 캐시를 사용 하도록 구성 합니다. AppFS 키는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.에 있습니다.

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">키</th>
   <th align="left">유형</th>
   <th align="left">값</th>
   <th align="left">목적</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>문자열</p></td>
   <td align="left"><p>FSD 경로</p></td>
   <td align="left"><p>공유 캐시 파일의 경로를 지정 합니다 (예: \VDIServername\Sharefolder\SFTFS.). FSD (필수).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>raid-1</p></td>
   <td align="left"><p>클라이언트가 읽기 전용 모드로 작동 하도록 구성 합니다. 이렇게 하면 클라이언트가 패키지 캐시에 대 한 업데이트 스트리밍을 시도 하지 않습니다. (필수)</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>문자열</p></td>
   <td align="left"><p>오류 로그 (.etl) 파일 경로</p></td>
   <td align="left"><p>오류 로그 경로를 지정 하는 데 사용 되는 항목입니다. 권장. C:\Logs\Sftfs.etl 같은 로컬 경로를 사용 합니다.</p></td>
   </tr>
   </tbody>
   </table>

     

7. 게시 서버를 사용 하 고 로그온 할 때 게시 새로 고침을 사용 하도록 마스터 VM 이미지 클라이언트를 구성 합니다. 사용자가 VDI 시스템에 로그온 하 고 해당 VM이 마스터 VM 이미지에서 빌드되기 때문에 게시 새로 고침 주기가 발생 하 고 계정이 승인 된 모든 응용 프로그램을 게시 합니다. 이러한 응용 프로그램은 공유 캐시에서 실행 됩니다.

**풀링된 VM 시나리오에서 패키지 업그레이드에 맞게 클라이언트를 구성 하려면**

1.  응용 프로그램 패키지의 업그레이드 및 테스트를 완료 합니다.

2.  앱-V 서버에서 패키지를 업그레이드 합니다. 그런 다음 새 버전의 응용 프로그램을 스테이징 컴퓨터의 클라이언트에 게시 하 고 스트리밍 하 여 완전히 캐시에 로드 합니다.

3.  안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않았는지 확인 합니다.

    **참고**  또는 services.msc에서 Application Virtualization 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다. 파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.

     

4.  모든 Vm이 액세스할 수 있는 VDI 서버의 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더). 다른 파일 이름을 사용할 수 있습니다 (예: SFTFS \ _V2). 새 버전을 구분 하는 FSD.

5.  업데이트 된 공유 캐시 파일을 사용 하도록 VDI 마스터 VM 이미지에서 App-v 데스크톱 클라이언트를 구성 하려면 업데이트 된 파일의 위치 (예: \\\\VDIServername\\Sharefolder\\SFTFS\ _V2를 가리키도록 AppFS 레지스트리 키 파일 이름 값을 변경 합니다. FSD. 사용자가 로그 오프 한 다음 다시 로그온 하면 업데이트 된 마스터 이미지를 사용 하 여 새 VM이 생성 됩니다. 모든 사용자 설정은 유지 되며 새 VM에 적용 됩니다. 그런 다음 업데이트 된 응용 프로그램에 액세스할 수 있습니다.

**정적 VM 시나리오에서 패키지 업그레이드에 맞게 클라이언트를 구성 하려면**

1.  응용 프로그램 패키지의 업그레이드 및 테스트를 완료 합니다.

2.  앱-V 서버에서 패키지를 업그레이드 합니다. 그런 다음 응용 프로그램이 캐시에 완전히 로드 되도록 새 버전의 응용 프로그램을 스테이징 컴퓨터의 클라이언트에 게시 하 고 스트리밍합니다.

3.  안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않았는지 확인 합니다.

    **참고**  또는 services.msc에서 Application Virtualization 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다. 파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.

     

4.  모든 Vm이 액세스할 수 있는 VDI 서버의 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더). 다른 파일 이름을 사용할 수 있습니다 (예: SFTFS \ _V2). 새 버전을 구분 하는 FSD.

5.  업데이트 된 공유 캐시 파일을 사용 하도록 VDI 마스터 VM 이미지에서 App-v 데스크톱 클라이언트를 구성 하려면 업데이트 된 파일의 위치 (예: \\\\VDIServername\\Sharefolder\\SFTFS\ _V2를 가리키도록 AppFS 레지스트리 키 파일 이름 값을 변경 합니다. FSD. 이렇게 하면 새 사용자가 새 버전을 받을 수 있습니다.

6.  AppFS 키 파일 이름 값을 편집 하 여 \\\\VDIServername\\Sharefolder\\SFTFS\ _V2와 같은 업데이트 된 캐시의 위치로 설정 하는 스크립트를 만듭니다. FSD. 이 스크립트는 사용자가 로그 오프할 때 (예: 그룹 정책 설정을 사용 하 여) App-v 클라이언트 드라이버가 시작 되기 전에 실행 되도록 구성 합니다. 사용자가 로그 오프 한 다음 다시 로그온 하면 기존 VM이 업데이트 되 고 캐시의 업데이트 된 복사본을 사용 하 게 됩니다. 업데이트 된 응용 프로그램에 액세스할 수 있습니다.

## 캐시를 업그레이드할 때 기호화 된 링크를 사용 하는 방법


새 또는 업그레이드 된 패키지를 포함 하는 새 캐시 파일이 배포 될 때마다 AppFS 키 파일 이름 값을 수정 하는 대신 Windows Vista, Windows 7 및 Windows Server 2008의 운영 체제에서 기호화 된 링크를 사용할 수 있습니다. 기호화 된 링크에 대 한 자세한 내용은 [기호화 된 링크](https://go.microsoft.com/fwlink/?LinkId=157626) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=157626) . 반대로, Windows XP는 심볼 링크의 사용을 지원 하지 않으며 대신 연결 지점을 사용 해야 합니다. 연결에 대 한 자세한 내용은 Microsoft 기술 자료 [문서 205524](https://go.microsoft.com/fwlink/?LinkId=182553) ( https://go.microsoft.com/fwlink/?LinkId=182553) 및 도구 [연결 v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=182554) .

**캐시를 참조 하도록 기호화 된 링크를 구성 하려면**

1.  초기 배포 단계에서 명령 프롬프트 창을 VDI 서버 호스트 운영 체제의 로컬 관리자로 엽니다.

2.  MKLINK 명령을 사용 하 여 기호화 된 링크를 만든 다음 Sftfs. fsd 파일을 가리키도록 구성 합니다.

    **     mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd**

3.  VDI 마스터 VM 이미지에서 **관리자 권한으로 실행** 옵션을 사용 하 여 명령 프롬프트 창을 열고 VM이 VDI 호스트 운영 체제의 기호화 된 링크에 액세스할 수 있도록 원격 링크 사용 권한을 부여 합니다. 기본적으로 원격 링크 사용 권한은 비활성화 되어 있습니다.

    **fsutil behavior set SymlinkEvaluation R2R: 1**

    **참고**  저장소 서버에서 적절 한 링크 사용 권한을 사용 하도록 설정 해야 합니다. 링크 위치 및 Sftfs. fsd 파일에 따라 사용 권한은 **L2L: 1** 또는 **L2R: 1** 또는 **R2L: 1** 또는 **R2R: 1**입니다.

     

4.  VDI 마스터 VM 이미지에서 App-v 데스크톱 클라이언트를 구성할 때 AppFS 키 파일 이름 값을 기호화 된 링크를 사용 하는 FSD 파일의 UNC 경로와 동일 하 게 설정 합니다. 예를 들어 \\\\VDIHostserver\\Symlinkname.로 설정 합니다. App-v 클라이언트가 먼저 캐시에 액세스 하면 기호화 된 링크가 클라이언트에 캐시 파일에 대 한 핸들을 전달 합니다. 클라이언트가 실행 되는 동안에는 클라이언트가 계속 해당 핸들을 사용 합니다. 기존 클라이언트에 이전 공유 캐시가 열려 있는 경우에도 기호화 된 링크의 값을 안전 하 게 업데이트할 수 있습니다.

5.  패키지를 업그레이드 하거나 캐시에 새 패키지를 추가 해야 하는 경우 정적 VM 또는 풀링된 VM 시나리오에 대 한 업그레이드 절차의 1 ~ 5 단계를 수행 합니다. 그런 다음 심볼 링크를 삭제 하 고 다시 만들어서 새 버전의 공유 캐시 파일을 가리킵니다. Vm이 업데이트 된 심볼 링크를 포함 하는 경로를 사용 하기 때문에, VM이 다시 시작 되 면 클라이언트는 업데이트 된 캐시 복사본에 대 한 핸들을 받습니다. 그런 다음 사용자가 새 응용 프로그램 및 업데이트 된 애플리케이션을 액세스할 수 있습니다.

## 관련 항목


[Application Virtualization Management Server 설치 방법](how-to-install-application-virtualization-management-server.md)

[Application Virtualization Client를 수동으로 설치하는 방법](how-to-manually-install-the-application-virtualization-client.md)

[명령줄을 사용하여 클라이언트를 설치하는 방법](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





