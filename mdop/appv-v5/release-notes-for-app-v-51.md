---
title: App-V 5.1 릴리스 정보
description: App-V 5.1 릴리스 정보
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813308"
---
# App-V 5.1 릴리스 정보


다음은 Microsoft Application Virtualization (App-v) 5.1의 알려진 문제점입니다.

## Windows 10에서 App-v 5.0 SP3 관리 서버 및 App-v 5.1 클라이언트 간 새로 고침을 게시 하는 동안 오류가 발생 합니다.


앱-V 5.0 SP3 관리 서버에서 Windows 10의 App-v 5.1 클라이언트에 패키지를 동기화 하는 경우 게시 새로 고침 중 오류가 발생 합니다. 이 오류는 App-v 5.0 SP3 서버에서 게시 URL에 지정 된 Windows 10 운영 체제를 인식 하지 못하기 때문에 발생 합니다. 이 문제는 App-v 5.1 게시 서버에 대해 해결 되었지만 App-v 5.0 SP3 또는 이전 버전으로 이식할 수 없습니다.

**해결 방법**: 앱 v 5.0 관리 서버를 Windows 10 클라이언트용 App-v 5.1 관리 서버로 업그레이드 합니다.

## App-v 5.1 서버를 사용 하 여 설정 하는 경우 전역으로 게시 되는 패키지에 대해 사용자 지정 구성이 적용 되지 않습니다.


컴퓨터 계정이 포함 된 광고 그룹에 패키지를 할당 하 고 App-v 서버를 사용 하 여 사용자 지정 구성을 해당 그룹에 적용 하는 경우 사용자 지정 구성이 해당 컴퓨터에 적용 되지 않습니다. App-v 5.1 클라이언트는 컴퓨터 계정에 할당 된 패키지를 전역적으로 게시 합니다. 그러나 각 사용자의 프로필에 사용자 당 사용자 지정 구성 파일을 저장 합니다. 전역 게시 된 패키지는이 사용자 지정 구성에 액세스할 수 없습니다.

**해결 방법**: 다음 중 하나를 수행 합니다.

-   사용자 계정만 포함 하는 그룹에 패키지를 할당 합니다. 이렇게 하면 패키지의 사용자 지정 구성이 각 사용자의 프로필에 저장 되므로 올바르게 적용 됩니다.

-   사용자 지정 배포 구성 파일을 만들고 – DynamicDeploymentConfiguration 매개 변수를 사용 하 여 AppvClientPackage cmdlet을 사용 하 여 클라이언트의 패키지에 적용 합니다. 자세한 내용은 [앱-V 5.1 동적 구성을](about-app-v-51-dynamic-configuration.md) 참조 하세요.

-   앱-V 5.1 시퀀서를 사용 하 여 사용자 지정 구성으로 새 패키지를 만듭니다.

## 새 앱-V 5.1 서버 설치 후에 서버 파일이 삭제 되지 않음


App-v 5.0 SP1 서버를 제거한 다음 App-v 5.1 서버를 설치 하면 설치에 실패 하 고 잘못 된 버전의 관리 서버를 설치 하 고 오류 메시지가 반환 됩니다. 이 문제는 App-v 5.0 SP1을 제거할 때 서버 파일이 삭제 되지 않기 때문에 발생 하므로 설치 프로세스가 새 설치 대신 업그레이드를 수행 합니다.

**해결 방법**:이 레지스트리 키를 삭제 한 후에 앱-V 5.1 설치를 시작 합니다.

HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall에서 값 데이터 "Microsoft Application Virtualization (App-v) Server"를 사용 하 여 DWORD 값 "DisplayName"이 포함 된 설치 GUID 키를 찾아 삭제 합니다. 삭제 해야 하는 유일한 키입니다.

## 수동으로 추가 된 파일 형식 연결이 올바르게 저장 되지 않음


응용 프로그램 업그레이드 마법사 종료 시 바로 가기 키 및 FTAs 탭을 사용 하 여 수동으로 응용 프로그램 패키지에 추가 된 파일 형식 연결이 올바르게 저장 되지 않았습니다. 저장 된 패키지를 다시 업데이트 하는 경우에는 App-v 클라이언트 또는 시퀀서에서 사용할 수 없습니다.

