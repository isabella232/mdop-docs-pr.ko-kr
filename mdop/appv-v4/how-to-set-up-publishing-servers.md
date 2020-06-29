---
title: 게시 서버를 설정하는 방법
description: 게시 서버를 설정하는 방법
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816528"
---
# <span data-ttu-id="25bab-103">게시 서버를 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="25bab-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="25bab-104">다음 절차를 사용 하 여 클라이언트 관리 콘솔에서 직접 Application Virtualization Server를 추가 하 고 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="25bab-105">응용 프로그램 게시 서버를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="25bab-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="25bab-106">**결과** 창에서 팝업 메뉴를 마우스 오른쪽 단추로 클릭 하 고 새 **서버** 를 선택 하 여 새 Application Virtualization server 마법사를 시작 하거나, **게시 서버** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **새 서버** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="25bab-107">마법사의 페이지 1에서 **표시 이름** 필드에 서버 이름을 입력 하 고 **유형** 드롭다운 목록에서 서버 유형을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="25bab-108">서버 유형의 드롭다운 목록에서 **응용 프로그램 가상화 서버**, **향상 된 보안 응용 프로그램 가상화 서버**, **표준 HTTP 서버**또는 **향상 된 보안 HTTP 서버** 를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="25bab-109">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-109">Click **Next**.</span></span>

4.  <span data-ttu-id="25bab-110">마법사의 2 페이지에서 **호스트 이름** 및 **포트** 필드에 적절 한 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="25bab-111">**Path** 필드는 Application Virtualization 서버에 대해 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="25bab-112">표준 HTTP 서버 또는 향상 된 보안 HTTP 서버에 대 한 경로를 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="25bab-113">**마침을** 클릭 하 여 서버를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="25bab-114">응용 프로그램 게시 서버를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="25bab-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="25bab-115">**결과** 창에서 원하는 서버를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="25bab-116">서버 이름을 변경할 수 있는 **일반** 탭을 클릭 하 고 서버 유형의 드롭다운 목록에서 유형을 선택한 다음 호스트 이름 및 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="25bab-117">서버 종류가 표준 HTTP 서버 또는 향상 된 보안 HTTP 서버인 경우 **경로** 필드도 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="25bab-118">**새로 고침** 탭을 클릭 하 고 **사용자 로그인 시 게시 새로 고침** 확인란이 기본적으로 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="25bab-119">새로 고침 빈도를 변경 하려면 **게시 새로 고침 간격** 확인란을 선택 하 고 필드의 빈도를 나타내는 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="25bab-120">그런 다음 드롭다운 메뉴에서 **분**, **시간**, **일** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="25bab-121">(입력할 수 있는 최소 시간은 30 분입니다.)</span><span class="sxs-lookup"><span data-stu-id="25bab-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="25bab-122">구성을 변경 하려면 **적용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="25bab-123">게시가 완료 되 면 **확인** 을 클릭 하 여 대화 상자를 종료 하 고 클라이언트 관리 콘솔로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="25bab-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="25bab-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="25bab-124">Related topics</span></span>


[<span data-ttu-id="25bab-125">연결이 끊긴 작업 모드 설정을 사용 중지하거나 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="25bab-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





