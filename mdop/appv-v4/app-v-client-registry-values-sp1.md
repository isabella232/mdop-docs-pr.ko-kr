---
title: App-V Client 레지스트리 값
description: App-V Client 레지스트리 값
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819808"
---
# <span data-ttu-id="6b049-103">App-V Client 레지스트리 값</span><span class="sxs-lookup"><span data-stu-id="6b049-103">App-V Client Registry Values</span></span>


<span data-ttu-id="6b049-104">Microsoft App-v (Application Virtualization) 클라이언트는 레지스트리에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-104">The Microsoft Application Virtualization (App-V) client stores its configuration in the registry.</span></span> <span data-ttu-id="6b049-105">레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="6b049-106">레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="6b049-107">이 항목에서는 모든 App-v (Application Virtualization) 클라이언트 레지스트리 키와 사용에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-107">This topic lists all the Application Virtualization (App-V) client registry keys and explains their uses.</span></span>

**<span data-ttu-id="6b049-108">중요</span><span class="sxs-lookup"><span data-stu-id="6b049-108">Important</span></span>**  
<span data-ttu-id="6b049-109">64 비트 운영 체제를 실행 하는 컴퓨터에서 다음 섹션에 설명 된 키와 값이 HKEY \ _LOCAL \ _MACHINE에 있습니다. \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="6b049-109">On a computer running a 64-bit operating system, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>



## <span data-ttu-id="6b049-110">구성 키</span><span class="sxs-lookup"><span data-stu-id="6b049-110">Configuration Key</span></span>


