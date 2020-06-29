---
title: 이전 버전에서 마이그레이션 계획
description: 이전 버전에서 마이그레이션 계획
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815928"
---
# 이전 버전에서 마이그레이션 계획


Microsoft Application Virtualization 4.5 이상 버전으로 업그레이드 하기 전에 4.1 이전 버전을 버전 4.1으로 업그레이드 해야 합니다. 먼저 클라이언트를 업그레이드 한 다음 서버 구성 요소를 업그레이드 해야 합니다. 4.5로 업그레이드 된 클라이언트는 아직 업그레이드 하지 않은 응용 프로그램 가상화 서버와 계속 작동 합니다. 이전 버전의 클라이언트는 4.5로 업그레이드 된 서버에서 지원 되지 않습니다. 시스템 구성 요소를 업그레이드 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 배포 및 업그레이드 고려 사항을](application-virtualization-deployment-and-upgrade-considerations.md)참조 하세요.

마이그레이션을 성공적으로 수행 하기 위해 응용 프로그램 가상화 시스템 구성 요소를 다음 순서로 업그레이드 해야 합니다.

1.  **Microsoft Application Virtualization 클라이언트.** 단계별 업그레이드 지침은 [Application Virtualization 클라이언트를 업그레이드 하는 방법을](how-to-upgrade-the-application-virtualization-client.md)참조 하세요.

2.  **Microsoft Application Virtualization 서버 및 데이터베이스.** 단계별 업그레이드 지침은 [서버 및 시스템 구성 요소를 업그레이드 하는 방법을](how-to-upgrade-the-servers-and-system-components.md)참조 하세요.

    **참고**  둘 이상의 서버에서 Application Virtualization 데이터베이스에 대 한 액세스를 공유 하는 경우에는 데이터베이스를 업그레이드 하는 동안 해당 서버를 모두 오프 라인 상태로 만들어야 합니다. 데이터베이스 업그레이드에 대 한 일반적인 비즈니스 관행을 준수 해야 하지만, 테스트 서버에서 먼저 데이터베이스의 백업 복사본을 사용 하 여 데이터베이스 업그레이드를 테스트 하는 것이 좋습니다. 그런 다음 데이터베이스 스키마를 업그레이드 하는 첫 번째 업그레이드에 대 한 서버 중 하나를 선택 해야 합니다. 프로덕션 데이터베이스가 성공적으로 업그레이드 된 후에는 다른 서버를 업그레이드할 수 있습니다.

     

3.  **Microsoft Application Virtualization 관리 웹 서비스.** 이 단계는 관리 웹 서비스가 별도의 서버에 있는 경우에만 적용 되며, 웹 서비스를 업그레이드 하려면 별도의 서버에서 서버 설치 관리자 프로그램을 실행 해야 합니다. 그렇지 않으면 이전 서버 업그레이드 단계에서 관리 웹 서비스를 자동으로 업그레이드 합니다.

4.  **Microsoft Application Virtualization 관리 콘솔.** 이 단계는 관리 콘솔이 별도의 컴퓨터에 있는 경우에만 적용 되 고 콘솔을 업그레이드 하려면 별도의 컴퓨터에서 서버 설치 관리자 프로그램을 실행 해야 합니다. 그렇지 않은 경우에는 이전 서버 업그레이드 단계에서 관리 콘솔을 업그레이드 합니다.

5.  **Microsoft Application Virtualization Sequencer.** 단계별 지침은 [Application Virtualization Sequencer를 설치 하는 방법을](how-to-install-the-application-virtualization-sequencer.md)참조 하세요. 버전 4.2에 시퀀싱 된 모든 가상 응용 프로그램 패키지는 버전 4.5에서 사용할 수 있도록 다시 시퀀싱 하지 않아도 됩니다. 그러나 기본 Acl (액세스 제어 목록)을 적용 하거나 Windows Installer 파일을 생성 하려면 가상 패키지를 Microsoft Application Virtualization 4.5 형식으로 업그레이드 하는 것이 좋습니다. 이는 간단한 프로세스 이며 4.5 시퀀서를 사용 하 여 기존 가상 응용 프로그램 패키지를 열고 저장할 수만 있어야 합니다. 이는 Application Virtualization Sequencer 명령줄 인터페이스를 사용 하 여 자동화할 수 있습니다.

## <a href="" id="app-v-4-6-client-package-support-"></a>앱-V 4.6 클라이언트 패키지 지원


이전 버전의 App-v 4.6 클라이언트에 만든 패키지를 배포할 수 있습니다. 그러나 적절 한 운영 체제 및 칩 아키텍처 정보가 포함 되도록 관련 된 **.osd** 파일을 수정 해야 합니다. 다음 값을 사용 합니다.

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">OS 값</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;OS 값 = "Win2003TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;OS 값 = "Win2003TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;OS 값 = "Win2008TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;OS 값 = "Win2008TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;OS 값 = "Win2008R2TS64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;OS 값 = "Win7"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;OS 값 = "Win764"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;OS 값 = "WinVista"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;OS 값 = "WinVista64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;OS 값 = "WinXP"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;OS 값 = "WinXP64"/&gt;</p></td>
</tr>
</tbody>
</table>

 

새로 만든 32 비트 패키지를 실행 하려면 App-V 4.6 Sequencer가 설치 된 32 비트 운영 체제를 실행 하는 컴퓨터에서 응용 프로그램을 시퀀싱 해야 합니다. 응용 프로그램을 시퀀싱 한 후에는 시퀀서 콘솔에서 **배포** 탭을 선택한 다음 필요에 따라 적절 한 운영 체제와 칩 아키텍처를 지정 합니다.

