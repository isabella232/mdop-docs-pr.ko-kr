---
title: Windows PowerShell을 사용하여 MBAM 2.5 관리
description: Windows PowerShell을 사용하여 MBAM 2.5 관리
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812737"
---
# <span data-ttu-id="49326-103">Windows PowerShell을 사용하여 MBAM 2.5 관리</span><span class="sxs-lookup"><span data-stu-id="49326-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="49326-104">이 항목에서는 사용자가 잠겨 있는 컴퓨터 또는 드라이브 복구와 관련 된 Microsoft BitLocker 관리 및 모니터링 (MBAM) 용 Windows PowerShell cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="49326-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="49326-105">MBAM 서버 기능을 구성 하는 데 사용 하는 cmdlet의 경우 [Windows PowerShell을 사용 하 여 mbam 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49326-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="49326-106">MBAM으로 관리 되는 컴퓨터 또는 드라이브를 복구 하기 위한 cmdlet</span><span class="sxs-lookup"><span data-stu-id="49326-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="49326-107">다음 Windows PowerShell cmdlet을 사용 하 여 MBAM으로 관리 되는 컴퓨터 또는 드라이브를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="49326-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="49326-108">이름</span><span class="sxs-lookup"><span data-stu-id="49326-108">Name</span></span></th>
<th align="left"><span data-ttu-id="49326-109">설명</span><span class="sxs-lookup"><span data-stu-id="49326-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49326-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="49326-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="49326-111">사용자가 컴퓨터 또는 암호화 된 드라이브의 잠금을 해제할 수 있는 MBAM 복구 키를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="49326-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="49326-112">Get-Mbamtpmo Erpassword</span><span class="sxs-lookup"><span data-stu-id="49326-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="49326-113">Tpm에서 tpm (신뢰할 수 있는 플랫폼 모듈)을 잠그고 해당 사용자의 PIN을 더 이상 허용 하지 않는 경우 잠금을 해제 하는 데 사용할 수 있는 TPM 소유자 암호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="49326-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="49326-114">MBAM cmdlet 도움말</span><span class="sxs-lookup"><span data-stu-id="49326-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="49326-115">MBAM cmdlet에 대 한 Windows PowerShell 도움말은 다음 형식으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49326-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="49326-116">Windows PowerShell 도움말 형식</span><span class="sxs-lookup"><span data-stu-id="49326-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="49326-117">추가 정보</span><span class="sxs-lookup"><span data-stu-id="49326-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49326-118">Windows PowerShell 명령 프롬프트에서 <strong> get-help </strong> &lt; <em> cmdlet을 입력 합니다.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="49326-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="49326-119">최신 Windows PowerShell cmdlet을 업로드 하려면 <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Windows powershell을 사용 하 여 MBAM 2.5 서버 기능을 구성 하는 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="49326-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="49326-120">웹 페이지로 TechNet에서</span><span class="sxs-lookup"><span data-stu-id="49326-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49326-121">다운로드 센터에서 Word .docx 파일로</span><span class="sxs-lookup"><span data-stu-id="49326-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="49326-122">.Pdf 파일로 다운로드 센터에서</span><span class="sxs-lookup"><span data-stu-id="49326-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="49326-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="49326-123">Related topics</span></span>


[<span data-ttu-id="49326-124">MBAM 2.5 기능 관리</span><span class="sxs-lookup"><span data-stu-id="49326-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="49326-125">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="49326-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="49326-126">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="49326-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="49326-127">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="49326-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="49326-128">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="49326-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





