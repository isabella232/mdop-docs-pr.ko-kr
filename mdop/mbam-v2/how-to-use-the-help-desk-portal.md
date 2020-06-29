---
title: 지원 센터 포털을 사용하는 방법
description: 지원 센터 포털을 사용하는 방법
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826328"
---
# <span data-ttu-id="f6275-103">지원 센터 포털을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="f6275-104">MBAM 관리 및 모니터링 웹 사이트는 지원 센터 포털이 라고도 하며, Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 인프라의 일부로 설치 된 BitLocker 드라이브 암호화에 대 한 관리 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="f6275-105">다음 섹션에서는이 웹 사이트를 사용 하 여 보고서를 검토 하 고, 최종 사용자의 드라이브를 복구 하 고, 최종 사용자의 Tpm을 관리 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="f6275-106">보고</span><span class="sxs-lookup"><span data-stu-id="f6275-106">Reports</span></span>


<span data-ttu-id="f6275-107">MBAM Active Directory 및 클라이언트 컴퓨터에서 정보를 수집 하 여 다양 한 보고서를 실행 하 여 BitLocker 사용 및 준수를 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="f6275-108">관리 및 모니터링 웹 사이트의 **보고서** 섹션을 사용 하 여 엔터프라이즈 준수, 개별 컴퓨터 및 키 복구 작업에 대 한 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="f6275-109">각 보고서에 대 한 설명은 [MBAM 보고서 이해](understanding-mbam-reports-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6275-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="f6275-110">보고서에 액세스 하려면</span><span class="sxs-lookup"><span data-stu-id="f6275-110">To access reports</span></span>**

1.  <span data-ttu-id="f6275-111">웹 브라우저를 열고 MBAM 관리 및 모니터링 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="f6275-112">왼쪽 창에서 **보고서** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="f6275-113">상단 메뉴 모음에서 생성할 보고서 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="f6275-114">보고서를 저장 하려면 보고서 메뉴 모음에서 **내보내기** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="f6275-115">MBAM 보고서를 실행 하는 방법에 대 한 자세한 내용은 [Mbam 보고서를 생성 하는 방법을](how-to-generate-mbam-reports-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6275-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="f6275-116">드라이브 복구</span><span class="sxs-lookup"><span data-stu-id="f6275-116">Drive Recovery</span></span>


<span data-ttu-id="f6275-117">관리 및 모니터링 웹 사이트의 **드라이브 복구** 기능을 통해 특정 관리자 역할 (예: 지원 센터 사용자)이 Mbam 클라이언트에서 수집한 복구 키 데이터에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="f6275-118">이 데이터는 BitLocker가 복구 모드로 전환 될 때 BitLocker로 보호 되는 드라이브에 액세스 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="f6275-119">복구 모드의 드라이브를 복구 하는 방법에 대 한 지침은 [복구 모드에서 드라이브를 복구 하는 방법을](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6275-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="f6275-120">또한 옮겨진 드라이브나 손상 된 드라이브는 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="f6275-121">이동된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="f6275-122">손상된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="f6275-123">BitLocker로 보호 되는 드라이브를 복구 하는 방법에 대 한 자세한 내용은 [MBAM을 사용 하 여 Bitlocker 관리 수행](performing-bitlocker-management-with-mbam-mbam-2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6275-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="f6275-124">TPM 관리</span><span class="sxs-lookup"><span data-stu-id="f6275-124">Manage TPM</span></span>


<span data-ttu-id="f6275-125">관리 및 모니터링 웹 사이트의 TPM 관리 기능은 사용자에 게 MBAM 클라이언트에서 수집한 TPM 데이터에 대 한 특정 관리자 역할 (예: "MBAM 헬프데스크 사용자")을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="f6275-126">TPM 잠금에서 관리자는 관리 및 모니터링 웹 사이트를 사용 하 여 TPM 잠금을 해제 하는 데 필요한 암호 파일을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="f6275-127">Tpm 잠금 후 TPM을 다시 설정 하는 방법에 대 한 지침은 [Tpm 잠금을 다시 설정](how-to-reset-a-tpm-lockout-mbam-2.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6275-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="f6275-128">MBAM 지원 센터 작업</span><span class="sxs-lookup"><span data-stu-id="f6275-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="f6275-129">관리 및 모니터링 웹 사이트는 BitLocker로 보호 되는 하드웨어 관리, 드라이브 복구, 보고서 실행 등의 다양 한 관리 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="f6275-130">&lt;설치 프로세스 중에 사용자 지정할 수 있지만 기본적으로 관리 및 모니터링 웹 사이트의 URL은 Http://*MBAMAdministrationServername*입니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="f6275-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="f6275-131">**참고**  관리 및 모니터링 웹 사이트에서 제공 하는 다양 한 기능에 액세스 하려면 해당 사용자 계정과 연결 된 적절 한 역할이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="f6275-132">사용자 역할을 이해 하는 방법에 대 한 자세한 내용은 [MBAM 관리자 역할을 관리 하는 방법을](how-to-manage-mbam-administrator-roles-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6275-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="f6275-133">다음 링크를 사용 하 여 관리 및 모니터링 웹 사이트를 사용 하 여 수행할 수 있는 작업에 대 한 정보를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f6275-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="f6275-134">TPM 잠금을 다시 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="f6275-135">복구 모드에서 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="f6275-136">이동된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="f6275-137">손상된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="f6275-138">분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6275-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





