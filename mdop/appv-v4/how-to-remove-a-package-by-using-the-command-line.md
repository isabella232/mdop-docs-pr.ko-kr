---
title: 명령줄을 사용하여 패키지를 제거하는 방법
description: 명령줄을 사용하여 패키지를 제거하는 방법
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816823"
---
# <span data-ttu-id="f601e-103">명령줄을 사용하여 패키지를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="f601e-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="f601e-104">다음 명령줄 프로시저를 사용 하 여 특정 컴퓨터의 App-v (Application Virtualization) 클라이언트에서 가상 응용 프로그램 패키지를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="f601e-105">모든 사용자의 가상 응용 프로그램 패키지를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="f601e-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="f601e-106">이전에/CGLOBAL 스위치를 사용 하 여 모든 사용자에 대해 패키지가 추가 된 경우 다음 명령을 사용 하 여 패키지와 전역 파일 형식 및 바로 가기를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="f601e-107">관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-107">Administrator rights are required.</span></span> <span data-ttu-id="f601e-108">이 명령은 항상 패키지의 전역 삭제를 수행 하므로이 경우/TGLOBAL 스위치가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="f601e-109">개별 사용자에 대해 이전에 추가 된 패키지를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="f601e-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="f601e-110">이전에 개별 사용자에 대해 패키지가 추가 된 경우 여러 가지 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="f601e-111">패키지가 게시 된 각 사용자의 사용자 계정에서 다음 명령을 한 번 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="f601e-112">이렇게 하면 사용자가 다른 컴퓨터로 로밍 하는 경우 응용 프로그램에 대 한 액세스가 거부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="f601e-113">프로필에서 특정 사용자의 설정, 바로 가기 및 파일 형식을 삭제 하 고 사용자의 컨텍스트 아래에서 백그라운드 로드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="f601e-114">또는 패키지가 게시 된 각 사용자의 사용자 계정에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="f601e-115">그런 다음 패키지에 대해이 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="f601e-116">이렇게 하면 패키지가 완전히 제거 되 고 해당 프로필에서 모든 사용자 설정, 바로 가기 및 파일 형식이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="f601e-117">이후 패키지가 다시 추가 되는 경우 사용자는 해당 설정을 다시 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="f601e-118">이 명령을 실행 하려면 "응용 프로그램 삭제" (**Deleteapp**) 권한만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="f601e-119">세 번째 방법으로 **패키지 게시 취소** 명령을 사용 하지 않고 **패키지 삭제** 명령을 간단히 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="f601e-120">이 경우 각 사용자의 파일 형식 및 바로 가기가 삭제 되지 않고 숨겨지고 사용자 설정이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="f601e-121">즉, 나중에 사용자를 위해 패키지가 다시 추가 되 면 파일 형식 및 바로 가기가 복원 되 고 사용자 설정이 다시 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f601e-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="f601e-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f601e-122">Related topics</span></span>


[<span data-ttu-id="f601e-123">명령줄을 사용하여 패키지를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="f601e-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="f601e-124">명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="f601e-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





