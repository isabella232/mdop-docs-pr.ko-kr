---
title: Microsoft 고급 그룹 정책 관리 4.0 SP3 릴리스 정보
description: Microsoft 고급 그룹 정책 관리 4.0 SP3 릴리스 정보
author: dansimp
ms.assetid: 955d7674-a8d9-4fc5-b18a-5a1639e38014
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 6e0da04d67b3d29135071e0bc82b8e01789e4e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818523"
---
# <span data-ttu-id="07de0-103">Microsoft 고급 그룹 정책 관리 4.0 SP3 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="07de0-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>


<span data-ttu-id="07de0-104">이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="07de0-105">이 릴리스 정보는 Microsoft AGPM (고급 그룹 정책 관리) 4.0 서비스 Pack3 (SP3)를 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="07de0-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="07de0-106">이 릴리스 정보에는 AGPM 4.0 SP3을 성공적으로 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-106">These release notes contain information that is required to successfully install AGPM4.0 SP3 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="07de0-107">이러한 릴리스 정보와 다른 AGPM 설명서 사이에 차이가 있는 경우에는 신뢰할 수 있는 최신 변경 사항을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="07de0-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="07de0-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="07de0-109">AGPM 4.0 SP3의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="07de0-109">AGPM4.0 SP3 known issues</span></span>


<span data-ttu-id="07de0-110">이 섹션에서는 AGPM 4.0 SP3의 알려진 문제에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-110">This section describes the known issues for AGPM 4.0 SP3.</span></span>

### <span data-ttu-id="07de0-111">Windows 10에서 AGPM 설치 실패</span><span class="sxs-lookup"><span data-stu-id="07de0-111">AGPM installation fails in Windows 10</span></span>

<span data-ttu-id="07de0-112">AGPM은 설치 하는 동안 WCF (Windows Communication Foundation) 비 Http-Activation 기능을 내부적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-112">AGPM internally enables the Windows Communication Foundation (WCF)-NonHTTP-Activation feature during installation.</span></span> <span data-ttu-id="07de0-113">Windows 10에는 wcf가 비 Http 활성화 기능을 사용 하도록 설정한 후에 Windows를 다시 시작 하 라는 요구 사항이 WCF에 포함 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-113">In Windows 10, WCF now includes a requirement to restart Windows after enabling the WCF NonHTTP-Activation feature.</span></span> <span data-ttu-id="07de0-114">그러나 현재 AGPM 설치 관리자 코드는이 다시 시작 요구 사항을 처리 하지 않으며 서비스가 활성화 될 때까지 대기 하는 동안 응답을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-114">However, the current AGPM installer code does not handle this restart requirement and stops responding while it waits for the service to be activated.</span></span>

<span data-ttu-id="07de0-115">**해결 방법:** AGPM 설치 관리자를 실행 하기 전에 WCF 비 HTTP 활성화 기능을 사용 하도록 설정한 다음 Windows를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-115">**Workaround:** Before you run the AGPM installer, enable the WCF Non-HTTP Activation feature and then restart Windows.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="07de0-116">AGPM 서버 설정을 변경 하려고 하면 제어판의 "제거" 도구가 작동 하지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="07de0-116">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="07de0-117">AGPM 서버 설정을 변경 하려고 할 때 프로그램을 제거 하거나 변경 하는 데 사용 하는 제어판의 도구가 작동 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-117">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="07de0-118">**해결 방법:** 제어판을 사용 하 여 AGPM 서버 설정을 변경 하기 전에 AGPM 보관 폴더의 복사본을 만들어 보세요.</span><span class="sxs-lookup"><span data-stu-id="07de0-118">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="07de0-119">그런 다음 Setup.exe를 사용 하 여 AGPM 서버를 다시 설치 하 고 원하는 구성 매개 변수를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-119">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="07de0-120">보고서는 그룹 정책 개체에 추가 된 링크를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-120">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="07de0-121">AGPM 설정 및 차이점 보고서에는 GPO (그룹 정책 개체)에 추가 된 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-121">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="07de0-122">**해결 방법:** 보고서의 링크를 보려면 GPMC (그룹 정책 관리) 콘솔에서 GPO를 선택한 다음 오른쪽 창에서 **설정** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-122">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="07de0-123">보고서에 모든 선택 옵션 속성 설정이 표시 되지 않음</span><span class="sxs-lookup"><span data-stu-id="07de0-123">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="07de0-124">AGPM 설정 및 차이점 보고서에는 그룹 정책 개체 편집기의 **선택 옵션 속성** 창에서 선택한 설정이 모두 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-124">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="07de0-125">**해결 방법:** GPMC를 사용 하 여 보고서에서 선택한 **선택 옵션의 속성** 설정을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-125">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="07de0-126">특정 브라우저에서 보고서에 표시 및 숨기기 탭이 표시 되지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="07de0-126">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="07de0-127">Google Chrome 또는 Mozilla Firefox에서 보고서를 볼 때 AGPM 설정 및 차이점 보고서의 오른쪽에 있는 **표시** 및 **숨기기** 탭이 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-127">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="07de0-128">**해결 방법:** Internet Explorer 브라우저를 사용 하 여 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-128">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="07de0-129">AGPM 설정 및 차이점 보고서에 GPMC 보고서의 다른 콘텐츠가 표시 될 수 있음</span><span class="sxs-lookup"><span data-stu-id="07de0-129">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="07de0-130">AGPM 설정 및 차이점 보고서에는 GPMC의 보고서와 동일한 콘텐츠가 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-130">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="07de0-131">**해결 방법:** GPMC를 사용 하 여 AGPM 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-131">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="07de0-132">도메인 컨트롤러가 오프 라인인 경우 AGPM 서비스가 시작 되지 않음</span><span class="sxs-lookup"><span data-stu-id="07de0-132">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="07de0-133">Windows® 8 운영 체제 이상 운영 체제의 도메인 컨트롤러에 AGPM 서비스가 설치 되어 있으면 도메인 컨트롤러가 오프 라인인 경우 서비스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-133">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="07de0-134">**해결 방법:** 도메인 컨트롤러가 온라인 상태 이면 AGPM 서비스를 수동으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-134">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="07de0-135">Agpm 4.0 release plus hotfix1에서 업그레이드 하는 경우 agpm 서버를 AGPM 4.0 SP2로 업그레이드 하는 것이 차단 됨</span><span class="sxs-lookup"><span data-stu-id="07de0-135">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="07de0-136">AGPM 서버를 AGPM 4.0로 업그레이드 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-136">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="07de0-137">SP2 4.0 서버를 설치한 다음 AGPM 4.0 이라는 AGPM 핫픽스를 설치 하면 HTML 보고서의 잘못 된 차이점을 보고 합니다 (기술 자료 문서 [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)참조), 업그레이드가 실패 하 고 완료할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-137">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="07de0-138">**해결 방법:** AGPM 4.0 서버를 제거한 다음 AGPM 4.0 SP2를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-138">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="07de0-139">보고서가 조직 구성 단위 링크를 표시 하지 않음</span><span class="sxs-lookup"><span data-stu-id="07de0-139">Reports do not display organizational unit links</span></span>

