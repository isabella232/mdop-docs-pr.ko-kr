---
title: 셀프 서비스 포털 알림 텍스트를 지역화하는 방법
description: 셀프 서비스 포털 알림 텍스트를 지역화하는 방법
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826713"
---
# <span data-ttu-id="280da-103">셀프 서비스 포털 알림 텍스트를 지역화하는 방법</span><span class="sxs-lookup"><span data-stu-id="280da-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="280da-104">셀프 서비스 포털에서 기본적으로 최종 사용자에 게 표시 되도록 지역화 된 알림 텍스트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="280da-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="280da-105">알림 텍스트를 표시 하는 Notice.txt 파일의 루트 디렉터리는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="280da-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="280da-106">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="280da-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="280da-107">지역화 된 알림 텍스트를 표시 하려면 지역화 Notice.txt 파일을 만든 후 다음 예제 디렉터리의 특정 언어 폴더 아래에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="280da-108">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="280da-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

<span data-ttu-id="280da-109">**참고**  **응용 프로그램 설정**에서 **NoticeTextPath** 항목을 사용 하 여 경로를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="280da-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="280da-110">MBAM은 다음 규칙에 따라 알림 텍스트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="280da-111">해당 언어 폴더에서 지역화 된 **Notice.txt** 파일을 만드는 경우 기본 **Notice.txt** 파일이 있으면 mbam에 지역화 된 알림 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="280da-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="280da-112">기본 **Notice.txt** 파일이 없으면 기본 파일이 없음을 나타내는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="280da-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="280da-113">MBAM이 Notice.txt 파일의 지역화 된 버전을 찾지 못하면 기본 Notice.txt 파일에 텍스트를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="280da-114">MBAM이 기본 Notice.txt 파일을 찾지 못하면 셀프 서비스 포털에 기본 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="280da-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="280da-115">**참고**  최종 사용자의 브라우저가 해당 언어 하위 폴더 또는 Notice.txt 없는 언어로 설정 된 경우에는 다음 루트 디렉터리의 Notice.txt 파일에 있는 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="280da-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="280da-116">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="280da-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

 

**<span data-ttu-id="280da-117">지역화 된 Notice.txt 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="280da-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="280da-118">셀프 서비스 포털을 구성한 서버에서 &lt; *Language* &gt; 다음 예제 디렉터리에 언어 폴더를 만들고 여기서 &lt; *언어* 는 &gt; 지역화 된 언어의 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="280da-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="280da-119">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website</span><span class="sxs-lookup"><span data-stu-id="280da-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website</span></span>\\

    <span data-ttu-id="280da-120">**참고**  일부 언어 폴더가 이미 있으므로 폴더를 만들 필요가 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="280da-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="280da-121">언어 폴더를 만들어야 하는 경우 언어 폴더에 사용할 수 있는 유효한 이름 목록에 대 한 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947) 를 참조 하세요 &lt; *Language* &gt; .</span><span class="sxs-lookup"><span data-stu-id="280da-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="280da-122">지역화 된 알림 텍스트를 포함 하는 Notice.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="280da-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="280da-123">Notice.txt 파일을 &lt; *언어* &gt; 폴더에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="280da-124">예를 들어 스페인어로 지역화 된 Notice.txt 파일을 만들려면 다음 예제 디렉터리에 지역화 된 Notice.txt 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="280da-125">&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\Es-es</span><span class="sxs-lookup"><span data-stu-id="280da-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="280da-126">언어 폴더의 이름은 **es**대신 언어 **중립 이름을 사용할** 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="280da-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="280da-127">최종 사용자의 브라우저가 **es** 로 설정 되 고 해당 폴더가 존재 하지 않는 경우, .net에서 정의 된 부모 로캘을 재귀적으로 검색 하 고 확인 하 여 &lt; &gt; 기본 Notice.txt 파일이 되기 전에\\SelfServiceWebsite\\es\\Notice.txt Mbam 서비스 설치 디렉터리를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="280da-128">이 재귀적 대체는 .NET 리소스 로딩 규칙을 모방 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="280da-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="280da-129">Related topics</span></span>


[<span data-ttu-id="280da-130">조직에 대한 셀프 서비스 포털 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="280da-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="280da-131">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="280da-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="280da-132">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="280da-133">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="280da-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





