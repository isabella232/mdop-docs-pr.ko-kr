---
title: 수동으로 응용 프로그램을 추가하는 방법
description: 수동으로 응용 프로그램을 추가하는 방법
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817098"
---
# <span data-ttu-id="eb9a9-103">수동으로 응용 프로그램을 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="eb9a9-103">How to Manually Add an Application</span></span>


<span data-ttu-id="eb9a9-104">응용 프로그램 가상화 관리 서버에 응용 프로그램을 추가할 때는 가져오는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="eb9a9-105">수동으로 응용 프로그램을 추가할 수 있지만이 섹션에서 호출 되는 응용 프로그램에 대 한 자세한 정보를 정확 하 게 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="eb9a9-106">수동으로 새 응용 프로그램을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="eb9a9-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="eb9a9-107">왼쪽 창에서 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 하 고 **새 응용 프로그램**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="eb9a9-108">**새 응용 프로그램 마법사**에서 **일반 정보** 대화 상자를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="eb9a9-109">**응용 프로그램 이름**— 사용자에 게 표시할 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="eb9a9-110">**버전**— 응용 프로그램 버전을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="eb9a9-111">**Enabled**-이 상자를 선택 해야 응용 프로그램을 만든 후 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="eb9a9-112">**설명**— 관리 사용에 대 한 설명을 입력 합니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="eb9a9-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="eb9a9-113">**Osd 경로**-응용 프로그램의 Osd (개방형 소프트웨어 설명자) 파일에 대 한 네트워크를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="eb9a9-114">이 파일은 공유 네트워크 폴더에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="eb9a9-115">**아이콘 경로**— 응용 프로그램의 .ico 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="eb9a9-116">**응용 프로그램 라이선스 그룹**-라이선스 그룹을 설정한 경우에는 풀 다운 목록에서 선택 하 여 응용 프로그램을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="eb9a9-117">**서버 그룹**— 여러 응용 프로그램 가상화 서버가 있는 경우 풀 다운 목록에서 선택 하 여 응용 프로그램을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="eb9a9-118">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-118">Click **Next**.</span></span>

4.  <span data-ttu-id="eb9a9-119">**패키지 선택** 대화 상자에서 관련 패키지를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="eb9a9-120">게시 된 **바로 가기** 화면에서 클라이언트 컴퓨터에 응용 프로그램 바로 가기를 표시할 위치에 해당 하는 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="eb9a9-121">**파일 연결** 화면에서이 응용 프로그램에 새 형식 파일 연결을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="eb9a9-122">이렇게 하려면 **추가**를 클릭 하 고 확장명 (앞에 있는 점을 포함 하지 않음)을 입력 한 다음 설명을 입력 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="eb9a9-123">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-123">Click **Next**.</span></span>

8.  <span data-ttu-id="eb9a9-124">**액세스 권한** 대화 상자에서 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="eb9a9-125">**사용자 그룹 추가/편집** 대화 상자에서 사용자 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="eb9a9-126">각 필드에 정보를 입력 하 여 도메인과 그룹을 입력할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="eb9a9-127">완료 되 면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-127">When you finish, click **OK**.</span></span> <span data-ttu-id="eb9a9-128">같은 페이지를 사용 하 여 다른 그룹을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="eb9a9-129">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-129">Click **Next**.</span></span>

11. <span data-ttu-id="eb9a9-130">**요약** 화면에서 가져오기 설정을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="eb9a9-131">**마침을** 클릭 하 여 응용 프로그램을 추가 하 고 **뒤로** 를 클릭 하 여 정보를 변경 하거나 **취소**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9a9-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="eb9a9-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="eb9a9-132">Related topics</span></span>


[<span data-ttu-id="eb9a9-133">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="eb9a9-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





