---
title: 그룹 정책 개체를 사용 하 여 UE-V 2. x 구성
description: 그룹 정책 개체를 사용 하 여 UE-V 2. x 구성
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824423"
---
# <span data-ttu-id="21468-103">그룹 정책 개체를 사용 하 여 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="21468-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="21468-104">일부 Microsoft UE-V (사용자 환경 가상화) 2.0, 2.1 및 2.1 SP1 그룹 정책 설정은 컴퓨터에 대해 정의 될 수 있으며 다른 그룹 정책 설정은 사용자에 대해 정의 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="21468-105">UE-V 그룹 정책 ADMX 파일을 설치 하는 방법에 대 한 자세한 내용은 [ue-v 2 그룹 정책 Admx 템플릿 설치](https://technet.microsoft.com/library/dn458891.aspx#admx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21468-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="21468-106">UE-V에 대해 다음 정책 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="21468-107">그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="21468-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21468-108">그룹 정책 설정 이름</span><span class="sxs-lookup"><span data-stu-id="21468-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="21468-109">대상</span><span class="sxs-lookup"><span data-stu-id="21468-109">Target</span></span></th>
<th align="left"><span data-ttu-id="21468-110">그룹 정책 설정 설명</span><span class="sxs-lookup"><span data-stu-id="21468-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="21468-111">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="21468-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-112">연락처 링크 텍스트</span><span class="sxs-lookup"><span data-stu-id="21468-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-113">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="21468-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-114">이 그룹 정책 설정은 회사 설정 센터에 있는 IT 대화 상대 URL 하이퍼링크의 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-115">이 그룹 정책 설정을 사용 하면 회사 설정 센터에 연락처 URL에 대 한 링크에 지정 된 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21468-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-116">연락처 URL</span><span class="sxs-lookup"><span data-stu-id="21468-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-117">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="21468-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-118">이 그룹 정책 설정은 회사 설정 센터의 IT 연락처 링크에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-119">이 설정을 사용 하면 회사 설정 센터에서 지정 된 URL에 대 한 텍스트 링크를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="21468-120">링크는 HTTP 또는 mailto와 같은 표준 프로토콜 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-121">동기화 공급자 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="21468-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-122">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-123">이 그룹 정책 설정을 사용 하 여 UE-V가 동기화 공급자 기능을 사용 하는지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="21468-124">이 정책 설정을 사용 하면 사용자 설정 가져오기가 지연 될 때 알림이 표시 되도록 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-125">이 설정을 사용 하면 UE-V Agent가 동기화 공급자를 사용 하지 않도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-126">첫 번째 사용 알림</span><span class="sxs-lookup"><span data-stu-id="21468-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-127">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="21468-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-128">이 그룹 정책 설정은 UE-V를 사용 하 여 표시 되는 알림 영역에서 알림을</span><span class="sxs-lookup"><span data-stu-id="21468-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="21468-129">에이전트를 처음 실행할 때 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21468-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-130">기본값을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-131">Windows 설정 로밍</span><span class="sxs-lookup"><span data-stu-id="21468-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-132">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-133">이 그룹 정책 설정은 Windows 설정의 동기화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-134">컴퓨터 간에 동기화 할 Windows 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="21468-135">기본적으로 Windows 테마, 데스크톱 설정 및 접근성 설정은 동일한 운영 체제 버전의 컴퓨터 간에 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-136">설정 패키지 크기 경고 임계값</span><span class="sxs-lookup"><span data-stu-id="21468-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-137">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-138">이 그룹 정책 설정을 사용 하 여 설정 패키지 파일 크기가 정의 된 임계값에 도달 하는 경우 UE-V 에이전트를 보고 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-139">설정 패키지 크기 (KB)에 대 한 기본 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="21468-140">기본적으로 UE-V Agent에는 패키지 파일 크기 임계값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-141">설정 저장소 경로</span><span class="sxs-lookup"><span data-stu-id="21468-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-142">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-143">이 그룹 정책 설정은 사용자 설정을 저장할 위치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-144">UNC (범용 명명 규칙) 경로 및 \Server\SettingsShare%username%. 등의 변수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-145">설정 서식 파일 카탈로그 경로</span><span class="sxs-lookup"><span data-stu-id="21468-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-146">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="21468-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-147">이 그룹 정책 설정은 사용자 지정 설정 위치 템플릿이 저장 되는 위치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="21468-148">이 정책 설정은 또한 UE-V Agent를 사용 하 여 설치 된 기본 Microsoft 템플릿을 바꾸는 데 카탈로그를 사용할지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-149">\Server\TemplateShare 또는 컴퓨터의 폴더 위치와 같은 UNC (범용 명명 규칙) 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="21468-150">기본 Microsoft 서식 파일을 바꾸려면 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-151">데이터 통신 연결을 통한 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="21468-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-152">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-153">이 그룹 정책 설정은 UE-V가 유료 연결을 통해 설정을 동기화할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-154">기본적으로 UE-V Agent는 데이터 통신 연결을 통해 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-155">로밍할 때에도 데이터 통신 연결을 통해 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="21468-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-156">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-157">이 그룹 정책 설정은 데이터 연결이 로밍 모드일 때와 같이 홈 공급자 네트워크 외부에서 UE-V가 통신 연결을 통해 설정을 동기화할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-158">기본적으로 UE-V는 로밍 모드일 때 데이터 통신 연결을 통해 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-159">동기화 시간 제한</span><span class="sxs-lookup"><span data-stu-id="21468-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-160">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-161">이 그룹 정책 설정은 원격 설정 위치에서 사용자 설정을 검색할 때 시간 초과 되기 전에 컴퓨터가 대기 하는 밀리초 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="21468-162">원격 저장소 위치를 사용할 수 없고 사용자가 동기화 공급자를 사용 하지 않는 경우에는 응용 프로그램 시작이이 시간 (밀리초) 만큼 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21468-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-163">기본 설정 동기화 시간 초과 (밀리초)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="21468-164">기본값은 2000 밀리초입니다.</span><span class="sxs-lookup"><span data-stu-id="21468-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-165">트레이 아이콘</span><span class="sxs-lookup"><span data-stu-id="21468-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-166">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="21468-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-167">이 그룹 정책 설정을 통해 UE-V (User Experience Virtualization) 트레이 아이콘을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-168">기본값을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-169">사용자 환경 가상화 사용 (UE-V)</span><span class="sxs-lookup"><span data-stu-id="21468-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-170">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-171">이 그룹 정책 설정을 통해 UE-V (User Experience Virtualization)를 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-172">이 그룹 정책 설정을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21468-173">**참고**  또한 다양 한 데스크톱 응용 프로그램 및 Windows 앱에서 그룹 정책 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="21468-174">이러한 설정을 사용 하 여 특정 응용 프로그램에 대 한 설정 동기화를 설정 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="21468-175">Windows 앱 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="21468-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21468-176">그룹 정책 설정 이름</span><span class="sxs-lookup"><span data-stu-id="21468-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="21468-177">대상</span><span class="sxs-lookup"><span data-stu-id="21468-177">Target</span></span></th>
<th align="left"><span data-ttu-id="21468-178">그룹 정책 설정 설명</span><span class="sxs-lookup"><span data-stu-id="21468-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="21468-179">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="21468-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-180">Windows 앱 동기화 안 함</span><span class="sxs-lookup"><span data-stu-id="21468-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-181">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-182">이 그룹 정책 설정은 UE-V Agent가 Windows 앱에 대 한 설정을 동기화할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-183">기본값은 Windows 앱을 동기화 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="21468-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21468-184">Windows 앱 목록</span><span class="sxs-lookup"><span data-stu-id="21468-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-185">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-186">이 설정에는 UE-V가 해당 앱의 설정을 동기화할지 여부를 명시적으로 Windows 앱 및 상태의 패밀리 패키지 이름이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21468-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-187">이 설정을 사용 하 여 다른 모든 Windows 앱의 설정이 동기화 된 경우에도 앱의 설정이 UE-V를 통해 동기화 되지 않도록 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21468-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21468-188">목록에 없는 Windows 앱 동기화</span><span class="sxs-lookup"><span data-stu-id="21468-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-189">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="21468-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-190">이 그룹 정책 설정은 Windows 앱 목록에 명시적으로 나열 되지 않은 Windows 용 UE-V Agent의 기본 설정 동기화 동작을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="21468-191">기본적으로 UE-V Agent는 Windows 앱 목록에 포함 된 Windows 앱의 설정만 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="21468-192">Windows 앱을 동기화 하는 방법에 대 한 자세한 내용은 [Windows 앱 목록을](https://technet.microsoft.com/library/dn458925.aspx#win8applist)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="21468-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="21468-193">컴퓨터 대상 그룹 정책 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="21468-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="21468-194">UE-V 컴퓨터에 대 한 그룹 정책 설정을 관리 하려면 도메인 컨트롤러 역할을 하는 컴퓨터의 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="21468-195">**컴퓨터 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="21468-196">편집할 그룹 정책 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="21468-197">사용자 대상 그룹 정책 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="21468-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="21468-198">UE-V (Microsoft 데스크톱 최적화 팩)의 GPMC (그룹 정책 관리 콘솔) 또는 MDOP (고급 그룹 정책 관리) 도구를 사용 하 여 온-V에 대 한 그룹 정책 설정을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="21468-199">**사용자 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="21468-200">편집 된 그룹 정책 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="21468-201">UE-V Agent는 다음 우선 순위를 사용 하 여 동기화를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="21468-202">UE-V 설정의 우선 순위 순서</span><span class="sxs-lookup"><span data-stu-id="21468-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="21468-203">그룹 정책 설정으로 관리 되는 사용자 대상 설정-이러한 구성 설정은의 그룹 정책에 따라 레지스트리 키에 저장 됩니다 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="21468-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="21468-204">그룹 정책 설정으로 관리 되는 컴퓨터 대상 설정-이러한 구성 설정은 아래의 그룹 정책에 의해 레지스트리 키에 저장 됩니다 `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="21468-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="21468-205">Windows PowerShell 또는 WMI (Windows management Instrumentation)를 사용 하 여 현재 사용자가 정의한 구성 설정-이 구성 설정은 다음 레지스트리 위치에 UE-V Agent에 의해 저장 됩니다 `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="21468-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="21468-206">Windows PowerShell 또는 WMI를 사용 하 여 컴퓨터에 대해 정의 된 구성 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="21468-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="21468-207">이러한 구성 설정은 UE-V Agent에서 다음 레지스트리 위치에 저장 `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21468-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="21468-208">**Ue-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="21468-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="21468-209">[여기](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="21468-210">**Ue-v 문제가**있나요?</span><span class="sxs-lookup"><span data-stu-id="21468-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="21468-211">[Ue-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21468-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="21468-212">관련 항목</span><span class="sxs-lookup"><span data-stu-id="21468-212">Related topics</span></span>


[<span data-ttu-id="21468-213">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="21468-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="21468-214">UE-V 2.x에 대한 구성 관리</span><span class="sxs-lookup"><span data-stu-id="21468-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