**해결 방법**: 파일 형식 연결을 추가 하려면 수정할 패키지를 열고 업데이트 마법사를 실행 합니다. 설치 단계에서 운영 체제를 통해 새 파일 형식 연결을 추가 합니다. 시퀀서는 시스템 레지스트리에서 새 연결을 검색 하 고 패키지의 가상 레지스트리에 추가 하 여 클라이언트에서 사용할 수 있게 됩니다.

## SCS (공유 콘텐츠 저장소) 모드의 패키지를 AppLocker와 함께 관리 되는 클라이언트에 스트리밍하는 경우, 추가 데이터는 로컬 디스크에 기록 됩니다.


클라이언트의 로컬 디스크에 기록 되는 데이터의 양을 줄이려면 App-v 5.1 클라이언트에서 SCS 모드를 사용 하도록 설정 하 여 요청 시 패키지의 콘텐츠를 스트리밍할 수 있습니다. 그러나 AppLocker에서 패키지 내의 응용 프로그램을 관리 하는 경우 일부 데이터가 해당 클라이언트의 로컬 디스크에 기록 되지 않을 수 있습니다.

**해결 방법**: 없음

## 관리 콘솔 패키지 추가 대화 상자에서 Chrome 또는 Firefox를 사용 하는 경우에는 찾아보기 단추를 사용할 수 없습니다.


관리 콘솔의 패키지 페이지에서 오른쪽 아래 모서리에 있는 **추가 또는 업그레이드** 를 클릭 하면 **패키지 추가** 대화 상자가 나타납니다. Chrome 또는 Firefox를 사용 하 여 관리 콘솔에 액세스 하는 경우에는 패키지의 위치로 이동할 수 없습니다.

**해결 방법**: 패키지의 경로를 입력 하거나 복사 하 여 Package input **추가** 필드에 붙여 넣습니다. 관리 콘솔에이 경로에 대 한 액세스 권한이 있는 경우 패키지를 추가할 수 있게 됩니다. 패키지가 네트워크 공유에 있는 경우 다음 단계를 수행 하 여 파일 탐색기를 사용 하 여 해당 위치로 이동할 수 있습니다.

1.  **Shift**키를 누른 상태에서 패키지 파일을 마우스 오른쪽 단추로 클릭 합니다.

2.  **경로로 복사** 선택

3.  **패키지 추가** 대화 상자의 입력 필드에 경로를 붙여 넣습니다.

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a>"데이터베이스 오류가 발생 했습니다." 라는 메시지와 함께 App-v 관리 서버를 5.1으로 업그레이드 하면 오류가 발생할 수 있습니다.


App-v 5.0 SP1 관리 서버를 설치한 다음 여러 연결 그룹을 구성 하 고 사용할 수 있는 경우 App-v 5.1 서버로 업그레이드 하려고 하면 다음 오류가 표시 됩니다. "데이터베이스 오류가 발생 했습니다. 이유: ' 열 이름 ' PackageOptional '이 잘못 되었습니다. 열 이름 ' VersionOptional '이 잘못 되었습니다.

**해결 방법**: SQL 데이터베이스에서 다음 명령을 실행 합니다.

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

여기서 "AppVManagement"는 데이터베이스의 이름입니다.

## 선택적 패키지를 추가 하거나 제거 하는 경우 사용자가 게시 된 연결 그룹에서 패키지를 열 수 없음


RDS 클라이언트를 실행 중이거나 컴퓨터당 여러 명의 동시 사용자가 있는 환경에서는 연결 그룹에 선택적 패키지가 추가 되거나 제거 되는 경우 로그인 한 사용자가 사용자가 게시 한 연결 그룹의 패키지에서 응용 프로그램을 열 수 없습니다.

**해결 방법**: 사용자가 로그 아웃 한 다음 다시 로그인 하도록 합니다.

## 연결 그룹이 사용자 에게만 게시 되 면 오류 메시지가 실수로 표시 됨


AppvClientConnectionGroup를 실행 하면 연결 그룹이 사용자 에게만 게시 된 경우에도 다음 오류가 표시 됩니다. "내부 앱-V 통합 오류: 사용자에 게 패키지가 통합 되지 않았습니다. 패키지가 컴퓨터에 추가 되 고 사용자에 게 게시 되었는지 확인 하십시오. "

