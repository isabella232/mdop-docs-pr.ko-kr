---
title: Microsoft 고급 그룹 정책 관리 4.0 SP2 릴리스 정보
description: Microsoft 고급 그룹 정책 관리 4.0 SP2 릴리스 정보
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820388"
---
# <span data-ttu-id="2d449-103">Microsoft 고급 그룹 정책 관리 4.0 SP2 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="2d449-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>


<span data-ttu-id="2d449-104">이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="2d449-105">이 릴리스 정보는 Microsoft AGPM (고급 그룹 정책 관리) 4.0 서비스 Pack2 (SP2)를 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="2d449-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="2d449-106">이 릴리스 정보에는 AGPM 4.0 SP2를 성공적으로 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-106">These release notes contain information that is required to successfully install AGPM4.0 SP2 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="2d449-107">이러한 릴리스 정보와 다른 AGPM 설명서 사이에 차이가 있는 경우에는 신뢰할 수 있는 최신 변경 사항을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d449-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="2d449-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="2d449-109">AGPM 4.0 SP2의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="2d449-109">AGPM4.0 SP2 known issues</span></span>


<span data-ttu-id="2d449-110">이 섹션에서는 AGPM 4.0 SP2의 알려진 문제에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-110">This section describes the known issues for AGPM 4.0 SP2.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="2d449-111">AGPM 서버 설정을 변경 하려고 하면 제어판의 "제거" 도구가 작동 하지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="2d449-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="2d449-112">AGPM 서버 설정을 변경 하려고 할 때 프로그램을 제거 하거나 변경 하는 데 사용 하는 제어판의 도구가 작동 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-112">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="2d449-113">**해결 방법:** 제어판을 사용 하 여 AGPM 서버 설정을 변경 하기 전에 AGPM 보관 폴더의 복사본을 만들어 보세요.</span><span class="sxs-lookup"><span data-stu-id="2d449-113">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="2d449-114">그런 다음 Setup.exe를 사용 하 여 AGPM 서버를 다시 설치 하 고 원하는 구성 매개 변수를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-114">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="2d449-115">보고서는 그룹 정책 개체에 추가 된 링크를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="2d449-116">AGPM 설정 및 차이점 보고서에는 GPO (그룹 정책 개체)에 추가 된 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="2d449-117">**해결 방법:** 보고서의 링크를 보려면 GPMC (그룹 정책 관리) 콘솔에서 GPO를 선택한 다음 오른쪽 창에서 **설정** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-117">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="2d449-118">보고서에 모든 선택 옵션 속성 설정이 표시 되지 않음</span><span class="sxs-lookup"><span data-stu-id="2d449-118">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="2d449-119">AGPM 설정 및 차이점 보고서에는 그룹 정책 개체 편집기의 **선택 옵션 속성** 창에서 선택한 설정이 모두 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-119">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="2d449-120">**해결 방법:** GPMC를 사용 하 여 보고서에서 선택한 **선택 옵션의 속성** 설정을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-120">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="2d449-121">특정 브라우저에서 보고서에 표시 및 숨기기 탭이 표시 되지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="2d449-121">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="2d449-122">Google Chrome 또는 Mozilla Firefox에서 보고서를 볼 때 AGPM 설정 및 차이점 보고서의 오른쪽에 있는 **표시** 및 **숨기기** 탭이 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-122">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="2d449-123">**해결 방법:** Internet Explorer 브라우저를 사용 하 여 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-123">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="2d449-124">AGPM 설정 및 차이점 보고서에 GPMC 보고서의 다른 콘텐츠가 표시 될 수 있음</span><span class="sxs-lookup"><span data-stu-id="2d449-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="2d449-125">AGPM 설정 및 차이점 보고서에는 GPMC의 보고서와 동일한 콘텐츠가 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-125">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="2d449-126">**해결 방법:** GPMC를 사용 하 여 AGPM 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-126">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="2d449-127">도메인 컨트롤러가 오프 라인인 경우 AGPM 서비스가 시작 되지 않음</span><span class="sxs-lookup"><span data-stu-id="2d449-127">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="2d449-128">Windows® 8 운영 체제 이상 운영 체제의 도메인 컨트롤러에 AGPM 서비스가 설치 되어 있으면 도메인 컨트롤러가 오프 라인인 경우 서비스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-128">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="2d449-129">**해결 방법:** 도메인 컨트롤러가 온라인 상태 이면 AGPM 서비스를 수동으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-129">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="2d449-130">Agpm 4.0 release plus hotfix1에서 업그레이드 하는 경우 agpm 서버를 AGPM 4.0 SP2로 업그레이드 하는 것이 차단 됨</span><span class="sxs-lookup"><span data-stu-id="2d449-130">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="2d449-131">AGPM 서버를 AGPM 4.0로 업그레이드 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="2d449-132">SP2 4.0 서버를 설치한 다음 AGPM 4.0 이라는 AGPM 핫픽스를 설치 하면 HTML 보고서의 잘못 된 차이점을 보고 합니다 (기술 자료 문서 [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)참조), 업그레이드가 실패 하 고 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-132">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="2d449-133">**해결 방법:** AGPM 4.0 서버를 제거한 다음 AGPM 4.0 SP2를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-133">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="2d449-134">보고서가 조직 구성 단위 링크를 표시 하지 않음</span><span class="sxs-lookup"><span data-stu-id="2d449-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="2d449-135">제어 되지 않은 GPO를 조직 구성 단위에 연결한 다음 AGPM을 사용 하 여 해당 GPO를 제어 하는 경우 AGPM 설정 및 차이점 보고서에 조직 구성 단위 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="2d449-136">**해결 방법:** **변경 설정** 노드의 **제어** 탭에서 gpo를 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **gpo 링크** 를 클릭 하 여 조직 링크를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-136">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="2d449-137">또는 GPMC를 사용 하 여 **범위** 탭에서 GPO에 대 한 링크를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="2d449-138">Agpm 클라이언트 변경, 복구 또는 제거 대화 상자에서 뒤로 단추를 클릭 하면 AGPM에서 오류를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-138">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="2d449-139">제어판에서 **프로그램 및 기능** 을 찾은 다음 **Microsoft 고급 그룹 정책 관리-클라이언트**를 선택 하면 오류 메시지가 표시 되 고 **수정을** 클릭 한 다음 **agpm 클라이언트 변경, 복구 또는 제거** 대화 상자에서 **뒤로** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-139">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="2d449-140">**해결 방법:** **취소** 를 클릭 하 여 오류를 지운 다음 프로세스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-140">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="2d449-141">**수정을** 클릭 한 후에는 **뒤로** 단추를 클릭 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="2d449-141">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="2d449-142">승인자가 GPO를 배포 하 고 메모를 입력 하면 기록 창에 주석이 표시 되지 않음</span><span class="sxs-lookup"><span data-stu-id="2d449-142">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="2d449-143">편집자 역할이 있는 사용자가 GPO 배포 요청을 제출 하 고 승인자 역할이 있는 사용자가 GPO를 배포 하 고 메모를 입력 하면 **기록** 창에 주석이 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d449-143">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="2d449-144">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="2d449-144">**Workaround:** None.</span></span>

## <span data-ttu-id="2d449-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2d449-145">Related topics</span></span>


[<span data-ttu-id="2d449-146">고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="2d449-146">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="2d449-147">AGPM 4.0 SP2의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="2d449-147">What's New in AGPM 4.0 SP2</span></span>](whats-new-in-agpm-40-sp2.md)

 

 





