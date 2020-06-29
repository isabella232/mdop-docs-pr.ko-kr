---
title: 로그인 시 게시 새로 고침을 설정하는 방법
description: 로그인 시 게시 새로 고침을 설정하는 방법
author: dansimp
ms.assetid: 196448db-7645-4fd5-a854-ef6405b15db4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd131ab5acbb8224e60077dfcc4272d4aa132b5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816558"
---
# <span data-ttu-id="720fb-103">로그인 시 게시 새로 고침을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="720fb-103">How to Set Up Publishing Refresh on Login</span></span>


<span data-ttu-id="720fb-104">다음 절차를 사용 하 여 컴퓨터에 로그인 할 때마다 서버에서 게시 정보를 새로 고치도록 Application Virtualization (App-v) 클라이언트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-104">You can use the following procedure to configure the Application Virtualization (App-V) Client to refresh the publishing information from the server each time you log in to the computer.</span></span> <span data-ttu-id="720fb-105">클라이언트가 구성 되 면 새로 고침 작업이 자동으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-105">After the client is configured, the refresh operation is automatic.</span></span>

**<span data-ttu-id="720fb-106">로그인에서 게시 정보를 새로 고치려면</span><span class="sxs-lookup"><span data-stu-id="720fb-106">To refresh the publishing information on login</span></span>**

1.  <span data-ttu-id="720fb-107">**범위** 창에서 **서버 게시** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-107">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="720fb-108">**결과** 창에서 원하는 서버를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-108">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="720fb-109">**속성** 대화 상자의 **새로 고침** 탭에서 **사용자 로그인에서 구성 서버 새로 고침** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-109">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration server on user login** check box.</span></span>

4.  <span data-ttu-id="720fb-110">구성을 변경 하려면 **적용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-110">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="720fb-111">설정 구성을 완료 하면 **확인** 을 클릭 하 여 대화 상자를 종료 하 고 Application Virtualization Management Console로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-111">When you finish configuring the settings, click **OK** to exit the dialog box and return to the Application Virtualization Management Console.</span></span>

    <span data-ttu-id="720fb-112">이제 시스템에 로그인 할 때마다 게시 정보가 새로 고쳐질 것입니다.</span><span class="sxs-lookup"><span data-stu-id="720fb-112">The publishing information will now be refreshed each time you log in to the system.</span></span>

## <span data-ttu-id="720fb-113">관련 항목</span><span class="sxs-lookup"><span data-stu-id="720fb-113">Related topics</span></span>


[<span data-ttu-id="720fb-114">Application Virtualization Client Management Console에서 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="720fb-114">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