<span data-ttu-id="07de0-140">제어 되지 않은 GPO를 조직 구성 단위에 연결한 다음 AGPM을 사용 하 여 해당 GPO를 제어 하는 경우 AGPM 설정 및 차이점 보고서에 조직 구성 단위 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-140">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="07de0-141">**해결 방법:** **변경 설정** 노드의 **제어** 탭에서 gpo를 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **gpo 링크** 를 클릭 하 여 조직 링크를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-141">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="07de0-142">또는 GPMC를 사용 하 여 **범위** 탭에서 GPO에 대 한 링크를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-142">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="07de0-143">Agpm 클라이언트 변경, 복구 또는 제거 대화 상자에서 뒤로 단추를 클릭 하면 AGPM에서 오류를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-143">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="07de0-144">제어판에서 **프로그램 및 기능** 을 찾은 다음 **Microsoft 고급 그룹 정책 관리-클라이언트**를 선택 하면 오류 메시지가 표시 되 고 **수정을** 클릭 한 다음 **agpm 클라이언트 변경, 복구 또는 제거** 대화 상자에서 **뒤로** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-144">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="07de0-145">**해결 방법:** **취소** 를 클릭 하 여 오류를 지운 다음 프로세스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-145">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="07de0-146">**수정을** 클릭 한 후에는 **뒤로** 단추를 클릭 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="07de0-146">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="07de0-147">승인자가 GPO를 배포 하 고 메모를 입력 하면 기록 창에 주석이 표시 되지 않음</span><span class="sxs-lookup"><span data-stu-id="07de0-147">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="07de0-148">편집자 역할이 있는 사용자가 GPO 배포 요청을 제출 하 고 승인자 역할이 있는 사용자가 GPO를 배포 하 고 메모를 입력 하면 **기록** 창에 주석이 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-148">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="07de0-149">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="07de0-149">**Workaround:** None.</span></span>

### <span data-ttu-id="07de0-150">GPO 권한 변경 제거의 AGPM 기본 동작을 재정의 하는 메커니즘이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-150">Added mechanism to override AGPM default behavior of removing GPO permission changes</span></span>

<span data-ttu-id="07de0-151">HF02의 경우 AGPM이 레지스트리 키를 추가 하 여 기본 AGPM GPO 권한 동작을 재정의할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de0-151">As of HF02, AGPM has added a registry key to enable overriding the default AGPM GPO permission behavior.</span></span> <span data-ttu-id="07de0-152">자세한 내용은 [AGPM을 통한 그룹 정책 개체 사용 권한에 대 한 변경 내용이 무시 됨](https://support.microsoft.com/kb/3174540) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07de0-152">For more information, please see [Changes to Group Policy object permissions through AGPM are ignored](https://support.microsoft.com/kb/3174540)</span></span>

## <span data-ttu-id="07de0-153">관련 항목</span><span class="sxs-lookup"><span data-stu-id="07de0-153">Related topics</span></span>


[<span data-ttu-id="07de0-154">고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="07de0-154">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="07de0-155">AGPM 4.0 SP3의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="07de0-155">What's New in AGPM 4.0 SP3</span></span>](whats-new-in-agpm-40-sp3.md)

 

 





