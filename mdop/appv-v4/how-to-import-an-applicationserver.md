---
title: 응용 프로그램을 가져오는 방법
description: 응용 프로그램을 가져오는 방법
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817403"
---
# <span data-ttu-id="9bf1d-103">응용 프로그램을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="9bf1d-103">How to Import an Application</span></span>


<span data-ttu-id="9bf1d-104">일반적으로 응용 프로그램 가상화 관리 서버에서 스트림에 사용할 수 있도록 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="9bf1d-105">수동으로 응용 프로그램을 추가할 수도 있지만 응용 프로그램에 대 한 자세한 정보를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="9bf1d-106">자세한 내용은 [응용 프로그램을 수동으로 추가 하는 방법을](how-to-manually-add-an-application.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="9bf1d-107">**참고**  응용 프로그램을 가져오려면 서버에서 사용할 수 있는 파일의 순차화 된 OSD (개방형 소프트웨어 설명자) 파일이 나 해당 Sequencer 프로젝트 (SPRJ) 파일이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="9bf1d-108">응용 프로그램을 가져올 때 서버는 **시스템 옵션** 대화 상자의 **일반** 탭에 있는 **기본 콘텐츠 경로** 필드의 값으로 구성 되었는지 확인 해야 합니다 (App-v server 콘솔의 **application Virtualization System** 노드를 마우스 오른쪽 단추로 클릭 하 여 액세스할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="9bf1d-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="9bf1d-109">기본 콘텐츠 경로 값은 응용 프로그램을 가져올 위치를 정의 하 고, 가져오기 프로세스 중에이 값을 사용 하 여 SFT 파일과 아이콘 바로 가기의 OSD 파일에 정의 된 경로를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="9bf1d-110">OSD 파일에서 SFT 파일의 경로는 CODEBASE HREF 엔트리에 지정 되며 아이콘에 대 한 경로는 바로 가기 항목에 지정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="9bf1d-111">가져오기 프로세스가 진행 되는 동안 OSD 파일의 이러한 두 경로에 지정 된 프로토콜, 서버 및 포트가 기본 콘텐츠 경로의 값으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="9bf1d-112">다음 표에서는 가져오기 경로에 영향을 주는 방법의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9bf1d-113">기본 콘텐츠 경로</span><span class="sxs-lookup"><span data-stu-id="9bf1d-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="9bf1d-114">OSD 파일 코드 베이스 HREF</span><span class="sxs-lookup"><span data-stu-id="9bf1d-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="9bf1d-115">결과 값</span><span class="sxs-lookup"><span data-stu-id="9bf1d-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9bf1d-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="9bf1d-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="9bf1d-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="9bf1d-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9bf1d-118">응용 프로그램을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="9bf1d-118">To import an application</span></span>**

1.  <span data-ttu-id="9bf1d-119">왼쪽 창에서 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 하 고 **응용 프로그램 가져오기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="9bf1d-120">**열기** 대화 상자에서 응용 프로그램의 SPRJ 또는 OSD 파일로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="9bf1d-121">파일을 강조 표시 하 고 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="9bf1d-122">**새 응용 프로그램 마법사**에서 스트리밍할 응용 프로그램에 대해 **사용** 상자가 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="9bf1d-123">또한 설명을 입력 하 고 서버 및 파일 경로를 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="9bf1d-124">또한 라이선스 및 서버 그룹을 설정한 경우 해당 사용자를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="9bf1d-125">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-125">Click **Next**.</span></span>

5.  <span data-ttu-id="9bf1d-126">게시 된 **바로 가기** 화면에서 응용 프로그램 바로 가기를 클라이언트 컴퓨터에 표시할 위치에 해당 하는 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="9bf1d-127">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-127">Click **Next**.</span></span>

7.  <span data-ttu-id="9bf1d-128">**파일 연결** 화면에서이 응용 프로그램에 새 파일 연결을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="9bf1d-129">이렇게 하려면 **추가**를 클릭 하 고 확장명 (앞에 있는 점을 포함 하지 않음)을 입력 한 다음 설명을 입력 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="9bf1d-130">**참고**  Sequencer 4.0으로 시퀀싱 된 응용 프로그램은 관리 콘솔을 통해 가져오거나 만들 때 **파일 연결** 대화 상자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="9bf1d-131">이전 Sequencer 버전 패키지를 사용 하는 응용 프로그램은 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="9bf1d-132">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-132">Click **Next**.</span></span>

9.  <span data-ttu-id="9bf1d-133">**액세스 권한** 화면에서 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="9bf1d-134">**그룹 선택** 대화 상자를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="9bf1d-135">완료 되 면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="9bf1d-136">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-136">Click **Next**.</span></span>

12. <span data-ttu-id="9bf1d-137">**요약** 화면에서 가져오기 설정을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="9bf1d-138">**마침을**클릭 하거나 **뒤로** 를 클릭 하 여 가져오기를 변경 하거나 **취소** 를 클릭 하 여 가져오기를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf1d-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="9bf1d-139">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9bf1d-139">Related topics</span></span>


[<span data-ttu-id="9bf1d-140">Server Management Console에서 응용 프로그램 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="9bf1d-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="9bf1d-141">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="9bf1d-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="9bf1d-142">수동으로 응용 프로그램을 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="9bf1d-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





