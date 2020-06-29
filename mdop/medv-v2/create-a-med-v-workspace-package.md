---
title: MED-V 작업 영역 패키지 만들기
description: MED-V 작업 영역 패키지 만들기
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823263"
---
# MED-V 작업 영역 패키지 만들기


MED-V 작업 영역은 MED-V에서 제공 하는 가상 컴퓨터와 최종 사용자가 상호 작용 하는 Windows XP 데스크톱 환경입니다. 관리자가 MED-V 작업 영역을 만들고 사용자 지정 합니다. 작업 영역은 이미지와 MED-V 작업 영역의 규칙 및 기능을 정의 하는 그룹 정책으로 구성 됩니다.

고유한 구성, 설정 및 규칙을 사용 하 여 각 사용자 지정 된 MED-V 작업 영역을 여러 개 만들 수 있습니다. 사용자, 그룹 또는 여러 사용자 또는 그룹을 각 MED-V 작업 영역에 연결할 수 있습니다. 사용자 지정 하면 MED-V 작업 영역을 해당 사용자나 그룹에만 사용할 수 있습니다.

**Med-v 작업 영역 포장기** 를 사용 하 여 med-v 작업 영역을 만듭니다. **Med-v 작업 영역 포장기** 는 다음 두 가지 주요 섹션으로 구분 됩니다.

-   MED-V 작업 영역을 만들고 관리 하는 데 사용 하는 세 개의 단추가 포함 된 주 패널 **Med-v 작업 영역 패키지 만들기** 단추는 med-v 작업 영역을 만드는 데 사용 하는 **Med-v 작업 영역 패키지 만들기 마법사** 를 엽니다.

-   창의 오른쪽에 있는 **도움말 센터** 에서 med-v 작업 영역을 만들고 테스트 하 고 관리 하는 데 도움이 되는 정보 및 지침을 제공 합니다.

**중요**  
**Med-v 작업 영역 포장기**를 사용 하려면 먼저 Windows PowerShell 실행 정책이 무제한으로 설정 되어 있는지 확인 해야 합니다.

`Set-ExecutionPolicy Unrestricted`

또한 **Med-v 작업 영역 포장기** 가 실행 되는 컴퓨터에 대 한 SAN 정책은 "Online All"으로 설정 해야 합니다. SAN 정책의 설정을 확인 하려면 관리자 자격 증명을 사용 하 여 명령 프롬프트에서 다음 명령을 실행 합니다.

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

필요한 경우 관리자 자격 증명을 사용 하 여 명령 프롬프트에 다음 명령을 입력 하 여 SAN 정책을 "온라인 All"으로 변경 합니다.

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**중요**  
가상 하드 디스크를 탑재 하 고 MED-V 작업 영역 패키지를 작성 하는 데 사용 하는 컴퓨터에 자동 디스크 암호화 소프트웨어가 설치 되어 있는 경우 시작 하기 전에 소프트웨어를 사용 하지 않도록 설정 해야 합니다. 그렇지 않으면 다른 컴퓨터의 MED-V 작업 영역을 사용할 수 없습니다.



여기서 제공 하는 정보는 MED-V 작업 영역 배포 패키지를 만드는 데 도움이 될 수 있습니다.

## <a href="" id="bkmk-prereq"></a>필수 구성 요소


MED-V 작업 영역 배포 패키지 빌드를 시작 하기 전에 다음 항목에 액세스할 수 있는지 확인 합니다.

-   **Windows XP 준비 이미지**

    MED-V와 함께 사용할 Windows XP 이미지를 만드는 방법에 대 한 자세한 내용은 [Med-v 이미지 준비](prepare-a-med-v-image.md)를 참조 하세요.

-   **URL 리디렉션 정보를 포함 하는 텍스트 파일 또는 목록**

    URL 리디렉션 텍스트 파일 또는 목록에는 호스트 컴퓨터에서 MED-V 작업 영역의 Internet Explorer로 리디렉션되는 Url이 포함 되어 있습니다. 패키지 마법사를 사용 하 여 MED-V 작업 영역을 만드는 경우 패키지 만들기 프로세스의 단계 중 하나로이 리디렉션 정보를 가져오거나 입력 하거나 복사 하 여 붙여넣습니다.

    **참고**  
    MED-V의 URL 리디렉션은 HTTP 및 HTTPS 프로토콜만 지원 합니다. MED-V는 FTP 또는 다른 프로토콜에 대 한 지원을 제공 하지 않습니다.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## MED-V 작업 영역 포장기 컴퓨터의 언어 이외의 언어에 대 한 MED-V 작업 영역 패키징


