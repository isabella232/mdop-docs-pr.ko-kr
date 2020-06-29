---
title: 배포 탭 정보
description: 배포 탭 정보
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819963"
---
# <span data-ttu-id="bf6c8-103">배포 탭 정보</span><span class="sxs-lookup"><span data-stu-id="bf6c8-103">About the Deployment Tab</span></span>


<span data-ttu-id="bf6c8-104">응용 프로그램 가상화 시퀀서 콘솔의 **배포** 탭을 사용 하 여 시퀀싱 하려는 응용 프로그램에 대 한 정보를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="bf6c8-105">이 탭에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="bf6c8-106">서버 URL</span><span class="sxs-lookup"><span data-stu-id="bf6c8-106">Server URL</span></span>


<span data-ttu-id="bf6c8-107">**서버 URL** 컨트롤을 사용 하 여 가상 응용 프로그램 서버 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf6c8-108">컨트롤</span><span class="sxs-lookup"><span data-stu-id="bf6c8-108">Control</span></span></th>
<th align="left"><span data-ttu-id="bf6c8-109">설명</span><span class="sxs-lookup"><span data-stu-id="bf6c8-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf6c8-110">프로토콜</span><span class="sxs-lookup"><span data-stu-id="bf6c8-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-111">가상 응용 프로그램 서버에서 응용 프로그램 가상화 데스크톱 클라이언트로 시퀀싱 된 응용 프로그램 패키지를 스트림할 프로토콜을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="bf6c8-112">다음 프로토콜을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="bf6c8-113">RTSP </strong> — 기본값은 실시간 스트리밍 프로토콜이 가상화 지원 응용 프로그램의 교환을 제어 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="bf6c8-114">RTSPS </strong> -전송 계층 보안이 포함 된 실시간 스트리밍 프로토콜이 시퀀싱 된 응용 프로그램 패키지의 교환을 제어 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="bf6c8-115">파일 </strong> -시퀀싱 된 응용 프로그램을 파일 공유에서 스트림할 것을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="bf6c8-116">HTTPS </strong> -보안 하이퍼텍스트 전송 프로토콜이 패키지의 교환을 제어 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf6c8-117">이름의</span><span class="sxs-lookup"><span data-stu-id="bf6c8-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-118">소프트웨어 패키지를 응용 프로그램 가상화 데스크톱 클라이언트로 스트리밍하는 가상 응용 프로그램 서버 그룹의 앞에 있는 가상 응용 프로그램 서버 또는 부하 분산 장치를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="bf6c8-119">시퀀싱 된 응용 프로그램 패키지를 만들려면이 항목을 완료 해야 하지만 기본% SFT_SOFTGRIDSERVER% 환경 변수를 가상 응용 프로그램 서버의 실제 호스트 이름 또는 IP 주소로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bf6c8-120">참고</span><span class="sxs-lookup"><span data-stu-id="bf6c8-120">Note</span></span></strong><br/><p><span data-ttu-id="bf6c8-121">정적 호스트 이름 또는 IP 주소를 지정 하지 않도록 선택한 경우 각 응용 프로그램 가상화 데스크톱 클라이언트에서 SFT_SOFTGRIDSERVER 라는 환경 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="bf6c8-122">해당 값은이 클라이언트&#39;s 응용 프로그램 원본에 해당 하는 부하 분산 장치 또는 가상 응용 프로그램 서버의 호스트 이름 또는 IP 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="bf6c8-123">이 환경 변수를 사용자 변수가 아닌 시스템 변수로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="bf6c8-124">이 변수를 할당 하는 동안이 컴퓨터에서 실행 되는 모든 Application Virtualization Desktop 클라이언트 세션을 닫은 후 열어야 다시 시작 된 세션에서 새 응용 프로그램 원본을 인식 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf6c8-125">Port</span><span class="sxs-lookup"><span data-stu-id="bf6c8-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-126">가상 응용 프로그램 서버 또는 부하 분산이 패키지에 대 한 응용 프로그램 가상화 데스크톱 클라이언트&#39;s 요청을 수신 대기 하는 포트를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="bf6c8-127">이 정보는 패키지를 만드는 데 필요 하지만 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="bf6c8-128">기본 포트는 554입니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf6c8-129">경로</span><span class="sxs-lookup"><span data-stu-id="bf6c8-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-130">소프트웨어 패키지가 저장 되 고 스트리밍되는 가상 응용 프로그램 서버의 상대 경로를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="bf6c8-131">이 정보는 SFT 파일을 콘텐츠의 하위 디렉터리에 저장 하는 경우 패키지를 만드는 데 필요 합니다. 그렇지 않은 경우에는이 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bf6c8-132">운영 체제</span><span class="sxs-lookup"><span data-stu-id="bf6c8-132">Operating Systems</span></span>


<span data-ttu-id="bf6c8-133">**Os** 컨트롤을 사용 하 여 응용 프로그램의 운영 체제 요구 사항을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="bf6c8-134">Application Virtualization 데스크톱 클라이언트가 선택 된 운영 체제를 지원할 수 없는 경우에는 응용 프로그램이 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf6c8-135">컨트롤</span><span class="sxs-lookup"><span data-stu-id="bf6c8-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="bf6c8-136">설명</span><span class="sxs-lookup"><span data-stu-id="bf6c8-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf6c8-137">사용할 수 있는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="bf6c8-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-138">패키지의 응용 프로그램을 지원할 수 있는 운영 체제 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf6c8-139">선택한 운영 체제</span><span class="sxs-lookup"><span data-stu-id="bf6c8-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-140">패키지의 응용 프로그램을 지 원하는 선택 된 운영 체제 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bf6c8-141">출력 옵션</span><span class="sxs-lookup"><span data-stu-id="bf6c8-141">Output Options</span></span>


<span data-ttu-id="bf6c8-142">**출력 옵션** 컨트롤을 사용 하 여 설치할 응용 프로그램의 출력 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bf6c8-143">컨트롤</span><span class="sxs-lookup"><span data-stu-id="bf6c8-143">Control</span></span></th>
<th align="left"><span data-ttu-id="bf6c8-144">설명</span><span class="sxs-lookup"><span data-stu-id="bf6c8-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf6c8-145">압축 알고리즘</span><span class="sxs-lookup"><span data-stu-id="bf6c8-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-146">네트워크를 통해 스트리밍하는 SFT 파일을 압축 하는 방법을 선택 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="bf6c8-147">다음 압축 방법 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="bf6c8-148">압축 됨 </strong> -SFT 파일을 ZLIB 형식으로 압축 하도록 지정 합니다 <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="bf6c8-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="bf6c8-149">압축 안 함 </strong> — 기본값은 SFT 파일이 압축 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bf6c8-150">보안 설명자 적용</span><span class="sxs-lookup"><span data-stu-id="bf6c8-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-151">클라이언트에 배포 된 후 패키지에 있는 응용 프로그램의 보안 설명자를 적용 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bf6c8-152">Microsoft Windows Installer (MSI) 패키지 생성</span><span class="sxs-lookup"><span data-stu-id="bf6c8-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bf6c8-153">Windows Installer를 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 설치 또는 배포 하려면 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="bf6c8-154">시퀀서를 사용 하 여 변경 하는 경우 변경 내용이 Windows Installer 파일에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="bf6c8-155">Windows Installer 파일은 항상 하드 디스크에 저장 된 sft 파일을 사용 하 여 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bf6c8-156">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bf6c8-156">Related topics</span></span>


[<span data-ttu-id="bf6c8-157">배포 속성을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="bf6c8-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="bf6c8-158">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="bf6c8-158">Sequencer Console</span></span>](sequencer-console.md)









