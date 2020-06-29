---
title: MBAM 2.5 정보
description: MBAM 2.5 정보
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824213"
---
# <span data-ttu-id="9dee5-103">MBAM 2.5 정보</span><span class="sxs-lookup"><span data-stu-id="9dee5-103">About MBAM 2.5</span></span>


<span data-ttu-id="9dee5-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5은 BitLocker 드라이브 암호화를 위한 간단한 관리 인터페이스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="9dee5-105">BitLocker는 분실 하거나 도난당 한 컴퓨터에 대 한 데이터 절도 또는 데이터 노출에 대 한 향상 된 보호 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="9dee5-106">BitLocker는 Windows 운영 체제 볼륨 및 드라이브 및 구성 된 데이터 드라이브에 저장 된 모든 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-106">BitLocker encrypts all data that is stored on the Windows operating system volumes and drives and configured data drives.</span></span>

## <span data-ttu-id="9dee5-107">MBAM 개요</span><span class="sxs-lookup"><span data-stu-id="9dee5-107">Overview of MBAM</span></span>


<span data-ttu-id="9dee5-108">MBAM 2.5에는 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-108">MBAM 2.5 has the following features:</span></span>

-   <span data-ttu-id="9dee5-109">관리자가 엔터프라이즈 전체의 클라이언트 컴퓨터에서 볼륨을 암호화 하는 프로세스를 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="9dee5-110">보안 관리자가 개별 컴퓨터 또는 엔터프라이즈 자체의 준수 상태를 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="9dee5-111">Microsoft System Center Configuration Manager를 사용 하 여 중앙 집중식 보고 및 하드웨어 관리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="9dee5-112">최종 사용자에 게 BitLocker PIN 및 복구 키 요청을 지원 하기 위해 지원 센터의 작업량을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="9dee5-113">셀프 서비스 포털을 사용 하 여 최종 사용자가 암호화 된 장치를 별도로 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="9dee5-114">보안 책임자가 키 정보 복구에 대 한 액세스를 쉽게 감사할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="9dee5-115">Windows Enterprise 사용자가 회사 데이터를 보호 한다는 보장으로 어디서 나 계속 작업 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="9dee5-116">MBAM은 엔터프라이즈에 대해 설정한 BitLocker 암호화 정책 옵션을 적용 하 고, 해당 정책으로 클라이언트 컴퓨터의 준수 여부를 모니터링 하 고, 엔터프라이즈 및 개인 컴퓨터의 암호화 상태를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="9dee5-117">또한, MBAM은 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="9dee5-118">다음 그룹은 MBAM을 사용 하 여 BitLocker를 관리 하는 데 관심이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="9dee5-119">권한 부여 없이 기밀 데이터가 공개 되지 않는지 확인 하는 관리자, IT 보안 전문가 및 규정 준수 책임자</span><span class="sxs-lookup"><span data-stu-id="9dee5-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="9dee5-120">원격 또는 지사에서 컴퓨터 보안을 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="9dee5-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="9dee5-121">Windows를 실행 하는 클라이언트 컴퓨터를 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="9dee5-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="9dee5-122">**참고**  이 MBAM 설명서에는 BitLocker에 대해 자세히 설명 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="9dee5-123">자세한 내용은 [BitLocker 드라이브 암호화 개요](https://go.microsoft.com/fwlink/p/?LinkId=225013)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5"></a><span data-ttu-id="9dee5-124">MBAM 2.5의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="9dee5-124">What’s new in MBAM 2.5</span></span>


<span data-ttu-id="9dee5-125">이 섹션에서는 MBAM 2.5의 새로운 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-125">This section describes the new features in MBAM 2.5.</span></span>

### <span data-ttu-id="9dee5-126">Microsoft SQL Server 2014에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="9dee5-126">Support for Microsoft SQL Server 2014</span></span>

<span data-ttu-id="9dee5-127">MBAM은 이전 버전의 MBAM에서 지원 되는 소프트웨어 외에 Microsoft SQL Server 2014에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-127">MBAM adds support for Microsoft SQL Server 2014, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> <span data-ttu-id="9dee5-128">MBAM 그룹 정책 서식 파일을 별도로 다운로드</span><span class="sxs-lookup"><span data-stu-id="9dee5-128">MBAM Group Policy Templates downloaded separately</span></span>

<span data-ttu-id="9dee5-129">MBAM 그룹 정책 서식 파일은 MBAM 설치와 별도로 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-129">The MBAM Group Policy Templates must be downloaded separately from the MBAM installation.</span></span> <span data-ttu-id="9dee5-130">이전 버전의 MBAM에는 mbam 설치 관리자에 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 필수 MBAM Gpo (그룹 정책 개체)가 포함 된 MBAM 정책 템플릿이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-130">In previous versions of MBAM, the MBAM installer included an MBAM Policy Template, which contained the required MBAM-specific Group Policy Objects (GPOs) that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="9dee5-131">이러한 Gpo는 MBAM 설치 관리자에서 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-131">These GPOs have been removed from the MBAM installer.</span></span> <span data-ttu-id="9dee5-132">이제 MBAM 클라이언트 설치를 시작 하기 전에 [MDOP 그룹 정책 (admx) 템플릿을 가져오고](https://go.microsoft.com/fwlink/p/?LinkId=393941) 이를 서버 또는 워크스테이션에 복사 하는 방법에서 gpo를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-132">You now download the GPOs from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation before you begin the MBAM Client installation.</span></span> <span data-ttu-id="9dee5-133">Windows Server 또는 Windows 운영 체제의 지원 되는 버전을 실행 하는 모든 서버 또는 워크스테이션에 그룹 정책 템플릿을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-133">You can copy the Group Policy Templates to any server or workstation that is running a supported version of the Windows Server or Windows operating system.</span></span>

