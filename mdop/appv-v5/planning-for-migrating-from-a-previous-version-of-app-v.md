---
title: App-V의 이전 버전에서 마이그레이션 계획
description: App-V의 이전 버전에서 마이그레이션 계획
author: dansimp
ms.assetid: d4ca8f09-86fd-456f-8ec2-242ff94ae9a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2242f58a29473e116506ec013b94a79d1bb814a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813473"
---
# <span data-ttu-id="fc3fb-103">App-V의 이전 버전에서 마이그레이션 계획</span><span class="sxs-lookup"><span data-stu-id="fc3fb-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="fc3fb-104">다음 정보를 사용 하 여 이전 버전의 App-v에서 앱-V 5.0으로 마이그레이션하는 방법을 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-104">Use the following information to plan how to migrate to App-V 5.0 from previous versions of App-V.</span></span>

## <span data-ttu-id="fc3fb-105">마이그레이션 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fc3fb-105">Migration requirements</span></span>


<span data-ttu-id="fc3fb-106">업그레이드를 시작 하기 전에 다음 요구 사항을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="fc3fb-107">App-v 4.6 SP2 이전 버전에서 업그레이드 하는 경우 App-v 5.0 이상으로 업그레이드 하기 전에 먼저 버전 App-V 4.6 SP3으로 업그레이드 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.0 or later.</span></span> <span data-ttu-id="fc3fb-108">이 시나리오에서는 먼저 App-v 클라이언트를 업그레이드 한 다음 서버 구성 요소를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="fc3fb-109">**참고:** App-v 4.6에서 메인스트림 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="fc3fb-110">App-v 5.0는 app-v 5.0를 사용 하 여 만든 패키지만 지원 하거나 App-v 5.0 (**appv**) 형식으로 변환 되는 패키지를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-110">App-V 5.0 supports only packages that are created using App-V 5.0, or packages that have been converted to the App-V 5.0 (**.appv**) format.</span></span>

-   <span data-ttu-id="fc3fb-111">App-v 5.0 SP3에만 해당: app-v 5.0 SP1에서 App-v 서버를 업그레이드 하는 경우 for app [-v 5.0 SP3에 대 한](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) 지침을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-111">App-V 5.0 SP3 only: If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) for instructions.</span></span>

## <span data-ttu-id="fc3fb-112">App-v 4.6을 사용 하 여 동시에 App-v 5.0 클라이언트 실행</span><span class="sxs-lookup"><span data-stu-id="fc3fb-112">Running the App-V 5.0 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="fc3fb-113">App-v 4.6 SP3 클라이언트를 사용 하 여 동일한 컴퓨터에서 앱-V 5.0 클라이언트를 동시에 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-113">You can run the App-V 5.0 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="fc3fb-114">다중 사용자 App-v 클라이언트를 실행 하는 경우 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="fc3fb-115">두 클라이언트가 모두 실행 되 고 있는 경우 App-v 4.6 SP3 패키지를 App-v 5.0 형식으로 변환 하 고 두 패키지를 모두 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-115">Convert an App-V 4.6 SP3 package to the App-V 5.0 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="fc3fb-116">변환 된 App-v 5.0 패키지에서 App-v 4.6 패키지의 파일 형식 연결 및 바로 가기를 사용할 수 있도록 변환 된 패키지에 대 한 마이그레이션 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-116">Define the migration policy for the converted package, which allows the converted App-V 5.0 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="fc3fb-117">지원 되는 공존 시나리오</span><span class="sxs-lookup"><span data-stu-id="fc3fb-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="fc3fb-118">다음 표에서는 지원 되는 앱-V 공존 시나리오를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="fc3fb-119">공존할 수 있는 클라이언트를 실행할 때 주어진 릴리스의 최신 업데이트를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc3fb-120">App-v 4.6 클라이언트 유형</span><span class="sxs-lookup"><span data-stu-id="fc3fb-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="fc3fb-121">App-v 5.0 클라이언트 유형</span><span class="sxs-lookup"><span data-stu-id="fc3fb-121">App-V 5.0 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc3fb-122">App-v 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="fc3fb-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc3fb-123">App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fc3fb-123">App-V 5.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc3fb-124">App-v 4.6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="fc3fb-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="fc3fb-125">App-v 5.0 RDS</span><span class="sxs-lookup"><span data-stu-id="fc3fb-125">App-V 5.0 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fc3fb-126">공존할 클라이언트를 실행 하기 위한 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fc3fb-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="fc3fb-127">공존할 수 있는 클라이언트를 실행 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="fc3fb-128">App-v 5.0 클라이언트를 설치 하기 전에 App-v 4.6 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-128">Install the App-V4.6 client before you install the App-V 5.0 client.</span></span>

