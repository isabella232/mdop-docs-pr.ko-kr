---
title: 응용 프로그램에 대한 액세스를 허용하는 방법
description: 응용 프로그램에 대한 액세스를 허용하는 방법
author: dansimp
ms.assetid: e54d9e84-21f5-488f-b040-25f374d9289f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9cd3dfe4661f09bb7e7d3514a397955cb892be81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817433"
---
# <span data-ttu-id="78265-103">응용 프로그램에 대한 액세스를 허용하는 방법</span><span class="sxs-lookup"><span data-stu-id="78265-103">How to Grant Access to an Application</span></span>


<span data-ttu-id="78265-104">관리자는 응용 프로그램 가상화 서버 관리 콘솔을 사용 하 여 어떤 사용자가 어떤 응용 프로그램에 액세스할 수 있는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78265-104">As the administrator, you can use the Application Virtualization Server Management Console to determine which users can access which applications.</span></span> <span data-ttu-id="78265-105">이 작업은 응용 프로그램의 **속성** 대화 상자를 사용 하 여 언제 든 지 Sequencer 프로젝트 (SPRJ) 또는 OSD (개방형 소프트웨어 설명자) 파일을 가져올 때 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78265-105">You can do this when you import the Sequencer Project (SPRJ) or Open Software Descriptor (OSD) file or at anytime using the application's **Properties** dialog box.</span></span> <span data-ttu-id="78265-106">두 방법 모두 **액세스 권한** 옵션을 사용 하 여 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-106">With both methods, use the **Access Permissions** options to add users.</span></span>

**<span data-ttu-id="78265-107">응용 프로그램에 대 한 액세스 권한을 부여 하려면</span><span class="sxs-lookup"><span data-stu-id="78265-107">To grant access to an application</span></span>**

1.  <span data-ttu-id="78265-108">기존 응용 프로그램의 경우 왼쪽 창에서 **응용 프로그램** 노드를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-108">For an existing application, click the **Applications** node in the left pane.</span></span> <span data-ttu-id="78265-109">오른쪽 창에서 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-109">Right-click an application in the right pane, and choose **Properties**.</span></span>

2.  <span data-ttu-id="78265-110">**액세스 권한** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-110">Select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="78265-111">사용자 그룹을 추가 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-111">To add user groups, click **Add**.</span></span>

4.  <span data-ttu-id="78265-112">**사용자 그룹 추가/편집** 대화 상자에서 사용자 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-112">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="78265-113">각 필드에 정보를 입력 하 여 도메인과 그룹을 입력할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78265-113">You can also enter the domain and group by typing the information in the respective fields.</span></span>

5.  <span data-ttu-id="78265-114">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-114">Click **OK**.</span></span> <span data-ttu-id="78265-115">같은 페이지를 사용 하 여 다른 그룹을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78265-115">You can add other groups with the same pages.</span></span>

6.  <span data-ttu-id="78265-116">마법사가 다시 나타나면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-116">When the wizard reappears, click **OK**.</span></span>

    <span data-ttu-id="78265-117">**참고**  응용 프로그램에 대 한 액세스 권한을 부여 하기 전에 Active Directory 도메인 서비스에서 그룹을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78265-117">**Note** You must set up your groups in Active Directory Domain Services before you attempt to grant access to applications.</span></span>

     

## <span data-ttu-id="78265-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="78265-118">Related topics</span></span>


[<span data-ttu-id="78265-119">응용 프로그램에 대한 액세스를 거부하는 방법</span><span class="sxs-lookup"><span data-stu-id="78265-119">How to Deny Access to an Application</span></span>](how-to-deny-access-to-an-application.md)

[<span data-ttu-id="78265-120">Server Management Console에서 응용 프로그램 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="78265-120">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="78265-121">Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="78265-121">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="78265-122">수동으로 응용 프로그램을 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="78265-122">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





