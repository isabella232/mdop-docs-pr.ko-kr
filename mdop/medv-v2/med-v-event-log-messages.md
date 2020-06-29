---
title: MED-V 이벤트 로그 메시지
description: MED-V 이벤트 로그 메시지
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823078"
---
# MED-V 이벤트 로그 메시지


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0의 로그 파일에서는 엔터프라이즈에서 MED-V를 배포 하 고 관리 하는 방법에 대 한 자세한 정보를 제공 하 고 기능을 확인 하거나 문제를 해결 하는 데 도움을 줍니다.

## 이벤트 Id


다음은 med-v를 배포 하거나 관리할 때 발생할 수 있는 문제를 해결 하는 데 도움이 되는 MED-V 이벤트 Id의 목록입니다.

### Fts

처음 설치할 때 이벤트 Id를 표시 합니다.

### 이벤트 ID 3066

가상 머신 시작 작업이 실패 했습니다.

<a href="" id="description"></a>**설명**  
MED-V 작업 영역을 만드는 데 사용 하는 VHD (가상 하드 디스크)에 잠재적인 문제가 있습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 용 VHD를 사용 하 여 가상 컴퓨터를 만들 수 있고 시작할 수 있는지 확인 합니다.

### 이벤트 ID 3071

가상 컴퓨터 준비에 실패 했습니다.

<a href="" id="description"></a>**설명**  
다양 한 문제로 인해 처음으로 설정 했을 때 문제가 발생 했습니다. 여기에는 네트워크 연결 문제 등이 포함 됩니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 호스트 에이전트를 다시 시작 하 여 처음 설정으로 다시 실행 합니다.

### 이벤트 ID 3078

가상 컴퓨터 준비에 실패 했습니다.

<a href="" id="description"></a>**설명**  
MED-V 작업 영역을 만드는 데 사용 하는 VHD에 잠재적인 문제가 있습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 용 VHD를 사용 하 여 가상 컴퓨터를 만들 수 있고 시작할 수 있는지 확인 합니다.

### 이벤트 ID 3079

가상 컴퓨터 준비를 다시 시도 합니다.

<a href="" id="description"></a>**설명**  
MED-V가 가상 컴퓨터를 준비 하는 중입니다.

<a href="" id="solution"></a>**해결 방법**  
필요한 작업은 없습니다. 처음 설치를 완료 하도록 합니다.

### 이벤트 ID 3080

가상 컴퓨터를 준비 하는 동안 클라이언트가 중지 되었습니다.

<a href="" id="description"></a>**설명**  
가상 컴퓨터를 준비 하려고 할 때 MED-V가 예기치 않게 중지 됩니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 호스트 에이전트를 시작 하 고 처음 설치를 완료 합니다.

### 이벤트 ID 3084

가상 머신이 유효 하지 않습니다. 처음으로 다시 실행 해야 할 때가 있습니다.

<a href="" id="description"></a>**설명**  
MED-V 호스트 에이전트에서 가상 컴퓨터의 문제를 발견 했습니다.

<a href="" id="solution"></a>**해결 방법**  
필요한 작업은 없습니다. 처음 설치를 완료 하도록 합니다.

### 이벤트 ID 3099

가상 머신을 시작 하기 위해 전화를 걸 수 없습니다.

<a href="" id="description"></a>**설명**  
MED-V 작업 영역을 만드는 데 사용 하는 VHD에 잠재적인 문제가 있습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 용 VHD를 사용 하 여 가상 컴퓨터를 만들 수 있고 열 수 있는지 확인 합니다.

### VM 관리

### 이벤트 ID 4022

VM에 대 한 명령을 실행 하는 동안 VMManagerException 심각한 오류가 발생 했습니다.

<a href="" id="description"></a>**설명**  
최종 사용자가 로그 오프 하거나 MED-V 호스트를 종료 하 여 MED-V를 종료 하려고 했지만 VMTaskTimeout 구성 설정이 초과 되었습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V를 다시 시작 합니다.

