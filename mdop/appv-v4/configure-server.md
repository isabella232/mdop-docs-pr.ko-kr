---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821973"
---
# <span data-ttu-id="63df6-103">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="63df6-103">CONFIGURE SERVER</span></span>


<span data-ttu-id="63df6-104">사용자가 서버의 설정을 변경할 수 있도록 합니다. 지정 하지 않은 설정은 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-104">Enables a user to change the setup of a server; any settings not specified will not be modified.</span></span>

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63df6-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="63df6-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="63df6-106">설명</span><span class="sxs-lookup"><span data-stu-id="63df6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-107">서버: &lt; 서버 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="63df6-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-108">게시 서버의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63df6-109">/NAME &lt; display-NAME&gt;</span><span class="sxs-lookup"><span data-stu-id="63df6-109">/NAME &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-110">서버의 새 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-110">New display name for the server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-111">/HOST &lt; 호스트 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="63df6-111">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-112">게시 서버의 호스트 이름 또는 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-112">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63df6-113">/PORT &lt; 포트&gt;</span><span class="sxs-lookup"><span data-stu-id="63df6-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-114">게시 서버가 수신 대기 하는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="63df6-115">일반 HTTP 서버용 80, 고급 보안을 사용 하는 HTTP 서버에 대 한 443, 일반 응용 프로그램 가상화 서버의 경우 554, 고급 보안을 사용 하는 서버의 경우 322를 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-116">/PATH &lt; 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="63df6-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-117">게시 요청에 사용 되는 URL의 경로 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="63df6-118">TYPE 매개 변수를 RTSP로 설정 하는 경우 경로는 선택 사항이 고 기본값은 &quot; / &quot; 입니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63df6-119">/TYPE</span><span class="sxs-lookup"><span data-stu-id="63df6-119">/TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-120">게시 서버가 웹 서버 ( &quot; HTTP &quot; ) 또는 RTSP (Application Virtualization server) 인지 여부를 나타냅니다 &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="63df6-120">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-121">/새로 고침</span><span class="sxs-lookup"><span data-stu-id="63df6-121">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-122">이로 설정 되 면 사용자가 로그인 할 때 게시 정보가 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-122">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="63df6-123">기본적으로 ON으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-123">Defaults to ON.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63df6-124">/CSECURE</span><span class="sxs-lookup"><span data-stu-id="63df6-124">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-125">있는 경우 게시 서버에 향상 된 보안의 연결을 설정 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-125">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-126">/LOG</span><span class="sxs-lookup"><span data-stu-id="63df6-126">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-127">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-127">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63df6-128">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="63df6-128">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-129">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="63df6-129">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-130">/GUI</span><span class="sxs-lookup"><span data-stu-id="63df6-130">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-131">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-131">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="63df6-132">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-132">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63df6-133">/LOGU</span><span class="sxs-lookup"><span data-stu-id="63df6-133">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="63df6-134">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63df6-134">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="63df6-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="63df6-135">Related topics</span></span>


[<span data-ttu-id="63df6-136">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="63df6-136">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