**해결 방법**: 다음 중 하나를 수행 합니다.

-   연결 그룹의 모든 패키지를 게시 합니다.

    복구 되는 연결 그룹에 사용자가 없거나 사용할 수 없는 패키지 (즉, 전역 또는 사용자에 게 게시 되지 않은 경우)가 발생 합니다. 그러나 모든 연결 그룹의 패키지를 사용할 수 있는 경우에는 복구가 작동 하므로 모든 패키지가 게시 되었는지 확인 합니다.

-   AppvClientConnectionGroup 명령을 복구 하는 대신 AppvClientPackage 명령을 사용 하 여 패키지를 개별적으로 복구 합니다.

    사용자가 사용할 수 있는 패키지를 확인 한 다음 각 패키지에 대해 AppvClientPackage 명령을 한 번씩 실행 합니다. PowerShell cmdlet을 사용 하 여 다음을 수행 합니다.

    1.  연결 그룹의 모든 패키지를 가져옵니다.

    2.  각 패키지가 현재 게시 되어 있는지 확인 하십시오.

    3.  패키지가 현재 게시 된 경우 해당 패키지에서 AppvClientPackage를 실행 합니다.

## 시퀀서에 제대로 표시 되지 않는 아이콘


App-v 시퀀서에서 패키지를 수정 하는 경우 바로 가기 및 파일 형식 연결 탭의 아이콘이 올바르게 표시 되지 않습니다. 이 문제는 아이콘의 크기가 16x16 또는 32x32이 아닌 경우에 발생 합니다.

**해결 방법**: 16x16 또는 32x32 아이콘을 사용 합니다.

## 관리 데이터베이스에 더 이상 InsertVersionInfo 스크립트가 필요 하지 않음


App-v 5.0 SP3 보다 이후 버전인 App-v 관리 데이터베이스 버전에는 InsertVersionInfo 스크립트가 필요 하지 않습니다.

사용 권한 .sql 스크립트는 [KB 문서 3031340](https://support.microsoft.com/kb/3031340)의 **2 단계** 에 따라 업데이트 해야 합니다.

**중요** 
 App-v 5.0 SP3 보다 이후 버전의 App-v에는 **1 단계가** 필요 하지 않습니다.

 

## Microsoft Visual Studio 2012 지원 되지 않음


App-v 5.1에서는 Visual Studio 2012을 지원 하지 않습니다.

**해결 방법**: 없음

## App-V 5 x 시퀀서에 대 한 응용 프로그램 파일 이름 제한


App-v 5. x 시퀀서는 파일 이름이 "CO_ x"가 일치 하는 응용 프로그램을 시퀀싱 할 수 없습니다 &lt; &gt; . 여기서 x는 숫자입니다. 오류 0x8007139F이 생성 됩니다.

**해결 방법**: 다른 파일 이름을 사용 합니다.

## 패키지를 탑재할 때 "파일을 찾을 수 없습니다" 오류가 발생 함


패키지를 탑재할 때 "0x80070002 (파일을 찾을 수 없음") 오류가 생성 됩니다. 일반적으로이는 App-v 패키지의 폴더에 여러 개의 파일 (예: 20K 이상)이 포함 되어 있는 경우에 발생 합니다. 이로 인해 스트리밍은 예상 보다 오래 걸리고 "파일을 찾을 수 없습니다." 오류가 발생 하는 시간이 초과 될 수 있습니다.

**해결 방법**: HF06부터이 시간 초과 기간을 연장 하는 데 사용할 새 레지스트리 키가 도입 되었습니다.

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left">경로</td>
<td align="left">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</td>
</tr>
<tr>
<td align="left">설정</td>
<td align="left">StreamResponseWaitTimeout</td>
</tr>
<tr>
<td align="left">메모나</td>
<td align="left">DWORD</td>
</tr>
<tr>
<td align="left">단위</td>
<td align="left">기다립니다</td>
</tr>
<tr>
<td align="left">Default</td>
<td align="left">5mb<br />
<strong>참고 </strong> : 레지스트리 키가 정의 되지 않았거나 값 &lt; = 5가 지정 된 경우이 값이 기본값입니다.
</td>
</tr>
</tbody>
</table>






## 관련 항목


[App-V 5.1 정보](about-app-v-51.md)

 

 





