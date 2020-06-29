---
title: 셀프 서비스 포털을 브랜딩하는 방법
description: 셀프 서비스 포털을 브랜딩하는 방법
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825148"
---
# <span data-ttu-id="19abe-103">셀프 서비스 포털을 브랜딩하는 방법</span><span class="sxs-lookup"><span data-stu-id="19abe-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="19abe-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 셀프 서비스 포털을 설치한 후에는 회사 이름, 지원 센터 URL 및 "알림" 텍스트를 사용 하 여 셀프 서비스 포털에 브랜드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="19abe-105">세션 시간 제한 설정을 변경 하 여 지정 된 기간 동안 사용 하지 않을 경우 최종 사용자의 세션이 만료 되도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="19abe-106">셀프 서비스 포털에 대 한 세션 시간 초과 및 브랜딩 설정</span><span class="sxs-lookup"><span data-stu-id="19abe-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="19abe-107">최종 사용자의 세션에 대 한 시간 초과 기간을 설정 하려면 **인터넷 정보 서비스 관리자**를 시작 하거나 **inetmgr.exe**를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="19abe-108">**Sites** &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **ASP.NET** &gt; **세션 상태**를 찾고, **쿠키 설정** 아래의 **시간 제한** 값을 최종 사용자의 셀프 서비스 포털 세션이 만료 되는 간격 (분)으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="19abe-109">기본값은 5입니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-109">The default is 5.</span></span> <span data-ttu-id="19abe-110">설정이 시간 초과 되지 않도록 해제 하려면 값을 **0**으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="19abe-111">셀프 서비스 포털에 대 한 브랜딩 항목을 설정 하려면 **인터넷 정보 서비스 관리자**를 시작 하거나 **inetmgr.exe**를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="19abe-112">**사이트** &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **응용 프로그램 설정을**찾습니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="19abe-113">**이름** 열에서 변경 하려는 항목을 선택 하 고 사용 하려는 이름을 반영 하도록 기본값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="19abe-114">다음 표에는 설정할 수 있는 값이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19abe-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="19abe-115">주의</span><span class="sxs-lookup"><span data-stu-id="19abe-115">Caution</span></span>**  
    <span data-ttu-id="19abe-116">셀프 서비스 포털이 작동 하지 않게 되므로 이름 열 (CompanyName \ \*)의 값을 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="19abe-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## <span data-ttu-id="19abe-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="19abe-117">Related topics</span></span>


[<span data-ttu-id="19abe-118">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="19abe-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









