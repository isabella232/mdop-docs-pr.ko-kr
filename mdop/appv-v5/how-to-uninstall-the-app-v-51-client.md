---
title: App-V 5.1 Client 제거 방법
description: App-V 5.1 Client 제거 방법
author: dansimp
ms.assetid: 21f2d946-fc9f-4cd3-899b-ac52b3fbc306
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9338bef6b8a3123f9b8f49036427121987e7aa9f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813657"
---
# <span data-ttu-id="8fd71-103">App-V 5.1 Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="8fd71-103">How to Uninstall the App-V 5.1 Client</span></span>


<span data-ttu-id="8fd71-104">컴퓨터에서 Microsoft App-v (Application Virtualization) 5.1 클라이언트를 제거 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-104">Use the following procedure to uninstall the Microsoft Application Virtualization (App-V) 5.1 client from a computer.</span></span> <span data-ttu-id="8fd71-105">App-v 5.1 클라이언트를 제거 하면 클라이언트를 실행 하는 컴퓨터에 게시 된 모든 패키지도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-105">When you uninstall the App-V 5.1 client all packages published to the computer running the client are also removed.</span></span> <span data-ttu-id="8fd71-106">제거 작업이 완료 되지 않은 경우에는 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 패키지를 다시 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-106">If the uninstall operation does not complete the packages will need to be re-published to the computer running the App-V 5.1 client.</span></span>

**<span data-ttu-id="8fd71-107">중요</span><span class="sxs-lookup"><span data-stu-id="8fd71-107">Important</span></span>**  
<span data-ttu-id="8fd71-108">제거 절차를 수행 하기 전에 App-v 5.1 클라이언트 서비스가 실행 되 고 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-108">You should ensure that the App-V 5.1 client service is running prior to performing the uninstall procedure.</span></span>



**<span data-ttu-id="8fd71-109">App-v 5.1 클라이언트를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="8fd71-109">To uninstall the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="8fd71-110">제어판에서 프로그램 제거 프로그램을 두 **번 클릭 한**  /  **Uninstall a Program**다음 **Microsoft Application Virtualization 클라이언트**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-110">In Control Panel, double-click **Programs** / **Uninstall a Program**, and then double-click **Microsoft Application Virtualization Client**.</span></span>

2.  <span data-ttu-id="8fd71-111">표시 되는 대화 상자에서 **예** 를 클릭 하 여 제거 프로세스를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-111">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    **<span data-ttu-id="8fd71-112">중요</span><span class="sxs-lookup"><span data-stu-id="8fd71-112">Important</span></span>**  
    <span data-ttu-id="8fd71-113">제거 프로세스는 취소 또는 중단할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-113">The uninstall process cannot be canceled or interrupted.</span></span>



3.  <span data-ttu-id="8fd71-114">진행률 표시줄에 남은 시간이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="8fd71-115">이 단계가 완료 되 면 제거 프로세스를 완료 하기 위해 모든 관련 드라이버를 중지할 수 있도록 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd71-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    **<span data-ttu-id="8fd71-116">참고</span><span class="sxs-lookup"><span data-stu-id="8fd71-116">Note</span></span>**  
    <span data-ttu-id="8fd71-117">명령줄을 사용 하 여 다음 스위치를 사용 하 여 App-v 5.1 클라이언트를 제거할 수도 **있습니다.**</span><span class="sxs-lookup"><span data-stu-id="8fd71-117">You can also use the command line to uninstall the App-V 5.1 client with the following switch: **/UNINSTALL**.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="8fd71-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8fd71-118">Related topics</span></span>


[<span data-ttu-id="8fd71-119">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="8fd71-119">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









