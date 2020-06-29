---
title: Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법
description: Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827283"
---
# <span data-ttu-id="7fdd5-103">Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="7fdd5-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="7fdd5-104">모든 MED-V 구성 요소를 windows 7에 설치 하는 것과 마찬가지로 기업 전체에 배포 하는 Windows 7 이미지에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="7fdd5-105">그러면 최종 사용자가 MED-V를 시작 하도록 구성한 **시작** 메뉴 바로 가기를 클릭 하 여 med-v 작업 영역의 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="7fdd5-106">처음으로 설치가 시작 되 고 최종 사용자가 지침에 따라 구성을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="7fdd5-107">다음 섹션에서는 Windows 7 이미지를 사용 하 여 엔터프라이즈 전체에 MED-V 작업 영역을 배포 하는 데 도움이 되는 정보와 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="7fdd5-108">Windows 7 이미지에 MED-V 작업 영역을 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="7fdd5-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="7fdd5-109">Windows 7 표준 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="7fdd5-110">자세한 내용은 [Windows 7의 표준 이미지 빌드: 단계별 가이드](https://go.microsoft.com/fwlink/?LinkId=204843) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="7fdd5-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="7fdd5-111">Windows 7 이미지에서 Windows 가상 PC 및 Windows 가상 PC 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="7fdd5-112">자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="7fdd5-113">MED-V \ _HostAgent \ _Setup 설치 파일을 사용 하 여 MED-V 호스트 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="7fdd5-114">자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="7fdd5-115">**경고가**  MED-V 호스트 에이전트를 설치 하기 전에 Internet Explorer를 닫아야 하며 그렇지 않으면 나중에 URL 리디렉션으로 충돌이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="7fdd5-116">배포 중에 컴퓨터 다시 시작을 지정 하 여이 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="7fdd5-117">MED-V 작업 영역 패키지 파일을 Windows 7 이미지에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="7fdd5-118">Med-v 작업 영역 패키지 파일은 **med-v 작업 영역**설치 관리자, medv 파일, 사용자가 직접 만든 setup.exe 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="7fdd5-119">**중요**  Medv 및 setup.exe 파일은 MED-V 작업 영역 설치 관리자와 같은 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="7fdd5-120">그런 다음 setup.exe를 실행 하 여 MED-V 작업 영역을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="7fdd5-121">**시작** 메뉴에서 med-v 작업 영역 패키지 설치를 열기 위한 바로 가기를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="7fdd5-122">최종 사용자가 필요에 따라 MED-V 설치를 시작할 수 있도록 하는 setup.exe 파일에 대 한 **시작** 메뉴 바로 가기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="7fdd5-123">회사 표준 이미지 배포 프로세스를 사용 하 여 Windows 7 이미지를 MED-V가 필요한 엔터프라이즈의 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="7fdd5-124">최종 사용자가 MED-V 작업 영역에 게시 된 응용 프로그램에 액세스 해야 하는 경우 **시작** 메뉴 바로 가기를 클릭 하 여 med-v 작업 영역을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="7fdd5-125">처음으로 설치를 시작 하 고 MED-V의 구성을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="7fdd5-126">처음 설치를 완료 한 후 최종 사용자는 **시작** 메뉴의 med-v 응용 프로그램에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fdd5-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="7fdd5-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7fdd5-127">Related topics</span></span>


[<span data-ttu-id="7fdd5-128">MED-V 2.0 배포 개요</span><span class="sxs-lookup"><span data-stu-id="7fdd5-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="7fdd5-129">전자 소프트웨어 배포 시스템을 통해 MED-V 작업 영역을 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="7fdd5-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





