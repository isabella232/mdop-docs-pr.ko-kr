---
title: 클라이언트 구성 설정 정보
description: 클라이언트 구성 설정 정보
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814940"
---
# <span data-ttu-id="3ac66-103">클라이언트 구성 설정 정보</span><span class="sxs-lookup"><span data-stu-id="3ac66-103">About Client Configuration Settings</span></span>


<span data-ttu-id="3ac66-104">Microsoft App-v (Application Virtualization) 5.0 클라이언트는 레지스트리에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="3ac66-105">레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="3ac66-106">레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="3ac66-107">이 항목에서는 App-v 5.0 클라이언트 구성 설정을 나열 하 고 해당 사용에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="3ac66-108">PowerShell을 사용 하 여 클라이언트 구성 설정을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="3ac66-109">PowerShell 및 App-v 5.0 사용에 대 한 자세한 내용은 PowerShell을 [사용 하 여 App-v 관리](administering-app-v-by-using-powershell.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ac66-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="3ac66-110">앱-V 5.0 클라이언트 구성 설정</span><span class="sxs-lookup"><span data-stu-id="3ac66-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="3ac66-111">다음 표에서는 App-v 5.0 클라이언트 구성 설정에 대 한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3ac66-112">설정 이름</span><span class="sxs-lookup"><span data-stu-id="3ac66-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="3ac66-113">설정 플래그</span><span class="sxs-lookup"><span data-stu-id="3ac66-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="3ac66-114">설명</span><span class="sxs-lookup"><span data-stu-id="3ac66-114">Description</span></span></th>
<th align="left"><span data-ttu-id="3ac66-115">설정 옵션</span><span class="sxs-lookup"><span data-stu-id="3ac66-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="3ac66-116">레지스트리 키 값</span><span class="sxs-lookup"><span data-stu-id="3ac66-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="3ac66-117">설정 되지 않은 정책 상태 키 및 값</span><span class="sxs-lookup"><span data-stu-id="3ac66-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-118">Package설치 루트</span><span class="sxs-lookup"><span data-stu-id="3ac66-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-119">PACKAGE설치 루트</span><span class="sxs-lookup"><span data-stu-id="3ac66-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-120">모든 새 응용 프로그램과 업데이트가 설치 되는 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-121">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="3ac66-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-123">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="3ac66-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="3ac66-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-126">패키지 콘텐츠를 다운로드할 원본 위치를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-127">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="3ac66-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-129">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="3ac66-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-131">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-132">이 설정은 데이터 통신 네트워크 연결을 통해 연결 된 Windows 8 컴퓨터에서 가상화 된 응용 프로그램을 시작할지 여부를 제어 합니다 (예: 4G).</span><span class="sxs-lookup"><span data-stu-id="3ac66-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-133">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="3ac66-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-135">0</span><span class="sxs-lookup"><span data-stu-id="3ac66-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="3ac66-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-137">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-138">삭제 된 세션을 다시 시도할 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-139">Integer (0-99)</span><span class="sxs-lookup"><span data-stu-id="3ac66-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="3ac66-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-141">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-143">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-144">삭제 된 세션을 다시 시도 하는 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-145">Integer (0-3600)</span><span class="sxs-lookup"><span data-stu-id="3ac66-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-147">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-148">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="3ac66-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-149">AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="3ac66-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-150">새 패키지를 앱-V가 특정 컴퓨터에서 자동으로 로드 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-151">(0x0) 없음; (0x1) 이전에 사용한 경우 (0x2) 모두</span><span class="sxs-lookup"><span data-stu-id="3ac66-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="3ac66-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-153">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-154">LocationProvider</span><span class="sxs-lookup"><span data-stu-id="3ac66-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-155">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-156">IAppvPackageLocationProvider 인터페이스의 호환 되는 구현에 대 한 CLSID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-157">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="3ac66-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-159">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="3ac66-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-161">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-162">인증서 저장소의 유효한 인증서에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-163">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="3ac66-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-165">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="3ac66-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-167">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-168">HTTPS를 사용 steaming 전에 서버 인증서 해지 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-169">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="3ac66-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-171">0</span><span class="sxs-lookup"><span data-stu-id="3ac66-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="3ac66-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="3ac66-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-174">스트리밍된 패키지 콘텐츠를 로컬 하드 디스크에 저장 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-175">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="3ac66-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-177">0</span><span class="sxs-lookup"><span data-stu-id="3ac66-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-178">이름</span><span class="sxs-lookup"><span data-stu-id="3ac66-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-179">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-179">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-180">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-181"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="3ac66-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-183">게시 서버의 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-184">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-185">Publishing\Servers {serverId} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3ac66-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-186">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-187">URL</span><span class="sxs-lookup"><span data-stu-id="3ac66-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-188">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-188">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-189">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-190"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="3ac66-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-192">게시 서버의 URL을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-193">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-194">Publishing\Servers {serverId} \ URL</span><span class="sxs-lookup"><span data-stu-id="3ac66-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-195">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="3ac66-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-197">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-197">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-198">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-199"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="3ac66-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-201">전역 게시 새로 고침을 사용 하도록 설정 합니다 (부울).</span><span class="sxs-lookup"><span data-stu-id="3ac66-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-202">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-203">Publishing\Servers {serverId} \ GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="3ac66-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-204">False</span><span class="sxs-lookup"><span data-stu-id="3ac66-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="3ac66-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-206">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-206">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-207">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-208"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="3ac66-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-210">로그온 시 전역 게시 새로 고침을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="3ac66-211">나타내는</span><span class="sxs-lookup"><span data-stu-id="3ac66-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-212">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-213">Publishing\Servers {serverId} \ GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="3ac66-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-214">False</span><span class="sxs-lookup"><span data-stu-id="3ac66-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-216">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-216">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-217">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-218"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="3ac66-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="3ac66-220">GlobalRefreshIntervalUnit을 사용 하 여 게시 새로 고침 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="3ac66-221">패키지 새로 고침을 사용 하지 않도록 설정 하려면 0을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-222">Integer (0-744</span><span class="sxs-lookup"><span data-stu-id="3ac66-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-224">0</span><span class="sxs-lookup"><span data-stu-id="3ac66-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="3ac66-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-226">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-226">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-227">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-228"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="3ac66-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-230">간격 단위 (시간 0-23, 일 0-31)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="3ac66-231">0 시간에 해당 하 고 1 일 동안</span><span class="sxs-lookup"><span data-stu-id="3ac66-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="3ac66-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-233">raid-1</span><span class="sxs-lookup"><span data-stu-id="3ac66-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="3ac66-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-235">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-235">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-236">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-237"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="3ac66-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="3ac66-239">사용자 게시 새로 고침을 사용 하도록 설정 합니다 (부울).</span><span class="sxs-lookup"><span data-stu-id="3ac66-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-240">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-241">Publishing\Servers {serverId} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="3ac66-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-242">False</span><span class="sxs-lookup"><span data-stu-id="3ac66-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="3ac66-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-244">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-244">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-245">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-246"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="3ac66-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-248">사용자 게시 새로 고침 onlogon을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="3ac66-249">나타내는</span><span class="sxs-lookup"><span data-stu-id="3ac66-249">( Boolean)</span></span></p>
<p><span data-ttu-id="3ac66-250">단어 개수 (공백 포함): 60</span><span class="sxs-lookup"><span data-stu-id="3ac66-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-251">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-252">Publishing\Servers {serverId} \ UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="3ac66-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-253">False</span><span class="sxs-lookup"><span data-stu-id="3ac66-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-255">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-255">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-256">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-257"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="3ac66-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="3ac66-259">UserRefreshIntervalUnit을 사용 하 여 게시 새로 고침 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="3ac66-260">패키지 새로 고침을 사용 하지 않도록 설정 하려면 0을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="3ac66-261">단어 개수 (공백 포함): 85</span><span class="sxs-lookup"><span data-stu-id="3ac66-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-262">Integer (0-744 시간)</span><span class="sxs-lookup"><span data-stu-id="3ac66-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-264">0</span><span class="sxs-lookup"><span data-stu-id="3ac66-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="3ac66-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-266">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-266">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-267">이 설정은 <strong> set-AppvclientConfiguration cmdLet을 사용 하 여 수정할 수 없습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="3ac66-268"><strong>Set-AppvPublishingServer cmdlet을 사용 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="3ac66-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="3ac66-270">간격 단위 (시간 0-23, 일 0-31)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="3ac66-271">0 시간에 해당 하 고 1 일 동안</span><span class="sxs-lookup"><span data-stu-id="3ac66-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="3ac66-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-273">raid-1</span><span class="sxs-lookup"><span data-stu-id="3ac66-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-274">MigrationMode</span><span class="sxs-lookup"><span data-stu-id="3ac66-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-275">MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="3ac66-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-276">마이그레이션 모드는 App-v 클라이언트에서 이전 버전의 App-v를 사용 하 여 만든 패키지에 대 한 바로 가기 및 FTA 수정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-277">True (enabled 상태), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="3ac66-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="3ac66-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="3ac66-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-281">앱-V 5.0 클라이언트를 실행 하는 컴퓨터가 특정 사용 정보를 수집 하 고 반환할 수 있도록 하 여 응용 프로그램을 더욱 개선 하는 데 도움을 드립니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-282">사용 안 함: 0 사용 하도록 설정 1</span><span class="sxs-lookup"><span data-stu-id="3ac66-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-283">소프트웨어/Microsoft/AppV/CEIP/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="3ac66-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-284">0</span><span class="sxs-lookup"><span data-stu-id="3ac66-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="3ac66-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="3ac66-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-287">실행 해야 하는 구성 파일의 패키지 매니페스트에 정의 된 스크립트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-288">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="3ac66-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="3ac66-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="3ac66-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-292">사용자&#39;s 프로필을 사용 하 여 로밍 하지 않는% userprofile%를 기준으로 하는 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="3ac66-293">사용 예:/ROAMINGFILEEXCLUSIONS =&#39;desktop, 내 사진&#39;</span><span class="sxs-lookup"><span data-stu-id="3ac66-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="3ac66-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="3ac66-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-296">사용자 프로필로 로밍되지 않는 레지스트리 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="3ac66-297">사용 예:/ROAMINGREGISTRYEXCLUSIONS = \\수업, \클라이언트</span><span class="sxs-lookup"><span data-stu-id="3ac66-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-298">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="3ac66-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-300">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="3ac66-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-302">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-303">사용자가 게시 한 패키지의 현재 버전과 연결 된 심볼 링크를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="3ac66-304">바로 가기 및 파일 형식 연결 등의 모든 가상 응용 프로그램 확장은이 경로를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="3ac66-305">경로를 지정 하지 않으면 패키지를 게시할 때 기호화 된 링크가 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="3ac66-306">예:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="3ac66-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-307">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="3ac66-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-309">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="3ac66-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-311">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-312">전역으로 게시 된 패키지의 현재 버전과 연결 된 심볼 링크를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="3ac66-313">바로 가기 및 파일 형식 연결 등의 모든 가상 응용 프로그램 확장은이 경로를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="3ac66-314">경로를 지정 하지 않으면 패키지를 게시할 때 기호화 된 링크가 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="3ac66-315">예:%allusersprofile%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="3ac66-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-316">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="3ac66-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-318">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="3ac66-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-320">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-321">로컬에 설치 된 응용 프로그램을 가상 환경에서 실행할 수 있는지 확인 하는 데 사용할 수 있는 쉼표로 구분 된 파일 확장명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="3ac66-322">게시 하는 동안 바로 가기, FTAs 및 기타 확장 지점을 만들면 앱-V는 확장 지점과 연결 된 응용 프로그램이 로컬에 설치 되어 있는 경우 목록에 확장명을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="3ac66-323">확장명이 있으면 <strong> runvirtual </strong> command 명령줄 매개 변수가 추가 되 고 응용 프로그램이 가상으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="3ac66-324"><strong>Runvirtual 매개 변수에 대 한 자세한 내용은 </strong> 가상화 된 <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> 응용 프로그램을 사용 하 여 가상 환경 내에서 로컬로 설치 된 응용 프로그램 실행을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3ac66-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-325">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="3ac66-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-327">기록 되지 않은 정책 값</span><span class="sxs-lookup"><span data-stu-id="3ac66-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ac66-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-329">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-330">클라이언트가 보고 서버로 정보를 반환할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-331">True (enabled), False (비활성 상태)</span><span class="sxs-lookup"><span data-stu-id="3ac66-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="3ac66-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-333">False</span><span class="sxs-lookup"><span data-stu-id="3ac66-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="3ac66-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-335">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-336">클라이언트 정보가 저장 되는 보고 서버의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-337">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="3ac66-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-339">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="3ac66-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-341">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-342">보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="3ac66-343">크기는 메모리의 캐시에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="3ac66-344">제한에 도달 하면 로그 파일이 롤오버 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="3ac66-345">0에서 1024 사이를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-346">Integer [0-1024]</span><span class="sxs-lookup"><span data-stu-id="3ac66-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="3ac66-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-348">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="3ac66-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-350">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-351">업로드 요청을 보고 하기 위해 서버로 전송할 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="3ac66-352">이는 로그가 유효 크기에 도달 했을 때 영구 전송 오류를 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="3ac66-353">1024에서 무제한으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-354">Integer [1024-무제한]</span><span class="sxs-lookup"><span data-stu-id="3ac66-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="3ac66-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-356">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="3ac66-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-358">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-359">보고서 서버에 데이터를 보내는 클라이언트를 시작 하는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="3ac66-360">일일 시간에 해당 하는 0-23 사이의 유효한 정수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="3ac66-361">기본적으로 <strong> ReportingStartTime는 </strong> 현재 날짜에서 10 P. M 또는 22로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-362">참고</span><span class="sxs-lookup"><span data-stu-id="3ac66-362">Note</span></span></strong><br/><p><span data-ttu-id="3ac66-363">App-v 5.0 클라이언트를 실행 하는 컴퓨터가 오프 라인 상태가 될 가능성이 적은 시간으로이 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-364">Integer (0-23)</span><span class="sxs-lookup"><span data-stu-id="3ac66-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-365">보고 \ StartTime</span><span class="sxs-lookup"><span data-stu-id="3ac66-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-366">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-368">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-369">클라이언트가 보고 서버에 데이터를 재전송 하는 데 사용할 다시 시도 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-370">정수</span><span class="sxs-lookup"><span data-stu-id="3ac66-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="3ac66-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-372">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="3ac66-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-374">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-375">보고 서버로 데이터를 보낼 최대 지연 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="3ac66-376">예약 된 작업이 시작 되 면 클라이언트는 0과 ReportingRandomDelay 사이의 임의 지연 시간을 <strong> 생성 </strong> 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="3ac66-377">서버에서 충돌을 방지 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-378">Integer [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="3ac66-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="3ac66-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-380">정책 값이 쓰여지지 않음 (구성 되지 않은 것과 같음)</span><span class="sxs-lookup"><span data-stu-id="3ac66-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="3ac66-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-382">중요</span><span class="sxs-lookup"><span data-stu-id="3ac66-382">Important</span></span></strong><br/><p><span data-ttu-id="3ac66-383">이 설정은 App-v 5.0 SP2 이상 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-384">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-385">지원 되는 셸 확장, 브라우저 도우미 개체 및 Active X 컨트롤을 가상 응용 프로그램을 사용 하 여 가상화 하 고 실행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-386">1 (사용), 0 (사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="3ac66-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-387">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</span><span class="sxs-lookup"><span data-stu-id="3ac66-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="3ac66-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-389">중요</span><span class="sxs-lookup"><span data-stu-id="3ac66-389">Important</span></span></strong><br/><p><span data-ttu-id="3ac66-390">이 설정은 App-v 5.0 SP2 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-391">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-392">App-v 5.0 클라이언트를 실행 하는 컴퓨터에 대해 게시 새로 고침 진행률 표시줄을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-393">1 (사용), 0 (사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="3ac66-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-394">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</span><span class="sxs-lookup"><span data-stu-id="3ac66-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ac66-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="3ac66-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3ac66-396">중요</span><span class="sxs-lookup"><span data-stu-id="3ac66-396">Important</span></span></strong><br/><p><span data-ttu-id="3ac66-397">이 설정은 App-v 5.0 SP2 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3ac66-398">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-399">게시 새로 고침 진행률 표시줄을 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-400">1 (사용), 0 (사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="3ac66-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ac66-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="3ac66-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-402">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="3ac66-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-403">동적 가상화를 사용 하기 위한 후보 (지원 되는 셸 확장, 브라우저 도우미 개체 및 ActiveX 컨트롤) 인 프로세스 경로 목록 (와일드 카드를 포함할 수 있음)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="3ac66-404">전체 경로가 이러한 항목 중 하 나와 일치 하는 프로세스만 동적 가상화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-405">문자열</span><span class="sxs-lookup"><span data-stu-id="3ac66-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="3ac66-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ac66-407">빈 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac66-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="3ac66-408">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3ac66-408">Related topics</span></span>


[<span data-ttu-id="3ac66-409">App-V 5.0 Sequencer 및 Client 배포</span><span class="sxs-lookup"><span data-stu-id="3ac66-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="3ac66-410">ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="3ac66-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="3ac66-411">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="3ac66-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









