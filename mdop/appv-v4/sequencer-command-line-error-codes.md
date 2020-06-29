---
title: Sequencer 명령줄 오류 코드
description: Sequencer 명령줄 오류 코드
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815558"
---
# <span data-ttu-id="4c6ac-103">Sequencer 명령줄 오류 코드</span><span class="sxs-lookup"><span data-stu-id="4c6ac-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="4c6ac-104">명령줄을 사용 하 여 응용 프로그램 시퀀싱 관련 오류를 식별 하는 데 도움이 되는 다음 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="4c6ac-105">연결 된 App-v 시퀀서 로그 파일을 보고이 정보를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="4c6ac-106">**참고**  시퀀싱 하는 동안 여러 오류가 발생할 수 있으며,이 경우 표시 되는 오류 코드는 두 오류 코드의 합이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="4c6ac-107">예를 들어 */InstallPath* 및 */OutputFile* 매개 변수가 없는 경우 app-v 시퀀서는 두 오류 코드의 합계인 **96**를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="4c6ac-108">01</span><span class="sxs-lookup"><span data-stu-id="4c6ac-108">01</span></span>  
<span data-ttu-id="4c6ac-109">알 수 없는 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="4c6ac-110">02</span><span class="sxs-lookup"><span data-stu-id="4c6ac-110">02</span></span>  
<span data-ttu-id="4c6ac-111">지정 된 설치 디렉터리 (/INSTALLPACKAGE)가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="4c6ac-112">월</span><span class="sxs-lookup"><span data-stu-id="4c6ac-112">04</span></span>  
<span data-ttu-id="4c6ac-113">지정 된 패키지 루트 디렉터리 (/INSTALLPATH)가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="4c6ac-114">2008</span><span class="sxs-lookup"><span data-stu-id="4c6ac-114">08</span></span>  
<span data-ttu-id="4c6ac-115">지정 된 */OutputFile* 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="4c6ac-116">16</span><span class="sxs-lookup"><span data-stu-id="4c6ac-116">16</span></span>  
<span data-ttu-id="4c6ac-117">설치 디렉터리 (/INSTALLPACKAGE)가 지정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="4c6ac-118">32</span><span class="sxs-lookup"><span data-stu-id="4c6ac-118">32</span></span>  
<span data-ttu-id="4c6ac-119">/INSTALLPATH (package root directory)가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="4c6ac-120">64</span><span class="sxs-lookup"><span data-stu-id="4c6ac-120">64</span></span>  
<span data-ttu-id="4c6ac-121">*/OutputFile* 매개 변수를 지정 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="4c6ac-122">128</span><span class="sxs-lookup"><span data-stu-id="4c6ac-122">128</span></span>  
<span data-ttu-id="4c6ac-123">지정 된 application virtualization 드라이브가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="4c6ac-124">256</span><span class="sxs-lookup"><span data-stu-id="4c6ac-124">256</span></span>  
<span data-ttu-id="4c6ac-125">설치 관리자가 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="4c6ac-126">512</span><span class="sxs-lookup"><span data-stu-id="4c6ac-126">512</span></span>  
<span data-ttu-id="4c6ac-127">응용 프로그램 시퀀싱에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="4c6ac-128">1024</span><span class="sxs-lookup"><span data-stu-id="4c6ac-128">1024</span></span>  
<span data-ttu-id="4c6ac-129">설치 된 바로 가기를 계산 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="4c6ac-130">2048</span><span class="sxs-lookup"><span data-stu-id="4c6ac-130">2048</span></span>  
<span data-ttu-id="4c6ac-131">시퀀싱 된 응용 프로그램 패키지를 저장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="4c6ac-132">4096</span><span class="sxs-lookup"><span data-stu-id="4c6ac-132">4096</span></span>  
<span data-ttu-id="4c6ac-133">지정 된 패키지 이름 (/PACKAGENAME)이 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="4c6ac-134">8192</span><span class="sxs-lookup"><span data-stu-id="4c6ac-134">8192</span></span>  
<span data-ttu-id="4c6ac-135">지정 된 블록 크기 (/BLOCKSIZE)가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="4c6ac-136">16384</span><span class="sxs-lookup"><span data-stu-id="4c6ac-136">16384</span></span>  
<span data-ttu-id="4c6ac-137">지정 된 압축 유형 (/CCOMPRESSION)이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="4c6ac-138">32768</span><span class="sxs-lookup"><span data-stu-id="4c6ac-138">32768</span></span>  
<span data-ttu-id="4c6ac-139">지정 된 프로젝트 경로가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="4c6ac-140">65536</span><span class="sxs-lookup"><span data-stu-id="4c6ac-140">65536</span></span>  
<span data-ttu-id="4c6ac-141">지정 된 업그레이드 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="4c6ac-142">131072</span><span class="sxs-lookup"><span data-stu-id="4c6ac-142">131072</span></span>  
<span data-ttu-id="4c6ac-143">지정 된 업그레이드 프로젝트 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="4c6ac-144">262144</span><span class="sxs-lookup"><span data-stu-id="4c6ac-144">262144</span></span>  
<span data-ttu-id="4c6ac-145">지정 된 디코드 경로 매개 변수가 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="4c6ac-146">525288</span><span class="sxs-lookup"><span data-stu-id="4c6ac-146">525288</span></span>  
<span data-ttu-id="4c6ac-147">패키지 이름이 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="4c6ac-147">The package name is not specified.</span></span>

## <span data-ttu-id="4c6ac-148">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4c6ac-148">Related topics</span></span>


[<span data-ttu-id="4c6ac-149">Application Virtualization Sequencer 참조</span><span class="sxs-lookup"><span data-stu-id="4c6ac-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="4c6ac-150">Sequencer 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4c6ac-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





