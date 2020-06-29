---
title: 하드웨어 호환성을 관리하는 방법
description: 하드웨어 호환성을 관리하는 방법
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812985"
---
# <span data-ttu-id="f351d-103">하드웨어 호환성을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="f351d-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="f351d-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 하드웨어 호환성 검사 허용 그룹 정책을 배포한 후 클라이언트 컴퓨터의 제조업체와 모델에 대 한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="f351d-105">이 정책을 구성 하는 경우 mbam 에이전트는 MBAM 클라이언트가 클라이언트 컴퓨터에 배포 될 때 MBAM 서버에 대 한 정보를 보고 하 고 사용자에 게 모델을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="f351d-106">하드웨어 호환성 기능은 조직이 TPM (신뢰할 수 있는 플랫폼 모듈) 칩을 지원 하지 않는 이전 컴퓨터 하드웨어 또는 컴퓨터를 사용할 때 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="f351d-107">이러한 경우 하드웨어 호환성 기능을 사용 하 여 BitLocker 암호화가이를 지 원하는 컴퓨터 모델에만 적용 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="f351d-108">조직의 모든 컴퓨터에서 BitLocker를 지 원하는 경우 하드웨어 호환성 기능을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="f351d-109">**참고**  기본적으로 MBAM 하드웨어 호환성 기능은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="f351d-110">이 기능을 사용 하려면 설치 하는 동안 **관리 및 모니터링 서버** 기능 아래에서 **하드웨어 호환성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="f351d-111">하드웨어 호환성을 설정 하 고 구성 하는 방법에 대 한 자세한 내용은 [MBAM 1.0 서버 인프라 배포](deploying-the-mbam-10-server-infrastructure.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f351d-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="f351d-112">하드웨어 호환성 기능은 다음과 같은 방식으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="f351d-113">MBAM 클라이언트 에이전트는 제조업체, 모델, BIOS maker, BIOS 버전, TPM maker, TPM 버전과 같은 기본 컴퓨터 정보를 검색 한 다음이 정보를 MBAM 서버에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="f351d-114">MBAM 서버는 클라이언트 컴퓨터의 목록을 생성 하 여 BitLocker를 지원 하거나 지원할 수 없는 것을 구분 하는 데 사용할 수 있도록 하는 모델을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="f351d-115">엔터프라이즈에 배포 된 MBAM 클라이언트 에이전트는 새 컴퓨터를 모두 사용 하 여이 목록을 자동으로 업데이트 하 고 **알 수 없는**상태로 검색 된 모델을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="f351d-116">그런 다음 관리자는 MBAM 관리 웹 사이트를 사용 하 여 목록 항목을 변경 하 여 특정 컴퓨터와 모델을 **호환** 되거나 호환 **되지 않는**상태로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="f351d-117">MBAM 클라이언트 에이전트에서 드라이브 암호화를 시작 하기 전에 에이전트는 먼저 실행 중인 하드웨어의 BitLocker 암호화 호환성을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="f351d-118">하드웨어가 호환 되는 것으로 표시 되 면 BitLocker 암호화 프로세스가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="f351d-119">또한 MBAM은 컴퓨터의 하드웨어 호환성 상태를 하루에 한 번 다시 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="f351d-120">하드웨어가 호환 되지 않는 것으로 표시 되는 경우 에이전트는 이벤트를 기록 하 고 규정 준수 보고의 일부로 "하드웨어 제외" 상태를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="f351d-121">에이전트는 7 일 마다 상태가 "호환"으로 변경 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="f351d-122">하드웨어가 알 수 없는 것으로 표시 되 면, BitLocker 암호화 프로세스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="f351d-123">MBAM 클라이언트 에이전트는 컴퓨터의 하드웨어 호환성 상태를 하루에 한 번 다시 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="f351d-124">**경고가**  MBAM 클라이언트 에이전트가 BitLocker 드라이브 암호화를 지원 하지 않는 컴퓨터를 암호화 하려고 하면 컴퓨터가 손상 될 가능성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="f351d-125">조직에서 BitLocker를 지원 하지 않는 구형 하드웨어를 보유 하 고 있는 경우 하드웨어 호환성 기능이 올바르게 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="f351d-126">하드웨어 호환성을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="f351d-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="f351d-127">웹 브라우저를 열고 Microsoft BitLocker 관리 및 모니터링 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="f351d-128">왼쪽 메뉴 모음에서 **하드웨어** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="f351d-129">오른쪽 창에서 **고급 검색**을 클릭 한 다음 필터링을 사용 하 여 **기능** 상태가 **"알 수 없음"** 인 모든 컴퓨터 모델의 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="f351d-130">검색 조건과 일치 하는 컴퓨터 모델 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="f351d-131">관리자가이 페이지에서 새 컴퓨터 종류를 추가, 편집 또는 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="f351d-132">각 알 수 없는 하드웨어 구성을 검토 하 여 구성이 **호환** 되는지 또는 **호환 되지 않는**것으로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="f351d-133">하나 이상의 행을 선택한 다음, 선택한 컴퓨터 모델에 대해 필요에 따라 **호환성** 설정 또는 **호환 되지 않는** 설정을 클릭 하 여 BitLocker 호환성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="f351d-134">**호환**으로 설정 되 면 BitLocker는 지원 되는 모델과 일치 하는 컴퓨터에 드라이브 암호화 정책을 적용 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="f351d-135">**호환 되지 않는**것으로 설정 된 경우 BitLocker는 해당 컴퓨터에 드라이브 암호화 정책을 적용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="f351d-136">**참고**  컴퓨터 모델을 호환으로 설정한 후에는 MBAM 클라이언트가 해당 하드웨어 모델과 일치 하는 컴퓨터에서 BitLocker 암호화를 시작 하는 데 24 시간 이상 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="f351d-137">관리자는 하드웨어 호환성 목록을 정기적으로 모니터링 하 여 MBAM 에이전트에서 검색 된 새 모델을 검토 한 다음 호환성 설정을 적절 하거나 호환 **되지 않는** **호환** 으로 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f351d-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="f351d-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f351d-138">Related topics</span></span>


[<span data-ttu-id="f351d-139">MBAM 1.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="f351d-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





