---
title: 클라이언트 설치 명령줄 참조
description: 클라이언트 설치 명령줄 참조
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826728"
---
# <span data-ttu-id="86c04-103">클라이언트 설치 명령줄 참조</span><span class="sxs-lookup"><span data-stu-id="86c04-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="86c04-104">명령줄에서 MED-V를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="86c04-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="86c04-105">명령줄에서 다음 표에 설명 된 선택적 매개 변수를 모두 사용한 다음에 MED-V .msi 패키지를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="86c04-106">MED-V 패키지는 *MED-V\_x.msi*호출 되며 여기서 *x* 는 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="86c04-107">예를 들어 *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="86c04-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86c04-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="86c04-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="86c04-109">값</span><span class="sxs-lookup"><span data-stu-id="86c04-109">Value</span></span></th>
<th align="left"><span data-ttu-id="86c04-110">설명</span><span class="sxs-lookup"><span data-stu-id="86c04-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-111">/quiet</span><span class="sxs-lookup"><span data-stu-id="86c04-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="86c04-112">자동 설치</span><span class="sxs-lookup"><span data-stu-id="86c04-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c04-113">&lt;로그 파일의/log full 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="86c04-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-114">로그 파일의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="86c04-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-116">설치 디렉터리의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c04-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="86c04-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-118">가상 컴퓨터 폴더의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="86c04-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="86c04-120">1, 0</span><span class="sxs-lookup"><span data-stu-id="86c04-120">1,0</span></span></strong></p>
<p><span data-ttu-id="86c04-121">기본값: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="86c04-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86c04-122">MED-V 관리 도구를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c04-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="86c04-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="86c04-124">1, 0</span><span class="sxs-lookup"><span data-stu-id="86c04-124">1,0</span></span></strong></p>
<p><span data-ttu-id="86c04-125">기본값: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="86c04-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86c04-126">사용자가 Windows에 로그온 할 때마다 MED-V 클라이언트가 자동으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="86c04-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-128">호스트 이름 또는 IP</span><span class="sxs-lookup"><span data-stu-id="86c04-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c04-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="86c04-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-130">포트</span><span class="sxs-lookup"><span data-stu-id="86c04-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="86c04-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="86c04-132">1, 0</span><span class="sxs-lookup"><span data-stu-id="86c04-132">1,0</span></span></strong></p>
<p><span data-ttu-id="86c04-133"><strong>https </strong> 또는 <strong> http</span><span class="sxs-lookup"><span data-stu-id="86c04-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c04-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="86c04-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="86c04-135">1, 0</span><span class="sxs-lookup"><span data-stu-id="86c04-135">1,0</span></span></strong></p>
<p><span data-ttu-id="86c04-136">기본값: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="86c04-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86c04-137">MED-V 설치가 완료 되 면 MED-V가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86c04-138">참고</span><span class="sxs-lookup"><span data-stu-id="86c04-138">Note</span></span></strong><br/><p><span data-ttu-id="86c04-139">MED-V가 시스템에 설치 되어 있는 경우를 대비 하 여 START_MEDV = 0을 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="86c04-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="86c04-141">1, 0</span><span class="sxs-lookup"><span data-stu-id="86c04-141">1,0</span></span></strong></p>
<p><span data-ttu-id="86c04-142">기본값: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="86c04-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86c04-143">바탕 화면에 MED-V 클라이언트를 시작 하는 바로 가기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c04-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="86c04-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-145">RAM (MB)</span><span class="sxs-lookup"><span data-stu-id="86c04-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c04-146">MED-V를 설치 하는 경우 컴퓨터에 최소 크기의 RAM이 지정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="86c04-147">그렇지 않으면 설치가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c04-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="86c04-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="86c04-149">1, 0</span><span class="sxs-lookup"><span data-stu-id="86c04-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86c04-150">운영 체제 유효성 검사를 생략 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c04-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











