---
title: 가상 응용 프로그램 패키지 추가 구성 요소
description: 가상 응용 프로그램 패키지 추가 구성 요소
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815078"
---
# <span data-ttu-id="c5b8d-103">가상 응용 프로그램 패키지 추가 구성 요소</span><span class="sxs-lookup"><span data-stu-id="c5b8d-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="c5b8d-104">App-v Sequencer에서 64 비트 및 32 비트 실행 파일 및/또는 side-by-side 어셈블리에 종속 된 dll (동적 연결 라이브러리) 파일이 포함 된 디렉터리를 검색 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="c5b8d-105">일반적으로 시퀀서는 패키지에 사용 되는 모든 공용 어셈블리에 대해 전용 side-by-side 어셈블리를 만듭니다. 그러나 동일한 디렉터리에 32 비트 및 64 비트 버전의 전용 어셈블리를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="c5b8d-106">Sequencer가 단일 충돌을 감지 하면 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="c5b8d-107">디렉터리에 충돌이 있는지 여부에 관계 없이 전체 패키지에서 기존의 모든 64 비트 전용 어셈블리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="c5b8d-108">전용 side-by-side 어셈블리의 32 비트 버전만 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="c5b8d-109">시퀀서를 실행 하는 컴퓨터와 모든 App-v 클라이언트 컴퓨터에 필요한 모든 64 비트 어셈블리의 공용 버전을 기본적으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="c5b8d-110">필요한 기존 공용 어셈블리를 찾으려면 패키지가 저장 된 디렉터리를 열고 **VFS** 폴더를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="c5b8d-111">예를 들어 패키지 루트가 **Q:\\MyApp**경우 응용 프로그램을 시퀀싱 하는 경우 **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** 을 찾아 기존 공용 어셈블리를 모두 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="c5b8d-112">이러한 파일의 64 비트 버전은 항상 매니페스트 이름의 시작 부분에서 다음 텍스트로 시작 **됩니다.**</span><span class="sxs-lookup"><span data-stu-id="c5b8d-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="c5b8d-113">어셈블리의 정확한 이름과 버전은 연결 된 매니페스트 파일에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="c5b8d-114">다음 링크 중 하나를 사용 하 여 올바른 버전의 필수 구성 요소를 다운로드 하 고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="c5b8d-115">Microsoft Visual c + + 2005 재배포 가능 패키지 (x64)</span><span class="sxs-lookup"><span data-stu-id="c5b8d-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="c5b8d-116">Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x64)</span><span class="sxs-lookup"><span data-stu-id="c5b8d-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="c5b8d-117">Microsoft Visual c + + 2008 재배포 가능 패키지 (x64)</span><span class="sxs-lookup"><span data-stu-id="c5b8d-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="c5b8d-118">Microsoft Visual c + + 2008 SP1 재배포 가능 패키지 (x64)</span><span class="sxs-lookup"><span data-stu-id="c5b8d-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





