---
title: App-V 패키지 가속기(App-V 4.6 SP1) 정보
description: App-V 패키지 가속기(App-V 4.6 SP1) 정보
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820093"
---
# <span data-ttu-id="f8864-103">App-V 패키지 가속기(App-V 4.6 SP1) 정보</span><span class="sxs-lookup"><span data-stu-id="f8864-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="f8864-104">앱-V 패키지 가속기를 사용 하 여 대규모의 복잡 한 응용 프로그램을 자동으로 시퀀싱 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="f8864-105">또한 App-v 패키지 가속기를 적용 하는 경우 가상 응용 프로그램 패키지를 만들기 위해 수동으로 응용 프로그램을 설치 해야 하는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="f8864-106">**참고**  경우에 따라 패키지 가속기를 사용 하기 전에 앱-V 시퀀서를 실행 하는 컴퓨터에 로컬로 응용 프로그램을 설치 하 라는 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="f8864-107">응용 프로그램을 설치 해야 하는 경우 응용 프로그램의 기본 위치에 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="f8864-108">이 설치는 App-v Sequencer에 의해 모니터링 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="f8864-109">App-v 패키지 가속기를 만들 때 패키지 가속기의 작성자가 응용 프로그램을 로컬로 설치할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="f8864-110">App-v Sequencer는 응용 프로그램 설치를 모니터링할 필요 없이 가상 패키지를 만들기 위해 App-v 패키지 가속기 및 관련 설치 미디어에서 필요한 파일을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="f8864-111">**중요**  부인: Microsoft Application Virtualization Sequencer는 패키지 가속기를 만드는 데 사용 하는 소프트웨어 응용 프로그램에 대 한 라이선스 권한을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="f8864-112">이러한 응용 프로그램에 대 한 모든 최종 사용자 사용권 계약을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="f8864-113">소프트웨어 응용 프로그램의 사용권 조항에 따라 Application Virtualization Sequencer를 사용 하 여 패키지 가속기를 만들 수 있도록 하는 것은 사용자의 책임입니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="f8864-114">App-v 패키지 액셀러레이터 키와 프로젝트 템플릿은 서로 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="f8864-115">패키지 가속기는 응용 프로그램에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="f8864-116">프로젝트 서식 파일을 사용 하면 사용자가 조직에 맞게 일반적으로 사용 되는 설정을 저장 하 고 여러 응용 프로그램에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="f8864-117">또한 명령 프롬프트에서 프로젝트 템플릿을 만들 수 있지만, 반면에 앱-V 시퀀서 콘솔을 사용 하 여 패키지 가속기를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="f8864-118">또한 패키지 가속기를 사용 하 여 패키지를 만들고 프로젝트 템플릿을 적용 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="f8864-119">공유 앱-V 패키지 가속기</span><span class="sxs-lookup"><span data-stu-id="f8864-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="f8864-120">이 섹션에서는 패키지 가속기를 공유 하는 방법에 대 한 모범 사례 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="f8864-121">패키지 가속기를 공유 하려는 경우 컴퓨터 이름, 사용자 계정 정보 및 연결 된 응용 프로그램에 대 한 정보 등의 정보가 패키지 가속기에 포함 될 수 있습니다. 다음 목록에서는 패키지 가속기를 만들 때 고려해 야 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="f8864-122">**사용자 이름**입니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-122">**User name**.</span></span> <span data-ttu-id="f8864-123">App-v Sequencer를 실행 하는 컴퓨터에 로그온 하는 경우 컴퓨터/도메인을 관리 하기 위한 기본 제공 **관리자** 계정 등의 일반 사용자 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="f8864-124">기존 사용자 이름을 기반으로 하는 계정은 사용해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="f8864-125">**컴퓨터 이름**입니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-125">**Computer Name**.</span></span> <span data-ttu-id="f8864-126">Sequencer를 실행 하는 컴퓨터에 대해 식별 하지 않는 일반 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="f8864-127">**서버 URL**입니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-127">**Server URL**.</span></span> <span data-ttu-id="f8864-128">Sequencer 콘솔의 **배포** 탭에서 서버 URL 구성 정보에 대 한 기본 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="f8864-129">**응용 프로그램**.</span><span class="sxs-lookup"><span data-stu-id="f8864-129">**Applications**.</span></span> <span data-ttu-id="f8864-130">패키지 가속기를 만들 때 Sequencer를 실행 하는 컴퓨터에 설치 된 응용 프로그램 목록을 공유 하지 않으려는 경우 **appv\_manifest.xml** 파일을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="f8864-131">이 파일은 가상 응용 프로그램 패키지의 패키지 루트 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="f8864-132">또한 가상 응용 프로그램 패키지와 연결 된 설정 또는 구성 파일을 검토 하 여 응용 프로그램에 개인 정보가 포함 되지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="f8864-133">App-v 패키지 가속기 보안 유지</span><span class="sxs-lookup"><span data-stu-id="f8864-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="f8864-134">앱-V 패키지 가속기 및 연결 된 모든 설치 미디어를 네트워크의 안전한 위치에 저장 하면 항상 App-v 패키지 가속기와 설치 파일이 훼손 되거나 손상 되는 것을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="f8864-135">패키지 가속기에는 암호 및 사용자 관련 정보가 포함 될 수도 있으므로, 앱-V 패키지 가속기를 안전한 위치에 저장 해야 하며, 패키지 가속기를 적용 했을 때 게시자를 확인할 수 있도록 패키지 가속기를 만든 후에 디지털 서명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8864-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="f8864-136">디지털 서명에 대 한 자세한 내용은 [일반 기준 보안에 대 한 디지털 서명 방법에 대 한 응용 프로그램 지침](https://go.microsoft.com/fwlink/?LinkId=204705) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="f8864-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="f8864-137">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f8864-137">Related topics</span></span>


[<span data-ttu-id="f8864-138">App-V 패키지 가속기(App-V 4.6 SP1)를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="f8864-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="f8864-139">패키지 가속기를 적용 하 여 가상 응용 프로그램 패키지를 만드는 방법 (App-v 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="f8864-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





