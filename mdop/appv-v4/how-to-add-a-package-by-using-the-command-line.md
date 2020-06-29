---
title: 명령줄을 사용하여 패키지를 추가하는 방법
description: 명령줄을 사용하여 패키지를 추가하는 방법
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821408"
---
# <span data-ttu-id="8009b-103">명령줄을 사용하여 패키지를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="8009b-103">How to Add a Package by Using the Command Line</span></span>


<span data-ttu-id="8009b-104">다음 절차에서는 가상 응용 프로그램 패키지를 특정 컴퓨터의 App-v (Application Virtualization) 클라이언트에 추가 하는 데 필요한 단계를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-104">The following procedures list the steps that are necessary to add a virtual application package to the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="8009b-105">특정 사용자에 대 한 가상 응용 프로그램 패키지를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="8009b-105">To add a virtual application package for a specific user</span></span>**

-   <span data-ttu-id="8009b-106">패키지를 받을 사람의 사용자 계정에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-106">Run the following command under the user account of the person who is to get the package.</span></span> <span data-ttu-id="8009b-107">이 명령은 해당 사용자의 패키지를 추가 하 고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-107">The command adds and publishes the package for that user.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**<span data-ttu-id="8009b-108">모든 사용자에 대 한 가상 응용 프로그램 패키지를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="8009b-108">To add a virtual application package for all users</span></span>**

-   <span data-ttu-id="8009b-109">관리자 권한이 있는 계정으로 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-109">Run the following command under an account that has administrator rights.</span></span> <span data-ttu-id="8009b-110">컴퓨터의 모든 사용자에 대해 패키지가 추가 되 고 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-110">The package is added and published for all users on the computer.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**<span data-ttu-id="8009b-111">전자 소프트웨어 배포 시스템을 사용 하 여 패키지를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="8009b-111">To add a package using an electronic software distribution system</span></span>**

1.  <span data-ttu-id="8009b-112">컴퓨터의 **시스템** 계정에서 명령을 실행 하는 전자 소프트웨어 배포 시스템을 사용 하는 경우/tglobal 스위치를 사용 하지 않는 한 해당 계정에 대해서만 패키지가 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-112">If you are using an electronic software distribution system that runs the commands under the computer’s **SYSTEM** account, the package is published for that account only, unless you use the /GLOBAL switch.</span></span> <span data-ttu-id="8009b-113">다음 명령을 실행 하 여 컴퓨터의 모든 사용자에 대 한 패키지를 추가 하 고 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-113">Run the following command to add and publish the package for all users on the computer:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    <span data-ttu-id="8009b-114">특정 사용자에 대해서만 패키지를 추가 하려면 **패키지 추가** 명령을 실행 한 다음 각 사용자의 사용자 계정 아래에서 다음 **게시 패키지** 명령을 실행 하 여 각 사용자에 대 한 패키지를 명시적으로 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-114">If you want to add the package for specific users only, run the **ADD PACKAGE** command, and then explicitly publish the package for each user by running the following **PUBLISH PACKAGE** command under each person’s user account:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    <span data-ttu-id="8009b-115">전역 매개 변수 없이 패키지를 게시 하면 패키지의 응용 프로그램에 대 한 액세스 권한이 사용자에 게 부여 되 고 매니페스트에 나열 된 파일 형식과 바로 가기가 사용자의 프로필에 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-115">Publishing the package without the GLOBAL parameter grants the user access to the applications in the package and publishes the file types and shortcuts that are listed in the manifest to the user’s profile.</span></span> <span data-ttu-id="8009b-116">필요한 사용 권한은 "파일 형식 연결 관리" (**ManageTypes**) 및 "**바로 가기 게시" (게시**안 됨)입니다.</span><span class="sxs-lookup"><span data-stu-id="8009b-116">Permissions required are “Manage file type associations” (**ManageTypes**) and “Publish shortcuts” (**PublishShortcut**).</span></span>

## <span data-ttu-id="8009b-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8009b-117">Related topics</span></span>


[<span data-ttu-id="8009b-118">명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="8009b-118">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[<span data-ttu-id="8009b-119">명령줄을 사용하여 패키지를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="8009b-119">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





