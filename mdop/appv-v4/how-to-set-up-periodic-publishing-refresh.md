---
title: 정기적인 게시 새로 고침을 설정하는 방법
description: 정기적인 게시 새로 고침을 설정하는 방법
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816553"
---
# <span data-ttu-id="90390-103">정기적인 게시 새로 고침을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="90390-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="90390-104">다음 절차를 사용 하 여 클라이언트에서 App-v 서버의 게시 정보를 정기적으로 새로 고치도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90390-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="90390-105">클라이언트가 구성 되 면 새로 고침 작업이 자동으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90390-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="90390-106">이러한 설정은이 컴퓨터의 모든 사용자가 동일한 설정을 볼 수 있도록 클라이언트에 대 한 기본 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90390-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="90390-107">**참고**  이 절차를 수행한 후에는 로그인 시 첫 번째 새로 고침 이후 새 설정에 따라 게시 정보가 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="90390-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="90390-108">이 첫 번째 새로 고침이 발생 하면 서버는 구성 방법에 따라 컴퓨터 설정을 다른 설정으로 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90390-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="90390-109">**속성** 대화 상자에 있는 **새로 고침** 탭에는 로컬로 구성 된 클라이언트 컴퓨터 설정 및 게시 서버에서 사용자에 게 구성 했을 수 있는 설정이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90390-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="90390-110">응용 프로그램 가상화 서버의 게시 정보를 정기적으로 새로 고치려면</span><span class="sxs-lookup"><span data-stu-id="90390-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="90390-111">**범위** 창에서 **서버 게시** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="90390-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="90390-112">**결과** 창에서 원하는 서버를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="90390-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="90390-113">**속성** 대화 상자의 **새로 고침** 탭에서 **구성 새로 고침 간격** 확인란을 선택 하 고 필드의 빈도를 나타내는 숫자를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="90390-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="90390-114">그런 다음 드롭다운 메뉴에서 **분**, **시간**, **일** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="90390-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="90390-115">**참고**  이 설정을 통해 클라이언트는 구성 된 기간이 경과할 때마다 게시 정보를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="90390-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="90390-116">새로 고침을 수행할 때 사용자가 로그인 하지 않으면 사용자가 다음에 로그인 할 때 새로 고침이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90390-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="90390-117">그러면 타이머가 다음 기간 동안 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90390-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="90390-118">구성을 변경 하려면 **적용** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="90390-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="90390-119">서버 구성을 마쳤으면 **확인** 을 클릭 하 여 대화 상자를 종료 하 고 응용 프로그램 가상화 클라이언트 관리 콘솔로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="90390-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="90390-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="90390-120">Related topics</span></span>


[<span data-ttu-id="90390-121">Application Virtualization Client Management Console에서 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="90390-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





