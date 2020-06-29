---
title: MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법
description: MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826918"
---
# <span data-ttu-id="d864a-103">MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="d864a-103">How to Download and Deploy MDOP Group Policy (.admx) Templates</span></span>


<span data-ttu-id="d864a-104">그룹 정책 템플릿, admx 및 adml 파일을 사용 하 여 특정 Microsoft 데스크톱 최적화 팩 (MDOP) 기술 (예: App-v, UE-V 또는 MBAM)의 기능 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-104">You can manage the feature settings of certain Microsoft Desktop Optimization Pack (MDOP) technologies (for example, App-V, UE-V, or MBAM) by using Group Policy templates, the .admx and .adml files.</span></span> <span data-ttu-id="d864a-105">MDOP 그룹 정책 템플릿은 기술 및 버전별 그룹화 된 자동 압축 풀림 압축 파일에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-105">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

## <span data-ttu-id="d864a-106">MDOP 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="d864a-106">MDOP Group Policy templates</span></span>

**<span data-ttu-id="d864a-107">MDOP 그룹 정책 템플릿을 다운로드 하 고 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="d864a-107">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="d864a-108">최신 [MDOP 그룹 정책 서식 파일](https://www.microsoft.com/download/details.aspx?id=55531) 다운로드</span><span class="sxs-lookup"><span data-stu-id="d864a-108">Download the latest [MDOP Group Policy templates](https://www.microsoft.com/download/details.aspx?id=55531)</span></span> 

2. <span data-ttu-id="d864a-109">실행 하 여 다운로드 한 .cab 파일 확장</span><span class="sxs-lookup"><span data-stu-id="d864a-109">Expand the downloaded .cab file by running</span></span> `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **<span data-ttu-id="d864a-110">Warning</span><span class="sxs-lookup"><span data-stu-id="d864a-110">Warning</span></span>**  
   <span data-ttu-id="d864a-111">그룹 정책 배포 디렉터리로 직접 서식 파일의 압축을 풀지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d864a-111">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="d864a-112">여러 기술과 버전이이 파일에 번들로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-112">Multiple technologies and versions are bundled in this file.</span></span>

3. <span data-ttu-id="d864a-113">추출 된 폴더에서 기술-버전의 admx 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-113">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="d864a-114">특정 MDOP 기술에는 그룹 정책 개체 (Gpo) 집합이 여러 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-114">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="d864a-115">예를 들어 MBAM에는 MBAM 관리 설정과 MBAM 사용자 설정이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-115">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="d864a-116">언어 문화권에 따라 적절 한 adml 파일을 찾습니다 (즉, *en-us* 는 영어-미국에 해당).</span><span class="sxs-lookup"><span data-stu-id="d864a-116">Locate the appropriate .adml file by language-culture (that is, *en-us* for English-United States).</span></span>

5. <span data-ttu-id="d864a-117">Admx 및 adml 파일을 정책 정의 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-117">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="d864a-118">템플릿을 저장 하는 위치에 따라 로컬 장치 또는 도메인의 컴퓨터에서 그룹 정책 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-118">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   - <span data-ttu-id="d864a-119">**로컬 파일:** 로컬 장치에서 그룹 정책 설정을 구성 하려면 서식 파일을 다음 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-119">**Local files:** To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="d864a-120">파일 형식</span><span class="sxs-lookup"><span data-stu-id="d864a-120">File type</span></span></th>
   <th align="left"><span data-ttu-id="d864a-121">파일 위치</span><span class="sxs-lookup"><span data-stu-id="d864a-121">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="d864a-122">그룹 정책 템플릿 (admx)</span><span class="sxs-lookup"><span data-stu-id="d864a-122">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="d864a-123">&lt;강력한 &gt; policydefinitions</span><span class="sxs-lookup"><span data-stu-id="d864a-123">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="d864a-124">그룹 정책 언어 파일 (adml)</span><span class="sxs-lookup"><span data-stu-id="d864a-124">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="d864a-125">&lt;강력한 &gt; policydefinitions</span><span class="sxs-lookup"><span data-stu-id="d864a-125">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>

   - <span data-ttu-id="d864a-126">**도메인 중앙 스토어:** 도메인의 컴퓨터에서 그룹 정책 관리자가 그룹 정책 설정 구성을 사용 하도록 설정 하려면 도메인 컨트롤러의 다음 위치에 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-126">**Domain central store:** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="d864a-127">파일 형식</span><span class="sxs-lookup"><span data-stu-id="d864a-127">File type</span></span></th>
   <th align="left"><span data-ttu-id="d864a-128">파일 위치</span><span class="sxs-lookup"><span data-stu-id="d864a-128">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="d864a-129">그룹 정책 템플릿 (admx)</span><span class="sxs-lookup"><span data-stu-id="d864a-129">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="d864a-130">&lt;강력한 &gt; sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="d864a-130">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="d864a-131">그룹 정책 언어 파일 (adml)</span><span class="sxs-lookup"><span data-stu-id="d864a-131">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="d864a-132">&lt;강력한 &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</span><span class="sxs-lookup"><span data-stu-id="d864a-132">&lt;strong&gt;sysvol\domain\policies\PolicyDefinitions[MUIculture]</span></span></strong><code>[MUIculture]</code></p>
   <p><span data-ttu-id="d864a-133">예를 들어 미국 영어 ADML 언어 관련 파일 은%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-133">For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</span></span></p></td>
   </tr>
   </tbody>
   </table>

6. <span data-ttu-id="d864a-134">GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 사용 하 여 그룹 정책 설정을 편집 하 여 MDOP 기술에 대 한 그룹 정책 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d864a-134">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span>

### <span data-ttu-id="d864a-135">기술별 MDOP 그룹 정책</span><span class="sxs-lookup"><span data-stu-id="d864a-135">MDOP Group Policy by technology</span></span>

<span data-ttu-id="d864a-136">지원 되는 MDOP 그룹 정책에 대 한 자세한 내용은 해당 기술에 대 한 특정 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d864a-136">For more information about supported MDOP Group Policy, see the specific documentation for the technology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d864a-137">MDOP 기술</span><span class="sxs-lookup"><span data-stu-id="d864a-137">MDOP Technology</span></span></th>
<th align="left"><span data-ttu-id="d864a-138">버전 번들</span><span class="sxs-lookup"><span data-stu-id="d864a-138">Version bundles</span></span></th>
<th align="left"><span data-ttu-id="d864a-139">참고</span><span class="sxs-lookup"><span data-stu-id="d864a-139">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d864a-140">App-V(Application Virtualization)</span><span class="sxs-lookup"><span data-stu-id="d864a-140">Application Virtualization (App-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d864a-141">App-v 5.0 및 App-V 5.0 서비스 팩</span><span class="sxs-lookup"><span data-stu-id="d864a-141">App-V 5.0 and App-V 5.0 Service Packs</span></span></p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)"><span data-ttu-id="d864a-142">ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="d864a-142">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d864a-143">UE-V(User Experience Virtualization)</span><span class="sxs-lookup"><span data-stu-id="d864a-143">User Experience Virtualization (UE-V)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d864a-144">UE-V 2.0 및 UE-V 2.1</span><span class="sxs-lookup"><span data-stu-id="d864a-144">UE-V 2.0 and UE-V 2.1</span></span></p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)"><span data-ttu-id="d864a-145">그룹 정책 개체를 사용 하 여 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="d864a-145">Configuring UE-V 2.x with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d864a-146">UE-V 1.0 (1.0 SP1 포함)</span><span class="sxs-lookup"><span data-stu-id="d864a-146">UE-V 1.0 including 1.0 SP1</span></span></p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)"><span data-ttu-id="d864a-147">그룹 정책 개체를 사용하여 UE-V 구성</span><span class="sxs-lookup"><span data-stu-id="d864a-147">Configuring UE-V with Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d864a-148">MBAM(Microsoft BitLocker Administration and Monitoring)</span><span class="sxs-lookup"><span data-stu-id="d864a-148">Microsoft BitLocker Administration and Monitoring (MBAM)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d864a-149">MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d864a-149">MBAM 2.5</span></span></p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="d864a-150">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="d864a-150">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d864a-151">MBAM 2.0 (2.0 SP1 포함)</span><span class="sxs-lookup"><span data-stu-id="d864a-151">MBAM 2.0 including 2.0 SP1</span></span></p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="d864a-152">MBAM 2.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="d864a-152">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="d864a-153">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="d864a-153">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d864a-154">MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d864a-154">MBAM 1.0</span></span></p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)"><span data-ttu-id="d864a-155">MBAM 1.0 GPO 설정을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="d864a-155">How to Edit MBAM 1.0 GPO Settings</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





