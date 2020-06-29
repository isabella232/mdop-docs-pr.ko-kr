---
title: PowerShell 명령을 사용하여 DaRT 작업을 수행하는 방법
description: PowerShell 명령을 사용하여 DaRT 작업을 수행하는 방법
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822598"
---
# <span data-ttu-id="bd271-103">PowerShell 명령을 사용하여 DaRT 작업을 수행하는 방법</span><span class="sxs-lookup"><span data-stu-id="bd271-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="bd271-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 10은 다음과 같이 나열 된 Windows PowerShell cmdlet 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="bd271-105">관리자는이 PowerShell cmdlet을 사용 하 여 DaRT 복구 이미지 마법사 대신 명령 프롬프트에서 다양 한 DaRT 10 서버 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-105">Administrators can use these PowerShell cmdlets to perform various DaRT 10 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="bd271-106">PowerShell 명령을 사용 하 여 DaRT를 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="bd271-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="bd271-107">여기에서 설명 하는 PowerShell cmdlet을 사용 하 여 DaRT를 관리 하세요.</span><span class="sxs-lookup"><span data-stu-id="bd271-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bd271-108">이름</span><span class="sxs-lookup"><span data-stu-id="bd271-108">Name</span></span></th>
<th align="left"><span data-ttu-id="bd271-109">설명</span><span class="sxs-lookup"><span data-stu-id="bd271-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd271-110">복사-DartImage</span><span class="sxs-lookup"><span data-stu-id="bd271-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd271-111">ISO를 CD, DVD 또는 USB 드라이브로 굽습니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd271-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="bd271-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd271-113">DaRT 이미지가 포함 된 원본 WIM 파일을 ISO 파일로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bd271-114">새로운 DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd271-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd271-115">Windows 이미지에 DaRT 도구 집합을 적용 하는 데 필요한 DaRT 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bd271-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="bd271-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bd271-117">DartConfiguration 개체를 탑재 된 Windows 이미지에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="bd271-118">여기에는 모든 파일, 구성, 패키지 종속성을 추가 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd271-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bd271-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bd271-119">Related topics</span></span>


[<span data-ttu-id="bd271-120">PowerShell을 사용하여 DaRT 10 관리</span><span class="sxs-lookup"><span data-stu-id="bd271-120">Administering DaRT 10 Using PowerShell</span></span>](administering-dart-10-using-powershell.md)

 

 





