---
title: 셀프 서비스 포털 "HelpdeskURL"을 지역화하는 방법
description: 셀프 서비스 포털 "HelpdeskURL"을 지역화하는 방법
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826708"
---
# <span data-ttu-id="149a9-103">셀프 서비스 포털 "HelpdeskURL"을 지역화하는 방법</span><span class="sxs-lookup"><span data-stu-id="149a9-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="149a9-104">최종 사용자에 게 기본적으로 표시 되도록 자체 서비스 포털 URL의 지역화 된 버전을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="149a9-105">셀프 서비스 포털 URL은 **HelpdeskURL**매개 변수로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="149a9-106">다음 지침에 설명 된 대로 지역화 된 버전을 만드는 경우 Microsoft BitLocker 관리 및 모니터링 (MBAM)에서 지역화 된 버전을 찾아 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="149a9-107">MBAM이 지역화 된 버전을 찾지 못하면 매개 변수 **HelpDeskURL**에 대해 구성 된 URL이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="149a9-108">**참고**  다음 지침에서는 *SelfService* 가 셀프 서비스 포털의 기본 가상 디렉터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="149a9-109">셀프 서비스 포털을 구성할 때 다른 이름을 사용 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="149a9-110">셀프 서비스 포털 URL을 지역화 하려면</span><span class="sxs-lookup"><span data-stu-id="149a9-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="149a9-111">셀프 서비스 **포털을 구성한** 서버에서 &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **응용 프로그램 설정**으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="149a9-112">**작업** 창에서 **추가** 를 클릭 하 여 **응용 프로그램 설정 추가** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="149a9-113">**이름** 필드에 **HelpdeskURL**\ _ &lt; *언어* &gt; 를 입력 &lt; *Language* &gt; 합니다. 여기서 해당 언어는 해당 URL에 대 한 언어 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="149a9-114">예를 들어 스페인어로 값의 지역화 된 버전을 만들려면 `HelpdeskURL` 매개 변수의 이름을 **HelpdeskURL \ _es로**표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="149a9-115">언어 폴더의 이름은 **es**대신 언어 **중립 이름을 사용할** 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="149a9-116">최종 사용자의 브라우저가 **es** 로 설정 되 고 해당 폴더가 존재 하지 않는 경우, .net에서 정의 된 부모 로캘을 재귀적으로 검색 하 고 확인 하 여 &lt; &gt; 기본 Notice.txt 파일이 되기 전에\\SelfServiceWebsite\\es\\Notice.txt Mbam 서비스 설치 디렉터리를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="149a9-117">이 재귀적 대체는 .NET 리소스 로딩 규칙을 모방 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="149a9-118">사용할 수 있는 유효한 언어 코드 목록은 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="149a9-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="149a9-119">**값** 필드에 `HelpdeskURL` 최종 사용자에 게 표시 하려는 값의 지역화 된 버전을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="149a9-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="149a9-120">Related topics</span></span>


[<span data-ttu-id="149a9-121">조직에 대한 셀프 서비스 포털 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="149a9-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="149a9-122">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="149a9-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="149a9-123">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="149a9-124">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="149a9-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




