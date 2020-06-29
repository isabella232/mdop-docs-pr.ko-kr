---
title: App-V를 사용하여 Microsoft Office 2010 배포
description: App-V를 사용하여 Microsoft Office 2010 배포
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814625"
---
# <span data-ttu-id="f8049-103">App-V를 사용하여 Microsoft Office 2010 배포</span><span class="sxs-lookup"><span data-stu-id="f8049-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="f8049-104">다음 방법 중 하나를 사용 하 여 Microsoft App-v (Application Virtualization) 5.1에 대 한 Office 2010 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="f8049-105">Application Virtualization (App-v) Sequencer</span><span class="sxs-lookup"><span data-stu-id="f8049-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="f8049-106">App-v (Application Virtualization) 패키지 가속기</span><span class="sxs-lookup"><span data-stu-id="f8049-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="f8049-107">Office 2010에 대 한 앱-V 지원</span><span class="sxs-lookup"><span data-stu-id="f8049-107">App-V support for Office 2010</span></span>


<span data-ttu-id="f8049-108">다음 표에서는 App-v 버전, Office 패키지 만들기 방법, 지원 되는 라이선스, Office 2010에 대해 지원 되는 배포를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f8049-109">지원 되는 항목</span><span class="sxs-lookup"><span data-stu-id="f8049-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="f8049-110">지원 수준</span><span class="sxs-lookup"><span data-stu-id="f8049-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-111">지원 되는 App-v 버전</span><span class="sxs-lookup"><span data-stu-id="f8049-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f8049-112">4.6</span><span class="sxs-lookup"><span data-stu-id="f8049-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="f8049-113">5.0</span><span class="sxs-lookup"><span data-stu-id="f8049-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="f8049-114">5.1</span><span class="sxs-lookup"><span data-stu-id="f8049-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-115">패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="f8049-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f8049-116">시퀀스</span><span class="sxs-lookup"><span data-stu-id="f8049-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="f8049-117">패키지 가속기</span><span class="sxs-lookup"><span data-stu-id="f8049-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="f8049-118">Office 배포 키트</span><span class="sxs-lookup"><span data-stu-id="f8049-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-119">지원 되는 라이선스</span><span class="sxs-lookup"><span data-stu-id="f8049-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-120">볼륨 라이선스</span><span class="sxs-lookup"><span data-stu-id="f8049-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-121">지원되는 배포</span><span class="sxs-lookup"><span data-stu-id="f8049-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f8049-122">Desktop</span><span class="sxs-lookup"><span data-stu-id="f8049-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="f8049-123">개인 VDI</span><span class="sxs-lookup"><span data-stu-id="f8049-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="f8049-124">RDS</span><span class="sxs-lookup"><span data-stu-id="f8049-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f8049-125">Sequencer를 사용 하 여 Office 2010 앱-V 5.1 만들기</span><span class="sxs-lookup"><span data-stu-id="f8049-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="f8049-126">Office 2010는 앱-V 5.1에서 Office 2010 패키지를 만들기 위한 주요 방법 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="f8049-127">Microsoft는 지식 기반 문서를 통해 자세한 작성법을 제공 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="f8049-128">App-v 5.1에서 Office 2010 패키지를 만들려면 다음 링크에서 자세한 지침을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8049-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="f8049-129">Microsoft Application Virtualization 5.0에서 Microsoft Office 2010을 시퀀싱 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f8049-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="f8049-130">패키지 가속기를 사용 하 여 Office 2010 앱-V 5.1 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="f8049-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="f8049-131">Office 2010 App-v 5.1 패키지는 패키지 가속기를 통해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="f8049-132">Microsoft는 Windows 10, Windows 8 및 Windows 7에서 Office 2010을 만들기 위한 패키지 가속기를 제공 했습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="f8049-133">패키지 가속기를 사용 하 여 App-v에 Office 2010 패키지를 만들려면 다음 페이지를 참조 하 여 적절 한 패키지 가속기에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="f8049-134">Office Professional Plus 2010 용 app-v 5.0 패키지 가속기 – Windows 8</span><span class="sxs-lookup"><span data-stu-id="f8049-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="f8049-135">Office Professional Plus 2010 용 app-v 5.0 패키지 가속기-Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8049-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="f8049-136">App-v 패키지 바로 연결을 사용 하 여 가상 응용 프로그램 패키지를 만드는 방법에 대 한 자세한 지침은 [App-v 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만드는 방법을](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8049-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="f8049-137">앱에 대 한 Microsoft Office 패키지 배포-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f8049-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="f8049-138">다음 App-v 배포 방법 중 하나를 사용 하 여 Office 2010 패키지를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="f8049-139">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f8049-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="f8049-140">App-v server</span><span class="sxs-lookup"><span data-stu-id="f8049-140">App-V server</span></span>

