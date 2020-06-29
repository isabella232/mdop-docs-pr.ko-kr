---
title: 셀프 서비스 포털 브랜딩 및 세션 시간 제한을 설정하는 방법
description: 셀프 서비스 포털 브랜딩 및 세션 시간 제한을 설정하는 방법
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812532"
---
# 셀프 서비스 포털 브랜딩 및 세션 시간 제한을 설정하는 방법


셀프 서비스 포털을 구성한 후에는 회사 이름, 지원 센터 URL 및 "알림" 텍스트를 사용 하 여 브랜드를 지정할 수 있습니다. 세션 시간 제한 설정을 변경 하 여 지정 된 기간 동안 사용 하지 않을 경우 최종 사용자의 세션이 만료 되도록 할 수도 있습니다.

**참고**  
또한 **Enable-MbamWebApplication** Windows PowerShell CMDLET 또는 Mbam 서버 구성 마법사를 사용 하 여 셀프 서비스 포털을 브랜딩 할 수 있습니다. 마법사를 사용 하는 방법에 대 한 지침은 [MBAM 2.5 웹 응용 프로그램을 구성 하는 방법을](how-to-configure-the-mbam-25-web-applications.md)참조 하세요.



**참고**  
다음 지침에서는 *SelfService* 가 셀프 서비스 포털의 기본 가상 디렉터리 이름입니다. 셀프 서비스 포털을 구성할 때 다른 이름을 사용 했을 수 있습니다.



**셀프 서비스 포털에 대 한 세션 시간 초과 및 브랜딩 설정**

1.  최종 사용자의 세션에 대 한 시간 초과 기간을 설정 하려면 **인터넷 정보 서비스 관리자**를 시작 하거나 **inetmgr.exe**를 실행 합니다.

2.  **Sites** &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **ASP.NET** &gt; **세션 상태**를 찾고, **쿠키 설정** 아래의 **시간 제한** 값을 최종 사용자의 셀프 서비스 포털 세션이 만료 되는 간격 (분)으로 변경 합니다. 기본값은 **5**입니다. 설정이 시간 초과 되지 않도록 해제 하려면 값을 **0**으로 설정 합니다.

3.  셀프 서비스 포털에 대 한 브랜딩 항목을 설정 하려면 **인터넷 정보 서비스 관리자** 를 시작 하거나 **inetmgr.exe**를 실행 합니다.

4.  **사이트** &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **응용 프로그램 설정을**찾습니다.

5.  **이름** 열에서 변경 하려는 항목을 선택 하 고 사용 하려는 이름을 반영 하도록 기본값을 변경 합니다. 다음 표에는 설정할 수 있는 값이 나와 있습니다.

    **주의**  
    셀프 서비스 포털의 작동이 중지 될 수 있으므로 이름 열 (CompanyName \ *)의 값을 변경 하지 마세요.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## 관련 항목


[조직에 대한 셀프 서비스 포털 사용자 지정](customizing-the-self-service-portal-for-your-organization.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





