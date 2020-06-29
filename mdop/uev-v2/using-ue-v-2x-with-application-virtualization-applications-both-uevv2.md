---
title: UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램
description: UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827273"
---
# <span data-ttu-id="94fb1-103">UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="94fb1-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="94fb1-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1은 App-v 패키지 또는 UE-V 템플릿에 대 한 필수 수정 없이 Microsoft Application Virtualization (App-v) 응용 프로그램을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="94fb1-105">그러나 UE-V 생성기를 가상화 된 App-v 응용 프로그램에서 직접 실행할 수 없기 때문에 추가 단계가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="94fb1-106">대신 응용 프로그램을 로컬로 설치 하 고 템플릿을 생성 한 다음 해당 템플릿을 가상화 된 응용 프로그램에 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="94fb1-107">UE-V를 통해 앱-V 4.5, App-v 4.6 및 App-v 5.0 패키지를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="94fb1-108">App-v 응용 프로그램에 대 한 UE-V 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="94fb1-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="94fb1-109">UE-V를 사용 하 여 응용 프로그램이 로컬로 설치 되는지 여부와 상관 없이 응용 프로그램이 프로그램 이름으로 열리거나, 선택적으로 파일 버전 번호와 제품 버전 번호로 열리는 시점을 모니터 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="94fb1-110">응용 프로그램이 시작 되 면 UE-V 프로세스를 모니터링 하 고 사용자 설정 저장소 경로에 저장 된 설정을 적용 한 다음 응용 프로그램을 정상적으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="94fb1-111">UE-V를 통해 app-v 응용 프로그램을 모니터 하 고, App-v 컴퓨팅 환경 외부의 실제 위치가 아닌 가상화 된 위치로 관련 파일 및 레지스트리 경로를 자동으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="94fb1-112">가상화 된 응용 프로그램에 대 한 설정 동기화를 구현 하려면</span><span class="sxs-lookup"><span data-stu-id="94fb1-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="94fb1-113">UE-V Generator를 실행 하 여 컴퓨터 간에 동기화 할 설정을 포함 하는 로컬로 설치 된 응용 프로그램의 설정을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="94fb1-114">이 프로세스는 설정 위치 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-114">This process creates a settings location template.</span></span> <span data-ttu-id="94fb1-115">Microsoft Office 2010 서식 파일과 같은 기본 제공 서식 파일을 사용 하는 경우에는이 단계를 건너뛰십시오.</span><span class="sxs-lookup"><span data-stu-id="94fb1-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="94fb1-116">UE-V 생성기를 실행 하는 방법에 대 한 자세한 내용은 [사용자 지정 응용 프로그램에 ue-v: x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94fb1-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="94fb1-117">아직 수행 하지 않은 경우 App-v 응용 프로그램 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="94fb1-118">설정 서식 파일 카탈로그의 위치에 서식 파일을 게시 하거나 Windows PowerShell cmdlet을 사용 하 여 수동으로 서식 파일을 설치 `Register-UEVTemplate` 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="94fb1-119">**참고**  새로 만든 서식 파일을 설정 서식 파일 카탈로그에 게시 하는 경우 클라이언트는 동기화 공급자가 설정을 업데이트할 때까지 해당 템플릿을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="94fb1-120">이 프로세스를 수동으로 시작 하려면 **작업 스케줄러**를 열고, **작업 스케줄러 라이브러리**를 확장 하 고, **Microsoft**를 확장 하 고, **ue-v**를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="94fb1-121">결과 창에서 **서식 파일 자동 업데이트**를 마우스 오른쪽 단추로 클릭 한 다음 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="94fb1-122">App-v 패키지를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="94fb1-122">Start the App-V package.</span></span>






## <span data-ttu-id="94fb1-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="94fb1-123">Related topics</span></span>


[<span data-ttu-id="94fb1-124">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="94fb1-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





