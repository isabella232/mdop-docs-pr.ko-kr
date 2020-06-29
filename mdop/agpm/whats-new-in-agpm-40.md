---
title: AGPM 4.0의 새로운 기능
description: AGPM 4.0의 새로운 기능
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820103"
---
# <span data-ttu-id="2a60e-103">AGPM 4.0의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="2a60e-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="2a60e-104">Microsoft AGPM (고급 그룹 정책 관리) 4.0에는 그룹 정책 개체 (Gpo)를 검색 하 고, 표시 된 Gpo 목록을 필터링 하 고, GPO를 다른 포리스트로 내보내고 가져오고, Windows7 및 Windows Server2008R2를 실행 하는 컴퓨터에 AGPM을 설치할 수 있는 새로운 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="2a60e-105">Gpo 검색 및 필터링</span><span class="sxs-lookup"><span data-stu-id="2a60e-105">Search and filter GPOs</span></span>


<span data-ttu-id="2a60e-106">AGPM 4.0에서 Gpo 목록에서 특정 특성을 검색 하 여 표시 되는 Gpo 목록을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="2a60e-107">예를 들어 특정 이름, 상태 또는 주석을 사용 하 여 Gpo를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="2a60e-108">특정 그룹 정책 관리자 또는 특정 날짜에 의해 마지막으로 변경 된 Gpo를 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="2a60e-109">*Gpo 특성 1: 검색 텍스트 1 gpo 특성 2: 검색 텍스트 2 ...* 를 사용 하 여 복잡 한 검색 문자열을 만들 수 있으며, 여기서는 사용자가 AGPM의 gpo 목록에 있는 gpo 특성이 있는 열 머리글을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="2a60e-110">예를 들어, 체크 인하고 사용자 Editor03에 의해 마지막으로 변경 된 "MyGPO" 텍스트를 포함 하는 모든 Gpo를 검색 하려면 검색 상자에 다음을 입력 합니다. **이름: mygpo state:\*\*\*\*checked in\*\*\*\*변경 된 사람: Editor03**에서 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="2a60e-111">일부 검색은 GPO 이름 또는 사용자 이름의 일부를 입력 하 고 이름에 해당 텍스트를 포함 하는 모든 Gpo 목록을 볼 수 있도록 부분적으로 일치 하는 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="2a60e-112">또한 특정 날짜 또는 날짜 범위에서 변경 된 Gpo를 검색 하기 위해 Windows에서 검색할 때 사용할 수 있는 동일한 특별 용어를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="2a60e-113">예를 들어 **날짜 변경:\*\*\*\*마지막 월** 또는 **변경 날짜:\*\*\*\*thisweek**</span><span class="sxs-lookup"><span data-stu-id="2a60e-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="2a60e-114">다른 포리스트로 Gpo 내보내기 및 가져오기</span><span class="sxs-lookup"><span data-stu-id="2a60e-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="2a60e-115">AGPM 4.0을 사용 하 여 한 포리스트의 도메인에 있는 제어 된 GPO를 두 번째 포리스트의 도메인으로 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="2a60e-116">예를 들어, AGPM을 사용 하 여 한 포리스트의 도메인에서 GPO를 CAB 파일로 내보내고, 해당 CAB 파일을 USB 드라이브로 복사 하 고, 두 번째 포리스트의 도메인에 있는 컴퓨터에 USB 드라이브를 연결 하 고, 두 번째 포리스트의 도메인에 있는 AGPM으로 GPO를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="2a60e-117">GPO를 새 제어 된 GPO로 가져오거나 가져와서 체크 아웃 된 기존 GPO의 설정을 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="2a60e-118">Windows Server 2008 R2 및 Windows 7에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="2a60e-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="2a60e-119">AGPM 4.0는 Windows Server2008R2 및 Windows7를 지원 하지만 여전히 Windows Server2008 및 WindowsVista Vista를 서비스 Pack1 (SP1)와 함께 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="2a60e-120">그러나 혼합 환경에는 다음 표에 표시 된 것 처럼 최신 및 이전 운영 체제를 모두 포함 하는 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2a60e-121">AGPM 서버 4.0이 실행 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="2a60e-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="2a60e-122">AGPM 클라이언트 4.0이 실행 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="2a60e-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="2a60e-123">AGPM 4.0 지원 상태</span><span class="sxs-lookup"><span data-stu-id="2a60e-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2a60e-124">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="2a60e-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-125">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="2a60e-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-126">지원함</span><span class="sxs-lookup"><span data-stu-id="2a60e-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2a60e-127">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="2a60e-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-128">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="2a60e-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-129">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2a60e-130">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="2a60e-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-131">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="2a60e-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-132">지원 안 됨</span><span class="sxs-lookup"><span data-stu-id="2a60e-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2a60e-133">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="2a60e-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-134">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="2a60e-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2a60e-135">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2a60e-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