### 이벤트 ID 4028

VM 작업 시간이 초과 되었습니다.

<a href="" id="description"></a>**설명**  
최종 사용자가 로그 오프 하거나 호스트를 종료 하 고 VMTaskTimeout 구성 설정을 초과한 경우 MED-V를 종료 하려고 시도 했습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V를 다시 시작 합니다.

### 이벤트 ID 4038

Vmsal에서 사용자에 게 오류 메시지를 게시 했습니다.

<a href="" id="description"></a>**설명**  
최종 사용자에 게 가상 응용 프로그램을 시작할 수 없다는 오류 메시지가 표시 됩니다.

<a href="" id="solution"></a>**해결 방법**  
오류가 한 행에 두 번 이상 기록 되는 경우, MED-V를 중지 하 고 Windows Virtual PC 콘솔을 사용 하 여 가상 컴퓨터에 연결 하 고 응용 프로그램을 전체 화면으로 시작 하려고 시도 합니다.

### 이벤트 ID 4040

TerminalServices가 게스트에서 초기화 되지 않았으므로 추가가 재생 됩니다.

<a href="" id="description"></a>**설명**  
가상 컴퓨터에서 원격 데스크톱 서비스가 초기화 되지 않았으므로 MED-V가 가상 컴퓨터를 다시 부팅 했습니다.

<a href="" id="solution"></a>**해결 방법**  
오류가 한 행에 두 번 이상 기록 되는 경우 MED-V를 중지 하 고 Windows 가상 PC 콘솔을 사용 하 여 가상 컴퓨터에 연결 합니다.

### 이벤트 ID 4042

게스트의 추가를 재활용할 수 없습니다.

<a href="" id="description"></a>**설명**  
MED-V가 가상 컴퓨터에서 가상 컴퓨터 추가 기능을 재활용 하지 못했습니다.

<a href="" id="solution"></a>**해결 방법**  
오류가 한 행에 두 번 이상 기록 되는 경우 MED-V를 중지 하 고 Windows 가상 PC 콘솔을 사용 하 여 가상 컴퓨터에 연결 합니다.

### 이벤트 ID 4043

가상 머신에서 만료 된 암호를 재설정 하지 못했습니다.

<a href="" id="description"></a>**설명**  
최종 사용자가 만료 되기 전에 가상 컴퓨터의 암호를 다시 설정 하지 않았습니다. 따라서 사용자는 네트워크 리소스에 액세스 하거나 작업을 저장 하지 못할 수 있습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 게스트를 종료 하 고 다시 시작 합니다.

### URL 리디렉션

### 이벤트 ID 5005

구성에서 VM 이름을 가져올 수 없습니다. 게스트 브라우저를 시작할 수 없습니다.

<a href="" id="description"></a>**설명**  
URL 리디렉션이 구성에서 MED-V 작업 영역 이름을 가져올 수 없습니다. 결과적으로, MED-V 작업 영역 브라우저에서 Windows 가상 PC에 리디렉션된 URL을 열 수 있습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 작업 영역 이름이 설정 되어 있고 C:\\Users\\ &lt; *사용자* &gt; \ 가상 컴퓨터 디렉터리의 가상 컴퓨터 이름과 일치 하는지 확인 합니다. MED-V 작업 영역 이름은 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.에 있습니다.

예를 들어 사용자가 "Matt"이 고 작업 영역 이름이 "mattsworkspace" 이면 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name의 값은 "mattsworkspace" 이어야 하며, C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx. 파일이 있어야 합니다.

### 이벤트 ID 5006

파이프 서버를 만들지 못했습니다.