기본적으로 MED-V 작업 영역은 컴퓨터 언어와 영어의 문자를 모두 지원 합니다. 컴퓨터에 설치 되어 있지 않은 언어에 대해 MED-V 작업 영역을 만들려면 MED-V 작업 영역 이름 뒤에 있는 PowerShell 스크립트 (ps1)에서 **-loc \ [locale \]** 을 지정 합니다.

Med-v 작업 영역 포장기 컴퓨터의 기본 언어가 아닌 다른 언어로 MED-V 작업 영역 패키지를 만들려면 MED-V 작업 영역 포장기를 실행 하 여 기본 언어로 스크립트를 생성 한 다음 로캘에 필요한 대로 출력 스크립트를 수정 합니다. 스크립트는 패키지 중에 지정 된 MED-V 작업 영역 출력 디렉터리에 있습니다. 로캘 설정의 이름은에 있습니다. 다음 디렉터리에 있는 WXL 파일:

C:\\program files Files\\Microsoft Enterprise 데스크톱 Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale

## MED-V 작업 영역 패키지 만들기


MED-V 작업 영역 패키지를 만들려면 다음 단계를 따릅니다.

****

1.  **Med-v 작업 영역 포장기**를 열려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 작업 영역 포장기**를 클릭 합니다.

2.  **Med-v 작업 영역 포장기** 기본 패널에서 **Med-v 작업 영역 패키지 만들기**를 클릭 합니다.

    MED-V **만들기 Med-v 작업 영역 패키지 마법사** 가 나타납니다. 마법사는 다음 페이지로 구성 됩니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>패키지 정보</strong></p></td>
    <td align="left"><p>MED-V 작업 영역의 이름을 지정 하 고 MED-V 작업 영역 패키지 파일이 저장 된 폴더를 선택 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Windows XP 이미지 선택</strong></p></td>
    <td align="left"><p>준비 된 Windows XP 가상 PC 이미지를 지정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>처음 설치 시</strong></p></td>
    <td align="left"><p>처음 설정 하는 동안 MED-V가 팔 로우 하는 설치 프로세스를 지정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>MED-V 메시지</strong></p></td>
    <td align="left"><p>최종 사용자가 처음 설정 하는 동안 표시 되는 도움말 정보에 대 한 메시지 및 선택적 URL을 지정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>컴퓨터 이름 지정</strong></p></td>
    <td align="left"><p>MED-V 가상 컴퓨터의 이름을 지정 하는 방법에 대해 설명 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>호스트에서 설정 복사</strong></p></td>
    <td align="left"><p>MED-V 작업 영역에 대 한 설정을 정의 하는 방법을 지정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>시작 및 네트워킹</strong></p></td>
    <td align="left"><p>MED-V 작업 영역, 네트워킹 및 사용자 자격 증명 시작에 대 한 설정을 지정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>웹 리디렉션</strong></p></td>
    <td align="left"><p>MED-V 작업 영역에서 Internet Explorer로 리디렉션할 텍스트 파일 또는 Url 목록을 지정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>요약</strong></p></td>
    <td align="left"><p>MED-V 작업 영역 설정을 확인 하 고 MED-V 작업 영역 배포 패키지 만들기를 시작 합니다.</p></td>
    </tr>
    </tbody>
    </table>



3.  **패키지 정보** 페이지에서 med-v 작업 영역의 이름을 입력 하 고 med-v 작업 영역 패키지 파일이 저장 된 폴더를 선택 합니다.

    **Warning**  
    MED-V 작업 영역의 이름을 지정 하 고 계속 하려면 폴더를 지정 해야 합니다.



~~~
After you have finished, click **Next**.
~~~

4. **WINDOWS Xp 이미지 선택** 페이지에서 준비 된 MED-V Windows XP 가상 PC 이미지 (.vhd 파일)의 위치를 지정 합니다.

   **Warning**  
   계속 하려면 Windows XP VHD 이미지를 지정 해야 합니다.



~~~
After you have finished, click **Next**.
~~~

