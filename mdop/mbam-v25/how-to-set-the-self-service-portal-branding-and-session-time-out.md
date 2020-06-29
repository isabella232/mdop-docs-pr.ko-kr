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
# <span data-ttu-id="ca231-103">셀프 서비스 포털 브랜딩 및 세션 시간 제한을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="ca231-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="ca231-104">셀프 서비스 포털을 구성한 후에는 회사 이름, 지원 센터 URL 및 "알림" 텍스트를 사용 하 여 브랜드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="ca231-105">세션 시간 제한 설정을 변경 하 여 지정 된 기간 동안 사용 하지 않을 경우 최종 사용자의 세션이 만료 되도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="ca231-106">참고</span><span class="sxs-lookup"><span data-stu-id="ca231-106">Note</span></span>**  
<span data-ttu-id="ca231-107">또한 **Enable-MbamWebApplication** Windows PowerShell CMDLET 또는 Mbam 서버 구성 마법사를 사용 하 여 셀프 서비스 포털을 브랜딩 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="ca231-108">마법사를 사용 하는 방법에 대 한 지침은 [MBAM 2.5 웹 응용 프로그램을 구성 하는 방법을](how-to-configure-the-mbam-25-web-applications.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca231-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="ca231-109">참고</span><span class="sxs-lookup"><span data-stu-id="ca231-109">Note</span></span>**  
<span data-ttu-id="ca231-110">다음 지침에서는 *SelfService* 가 셀프 서비스 포털의 기본 가상 디렉터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="ca231-111">셀프 서비스 포털을 구성할 때 다른 이름을 사용 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="ca231-112">셀프 서비스 포털에 대 한 세션 시간 초과 및 브랜딩 설정</span><span class="sxs-lookup"><span data-stu-id="ca231-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="ca231-113">최종 사용자의 세션에 대 한 시간 초과 기간을 설정 하려면 **인터넷 정보 서비스 관리자**를 시작 하거나 **inetmgr.exe**를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="ca231-114">**Sites** &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **ASP.NET** &gt; **세션 상태**를 찾고, **쿠키 설정** 아래의 **시간 제한** 값을 최종 사용자의 셀프 서비스 포털 세션이 만료 되는 간격 (분)으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="ca231-115">기본값은 **5**입니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-115">The default value is **5**.</span></span> <span data-ttu-id="ca231-116">설정이 시간 초과 되지 않도록 해제 하려면 값을 **0**으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="ca231-117">셀프 서비스 포털에 대 한 브랜딩 항목을 설정 하려면 **인터넷 정보 서비스 관리자** 를 시작 하거나 **inetmgr.exe**를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="ca231-118">**사이트** &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **응용 프로그램 설정을**찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="ca231-119">**이름** 열에서 변경 하려는 항목을 선택 하 고 사용 하려는 이름을 반영 하도록 기본값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="ca231-120">다음 표에는 설정할 수 있는 값이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="ca231-121">주의</span><span class="sxs-lookup"><span data-stu-id="ca231-121">Caution</span></span>**  
    <span data-ttu-id="ca231-122">셀프 서비스 포털의 작동이 중지 될 수 있으므로 이름 열 (CompanyName \ \*)의 값을 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ca231-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



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





## <span data-ttu-id="ca231-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ca231-123">Related topics</span></span>


[<span data-ttu-id="ca231-124">조직에 대한 셀프 서비스 포털 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="ca231-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="ca231-125">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="ca231-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ca231-126">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ca231-127">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca231-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





