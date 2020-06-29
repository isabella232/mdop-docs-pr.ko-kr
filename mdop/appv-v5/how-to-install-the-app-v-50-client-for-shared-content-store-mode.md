---
title: 공유 콘텐츠 저장소 모드에서 App-V 5.0 Client를 설치하는 방법
description: 공유 콘텐츠 저장소 모드에서 App-V 5.0 Client를 설치하는 방법
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814057"
---
# <span data-ttu-id="6b1a5-103">공유 콘텐츠 저장소 모드에서 App-V 5.0 Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="6b1a5-103">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="6b1a5-104">앱-V 5.0 공유 콘텐츠 저장소 (SCS) 모드를 사용 하도록 Microsoft Application Virtualization (App-v) 5.0 클라이언트를 설치 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 client so that it uses the App-V 5.0 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="6b1a5-105">설치 하려는 컴퓨터에 필수 구성 요소가 모두 설치 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="6b1a5-106">[App-v 5.0 필수 조건](app-v-50-prerequisites.md)에 대해 다음 링크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-106">Use the following link for a [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

<span data-ttu-id="6b1a5-107">**참고**  필요한 경우이 절차를 수행 하기 전에 앱-V 5.0 클라이언트의 기존 버전을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.0 client.</span></span>

 

<span data-ttu-id="6b1a5-108">SCS 모드에 대 한 자세한 내용은 Microsoft App-v 5.0 ()에서 (() [백그라운드에서 공유 콘텐츠 저장소](https://go.microsoft.com/fwlink/?LinkId=316879) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="6b1a5-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="6b1a5-109">SCS 모드에 대 한 App-v 5.0 클라이언트 설치 및 구성</span><span class="sxs-lookup"><span data-stu-id="6b1a5-109">Install and configure the App-V 5.0 client for SCS mode</span></span>**

1.  <span data-ttu-id="6b1a5-110">앱-V 5.0 클라이언트 설치 파일을 설치할 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-110">Copy the App-V 5.0 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="6b1a5-111">명령줄을 열고 설치 파일이 저장 된 디렉터리에서 설치 중인 클라이언트 버전에 따라 다음 옵션 중 하나를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="6b1a5-112">RDS 버전의 App-v 5.0 클라이언트 형식을 설치 하려면 다음을 수행 합니다. **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="6b1a5-112">To install the RDS version of the App-V 5.0 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="6b1a5-113">App-v 5.0 클라이언트 유형의 표준 버전을 설치 하려면: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="6b1a5-113">To install the standard version of the App-V 5.0 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="6b1a5-114">**중요**  자동 설치를 수행 해야 하며 설치에 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="6b1a5-115">설치를 완료 한 후에는 클라이언트를 실행 하는 컴퓨터에 패키지를 배포 하 고 모든 패키지 내용이 네트워크를 통해 스트리밍되 게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="6b1a5-116">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="6b1a5-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6b1a5-117">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6b1a5-118">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="6b1a5-118">Got an App-V issue?</span></span>** <span data-ttu-id="6b1a5-119">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1a5-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6b1a5-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6b1a5-120">Related topics</span></span>


[<span data-ttu-id="6b1a5-121">App-V 5.0 Sequencer 및 Client 배포</span><span class="sxs-lookup"><span data-stu-id="6b1a5-121">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





