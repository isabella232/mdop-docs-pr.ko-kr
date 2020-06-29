---
title: 스크립트 동작을 설정하는 방법
description: 스크립트 동작을 설정하는 방법
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812388"
---
# 스크립트 동작을 설정하는 방법


스크립트 작업 편집기에서는 관리자가 MED-V 작업 영역 설정 중 수행할 동작과 수행할 순서를 정의 하는 작업을 만들 수 있습니다.

다음은 도메인 설정 스크립트에 추가할 수 있는 작업의 목록입니다.

-   Windows **다시 시작**-windows를 다시 시작 합니다.

-   **도메인에 가입**— 도메인에 참가 하는 경우이 작업을 포함 하 고 사용자 이름, 암호, 정규화 된 도메인 이름, NetBIOS 도메인 이름 및 조직 단위를 구성 합니다 (선택 사항).

-   연결 **확인**-연결할 서버를 구성 하 고 med-v 작업 영역이 네트워크 리소스 (예: 도메인 서버)에 연결할 수 있는지 확인 합니다.

-   **명령줄-med-v**작업 영역에서 스크립트를 구성 하 고 스크립트 경로와 스크립트 인수를 포함 하는 명령줄을 입력 합니다.

-   **컴퓨터 이름 바꾸기**— 정의 된 설정을 기반으로 가상 컴퓨터 컴퓨터의 이름을 바꿉니다.

-   **자동 로그온 사용 안 함**-Windows 자동 로그온을 사용 하지 않습니다. 이 작업은 컴퓨터를 도메인에 추가 하는 스크립트의 끝에 추가 해야 합니다.

## <a href="" id="how-to-set-up-script-actions-"></a>스크립트 동작을 설정하는 방법


**스크립트 동작을 설정 하려면**

1.  **VM 설정** 탭에서 **스크립트 편집기**를 클릭 합니다.

2.  **스크립트 작업** 대화 상자에서 **추가**를 클릭 하 고 하위 메뉴에서 원하는 작업을 클릭 합니다.

3.  다음 표에 설명 된 대로 작업을 구성 합니다.

    **참고** 
     **컴퓨터 이름 바꾸기** 는 **VM 설정** 탭에서 구성 합니다. 자세한 내용은 [VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)참조 하세요.

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. 작업을 선택 하 고 **위쪽** 또는 **아래**를 클릭 하 여 작업 순서를 설정 합니다.

5. **OK**(확인)를 클릭합니다.

**참고**  
도메인 가입 스크립트를 실행할 때 스크립트 작동을 위해 MED-V 작업 영역 가상 컴퓨터에 로그인 한 사용자에 게 로컬 관리자 권한이 있어야 합니다.



**참고**  
자동 로그온 사용 안 함 스크립트를 실행 하는 경우 초기 설정이 완료 되 면 자동 로그온에 사용 되는 로컬 게스트 계정을 사용 하지 않도록 설정 하는 것이 좋습니다.



### <a href="" id="bkmk-joindomainproperties"></a>

