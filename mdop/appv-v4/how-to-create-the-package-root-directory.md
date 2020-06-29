---
title: 패키지 루트 디렉터리를 만드는 방법
description: 패키지 루트 디렉터리를 만드는 방법
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817628"
---
# <span data-ttu-id="f0fa8-103">패키지 루트 디렉터리를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="f0fa8-103">How to Create the Package Root Directory</span></span>


<span data-ttu-id="f0fa8-104">패키지 루트 디렉터리는 시퀀싱 된 응용 프로그램의 파일이 설치 된 App-v 시퀀서를 실행 하는 컴퓨터의 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="f0fa8-105">이 디렉터리는 시퀀싱 된 응용 프로그램이 스트리밍되는 컴퓨터에도 사실상 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="f0fa8-106">새 응용 프로그램의 설치를 모니터링 하기 전에 패키지 루트 디렉터리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="f0fa8-107">패키지 루트 디렉터리를 만든 후에는 응용 프로그램 시퀀싱을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="f0fa8-108">새 응용 프로그램을 시퀀싱 하는 방법에 대 한 자세한 내용은 [Sequencer 설치 방법을](how-to-install-the-sequencer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-108">For more information about sequencing a new application, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

**<span data-ttu-id="f0fa8-109">패키지 루트 디렉터리를 만들려면</span><span class="sxs-lookup"><span data-stu-id="f0fa8-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="f0fa8-110">패키지 루트 디렉터리를 만들려면 App-v Sequencer를 실행 하는 컴퓨터에서 Q:\\ 드라이브를 지정 된 네트워크 위치로 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="f0fa8-111">시퀀싱 하는 응용 프로그램을 저장할 충분 한 공간이 지정 된 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="f0fa8-112">새 가상 응용 프로그램에 사용할 수 있는 디렉터리를 만들려면 Q:\\ 드라이브에 폴더를 만들고 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="f0fa8-113">**중요**  패키지 루트 디렉터리에 저장 되는 가상 응용 프로그램 파일에 할당 하는 이름은 8.3 명명 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="f0fa8-114">파일 이름은 8 자 미만 이어야 하며, 파일 이름 확장명은 3 자로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0fa8-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="f0fa8-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f0fa8-115">Related topics</span></span>


[<span data-ttu-id="f0fa8-116">Application Virtualization Sequencer에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="f0fa8-116">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 




