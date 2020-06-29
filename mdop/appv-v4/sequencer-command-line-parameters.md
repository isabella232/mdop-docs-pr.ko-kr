---
title: Sequencer 명령줄 매개 변수
description: Sequencer 명령줄 매개 변수
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815553"
---
# <span data-ttu-id="2ccb6-103">Sequencer 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ccb6-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="2ccb6-104">다음 Application Virtualization (App-v) Sequencer 매개 변수를 사용 하 여 응용 프로그램을 시퀀싱 하 고 명령줄을 사용 하 여 기존 가상 응용 프로그램을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="2ccb6-105">명령줄을 사용 하 여 응용 프로그램을 시퀀싱 하는 방법에 대 한 자세한 내용은 [명령줄을 사용 하 여 새 응용 프로그램을 시퀀스 하는 방법](how-to-sequence-a-new-application-by-using-the-command-line.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="2ccb6-106">Sequencer 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ccb6-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="2ccb6-107">/HELP 또는/?</span><span class="sxs-lookup"><span data-stu-id="2ccb6-107">/HELP or /?</span></span>**  
<span data-ttu-id="2ccb6-108">명령줄을 사용 하 여 응용 프로그램을 시퀀싱 하는 데 사용할 수 있는 매개 변수에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="2ccb6-109">/INSTALLPACKAGE 또는/I</span><span class="sxs-lookup"><span data-stu-id="2ccb6-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="2ccb6-110">시퀀싱 될 수 있도록 응용 프로그램을 설치 하는 데 사용 되는 Windows Installer 또는 배치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="2ccb6-111">/INSTALLPATH 또는/P</span><span class="sxs-lookup"><span data-stu-id="2ccb6-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="2ccb6-112">응용 프로그램에 대 한 패키지 루트 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="2ccb6-113">/OUTPUTFILE 또는/O</span><span class="sxs-lookup"><span data-stu-id="2ccb6-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="2ccb6-114">생성 될 SPRJ 파일의 경로와 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="2ccb6-115">/FULLLOAD 또는/F</span><span class="sxs-lookup"><span data-stu-id="2ccb6-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="2ccb6-116">모든 파일을 기본 기능 블록에 포함할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="2ccb6-117">명령줄에 **/FULLLOAD** 매개 변수를 지정 하면 연결 된 모든 응용 프로그램 데이터가 기본 기능 블록에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="2ccb6-118">명령줄에서 **/FULLLOAD** 매개 변수를 지정 하지 않으면 연결 된 응용 프로그램 데이터가 기본 기능 블록에 모두 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="2ccb6-119">/PACKAGENAME 또는/K</span><span class="sxs-lookup"><span data-stu-id="2ccb6-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="2ccb6-120">시퀀싱 된 응용 프로그램에 할당 될 패키지 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="2ccb6-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="2ccb6-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="2ccb6-122">패키지를 클라이언트 컴퓨터로 스트리밍하는 데 사용 되는 SFT 파일 블록 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="2ccb6-123">다음 값 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="2ccb6-124">4KB</span><span class="sxs-lookup"><span data-stu-id="2ccb6-124">4 KB</span></span>

-   <span data-ttu-id="2ccb6-125">16kb</span><span class="sxs-lookup"><span data-stu-id="2ccb6-125">16 KB</span></span>

-   <span data-ttu-id="2ccb6-126">32 KB</span><span class="sxs-lookup"><span data-stu-id="2ccb6-126">32 KB</span></span>

-   <span data-ttu-id="2ccb6-127">64 KB</span><span class="sxs-lookup"><span data-stu-id="2ccb6-127">64 KB</span></span>

<span data-ttu-id="2ccb6-128">블록 크기를 지정할 때 SFT 파일의 크기를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="2ccb6-129">더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="2ccb6-130">블록 크기가 더 많은 파일은 더 많은 네트워크 대역폭을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="2ccb6-131">/C압축</span><span class="sxs-lookup"><span data-stu-id="2ccb6-131">/COMPRESSION</span></span>**  
<span data-ttu-id="2ccb6-132">클라이언트로 스트리밍할 SFT 파일을 압축 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="2ccb6-133">/MSI 또는/M</span><span class="sxs-lookup"><span data-stu-id="2ccb6-133">/MSI or /M</span></span>**  
<span data-ttu-id="2ccb6-134">시퀀싱 된 응용 프로그램에 대 한 Windows Installer를 만들지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="2ccb6-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2ccb6-135">/DEFAULT</span></span>**  
<span data-ttu-id="2ccb6-136">가상 응용 프로그램 패키지를 만들 때 사용 되는 기본 SPRJ 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="2ccb6-137">이 파일은 응용 프로그램을 처음으로 시퀀싱 하는 경우 sprj 템플릿으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="2ccb6-138">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="2ccb6-138">/UPGRADE</span></span>**  
<span data-ttu-id="2ccb6-139">업그레이드 될 SPRJ 파일의 경로와 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="2ccb6-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="2ccb6-140">/DECODEPATH</span></span>**  
<span data-ttu-id="2ccb6-141">시퀀싱 하는 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지와 관련 된 파일이 설치 된 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="2ccb6-142">디렉터리를 지정할 때 다음 형식 중 하나를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="2ccb6-143">/decodepath: Q:</span><span class="sxs-lookup"><span data-stu-id="2ccb6-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="2ccb6-144">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="2ccb6-145">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="2ccb6-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="2ccb6-146">/decodepath: "Q:"</span><span class="sxs-lookup"><span data-stu-id="2ccb6-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="2ccb6-147">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2ccb6-147">Related topics</span></span>


[<span data-ttu-id="2ccb6-148">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2ccb6-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="2ccb6-149">Sequencer 명령줄 오류 코드</span><span class="sxs-lookup"><span data-stu-id="2ccb6-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