-   <span data-ttu-id="f8049-141">독립 실행형-PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="f8049-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="f8049-142">Office 앱-V 패키지 관리 및 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="f8049-142">Office App-V package management and customization</span></span>


<span data-ttu-id="f8049-143">Office 2010 패키지는 알려진 패키지 관리 메커니즘을 통해 다른 App-v 5.1 패키지와 같이 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="f8049-144">예를 들어 Office 패키지 추가, 게시, 게시 취소 또는 제거 등 특별 한 지침이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="f8049-145">Windows와 Microsoft Office 통합</span><span class="sxs-lookup"><span data-stu-id="f8049-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="f8049-146">다음 표에는 Office 2010의 지원 되는 통합 지점에 대 한 전체 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f8049-147">확장점</span><span class="sxs-lookup"><span data-stu-id="f8049-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="f8049-148">설명</span><span class="sxs-lookup"><span data-stu-id="f8049-148">Description</span></span></th>
<th align="left"><span data-ttu-id="f8049-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="f8049-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-150">Firefox 및 Chrome 용 Lync 모임 참가 플러그 인</span><span class="sxs-lookup"><span data-stu-id="f8049-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-151">사용자가 Firefox 및 Chrome에서 Lync 모임에 참가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-152">OneNote 인쇄 드라이버로 전송 됨</span><span class="sxs-lookup"><span data-stu-id="f8049-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-153">사용자가 OneNote에 인쇄할 수 있음</span><span class="sxs-lookup"><span data-stu-id="f8049-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-154">예</span><span class="sxs-lookup"><span data-stu-id="f8049-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-155">OneNote에 연결 된 노트</span><span class="sxs-lookup"><span data-stu-id="f8049-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-156">OneNote에 연결 된 노트</span><span class="sxs-lookup"><span data-stu-id="f8049-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-157">OneNote Internet Explorer 추가 기능으로 보내기</span><span class="sxs-lookup"><span data-stu-id="f8049-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-158">IE에서 OneNote로 보낼 수 있는 사용자</span><span class="sxs-lookup"><span data-stu-id="f8049-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-159">Lync 및 Outlook에 대 한 방화벽 예외</span><span class="sxs-lookup"><span data-stu-id="f8049-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-160">Lync 및 Outlook에 대 한 방화벽 예외</span><span class="sxs-lookup"><span data-stu-id="f8049-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-161">MAPI 클라이언트</span><span class="sxs-lookup"><span data-stu-id="f8049-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-162">기본 앱과 추가 기능은 MAPI를 통해 가상 Outlook과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-163">Firefox 용 SharePoint 플러그 인</span><span class="sxs-lookup"><span data-stu-id="f8049-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-164">사용자가 Firefox에서 SharePoint 기능을 사용할 수 있음</span><span class="sxs-lookup"><span data-stu-id="f8049-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-165">메일 제어판 애플릿</span><span class="sxs-lookup"><span data-stu-id="f8049-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-166">사용자가 Outlook의 메일 제어판 애플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-167">예</span><span class="sxs-lookup"><span data-stu-id="f8049-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-168">기본 Interop 어셈블리</span><span class="sxs-lookup"><span data-stu-id="f8049-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-169">관리 되는 추가 기능 지원</span><span class="sxs-lookup"><span data-stu-id="f8049-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-170">Office 문서 캐시 처리기</span><span class="sxs-lookup"><span data-stu-id="f8049-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-171">Office 응용 프로그램에 대해 문서 캐시를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8049-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-172">Outlook 프로토콜 검색 처리기</span><span class="sxs-lookup"><span data-stu-id="f8049-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-173">사용자가 outlook에서 검색할 수 있음</span><span class="sxs-lookup"><span data-stu-id="f8049-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-174">예</span><span class="sxs-lookup"><span data-stu-id="f8049-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f8049-175">Active X 컨트롤:</span><span class="sxs-lookup"><span data-stu-id="f8049-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-176">ActiveX 컨트롤에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> Activex 컨트롤 API 참조를 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8049-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-177">SiteClient</span><span class="sxs-lookup"><span data-stu-id="f8049-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-178">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-179">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="f8049-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-180">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-181">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="f8049-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-182">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="f8049-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-184">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="f8049-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-186">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="f8049-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-188">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="f8049-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-190">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="f8049-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-192">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-193">Sharpoint Xmldocuments</span><span class="sxs-lookup"><span data-stu-id="f8049-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-194">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-195">Sharepoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="f8049-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-196">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-197">WinProj</span><span class="sxs-lookup"><span data-stu-id="f8049-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-198">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-199">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="f8049-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-200">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-201">이 (가) Copysud.</span><span class="sxs-lookup"><span data-stu-id="f8049-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-202">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-203">CommunicatorMeetingJoinAx 관리자</span><span class="sxs-lookup"><span data-stu-id="f8049-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-204">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="f8049-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="f8049-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-206">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="f8049-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="f8049-207">OneDrive Pro 브라우저 도우미</span><span class="sxs-lookup"><span data-stu-id="f8049-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-208">Active X Control]</span><span class="sxs-lookup"><span data-stu-id="f8049-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f8049-209">OneDrive Pro 아이콘 오버레이</span><span class="sxs-lookup"><span data-stu-id="f8049-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="f8049-210">사용자가 폴더를 찾을 때 Windows 탐색기 셸 아이콘 오버레이 (OneDrive Pro 폴더)</span><span class="sxs-lookup"><span data-stu-id="f8049-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f8049-211">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="f8049-211">Additional resources</span></span>


