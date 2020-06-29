---
title: MBAM 2.5 그룹 정책 템플릿 복사
description: MBAM 2.5 그룹 정책 템플릿 복사
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825223"
---
# <span data-ttu-id="fcf00-103">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="fcf00-103">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="fcf00-104">MBAM 클라이언트 설치를 배포 하기 전에 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정이 포함 된 MBAM 그룹 정책 템플릿을 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-104">Before deploying the MBAM Client installation, you must download the MBAM Group Policy Templates, which contain Group Policy settings that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="fcf00-105">서식 파일을 다운로드 한 후에는 그룹 정책 설정을 엔터프라이즈에서 구현 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-105">After downloading the templates, you then set the Group Policy settings to implement across your enterprise.</span></span>

## <span data-ttu-id="fcf00-106">MDOP 그룹 정책 템플릿 다운로드 및 배포</span><span class="sxs-lookup"><span data-stu-id="fcf00-106">Downloading and deploying the MDOP Group Policy templates</span></span>


<span data-ttu-id="fcf00-107">MDOP 그룹 정책 템플릿은 기술 및 버전별 그룹화 된 자동 압축 풀림 압축 파일에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-107">MDOP Group Policy templates are available for download in a self-extracting, compressed file, grouped by technology and version.</span></span>

**<span data-ttu-id="fcf00-108">MDOP 그룹 정책 템플릿을 다운로드 하 고 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="fcf00-108">How to download and deploy the MDOP Group Policy templates</span></span>**

1. <span data-ttu-id="fcf00-109">[Microsoft 데스크톱 최적화 팩 그룹 정책 관리 템플릿에서](https://www.microsoft.com/download/details.aspx?id=55531)MDOP 그룹 정책 서식 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-109">Download the MDOP Group Policy templates from [Microsoft Desktop Optimization Pack Group Policy Administrative Templates](https://www.microsoft.com/download/details.aspx?id=55531).</span></span>

2. <span data-ttu-id="fcf00-110">다운로드 한 파일을 실행 하 여 서식 파일 폴더의 압축을 풉니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-110">Run the downloaded file to extract the template folders.</span></span>

   **<span data-ttu-id="fcf00-111">Warning</span><span class="sxs-lookup"><span data-stu-id="fcf00-111">Warning</span></span>**  
   <span data-ttu-id="fcf00-112">그룹 정책 배포 디렉터리로 직접 서식 파일의 압축을 풀지 마세요.</span><span class="sxs-lookup"><span data-stu-id="fcf00-112">Do not extract the templates directly to the Group Policy deployment directory.</span></span> <span data-ttu-id="fcf00-113">여러 기술과 버전이이 파일에 번들로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-113">Multiple technologies and versions are bundled in this file.</span></span>



3. <span data-ttu-id="fcf00-114">추출 된 폴더에서 기술-버전의 admx 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-114">In the extracted folder, locate the technology-version .admx file.</span></span> <span data-ttu-id="fcf00-115">특정 MDOP 기술에는 그룹 정책 개체 (Gpo) 집합이 여러 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-115">Certain MDOP technologies have multiple sets of Group Policy Objects (GPOs).</span></span> <span data-ttu-id="fcf00-116">예를 들어 MBAM에는 MBAM 관리 설정과 MBAM 사용자 설정이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-116">For example, MBAM includes MBAM Management settings and MBAM User settings.</span></span>

4. <span data-ttu-id="fcf00-117">언어 문화권에 따라 적절 한 adml 파일을 찾습니다 (영어-미국에 해당 하는 *en-us* ).</span><span class="sxs-lookup"><span data-stu-id="fcf00-117">Locate the appropriate .adml file by language-culture (that is, *en* for English-United States).</span></span>

5. <span data-ttu-id="fcf00-118">Admx 및 adml 파일을 정책 정의 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-118">Copy the .admx and .adml files to a policy definition folder.</span></span> <span data-ttu-id="fcf00-119">템플릿을 저장 하는 위치에 따라 로컬 장치 또는 도메인의 컴퓨터에서 그룹 정책 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-119">Depending on where you store the templates, you can configure Group Policy settings from the local device or from any computer on the domain.</span></span>

   **<span data-ttu-id="fcf00-120">로컬 파일</span><span class="sxs-lookup"><span data-stu-id="fcf00-120">Local files.</span></span>** <span data-ttu-id="fcf00-121">로컬 장치에서 그룹 정책 설정을 구성 하려면 서식 파일을 다음 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-121">To configure Group Policy settings from the local device, copy template files to the following locations:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="fcf00-122">파일 형식</span><span class="sxs-lookup"><span data-stu-id="fcf00-122">File type</span></span></th>
   <th align="left"><span data-ttu-id="fcf00-123">파일 위치</span><span class="sxs-lookup"><span data-stu-id="fcf00-123">File location</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="fcf00-124">그룹 정책 템플릿 (admx)</span><span class="sxs-lookup"><span data-stu-id="fcf00-124">Group Policy template (.admx)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="fcf00-125">&lt;강력한 &gt; policydefinitions</span><span class="sxs-lookup"><span data-stu-id="fcf00-125">&lt;strong&gt;policyDefinitions</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="fcf00-126">그룹 정책 언어 파일 (adml)</span><span class="sxs-lookup"><span data-stu-id="fcf00-126">Group Policy language file (.adml)</span></span></p></td>
   <td align="left"><p><code>%systemroot%</code><span data-ttu-id="fcf00-127">&lt;강력한 &gt; policydefinitions</span><span class="sxs-lookup"><span data-stu-id="fcf00-127">&lt;strong&gt;policyDefinitions</span></span></strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. <span data-ttu-id="fcf00-128">GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 사용 하 여 그룹 정책 설정을 편집 하 여 MDOP 기술에 대 한 그룹 정책 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-128">Edit the Group Policy settings using Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) to configure Group Policy settings for the MDOP technology.</span></span> <span data-ttu-id="fcf00-129">자세한 내용은 [MBAM 2.5 그룹 정책 설정을 편집](editing-the-mbam-25-group-policy-settings.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fcf00-129">See [Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md) for more information.</span></span>

   <span data-ttu-id="fcf00-130">그룹 정책 설정에 대 한 설명은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fcf00-130">For descriptions of the Group Policy settings, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>


## <span data-ttu-id="fcf00-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fcf00-131">Related topics</span></span>


[<span data-ttu-id="fcf00-132">MBAM 2.5 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="fcf00-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)


## <span data-ttu-id="fcf00-133">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="fcf00-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fcf00-134">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fcf00-135">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcf00-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






