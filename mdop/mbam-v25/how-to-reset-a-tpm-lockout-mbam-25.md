---
title: TPM 잠금을 다시 설정하는 방법
description: TPM 잠금을 다시 설정하는 방법
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823323"
---
# <span data-ttu-id="cb8b6-103">TPM 잠금을 다시 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="cb8b6-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="cb8b6-104">이 항목에서는 관리 및 모니터링 웹 사이트 (지원 데스크 라고도 함)를 사용 하 여 TPM 잠금을 다시 설정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="cb8b6-105">최종 사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="cb8b6-106">TPM 잠금이 설정 되기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수는 제조업체 마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="cb8b6-107">관리 및 모니터링 웹 사이트의 **Tpm 관리** 영역에서 컴퓨터 ID 및 연결 된 사용자 식별자를 제공할 때 tpm 소유자 암호 파일을 제공 하는 중앙 집중화 된 키 복구 데이터 시스템에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="cb8b6-108">관리 및 모니터링 웹 사이트의 TPM 관리 영역에 액세스 하려면 MBAM 헬프데스크 사용자 역할 또는 MBAM 고급 헬프 데스크 사용자 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="cb8b6-109">이러한 역할은 관리자가 Active Directory에서 만드는 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="cb8b6-110">이러한 그룹에 임의의 이름을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-110">You can use any name for these groups.</span></span> <span data-ttu-id="cb8b6-111">자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="cb8b6-112">MBAM 및 TPM 소유권에 대 한 자세한 내용은 [mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-tpm)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="cb8b6-113">TPM 잠금을 다시 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="cb8b6-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="cb8b6-114">웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="cb8b6-115">왼쪽 창에서 **Tpm 관리** 를 클릭 하 여 **tpm 관리** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="cb8b6-116">컴퓨터 및 컴퓨터 이름의 정규화 된 도메인 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="cb8b6-117">최종 사용자의 Windows 로그온 도메인 및 사용자 이름을 입력 하 여 TPM 소유자 암호 파일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="cb8b6-118">**참고**  MBAM 헬프데스크 사용자 그룹에 속한 사용자 도메인 및 사용자 ID 필드는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="cb8b6-119">**TPM 소유자 암호 요청 이유** 목록에서 요청의 이유를 선택 하 고 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="cb8b6-120">MBAM 다음 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="cb8b6-121">일치 하는 TPM 소유자 암호 파일을 찾을 수 없는 경우 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="cb8b6-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="cb8b6-122">제출 된 컴퓨터에 대 한 TPM 소유자 암호 파일</span><span class="sxs-lookup"><span data-stu-id="cb8b6-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="cb8b6-123">TPM 소유자 암호를 검색 한 후 소유자 암호가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="cb8b6-124">Tpm 파일에 암호를 저장 하려면 **저장** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="cb8b6-125">**관리 및 모니터링 웹 사이트**의 **tpm 관리** 영역에서 **tpm 잠금 다시 설정** 옵션을 선택 하 고 tpm 소유자 암호 파일을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="cb8b6-126">TPM 잠금이 다시 설정 되 고 최종 사용자의 액세스가 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="cb8b6-127">**중요**  TPM 해시 값 또는 TPM 소유자 암호 파일을 최종 사용자에 게 제공 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="cb8b6-128">TPM 정보는 변경 되지 않으므로 파일을 최종 사용자에 게 제공 하는 것이 보안 위험을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="cb8b6-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cb8b6-129">Related topics</span></span>


[<span data-ttu-id="cb8b6-130">MBAM 2.5를 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="cb8b6-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="cb8b6-131">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="cb8b6-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="cb8b6-132">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="cb8b6-133">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8b6-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