<span data-ttu-id="9dee5-134">**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-134">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="9dee5-135">**MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 Bitlocker 드라이브 암호화 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-135">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the BitLocker Drive Encryption settings for you.</span></span>

 

<span data-ttu-id="9dee5-136">서버 또는 워크스테이션에 복사 해야 하는 서식 파일은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-136">The template files that you need to copy to a server or workstation are:</span></span>

-   <span data-ttu-id="9dee5-137">BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="9dee5-137">BitLockerManagement.adml</span></span>

-   <span data-ttu-id="9dee5-138">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="9dee5-138">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="9dee5-139">BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="9dee5-139">BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="9dee5-140">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="9dee5-140">BitLockerUserManagement.admx</span></span>

<span data-ttu-id="9dee5-141">서식 파일을 사용자의 요구에 가장 잘 맞는 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-141">Copy the template files to the location that best meets your needs.</span></span> <span data-ttu-id="9dee5-142">언어별 폴더에 복사 해야 하는 언어별 파일의 경우 해당 파일을 보려면 그룹 정책 관리 콘솔이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-142">For the language-specific files, which must be copied to a language-specific folder, the Group Policy Management Console is required to view the files.</span></span>

- <span data-ttu-id="9dee5-143">서버 또는 워크스테이션에 로컬로 서식 파일을 설치 하려면 다음 위치 중 하나에 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-143">To install the template files locally on a server or workstation, copy the files to one of the following locations.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="9dee5-144">파일 형식</span><span class="sxs-lookup"><span data-stu-id="9dee5-144">File type</span></span></th>
  <th align="left"><span data-ttu-id="9dee5-145">파일 위치</span><span class="sxs-lookup"><span data-stu-id="9dee5-145">File location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="9dee5-146">언어 중립 (admx)</span><span class="sxs-lookup"><span data-stu-id="9dee5-146">language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="9dee5-147">% \ systemroot% </em> \Policydefinitions</span><span class="sxs-lookup"><span data-stu-id="9dee5-147">%systemroot%</em>\policyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="9dee5-148">언어별 (adml)</span><span class="sxs-lookup"><span data-stu-id="9dee5-148">language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="9dee5-149">% systemroot% </em> \Policydefinitions [ <em> MUIculture </em> ] (예를 들어 미국 영어 언어 관련 파일이 <em> % systemroot% &lt; /em policydefinition\ \ u s에 저장 됩니다. \ n/ &gt; us)</span><span class="sxs-lookup"><span data-stu-id="9dee5-149">%systemroot%</em>\policyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language specific file will be stored in <em>%systemroot%&lt;/em&gt;policyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

- <span data-ttu-id="9dee5-150">도메인에 있는 모든 그룹 정책 관리자가 서식 파일을 사용할 수 있도록 하려면 도메인 컨트롤러의 다음 위치 중 하나에 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-150">To make the templates available to all Group Policy administrators in a domain, copy the files to one of the following locations on a domain controller.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="9dee5-151">파일 형식</span><span class="sxs-lookup"><span data-stu-id="9dee5-151">File type</span></span></th>
  <th align="left"><span data-ttu-id="9dee5-152">도메인 컨트롤러 파일 위치</span><span class="sxs-lookup"><span data-stu-id="9dee5-152">Domain controller file location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="9dee5-153">언어 중립 (admx)</span><span class="sxs-lookup"><span data-stu-id="9dee5-153">Language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="9dee5-154">% systemroot% </em> sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="9dee5-154">%systemroot%</em>sysvol\domain\policies\PolicyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="9dee5-155">언어별 (adml)</span><span class="sxs-lookup"><span data-stu-id="9dee5-155">Language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="9dee5-156">% systemroot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (예: 미국 영어 언어별 파일은 <em> % systemroot% \sysvol\domain\policies\PolicyDefinitions\en-us에 저장 됩니다. </em> )</span><span class="sxs-lookup"><span data-stu-id="9dee5-156">%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language-specific file will be stored in <em>%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