<a href="" id="description"></a>**설명**  
URL 리디렉션 서비스가 Internet Explorer와 통신 하는 데 파이프 서버를 만들 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
시스템 이벤트 로그에서 경로가 "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_"와 유사 하 게 시작 하 고 사용자의 사용자 이름 및 도메인 이름으로 끝나는 파일 또는 리소스를 만들려는 시도에 대 한 확인을 수행 합니다. 이 이벤트가 이벤트 로그에 표시 되지 않으면 컴퓨터를 다시 시작 합니다.

### ConfigMgr (게스트)

### 이벤트 ID 7001

호스트 네트워크 구성 데이터의 형식이 잘못 되었습니다.

<a href="" id="description"></a>**설명**  
호스트에서 받은 네트워크 구성이 잘못 된 형식의 XML 문자열 이거나 호스트에서 반환 된 네트워크 정보를 XML 문서에 쓸 수 없는 경우

<a href="" id="solution"></a>**해결 방법**  
호스트 컴퓨터와 가상 컴퓨터를 다시 시작 합니다.

### 이벤트 ID 7005

호스트 네트워크 구성에 대 한 변경 내용이 검색 되었지만 호스트 네트워크 구성 데이터의 형식이 잘못 되어 적용할 수 없습니다.

<a href="" id="description"></a>**설명**  
호스트 네트워크 구성에 대 한 변경 내용이 가상 컴퓨터에 통신 되었지만 오류 때문에 가상 머신에서 처리 될 수 없습니다. 이 오류는 잘못 된 형식의 데이터 또는 WMI (Windows Management Instrumentation) CCMNetworkAdapter 인스턴스에 대 한 정보를 설정할 수 없는 경우에 발생할 수 있습니다.

<a href="" id="solution"></a>**해결 방법**  
호스트 및 가상 컴퓨터를 다시 시작 합니다.

### ConfigMgr (호스트)

### 이벤트 ID 8006

가상 컴퓨터를 찾을 수 없습니다.

<a href="" id="description"></a>**설명**  
Windows 가상 PC 7에서 가상 컴퓨터를 찾을 수 없습니다. 가상 머신이 삭제, 이동, 제거 되었거나 액세스가 거부 되었을 수 있습니다.

<a href="" id="solution"></a>**해결 방법**  
가상 컴퓨터를 다시 설치 합니다.

### 이벤트 ID 8008

워크스테이션의 네트워크 구성 정보를 검색할 수 없습니다.

<a href="" id="description"></a>**설명**  
대부분의 경우 .NET Framework의 시스템 호출 오류로 인해 MED-V 호스트에서 네트워크 구성 정보를 수집할 수 없습니다. 이 오류는 MED-V 호스트에서 반환 된 네트워크 정보를 XML 문서에 쓸 수 없는 경우에도 발생할 수 있습니다.

<a href="" id="solution"></a>**해결 방법**  
호스트 워크스테이션을 다시 시작 합니다.

### 이벤트 ID 8010

가상 머신에서 네트워크 구성 데이터를 설정할 수 없습니다.

<a href="" id="description"></a>**설명**  
가상 컴퓨터가 잘못 된 상태 이거나 Windows 가상 PC 추가가 설치 되지 않았거나 사용 하도록 설정 되어 있지 않기 때문에 MED-V 호스트 NAT (network address translation)가 가상 컴퓨터에 통신 되지 않을 수 있습니다.

<a href="" id="solution"></a>**해결 방법**  
가상 컴퓨터를 종료 하 고 다시 시작 합니다. 또한 가상 컴퓨터를 다시 설치 해야 할 수 있습니다.

### 이벤트 ID 8011

가상 머신에서 네트워크 구성 데이터를 다시 설정할 수 없습니다.

<a href="" id="description"></a>**설명**  
가상 컴퓨터가 잘못 된 상태 이거나 Windows 가상 PC 추가가 설치 되지 않았거나 사용 하도록 설정 되어 있지 않기 때문에 MED-V 호스트의 네트워크 구성 (브리지)을 가상 컴퓨터에 통신할 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
가상 컴퓨터를 종료 하 고 다시 시작 합니다. 또한 가상 컴퓨터를 다시 설치 해야 할 수 있습니다.

