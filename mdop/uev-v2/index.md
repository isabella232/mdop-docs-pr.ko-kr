---
title: Microsoft UE-V (User Experience Virtualization) 2. x
description: Microsoft UE-V (User Experience Virtualization) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795970"
---
# <span data-ttu-id="7ca96-103">Microsoft UE-V (User Experience Virtualization) 2. x</span><span class="sxs-lookup"><span data-stu-id="7ca96-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="7ca96-104">이 설명서는 MDOP (Microsoft 데스크톱 최적화 팩)에 포함 된 for UE-V for 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="7ca96-105">Windows 10 Enterprise에 포함 되어 있는 최신 버전의 UE-V에 대 한 자세한 내용은 [Ue-v 시작](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ca96-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="7ca96-106">UE-V (사용자 환경 가상화) 2.0 또는 2.1을 구현 하 여 사용자의 응용 프로그램 설정 및 Windows OS 설정을 캡처하고 중앙 집중화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="7ca96-107">그런 다음 데스크톱 컴퓨터, 랩톱 또는 VDI (가상 데스크톱 인프라) 세션과 같은 사용자의 엔터프라이즈 액세스 장치에 이러한 설정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="7ca96-108">UE-V를 사용 하 여 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="7ca96-109">동기화 할 응용 프로그램 및 데스크톱 설정 지정</span><span class="sxs-lookup"><span data-stu-id="7ca96-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="7ca96-110">엔터프라이즈 전체에서 사용자가 작업하는 모든 시간과 위치에 설정 제공</span><span class="sxs-lookup"><span data-stu-id="7ca96-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="7ca96-111">타사 또는 기간 업무 응용 프로그램의 사용자 지정 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="7ca96-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="7ca96-112">하드웨어를 대체 하거나 업그레이드 한 후 또는 가상 컴퓨터를 초기 상태로 reimaging 후에 설정 복구</span><span class="sxs-lookup"><span data-stu-id="7ca96-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="7ca96-113">UE-V 2. x의 구성 요소</span><span class="sxs-lookup"><span data-stu-id="7ca96-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="7ca96-114">이 다이어그램은 배포 된 UE-V 구성 요소가 함께 작동 하 여 설정을 동기화 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![uev2 아키텍처 다이어그램](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ca96-116">구성 요소</span><span class="sxs-lookup"><span data-stu-id="7ca96-116">Component</span></span></th>
<th align="left"><span data-ttu-id="7ca96-117">함수</span><span class="sxs-lookup"><span data-stu-id="7ca96-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7ca96-118">UE-V 에이전트</span><span class="sxs-lookup"><span data-stu-id="7ca96-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-119">설정을 동기화 해야 하는 모든 컴퓨터에 설치 되어 있는 경우 <strong> Ue-v agent가 </strong> 설정 변경에 대해 등록 된 응용 프로그램 및 운영 체제를 모니터링 한 다음 해당 설정을 컴퓨터 간에 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7ca96-120">설정 패키지</span><span class="sxs-lookup"><span data-stu-id="7ca96-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-121">응용 프로그램 설정 및 Windows 설정은 <strong> Ue-v agent에서 만든 설정 패키지에 저장 됩니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="7ca96-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="7ca96-122">설정 패키지가 빌드되어 로컬에 저장되며 설정 저장소 위치에 복사됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="7ca96-123">데스크톱 응용 프로그램에 대 한 설정 값은 <strong> </strong> 사용자가 응용 프로그램을 닫을 때 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="7ca96-124">Windows 설정에 대 한 값 <strong> </strong> 은 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있거나 컴퓨터에서 원격으로 연결이 끊어질 때 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="7ca96-125">동기화 공급자는 설정 패키지에서 응용 프로그램 또는 운영 체제 설정을 읽고 동기화 할 때를 결정 <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7ca96-126">설정 저장소 위치</span><span class="sxs-lookup"><span data-stu-id="7ca96-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-127">사용자가 액세스할 수 있는 표준 네트워크 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="7ca96-128">UE-V Agent는 위치를 확인 하 고 사용자 설정을 저장 하 고 검색할 숨겨진 시스템 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7ca96-129">설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="7ca96-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-130">UE-V는 XML 파일을 설정 위치 템플릿으로 사용 하 여 데스크톱 응용 프로그램 설정 및 사용자 컴퓨터 간에 Windows 데스크톱 설정을 모니터링 하 고 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="7ca96-131">기본적으로 일부 설정 위치 템플릿은 UE-V에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="7ca96-132"><a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">사용자 지정 응용 프로그램의 설정 동기화를 관리 하 여 사용자 지정 설정 위치 템플릿을 만들거나 편집 하거나 유효성을 검사할 수도 있습니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="7ca96-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7ca96-133">참고</span><span class="sxs-lookup"><span data-stu-id="7ca96-133">Note</span></span></strong><br/><p><span data-ttu-id="7ca96-134">Windows 앱에는 설정 위치 템플릿이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7ca96-135">Windows 앱 목록</span><span class="sxs-lookup"><span data-stu-id="7ca96-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-136">Windows 앱에 대 한 설정이 동적으로 캡처되고 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="7ca96-137">앱 개발자는 각 앱에 대해 동기화 되는 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="7ca96-138">UE-V는 관리 되는 앱 목록을 사용 하 여 설정 동기화를 사용 하도록 설정 된 Windows 앱을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="7ca96-139">기본적으로이 목록에는 대부분의 Windows 앱이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="7ca96-140">다음 절차에 따라 Windows 앱 목록에서 응용 프로그램을 추가 하거나 제거할 수 있습니다 <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="7ca96-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="7ca96-141">사용자 지정 응용 프로그램의 설정 동기화 관리</span><span class="sxs-lookup"><span data-stu-id="7ca96-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="7ca96-142">이러한 UE-V 구성 요소를 사용 하 여 타사 또는 lob (기간 업무) 응용 프로그램에 대 한 사용자 지정 템플릿을 만들고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7ca96-143">UE-V 생성기</span><span class="sxs-lookup"><span data-stu-id="7ca96-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-144"><strong> </strong> 사용자 컴퓨터에 배포할 수 있는 사용자 지정 설정 위치 템플릿을 만들려면 ue-v 생성기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="7ca96-145">또한 UE-V 생성기를 통해 기존 서식 파일을 편집 하거나 다른 XML 편집기를 사용 하 여 만든 서식 파일의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7ca96-146">설정 서식 파일 카탈로그</span><span class="sxs-lookup"><span data-stu-id="7ca96-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ca96-147"><strong>설정 템플릿 카탈로그는 </strong> ue-v 컴퓨터의 폴더 경로 이거나 사용자 지정 설정 위치 템플릿을 저장 하는 SMB (서버 메시지 블록) 네트워크 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="7ca96-148">UE-V Agent가 하루에 한 번이 위치를 확인 하 고, 새 템플릿 또는 업데이트 된 템플릿을 검색 하 고, 동기화 동작을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="7ca96-149">UE-V 기본 설정 위치 템플릿만 사용 하는 경우 설정 템플릿 카탈로그는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="7ca96-150">설정 배포 카탈로그에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> ue-v 설정 템플릿 카탈로그 구성을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="7ca96-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![ue-v 생성자 프로세스](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="7ca96-152">설정이 기본적으로 동기화 됨</span><span class="sxs-lookup"><span data-stu-id="7ca96-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="7ca96-153">UE-V는 기본적으로 이러한 응용 프로그램에 대 한 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="7ca96-154">전체 목록 및 자세한 내용은 [ue-v 배포에서 자동으로 동기화 되는 설정을](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ca96-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="7ca96-155">Microsoft Office 2013 응용 프로그램 (UE-V 2.1 SP1 및 2.1)</span><span class="sxs-lookup"><span data-stu-id="7ca96-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="7ca96-156">Microsoft Office 2010 응용 프로그램 (UE-V 2.1 SP1, 2.1 및 2.0)</span><span class="sxs-lookup"><span data-stu-id="7ca96-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="7ca96-157">Microsoft Office 2007 응용 프로그램 (UE-V 2.0에만 해당)</span><span class="sxs-lookup"><span data-stu-id="7ca96-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="7ca96-158">Internet Explorer 8, 9, 10</span><span class="sxs-lookup"><span data-stu-id="7ca96-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="7ca96-159">Internet Explorer 11 (UE-V 2.1 SP1 및 2.1)</span><span class="sxs-lookup"><span data-stu-id="7ca96-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="7ca96-160">Xbox와 같은 대부분의 Windows 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="7ca96-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="7ca96-161">여러 Windows 데스크톱 응용 프로그램 (예: 메모장)</span><span class="sxs-lookup"><span data-stu-id="7ca96-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="7ca96-162">바탕 화면 배경 또는 배경 무늬 등의 다양 한 Windows 설정</span><span class="sxs-lookup"><span data-stu-id="7ca96-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="7ca96-163">참고</span><span class="sxs-lookup"><span data-stu-id="7ca96-163">Note</span></span>**  
<span data-ttu-id="7ca96-164">기본적으로 동기화 되지 않은 응용 프로그램에 대 한 [설정을 동기화 하도록 ue-v를 사용자 지정할](https://technet.microsoft.com/library/dn458942.aspx) 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="7ca96-165">UE-V를 다른 Microsoft 제품과 비교</span><span class="sxs-lookup"><span data-stu-id="7ca96-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="7ca96-166">이 표를 사용 하 여 Windows 7에서 UE-V를 비교 하 고, Windows 8의 프로필을 동기화 하 고, Microsoft 계정의 동기화 PC 설정 기능을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ca96-167">기능</span><span class="sxs-lookup"><span data-stu-id="7ca96-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="7ca96-168">Windows 7을 사용 하 여 프로필 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="7ca96-169">Windows 8을 사용 하 여 프로필 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="7ca96-170">Windows 10을 사용 하 여 프로필 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="7ca96-171">Microsoft 계정</span><span class="sxs-lookup"><span data-stu-id="7ca96-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="7ca96-172">UE-V 2.0</span><span class="sxs-lookup"><span data-stu-id="7ca96-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="7ca96-173">UE-V 2.1 및 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="7ca96-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ca96-174">여러 컴퓨터 간 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-175">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-176">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-177">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-178">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-179">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-180">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ca96-181">실제 및 가상 앱 간에 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-182">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-183">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ca96-184">Windows 앱 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-185">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-186">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-187">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ca96-188">WMI를 통해 관리</span><span class="sxs-lookup"><span data-stu-id="7ca96-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-189">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-190">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-191">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-192">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ca96-193">설정 변경 내용을 정기적으로 동기화</span><span class="sxs-lookup"><span data-stu-id="7ca96-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-194">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-195">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-196">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ca96-197">최소 설치 구성</span><span class="sxs-lookup"><span data-stu-id="7ca96-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-198">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-199">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-200">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-201">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-202">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-203">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ca96-204">비도메인 가입 컴퓨터에서 지원</span><span class="sxs-lookup"><span data-stu-id="7ca96-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-205">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ca96-206">기본 컴퓨터 Active Directory 특성 지원</span><span class="sxs-lookup"><span data-stu-id="7ca96-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-207">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-208">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ca96-209">VDI (가상 데스크톱 인프라)에서 RDS (/Remote 데스크톱 서비스) 및 리치 데스크톱 간의 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-210">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-211">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ca96-212">무제한 설정 저장소 공간</span><span class="sxs-lookup"><span data-stu-id="7ca96-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-213">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-214">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-215">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-216">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-217">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ca96-218">동기화 할 앱 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-219">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-220">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ca96-221">IT 전문가를 위한 백업/복원</span><span class="sxs-lookup"><span data-stu-id="7ca96-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ca96-222">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-223">부분</span><span class="sxs-lookup"><span data-stu-id="7ca96-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ca96-224">●</span><span class="sxs-lookup"><span data-stu-id="7ca96-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="7ca96-225">UE-V 2. x 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="7ca96-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="7ca96-226">이 문서에 대 한 자세한 내용 및 최신 뉴스를 보려면 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ca96-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="7ca96-227">Microsoft User Experience Virtualization(UE-V) 2.1 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="7ca96-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="7ca96-228">Microsoft User Experience Virtualization(UE-V) 2.1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="7ca96-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="7ca96-229">Microsoft User Experience Virtualization(UE-V) 2.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="7ca96-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="7ca96-230">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="7ca96-230">Other resources for this product</span></span>


-   [<span data-ttu-id="7ca96-231">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="7ca96-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="7ca96-232">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="7ca96-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="7ca96-233">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="7ca96-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="7ca96-234">UE-V 2. x 문제 해결</span><span class="sxs-lookup"><span data-stu-id="7ca96-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="7ca96-235">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="7ca96-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="7ca96-236">추가 정보</span><span class="sxs-lookup"><span data-stu-id="7ca96-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="7ca96-237">[MDOP TechCenter 페이지](https://go.microsoft.com/fwlink/p/?LinkId=225286) 최신 MDOP 정보 및 리소스에 대해 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="7ca96-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="7ca96-238">[MDOP 정보 환경](https://go.microsoft.com/fwlink/p/?LinkId=236032) MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="7ca96-239">[Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 팔 로우 하 여 [피드백을 보내거나](mailto:MDOPDocs@microsoft.com) 업데이트에 대 한 정보를 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca96-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














