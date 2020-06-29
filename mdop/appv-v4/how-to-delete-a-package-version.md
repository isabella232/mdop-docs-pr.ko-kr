---
title: 패키지 버전을 삭제하는 방법
description: 패키지 버전을 삭제하는 방법
author: dansimp
ms.assetid: a55adb9d-ffa6-4df3-a2d1-5e0c73c35e1b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc77e60ac9745033ae8f074ae71db0cb8517a202
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817563"
---
# <span data-ttu-id="bbbff-103">패키지 버전을 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="bbbff-103">How to Delete a Package Version</span></span>


<span data-ttu-id="bbbff-104">응용 프로그램 가상화 서버 관리 콘솔에서 여러 버전이 있는 패키지에 대해 다음 절차를 사용 하 여 하나 이상의 버전을 삭제 하 고 나머지 패키지 버전을 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-104">From the Application Virtualization Server Management Console, for a package that has multiple versions, you can use the following procedure to delete one or more versions and still stream the remaining versions of the package.</span></span> <span data-ttu-id="bbbff-105">서버에서 파일을 보다 효율적으로 관리 하거나 오래 된 버전을 제거 하기 위해이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-105">You might do this to more effectively manage files on the server or to remove an obsolete version.</span></span>

<span data-ttu-id="bbbff-106">**참고**  버전을 삭제 하도록 선택 하면 클라이언트 컴퓨터가 사용할 수 있다는 것을 확인 상자에 알려 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-106">**Note** When you choose to delete a version, a confirmation box reminds you that client computers might still be using it.</span></span> <span data-ttu-id="bbbff-107">사용 중인 버전을 제거 하기 전에 사용자에 게 모든 응용 프로그램을 종료 하 고 언로드해야 한다는 것을 조언 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-107">You should advise users to exit and unload any applications before you remove a version that is in use.</span></span>

 

**<span data-ttu-id="bbbff-108">패키지 버전을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="bbbff-108">To delete a package version</span></span>**

1.  <span data-ttu-id="bbbff-109">Application Virtualization Server 관리 콘솔의 왼쪽 패널에서 **패키지**를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-109">In the left panel of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

2.  <span data-ttu-id="bbbff-110">삭제 하려는 버전이 포함 된 패키지를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-110">Click the package that contains the version you want to delete.</span></span>

3.  <span data-ttu-id="bbbff-111">가운데 창에서 삭제 하려는 패키지의 버전을 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-111">In the center pane, right-click the version of the package you want to delete and choose **Delete**.</span></span>

4.  <span data-ttu-id="bbbff-112">확인 창을 읽고 **예** 를 클릭 하 여 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-112">Read the confirmation window, and click **Yes** to complete the action.</span></span>

    <span data-ttu-id="bbbff-113">**참고**  연결이 끊긴 작업에 사용자가 있는 경우 해당 응용 프로그램은 다음에 서버에 연결할 때 새 버전으로 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-113">**Note** If you have users in disconnected operation, their applications will be replaced with the new versions the next time they connect to the servers.</span></span> <span data-ttu-id="bbbff-114">모든 사용자가 응용 프로그램을 업데이트 한 후에는 이전 버전을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbbff-114">After you are sure all users have updated applications, you can delete old versions.</span></span>

     

## <span data-ttu-id="bbbff-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bbbff-115">Related topics</span></span>


[<span data-ttu-id="bbbff-116">패키지를 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="bbbff-116">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="bbbff-117">Server Management Console에서 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="bbbff-117">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