**중요**  64 비트 운영 체제를 실행 하는 컴퓨터에서 시퀀싱 된 응용 프로그램은 64 비트 운영 체제를 실행 하는 컴퓨터에 배포 해야 합니다. 새 32-app-v 4.6 Sequencer를 사용 하 여 만든 비트 패키지는 App-v 4.5 클라이언트를 실행 하는 컴퓨터에서 실행 되지 않습니다.

 

App-v 4.6 클라이언트에서 새 64 비트 패키지를 실행 하려면 App-v 4.6 Sequencer를 실행 하는 컴퓨터에서 응용 프로그램을 시퀀싱 하 고 64 비트 운영 체제를 실행 중 이어야 합니다. 응용 프로그램을 시퀀싱 한 후에는 시퀀서 콘솔에서 **배포** 탭을 선택한 다음 필요에 따라 적절 한 운영 체제와 칩 아키텍처를 지정 합니다.

다음 표에는 다양 한 버전의 시퀀서를 사용 하 여 만든 패키지를 실행 하는 클라이언트 버전이 나와 있습니다.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">App-V 4.2 Sequencer를 사용 하 여 시퀀싱</th>
<th align="left">App-V 4.5 Sequencer를 사용 하 여 시퀀싱</th>
<th align="left">32 비트 앱-V 4.6 시퀀서를 사용 하 여 시퀀싱</th>
<th align="left">64 비트 앱-V 4.6 시퀀서를 사용 하 여 시퀀싱</th>
<th align="left">32 비트 앱-V 4.6 SP1 시퀀서를 사용 하 여 시퀀싱</th>
<th align="left">64 비트 앱-V 4.6 SP1 시퀀서를 사용 하 여 시퀀싱</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>4.2 클라이언트</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>아니오</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.5 클라이언트 ¹</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>아니오</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4.6 클라이언트 (32 비트)</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.6 클라이언트 (64 비트)</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4.6 SP1 클라이언트</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니요</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>아니오</p></td>
</tr>
<tr class="even">
<td align="left"><p>4.6 SP1 클라이언트 (64 비트)</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
</tbody>
</table>

 

¹ App-V 4.5, App-v 4.5 CU1 및 App-v 4.5 SP1을 비롯 한 모든 App-v 4.5 클라이언트 버전에 적용 됩니다.

## 추가 마이그레이션 고려 사항


App-v 4.5 시퀀서의 기능 중 하나는 Microsoft 끝점 구성 관리자와 같은 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 가상 응용 프로그램 패키지의 제어 지점으로 Windows Installer 파일 (.msi)을 만드는 기능입니다. Xxx 4.1 또는 4.2 클라이언트에 설치 되어 있으며 이후 4.5로 업그레이드 되는 응용 프로그램 가상화에 대 한 .msi 도구를 사용 하 여 만든 이전 Windows Installer 파일은 4.5 클라이언트에 설치 될 수 없습니다. 그러나 4.5 시퀀서에서 업그레이드 하지 않는 한 제거 하거나 업그레이드할 수 없습니다. 원본 사전 4.5 가상 응용 프로그램 패키지는 4.5 시퀀서에서 열고 Windows Installer 파일로 저장 해야 합니다.

**참고**  App-v 4.2 클라이언트가 4.5로 이미 업그레이드 된 경우 스크립트를 사용 하 여 4.5 클라이언트에서 4.2 패키지를 보존 하 고 관리 하도록 허용할 수 있습니다. 이 스크립트는 msvcp71.dll 및 msvcr71.dll의 두 파일을 App-v 설치 폴더에 복사 하 고 레지스트리 키 \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\] 아래에 다음 레지스트리 키 값을 설정 해야 합니다.

"ClientVersion" = "4.2.1.20"

"GlobalDataDirectory" = "C:\\\\Documents 및 Settings\\\\All Users\\\\Documents\\\\" (전역적으로 쓰기 가능한 위치)

 

App-v 4.5 Sequencer에서 생성 된 Windows Installer 파일은 App-v 4.6 클라이언트에서 실행 하려고 할 때 "이 패키지에 Microsoft Application Virtualization 클라이언트 4.5 이상"이 필요 합니다. 라는 오류 메시지가 표시 됩니다. App-v 4.5 SP1 Sequencer 또는 App-v 4.6 Sequencer를 사용 하 여 이전 패키지를 열고 패키지에 대 한 새 .msi를 생성 합니다.

생성 및 저장 된 모든 4.2 보고서는 서버를 4.5로 업그레이드할 때 덮어쓰여집니다. 이러한 보고서를 유지 해야 하는 경우 서버의 SoftGrid 관리 콘솔 폴더에 있는 SftMMC .msc 파일의 백업 복사본을 저장 하 고 해당 복사본을 사용 하 여 업그레이드 중에 설치 된 새 SftMMC를 대체 해야 합니다.

이전 버전에서 업그레이드 하는 방법에 대 한 자세한 내용은 [Microsoft Application Virtualization 4.5 질문과 대답 ()으로 업그레이드](https://go.microsoft.com/fwlink/?LinkId=120358) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=120358) .

## 관련 항목


[Application Virtualization 시스템 배포 계획](planning-for-application-virtualization-system-deployment.md)

 

 





