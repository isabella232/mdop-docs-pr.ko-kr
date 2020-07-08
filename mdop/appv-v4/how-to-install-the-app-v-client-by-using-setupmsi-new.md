---
title: Setup.msi를 사용하여 App-V Client를 설치하는 방법
description: Setup.msi를 사용하여 App-V Client를 설치하는 방법
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817333"
---
# Setup.msi를 사용하여 App-V Client를 설치하는 방법


이 항목에서는 setup.msi 프로그램을 사용 하 여 앱 V 클라이언트를 설치 하는 방법에 대해 설명 합니다. setup.msi 프로그램을 사용 하 여 App-v 클라이언트를 설치 하기 전에 먼저 필수 구성 요소 소프트웨어를 설치 해야 하는지 확인 한 다음 설치 해야 합니다. 필수 구성 요소 소프트웨어를 설치 하려면이 항목의 [필수 구성 요소 소프트웨어 설치](#prereq-sw) 섹션을 참조 하세요. 클라이언트 소프트웨어를 설치 하려면이 항목의 [Setup.msi 프로그램 섹션을 사용 하 여 App-v 클라이언트 설치](#msi-setup) 를 참조 하세요.

## <a href="" id="prereq-sw"></a>필수 소프트웨어 설치


다음 절차를 사용 하 여 필수 구성 요소 소프트웨어를 설치할 수 있습니다. 명령 파일을 만들고 명령 프롬프트에서 명령을 실행 하거나, VBScript 또는 Windows PowerShell 같은 스크립트 언어를 사용 하 여 명령을 실행할 수 있습니다.

**참고**  X86 및 x64 버전의 App-v 클라이언트에는 다음 소프트웨어의 x86 버전이 필요 합니다.

 

**Microsoft VisualC + + 2005SP1 재배포 가능 패키지 (x86)를 설치 하려면**

1. Microsoft 다운로드 센터 ()에서 [Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) 소프트웨어 패키지를 다운로드 <https://go.microsoft.com/fwlink/?LinkId=119961> 합니다. \ [Template Token Value \] 버전 4.5 SP2 이상의 App-v 클라이언트의 경우 [Microsoft Visual c + + 2005 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [Template token Value \])에서 vcredist\_x86.exe를 다운로드 하세요.

2. 자동으로 설치 하려면 명령줄 옵션 "/Q"를 vcredist\_x86.exe와 함께 사용 합니다 (예: **vcredist\_x86.exe/q**.

3. vcredist\_x86.msi 파일을 사용 하 여 소프트웨어를 설치 하려면 명령줄 옵션인 "/C/T: &lt; fullpathtofolder &gt; "를 사용 하 여 vcredist.msi 파일을 추출 하 고 vcredist\_x86.exe에서 임시 폴더로 vcredis1.cab 합니다. 자동으로 설치 하려면 명령줄 옵션/quiet (예: **msiexec/i vcredist.msi** /quiet.를 사용 합니다.

### Microsoft VisualC + + 2008을 설치 하려면 SP1 재배포 가능 패키지 (x86)

**중요**  App-v 클라이언트의 버전 4.6 이상에서는 Microsoft Visual c + + 2008 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트도 설치 해야 합니다.

 

****

1.  Microsoft 다운로드 센터 [2008 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트](https://go.microsoft.com/fwlink/?LinkId=150700) 소프트웨어 패키지를 다운로드 합니다 ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  자동으로 설치 하려면 명령줄 옵션 "/Q"를 vcredist\_x86.exe와 함께 사용 합니다 (예: **vcredist\_x86.exe/q**.

### MSXML (Microsoft Core XML Services) 6.0 SP1 (x86)을 설치 하려면

****

1.  Microsoft 다운로드 센터 ()에서 [MICROSOFT MSXML (CORE XML Services) 6.0 sp1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) 소프트웨어 패키지를 다운로드 https://go.microsoft.com/fwlink/?LinkId=63266) 합니다 (.

2.  자동으로 설치 하려면 명령줄 옵션/quiet (예: **msiexec/i msxml6\_x86.msi/quiet**)를 사용 합니다.

### Microsoft 응용 프로그램 오류 보고를 설치 하려면

Microsoft 응용 프로그램 오류 보고를 설치할 때 *Appguid* 매개 변수를 사용 하 여 app-v 제품 코드를 지정 해야 합니다. 제품 코드는 각 App-v 클라이언트 유형 및 버전에 대해 고유 합니다. 다음 표에서 올바른 제품 코드를 선택 합니다.

**중요**  App-v 4.6 SP2 이상 버전에서는 더 이상 Microsoft 응용 프로그램 오류 보고 (dw20shared.msi)를 설치할 필요가 없습니다. 이제 app-v에서 Microsoft 오류 보고를 사용 합니다.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">버전</th>
<th align="left">데스크톱 클라이언트용 제품 코드</th>
<th align="left">원격 데스크톱 서비스용 클라이언트에 대 한 제품 코드</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 4.5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 4.5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 4.6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 4.6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 4.6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 4.6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 4.6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 4.6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

¹ App-V "언어" 릴리스.

**참고**  제품 코드를 찾아야 하는 경우 Orca.exe 데이터베이스 편집기 또는 유사한 도구를 사용 하 여 Windows Installer 파일을 검사 하 고 *ProductCode* 속성 값을 찾을 수 있습니다. Orca.exe 사용에 대 한 자세한 내용은 [Windows Installer 개발 도구](https://go.microsoft.com/fwlink/?LinkId=150008) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Release media의 **Support\\watson** 폴더에서 찾을 수 있는 dw20shared.msi Microsoft 응용 프로그램 오류 보고 설치 프로그램을 찾습니다.

2.  소프트웨어를 설치 하려면 다음 명령을 실행 합니다.

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Setup.msi 프로그램을 사용 하 여 앱 V 클라이언트 설치


다음 절차를 사용 하 여 App-v 클라이언트를 설치 합니다. 필수 구성 요소 소프트웨어가 모두 설치 되어 있는지 확인 합니다. \ [Template Token Value \] 버전 4.6 클라이언트의 경우 setup.msi 프로그램이 시스템을 확인 하 고 필수 구성 요소 소프트웨어가 설치 되어 있지 않은 경우 설치를 계속할 수 없다는 오류 메시지가 생성 됩니다. \ [Template 토큰 값 \]

**Setup.msi를 사용 하 여 응용 프로그램 가상화 클라이언트 설치**

1.  컴퓨터에 대 한 관리자 권한이 있는 계정으로 로그온 했는지 확인 합니다.

2.  승격 된 권한을 사용 하 여 명령 프롬프트 창을 연 다음 디렉터리를 설치 파일이 포함 된 폴더로 변경 합니다. App-v 클라이언트의 버전 4.6 또는 이후 버전을 설치할 때 컴퓨터의 운영 체제 32 비트 또는 64 비트에 대 한 올바른 설치 관리자를 사용 해야 합니다. 설치에 실패 하 고 잘못 된 설치 관리자를 사용 하는 경우 오류 메시지가 표시 됩니다.

3.  명령 프롬프트에 설치 명령 문자열을 입력 합니다. 또는 명령 파일을 만들어 명령 프롬프트에서 실행할 수 있습니다. VBScript 또는 Windows PowerShell 같은 스크립트 언어를 사용 하 여 명령을 실행할 수도 있습니다.

4.  다음 명령줄 예제에서는 여러 개의 선택적 매개 변수를 사용 하 여 setup.msi를 사용할 수 있는 방법을 보여 줍니다. 이러한 매개 변수에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "프로덕션 시스템" SWIPUBSVRTYPE = "HTTP/secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "SWIGLOBALDATA" D:\\AppVirt\\Global = "SWIUSERDATA" LOCALAPPDATA = "SWIFSDRIVE ^%\\Windows\\Application 가상화 Client" = "S"/q**

    **중요**  
    -   Windows Installer 스위치 "**/q**"를 사용 하 여 자동 설치를 수행 합니다.

    -   " **%** **% HomeDrive%**"의 "" 문자는 "" 이스케이프 문자 앞에와 야 합니다 **^** . 그렇지 않으면 Windows 명령 셸에서는 설치를 수행 하는 사용자의 값을 설정 합니다.

    -   설치 로깅을 설정 하려면 msiexec 스위치 **/l\ * v 파일 이름 .log**를 사용 합니다.

     

## 관련 항목


[명령줄을 사용하여 클라이언트를 설치하는 방법](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





