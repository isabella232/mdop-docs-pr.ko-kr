---
title: TPM 잠금을 다시 설정하는 방법
description: TPM 잠금을 다시 설정하는 방법
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812921"
---
# <span data-ttu-id="db6a4-103">TPM 잠금을 다시 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="db6a4-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="db6a4-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)의 암호화 된 드라이브 복구 기능에는 데이터 캡처 및 저장소와 TPM (신뢰할 수 있는 플랫폼 모듈)을 관리 하는 데 필요한 도구의 가용성이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="db6a4-105">이 항목에서는 bit \ _admmon \ _tlanextref 관리 웹 사이트에서 중앙 집중화 된 키 복구 데이터 시스템에 액세스 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="db6a4-106">키 복구 데이터 시스템은 컴퓨터 id 및 연결 된 사용자 식별자가 제공 되는 경우 TPM 소유자 암호 파일을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="db6a4-107">사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="db6a4-108">TPM 잠금이 컴퓨터 제조업체의 사양을 기반으로 하기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="db6a4-109">TPM 잠금을 다시 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="db6a4-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="db6a4-110">MBAM 관리 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="db6a4-111">탐색 창에서 **TPM 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="db6a4-112">**TPM 관리** 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="db6a4-113">컴퓨터 및 컴퓨터 이름의 FQDN (정규화 된 도메인 이름)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="db6a4-114">사용자의 Windows 로그온 도메인 및 사용자의 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="db6a4-115">**TPM 소유자 암호 파일 요청 이유** 드롭다운 메뉴에서 미리 정의 된 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="db6a4-116">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="db6a4-117">MBAM은 다음 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="db6a4-118">일치 하는 TPM 소유자 암호 파일을 찾을 수 없는 경우 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="db6a4-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="db6a4-119">제출 된 컴퓨터에 대 한 TPM 소유자 암호 파일</span><span class="sxs-lookup"><span data-stu-id="db6a4-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="db6a4-120">**참고**  고급 헬프 데스크 사용자 인 경우 사용자 도메인 및 사용자 ID 필드가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="db6a4-121">검색 시 소유자 암호가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="db6a4-122">이 암호를 tpm 파일에 저장 하려면 **저장** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="db6a4-123">사용자는 TPM 관리 콘솔을 실행 하 고 tpm **잠금 다시 설정** 옵션을 선택 하 고 tpm 소유자 암호 파일을 제공 하 여 tpm 잠금을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a4-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="db6a4-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="db6a4-124">Related topics</span></span>


[<span data-ttu-id="db6a4-125">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="db6a4-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





