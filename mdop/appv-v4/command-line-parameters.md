---
title: 명령줄 매개 변수
description: 명령줄 매개 변수
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819403"
---
# <span data-ttu-id="0958e-103">명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0958e-103">Command-Line Parameters</span></span>


<span data-ttu-id="0958e-104">다음 응용 프로그램 가상화 시퀀서 매개 변수를 사용 하 여 응용 프로그램을 시퀀싱 하 고 명령 프롬프트에서 시퀀싱 된 응용 프로그램 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="0958e-105">Microsoft Application Virtualization Sequencer 디렉터리에서 **Sftsequencer**를 입력 한 다음 적절 한 매개 변수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="0958e-106">*/Help* 또는 */?*</span><span class="sxs-lookup"><span data-stu-id="0958e-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="0958e-107">명령줄 시퀀싱에 사용할 수 있는 매개 변수 목록을 표시 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="0958e-108">*/INSTALLPACKAGE* 또는 */i*</span><span class="sxs-lookup"><span data-stu-id="0958e-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="0958e-109">시퀀싱 될 응용 프로그램의 배치 파일 또는 설치 관리자를 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="0958e-110">*/INSTALLPATH* 또는 */p*</span><span class="sxs-lookup"><span data-stu-id="0958e-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="0958e-111">패키지 루트 디렉터리를 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="0958e-112">*/OUTPUTFILE* 또는 */o*</span><span class="sxs-lookup"><span data-stu-id="0958e-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="0958e-113">생성 되는 SPRJ 파일의 경로와 파일 이름을 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="0958e-114">**중요**  */OUTPUTFILE* 매개 변수는 업그레이드 하지 않으려는 패키지를 여는 경우에는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="0958e-115">*/FULLLOAD* 또는 */f*</span><span class="sxs-lookup"><span data-stu-id="0958e-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="0958e-116">모든 것을 기본 기능 블록에 넣을지 여부를 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="0958e-117">*/Packagename* 또는 */k*</span><span class="sxs-lookup"><span data-stu-id="0958e-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="0958e-118">시퀀싱 된 응용 프로그램의 패키지 이름을 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="0958e-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="0958e-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="0958e-120">패키지를 클라이언트 컴퓨터로 스트리밍하는 데 사용 되는 SFT 파일 블록 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="0958e-121">다음 값 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="0958e-122">4KB</span><span class="sxs-lookup"><span data-stu-id="0958e-122">4 KB</span></span>

-   <span data-ttu-id="0958e-123">16kb</span><span class="sxs-lookup"><span data-stu-id="0958e-123">16 KB</span></span>

-   <span data-ttu-id="0958e-124">32 KB</span><span class="sxs-lookup"><span data-stu-id="0958e-124">32 KB</span></span>

-   <span data-ttu-id="0958e-125">64 KB</span><span class="sxs-lookup"><span data-stu-id="0958e-125">64 KB</span></span>

<span data-ttu-id="0958e-126">블록 크기를 지정할 때 SFT 파일의 크기를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="0958e-127">더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="0958e-128">블록 크기가 더 많은 파일은 더 많은 네트워크 대역폭을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="0958e-129">/C압축</span><span class="sxs-lookup"><span data-stu-id="0958e-129">/COMPRESSION</span></span>*  
<span data-ttu-id="0958e-130">SFT 파일을 클라이언트로 스트리밍할 때 압축 하는 방법을 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="0958e-131">*/MSI* 또는 */m*</span><span class="sxs-lookup"><span data-stu-id="0958e-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="0958e-132">시퀀싱 된 응용 프로그램에 대 한 Microsoft Windows Installer 패키지 생성을 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="0958e-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0958e-133">/DEFAULT</span></span>*  
<span data-ttu-id="0958e-134">가상 응용 프로그램 패키지를 만들 때 사용 되는 기본 SPRJ 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="0958e-135">이 파일은 응용 프로그램을 처음으로 시퀀싱 하는 경우 sprj 템플릿으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="0958e-136">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="0958e-136">/UPGRADE</span></span>*  
<span data-ttu-id="0958e-137">업그레이드 될 SPRJ 파일의 경로와 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="0958e-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="0958e-138">/DECODEPATH</span></span>*  
<span data-ttu-id="0958e-139">시퀀싱 하는 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지와 관련 된 파일이 설치 된 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="0958e-140">디렉터리를 지정할 때 다음 형식 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0958e-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="0958e-141">/decodepath: Q:</span><span class="sxs-lookup"><span data-stu-id="0958e-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="0958e-142">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="0958e-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="0958e-143">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="0958e-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="0958e-144">/decodepath: "Q:"</span><span class="sxs-lookup"><span data-stu-id="0958e-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="0958e-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0958e-145">Related topics</span></span>


[<span data-ttu-id="0958e-146">Sequencer 명령줄 사용 정보</span><span class="sxs-lookup"><span data-stu-id="0958e-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="0958e-147">명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법</span><span class="sxs-lookup"><span data-stu-id="0958e-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="0958e-148">패키지 열기 명령을 사용하여 패키지를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="0958e-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