### 프린터 리디렉션

### 이벤트 ID 9001

파일 사용 권한 오류.

<a href="" id="description"></a>**설명**  
최종 사용자는 읽기용으로 MED-V 프린터 파일을 열거나 만드는 데 필요한 폴더에 액세스할 수 있는 권한이 없습니다.

<a href="" id="solution"></a>**해결 방법**  
User\\AppData\\ 경로에 액세스할 수 있고 사용자에 게 읽기 및 쓰기 권한이 있는지 확인 합니다. 예를 들어 사용자가 "Matt"이 고 경로가 C:\\Users\\Matt\\AppData\\, 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다. 있는 경우 경로 C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ 및 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.

### 이벤트 ID 9002

파일 사용 권한 오류.

<a href="" id="description"></a>**설명**  
최종 사용자에 게는 쓰기용으로 MED-V 프린터 파일을 열거나 만드는 데 필요한 폴더에 액세스할 수 있는 권한이 없습니다.

<a href="" id="solution"></a>**해결 방법**  
User\\AppData\\ 경로에 액세스할 수 있고 사용자에 게 읽기 및 쓰기 권한이 있는지 확인 합니다. 예를 들어 사용자가 "Matt" 인 경우 경로 C:\\Users\\Matt\\AppData\\와 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다. 있는 경우 경로 C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ 및 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.

### 이벤트 ID 9004

MEDV 프린터 파일을 저장할 경로를 만들 수 없습니다.

<a href="" id="description"></a>**설명**  
프린터 리디렉션 서비스에서 파일에 액세스 하거나 프린터 정보를 저장 하는 데 필요한 디렉터리를 만들 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
User\\AppData\\ 경로에 액세스할 수 있고 사용자에 게 읽기 및 쓰기 권한이 있는지 확인 합니다. 예를 들어 사용자가 "Matt" 인 경우 경로 C:\\Users\\Matt\\AppData\\와 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다. 있는 경우 경로 C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ 및 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.

### 이벤트 ID 9005

구성에서 VM 이름을 가져올 수 없습니다. 게스트 설치 관리자를 시작할 수 없습니다. MED-V를 업데이트할 수 없습니다-호스트 네트워크가 검색 되지 않았습니다.

<a href="" id="description"></a>**설명**  
프린터 리디렉션 서비스가 med-v 구성에서 MED-V 작업 영역 이름을 가져올 수 없으며 MED-V 게스트에서 설치 관리자를 시작 하도록 Windows 가상 PC에 알릴 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V 작업 영역 이름이 설정 되어 있고 C:\\Users\\ &lt; *사용자* &gt; \ 가상 컴퓨터 디렉터리의 가상 컴퓨터 이름과 일치 하는지 확인 합니다. MED-V 작업 영역 이름은 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.에 있습니다.

예를 들어 사용자가 "Matt"이 고 작업 영역 이름이 "mattsworkspace" 이면 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name의 값은 "mattsworkspace" 이어야 하며 C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx. 파일이 있어야 합니다.

### 응용 프로그램 게시

### 이벤트 ID 10015

조정 프로세스 중에 파일 시스템 오류가 발생 했습니다. 조정 프로세스는 파일 이름을 처리 하지 &lt; *filename* &gt; 않지만, 계속 해 서 다른 변경 내용을 처리 하 게 됩니다.

<a href="" id="description"></a>**설명**  
바로 가기를 만들거나 삭제 하는 동안 허가 되지 않은 액세스 또는 I/o 오류가 발생 했습니다.

<a href="" id="solution"></a>**해결 방법**  
파일 경로에 액세스할 수 있고 사용자에 게 지정 된 파일을 만들거나 삭제할 권한이 있는지 확인 합니다.