-   <span data-ttu-id="fc3fb-129">**App-v** 클라이언트 공존 노드에서 **마이그레이션 모드 설정** 그룹 정책 설정을 사용 하도록 설정 합니다 &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="fc3fb-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="fc3fb-130">Admx 서식 파일 배포를 가져오려면 [MDOP 그룹 정책 (admx) 템플릿을 다운로드 하 고 배포 하는 방법을](https://technet.microsoft.com/library/dn659707.aspx)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-130">To get the deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

### <span data-ttu-id="fc3fb-131">클라이언트 다운로드 및 문서</span><span class="sxs-lookup"><span data-stu-id="fc3fb-131">Client downloads and documentation</span></span>

<span data-ttu-id="fc3fb-132">다음 표에서는 릴리스에 대 한 TechNet 설명서에 대 한 링크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-132">The following table provides link to the TechNet documentation about the releases.</span></span> <span data-ttu-id="fc3fb-133">다른 언급이 없는 한, App-v 클라이언트에 대 한 TechNet 문서는 두 클라이언트에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-133">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fc3fb-134">App-V 버전</span><span class="sxs-lookup"><span data-stu-id="fc3fb-134">App-V version</span></span></th>
<th align="left"><span data-ttu-id="fc3fb-135">TechNet 문서 링크</span><span class="sxs-lookup"><span data-stu-id="fc3fb-135">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fc3fb-136">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="fc3fb-136">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="fc3fb-137">Microsoft Application Virtualization 4.6 SP3 정보</span><span class="sxs-lookup"><span data-stu-id="fc3fb-137">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fc3fb-138">App-v 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="fc3fb-138">App-V 5.0SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-50-sp3.md" data-raw-source="[About Microsoft Application Virtualization 5.0 SP3](about-app-v-50-sp3.md)"><span data-ttu-id="fc3fb-139">Microsoft Application Virtualization 5.0 SP3에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="fc3fb-139">About Microsoft Application Virtualization 5.0 SP3</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fc3fb-140">App-v 5.0 클라이언트 공존을 구성 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-140">For more information about how to configure App-V 5.0 client coexistence, see:</span></span>

-   [<span data-ttu-id="fc3fb-141">앱-V 4.6 및 앱-V 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="fc3fb-141">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

-   [<span data-ttu-id="fc3fb-142">App-v 5.0 공존 및 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="fc3fb-142">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="fc3fb-143">패키지 변환기를 사용 하 여 "이전 버전" 패키지 변환</span><span class="sxs-lookup"><span data-stu-id="fc3fb-143">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="fc3fb-144">App-V 4.6 SP3 또는 이전 버전을 사용 하 여 만든 패키지를 마이그레이션하기 전에 App-v 5.0에 다음 요구 사항을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-144">Before migrating a package, created using App-V4.6SP3 or earlier, to App-V 5.0, review the following requirements:</span></span>

-   <span data-ttu-id="fc3fb-145">패키지를 **appv** 파일 형식으로 변환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-145">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="fc3fb-146">Package Converter는 App-v 4.5 이상을 사용 하 여 만든 패키지의 직접 변환만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-146">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="fc3fb-147">이전 버전을 사용 하 여 만든 패키지에서 패키지 변환기를 사용 하려면 App-v 4.5 이상 버전의 sequencer를 사용 하 여 패키지를 업그레이드 한 다음 패키지 변환을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-147">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="fc3fb-148">패키지 변환기를 사용 하 여 패키지를 변환 하는 방법에 대 한 자세한 내용은 [이전 버전의 app-v에서 만든 패키지를 변환 하는 방법을](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-148">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span></span> <span data-ttu-id="fc3fb-149">파일을 변환한 후에는 App-v 5.0 클라이언트를 실행 하는 대상 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc3fb-149">After you convert the file, you can deploy it to target computers that run the App-V 5.0 client.</span></span>






## <span data-ttu-id="fc3fb-150">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fc3fb-150">Related topics</span></span>


[<span data-ttu-id="fc3fb-151">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="fc3fb-151">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





