---
title: MED-V 관리 콘솔 사용자 인터페이스 사용
description: MED-V 관리 콘솔 사용자 인터페이스 사용
author: dansimp
ms.assetid: f42714d7-6f0c-4995-ab31-d4ef0845a22c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22fc98c3edbea48847e1a00369bea21a470e66b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825848"
---
# <span data-ttu-id="5b84b-103">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="5b84b-103">Using the MED-V Management Console User Interface</span></span>


<span data-ttu-id="5b84b-104">콘솔 사용자 인터페이스는 다음 섹션으로 나뉘어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-104">The console user interface is divided into the following sections:</span></span>

-   <span data-ttu-id="5b84b-105">다음 **med-v 관리 단추**는 다음 세 모듈에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-105">The following **MED-V management buttons**, which correspond to the three modules:</span></span>

    -   <span data-ttu-id="5b84b-106">**정책**— **정책** 모듈은 med-v 작업 영역과 관련 설정 및 사용 권한을 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-106">**Policy**—The **Policy** module is used to define the MED-V workspaces and their related settings and permissions.</span></span>

    -   <span data-ttu-id="5b84b-107">**이미지**- **이미지** 모듈은 med-v 작업 영역 이미지를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-107">**Images**—The **Images** module is used to manage MED-V workspace images.</span></span>

    -   <span data-ttu-id="5b84b-108">**보고서**- **보고서** 모듈은 med-v 작업 영역 보고서를 생성 하 고 보는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-108">**Reports**—The **Reports** module is used for generating and viewing MED-V workspace reports.</span></span>

-   <span data-ttu-id="5b84b-109">**도구 모음** 에는 선택한 단추와 관련 된 바로 가기가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-109">The **toolbar** displays shortcuts relevant to the button selected.</span></span>

-   <span data-ttu-id="5b84b-110">**표시 창** 에는 선택한 단추에 해당 하는 모듈이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-110">The **display pane** displays a module corresponding to the button that is selected.</span></span>

![](images/medv-ui-console-general.gif)

## <span data-ttu-id="5b84b-111">MED-V 관리 콘솔에 로그인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="5b84b-111">How to Log In to the MED-V Management Console</span></span>


**<span data-ttu-id="5b84b-112">MED-V 관리 콘솔을 열려면</span><span class="sxs-lookup"><span data-stu-id="5b84b-112">To open the MED-V management console</span></span>**

-   <span data-ttu-id="5b84b-113">Windows **시작** 메뉴에서 모든 프로그램을 선택 합니다. \*\* &gt; med-v &gt; 관리\*\*또는 바탕 화면에서 med-v 관리 아이콘을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-113">On the Windows **Start** menu, select **All Programs &gt; MED-V &gt; MED-V Management**, or on the desktop, double-click the MED-V Management icon.</span></span>

    <span data-ttu-id="5b84b-114">**Med-v 관리 로그인** 창이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-114">The **MED-V Management Login** window appears.</span></span>

<span data-ttu-id="5b84b-115">**참고**  보안상의 이유로 MED-V 관리 콘솔에 로그인 하는 첫 번째 사용자는 해당 컴퓨터의 유일한 사용자가 되어 관리 콘솔에 액세스할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-115">**Note** For security reasons, the first user to log in to the MED-V management console will become the only user on that computer allowed to access the management console.</span></span>

 

**<span data-ttu-id="5b84b-116">로그인 하려면</span><span class="sxs-lookup"><span data-stu-id="5b84b-116">To log in</span></span>**

1.  <span data-ttu-id="5b84b-117">도메인 사용자 자격 증명을 다음 형식으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-117">Type in your domain user credentials in the following format:</span></span>

    <span data-ttu-id="5b84b-118">"domain \ _name \\user\ _name", "password"</span><span class="sxs-lookup"><span data-stu-id="5b84b-118">"domain\_name\\user\_name", "password"</span></span>

    <span data-ttu-id="5b84b-119">**참고**  서버를 구성할 때 읽기 전용 액세스 권한이 있는 사용자는 물론 모든 권한을 가진 사용자가 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-119">**Note** When configuring the server, users with full access as well as users with read-only access are defined.</span></span> <span data-ttu-id="5b84b-120">모든 사용자는 도메인 사용자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-120">All users must be domain users.</span></span> <span data-ttu-id="5b84b-121">도메인 사용자 이름 및 암호는 MED-V 관리 로그인에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-121">The domain user name and password is used for MED-V management login.</span></span>

     

2.  <span data-ttu-id="5b84b-122">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-122">Click **OK**.</span></span>

    <span data-ttu-id="5b84b-123">**Med-v 관리** 콘솔이 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="5b84b-123">The **MED-V Management** console appears.</span></span>

## <span data-ttu-id="5b84b-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5b84b-124">Related topics</span></span>


[<span data-ttu-id="5b84b-125">MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="5b84b-125">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

 

 





