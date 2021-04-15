---
title: 그룹 정책 개체를 사용하여 UE-V 2.x 구성
description: 그룹 정책 개체를 사용하여 UE-V 2.x 구성
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494063"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="c8e61-103">그룹 정책 개체를 사용하여 UE-V 2.x 구성</span><span class="sxs-lookup"><span data-stu-id="c8e61-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="c8e61-104">컴퓨터에 대해 일부 Microsoft UE-V(User Experience Virtualization) 2.0, 2.1 및 2.1 SP1 그룹 정책 설정을 정의할 수 있으며 사용자에 대해 다른 그룹 정책 설정을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="c8e61-105">UE-V 그룹 정책 ADMX 파일을 설치하는 방법에 대한 자세한 내용은 [UE-V 2](https://technet.microsoft.com/library/dn458891.aspx#admx)그룹 정책 ADMX 템플릿 설치를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8e61-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="c8e61-106">UE-V에 대해 다음 정책 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="c8e61-107">그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c8e61-108">그룹 정책 설정 이름</span><span class="sxs-lookup"><span data-stu-id="c8e61-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="c8e61-109">대상</span><span class="sxs-lookup"><span data-stu-id="c8e61-109">Target</span></span></th>
<th align="left"><span data-ttu-id="c8e61-110">그룹 정책 설정 설명</span><span class="sxs-lookup"><span data-stu-id="c8e61-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="c8e61-111">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="c8e61-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-112">동기화 방법 구성</span><span class="sxs-lookup"><span data-stu-id="c8e61-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-113">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-114">이 그룹 정책 설정을 사용하여 UE-V(User Experience Virtualization)에서 동기화 공급자 기능을 사용할지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="c8e61-115">이 정책 설정을 사용하면 사용자 설정 가져오기가 지연될 때 알림을 표시하도록 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-116">UE-V 에이전트가 동기화 공급자를 사용하지 못하도록 구성하거나 외부 동기화 엔진을 사용하도록 구성하려면 이 설정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-117">IT 링크 텍스트에 문의</span><span class="sxs-lookup"><span data-stu-id="c8e61-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-118">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="c8e61-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-119">이 그룹 정책 설정은 회사 설정 센터에서 연락처 IT URL 하이퍼링크의 텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-120">이 그룹 정책 설정을 사용하면 회사 설정 센터에 연락처 IT URL 링크에 지정된 텍스트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-121">IT URL에 문의</span><span class="sxs-lookup"><span data-stu-id="c8e61-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-122">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="c8e61-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-123">이 그룹 정책 설정은 회사 설정 센터의 연락처 IT 링크에 대한 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-124">이 설정을 사용하면 회사 설정 센터 IT 담당자가 지정한 URL에 대한 텍스트 링크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="c8e61-125">연결은 HTTP 또는 mailto와 같은 모든 표준 프로토콜일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-126">첫 번째 사용 알림</span><span class="sxs-lookup"><span data-stu-id="c8e61-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-127">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="c8e61-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-128">이 그룹 정책 설정은 UE-V가 나타날 때 나타나는 알림 영역에 알림을 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="c8e61-129">에이전트가 처음으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-130">기본값은 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-131">동기화하기 전에 설정 저장 위치 Ping</span><span class="sxs-lookup"><span data-stu-id="c8e61-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-132">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-133">이 정책 설정을 사용하면 연결을 확인하기 위해 설정을 동기화하기 전에 UE-V 동기화 공급자를 구성하여 설정 저장 경로를 ping할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-134">이 그룹 정책 설정을 사용 또는 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-135">설정 패키지 크기 경고 임계값</span><span class="sxs-lookup"><span data-stu-id="c8e61-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-136">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-137">이 그룹 정책 설정을 통해 설정 패키지 파일 크기가 정의된 임계값에 도달한 경우 보고하도록 UE-V 에이전트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-138">설정 패키지 크기에 대한 기본 임계값을 KB(킬로바이트)로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="c8e61-139">기본적으로 UE-V 에이전트에는 패키지 파일 크기 임계값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-140">설정 저장소 경로</span><span class="sxs-lookup"><span data-stu-id="c8e61-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-141">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-142">이 그룹 정책 설정은 사용자 설정을 저장할 위치를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-143">UNC(범용 이름 규칙) 경로 및 \Server\SettingsShare%username%와 같은 변수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-144">설정 템플릿 카탈로그 경로</span><span class="sxs-lookup"><span data-stu-id="c8e61-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-145">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="c8e61-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-146">이 그룹 정책 설정은 사용자 지정 설정 위치 템플릿이 저장되는 위치를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="c8e61-147">이 정책 설정은 설치된 기본 Microsoft 템플릿을 UE-V 에이전트로 바꾸기 위해 카탈로그를 사용할지 여부도 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-148">\Server\TemplateShare와 같은 UNC(범용 이름 규칙) 경로 또는 컴퓨터의 폴더 위치를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="c8e61-149">기본 Microsoft 서식 파일을 바꾸기 위해 확인란을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-150">데이터 연결에 대한 동기화 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-151">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-152">이 그룹 정책 설정은 UE-V가 데이터 연결에서 설정을 동기화할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-153">기본적으로 UE-V 에이전트는 데이터 데이터 연결을 통해 설정을 동기화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-154">로밍 시에도 데이터 연결에 대한 동기화 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-155">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-156">이 그룹 정책 설정은 UE-V가 홈 공급자 네트워크 외부의 데이터 통신 연결(예: 데이터 연결이 로밍 모드인 경우)을 통해 설정을 동기화할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-157">기본적으로 UE-V는 로밍 모드일 때 데이터 데이터 연결을 통해 설정을 동기화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-158">동기화 시간 제한</span><span class="sxs-lookup"><span data-stu-id="c8e61-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-159">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-160">이 그룹 정책 설정은 컴퓨터가 원격 설정 위치에서 사용자 설정을 검색할 때 시간이 너무 되기 전에 대기하는 시간(밀리초)을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="c8e61-161">원격 저장소 위치를 사용할 수 없는 경우 사용자가 동기화 공급자를 사용하지 않는 경우 응용 프로그램 시작이 이 밀리초까지 지연됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-162">기본 동기화 시간(밀리초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="c8e61-163">기본값은 2000밀리초입니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-164">Windows 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="c8e61-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="c8e61-165">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-166">이 그룹 정책 설정은 Windows 설정의 동기화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-167">컴퓨터 간에 동기화할 Windows 설정을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="c8e61-168">기본적으로 Windows 테마, 데스크톱 설정 및 접근성 설정은 동일한 운영 체제 버전의 컴퓨터 간에 설정을 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-169">트레이 아이콘</span><span class="sxs-lookup"><span data-stu-id="c8e61-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-170">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="c8e61-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-171">이 그룹 정책 설정은 UE-V 트레이 아이콘을 사용 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-172">기본값은 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-173">UE-V(User Experience Virtualization) 사용</span><span class="sxs-lookup"><span data-stu-id="c8e61-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-174">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-175">이 그룹 정책 설정을 통해 UE-V를 활성화 또는 비활성화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-176">이 그룹 정책 설정을 사용 또는 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-177">VDI 구성</span><span class="sxs-lookup"><span data-stu-id="c8e61-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-178">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-179">이 정책 설정은 풀링된 VDI 환경에서 실행되는 컴퓨터의 UE-V 롤백 정보 동기화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="c8e61-180">해당 정책을 사용하도록 설정하면 UE-V 롤백 상태가 로그아웃 시 설정 저장소 위치에 복사되고 로그인 시 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-181">이 그룹 정책 설정을 사용 또는 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="c8e61-182">참고</span><span class="sxs-lookup"><span data-stu-id="c8e61-182">Note</span></span>**  
<span data-ttu-id="c8e61-183">또한 그룹 정책 설정은 많은 데스크톱 응용 프로그램 및 Windows 앱에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="c8e61-184">이러한 설정을 사용하여 특정 응용 프로그램에 대해 설정 동기화를 설정하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="c8e61-185">Windows 앱 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="c8e61-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c8e61-186">그룹 정책 설정 이름</span><span class="sxs-lookup"><span data-stu-id="c8e61-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="c8e61-187">대상</span><span class="sxs-lookup"><span data-stu-id="c8e61-187">Target</span></span></th>
<th align="left"><span data-ttu-id="c8e61-188">그룹 정책 설정 설명</span><span class="sxs-lookup"><span data-stu-id="c8e61-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="c8e61-189">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="c8e61-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-190">Windows 앱을 동기화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-191">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-192">이 그룹 정책 설정은 UE-V 에이전트가 Windows 앱의 설정을 동기화하는지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-193">기본값은 Windows 앱을 동기화하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c8e61-194">Windows 앱 목록</span><span class="sxs-lookup"><span data-stu-id="c8e61-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-195">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-196">이 설정은 Windows 앱의 패밀리 패키지 이름을 나열하고 UE-V가 해당 앱의 설정을 동기화하는지 여부를 하여 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-197">다른 모든 Windows 앱의 설정이 동기화된 경우에도 이 설정을 사용하여 앱 설정이 UE-V와 동기화되지 않는지 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c8e61-198">목록에 없는 Windows 앱 동기화</span><span class="sxs-lookup"><span data-stu-id="c8e61-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-199">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="c8e61-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-200">이 그룹 정책 설정은 Windows 앱 목록에 명시적으로 나열되지 않은 Windows 앱용 UE-V 에이전트의 기본 설정 동기화 동작을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c8e61-201">기본적으로 UE-V 에이전트는 Windows 앱 목록에 포함된 Windows 앱의 설정만 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c8e61-202">Windows 앱 동기화에 대한 자세한 내용은 [Windows 앱 목록 을 참조하세요.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)</span><span class="sxs-lookup"><span data-stu-id="c8e61-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="c8e61-203">컴퓨터 대상 그룹 정책 설정을 구성하려면</span><span class="sxs-lookup"><span data-stu-id="c8e61-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="c8e61-204">도메인 컨트롤러 역할을 하는 컴퓨터에서 GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리)을 사용하여 UE-V 컴퓨터에 대한 그룹 정책 설정을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="c8e61-205">컴퓨터 **구성으로 이동하여** **정책을**선택하고 관리 템플릿을 선택하고 **Windows**구성 요소를 클릭한 다음 **Microsoft User Experience Virtualization 을 선택합니다.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c8e61-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="c8e61-206">편집할 그룹 정책 설정을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="c8e61-207">사용자 대상 그룹 정책 설정을 구성하려면</span><span class="sxs-lookup"><span data-stu-id="c8e61-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="c8e61-208">도메인 컨트롤러 컴퓨터에서 MDOP(Microsoft Desktop Optimization Pack)의 GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리) 도구를 사용하여 UE-V에 대한 그룹 정책 설정을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="c8e61-209">사용자 **구성으로 이동하여** **정책,** 관리 **템플릿을**선택하고 **Windows**구성 요소를 클릭한 다음 **Microsoft User Experience Virtualization 을 선택합니다.**</span><span class="sxs-lookup"><span data-stu-id="c8e61-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="c8e61-210">편집된 그룹 정책 설정을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="c8e61-211">UE-V 에이전트는 다음 우선 순위를 사용하여 동기화를 파악합니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="c8e61-212">UE-V 설정의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="c8e61-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="c8e61-213">그룹 정책 설정으로 관리되는 사용자 대상 설정 - 이러한 구성 설정은 에서 그룹 정책에 의해 레지스트리 키에 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="c8e61-214">그룹 정책 설정에 의해 관리되는 컴퓨터 대상 설정 - 이러한 구성 설정은 의 그룹 정책에 의해 레지스트리 키에 `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="c8e61-215">Windows PowerShell 또는 WMI(Windows management Instrumentation)를 사용하여 현재 사용자가 정의하는 구성 설정 - 이러한 구성 설정은 이 레지스트리 위치의 UE-V 에이전트에 의해 저장됩니다. `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="c8e61-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="c8e61-216">WMI 또는 WMI를 사용하여 컴퓨터에 Windows PowerShell 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="c8e61-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="c8e61-217">이러한 구성 설정은 UE-V 에이전트에 의해 이 레지스트리 위치 아래에 `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` 저장됩니다. .</span><span class="sxs-lookup"><span data-stu-id="c8e61-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="c8e61-218">**UE-V에 대한 제안이 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c8e61-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="c8e61-219">여기에 제안을 추가하거나 [투표합니다.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)</span><span class="sxs-lookup"><span data-stu-id="c8e61-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="c8e61-220">**UE-V 문제가 있나요?**</span><span class="sxs-lookup"><span data-stu-id="c8e61-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="c8e61-221">[UE-V TechNet 포럼을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)</span><span class="sxs-lookup"><span data-stu-id="c8e61-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8e61-222">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c8e61-222">Related topics</span></span>


[<span data-ttu-id="c8e61-223">UE-V 2.x 관리</span><span class="sxs-lookup"><span data-stu-id="c8e61-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="c8e61-224">UE-V 2.x에 대한 구성 관리</span><span class="sxs-lookup"><span data-stu-id="c8e61-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
