---
title: 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법
description: 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824493"
---
# <span data-ttu-id="ebb9c-103">클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="ebb9c-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="ebb9c-104">조직의 클라이언트 컴퓨터에서 Microsoft 사용자 CDN (콘텐츠 배달 네트워크)에 액세스할 수 없는 경우 다음 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="ebb9c-105">구성 해야 하는 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-105">Why you need to configure this:</span></span>**

<span data-ttu-id="ebb9c-106">클라이언트 컴퓨터는 특정 JavaScript 파일에 대 한 필수 액세스를 셀프 서비스 포털에 제공 하는 CDN에 대 한 액세스 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="ebb9c-107">클라이언트 컴퓨터가 CDN에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하지 않은 경우에는 최종 사용자가 로그인 하는 회사 이름과 계정만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="ebb9c-108">오류 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-108">No error message will be shown.</span></span>

<span data-ttu-id="ebb9c-109">**참고**  MBAM 2.5 SP1에는 JavaScript 파일이 제품에 포함 되어 있으므로이 섹션의 지침에 따라 인터넷에 액세스할 수 없는 클라이언트를 지원 하도록 SSP를 구성할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="ebb9c-110">클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ebb9c-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="ebb9c-111">CDN에서 다음 JavaScript 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="ebb9c-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="ebb9c-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="ebb9c-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="ebb9c-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="ebb9c-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="ebb9c-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="ebb9c-115">JavaScript 파일을 셀프 서비스 포털의 **Scripts** 디렉터리에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="ebb9c-116">이 디렉터리는 <em> &lt; mbam 셀프 서비스 설치 디렉터리 &gt; \\ </em> 셀프 서비스 Website\\Scripts.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="ebb9c-117">IIS (인터넷 정보 서비스) 관리자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="ebb9c-118">**사이트** &gt; **Microsoft BitLocker 관리 및 모니터링**을 확장 하 고 **SelfService**를 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="ebb9c-119">참고</span><span class="sxs-lookup"><span data-stu-id="ebb9c-119">Note</span></span>**  
   <span data-ttu-id="ebb9c-120">*SelfService* 는 기본 가상 디렉터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="ebb9c-121">구성 중에이 디렉터리에 대해 다른 이름을 선택한 경우에는이 지침에서 *SelfService* 을 선택한 이름으로 바꿔야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="ebb9c-122">가운데 창에서 **응용 프로그램 설정을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="ebb9c-123">다음 목록에 있는 각 항목에 대해 &lt; *virtual directory* &gt; /SelfService/(또는 구성 중에 선택한 이름)을 사용 하 여 새 위치를 참조 하는 응용 프로그램 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="ebb9c-124">예를 들어 가상 디렉터리 경로는/selfservice/Scripts/jQuery-1.10.2.min.js와 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="ebb9c-125">jQueryPath:/ &lt; *virtual directory* &gt; /Scripts/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="ebb9c-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="ebb9c-126">jQueryValidatePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="ebb9c-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="ebb9c-127">jQueryValidateUnobtrusivePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="ebb9c-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="ebb9c-128">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ebb9c-128">Related topics</span></span>


[<span data-ttu-id="ebb9c-129">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="ebb9c-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="ebb9c-130">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="ebb9c-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ebb9c-131">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ebb9c-132">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb9c-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