5. **처음 설정** 페이지에서 유인 또는 무인 모드를 처음으로 실행할 것인지 아니면 공유 컴퓨터의 모든 최종 사용자가 개별적으로 사용할 것인지 아니면 사용할 수 있는지를 선택 합니다.

   **알림 없이 무인 설치를**선택 하는 경우 최종 사용자에 게는 처음 설치를 실행할 때 알림이 표시 되지 않으며, 처음 설정 하는 동안에는 가상 컴퓨터가 최종 사용자에 게 표시 되지 않습니다. 또한 설치 프로그램이 완전히 무인 모드에서 실행 되는 경우에는 메시지가 필요 하지 않으므로, 마법사의 **Med-v 메시지** 페이지가 숨겨집니다.

   **무인 설치를 선택 했지만 최종 사용자에 게 처음 설치를 시작 하기 전에 알림**메시지가 표시 되는 경우 최종 사용자에 게 처음 설치를 실행 하기 전에 알림을 보냅니다. 그러나 처음 설정 하는 동안에는 가상 컴퓨터가 최종 사용자에 게 표시 되지 않습니다.

   최종 사용자가 처음 설정 하는 동안 정보를 입력 해야 하는 경우 **유인 설정을** 선택 합니다.

   기본 동작은 **무인 설정 이지만 처음 설치를 시작 하기 전에 최종 사용자에 게 알립니다**.

   **주의**  
   미니 설치가 완료 되려면 사용자 입력이 필요 하도록 Sysprep.inf 파일을 만든 경우 설치를 시작 하는 동안 **유인 설정** 또는 문제가 발생할 수 있습니다를 선택 해야 합니다.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. **Med-v 메시지** 페이지에서 최종 사용자가 처음 설정 하는 동안 표시 되는 다음 메시지를 지정 합니다.

   -   설치가 처음 시작 될 때 최종 사용자에 게 표시 되는 메시지입니다.

   -   처음 설치에 실패 하거나 오류가 발생 한 경우 최종 사용자에 게 표시 되는 메시지입니다.

   **참고**  
   마법사의 **Med-v 메시지** 페이지는 **처음 설정** 페이지에서 **알림 메시지 없이 무인 설치를** 선택한 경우에는 숨겨집니다.



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. 컴퓨터 **이름 지정** 페이지에서 컴퓨터 명명을 Med-v 또는 Sysprep 등의 시스템 관리 도구를 통해 관리 하는지 여부를 지정할 수 있습니다. 기본값은 컴퓨터 명명이 시스템 관리 도구에 의해 관리 됨입니다.

   컴퓨터 명명을 MED-V에서 관리 하도록 지정 하는 경우 드롭다운 목록에서 미리 정의 된 컴퓨터 명명 규칙 (마스크)을 선택 합니다. 예제 컴퓨터 이름의 미리 보기는 MED-V 작업 영역 패키지를 작성 하는 데 사용 하는 컴퓨터에 따라 표시 됩니다.

   사용자 지정 명명 규칙 중 하나를 선택 하는 경우 지정할 수 있는 필드는 다음 문자로 제한 됩니다.

   -   접두 번호와 접미사 필드는 A-z, a-z, 0-9 및 특수 문자로 이루어진 문자 수로 제한 됩니다.! @ \ # $% ^ & ()-\ _ ' {}. 및 ~.

   -   호스트 이름 및 사용자 이름 필드는 0 ~ 9의 숫자로 제한 됩니다.

   **중요**  
   컴퓨터 이름은 고유 해야 하 고 최대 15 자로 제한 됩니다. 컴퓨터 명명 방법을 결정할 때는 여러 컴퓨터를 보유 하거나 컴퓨터를 공유 하는 최종 사용자를 고려 하 고 네트워크 충돌을 일으킬 수 있는 컴퓨터 이름 마스크를 사용 하지 않는 것이 좋습니다.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. **호스트의 설정 복사** 페이지에서 다음 설정을 선택 하 여 med-v 작업 영역을 구성 하는 방법을 지정할 수 있습니다.

   **주의**  
   호스트 컴퓨터에서 MED-V 작업 영역으로 복사 되는이 페이지에서 지정 하는 설정은 Sysprep.inf 응답 파일에 지정 된 설정 보다 우선 합니다.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. **시작 및 네트워킹** 페이지에서 다음 설정에 대 한 기본 동작을 변경할 수 있습니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>MED-V 작업 영역 시작</strong></p></td>
   <td align="left"><p>사용자가 로그온 할 때 MED-V 작업 영역을 시작할지, 처음 사용할 때 또는 최종 사용자가 MED-V 작업 영역이 시작 되는 시점을 결정할 수 있도록 할지 선택 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>MED-V 작업 영역은 최종 사용자가 로그온 하거나, 게시 된 응용 프로그램을 열거나 리디렉션이 필요한 URL을 입력 하는 등 MED-V가 필요한 작업을 처음 시작 하는 경우 두 가지 방법 중 하나로 시작 됩니다.</p>
   <p>최종 사용자에 대해이 설정을 정의 하거나 최종 사용자가 MED-V를 시작 하는 방법을 제어할 수 있습니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>최종 사용자가 결정 하는 경우 기본 동작은 기본적으로 로그온 할 때 MED-V 작업 영역을 시작 하는 것입니다. 알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 하 고 Med-v 사용자 설정을 선택 하 여 기본값을 변경할 수 있습니다 <strong> </strong> . 최종 사용자에 대해이 설정을 정의 하는 경우에는 MED-V가 시작 되는 방식을 변경할 수 없습니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>네트워킹</strong></p></td>
   <td align="left"><p><strong> </strong> <strong> </strong> 네트워킹 설정에 대 한 공유 또는 브리지를 선택 합니다. 기본값은 <strong> 공유 </strong> 입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>공유 </strong> - med-v 작업 영역은 NAT (Network Address Translation)를 사용 하 여 송신 트래픽에 대 한 호스트&#39;s IP를 공유 합니다.</p>
   <p><strong>브리지 </strong> - 된 med-v 작업 영역에는 일반적으로 DHCP를 통해 얻은 고유한 네트워크 주소가 있습니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>스토어 자격 증명</strong></p></td>
   <td align="left"><p>최종 사용자 자격 증명을 저장할지 여부를 선택 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>기본 동작은 자격 증명 저장을 사용 하지 않도록 설정 하 여 최종 사용자가 로그온 할 때마다 인증을 받아야 한다는 것입니다.</p>
   <div class="alert">
   <strong>중요</strong><br/><p>최종 사용자의 자격 증명을 캐시 하는 것이 최상의 사용자 환경을 제공 하는 경우에도 관련 된 위험에 유의 해야 합니다.</p>
   <p>최종 사용자의 도메인 자격 증명은 Windows 자격 증명 관리자의 해독 가능한 형식으로 저장 됩니다. 결과적으로 공격자는 암호를 검색 하는 프로그램을 작성 하 고 사용자의 자격 증명에 액세스할 수 있습니다. 최종 사용자 자격 증명을 저장 하지 않도록 설정 하 여이 위험을 줄일 수 있습니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. **웹 리디렉션** 페이지에서 med-v 작업 영역의 Internet Explorer로 리디렉션되는 url 목록을 입력 하거나, 붙여 넣거나, 가져올 수 있습니다. URL 리디렉션 정보를 구성 하는 방법에 대 한 자세한 내용은 [필수 구성 요소](#bkmk-prereq)를 참조 하세요.

   또한 MED-V 작업 영역의 Internet Explorer가 최종 사용자에 대해 구성 되는 방식을 지정할 수 있습니다. 기본적으로 인터넷 영역 보안 수준은 높음으로 설정 됩니다. 또한 주소 표시줄과 같은 특정 검색 기능도 제거 됩니다. MED-V 작업 영역에서 Internet Explorer의이 기본 구성은 최종 사용자에 게 더욱 안전한 검색 환경을 제공 합니다.

   **주의**  
   기본 설정을 변경 하 여 MED-V 작업 영역에서 Internet Explorer를 사용자 지정할 수 있습니다. 그러나 기본 설정을 변경 하 여 보안 수준을 낮게 설정 하는 경우 이전 버전의 Internet Explorer에 있는 보안 위험에 조직을 공개할 수 있다는 것을 염두에 두는 것이 좋습니다. 자세한 내용은 [Med-v 작업에 대 한 보안 모범 사례](security-best-practices-for-med-v-operations.md)를 참조 하세요.



~~~
After you have finished, click **Next**.
~~~

11. **요약** 페이지에서이 med-v 작업 영역의 패키지 설정을 검토할 수 있습니다. 설정을 변경 하려는 경우 **이전** 단추를 클릭 하 여 관련 페이지로 돌아갑니다. 설정 검토를 완료 한 후에 **만들기**를 클릭 합니다.

   **Med-v 작업 영역 패키지 만들기 마법사** 의 **완료** 페이지가 열리며 패키지 생성 진행률을 표시 합니다.

   **참고**  
   MED-V 작업 영역 패키지 만들기 프로세스는 지정 된 VHD 크기에 따라 완료 하는 데 몇 분 정도 걸릴 수 있습니다.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. **닫기를** 클릭 하 여 패키지 마법사를 닫고 **Med-v 작업 영역 포장기**로 돌아갑니다.

이제 배포 전에 MED-V 작업 영역 패키지를 테스트할 준비가 되었습니다.

## 관련 항목


[Windows PowerShell을 사용하여 고급 설정 구성](configuring-advanced-settings-by-using-windows-powershell.md)

[MED-V 작업 영역 패키지 테스트](testing-the-med-v-workspace-package.md)

[MED-V 이미지 준비](prepare-a-med-v-image.md)









