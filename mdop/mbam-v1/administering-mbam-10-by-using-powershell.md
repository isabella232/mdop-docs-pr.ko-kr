---
title: PowerShell을 사용하여 MBAM 1.0 관리
description: PowerShell을 사용하여 MBAM 1.0 관리
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825138"
---
# <span data-ttu-id="9a017-103">PowerShell을 사용하여 MBAM 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="9a017-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="9a017-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음과 같이 나열 된 Windows PowerShell cmdlet 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="9a017-105">관리자는 이러한 PowerShell cmdlet을 사용 하 여 MBAM 관리 웹 사이트 대신 명령 프롬프트에서 다양 한 MBAM 서버 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="9a017-106">PowerShell을 사용 하 여 MBAM을 관리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="9a017-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="9a017-107">여기에 설명 된 PowerShell cmdlet을 사용 하 여 MBAM을 관리 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a017-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a017-108">이름</span><span class="sxs-lookup"><span data-stu-id="9a017-108">Name</span></span></th>
<th align="left"><span data-ttu-id="9a017-109">설명</span><span class="sxs-lookup"><span data-stu-id="9a017-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a017-110">추가-Mbam하드 다시 입력</span><span class="sxs-lookup"><span data-stu-id="9a017-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-111">MBAM 하드웨어 인벤토리에 새 하드웨어 모델을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="9a017-112">이 cmdlet은 하드웨어가 BitLocker 드라이브 암호화에 지원 되는지 또는 지원 되지 않는 경우에도 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a017-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="9a017-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-114">사용자가 컴퓨터 또는 암호화 된 드라이브의 잠금을 해제할 수 있는 MBAM 키를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a017-115">Get-Mbam하드 다시 입력</span><span class="sxs-lookup"><span data-stu-id="9a017-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-116">하드웨어 모델이 BitLocker 드라이브 암호화와 호환 되는지 또는 호환 되지 않는지 여부를 나타내는 데이터를 포함 하는 마스터 하드웨어 인벤토리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a017-117">Get-Mbamtpmo<c13> Erpassword</span><span class="sxs-lookup"><span data-stu-id="9a017-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-118">사용자가 TPM (신뢰할 수 있는 플랫폼 모듈) 액세스를 관리 하는 데 사용할 TPM 소유자 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="9a017-119">TPM이 파일을 잠그고 해당 PIN을 더 이상 허용 하지 않는 사용자에 게 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a017-120">설치-Mbam</span><span class="sxs-lookup"><span data-stu-id="9a017-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-121">고급 그룹 정책, 암호화, 키 복구, 준수 보고 도구를 제공 하는 MBAM 기능을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a017-122">제거-Mbam하드 다시 입력</span><span class="sxs-lookup"><span data-stu-id="9a017-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-123">하드웨어 인벤토리에서 하드웨어 모델을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a017-124">설정-Mbam하드 다시 입력</span><span class="sxs-lookup"><span data-stu-id="9a017-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-125">하드웨어 모델이 BitLocker 암호화를 수행할 수 있는지 여부를 지정 하기 위해 마스터 하드웨어 인벤토리를 관리할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a017-126">제거-Mbam</span><span class="sxs-lookup"><span data-stu-id="9a017-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a017-127">고급 정책, 암호화, 키 복구, 준수 보고 도구를 제공 하는 이전에 설치 된 MBAM 기능을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a017-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9a017-128">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9a017-128">Related topics</span></span>


[<span data-ttu-id="9a017-129">MBAM 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="9a017-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