### 이벤트 ID 10021

파일 &lt; *error\_information* &gt; 이름에 대 한 파일 작업 작업에 대 한 오류 오류 \ _information &lt; *\ _name* &gt; &lt; *filename* &gt; .

<a href="" id="description"></a>**설명**  
바로 가기를 만들거나 삭제 하는 동안 허가 되지 않은 액세스 또는 I/o 오류가 발생 했습니다.

<a href="" id="solution"></a>**해결 방법**  
파일 경로에 액세스할 수 있고 사용자에 게 지정 된 파일을 만들거나 삭제할 권한이 있는지 확인 합니다.

### 게스트 패치

### 이벤트 ID 11001

게스트 웨이크업 작업 사용 메시지

<a href="" id="description"></a>**설명**  
/GuestWakeup 옵션을 사용 하 여 MedvHost.exe를 틀리게 실행 했거나 명령의 형식이 잘못 되었습니다.

<a href="" id="solution"></a>**해결 방법**  
명령이 다음 형식으로 실행 되는지 확인 합니다.

Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *workspace \ _name* &gt; " 위치

&lt;*기간 \ _in \ _minutes* &gt; 가상 컴퓨터가 활성 상태로 유지 되어야 하는 시간 (분)입니다 (기본값 240).

&lt;*작업 영역 \ _name* &gt; 은 활성화 되어야 하는 가상 컴퓨터의 이름입니다.

### 이벤트 ID 11002

MED-V를 업데이트할 수 없습니다-호스트 네트워크가 검색 되지 않았습니다.

<a href="" id="description"></a>**설명**  
호스트 네트워크 연결이 검색 되지 않아 게스트 패치가 완료 되지 않았습니다.

<a href="" id="solution"></a>**해결 방법**  
게스트 패치를 실행 하기 전에 MED-V 호스트를 활성 네트워크 연결에 연결 합니다.

### 이벤트 ID 11003

MED-V를 업데이트할 수 없습니다. A/C powerFailed가 실행 되 고 있지 않습니다. 파이프 서버를 만들지 못했습니다.

<a href="" id="description"></a>**설명**  
호스트가 전원 코드 대신 배터리 전원으로 실행 되는 것으로 나타나기 때문에 게스트 패치가 완료 되지 않았습니다.

<a href="" id="solution"></a>**해결 방법**  
게스트 패치를 실행 하기 전에 호스트 컴퓨터를 전원 코드에 연결 합니다.

### 클라이언트 UX

### 이벤트 ID 14003

다음 용지함 상태 메시지가 너무 길어서 표시할 수 없습니다: &lt; *용지함 \ _status \ _message*&gt;

<a href="" id="description"></a>**설명**  
MED-V가 트레이 도구 설명 또는 풍선 메시지에 비해 너무 긴 예기치 않은 문자열을 만들었습니다. 그 결과 표시 된 메시지가 잘렸습니다.

<a href="" id="solution"></a>**해결 방법**  
이 오류는 MED-V가 도구 설명 텍스트를 무작위로 만드는 경우 발생할 수 있는 드문 경우입니다. 해결 방법이 없습니다.

### 이벤트 ID 14004

처리 되지 않은 예외로 인해 MED-V가 중지 되었습니다.

<a href="" id="description"></a>**설명**  
처리 되지 않은 예외로 인해 MED-V가 예기치 않게 중지 됩니다.

<a href="" id="solution"></a>**해결 방법**  
MED-V를 다시 시작 합니다.

### 이벤트 ID 14005

서버에서 mutex을 만들려고 했지만 이미 존재 했습니다.

<a href="" id="description"></a>**설명**  
MedvHost.exe의 두 번째 인스턴스는 메모리에 남아 있습니다.

<a href="" id="solution"></a>**해결 방법**  
TaskManager를 열고 모든 MedvHost.exe 프로세스를 종료 합니다.

