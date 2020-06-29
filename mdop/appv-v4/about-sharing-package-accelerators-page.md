---
title: 패키지 가속기 공유 페이지 정보
description: 패키지 가속기 공유 페이지 정보
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819993"
---
# <span data-ttu-id="1944f-103">패키지 가속기 공유 페이지 정보</span><span class="sxs-lookup"><span data-stu-id="1944f-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="1944f-104">다음 정보는 패키지 가속기를 공유 하는 방법에 대 한 모범 사례 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="1944f-105">패키지 가속기 파일을 공유 하려는 경우 컴퓨터 이름, 사용자 계정 정보, 변형에 포함 된 응용 프로그램에 대 한 정보 등의 정보가 패키지 가속기 파일에 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="1944f-106">가상 응용 프로그램 패키지와 연결 된 설정 또는 구성 파일을 검토 하 여 응용 프로그램에 개인 정보가 포함 되지 않도록 해야 합니다. 이 페이지에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="1944f-107">**사용자 이름**.</span><span class="sxs-lookup"><span data-stu-id="1944f-107">**Username**.</span></span> <span data-ttu-id="1944f-108">Microsoft App-v Sequencer를 실행 하는 컴퓨터에 로그온 하는 경우 기본 제공 **관리자** 계정과 같은 일반 사용자 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="1944f-109">기존 사용자 이름을 기반으로 하는 계정은 사용해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="1944f-110">**컴퓨터 이름**입니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-110">**Computer Name**.</span></span> <span data-ttu-id="1944f-111">Sequencer를 실행 하는 컴퓨터의 식별 되지 않는 일반 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="1944f-112">**서버 URL**입니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-112">**Server URL**.</span></span> <span data-ttu-id="1944f-113">App-v Sequencer 콘솔의 **배포** 탭에서 서버 URL 구성 정보에 대 한 기본 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="1944f-114">**응용 프로그램**.</span><span class="sxs-lookup"><span data-stu-id="1944f-114">**Applications**.</span></span> <span data-ttu-id="1944f-115">패키지 가속기를 만들 때 Sequencer를 실행 하는 컴퓨터에 설치 된 응용 프로그램 목록을 공유 하지 않으려는 경우 **appv\_manifest.xml** 파일을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="1944f-116">이 파일은 가상 응용 프로그램 패키지의 패키지 루트 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1944f-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="1944f-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1944f-117">Related topics</span></span>


[<span data-ttu-id="1944f-118">패키지 가속기 만들기 마법사(App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="1944f-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="1944f-119">App-V 패키지 가속기(App-V 4.6 SP1) 정보</span><span class="sxs-lookup"><span data-stu-id="1944f-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





