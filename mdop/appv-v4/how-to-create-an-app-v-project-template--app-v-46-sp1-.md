---
title: App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법
description: App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817648"
---
# <span data-ttu-id="ec2f3-103">App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="ec2f3-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="ec2f3-104">앱-V 프로젝트 템플릿을 사용 하 여 기존 가상 응용 프로그램 패키지와 연결 된 일반적으로 적용 되는 설정을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="ec2f3-105">이러한 설정은 가상 응용 프로그램 패키지를 만드는 프로세스를 간소화 하는 데 도움이 될 수 있는 환경에서 새 가상 응용 프로그램 패키지를 만들 때 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="ec2f3-106">**참고**  새 가상 응용 프로그램 패키지를 만들 때만 App-v 프로젝트 템플릿을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="ec2f3-107">기존 가상 응용 프로그램 패키지에 프로젝트 템플릿을 적용 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="ec2f3-108">App-v 프로젝트 템플릿을 적용 하는 방법에 대 한 자세한 내용은 [App-v 프로젝트 템플릿 적용 방법 (app-v 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="ec2f3-109">App-v 응용 프로그램 가속기는 응용 프로그램에 따라 다르며 앱-v 프로젝트 템플릿은 여러 응용 프로그램에 적용 될 수 있으므로 app-v 프로젝트 템플릿은 앱-v 응용 프로그램 가속기와 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="ec2f3-110">또한 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만들 때는 프로젝트 템플릿을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="ec2f3-111">다음 일반 설정은 App-v 프로젝트 템플릿과 함께 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="ec2f3-112">**고급 모니터링 옵션**</span><span class="sxs-lookup"><span data-stu-id="ec2f3-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="ec2f3-113">모니터링 하는 동안 Microsoft Update를 실행할 수 있도록 설정 하 고 .dll을 다시 기준으로 합니다 **.**</span><span class="sxs-lookup"><span data-stu-id="ec2f3-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="ec2f3-114">**패키지 배포 설정**</span><span class="sxs-lookup"><span data-stu-id="ec2f3-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="ec2f3-115">**프로토콜**, **호스트 이름**, **포트**, **경로**, **운영**체제, **보안 설명자 적용**, **MSI 만들기**, **압축 패키지**를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="ec2f3-116">**일반 옵션**</span><span class="sxs-lookup"><span data-stu-id="ec2f3-116">**General Options**.</span></span> <span data-ttu-id="ec2f3-117">**Microsoft Windows Installer (MSI)** 패키지를 생성 하 고, **이벤트 가상화 허용**, **서비스 가상화 허용**, **패키지 버전을 파일 이름에 추가**하도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="ec2f3-118">**제외 항목**</span><span class="sxs-lookup"><span data-stu-id="ec2f3-118">**Exclusion Items**.</span></span> <span data-ttu-id="ec2f3-119">제외 패턴 목록을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="ec2f3-120">프로젝트 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="ec2f3-120">To create a project template</span></span>**

1.  <span data-ttu-id="ec2f3-121">App-v sequencer를 시작 하려면 app-v sequencer를 실행 하는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="ec2f3-122">가상 응용 프로그램 패키지가 현재 App-v Sequencer에서 열려 있는 경우이 절차의 3 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="ec2f3-123">앱-V 프로젝트 템플릿을 사용 하 여 저장할 설정이 포함 된 기존 가상 응용 프로그램 패키지를 열려면 **파일**  /  **열기** 를 클릭 하 고 **패키지** **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="ec2f3-124">**패키지 선택** 페이지에서 **찾아보기를** 클릭 하 고 열려고 하는 가상 응용 프로그램 패키지를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="ec2f3-125">**편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="ec2f3-126">App-v Sequencer 콘솔에서 **파일**  /  **을 서식 파일로 저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="ec2f3-127">새 서식 파일과 함께 저장 되는 설정을 검토 한 후 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="ec2f3-128">새 App-v 프로젝트 템플릿과 연결 되는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="ec2f3-129">**Save**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-129">Click **Save**.</span></span>

    <span data-ttu-id="ec2f3-130">새 App-v 프로젝트 템플릿은이 절차의 3 단계에서 지정한 디렉터리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec2f3-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="ec2f3-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ec2f3-131">Related topics</span></span>


[<span data-ttu-id="ec2f3-132">Application Virtualization Sequencer(App-V 4.6 SP1)에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="ec2f3-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="ec2f3-133">App-V 프로젝트 템플릿(App-V 4.6 SP1)을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="ec2f3-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