<span data-ttu-id="9dee5-157">서식 파일에 대 한 자세한 내용은 [그룹 정책 ADMX 파일 관리 단계별 가이드](https://go.microsoft.com/fwlink/?LinkId=392818)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-157">For more information about template files, see [Managing Group Policy ADMX Files Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=392818).</span></span>

### <span data-ttu-id="9dee5-158">운영 체제 및 고정 데이터 드라이브에 대 한 암호화 정책 적용 기능</span><span class="sxs-lookup"><span data-stu-id="9dee5-158">Ability to enforce encryption policies on operating system and fixed data drives</span></span>

<span data-ttu-id="9dee5-159">MBAM 2.5를 사용 하 여 조직의 컴퓨터에 대 한 운영 체제 및 고정 데이터 드라이브에 대 한 암호화 정책을 적용 하 고 최종 사용자가 MBAM 암호화 정책을 준수 하기 위해 요구 사항에 대 한 postponement 요청 하는 일 수를 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-159">MBAM2.5 enables you to enforce encryption policies on operating system and fixed data drives for computers in your organization and limit the number of days that end users can request a postponement of the requirement to comply with MBAM encryption policies.</span></span>

<span data-ttu-id="9dee5-160">암호화 정책 적용을 구성할 수 있도록 하려면 운영 체제 드라이브 및 고정 데이터 드라이브에 대해 암호화 정책 적용 설정 이라는 새 그룹 정책 설정이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-160">To enable you to configure encryption policy enforcement, a new Group Policy setting, called Encryption Policy Enforcement Settings, has been added for operating system drives and fixed data drives.</span></span> <span data-ttu-id="9dee5-161">이 정책은 다음 표에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-161">This policy is described in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dee5-162">그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="9dee5-162">Group Policy setting</span></span></th>
<th align="left"><span data-ttu-id="9dee5-163">설명</span><span class="sxs-lookup"><span data-stu-id="9dee5-163">Description</span></span></th>
<th align="left"><span data-ttu-id="9dee5-164">이 설정을 구성 하는 데 사용 되는 그룹 정책 노드</span><span class="sxs-lookup"><span data-stu-id="9dee5-164">Group Policy node used to configure this setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dee5-165">암호화 정책 적용 설정 (운영 체제 드라이브)</span><span class="sxs-lookup"><span data-stu-id="9dee5-165">Encryption Policy Enforcement Settings (Operating System Drive)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-166">이 설정을 사용 하는 경우 <strong> 운영 체제 드라이브에서 유예 기간을 구성할 수 있는 비 준수 유예 기간 (일)을 구성 하는 옵션을 사용 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-166">For this setting, use the option <strong>Configure the number of noncompliance grace period days for operating system drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="9dee5-167">유예 기간은 드라이브가 비규격으로 검색 된 후 최종 사용자가 해당 운영 체제 드라이브에 대 한 MBAM 정책 준수를 연기할 수 있는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-167">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their operating system drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="9dee5-168">구성 된 유예 기간이 만료 되 면 사용자는 필요한 작업을 연기 하거나 예외를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-168">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span></p>
<p><span data-ttu-id="9dee5-169">사용자 조작이 필요한 경우 (예: TPM (신뢰할 수 있는 플랫폼 모듈) + PIN을 사용 하거나 암호 보호기를 사용 하는 경우) 대화 상자가 나타나고 사용자가 필요한 정보를 제공할 때까지 닫을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-169">If user interaction is required (for example, if you are using the Trusted Platform Module (TPM) + PIN or using a password protector), a dialog box appears, and users cannot close it until they provide the required information.</span></span> <span data-ttu-id="9dee5-170">보호기만 TPM 인 경우 사용자 입력 없이 백그라운드에서 암호화가 즉시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-170">If the protector is TPM only, encryption begins immediately in the background without user input.</span></span></p>
<p><span data-ttu-id="9dee5-171">사용자는 BitLocker 암호화 마법사를 통해 예외를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-171">Users cannot request exemptions through the BitLocker encryption wizard.</span></span> <span data-ttu-id="9dee5-172">그 대신 지원 센터에 문의 하거나 조직에서 예외를 요청 하는 데 사용 하는 모든 프로세스를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-172">Instead, they must contact their Help Desk or use whatever process their organization uses for exemption requests.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-173">컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; Windows 구성 요소 &gt; MDOP Mbam (BitLocker Management) &gt; 운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="9dee5-173">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Operating System Drive</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dee5-174">암호화 정책 적용 설정 (고정 데이터 드라이브)</span><span class="sxs-lookup"><span data-stu-id="9dee5-174">Encryption Policy Enforcement Settings (Fixed Data Drives)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-175">이 설정에 대해 옵션을 사용 하 여 <strong> 유예 기간을 구성할 고정 드라이브의 비 준수 유예 기간 일 수를 구성 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-175">For this setting, use the option <strong>Configure the number of noncompliance grace period days for fixed drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="9dee5-176">유예 기간은 드라이브가 비규격으로 검색 된 후 최종 사용자가 해당 고정 드라이브에 대 한 MBAM 정책 준수를 연기할 수 있는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-176">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their fixed drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="9dee5-177">유예 기간은 고정 드라이브를 비규격으로 결정할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-177">The grace period begins when the fixed drive is determined to be noncompliant.</span></span> <span data-ttu-id="9dee5-178">자동 잠금 해제를 사용 하는 경우 운영 체제 드라이브가 호환 될 때까지 정책이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-178">If you are using auto-unlock, the policy will not be enforced until the operating system drive is compliant.</span></span> <span data-ttu-id="9dee5-179">그러나 자동 잠금 해제를 사용 하지 않는 경우에는 운영 체제 드라이브가 완전히 암호화 되기 전에 고정 데이터 드라이브의 암호화가 시작 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-179">However, if you are not using auto-unlock, encryption of the fixed data drive can begin before the operating system drive is fully encrypted.</span></span></p>
<p><span data-ttu-id="9dee5-180">구성 된 유예 기간이 만료 되 면 사용자는 필요한 작업을 연기 하거나 예외를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-180">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span> <span data-ttu-id="9dee5-181">사용자 조작이 필요한 경우 대화 상자가 나타나고 사용자가 필요한 정보를 제공할 때까지 닫을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-181">If user interaction is required, a dialog box appears and users cannot close it until they provide the required information.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-182">컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; Windows 구성 요소 &gt; MDOP Mbam (BitLocker Management) &gt; 고정 드라이브</span><span class="sxs-lookup"><span data-stu-id="9dee5-182">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Fixed Drive</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9dee5-183">BitLocker 드라이브 암호화 마법사에서 보안 정책을 가리키는 URL을 제공 하는 기능</span><span class="sxs-lookup"><span data-stu-id="9dee5-183">Ability to provide a URL in the BitLocker Drive Encryption wizard to point to your security policy</span></span>

<span data-ttu-id="9dee5-184">새 그룹 정책 설정을 사용 하 여 **보안 정책 링크에 대 한 url을 제공**하면 최종 사용자에 게 표시 되는 Url을 **회사 보안 정책**이라는 링크로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-184">A new Group Policy setting, **Provide the URL for the Security Policy link**, enables you to configure a URL that will be presented to end users as a link called **Company Security Policy**.</span></span> <span data-ttu-id="9dee5-185">이 링크는 MBAM이 볼륨을 암호화 하도록 사용자에 게 메시지를 표시 하는 경우에 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-185">This link will appear when MBAM prompts users to encrypt a volume.</span></span>

<span data-ttu-id="9dee5-186">이 정책 설정을 사용 하면 **회사 보안 정책** 링크에 대 한 URL을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-186">If you enable this policy setting, you can configure the URL for the **Company Security Policy** link.</span></span> <span data-ttu-id="9dee5-187">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 **회사 보안 정책** 링크가 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-187">If you disable or do not configure this policy setting, the **Company Security Policy** link is not displayed to users.</span></span>

<span data-ttu-id="9dee5-188">새 그룹 정책 설정은 다음 GPO 노드에 있습니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management) &gt; 클라이언트 관리**</span><span class="sxs-lookup"><span data-stu-id="9dee5-188">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management) &gt; Client Management**.</span></span>

