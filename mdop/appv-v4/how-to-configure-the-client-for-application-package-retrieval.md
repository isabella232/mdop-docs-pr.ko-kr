---
title: 응용 프로그램 패키지 검색에 대한 클라이언트를 구성하는 방법
description: 응용 프로그램 패키지 검색에 대한 클라이언트를 구성하는 방법
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817828"
---
# <span data-ttu-id="baf2a-103">응용 프로그램 패키지 검색에 대한 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="baf2a-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="baf2a-104">클라이언트가 Application Virtualization (App-v) 관리 서버를 사용 하 여 게시 서버로 구성 되는 경우, 다음 게시 새로 고침 주기에 기본적으로 클라이언트는 사용자가 사용할 수 있도록 허가 받은 각 패키지에 대 한 OSD (Open Software Descriptor) 및 패키지 매니페스트 파일을 서버에서 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="baf2a-105">클라이언트는 이러한 파일에 정의 된 패키지 원본 정보를 사용 하 여 패키지 콘텐츠, 아이콘 및 파일 형식 연결을 찾을 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="baf2a-106">클라이언트가 App-v 관리 서버 대신 웹 서버 또는 파일 서버와 같은 로컬 App-v 스트리밍 서버 또는 다른 대체 원본에서 패키지 콘텐츠 (SFT 파일)를 얻으려면 다른 서버의 로컬 콘텐츠 공유를 가리키도록 컴퓨터의 ApplicationSourceRoot 레지스트리 키 값을 구성할 수 있습니다 (선택).</span><span class="sxs-lookup"><span data-stu-id="baf2a-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="baf2a-107">OSD 파일은 여전히 패키지 콘텐츠의 원래 원본 경로를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="baf2a-108">그러나 클라이언트는 서버 대신 ApplicationSourceRoot 설정 값을 사용 하 고 OSD 파일의 콘텐츠 경로에 지정 된 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="baf2a-109">이렇게 하면 클라이언트가 다른 서버의 콘텐츠를 검색할 수 있도록 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="baf2a-110">패키지 매니페스트 파일 또는 게시 서버에서 보낸 경로에 해당 설정을 재정의 하려는 경우 OSDSourceRoot 및 IconSourceRoot 레지스트리 키 값도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="baf2a-111">OSDSourceRoot는 게시 하는 동안 응용 프로그램 패키지에 대 한 OSD 파일 검색의 원본 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="baf2a-112">IconSourceRoot는 게시 하는 동안 응용 프로그램 패키지에 대 한 아이콘 검색의 원본 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="baf2a-113">참고</span><span class="sxs-lookup"><span data-stu-id="baf2a-113">Note</span></span>**  
-   <span data-ttu-id="baf2a-114">IconSourceRoot 및 OSDSourceRoot 설정은 패키지 매니페스트 파일의 값을 재정의 하므로 Windows Installer (.msi) 파일 메서드를 사용 하 여 패키지를 배포 하려고 하면 해당 .msi 파일에 포함 된 패키지 매니페스트 파일의 값도 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="baf2a-115">게시 및 HTTP (S) 스트리밍 작업 중에 App-v 4.5 SP1 클라이언트는 사용자 컴퓨터의 Internet Explorer에서 구성한 프록시 서버 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="baf2a-116">ApplicationSourceRoot 레지스트리 키 값을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="baf2a-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="baf2a-117">UNC 경로 또는 URL 중 하나를 사용 하 여 ApplicationSourceRoot를 다음 레지스트리 키 값으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="baf2a-118">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="baf2a-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="baf2a-119">UNC (범용 명명 규칙) 경로에 대 한 올바른 형식은 **\\\\computername\\sharefolder\\\ [folder \] \ [\\ \]** 입니다. 여기서 **폴더** 는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="baf2a-120">**Computername** 은 FQDN (정규화 된 도메인 이름) 또는 IP 주소이 될 수 있으며, **sharefolder** 는 드라이브 문자 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="baf2a-121">OSD 경로의 **\\\\computername\\sharedfolder** 또는 drive 문자 부분만 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="baf2a-122">URL 경로의 올바른 형식은 **프로토콜://servername: \ [port \] \ [/c\] \ [/\]**, 여기서 **port** 와 **path** 는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="baf2a-123">**Port** 를 지정 하지 않으면 프로토콜에 대 한 기본 포트가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="baf2a-124">OSD URL의 **//server: port** 부분만 대체 되는 프로토콜:</span><span class="sxs-lookup"><span data-stu-id="baf2a-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="baf2a-125">중요</span><span class="sxs-lookup"><span data-stu-id="baf2a-125">Important</span></span>**  
    <span data-ttu-id="baf2a-126">환경 변수는 ApplicationSourceRoot 정의에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="baf2a-127">OSDSourceRoot 값을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="baf2a-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="baf2a-128">UNC 경로 또는 URL 중 하나를 사용 하 여 OSDSourceRoot를 다음 레지스트리 키 값으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="baf2a-129">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="baf2a-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="baf2a-130">OSDSourceRoot에 허용 되는 형식에는 다음 예제와 같이 UNC 경로 및 Url이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="baf2a-131">**\\\\computername\\sharefolder\\resource** 또는 **\\\\computername\\content** 또는 \*\* &lt; drive &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="baf2a-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="baf2a-132">**http://computername/productivity/** 또는**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="baf2a-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="baf2a-133">IconSourceRoot 값을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="baf2a-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="baf2a-134">UNC 경로 또는 URL 중 하나를 사용 하 여 IconSourceRoot를 다음 레지스트리 키 값으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="baf2a-135">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="baf2a-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="baf2a-136">IconSourceRoot에 허용 되는 형식에는 다음 예제와 같이 UNC 경로 및 Url이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baf2a-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="baf2a-137">**\\\\computername\\sharefolder\\resource** 또는 **\\\\computername\\content** 또는 \*\* &lt; drive &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="baf2a-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="baf2a-138">**http://computername/productivity/** 또는**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="baf2a-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="baf2a-139">관련 항목</span><span class="sxs-lookup"><span data-stu-id="baf2a-139">Related topics</span></span>


[<span data-ttu-id="baf2a-140">명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="baf2a-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