**도메인 속성 참가**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>VM을 도메인에 참가할 때 사용할 자격 증명</p></td>
<td align="left"><p>VM을 도메인에 참가할 때 사용할 다음 자격 증명 중 하나를 선택 합니다.</p>
<ul>
<li><p><strong>MED-V 자격 증명 </strong> -최종 사용자 자격 증명을 사용 합니다.</p></li>
<li><p><strong>지정 된 자격 증명으로 다음 자격 증명을 사용 합니다. </strong> 해당 필드에 사용자 이름 및 암호를 입력 합니다.</p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>입력 하는 자격 증명은 모든 MED-V 작업 영역 사용자에 게 표시 됩니다. 도메인 관리자 자격 증명을 제공 하지 않는 것이 좋습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>가입할 도메인</p></td>
<td align="left"><p>다음 중 하나를 선택하세요.</p>
<ul>
<li><p><strong>작업 영역을 시작 하는 데 사용 된 도메인 이름 </strong> , 즉 med-v 클라이언트에 로그인 할 때 최종 사용자가 입력 한 도메인에 참가 합니다.</p>
<p>NetBIOS에서 정규화 된 도메인 이름으로의 매핑을 정의 하려면 <strong> 전역 도메인 매핑 테이블을 클릭 </strong> 합니다. 전역 도메인 매핑 테이블에서 <strong> 추가 </strong> 를 클릭 하 고 <strong> NetBIOS 도메인 이름 </strong> 및 정규화 된 <strong> 도메인 이름을 입력 </strong> 한 다음 확인을 클릭 <strong> </strong> 합니다.</p></li>
<li><p><strong>다음 도메인 이름 사용 </strong> -지정 된 도메인에 참가 합니다. 도메인 이름 및 NetBIOS 도메인 이름을 해당 필드에 입력 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>조직 구성 단위</p></td>
<td align="left"><p>OU (조직 구성 단위)는 컴퓨터를 특정 OU에 가입 하도록 지정할 수 있습니다. 형식은 ou 고유 이름 다음에와 야 합니다. OU = &lt; 조직 구성 단위 &gt; , &lt; 도메인 컨트롤러 &gt; (예: OU = QATest, DC = IL, DC = med-v, dc = com).</p>
<div class="alert">
<strong>Warning</strong><br/><p>위의 예제에 나와 있는 것 처럼 단일 수준 OU만 지원 됩니다.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**연결 속성 확인**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IP 주소</p></td>
<td align="left"><p>연결을 확인 하는 서버의 IP 주소입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Port</p></td>
<td align="left"><p>연결을 확인 하는 서버의 포트입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>시간 제한</p></td>
<td align="left"><p>제한 시간 전에 응답을 기다리는 시간 (초)입니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**명령줄 속성**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>경로</p></td>
<td align="left"><p>명령줄의 경로입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>인수</p></td>
<td align="left"><p>명령줄 인수</p></td>
</tr>
<tr class="odd">
<td align="left"><p>끝내기 대기</p></td>
<td align="left"><p>스크립트 작업을 계속 하기 전에 반환 될 때까지 대기 하는 확인란을 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>오류 발생 시 실패</p></td>
<td align="left"><p>반환 내용이 지정 된 값인 경우에는이 확인란을 선택 합니다.</p>
<p>명령이 성공으로 표시 되는 값을 입력 합니다.</p>
<p>기본값: <strong> 0</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>한 번만 수행</p></td>
<td align="left"><p>명령줄을 한 번만 실행 하려면이 확인란을 선택 합니다. 스크립트가 실패 하거나 취소 되 면이 명령은 다시 실행 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이 명령줄을 실행 하면 작업 영역에서 Windows가 다시 시작 됩니다.</p></td>
<td align="left"><p>명령줄에 완료 후 다시 시작이 발생 하는 경우이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>조작 허용</p></td>
<td align="left"><p>명령에 사용자 조작이 필요한 경우이 확인란을 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>진행률 메시지</p></td>
<td align="left"><p>명령이 실행 되는 동안 사용자에 게 표시할 메시지</p></td>
</tr>
<tr class="odd">
<td align="left"><p>오류 메시지</p></td>
<td align="left"><p>명령이 실패 하는 경우 사용자에 게 표시 되는 메시지</p></td>
</tr>
</tbody>
</table>

 

명령줄 작업을 구성할 때 다음 표에 정의 된 대로 여러 변수를 사용할 수 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">값</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>% MEDVUser%</p></td>
<td align="left"><p>인증 된 사용자 이름입니다.</p></td>
<td align="left"><p>MED-V 인증 된 사용자 이름입니다. 사용자 이름 및 암호는 도메인 VM 설치 스크립트에서 사용할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% MEDVPassword%</p></td>
<td align="left"><p>인증 된 비밀 번호입니다.</p></td>
<td align="left"><p>MED-V 인증 된 암호입니다. 사용자 이름 및 암호는 도메인 VM 설치 스크립트에서 사용할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% MEDVDomain%</p></td>
<td align="left"><p>도메인을 구성 합니다.</p></td>
<td align="left"><p>MED-V 인증에서 구성 된 도메인입니다. VM 설치 스크립트에서 사용할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%DesiredMachineName%</p></td>
<td align="left"><p>컴퓨터 이름입니다.</p></td>
<td align="left"><p>관리 응용 프로그램에 구성 된 고유한 컴퓨터 이름입니다. VM 설치 스크립트에서 사용할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[VM 컴퓨터 이름 패턴 속성을 구성하는 방법](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