### <span data-ttu-id="9dee5-189">FIPS 규격 복구 키 지원</span><span class="sxs-lookup"><span data-stu-id="9dee5-189">Support for FIPS-compliant recovery keys</span></span>

<span data-ttu-id="9dee5-190">MBAM 2.5는 Windows 8.1 운영 체제를 실행 하는 디바이스에서 FIPS (미국 정보 처리 표준) 규격 BitLocker 복구 키를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-190">MBAM2.5 supports Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices that are running the Windows8.1 operating system.</span></span> <span data-ttu-id="9dee5-191">복구 키는 이전 버전의 Windows에서 FIPS 규격이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-191">The recovery key was not FIPS compliant in earlier versions of Windows.</span></span> <span data-ttu-id="9dee5-192">이 향상 된 기능은 최종 사용자가 자체 서비스 포털 또는 관리 및 모니터링 웹 사이트 (지원 센터)를 사용 하 여 드라이브의 PIN 이나 암호를 잊었거나 컴퓨터를 잠근 경우 드라이브를 복구할 수 있도록 하기 때문에 FIPS 준수를 필요로 하는 조직의 드라이브 복구 프로세스를 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-192">This enhancement improves the drive recovery process in organizations that require FIPS compliance because it enables end users to use the Self-Service Portal or Administration and Monitoring Website (Help Desk) to recover their drives if they forget their PIN or password or get locked out of their computers.</span></span> <span data-ttu-id="9dee5-193">새로운 FIPS 준수 기능은 암호 보호기로 확장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-193">The new FIPS compliance feature does not extend to password protectors.</span></span>

<span data-ttu-id="9dee5-194">조직에서 FIPS 준수를 사용 하도록 설정 하려면 연방 정보 처리 표준 (FIPS) 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-194">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="9dee5-195">구성 방법에 대 한 자세한 내용은 [BitLocker 그룹 정책 설정을](https://go.microsoft.com/fwlink/?LinkId=393560)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-195">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

