---
title: 응용 프로그램에 대한 액세스를 거부하는 방법
description: 응용 프로그램에 대한 액세스를 거부하는 방법
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817518"
---
# <span data-ttu-id="a5a11-103">응용 프로그램에 대한 액세스를 거부하는 방법</span><span class="sxs-lookup"><span data-stu-id="a5a11-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="a5a11-104">응용 프로그램을 로드 하 고 사용 하려면 사용자가 응용 프로그램의 **액세스 권한** 목록에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="a5a11-105">응용 프로그램 가상화 서버 관리 콘솔은 응용 프로그램에 대 한 사용자 그룹 액세스를 명시적으로 거부 하는 것을 지원 하지 않지만,이를 위해 응용 프로그램의 속성에서 사용자 그룹을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="a5a11-106">응용 프로그램에 대 한 액세스를 거부 하려면</span><span class="sxs-lookup"><span data-stu-id="a5a11-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="a5a11-107">기존 응용 프로그램의 경우 왼쪽 창에서 **응용 프로그램** 노드를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="a5a11-108">오른쪽 창에서 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="a5a11-109">그런 다음 **액세스 권한** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="a5a11-110">사용자 그룹에 대 한 액세스 권한을 제거 하려면 사용자 그룹을 강조 표시 하 고 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="a5a11-111">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-111">Click **OK**.</span></span>

    <span data-ttu-id="a5a11-112">**참고**  응용 프로그램에 대 한 액세스를 제어 하기 위해 응용 프로그램 라이선스를 제한할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="a5a11-113">Active Directory 도메인 서비스에서 적절 한 사용자 그룹을 설정 하면 특정 사용자 집합에 대 한 액세스 권한을 부여 하 고 거부 하는 가장 쉬운 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a11-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="a5a11-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a5a11-114">Related topics</span></span>


[<span data-ttu-id="a5a11-115">응용 프로그램에 대한 액세스를 허용하는 방법</span><span class="sxs-lookup"><span data-stu-id="a5a11-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="a5a11-116">Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="a5a11-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="a5a11-117">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="a5a11-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





