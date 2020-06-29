---
title: 이동된 드라이브를 복구하는 방법
description: 이동된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825063"
---
# <span data-ttu-id="ad651-103">이동된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad651-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="ad651-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 암호화 된 운영 체제 드라이브를 이동 하는 경우 TPM (신뢰할 수 있는 플랫폼 모듈) 칩에 대 한 변경 때문에 드라이브가 이전 컴퓨터에서 사용한 PIN을 수락 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="ad651-105">이동 된 드라이브를 사용 하려면 복구 키 ID를 가져와서 복구 암호를 검색 하는 방법이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="ad651-106">이동한 드라이브를 복구 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="ad651-107">이동한 드라이브를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="ad651-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="ad651-108">이동한 드라이브를 포함 하는 컴퓨터에서 WinRE (Windows 복구 환경) 모드에서 컴퓨터를 시작 하거나 Microsoft 진단 및 복구 도구 집합 (DaRT)을 사용 하 여 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="ad651-109">컴퓨터가 WinRE 또는 DaRT로 시작 되 면 Microsoft BitLocker 관리 및 모니터링에서 이동 된 운영 체제 드라이브를 데이터 드라이브로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="ad651-110">이제 MBAM이 드라이브의 복구 암호 ID를 표시 하 고 복구 암호를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="ad651-111">**참고**  경우에 따라 시작 프로세스 중 **PIN을 잊어버린** 경우 복구 모드를 입력 하 여 복구 키 ID를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="ad651-112">복구 키 ID를 사용 하 여 복구 암호를 검색 하 고 관리 및 모니터링 웹 사이트에서 드라이브 잠금을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="ad651-113">이동한 드라이브가 원래 컴퓨터에서 TPM 칩을 사용 하도록 구성 된 경우 드라이브 잠금을 해제 하 고 시작 프로세스를 완료 한 후에 추가 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="ad651-114">WinRE 모드에서 명령 프롬프트를 열고 **manage-bde** 도구를 사용 하 여 드라이브의 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="ad651-115">이 도구를 사용 하는 유일한 방법은 TPM plus PIN 보호기를 원래 TPM 칩 없이 제거 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="ad651-116">제거가 완료 되 면 컴퓨터를 정상적으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="ad651-117">MBAM 에이전트는 이제 새 컴퓨터의 TPM plus PIN을 사용 하 여 드라이브를 암호화 하는 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad651-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="ad651-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ad651-118">Related topics</span></span>


[<span data-ttu-id="ad651-119">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="ad651-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