**<span data-ttu-id="f8049-212">Office 2013 앱-V 패키지 추가 리소스</span><span class="sxs-lookup"><span data-stu-id="f8049-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="f8049-213">Microsoft Office를 시퀀싱 된 앱으로 배포 하는 데 지원 되는 시나리오-V 패키지</span><span class="sxs-lookup"><span data-stu-id="f8049-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="f8049-214">Office 2010 앱-V 패키지</span><span class="sxs-lookup"><span data-stu-id="f8049-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="f8049-215">Microsoft Application Virtualization 5.0 용 microsoft Office 2010 시퀀싱 키트</span><span class="sxs-lookup"><span data-stu-id="f8049-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="f8049-216">앱-V 5.0 Office 2010 패키지를 만들거나 사용할 때의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="f8049-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="f8049-217">Microsoft Application Virtualization 5.0에서 Microsoft Office 2010을 시퀀싱 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f8049-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="f8049-218">연결 그룹</span><span class="sxs-lookup"><span data-stu-id="f8049-218">Connection Groups</span></span>**

[<span data-ttu-id="f8049-219">Microsoft App-V v5에 연결 그룹 배포</span><span class="sxs-lookup"><span data-stu-id="f8049-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="f8049-220">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="f8049-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="f8049-221">동적 구성</span><span class="sxs-lookup"><span data-stu-id="f8049-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="f8049-222">App-V 5.1 동적 구성 정보</span><span class="sxs-lookup"><span data-stu-id="f8049-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