<span data-ttu-id="6b049-111">다음 표에서는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-111">The following table provides information about the registry values associated with the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-112">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-112">Name</span></span></th>
<th align="left"><span data-ttu-id="6b049-113">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-113">Type</span></span></th>
<th align="left"><span data-ttu-id="6b049-114">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-114">Data (Examples)</span></span></th>
<th align="left"><span data-ttu-id="6b049-115">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-116">ProductName</span><span class="sxs-lookup"><span data-stu-id="6b049-116">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-117">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-117">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-118">Microsoft Application Virtualization 데스크톱 클라이언트</span><span class="sxs-lookup"><span data-stu-id="6b049-118">Microsoft Application Virtualization Desktop Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-119">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-119">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-120">버전</span><span class="sxs-lookup"><span data-stu-id="6b049-120">Version</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-121">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-121">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-122">4.5.0.xxx</span><span class="sxs-lookup"><span data-stu-id="6b049-122">4.5.0.xxx</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-123">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-123">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-124">드라이버</span><span class="sxs-lookup"><span data-stu-id="6b049-124">Drivers</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-125">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-125">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-126">Sftfs.sys</span><span class="sxs-lookup"><span data-stu-id="6b049-126">Sftfs.sys</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-127">이 키 값이 있으면 마지막으로 코어를 시작 했을 때 중지 오류를 일으킨 드라이버의 이름을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-127">If this key value is present, it contains the name of the driver that caused a stop error the last time the core was starting.</span></span> <span data-ttu-id="6b049-128">중지 오류를 해결 한 후에는이 키 값을 삭제 하 여 sftlist를 시작할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-128">After you have fixed the stop error, you must delete this key value so that sftlist can start.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-129">InstallPath</span><span class="sxs-lookup"><span data-stu-id="6b049-129">InstallPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-130">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-130">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-131">기본값 = C:\Program Files\Microsoft 응용 프로그램 가상화 클라이언트</span><span class="sxs-lookup"><span data-stu-id="6b049-131">Default=C:\Program Files\Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-132">클라이언트가 설치 된 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-132">The location where the client is installed.</span></span> <span data-ttu-id="6b049-133">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-133">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-134">LogFileName</span><span class="sxs-lookup"><span data-stu-id="6b049-134">LogFileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-135">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-135">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-136">Default = CSIDL_COMMON_APPDATA \Microsoft\Application 가상화 Client\sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="6b049-136">Default=CSIDL_COMMON_APPDATA\Microsoft\Application Virtualization Client\sftlog.txt</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-137">클라이언트 로그 파일의 경로 및 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-137">The path and name for the client log file.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6b049-138">참고</span><span class="sxs-lookup"><span data-stu-id="6b049-138">Note</span></span></strong><br/><p><span data-ttu-id="6b049-139">앱-V 4.6, SP1 보다 이전 버전을 실행 중이 고 로그 파일 이름 또는 위치를 수정한 경우에는 sftlist 서비스를 다시 시작 해야 변경 내용이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-139">If you are running an earlier version than App-V 4.6, SP1 and you modify the log file name or location, you must restart the sftlist service for the change to take effect.</span></span></p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-140">로그 인 Min심각도</span><span class="sxs-lookup"><span data-stu-id="6b049-140">LogMinSeverity</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-141">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-141">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-142">기본값 = 4, 정보</span><span class="sxs-lookup"><span data-stu-id="6b049-142">Default=4, Informational</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-143">로그에 기록할 메시지를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-143">Controls which messages are written to the log.</span></span> <span data-ttu-id="6b049-144">값은 기록 되는 항목의 임계값을 나타내며, 해당 값 보다 작거나 같은 모든 항목은 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-144">The value indicates a threshold of what is logged—everything less than or equal to that value is logged.</span></span> <span data-ttu-id="6b049-145">예를 들어 0x3 (경고) 값은 경고 (0x3), 오류 (0x2) 및 치명적 오류 (0x1)가 기록 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-145">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="6b049-146">값 범위: 0x0 = 없음, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (기본값), 0x5 = Verbose입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-146">Value Range: 0x0 = None, 0x1 = Critical, 0x2 = Error, 0x3 = Warning, 0x4 = Information (Default), 0x5 = Verbose.</span></span></p>
<p><span data-ttu-id="6b049-147">로그 수준은 Application Virtualization (App-v) 클라이언트 콘솔과 명령 프롬프트에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-147">The log level is configurable from the Application Virtualization (App-V) client console and from the command prompt.</span></span> <span data-ttu-id="6b049-148">명령 프롬프트에서 명령이/verboselog를 sftlist.exe 하면 로그 수준이 verbose로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-148">At a command prompt, the command sftlist.exe /verboselog will increase the log level to verbose.</span></span> <span data-ttu-id="6b049-149">명령줄 세부 정보에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-149">For more information on command-line details see</span></span></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p><span data-ttu-id="6b049-150">.</span><span class="sxs-lookup"><span data-stu-id="6b049-150">.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-151">LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="6b049-151">LogRolloverCount</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-152">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-152">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-153">기본값 = 4</span><span class="sxs-lookup"><span data-stu-id="6b049-153">Default=4</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-154">다시 설정 될 때 보관 되는 로그 파일의 백업 복사본 수를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-154">Defines the number of backup copies of the log file that are kept when it is reset.</span></span> <span data-ttu-id="6b049-155">유효한 범위는 0 – 9999입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-155">The valid range is 0–9999.</span></span> <span data-ttu-id="6b049-156">기본값은 4입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-156">The default is 4.</span></span> <span data-ttu-id="6b049-157">값이 0 이면 복사본이 보존 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-157">A value of 0 means no copies will be kept.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-158">로그 Maxsize</span><span class="sxs-lookup"><span data-stu-id="6b049-158">LogMaxSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-159">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-160">기본값 = 256</span><span class="sxs-lookup"><span data-stu-id="6b049-160">Default=256</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-161">로그 파일이 다시 설정 되기 전에 커질 수 있는 최대 크기를 mb 단위로 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-161">Defines the maximum size in megabytes (MB) that the log file can grow before being reset.</span></span> <span data-ttu-id="6b049-162">기본 크기는 256 MB입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-162">The default size is 256 MB.</span></span> <span data-ttu-id="6b049-163">이 크기에 도달 하면 다음 쓰기 시도 시 로그 재설정이 강제 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-163">When this size is reached, a log reset will be forced on the next write attempt.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-164">SystemEventLogLevel</span><span class="sxs-lookup"><span data-stu-id="6b049-164">SystemEventLogLevel</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-165">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-165">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-166">Default = 0x4 (App-V 4.5)</span><span class="sxs-lookup"><span data-stu-id="6b049-166">Default=0x4 (App-V 4.5)</span></span></p>
<p><span data-ttu-id="6b049-167">기본값 = 0x3 (App-V 4.6)</span><span class="sxs-lookup"><span data-stu-id="6b049-167">Default=0x3 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-168">로그 메시지가 NT 이벤트 로그에 기록 되는 로깅 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-168">Indicates the logging level at which log messages are written to the NT event log.</span></span> <span data-ttu-id="6b049-169">값은 기록 되는 항목의 임계값 (즉, 해당 값과 같거나 작은 모든 항목은 기록 됨)을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-169">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="6b049-170">예를 들어 0x3 (경고) 값은 경고 (0x3), 오류 (0x2) 및 치명적 오류 (0x1)가 기록 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-170">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="6b049-171">값 범위</span><span class="sxs-lookup"><span data-stu-id="6b049-171">Value Range</span></span></p>
<p><span data-ttu-id="6b049-172">0x0 = 없음</span><span class="sxs-lookup"><span data-stu-id="6b049-172">0x0 = None</span></span></p>
<p><span data-ttu-id="6b049-173">0x1 = 중요</span><span class="sxs-lookup"><span data-stu-id="6b049-173">0x1 = Critical</span></span></p>
<p><span data-ttu-id="6b049-174">0x2 = 오류</span><span class="sxs-lookup"><span data-stu-id="6b049-174">0x2 = Error</span></span></p>
<p><span data-ttu-id="6b049-175">0x3 = 경고</span><span class="sxs-lookup"><span data-stu-id="6b049-175">0x3 = Warning</span></span></p>
<p><span data-ttu-id="6b049-176">0x4 = 정보 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b049-176">0x4 = Information (Default)</span></span></p>
<p><span data-ttu-id="6b049-177">0x5 = Verbose</span><span class="sxs-lookup"><span data-stu-id="6b049-177">0x5 = Verbose</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-178">AllowIndependentFileStreaming</span><span class="sxs-lookup"><span data-stu-id="6b049-178">AllowIndependentFileStreaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-179">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-179">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-180">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-180">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-181">클라이언트가 APPLICATIONSOURCEROOT 매개 변수를 사용 하 여 구성 된 방식에 관계 없이 파일에서 스트리밍을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-181">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the APPLICATIONSOURCEROOT parameter.</span></span> <span data-ttu-id="6b049-182">FALSE로 설정 된 경우 OSD HREF 또는 APPLICATIONSOURCEROOT 매개 변수에 파일 경로가 포함 된 경우에도 트랜스포트가 파일에서 스트리밍을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-182">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the APPLICATIONSOURCEROOT parameter contains a file path.</span></span></p>
<p><span data-ttu-id="6b049-183">0x0 = False (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b049-183">0x0=False (default)</span></span></p>
<p><span data-ttu-id="6b049-184">0x1 = True</span><span class="sxs-lookup"><span data-stu-id="6b049-184">0x1=True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-185">ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="6b049-185">ApplicationSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-186">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-186">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-187">rtsps://mainserver:322/prodapps</span><span class="sxs-lookup"><span data-stu-id="6b049-187">rtsps://mainserver:322/prodapps</span></span></p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p><span data-ttu-id="6b049-188">파일://\uncserver\share\prodapps</span><span class="sxs-lookup"><span data-stu-id="6b049-188">file://\uncserver\share\prodapps</span></span></p>
<p><span data-ttu-id="6b049-189">파일://\uncserver\share</span><span class="sxs-lookup"><span data-stu-id="6b049-189">file://\uncserver\share</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-190">관리자 또는 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 토폴로지 관리 체계에 따라 응용 프로그램 로딩을 수행 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-190">Enables an administrator or electronic software distribution (ESD) system to ensure application loading is performed according to the topology management scheme.</span></span> <span data-ttu-id="6b049-191">이 키 값을 사용 하 여 응용 프로그램의 HREF 요소 (예: 원본 위치)에 대 한 OSD CODEBASE를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-191">Use this key value to override the OSD CODEBASE for the HREF element (for example, the source location) for an application.</span></span> <span data-ttu-id="6b049-192">응용 프로그램 원본 루트는 Url 및 UNC (범용 명명 규칙) 경로 형식을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-192">Application Source Root supports URLs and Universal Naming Convention (UNC) path formats.</span></span></p>
<p><span data-ttu-id="6b049-193">URL 경로의 올바른 형식은 프로토콜://servername: [port] [/path] [/], 여기서 port와 path는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-193">The correct format for the URL path is protocol://servername:[port][/path][/], where port and path are optional.</span></span> <span data-ttu-id="6b049-194">포트를 지정 하지 않으면 프로토콜에 대 한 기본 포트가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-194">If a port is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="6b049-195">OSD URL의//server: port 부분만 대체 되는 프로토콜:</span><span class="sxs-lookup"><span data-stu-id="6b049-195">Only the protocol://server:port portion of the OSD URL is replaced.</span></span> </p>
<p><span data-ttu-id="6b049-196">UNC 경로에 대 한 올바른 형식은 \computername. 폴더 [folder] []입니다. 여기서 폴더는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-196">The correct format for the UNC path is \computername\sharefolder[folder][], where folder is optional.</span></span> <span data-ttu-id="6b049-197">컴퓨터 이름은 FQDN (정규화 된 도메인 이름) 또는 IP 주소이 될 수 있으며, sharefolder는 드라이브 문자 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-197">The computer name can be a fully qualified domain name (FQDN) or an IP address, and sharefolder can be a drive letter.</span></span> <span data-ttu-id="6b049-198">OSD 경로의 \computernameatesharefolder 또는 drive letter 부분만 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-198">Only the \computername\sharefolder or drive letter portion of the OSD path is replaced.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-199">OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="6b049-199">OSDSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-200">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-200">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-201">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="6b049-201">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="6b049-202">\computer\ 내용</span><span class="sxs-lookup"><span data-stu-id="6b049-202">\computername\content</span></span></p>
<p><span data-ttu-id="6b049-203">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="6b049-203">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="6b049-204">관리자가 게시 하는 동안 시퀀싱 된 응용 프로그램 패키지에 대 한 OSD 파일 검색의 원본 위치를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-204">Enables an administrator to specify a source location for OSD file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="6b049-205">OSDSourceRoot에 허용 되는 형식에는 UNC 경로 및 Url (http 또는 https)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-205">Acceptable formats for the OSDSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-206">IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="6b049-206">IconSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-207">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-207">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-208">\computername\sharefolder\resource</span><span class="sxs-lookup"><span data-stu-id="6b049-208">\computername\sharefolder\resource</span></span></p>
<p><span data-ttu-id="6b049-209">\computer\ 내용</span><span class="sxs-lookup"><span data-stu-id="6b049-209">\computername\content</span></span></p>
<p><span data-ttu-id="6b049-210">C:\foldername</span><span class="sxs-lookup"><span data-stu-id="6b049-210">C:\foldername</span></span></p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p><span data-ttu-id="6b049-211">관리자가 게시 하는 동안 시퀀싱 된 응용 프로그램 패키지의 아이콘 파일 검색에 대 한 원본 위치를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-211">Enables an administrator to specify a source location for icon file retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="6b049-212">IconSourceRoot에 허용 되는 형식에는 UNC 경로 및 Url (http 또는 https)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-212">Acceptable formats for the IconSourceRoot include UNC paths and URLs (http or https).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-213">AutoLoadTriggers</span><span class="sxs-lookup"><span data-stu-id="6b049-213">AutoLoadTriggers</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-214">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-214">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-215">기본값 = 5</span><span class="sxs-lookup"><span data-stu-id="6b049-215">Default=5</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-216">AutoLoad는 가상화 된 응용 프로그램의 보조 기능 블록을 백그라운드에서 자동으로 클라이언트로 스트리밍할 수 있도록 하는 클라이언트 런타임 정책 구성 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-216">AutoLoad is a client runtime policy configuration parameter that enables the secondary feature block of a virtualized application to be streamed to the client automatically in the background.</span></span> <span data-ttu-id="6b049-217">AutoLoad 트리거는 응용 프로그램의 자동 로드를 시작 하는 이벤트를 나타내기 위한 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-217">The AutoLoad triggers are flags to indicate events that initiate auto-loading of applications.</span></span> <span data-ttu-id="6b049-218">AutoLoad는 백그라운드 스트리밍을 사용 하 여 응용 프로그램을 캐시에 완전히 로드할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-218">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span> <span data-ttu-id="6b049-219">기본 기능 블록이 먼저 로드 되 고, 응용 프로그램과의 사용자 조작 등의 포그라운드 작업을 수행 하기 위해 나머지 기능 블록이 백그라운드에 로드 되 고 최적의 성능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-219">The primary feature block will be loaded first, and the remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take place and provide optimal perceived performance.</span></span></p>
<p><span data-ttu-id="6b049-220">비트 마스크 값:</span><span class="sxs-lookup"><span data-stu-id="6b049-220">Bit mask values:</span></span></p>
<p><span data-ttu-id="6b049-221">(0) Never: 비트가 설정 되어 있지 않으면 (값이 0), 트리거가 설정 되지 않았으므로 자동 로드를 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-221">(0) Never: No bits are set (value is 0), no auto loading will be performed, because there are no triggers set.</span></span></p>
<p><span data-ttu-id="6b049-222">(1) OnLaunch: 로드는 사용자가 응용 프로그램을 시작할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-222">(1) OnLaunch: Loading starts when a user starts an application.</span></span></p>
<p><span data-ttu-id="6b049-223">(2) OnRefresh: 로드는 응용 프로그램을 게시할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-223">(2) OnRefresh: Loading starts when the application is published.</span></span> <span data-ttu-id="6b049-224">이는 게시 새로 고침이 발생 하는 등의 경우와 같이 패키지 레코드가 추가 되거나 업데이트 될 때마다 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-224">This occurs whenever the package record is added or updated—for example, when a publishing refresh occurs.</span></span></p>
<p><span data-ttu-id="6b049-225">(4) OnLogin: 사용자가 로그인 할 때 로드가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-225">(4) OnLogin: Loading starts when a user logs in.</span></span></p>
<p><span data-ttu-id="6b049-226">(5) OnLaunch 및 Onlaunch: Default.</span><span class="sxs-lookup"><span data-stu-id="6b049-226">(5) OnLaunch and OnLogin: Default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-227">AutoLoadTarget</span><span class="sxs-lookup"><span data-stu-id="6b049-227">AutoLoadTarget</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-228">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-229">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-229">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-230">지정 된 AutoLoad 트리거가 발생할 때 자동으로 로드 되는 항목을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-230">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span> <span data-ttu-id="6b049-231">비트 마스크 값:</span><span class="sxs-lookup"><span data-stu-id="6b049-231">Bit mask values:</span></span></p>
<p><span data-ttu-id="6b049-232">(0) 없음: 어떤 트리거가 설정 될 수 있는지에 관계 없이 자동으로 로드 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-232">(0) None: No auto-loading, regardless of what triggers may be set.</span></span></p>
<p><span data-ttu-id="6b049-233">(1) PreviouslyUsed (기본값): AutoLoad trigger를 사용 하는 경우 패키지에서 하나 이상의 응용 프로그램이 이미 사용 된 패키지 (즉, 시작 됨 또는 precached)만 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-233">(1) PreviouslyUsed (default): If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used—that is, started or precached.</span></span></p>
<p><span data-ttu-id="6b049-234">(2) 모두: AutoLoad trigger를 사용 하는 경우 패키지 (패키지 당) 또는 모든 패키지 (클라이언트에 대해 설정)의 모든 응용 프로그램이 시작 된 적이 없는지 여부에 관계 없이 자동으로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-234">(2) All: If any AutoLoad trigger is enabled, all applications in the package (per package) or all packages (set for client) will be automatically loaded, whether or not they have ever been started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-235">RequireAuthorizationIfCached</span><span class="sxs-lookup"><span data-stu-id="6b049-235">RequireAuthorizationIfCached</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-236">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-236">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-237">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-237">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-238">응용 프로그램이 이미 캐시에 있는지 여부에 관계 없이 항상 인증이 필요 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-238">Indicates that authorization is always required, whether or not an application is already in cache.</span></span> <span data-ttu-id="6b049-239">가능한 값:</span><span class="sxs-lookup"><span data-stu-id="6b049-239">Possible values:</span></span></p>
<p><span data-ttu-id="6b049-240">0 = False: 항상 서버 연결을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-240">0=False: Always try to connect to the server.</span></span> <span data-ttu-id="6b049-241">서버에 대 한 연결을 설정할 수 없는 경우에도 클라이언트는 사용자가 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-241">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p>
<p><span data-ttu-id="6b049-242">1 = True (기본값): 응용 프로그램을 시작할 때 항상 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-242">1=True (default): Application always must be authorized at startup.</span></span> <span data-ttu-id="6b049-243">RTSP로 스트리밍된 응용 프로그램의 경우 인증을 위해 사용자 인증 토큰이 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-243">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="6b049-244">파일 기반 응용 프로그램의 경우 파일 Acl은 사용자가 응용 프로그램에 액세스할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-244">For file-based applications, file ACLs control whether a user may access the application.</span></span></p>
<p><span data-ttu-id="6b049-245">변경 내용을 적용 하려면 sftlist 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-245">Restart the sftlist service for the change to take effect.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-246">UserDataDirectory</span><span class="sxs-lookup"><span data-stu-id="6b049-246">UserDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-247">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-247">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-248">APPDATA</span><span class="sxs-lookup"><span data-stu-id="6b049-248">%APPDATA%</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-249">아이콘 캐시와 사용자 설정이 저장 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-249">Location where the icon cache and user settings are stored.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-250">GlobalDataDirectory</span><span class="sxs-lookup"><span data-stu-id="6b049-250">GlobalDataDirectory</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-251">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-251">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-252">C:\Users\Public\Documents</span><span class="sxs-lookup"><span data-stu-id="6b049-252">C:\Users\Public\Documents</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-253">OSD 파일에 대 한 캐시, 아이콘 파일, 바로 가기 정보 및 .ini 파일과 같은 SystemGuard 리소스를 포함 하 여 전역 App-v 데이터에 사용할 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-253">Directory to use for global App-V data, including caches for OSD files, icon files, shortcut information, and SystemGuard resources such as .ini files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-254">AllowCrashes</span><span class="sxs-lookup"><span data-stu-id="6b049-254">AllowCrashes</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-255">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-256">0 또는 1</span><span class="sxs-lookup"><span data-stu-id="6b049-256">0 or 1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-257">Default = 0: 값 0은 클라이언트가 내부 프로그램 예외를 catch 하 여 충돌이 발생할 경우 다른 사용자 응용 프로그램이 복구 하 고 계속할 수 있도록 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-257">Default=0: A value of 0 means that the client tries to catch internal program exceptions so that other user applications can recover and continue when a crash happens.</span></span> <span data-ttu-id="6b049-258">값 1은 클라이언트에서 내부 프로그램 예외가 발생 하 여 디버거에서 캡처할 수 있다는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-258">A value of 1 means that the client allows the internal program exceptions to occur so that they can be captured in a debugger.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-259">CoreInternalTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-259">CoreInternalTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-260">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-260">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-261">60</span><span class="sxs-lookup"><span data-stu-id="6b049-261">60</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-262">코어와 프런트 엔드 간의 내부 IPC 요청에 대 한 제한 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-262">Time-out in seconds for internal IPC requests between core and front-end.</span></span> <span data-ttu-id="6b049-263">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-263">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-264">DefaultSuiteCombineTime</span><span class="sxs-lookup"><span data-stu-id="6b049-264">DefaultSuiteCombineTime</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-265">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-266">1천만</span><span class="sxs-lookup"><span data-stu-id="6b049-266">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-267">이 값을 사용 하 여 프로그램이 종료 되는 시간을 표시 하 고 동일한 도구 모음의 다른 응용 프로그램이 실행 되는 동안에는 오류 메시지가 생성 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-267">This value is used to indicate how soon after being started that a program can shut down and not generate any error messages when another application in the same suite is running.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-268">SerializedSuiteLaunchTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-268">SerializedSuiteLaunchTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-269">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-269">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-270">기본값 = 60000</span><span class="sxs-lookup"><span data-stu-id="6b049-270">Default=60000</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-271">클라이언트가 프로그램을 직렬화 하는 데 걸리는 시간 (밀리초)을 동일한 도구 모음에서 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-271">Defines how long in milliseconds the client will wait as it tries to serialize program starts in the same suite.</span></span> <span data-ttu-id="6b049-272">클라이언트가 시간 초과 되 면 프로그램 시작은 계속 되지만 직렬화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-272">If the client times out, the program start will continue but it will not be serialized.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-273">ScriptTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-273">ScriptTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-274">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-274">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-275">300</span><span class="sxs-lookup"><span data-stu-id="6b049-275">300</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-276">WAIT = TRUE 일 경우 OSD 파일의 스크립트에 대 한 기본 제한 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-276">Default time-out in seconds for scripts in OSD file if WAIT=TRUE.</span></span> <span data-ttu-id="6b049-277">WAIT 대신 TIMEOUT을 사용 하 여 스크립트 단위 시간 제한을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-277">You can specify per-script time-outs with TIMEOUT instead of WAIT.</span></span> <span data-ttu-id="6b049-278">값 0은 기다리지 않음을 의미 하 고 0xFFFFFFFF는 영원히 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-278">A value of 0 means no wait, and 0xFFFFFFFF means wait forever.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-279">LaunchRecordLogPath</span><span class="sxs-lookup"><span data-stu-id="6b049-279">LaunchRecordLogPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-280">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-280">String</span></span> </p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6b049-281">HKLM 또는 HKCU에이 값이 로그 파일에 대 한 유효한 경로를 포함 하는 경우, 프로그램을 시작 하 고, 종료 하 고, 시작 하지 못하거나, 연결이 끊긴 모드를 입력 하거나 종료할 때 Ft트레이가이 로그에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-281">If, under either HKLM or HKCU, this value contains a valid path to a log file, SFTTray will write to this log when programs start, shut down, fail to launch, and enter or exit disconnected mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-282">LaunchRecordMask</span><span class="sxs-lookup"><span data-stu-id="6b049-282">LaunchRecordMask</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-283">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-284">0x1A (26) 시작 오류 및 연결 끊김 모드 항목과 종료 활동을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-284">0x1A (26) log launch errors and disconnected mode entry and exit activity.</span></span></p>
<p><span data-ttu-id="6b049-285">0x1F (31)는 모든 것을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-285">0x1F (31) logs everything.</span></span></p>
<p><span data-ttu-id="6b049-286">0x0 (0)은 아무것도 기록 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-286">0x0 (0) logs nothing.</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-287">다섯 가지 이벤트 (비트 마스크 값) 중에서 어떤 것을 기록 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-287">Specifies which of the five events are logged (bitmask values):</span></span></p>
<p><span data-ttu-id="6b049-288">프로그램이 시작 되는 경우 1</span><span class="sxs-lookup"><span data-stu-id="6b049-288">1 for program starts</span></span></p>
<p><span data-ttu-id="6b049-289">2 시작 실패 오류</span><span class="sxs-lookup"><span data-stu-id="6b049-289">2 for launch failure errors</span></span></p>
<p><span data-ttu-id="6b049-290">시스템 종료 4</span><span class="sxs-lookup"><span data-stu-id="6b049-290">4 for shutdowns</span></span></p>
<p><span data-ttu-id="6b049-291">연결이 끊긴 모드를 시작 하는 방법 8</span><span class="sxs-lookup"><span data-stu-id="6b049-291">8 for entering disconnected mode</span></span></p>
<p><span data-ttu-id="6b049-292">16 연결이 끊긴 모드를 종료 하 고 서버에 다시 연결</span><span class="sxs-lookup"><span data-stu-id="6b049-292">16 for exiting disconnected mode to reconnect to a server</span></span></p>
<p><span data-ttu-id="6b049-293">이러한 숫자의 조합을 추가 하 여 각 메시지를 켭니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-293">Add any combination of those numbers to turn on the respective messages.</span></span> <span data-ttu-id="6b049-294">0x1F가 레지스트리에 없으면 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-294">Defaults to 0x1F if not in registry.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-295">LaunchRecordWriteTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-295">LaunchRecordWriteTimeout</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-296">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-296">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-297">기본값 = 3000</span><span class="sxs-lookup"><span data-stu-id="6b049-297">Default=3000</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-298">다른 프로세스에서 사용 중인 레코드 로그에 쓰려고 할 때 트레이가 대기 하는 시간 (밀리초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-298">Specifies in milliseconds how long the tray will wait when trying to write to the launch record log if another process is using it.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-299">ImportSearchPath</span><span class="sxs-lookup"><span data-stu-id="6b049-299">ImportSearchPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-300">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-300">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-301">d:\files; C:\documents 및 settings\user1\SFTs</span><span class="sxs-lookup"><span data-stu-id="6b049-301">d:\files;C:\documents and settings\user1\SFTs</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-302">디렉터리를 선택 하도록 사용자에 게 요청 하기 전에 이동식 SFT 파일을 검색 하는 최대 5 개 디렉터리의 세미콜론으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-302">A semicolon delimited list of up to five directories to search for portable SFT files before prompting the user to select a directory.</span></span> <span data-ttu-id="6b049-303">경로의 후행 백슬래시는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-303">Trailing backslash in paths is optional.</span></span> <span data-ttu-id="6b049-304">이 값은 기본적으로 제공 되지 않으며 수동으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-304">This value is not present by default and must be set manually.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-305">UserImportPath</span><span class="sxs-lookup"><span data-stu-id="6b049-305">UserImportPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-306">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-306">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-307">D:\SFTs</span><span class="sxs-lookup"><span data-stu-id="6b049-307">D:\SFTs</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="6b049-308">HKCU 에서만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-308">Valid only under HKCU.</span></span> <span data-ttu-id="6b049-309">패키지 가져오기에 대 한 SFT 파일을 찾는 동안 사용자가 찾아본 마지막 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-309">The last location the user browsed to while finding a SFT file for package import.</span></span> <span data-ttu-id="6b049-310">SFT를 성공적으로 찾은 경우 자동으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-310">Set automatically if the SFT is found successfully.</span></span> <span data-ttu-id="6b049-311">이는 SFT 파일을 자동으로 찾는 동안 연속 가져오기에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-311">This is used on successive imports when trying to automatically locate SFT files.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-312">공유 키</span><span class="sxs-lookup"><span data-stu-id="6b049-312">Shared Key</span></span>


<span data-ttu-id="6b049-313">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key는 App-v 구성 요소 간에 공유 되는 값을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-313">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared key controls values that are shared across App-V components.</span></span> <span data-ttu-id="6b049-314">다음 표에서는 공유 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-314">The following table provides information about the registry values associated with the Shared key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-315">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-315">Name</span></span> </th>
<th align="left"><span data-ttu-id="6b049-316">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-316">Type</span></span> </th>
<th align="left"><span data-ttu-id="6b049-317">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-317">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="6b049-318">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-318">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-319">가을 경로</span><span class="sxs-lookup"><span data-stu-id="6b049-319">DumpPath</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-320">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-320">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-321">기본값 = C:</span><span class="sxs-lookup"><span data-stu-id="6b049-321">Default=C:</span></span>\ </p></td>
<td align="left"><p><span data-ttu-id="6b049-322">예외에 대 한 미니 덤프를 생성할 때 덤프 파일을 만들기 위한 기본 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-322">Default path to create dump files when generating a minidump on an exception.</span></span> <span data-ttu-id="6b049-323">기본값은 C:\입니다. 지정 하지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="6b049-323">This defaults to C:\ if not specified.</span></span> <span data-ttu-id="6b049-324">클라이언트 설치 관리자가이 키를 &lt; 앱 가상화 전역 데이터 디렉터리 &gt; \Dumps. 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-324">The Client installer sets this key to the &lt;App Virtualization global data directory&gt;\Dumps.</span></span> <span data-ttu-id="6b049-325">Sequencer 설치 관리자가이 키를 설치 디렉터리로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-325">The Sequencer installer sets this key to the installation directory.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-326">가을 Pathsizelimit</span><span class="sxs-lookup"><span data-stu-id="6b049-326">DumpPathSizeLimit</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-327">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-327">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-328">1000</span><span class="sxs-lookup"><span data-stu-id="6b049-328">1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-329">미니 덤프를 저장 하는 데 사용할 수 있는 최대 디스크 공간 크기 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-329">Specifies the maximum total amount of disk space in megabytes that can be used to store minidumps.</span></span> <span data-ttu-id="6b049-330">기본값 = 1000 MB.</span><span class="sxs-lookup"><span data-stu-id="6b049-330">Default = 1000 MB.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-331">네트워크 키</span><span class="sxs-lookup"><span data-stu-id="6b049-331">Network Key</span></span>


<span data-ttu-id="6b049-332">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key는 다양 한 네트워크 관련 매개 변수를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-332">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network key controls a variety of network-related parameters.</span></span> <span data-ttu-id="6b049-333">이 키는 주로 네트워크 전송 에이전트에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-333">This key is primarily used by the network transport agent.</span></span> <span data-ttu-id="6b049-334">다음 표에서는 네트워크 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-334">The following table provides information about the registry values associated with the Network key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-335">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-335">Name</span></span> </th>
<th align="left"><span data-ttu-id="6b049-336">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-336">Type</span></span> </th>
<th align="left"><span data-ttu-id="6b049-337">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-337">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="6b049-338">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-338">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-339">온라인</span><span class="sxs-lookup"><span data-stu-id="6b049-339">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-340">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-340">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-341">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-341">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-342">오프 라인 모드를 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-342">Enables or disables offline mode.</span></span> <span data-ttu-id="6b049-343">0으로 설정 되 면 클라이언트가 App-v 관리 서버 또는 게시 서버와 통신 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-343">If set to 0, the client will not communicate with App-V Management Servers or publishing servers.</span></span> <span data-ttu-id="6b049-344">연결이 끊긴 작업에서는 클라이언트가 App-v 관리 서버에 연결 되어 있지 않은 경우에도 로드 된 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-344">In disconnected operations, the client can start a loaded application even when it is not connected to an App-V Management Server.</span></span> <span data-ttu-id="6b049-345">오프 라인 모드에서는 클라이언트가 App-v 관리 서버 또는 게시 서버에 연결 하려고 시도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-345">In offline mode, the client does not attempt to connect to an App-V Management Server or publishing server.</span></span> <span data-ttu-id="6b049-346">연결이 끊긴 작업을 오프 라인으로 작업할 수 있도록 허용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-346">You must allow disconnected operations to be able to work offline.</span></span> <span data-ttu-id="6b049-347">기본값은 1 (온라인)으로 설정 되 고, 0은 비활성 (오프 라인)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-347">Default value is 1 enabled (online), and 0 is disabled (offline).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-348">AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="6b049-348">AllowDisconnectedOperation</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-349">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-350">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-350">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-351">연결이 끊긴 작업을 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-351">Enables or disables disconnected operation.</span></span> <span data-ttu-id="6b049-352">기본값은 1로 설정 되 고 0을 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-352">Default value is 1 enabled, and 0 is disabled.</span></span> <span data-ttu-id="6b049-353">연결이 끊긴 작업을 사용 하는 경우 app-v 클라이언트는 App-v 관리 서버에 연결 되어 있지 않은 경우에도 로드 된 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-353">When disconnected operations are enabled, the App-V client can start a loaded application even when it is not connected to an App-V Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-354">FastConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-354">FastConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-355">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-355">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-356">기본값 = 1000</span><span class="sxs-lookup"><span data-stu-id="6b049-356">Default=1000</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-357">이 값은 연결이 끊긴 작업 모드로 전환 되는 시점을 결정 하는 TCP 연결 시간 초과 (밀리초)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-357">This value specifies the TCP connect time-out in milliseconds to determine when to go into disconnected operations mode.</span></span> <span data-ttu-id="6b049-358">이 값을 사용 하 여 기본 ConnectTimeout을 20 초 (App-v connect (네트워크 거래)에 대 한 시간 제한) 또는 시스템의 TCP 시간 제한 (약 25 초)을 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-358">This value can be used to override the default ConnectTimeout of 20 seconds (App-V connect time-out for network transactions) or the system’s TCP time-out of approximately 25 seconds.</span></span> <span data-ttu-id="6b049-359">이렇게 하면 클라이언트가 연결이 끊긴 작업 모드로 빠르게 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-359">This brings the client into disconnected operations mode quickly.</span></span> <span data-ttu-id="6b049-360">다음 연결에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-360">Applied on the next connect.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-361">LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="6b049-361">LimitDisconnectedOperation</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-362">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-362">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-363">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-363">Default=1</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-364">AllowDisconnectedOperation가 1 인 경우에만 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-364">Applicable only if AllowDisconnectedOperation is 1, enabled.</span></span> <span data-ttu-id="6b049-365">이 값은 연결이 끊긴 작업에서 클라이언트가 작동할 수 있는 기간에 대 한 시간 제한이 있는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-365">This value determines whether there will be a time limit for how long the client will be allowed to operate in disconnected operations.</span></span> <span data-ttu-id="6b049-366">1 = 제한 됨.</span><span class="sxs-lookup"><span data-stu-id="6b049-366">1=limited.</span></span> <span data-ttu-id="6b049-367">0 = 무제한.</span><span class="sxs-lookup"><span data-stu-id="6b049-367">0=unlimited.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-368">DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="6b049-368">DOTimeoutMinutes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-369">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-369">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-370">Default = 129600</span><span class="sxs-lookup"><span data-stu-id="6b049-370">Default=129,600</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-371">연결이 끊긴 작업 모드에서 응용 프로그램을 사용할 수 있는 시간 (분)을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-371">Indicates how many minutes an application may be used in disconnected operation mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6b049-372">유효한 값은 1 – 999999 in (1 – 1439998560 분)으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-372">The valid values are 1–999,999 in days expressed in minutes (1–1,439,998,560 minutes).</span></span> <span data-ttu-id="6b049-373">기본값은 90 일 또는 129600 분입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-373">The default value is 90 days or 129,600 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-374">프로토콜</span><span class="sxs-lookup"><span data-stu-id="6b049-374">Protocol</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-375">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-375">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-376">기본값 = 8</span><span class="sxs-lookup"><span data-stu-id="6b049-376">Default=8</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-377">사용할 기본 프로토콜 (TCP vs SSL)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-377">Default protocol to use (TCP vs SSL).</span></span> <span data-ttu-id="6b049-378">옵션 대화 상자에서 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-378">Configure in Options Dialog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-379">ReadTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-379">ReadTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-380">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-380">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-381">명</span><span class="sxs-lookup"><span data-stu-id="6b049-381">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-382">네트워크 거래에 대 한 시간 제한 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-382">Read time-out for network transactions, in seconds.</span></span> <span data-ttu-id="6b049-383">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-383">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-384">WriteTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-384">WriteTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-385">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-386">명</span><span class="sxs-lookup"><span data-stu-id="6b049-386">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-387">네트워크 거래에 대 한 쓰기 시간을 초 단위로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-387">Write time-out for network transactions, in seconds.</span></span> <span data-ttu-id="6b049-388">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-388">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-389">ConnectTimeout</span><span class="sxs-lookup"><span data-stu-id="6b049-389">ConnectTimeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-390">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-390">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-391">명</span><span class="sxs-lookup"><span data-stu-id="6b049-391">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-392">네트워크 거래에 대 한 연결 시간 제한 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-392">Connect time-out for network transactions, in seconds.</span></span> <span data-ttu-id="6b049-393">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-393">Do not modify.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-394">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="6b049-394">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-395">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-395">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-396">3-4</span><span class="sxs-lookup"><span data-stu-id="6b049-396">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-397">삭제 된 세션을 다시 설정 하는 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-397">The number of times to try to reestablish a dropped session.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-398">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="6b049-398">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-399">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-400">~</span><span class="sxs-lookup"><span data-stu-id="6b049-400">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-401">손실 된 세션 다시 시작을 시도 하는 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-401">The number of seconds to wait between tries to reestablish a dropped session.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-402">Http 키</span><span class="sxs-lookup"><span data-stu-id="6b049-402">Http Key</span></span>


<span data-ttu-id="6b049-403">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http 키는 Http 스트림과 관련 된 매개 변수를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-403">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http key controls the parameters that are related to Http streaming.</span></span> <span data-ttu-id="6b049-404">이 키는 주로 네트워크 전송 에이전트에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-404">This key is used primarily by the network transport agent.</span></span> <span data-ttu-id="6b049-405">다음 표에서는 Http 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-405">The following table provides information about the registry values that are associated with the Http key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-406">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-406">Name</span></span> </th>
<th align="left"><span data-ttu-id="6b049-407">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-407">Type</span></span> </th>
<th align="left"><span data-ttu-id="6b049-408">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-408">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="6b049-409">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-409">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-410">LaunchIfNotFound</span><span class="sxs-lookup"><span data-stu-id="6b049-410">LaunchIfNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-411">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-411">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-412">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-412">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-413">Http 서버에 대 한 연결을 설정할 수 있고 패키지 파일이 더 이상 HTTP 서버에 존재 하지 않는 경우 HTTP 스트리밍의 동작을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-413">Controls the behavior of HTTP streaming when a connection to the HTTP server can be established and the package file no longer exists on the HTTP server.</span></span> <span data-ttu-id="6b049-414">값이 없거나 1로 설정 되어 있지 않은 경우 App-v 클라이언트에서 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-414">If the value does not exist or if it is not set to 1, the App-V client does not let you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6b049-415">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-415">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-416">이 값을 1로 설정 하면 App-v 클라이언트를 사용 하 여 이전에 캐시에 로드 한 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-416">If this value is set to 1, the App-V client lets you launch an application that has previously been loaded into cache.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-417">파일 시스템 키</span><span class="sxs-lookup"><span data-stu-id="6b049-417">File System Key</span></span>


<span data-ttu-id="6b049-418">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS 키 아래에 포함 된 값이 App-v의 파일 시스템 매개 변수를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-418">The values that are contained under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS key control the file system parameters for App-V.</span></span> <span data-ttu-id="6b049-419">다음 표에서는 AppFS 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-419">The following table provides information about the registry values associated with the AppFS key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-420">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-420">Name</span></span> </th>
<th align="left"><span data-ttu-id="6b049-421">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-421">Type</span></span> </th>
<th align="left"><span data-ttu-id="6b049-422">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-422">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="6b049-423">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-423">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-424">FileSize</span><span class="sxs-lookup"><span data-stu-id="6b049-424">FileSize</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-425">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-425">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-426">4096</span><span class="sxs-lookup"><span data-stu-id="6b049-426">4096</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-427">파일 시스템 캐시 파일의 최대 크기 (mb)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-427">Maximum size in megabytes of file system cache file.</span></span> <span data-ttu-id="6b049-428">레지스트리에서이 값을 변경 하는 경우 상태를 0으로 설정 하 고 다시 부팅 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-428">If you change this value in the registry, you must set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-429">FileName</span><span class="sxs-lookup"><span data-stu-id="6b049-429">FileName</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-430">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-430">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-431">C:\Users\Public\Documents\SoftGrid Client\sftfsordfd</span><span class="sxs-lookup"><span data-stu-id="6b049-431">C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-432">파일 시스템 캐시 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-432">Location of file system cache file.</span></span> <span data-ttu-id="6b049-433">레지스트리에서이 값을 변경 하는 경우 FileSize을 동일 하 게 유지 하 고 다시 부팅 하거나 상태를 0으로 설정 하 고 다시 부팅 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-433">If you change this value in the registry, you must either leave FileSize the same and reboot or set State to 0 and reboot.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-434">DriveLetter</span><span class="sxs-lookup"><span data-stu-id="6b049-434">DriveLetter</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-435">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-435">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-436">Q:</span><span class="sxs-lookup"><span data-stu-id="6b049-436">Q:</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-437">사용할 수 있는 경우 App-v 파일 시스템이 탑재 될 드라이브</span><span class="sxs-lookup"><span data-stu-id="6b049-437">Drive where App-V file system will be mounted, if it is available.</span></span> <span data-ttu-id="6b049-438">이 값은 수신기 또는 설치 관리자가 설정 하며 파일 시스템에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-438">This value is set either by the listener or the installer, and it is read by the file system.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-439">시</span><span class="sxs-lookup"><span data-stu-id="6b049-439">State</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-440">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-440">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-441">0x100</span><span class="sxs-lookup"><span data-stu-id="6b049-441">0x100</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-442">파일 시스템의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-442">State of file system.</span></span> <span data-ttu-id="6b049-443">0으로 설정 하 고 다시 부팅 하 여 파일 시스템 캐시를 완전히 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-443">Set to 0 and reboot to completely clear the file system cache.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-444">FileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="6b049-444">FileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-445">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-445">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-446">C:\Profiles\Joe\SG</span><span class="sxs-lookup"><span data-stu-id="6b049-446">C:\Profiles\Joe\SG</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-447">Symlinks의 경로 이며 HKCU 아래에서 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-447">Path for symlinks, set under HKCU.</span></span> <span data-ttu-id="6b049-448">수정 안 함 (구성 아래의 데이터 디렉터리를 사용 하 여 변경)</span><span class="sxs-lookup"><span data-stu-id="6b049-448">Do not modify (use data directory under Configuration to change).</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-449">GlobalFileSystemStorage</span><span class="sxs-lookup"><span data-stu-id="6b049-449">GlobalFileSystemStorage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-450">문자열</span><span class="sxs-lookup"><span data-stu-id="6b049-450">String</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-451">C:\Users\Public\Documents\SoftGrid Client\AppFS 저장소</span><span class="sxs-lookup"><span data-stu-id="6b049-451">C:\Users\Public\Documents\SoftGrid Client\AppFS Storage</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-452">전역 파일 시스템 데이터의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-452">Path for global file system data.</span></span> <span data-ttu-id="6b049-453">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-453">Do not modify.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-454">MaxPercentToLockInCache</span><span class="sxs-lookup"><span data-stu-id="6b049-454">MaxPercentToLockInCache</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-455">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-455">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-456">Default = 90</span><span class="sxs-lookup"><span data-stu-id="6b049-456">Default=90</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-457">잠글 수 있는 파일 시스템 캐시 파일의 최대 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-457">Specifies the maximum percentage of the file system cache file that can be locked.</span></span> <span data-ttu-id="6b049-458">수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b049-458">Do not modify.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-459">UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="6b049-459">UnloadLeastRecentlyUsed</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-460">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-460">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-461">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-461">Default=1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-462">파일 시스템 캐시 공간 관리 기능은 LRU (최근에 사용한) 알고리즘을 사용 하며 기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-462">The file system cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="6b049-463">새 패키지에 필요한 공간이 캐시의 사용 가능한 공간을 초과 하는 경우 App-v 클라이언트는이 기능을 사용 하 여 새 패키지를 위한 공간을 만들기 위해 캐시에서 삭제할 수 있는 기존 패키지를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-463">If the space that is required for a new package would exceed the available free space in the cache, the App-V Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="6b049-464">클라이언트가 MinPkgAge 레지스트리 값에 지정 된 값 보다 오래 된 경우 가장 오래 된 마지막으로 액세스 한 날짜를 사용 하 여 패키지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-464">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="6b049-465">값은 0 (사용 안 함) 및 1 (기본값, 사용)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-465">Values are 0 (disabled) and 1 (default, enabled).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-466">MinPackageAge</span><span class="sxs-lookup"><span data-stu-id="6b049-466">MinPackageAge</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-467">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-467">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-468">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-468">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-469">삭제를 위해 패키지를 선택할 수 있는 시간을 결정 하려면이 레지스트리 값을 패키지를 마지막으로 액세스 한 이후 경과 되는 최소 날짜 수와 동일 하 게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-469">To determine when the package can be selected for discard, set this registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="6b049-470">최근에 사용한 패키지는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-470">Packages that have been used more recently are not discarded.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-471">사용 권한 키</span><span class="sxs-lookup"><span data-stu-id="6b049-471">Permissions Key</span></span>


<span data-ttu-id="6b049-472">사용자가 실수 하는 것을 방지 하기 위해 관리자는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions 키를 사용 하 여 관리자가 아닌 사용자의 일부 작업에 대 한 액세스를 제어할 수 있습니다 (예: 사용자가 실수로 프로그램을 언로드하는 것을 방지).</span><span class="sxs-lookup"><span data-stu-id="6b049-472">To help to prevent users from making mistakes, administrators can use the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions key to control access to some actions for non-administrative users—for example, to prevent users from accidentally unloading programs.</span></span> <span data-ttu-id="6b049-473">관리 권한이 있는 사용자는 자신에 게 이러한 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-473">Users with administrative rights can give themselves any of these permissions.</span></span> <span data-ttu-id="6b049-474">RD 세션 호스트 (원격 데스크톱 세션 호스트) 서버 (이전의 터미널 서버) 시스템 등의 공유 시스템에서는 이러한 사용 권한 중 일부는 사용자가 시스템의 모든 사용자가 사용 하는 응용 프로그램을 제어할 수 있도록 허용 하므로 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-474">On shared systems, such as a Remote Desktop Session Host (RD Session Host) server (formerly Terminal Server) system, be careful when granting additional permissions to users because some of these permissions would enable users to control the applications used by all users on the system.</span></span> <span data-ttu-id="6b049-475">이러한 설정의 가능 값은 1 (허용) 및 0 (허용 안 함)입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-475">Possible values for these settings are 1 (allow) and 0 (disallow).</span></span>

<span data-ttu-id="6b049-476">권한 키 설정은 명명 된 작업을 사용 하도록 설정 하는 모든 인터페이스를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-476">The Permissions key settings control all interfaces that enable the named actions.</span></span> <span data-ttu-id="6b049-477">여기에는 옵션 대화 상자, SFTTray, Sfttray이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-477">This includes the Options Dialog, SFTTray, and SFTMime.</span></span> <span data-ttu-id="6b049-478">이러한 설정은 관리자에 게 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-478">These settings do not affect administrators.</span></span> <span data-ttu-id="6b049-479">다음 표에서는 사용 권한 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-479">The following table provides information about the registry values associated with the Permissions key.</span></span>

<span data-ttu-id="6b049-480">이름 형식 데이터 (예제) 설명 ChangeFSDrive</span><span class="sxs-lookup"><span data-stu-id="6b049-480">Name Type Data (Examples) Description ChangeFSDrive</span></span>

<span data-ttu-id="6b049-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-481">DWORD</span></span>

<span data-ttu-id="6b049-482">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-482">Default=0</span></span>

<span data-ttu-id="6b049-483">값 1은 사용자가 파일 시스템 드라이브로 사용할 다른 드라이브 문자를 선택할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-483">A value of 1 allows users to pick a different drive letter to be used as the file system drive.</span></span>

<span data-ttu-id="6b049-484">ChangeCacheSize</span><span class="sxs-lookup"><span data-stu-id="6b049-484">ChangeCacheSize</span></span>

<span data-ttu-id="6b049-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-485">DWORD</span></span>

<span data-ttu-id="6b049-486">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-486">Default=0</span></span>

<span data-ttu-id="6b049-487">값 1은 사용자가 캐시 크기를 변경할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-487">A value of 1 allows users to change the cache size.</span></span>

<span data-ttu-id="6b049-488">ChangeLogSettings</span><span class="sxs-lookup"><span data-stu-id="6b049-488">ChangeLogSettings</span></span>

<span data-ttu-id="6b049-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-489">DWORD</span></span>

<span data-ttu-id="6b049-490">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-490">Default=0</span></span>

<span data-ttu-id="6b049-491">값 1은 사용자가 로그 수준을 수정 하 고, 위치를 변경 하 고, 사용자 인터페이스를 통해 다시 설정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-491">A value of 1 allows users to modify the log level, change its location, and reset it through the user interface.</span></span>

<span data-ttu-id="6b049-492">AddApp</span><span class="sxs-lookup"><span data-stu-id="6b049-492">AddApp</span></span>

<span data-ttu-id="6b049-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-493">DWORD</span></span>

<span data-ttu-id="6b049-494">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-494">Default=0</span></span>

<span data-ttu-id="6b049-495">값 1을 사용 하면 사용자가 응용 프로그램을 명시적으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-495">A value of 1 allows users to add applications explicitly.</span></span> <span data-ttu-id="6b049-496">이는 게시 새로 고침을 통해 추가 되는 응용 프로그램에는 사용자가 아직 추가 되지 않은 응용 프로그램을 시작 (및 암시적으로 추가 하지 않음) 하는 것은 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-496">This does not affect applications that are added through publishing refresh nor does it prevent users from starting (and thereby implicitly adding) applications that have not already been added.</span></span> <span data-ttu-id="6b049-497">값은 0 또는 1입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-497">Values are 0 or 1.</span></span>

<span data-ttu-id="6b049-498">LoadApp</span><span class="sxs-lookup"><span data-stu-id="6b049-498">LoadApp</span></span> 

<span data-ttu-id="6b049-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-499">DWORD</span></span> 

<span data-ttu-id="6b049-500">0</span><span class="sxs-lookup"><span data-stu-id="6b049-500">0</span></span>

<span data-ttu-id="6b049-501">사용자가 응용 프로그램을 로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-501">Does not allow a user to load an application.</span></span> <span data-ttu-id="6b049-502">이것은 RD 세션 호스트의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-502">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="6b049-503">모바일 사용자는 연결 되지 않은 작업 또는 오프 라인 모드에서 응용 프로그램을 사용 하도록 캐시에 완전히 로드 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-503">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="6b049-504">App-v 관리 서버 또는 App-v 스트리밍 서버에서 응용 프로그램을 스트리밍하려면 응용 프로그램을 로드 하려면 서버에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-504">To stream applications from the App-V Management Server or the App-V Streaming Server, you must be connected to a server to load applications.</span></span>

<span data-ttu-id="6b049-505">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-505">1</span></span>

<span data-ttu-id="6b049-506">사용자가 응용 프로그램을 로드할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-506">Allows a user to load an application.</span></span> <span data-ttu-id="6b049-507">Windows 데스크톱의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-507">This is the default for Windows desktops.</span></span> 

<span data-ttu-id="6b049-508">UnloadApp</span><span class="sxs-lookup"><span data-stu-id="6b049-508">UnloadApp</span></span> 

<span data-ttu-id="6b049-509">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-509">DWORD</span></span> 

<span data-ttu-id="6b049-510">0</span><span class="sxs-lookup"><span data-stu-id="6b049-510">0</span></span>

<span data-ttu-id="6b049-511">사용자가 응용 프로그램을 언로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-511">Does not allow a user to unload an application.</span></span> <span data-ttu-id="6b049-512">패키지를 로드 하거나 언로드하면 패키지의 모든 응용 프로그램이 캐시에서 로드 되거나 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-512">When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span>

<span data-ttu-id="6b049-513">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-513">1</span></span>

<span data-ttu-id="6b049-514">사용자가 응용 프로그램을 언로드할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-514">Allows a user to unload an application.</span></span> 

<span data-ttu-id="6b049-515">LockApp</span><span class="sxs-lookup"><span data-stu-id="6b049-515">LockApp</span></span> 

<span data-ttu-id="6b049-516">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-516">DWORD</span></span> 

<span data-ttu-id="6b049-517">0</span><span class="sxs-lookup"><span data-stu-id="6b049-517">0</span></span>

<span data-ttu-id="6b049-518">사용자가 응용 프로그램을 잠그고 잠금을 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-518">Does not allow a user to lock and unlock an application.</span></span> <span data-ttu-id="6b049-519">이것은 RD 세션 호스트의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-519">This is the default for RD Session Hosts.</span></span> <span data-ttu-id="6b049-520">잠긴 응용 프로그램을 캐시에서 제거 하 여 새 응용 프로그램을 위한 공간을 확보할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-520">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="6b049-521">App-v 데스크톱 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 캐시의 클라이언트에서 잠긴 응용 프로그램을 제거 하려면 잠금을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-521">To remove a locked application from the App-V Desktop or Client for Remote Desktop Services (formerly Terminal Services) cache, you must unlock it.</span></span>

<span data-ttu-id="6b049-522">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-522">1</span></span>

<span data-ttu-id="6b049-523">사용자가 응용 프로그램을 잠그고 잠금을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-523">Allows a user to lock and unlock an application.</span></span> <span data-ttu-id="6b049-524">Windows 데스크톱의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-524">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="6b049-525">ManageTypes</span><span class="sxs-lookup"><span data-stu-id="6b049-525">ManageTypes</span></span> 

<span data-ttu-id="6b049-526">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-526">DWORD</span></span> 

<span data-ttu-id="6b049-527">0</span><span class="sxs-lookup"><span data-stu-id="6b049-527">0</span></span>

<span data-ttu-id="6b049-528">사용자가 해당 사용자의 파일 형식 연결을 추가 하거나 편집 하거나 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-528">Does not allow a user to add, edit, or remove file type associations for that User alone.</span></span> <span data-ttu-id="6b049-529">이것은 RD 세션 호스트의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-529">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="6b049-530">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-530">1</span></span>

<span data-ttu-id="6b049-531">사용자가 해당 사용자의 파일 형식 연결을 추가, 편집 및 제거할 수 있습니다 (전역에만 해당).</span><span class="sxs-lookup"><span data-stu-id="6b049-531">Allows a user to add, edit, and remove file type associations for that user only and not globally.</span></span> <span data-ttu-id="6b049-532">Windows 데스크톱의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-532">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="6b049-533">RefreshServer</span><span class="sxs-lookup"><span data-stu-id="6b049-533">RefreshServer</span></span> 

<span data-ttu-id="6b049-534">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-534">DWORD</span></span> 

<span data-ttu-id="6b049-535">0</span><span class="sxs-lookup"><span data-stu-id="6b049-535">0</span></span>

<span data-ttu-id="6b049-536">사용자가 MIME 설정 새로 고침을 트리거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-536">Does not allow a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="6b049-537">이것은 RD 세션 호스트의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-537">This is the default for RD Session Hosts.</span></span> 

<span data-ttu-id="6b049-538">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-538">1</span></span>

<span data-ttu-id="6b049-539">사용자가 MIME 설정 새로 고침을 트리거할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-539">Enables a user to trigger a refresh of MIME settings.</span></span> <span data-ttu-id="6b049-540">Windows 데스크톱의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-540">This is the default for Windows Desktops.</span></span> 

<span data-ttu-id="6b049-541">UpdateOSDFile</span><span class="sxs-lookup"><span data-stu-id="6b049-541">UpdateOSDFile</span></span>

<span data-ttu-id="6b049-542">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-542">DWORD</span></span>

<span data-ttu-id="6b049-543">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-543">Default= 0</span></span>

<span data-ttu-id="6b049-544">값 1은 사용자가 수정 된 OSD 파일을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-544">A value of 1 enables a user to use a modified OSD file.</span></span>

<span data-ttu-id="6b049-545">ImportApp</span><span class="sxs-lookup"><span data-stu-id="6b049-545">ImportApp</span></span> 

<span data-ttu-id="6b049-546">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-546">DWORD</span></span> 

<span data-ttu-id="6b049-547">0</span><span class="sxs-lookup"><span data-stu-id="6b049-547">0</span></span>

<span data-ttu-id="6b049-548">사용자가 응용 프로그램을 캐시로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-548">Does not allow a user to import applications into cache.</span></span> <span data-ttu-id="6b049-549">로드와 가져오기의 차이점은 로드가 트리거되면 클라이언트는 OSD, ASR 또는 Override URL에 포함 된 현재 구성 된 위치에서 패키지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-549">The difference between Load and Import is that when a Load is triggered, the client gets the package from the currently configured location contained in the OSD, ASR, or Override URL.</span></span> <span data-ttu-id="6b049-550">가져오기를 사용 하는 경우 패키지를 가져올 위치를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-550">When using Import, a location to get the package from must be specified.</span></span> 

<span data-ttu-id="6b049-551">raid-1</span><span class="sxs-lookup"><span data-stu-id="6b049-551">1</span></span>

<span data-ttu-id="6b049-552">사용자가 응용 프로그램을 캐시로 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-552">Allows a user to import applications into cache.</span></span> 

<span data-ttu-id="6b049-553">ChangeRefreshSettings</span><span class="sxs-lookup"><span data-stu-id="6b049-553">ChangeRefreshSettings</span></span>

<span data-ttu-id="6b049-554">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-554">DWORD</span></span>

<span data-ttu-id="6b049-555">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-555">Default=0</span></span>

<span data-ttu-id="6b049-556">값 1은 사용자가 서버에 대 한 새로 고침 설정을 수정할 수 있도록 합니다 (로그인 및 주기적 새로 고침 시 새로 고침).</span><span class="sxs-lookup"><span data-stu-id="6b049-556">A value of 1 allows users to modify the refresh settings for servers (refresh on login and periodic refresh).</span></span> <span data-ttu-id="6b049-557">이는 사용자가 다른 서버 설정 (path, host 등)을 수정할 수 있다는 것을 의미 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-557">This does not imply that the user can modify other server settings (path, host, and so on).</span></span>

<span data-ttu-id="6b049-558">ManageServers</span><span class="sxs-lookup"><span data-stu-id="6b049-558">ManageServers</span></span>

<span data-ttu-id="6b049-559">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-559">DWORD</span></span>

<span data-ttu-id="6b049-560">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-560">Default=0</span></span>

<span data-ttu-id="6b049-561">값 1을 사용 하면 사용자가 ChangeRefreshSettings 사용 권한에 의해 제어 되는 새로 고침 설정 편집을 제외 하 고 서버를 추가, 편집 및 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-561">A value of 1 allows the user to add, edit, and remove servers, except for editing the refresh settings, which is controlled by the ChangeRefreshSettings permission.</span></span>

<span data-ttu-id="6b049-562">기타 바로 가기</span><span class="sxs-lookup"><span data-stu-id="6b049-562">PublishShortcut</span></span>

<span data-ttu-id="6b049-563">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-563">DWORD</span></span>

<span data-ttu-id="6b049-564">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-564">Default=0</span></span>

<span data-ttu-id="6b049-565">값 1은 사용자 인터페이스를 통해 바로 가기를 게시할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-565">A value of 1 allows users to publish shortcuts through the user interface.</span></span> <span data-ttu-id="6b049-566">이는 게시 새로 고침 중에 게시 되는 바로 가기에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-566">This does not affect shortcuts that are published during a publishing refresh.</span></span>

<span data-ttu-id="6b049-567">ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="6b049-567">ViewAllApplications</span></span>

<span data-ttu-id="6b049-568">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-568">DWORD</span></span>

<span data-ttu-id="6b049-569">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-569">Default=0</span></span>

<span data-ttu-id="6b049-570">값 1은 사용자 인터페이스를 통해 모든 응용 프로그램을 표시 합니다. 그렇지 않으면 사용자의 응용 프로그램만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-570">A value of 1 displays all applications through the user interface; otherwise, only the user’s applications are displayed.</span></span>

<span data-ttu-id="6b049-571">RepairApp</span><span class="sxs-lookup"><span data-stu-id="6b049-571">RepairApp</span></span>

<span data-ttu-id="6b049-572">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-572">DWORD</span></span>

<span data-ttu-id="6b049-573">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-573">Default=1</span></span>

<span data-ttu-id="6b049-574">값 1은 사용자가 SFTMime 또는 클라이언트 관리 콘솔의 응용 프로그램에 대해 복구 작업을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-574">A value of 1 allows the user to use the Repair action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="6b049-575">응용 프로그램을 복구 하는 경우 사용자 지정 사용자 설정을 제거 하 고 기본 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-575">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="6b049-576">이 작업은 바로 가기 또는 파일 형식 연결을 변경 하거나 삭제 하지 않으며 캐시에서 응용 프로그램을 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-576">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

<span data-ttu-id="6b049-577">ClearApp</span><span class="sxs-lookup"><span data-stu-id="6b049-577">ClearApp</span></span>

<span data-ttu-id="6b049-578">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-578">DWORD</span></span>

<span data-ttu-id="6b049-579">기본값 = 1</span><span class="sxs-lookup"><span data-stu-id="6b049-579">Default=1</span></span>

<span data-ttu-id="6b049-580">값 1은 사용자가 SFTMime 또는 클라이언트 관리 콘솔의 응용 프로그램에 대해 Clear 작업을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-580">A value of 1 allows the user to use the Clear action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="6b049-581">콘솔에서 응용 프로그램을 지우면 해당 응용 프로그램을 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-581">When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="6b049-582">그러나 응용 프로그램은 캐시에 유지 되며 동일한 시스템의 다른 사용자가 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-582">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="6b049-583">게시 새로 고침 후에는 지워진 응용 프로그램을 다시 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-583">After a publishing refresh, the cleared applications will again become available to you.</span></span>

<span data-ttu-id="6b049-584">DeleteApp</span><span class="sxs-lookup"><span data-stu-id="6b049-584">DeleteApp</span></span>

<span data-ttu-id="6b049-585">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-585">DWORD</span></span>

<span data-ttu-id="6b049-586">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-586">Default=0</span></span>

<span data-ttu-id="6b049-587">값 1은 사용자가 SFTMime 또는 클라이언트 관리 콘솔의 응용 프로그램에 대해 Delete 작업을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-587">A value of 1 allows the user to use the Delete action on applications in SFTMime or the Client Management Console.</span></span> <span data-ttu-id="6b049-588">응용 프로그램을 삭제 하면 해당 클라이언트의 모든 사용자가 선택한 응용 프로그램을 더 이상 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-588">When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="6b049-589">바로 가기 및 파일 형식 연결이 삭제 되 고 응용 프로그램이 캐시에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-589">Shortcuts and file type associations are deleted and the application is deleted from cache.</span></span> <span data-ttu-id="6b049-590">그러나 다른 응용 프로그램이 선택한 응용 프로그램에 대 한 파일 시스템 캐시 또는 설정 데이터의 데이터를 참조 하는 경우 이러한 항목은 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-590">However, if another application refers to data in the file system cache or settings data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="6b049-591">게시 새로 고침을 수행한 후에는 삭제 된 응용 프로그램을 다시 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-591">After a publishing refresh, the deleted applications will again become available to you.</span></span>

<span data-ttu-id="6b049-592">ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="6b049-592">ToggleOfflineMode</span></span>

<span data-ttu-id="6b049-593">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-593">DWORD</span></span>

<span data-ttu-id="6b049-594">값 1은 사용자가 오프 라인 모드에서 클라이언트를 실행 하도록 선택할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-594">A value of 1 allows the users to select to run the client in Offline Mode.</span></span> <span data-ttu-id="6b049-595">오프 라인 모드에서 응용 프로그램 가상화 클라이언트는 응용 프로그램 가상화 서버에 연결 되어 있지 않은 경우에도 로드 된 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-595">In Offline Mode, the Application Virtualization client can start a loaded application even when it is not connected to an Application Virtualization Server.</span></span>



## <span data-ttu-id="6b049-596">사용자 지정 설정</span><span class="sxs-lookup"><span data-stu-id="6b049-596">Custom Settings</span></span>


<span data-ttu-id="6b049-597">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings 키에는 프런트 엔드 구성 요소에 대 한 값이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-597">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings key contains values specific to front-end components.</span></span> <span data-ttu-id="6b049-598">모든 사용자 지정 설정은 문자열로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-598">All custom settings are stored as strings.</span></span> <span data-ttu-id="6b049-599">다음 표에서는 CustomSettings 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-599">The following table provides information about the registry values associated with the CustomSettings key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-600">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-600">Name</span></span> </th>
<th align="left"><span data-ttu-id="6b049-601">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-601">Type</span></span> </th>
<th align="left"><span data-ttu-id="6b049-602">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-602">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="6b049-603">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-603">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-604">TrayErrorDelay</span><span class="sxs-lookup"><span data-stu-id="6b049-604">TrayErrorDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-605">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-605">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-606">기본값 = 30</span><span class="sxs-lookup"><span data-stu-id="6b049-606">Default=30</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-607">응용 프로그램 가상화 알림 영역에 시작 실패와 같은 오류 메시지가 표시 되는 시간 (초)입니다 &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="6b049-607">Time in seconds that the Application Virtualization notification area will display error messages like &quot;Launch failed&quot;.</span></span> <span data-ttu-id="6b049-608">최 솟 값 1</span><span class="sxs-lookup"><span data-stu-id="6b049-608">Minimum value of 1.</span></span> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-609">TraySuccessDelay</span><span class="sxs-lookup"><span data-stu-id="6b049-609">TraySuccessDelay</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-610">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-610">DWORD</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-611">기본값 = 10</span><span class="sxs-lookup"><span data-stu-id="6b049-611">Default=10</span></span> </p></td>
<td align="left"><p><span data-ttu-id="6b049-612">Appvmed 알림 영역에 &quot; Word 시작 &quot; 또는 &quot; Excel 종료와 같은 성공 메시지가 표시 되는 시간 (초)입니다 &quot; .</span><span class="sxs-lookup"><span data-stu-id="6b049-612">Time in seconds that the appvmed notification area will display success messages like &quot;Word launched&quot; or &quot;Excel shut down&quot;.</span></span> <span data-ttu-id="6b049-613">0 인 경우 해당 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-613">If 0, those messages will be suppressed.</span></span> </p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-614">TrayVisibility</span><span class="sxs-lookup"><span data-stu-id="6b049-614">TrayVisibility</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-615">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-616">기본값 = 0</span><span class="sxs-lookup"><span data-stu-id="6b049-616">Default=0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-617">0 = 가상화 된 응용 프로그램을 사용 하는 경우 트레이를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-617">0=Show Tray when virtualized applications are in use.</span></span></p>
<p><span data-ttu-id="6b049-618">1 = 항상 용지함을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-618">1=Show Tray always.</span></span></p>
<p><span data-ttu-id="6b049-619">2 = 용지함을 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-619">2=Never show Tray.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-620">TrayShowRefresh</span><span class="sxs-lookup"><span data-stu-id="6b049-620">TrayShowRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-621">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-621">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6b049-622">이 값을 1로 설정 하면 트레이 메뉴에 메뉴 항목 새로 고침 응용 프로그램이 표시 되 고 사용자가 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-622">When present and set to a value of 1, allows menu item Refresh Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-623">TrayShowLoad</span><span class="sxs-lookup"><span data-stu-id="6b049-623">TrayShowLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-624">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-624">DWORD</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6b049-625">값을 1로 설정 하면 트레이 메뉴에 메뉴 항목 로드 응용 프로그램이 표시 되 고 사용자가 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-625">When present and set to a value of 1, allows menu item Load Applications to be displayed on the Tray menu and is accessible by the user.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-626">보고 설정</span><span class="sxs-lookup"><span data-stu-id="6b049-626">Reporting Settings</span></span>


<span data-ttu-id="6b049-627">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting 키에는 App-v 관리 서버에 대 한 보고 관련 값이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-627">The HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting key contains values specific to reporting to an App-V Management Server.</span></span> <span data-ttu-id="6b049-628">다음 표에서는 보고 키와 연결 된 레지스트리 값에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-628">The following table provides information about the registry values associated with the Reporting key.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6b049-629">이름</span><span class="sxs-lookup"><span data-stu-id="6b049-629">Name</span></span> </th>
<th align="left"><span data-ttu-id="6b049-630">유형</span><span class="sxs-lookup"><span data-stu-id="6b049-630">Type</span></span> </th>
<th align="left"><span data-ttu-id="6b049-631">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="6b049-631">Data (Examples)</span></span> </th>
<th align="left"><span data-ttu-id="6b049-632">설명</span><span class="sxs-lookup"><span data-stu-id="6b049-632">Description</span></span> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6b049-633">DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="6b049-633">DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-634">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-634">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-635">기본값 = 20</span><span class="sxs-lookup"><span data-stu-id="6b049-635">Default=20</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-636">이 값은 보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-636">This value specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="6b049-637">크기는 메모리의 캐시에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-637">The size applies to the cache in memory.</span></span> <span data-ttu-id="6b049-638">제한에 도달 하면 로그 파일이 롤오버 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-638">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="6b049-639">목록 맨 아래에 새 레코드가 추가 되 면 하나 이상의 가장 오래 된 레코드 (목록 맨 위)가 삭제 되어 공간을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-639">When a new record is added (bottom of the list), one or more of the oldest records (top of the list) will be deleted to make room.</span></span> <span data-ttu-id="6b049-640">경고가 처음 발생 하면 클라이언트 로그 및 이벤트 로그에 기록 되 고, 전송이 성공적으로 취소 되 고 로그가 다시 채워지면 다시 기록 됩니다. 1.</span><span class="sxs-lookup"><span data-stu-id="6b049-640">A warning will be logged to the Client log and the event log the first time this occurs, and it will not be logged again until after the cache has been successfully cleared on transmission and the log has filled up again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6b049-641">DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="6b049-641">DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-642">DWORD</span><span class="sxs-lookup"><span data-stu-id="6b049-642">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-643">기본값 = 65536</span><span class="sxs-lookup"><span data-stu-id="6b049-643">Default=65536</span></span></p></td>
<td align="left"><p><span data-ttu-id="6b049-644">이 값은 로그가 유효 크기에 도달 했을 때 영구 전송 오류를 방지 하기 위해 게시 새로 고침 시 서버로 전송할 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-644">This value specifies the maximum size in bytes to transmit to the server at once on publishing refresh, to avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="6b049-645">기본값은 65536입니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-645">The default value is 65536.</span></span> <span data-ttu-id="6b049-646">보고서 데이터를 서버에 전송할 때 응용 프로그램 레코드의 블록 (바이트의 블록 크기 (XML 데이터))이 캐시에서 제거 되 고 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-646">When transmitting report data to the server, one block of application records—less than or equal to the block size in bytes of XML data—will be removed from the cache and sent to the server.</span></span> <span data-ttu-id="6b049-647">각 블록에는 일반 클라이언트 데이터 및 전역 패키지 목록 데이터가 앞에 있으며 블록 크기 계산에는 영향을 주지 않습니다. 매우 큰 패키지 목록을 통해 낮은 대역폭과 불안정 한 연결을 통해 전송 오류가 발생할 가능성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b049-647">Each block will have the general Client data and global package list data prepended, and these will not factor into the block size calculations; the potential exists for an extremely large package list to result in transmission failures over low bandwidth or unreliable connections.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6b049-648">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6b049-648">Related topics</span></span>


[<span data-ttu-id="6b049-649">Application Virtualization Client 참조</span><span class="sxs-lookup"><span data-stu-id="6b049-649">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)









