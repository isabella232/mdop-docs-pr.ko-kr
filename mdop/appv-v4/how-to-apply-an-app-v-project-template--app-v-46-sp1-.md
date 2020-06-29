---
title: App-V 프로젝트 템플릿(App-V 4.6 SP1)을 적용하는 방법
description: App-V 프로젝트 템플릿(App-V 4.6 SP1)을 적용하는 방법
author: dansimp
ms.assetid: 8ef120ab-8cfb-438c-8136-671167b7bd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b5f04f3f31838bfb13c19eee5f2314c3a3d291f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821373"
---
# <span data-ttu-id="f4421-103">App-V 프로젝트 템플릿(App-V 4.6 SP1)을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="f4421-103">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="f4421-104">앱-V 프로젝트 템플릿을 사용 하 여 기존 가상 응용 프로그램 패키지와 연결 된 일반 설정을 새 가상 응용 프로그램 패키지에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-104">You can use an App-V project template to apply common settings associated with an existing virtual application package to a new virtual application package.</span></span> <span data-ttu-id="f4421-105">앱-V 프로젝트 템플릿을 사용 하면 응용 프로그램 시퀀싱을 시작 하기 전에 일반적인 설정을 구성 하 여 가상 응용 프로그램 패키지를 만드는 프로세스를 간소화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-105">Using App-V project templates can help streamline the process of creating virtual application packages by configuring common settings before you begin sequencing an application.</span></span>

<span data-ttu-id="f4421-106">**참고**  새 가상 응용 프로그램 패키지를 만들 때만 App-v 프로젝트 템플릿을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="f4421-107">기존 가상 응용 프로그램 패키지에 프로젝트 템플릿을 적용 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-107">Applying project templates to existing virtual application packages is not supported.</span></span> <span data-ttu-id="f4421-108">또한 패키지 가속기와 함께 프로젝트 템플릿을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-108">Additionally, you cannot use a project template in conjunction with a Package Accelerator.</span></span>

 

<span data-ttu-id="f4421-109">App-v 프로젝트 템플릿을 만드는 방법에 대 한 자세한 내용은 [App-v 프로젝트 템플릿 만드는 방법 (app-v 4.6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4421-109">For more information about creating App-V project templates, see [How to Create an App-V Project Template (App-V 4.6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="f4421-110">앱-V 프로젝트 서식 파일을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="f4421-110">To apply an App-V project template</span></span>**

1.  <span data-ttu-id="f4421-111">Microsoft application virtualization sequencer를 시작 하려면 app-v Sequencer가 설치 되어 있는 컴퓨터에서 **Start**  /  **모든 프로그램**시작 microsoft application virtualization  /  **Microsoft Application Virtualization**  /  **microsoft application virtualization Sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-111">To start the Microsoft Application Virtualization Sequencer, on the computer on which App-V Sequencer is installed, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="f4421-112">App-v 프로젝트 템플릿을 사용 하 여 새 가상 응용 프로그램 패키지를 만들려면 서식 **파일**  /  **에서 새로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-112">To create a new virtual application package by using an App-V project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="f4421-113">사용할 프로젝트 서식 파일을 선택 하려면 프로젝트 서식 파일이 저장 된 디렉터리로 이동 하 여 프로젝트 템플릿을 선택한 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-113">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

4.  <span data-ttu-id="f4421-114">새 가상 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-114">Create the new virtual application package.</span></span> <span data-ttu-id="f4421-115">지정 된 서식 파일을 사용 하 여 저장 한 설정이 만들려는 새 가상 응용 프로그램 패키지에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4421-115">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span> <span data-ttu-id="f4421-116">새 가상 응용 프로그램 패키지를 만드는 방법에 대 한 자세한 내용은 [시퀀싱 하는 응용 프로그램 유형 (app-v 4.6 SP1)을 확인](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)하 고 적절 한 절차를 선택 하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4421-116">For more information about creating a new virtual application package, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md), and select the appropriate procedure.</span></span>

## <span data-ttu-id="f4421-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f4421-117">Related topics</span></span>


[<span data-ttu-id="f4421-118">Application Virtualization Sequencer(App-V 4.6 SP1)에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="f4421-118">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="f4421-119">App-V 프로젝트 템플릿(App-V 4.6 SP1)을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="f4421-119">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-create-an-app-v-project-template--app-v-46-sp1-.md)

 

 