<span data-ttu-id="9dee5-196">[설치 된 BitLocker 핫픽스](https://support.microsoft.com/kb/3015477)없이 Windows8 또는 Windows7 운영 체제를 실행 하는 클라이언트 컴퓨터의 경우 IT 관리자는 FIPS 규격 환경에서 계속 해 서 DRA (Data Recovery agent) 보호기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-196">For client computers that are running the Windows8 or Windows7 operating systems without the [installed BitLocker hotfix](https://support.microsoft.com/kb/3015477), IT administrators will continue to use the Data Recovery Agents (DRA) protector in FIPS-compliant environments.</span></span> <span data-ttu-id="9dee5-197">DRA에 대 한 자세한 내용은 [BitLocker를 사용 하 여 데이터 복구 에이전트 사용](https://go.microsoft.com/fwlink/?LinkId=393557)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-197">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

<span data-ttu-id="9dee5-198">Windows 7 및 Windows 8 컴퓨터용 BitLocker 핫픽스를 다운로드 하 고 설치 하려면 [Bitlocker 관리 및 모니터링 2.5에 대 한 핫픽스 패키지 2](https://support.microsoft.com/kb/3015477) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-198">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="9dee5-199">고가용성 배포 지원</span><span class="sxs-lookup"><span data-stu-id="9dee5-199">Support for high availability deployments</span></span>

<span data-ttu-id="9dee5-200">MBAM은 표준 2 서버 및 구성 관리자 통합 토폴로지와 함께 다음과 같은 고가용성 시나리오를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-200">MBAM supports the following high-availability scenarios in addition to the standard two-server and Configuration Manager Integration topologies:</span></span>

-   <span data-ttu-id="9dee5-201">SQL Server AlwaysOn 가용성 그룹</span><span class="sxs-lookup"><span data-stu-id="9dee5-201">SQL Server AlwaysOn availability groups</span></span>

-   <span data-ttu-id="9dee5-202">SQL Server 클러스터링</span><span class="sxs-lookup"><span data-stu-id="9dee5-202">SQL Server clustering</span></span>

-   <span data-ttu-id="9dee5-203">NLB (네트워크 부하 분산)</span><span class="sxs-lookup"><span data-stu-id="9dee5-203">Network load balancing (NLB)</span></span>

-   <span data-ttu-id="9dee5-204">SQL Server 미러링</span><span class="sxs-lookup"><span data-stu-id="9dee5-204">SQL Server mirroring</span></span>

-   <span data-ttu-id="9dee5-205">VSS (볼륨 섀도 복사본 서비스) 백업</span><span class="sxs-lookup"><span data-stu-id="9dee5-205">Volume Shadow Copy Service (VSS) Backup</span></span>

<span data-ttu-id="9dee5-206">이러한 기능에 대 한 자세한 내용은 [MBAM 2.5 고가용성에 대 한 계획](planning-for-mbam-25-high-availability.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-206">For more information about these features, see [Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md).</span></span>

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a><span data-ttu-id="9dee5-207">관리 및 모니터링 웹 사이트의 역할 관리 변경</span><span class="sxs-lookup"><span data-stu-id="9dee5-207">Management of roles for Administration and Monitoring Website changed</span></span>

<span data-ttu-id="9dee5-208">MBAM 2.5에서는 관리 및 모니터링 웹 사이트에 대 한 액세스 권한을 제공 하는 역할을 관리 하기 위해 Active Directory 도메인 서비스 (추가)에서 보안 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-208">In MBAM2.5, you must create security groups in Active Directory Domain Services (ADDS) to manage the roles that provide access rights to the Administration and Monitoring Website.</span></span> <span data-ttu-id="9dee5-209">역할을 사용 하면 특정 보안 그룹에 속한 사용자가 보고서 보기, 최종 사용자의 암호화 된 드라이브 복구 등의 다른 작업을 웹 사이트에서 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-209">Roles enable users who are in specific security groups to perform different tasks in the website such as viewing reports or helping end users recover encrypted drives.</span></span> <span data-ttu-id="9dee5-210">이전 버전의 MBAM에서는 로컬 그룹을 사용 하 여 역할을 관리 했습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-210">In previous versions of MBAM, roles were managed by using local groups.</span></span>

<span data-ttu-id="9dee5-211">MBAM 2.5에서 "역할" 이라는 용어는 이전 버전의 MBAM에 사용 된 "관리자 역할" 이라는 용어를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-211">In MBAM2.5, the term “roles” replaces the term “administrator roles,” which was used in earlier versions of MBAM.</span></span> <span data-ttu-id="9dee5-212">또한 MBAM 2.5에서는 "MBAM 시스템 관리자" 역할이 제거 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-212">In addition, in MBAM2.5 the “MBAM System Administrators” role has been removed.</span></span>

<span data-ttu-id="9dee5-213">다음 표에는 AD DS에서 만들어야 하는 보안 그룹이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-213">The following table lists the security groups that you must create in AD DS.</span></span> <span data-ttu-id="9dee5-214">보안 그룹의 모든 이름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-214">You can use any name for the security groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dee5-215">역할</span><span class="sxs-lookup"><span data-stu-id="9dee5-215">Role</span></span></th>
<th align="left"><span data-ttu-id="9dee5-216">관리 및 모니터링 웹 사이트의이 역할에 대 한 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="9dee5-216">Access rights for this role on the Administration and Monitoring Website</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dee5-217">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="9dee5-217">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-218">MBAM 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 대 한 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-218">Provides access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="9dee5-219">이러한 영역에 대 한 액세스 권한이 있는 사용자는 두 영역 중 하나를 사용할 때 모든 필드를 채워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-219">Users who have access to these areas must fill in all fields when they use either area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dee5-220">MBAM 보고서 사용자</span><span class="sxs-lookup"><span data-stu-id="9dee5-220">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-221">관리 및 모니터링 웹 사이트의 보고서에 대 한 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-221">Provides access to the Reports in the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dee5-222">MBAM 헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="9dee5-222">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-223">관리 및 모니터링 웹 사이트의 모든 영역에 대 한 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-223">Provides access to all areas in the Administration and Monitoring Website.</span></span> <span data-ttu-id="9dee5-224">최종 사용자가 드라이브를 복구 하는 데 도움이 되는 경우이 그룹의 사용자는 최종 사용자의 도메인 및 사용자 이름이 아닌 복구 키만 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-224">Users in this group have to enter only the recovery key, not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="9dee5-225">사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 사용자 그룹 권한 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-225">If a user is a member of the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users group permissions.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9dee5-226">추가에서 보안 그룹을 만든 후 해당 보안 그룹에 사용자 및/또는 그룹을 지정 하 여 관리 및 모니터링 웹 사이트에 대 한 해당 수준의 액세스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-226">After you create the security groups in ADDS, assign users and/or groups to the appropriate security group to enable the corresponding level of access to the Administration and Monitoring Website.</span></span> <span data-ttu-id="9dee5-227">각 역할의 사용자가 관리 및 모니터링 웹 사이트에 액세스할 수 있도록 하려면 관리 및 모니터링 웹 사이트를 구성할 때 각 보안 그룹도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-227">To enable individuals with each role to access the Administration and Monitoring Website, you must also specify each security group when you are configuring the Administration and Monitoring Website.</span></span>

### <span data-ttu-id="9dee5-228">MBAM 서버 기능을 구성 하기 위한 Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="9dee5-228">Windows PowerShell cmdlets for configuring MBAM Server features</span></span>

<span data-ttu-id="9dee5-229">MBAM 2.5 용 Windows PowerShell cmdlet을 사용 하면 MBAM 서버 기능을 구성 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-229">Windows PowerShell cmdlets for MBAM2.5 enable you to configure and manage the MBAM Server features.</span></span> <span data-ttu-id="9dee5-230">각 기능에는 기능을 사용 하거나 사용 하지 않도록 설정 하거나 기능에 대 한 정보를 가져오는 데 사용할 수 있는 해당 Windows PowerShell cmdlet이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-230">Each feature has a corresponding Windows PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="9dee5-231">Windows PowerShell을 사용 하기 위한 필수 구성 요소 및 필수 구성 요소는 [Windows powershell을 사용 하 여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-231">For prerequisites and prerequisites for using Windows PowerShell, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

**<span data-ttu-id="9dee5-232">MBAM 서버 소프트웨어를 설치한 후 Windows PowerShell cmdlet에 대 한 MBAM 2.5 도움말을 로드 하려면</span><span class="sxs-lookup"><span data-stu-id="9dee5-232">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="9dee5-233">Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-233">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="9dee5-234">Type **Update-도움말-Microsoft \* MBAM**.</span><span class="sxs-lookup"><span data-stu-id="9dee5-234">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

<span data-ttu-id="9dee5-235">MBAM에 대 한 Windows PowerShell 도움말은 다음 형식으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-235">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dee5-236">Windows PowerShell 도움말 형식</span><span class="sxs-lookup"><span data-stu-id="9dee5-236">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="9dee5-237">추가 정보</span><span class="sxs-lookup"><span data-stu-id="9dee5-237">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dee5-238">Windows PowerShell 명령 프롬프트에서 <strong> get-help </strong> &lt; <em> cmdlet을 입력 합니다.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="9dee5-238">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dee5-239">최신 Windows PowerShell cmdlet을 업로드 하려면, MBAM에 대 한 Windows PowerShell 도움말을 로드 하는 방법에 대 한 이전 섹션의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-239">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dee5-240">웹 페이지로 TechNet에서</span><span class="sxs-lookup"><span data-stu-id="9dee5-240">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dee5-241">다운로드 센터에서 Word .docx 파일로</span><span class="sxs-lookup"><span data-stu-id="9dee5-241">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dee5-242">.Pdf 파일로 다운로드 센터에서</span><span class="sxs-lookup"><span data-stu-id="9dee5-242">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9dee5-243">ASCII 전용 및 향상 된 Pin 및 순차적 및 반복 되는 문자 방지 기능 지원</span><span class="sxs-lookup"><span data-stu-id="9dee5-243">Support for ASCII-only and enhanced PINs and ability to prevent sequential and repeating characters</span></span>

**<span data-ttu-id="9dee5-244">시작 그룹 정책 설정에 향상 된 Pin 허용</span><span class="sxs-lookup"><span data-stu-id="9dee5-244">Allow enhanced PINs for startup Group Policy setting</span></span>**

<span data-ttu-id="9dee5-245">그룹 정책 설정, **시작 Pin 허용**, BitLocker에 향상 된 시작 pin을 사용할지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-245">The Group Policy setting, **Allow enhanced PINs for startup**, enables you to configure whether enhanced startup PINs are used with BitLocker.</span></span> <span data-ttu-id="9dee5-246">향상 된 시작 Pin을 통해 사용자는 대/소문자, 기호, 숫자, 공백을 포함 하 여 전체 키보드에 키를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-246">Enhanced startup PINs permit users to enter any keys on a full keyboard, including uppercase and lowercase letters, symbols, numbers, and spaces.</span></span> <span data-ttu-id="9dee5-247">이 정책 설정을 사용 하면 설정 된 모든 새 BitLocker 시작 핀의 Pin이 향상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-247">If you enable this policy setting, all new BitLocker startup PINs that are set will be enhanced PINs.</span></span> <span data-ttu-id="9dee5-248">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 강화 된 Pin을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-248">If you disable or do not configure this policy setting, enhanced PINs cannot be used.</span></span>

<span data-ttu-id="9dee5-249">일부 컴퓨터는 PXE (사전 부팅 실행 환경)에서 향상 된 Pin의 항목을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-249">Not all computers support the entry of enhanced PINs in the Pre-Boot Execution Environment (PXE).</span></span> <span data-ttu-id="9dee5-250">조직에 대해이 그룹 정책 설정을 사용 하도록 설정 하기 전에 BitLocker 설치 프로세스 중 시스템 검사를 실행 하 여 컴퓨터의 BIOS가 PXE의 전체 키보드 사용을 지원 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-250">Before you enable this Group Policy setting for your organization, run a system check during the BitLocker setup process to ensure that the computer’s BIOS supports the use of the full keyboard in PXE.</span></span> <span data-ttu-id="9dee5-251">자세한 내용은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-251">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

**<span data-ttu-id="9dee5-252">ASCII 전용 핀이 필요 함 확인란</span><span class="sxs-lookup"><span data-stu-id="9dee5-252">Require ASCII-only PINs check box</span></span>**

<span data-ttu-id="9dee5-253">**시작에 향상 된 Pin 허용** 그룹 정책 설정에도 **ASCII 전용 pin 필요** 확인란이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-253">The **Allow enhanced PINs for startup** Group Policy setting also contains a **Require ASCII-only PINs** check box.</span></span> <span data-ttu-id="9dee5-254">조직의 컴퓨터에서 PXE의 전체 키보드 사용을 지원 하지 않는 경우 **시작 그룹에 대해 향상 된 Pin 허용** 확인란을 사용 하도록 설정한 다음 **Ascii 전용 pin 필요** 확인란을 선택 하 여 향상 된 PIN에 인쇄 가능한 ASCII 문자만 사용 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-254">If the computers in your organization do not support the use of the full keyboard in PXE, you can enable the **Allow enhanced PINs for startup** Group Policy setting, and then select the **Require ASCII-only PINs** check box to require that enhanced PINs use only printable ASCII characters.</span></span>

**<span data-ttu-id="9dee5-255">비순차 및 반복 되지 않는 문자의 강제 사용</span><span class="sxs-lookup"><span data-stu-id="9dee5-255">Enforced use of nonsequential and nonrepeating characters</span></span>**

<span data-ttu-id="9dee5-256">MBAM 2.5는 최종 사용자가 반복 되는 숫자 (예: 1111) 또는 순차적 번호 (예: 1234)로 구성 된 Pin을 만들 수 없도록 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-256">MBAM2.5 prevents end users from creating PINs that consist of repeating numbers (such as 1111) or sequential numbers (such as 1234).</span></span> <span data-ttu-id="9dee5-257">최종 사용자가 세 개 이상의 반복 또는 순차 번호를 포함 하는 암호를 입력 하려고 하면 Bitlocker 드라이브 암호화 마법사에 오류 메시지가 표시 되 고 사용자가 허용 되지 않은 문자가 있는 PIN을 입력할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-257">If end users try to enter a password that contains three or more repeating or sequential numbers, the Bitlocker Drive Encryption wizard displays an error message and prevents users from entering a PIN with the prohibited characters.</span></span>

### <span data-ttu-id="9dee5-258">BitLocker 컴퓨터 준수 보고서에 DRA 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="9dee5-258">Addition of DRA Certificate to BitLocker Computer Compliance report</span></span>

<span data-ttu-id="9dee5-259">새 보호기 유형, DRA (데이터 복구 에이전트) 인증서가 구성 관리자의 BitLocker 컴퓨터 준수 보고서에 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-259">A new protector type, the Data Recovery Agent (DRA) Certificate, has been added to the BitLocker Computer Compliance Report in Configuration Manager.</span></span> <span data-ttu-id="9dee5-260">이 보호기 유형은 운영 체제 드라이브에 적용 되며, **보호 유형** 열의 **컴퓨터 볼륨 (s)** 섹션에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-260">This protector type applies to operating system drives, and it appears in the **Computer Volume(s)** section in the **Protector Types** column.</span></span>

### <span data-ttu-id="9dee5-261">다중 포리스트 지원 배포 지원</span><span class="sxs-lookup"><span data-stu-id="9dee5-261">Support for multi-forest support deployments</span></span>

<span data-ttu-id="9dee5-262">MBAM 2.5는 다음과 같은 유형의 다중 포리스트 배포를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-262">MBAM 2.5 supports the following types of multi-forest deployments:</span></span>

-   <span data-ttu-id="9dee5-263">단일 도메인이 있는 단일 포리스트</span><span class="sxs-lookup"><span data-stu-id="9dee5-263">Single forest with single domain</span></span>

-   <span data-ttu-id="9dee5-264">단일 트리 및 여러 도메인이 있는 단일 포리스트</span><span class="sxs-lookup"><span data-stu-id="9dee5-264">Single forest with a single tree and multiple domains</span></span>

-   <span data-ttu-id="9dee5-265">여러 트리 및 분리 네임 스페이스가 있는 단일 포리스트</span><span class="sxs-lookup"><span data-stu-id="9dee5-265">Single forest with multiple trees and disjoint namespaces</span></span>

-   <span data-ttu-id="9dee5-266">중앙 포리스트 토폴로지의 여러 포리스트</span><span class="sxs-lookup"><span data-stu-id="9dee5-266">Multiple forests in a central forest topology</span></span>

-   <span data-ttu-id="9dee5-267">리소스 포리스트 토폴로지의 여러 포리스트</span><span class="sxs-lookup"><span data-stu-id="9dee5-267">Multiple forests in a resource forest topology</span></span>

<span data-ttu-id="9dee5-268">포리스트 마이그레이션에 대 한 지원 (단일에서 여러 개, 단일에서 single로, 여러 개의 포리스트를 통해 리소스 등으로) 또는 업그레이드 또는 다운 그레이드에 대 한 지원이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-268">There is no support for forest migration (going from single to multiple, multiple to single, resource to across the forest, etc.), or upgrade or downgrade.</span></span>

<span data-ttu-id="9dee5-269">다중 포리스트 배포에서 MBAM을 배포 하기 위한 전제 조건은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-269">The prerequisites for deploying MBAM in multi-forest deployments are:</span></span>

-   <span data-ttu-id="9dee5-270">포리스트는 지원 되는 버전의 Windows Server에서 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-270">Forest must be running on supported versions of Windows Server.</span></span>

-   <span data-ttu-id="9dee5-271">양방향 또는 단방향 트러스트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-271">A two-way or one-way trust is required.</span></span> <span data-ttu-id="9dee5-272">단방향 트러스트의 경우 서버의 도메인이 클라이언트의 도메인을 신뢰 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-272">One-way trusts require that the server’s domain trusts the client’s domain.</span></span> <span data-ttu-id="9dee5-273">즉, 서버의 도메인이 클라이언트의 도메인을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-273">In other words, the server’s domain is pointed at the client’s domain.</span></span>

### <span data-ttu-id="9dee5-274">암호화 된 하드 드라이브에 대 한 MBAM 클라이언트 지원</span><span class="sxs-lookup"><span data-stu-id="9dee5-274">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="9dee5-275">MBAM은 오 팔에 대 한 TCG 사양 요구 사항 및 IEEE 1667 표준을 충족 하는 암호화 된 하드 드라이브에서 BitLocker를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-275">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="9dee5-276">이러한 디바이스에서 BitLocker를 사용 하도록 설정 하면 암호화 된 드라이브에서 키를 생성 하 고 관리 기능을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-276">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="9dee5-277">자세한 내용은 [암호화 된 하드 드라이브](https://technet.microsoft.com/library/hh831627.aspx) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-277">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

## <span data-ttu-id="9dee5-278">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9dee5-278">How to Get MDOP Technologies</span></span>


<span data-ttu-id="9dee5-279">MBAM은 Microsoft 데스크톱 최적화 팩 (MDOP)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-279">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="9dee5-280">MDOP는 Microsoft 소프트웨어 보증 프로그램의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-280">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="9dee5-281">Microsoft 소프트웨어 보증 프로그램 및 MDOP를 구입 하는 방법에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-281">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <a href="" id="---------mbam-2-5-release-notes"></a> <span data-ttu-id="9dee5-282">MBAM 2.5 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="9dee5-282">MBAM 2.5 Release Notes</span></span>


<span data-ttu-id="9dee5-283">이 설명서에 포함 되지 않은 최신 뉴스에 대 한 자세한 내용은 [MBAM 2.5에 대 한 릴리스 정보](release-notes-for-mbam-25.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-283">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5](release-notes-for-mbam-25.md).</span></span>

## <span data-ttu-id="9dee5-284">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="9dee5-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9dee5-285">[여기](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub)에서 여러분의 의견을 보내세요.</span><span class="sxs-lookup"><span data-stu-id="9dee5-285">Send your feedback [here](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span></span> 
- <span data-ttu-id="9dee5-286">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dee5-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="9dee5-287">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9dee5-287">Related topics</span></span>


[<span data-ttu-id="9dee5-288">Microsoft BitLocker 관리 및 모니터링 2.5</span><span class="sxs-lookup"><span data-stu-id="9dee5-288">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="9dee5-289">MBAM 2.5 시작</span><span class="sxs-lookup"><span data-stu-id="9dee5-289">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