### 이벤트 ID 14006

레지스트리 값 레지스트리를 수정 또는 삭제 하는 중 오류가 발생 했습니다 &lt; . *\ _value* &gt; .

<a href="" id="description"></a>**설명**  
MED-V는 레지스트리의 지정 된 항목을 수정할 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
관리 자격 증명을 사용 하 여 MED-V를 설치 하거나 제거 해야 합니다.

### 이벤트 ID 14007

지정 된 파일 ( &lt; *filename* &gt; )이 잘못 되었습니다.

<a href="" id="description"></a>**설명**  
설치 또는 제거 하는 동안 손상 된 임시 파일이 MED-V 호스트에 전달 되었습니다.

<a href="" id="solution"></a>**해결 방법**  
Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.

### 이벤트 ID 14008

파일을 찾을 수 없습니다: &lt; *filename* &gt; .

<a href="" id="description"></a>**설명**  
설치 또는 제거 하는 동안 필요한 임시 파일의 경로를 찾을 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.

### 이벤트 ID 14009

매개 변수 파일 이름을 읽을 수 없습니다 &lt; *filename* &gt; .

<a href="" id="description"></a>**설명**  
설치 또는 제거 프로세스가 진행 되는 동안 MED-V가 임시 파일을 읽을 수 없습니다.

<a href="" id="solution"></a>**해결 방법**  
Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다. 또한 사용자에 게 Temp 폴더에 대 한 필요한 권한과 권한이 있는지 확인 합니다.

### 이벤트 ID 14010

매개 변수 파일 이름을 역직렬화 하는 동안 오류가 발생 했습니다 &lt; *filename* &gt; .

<a href="" id="description"></a>**설명**  
설치 또는 제거 프로세스가 진행 되는 동안 MED-V에 손상 된 임시 파일이 발견 되었습니다.

<a href="" id="solution"></a>**해결 방법**  
Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다. 또한 사용자에 게 Temp 폴더에 대 한 필요한 권한과 권한이 있는지 확인 합니다.

### 이벤트 ID 14011

매개 변수 파일 이름을 역직렬화 하는 동안 예기치 않은 오류가 발생 했습니다 &lt; *filename* &gt; .

<a href="" id="description"></a>**설명**  
설치 또는 제거 프로세스가 진행 되는 동안 MED-V에 손상 된 임시 파일이 발견 되었습니다.

<a href="" id="solution"></a>**해결 방법**  
Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다. 또한 사용자에 게 Temp 폴더에 대 한 필요한 권한과 권한이 있는지 확인 합니다.

### 이벤트 ID 14012

폴더 폴더의 설정 권한이 &lt; *folder\_name* &gt; 사용자 &lt; *사용자 이름*에 대해 \ _name 하는 동안 예기치 않은 오류가 발생 했습니다 &gt; .

<a href="" id="description"></a>**설명**  
MED-V가 설치 중 특정 폴더에 대 한 권한 및 사용 권한을 설정할 수 없는 경우 오류가 발생 합니다.

<a href="" id="solution"></a>**해결 방법**  
다음 폴더에 대 한 관리자 권한을 확인 합니다.

@"%ProgramData%\\Microsoft\\Medv\\AllUsers"

@"%ProgramData%\\Microsoft\\Medv\\MedvLock"

@"%ProgramData%\\Microsoft\\Medv\\Monitoring"

### 이벤트 ID 14013

잠금 파일을 만들 때 예기치 않은 오류가 발생 했습니다.

<a href="" id="description"></a>**설명**  
MED-V가 설치 중 @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" 폴더에 파일을 만들 수 없는 경우 오류가 발생 합니다.

<a href="" id="solution"></a>**해결 방법**  
MedvLock 폴더에 대 한 관리자 권한을 확인 합니다.

## 관련 항목


[MED-V 문제 해결](troubleshooting-med-vmedv2.md)

 

 





