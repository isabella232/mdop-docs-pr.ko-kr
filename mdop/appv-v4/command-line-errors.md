---
title: 명령줄 오류
description: 명령줄 오류
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819408"
---
# <span data-ttu-id="54de3-103">명령줄 오류</span><span class="sxs-lookup"><span data-stu-id="54de3-103">Command-Line Errors</span></span>


<span data-ttu-id="54de3-104">다음 오류 목록을 사용 하 여 명령줄 시퀀싱이 제대로 작동 하지 않는 이유를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="54de3-105">시퀀서 로그 파일을 보고 이러한 오류를 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="54de3-106">**참고**  시퀀싱 하는 동안 두 개 이상의 오류가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="54de3-107">또한, 표시 되는 오류 코드는 두 오류 코드의 합계 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="54de3-108">예를 들어 */InstallPath* 및 */OutputFile* 매개 변수가 없는 경우 Microsoft System Center Application 가상화 시퀀서는 두 오류 코드의 합계인 96을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="54de3-109">01</span><span class="sxs-lookup"><span data-stu-id="54de3-109">01</span></span>  
<span data-ttu-id="54de3-110">알 수 없는 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="54de3-111">02</span><span class="sxs-lookup"><span data-stu-id="54de3-111">02</span></span>  
<span data-ttu-id="54de3-112">지정 된/INSTALLPACKAGE (지정 된 설치 디렉터리)가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="54de3-113">월</span><span class="sxs-lookup"><span data-stu-id="54de3-113">04</span></span>  
<span data-ttu-id="54de3-114">지정 된 패키지 루트 디렉터리 (/INSTALLPATH)가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="54de3-115">2008</span><span class="sxs-lookup"><span data-stu-id="54de3-115">08</span></span>  
<span data-ttu-id="54de3-116">지정 된 */OutputFile* 매개 변수가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="54de3-117">16</span><span class="sxs-lookup"><span data-stu-id="54de3-117">16</span></span>  
<span data-ttu-id="54de3-118">설치 디렉터리 (/INSTALLPACKAGE)가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="54de3-119">32</span><span class="sxs-lookup"><span data-stu-id="54de3-119">32</span></span>  
<span data-ttu-id="54de3-120">/INSTALLPATH (package root directory)가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="54de3-121">64</span><span class="sxs-lookup"><span data-stu-id="54de3-121">64</span></span>  
<span data-ttu-id="54de3-122">*/OutputFile* 매개 변수를 지정 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="54de3-123">128</span><span class="sxs-lookup"><span data-stu-id="54de3-123">128</span></span>  
<span data-ttu-id="54de3-124">지정 된 application virtualization 드라이브가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="54de3-125">256</span><span class="sxs-lookup"><span data-stu-id="54de3-125">256</span></span>  
<span data-ttu-id="54de3-126">설치 관리자가 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="54de3-127">512</span><span class="sxs-lookup"><span data-stu-id="54de3-127">512</span></span>  
<span data-ttu-id="54de3-128">응용 프로그램 시퀀싱에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="54de3-129">1024</span><span class="sxs-lookup"><span data-stu-id="54de3-129">1024</span></span>  
<span data-ttu-id="54de3-130">설치 된 바로 가기를 계산 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="54de3-131">2048</span><span class="sxs-lookup"><span data-stu-id="54de3-131">2048</span></span>  
<span data-ttu-id="54de3-132">시퀀싱 된 응용 프로그램 패키지를 저장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="54de3-133">4096</span><span class="sxs-lookup"><span data-stu-id="54de3-133">4096</span></span>  
<span data-ttu-id="54de3-134">지정 된 패키지 이름 (/PACKAGENAME)이 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="54de3-135">8192</span><span class="sxs-lookup"><span data-stu-id="54de3-135">8192</span></span>  
<span data-ttu-id="54de3-136">지정 된 블록 크기 (/BLOCKSIZE <em> ) </em> 가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="54de3-137">16384</span><span class="sxs-lookup"><span data-stu-id="54de3-137">16384</span></span>  
<span data-ttu-id="54de3-138">지정 된 압축 유형 (/CCOMPRESSION)이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="54de3-139">32768</span><span class="sxs-lookup"><span data-stu-id="54de3-139">32768</span></span>  
<span data-ttu-id="54de3-140">지정 된 프로젝트 경로가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="54de3-141">65536</span><span class="sxs-lookup"><span data-stu-id="54de3-141">65536</span></span>  
<span data-ttu-id="54de3-142">지정 된 업그레이드 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="54de3-143">131072</span><span class="sxs-lookup"><span data-stu-id="54de3-143">131072</span></span>  
<span data-ttu-id="54de3-144">지정 된 업그레이드 프로젝트 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="54de3-145">262144</span><span class="sxs-lookup"><span data-stu-id="54de3-145">262144</span></span>  
<span data-ttu-id="54de3-146">지정 된 디코드 경로 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="54de3-147">525288</span><span class="sxs-lookup"><span data-stu-id="54de3-147">525288</span></span>  
<span data-ttu-id="54de3-148">패키지 이름이 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="54de3-148">The package name was not specified.</span></span>

## <span data-ttu-id="54de3-149">관련 항목</span><span class="sxs-lookup"><span data-stu-id="54de3-149">Related topics</span></span>


[<span data-ttu-id="54de3-150">Sequencer 명령줄 사용 정보</span><span class="sxs-lookup"><span data-stu-id="54de3-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="54de3-151">명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="54de3-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





