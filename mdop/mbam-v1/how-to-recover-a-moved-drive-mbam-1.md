---
title: 이동된 드라이브를 복구하는 방법
description: 이동된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812929"
---
# <span data-ttu-id="de9f4-103">이동된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="de9f4-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="de9f4-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 이전에 암호화 된 운영 체제 드라이브를 이동 하는 경우 특정 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="de9f4-105">새 컴퓨터에 PIN을 연결 하면 드라이브는 이전 컴퓨터에서 사용한 시작 PIN을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="de9f4-106">시스템은 TPM (신뢰할 수 있는 플랫폼 모듈) 칩에 대 한 변경 때문에 PIN이 유효 하지 않은 것으로 간주 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="de9f4-107">복구 암호를 검색 하려면 이동한 드라이브를 사용 하기 위해 복구 키 ID를 얻어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="de9f4-108">이렇게 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="de9f4-109">이동한 드라이브를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="de9f4-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="de9f4-110">이동한 드라이브를 포함 하는 컴퓨터에서 WinRE (Windows 복구 환경) 모드를 시작 하거나 Microsoft 진단 및 복구 도구 집합 (DaRT)을 사용 하 여 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="de9f4-111">컴퓨터가 WinRE 또는 DaRT로 시작 되 면, MBAM은 이동 된 운영 체제 드라이브를 데이터 드라이브로 간주 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="de9f4-112">이제 MBAM이 드라이브의 복구 암호 ID를 표시 하 고 복구 암호를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="de9f4-113">**참고**  경우에 따라 시작 프로세스 중 **PIN을 잊어버린** 을 클릭 하 여 복구 모드로 전환 하는 경우도 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="de9f4-114">여기에는 복구 키 ID도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="de9f4-115">MBAM 관리 웹 사이트에서 복구 키 ID를 사용 하 여 복구 암호를 검색 하 고 드라이브 잠금을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="de9f4-116">이동한 드라이브가 원래 컴퓨터에서 TPM 칩을 사용 하도록 구성 된 경우 드라이브 잠금을 해제 하 고 시작 프로세스를 완료 한 후에 추가 단계를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="de9f4-117">WinRE 모드에서 명령 프롬프트를 열고 **manage-bde** 도구를 사용 하 여 드라이브의 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="de9f4-118">이 도구의 사용은 원본 TPM 칩 없이도 TPM과 핀 보호를 제거 하는 유일한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="de9f4-119">제거가 완료 되 면 시스템을 정상적으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="de9f4-120">MBAM 에이전트는 계속 해 서 새 컴퓨터의 TPM plus PIN을 사용 하 여 드라이브를 암호화 하도록 정책을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de9f4-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="de9f4-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="de9f4-121">Related topics</span></span>


[<span data-ttu-id="de9f4-122">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="de9f4-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





