---
title: 독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법
description: 독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813972"
---
# <span data-ttu-id="5373d-103">독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="5373d-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="5373d-104">다음 절차를 사용 하 여 독립 실행형 컴퓨터에 보고 서버를 설치 하 고 데이터베이스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="5373d-105">**중요** 다음 절차를 수행 하기 전에 [app-v 5.1 보고에 대해](about-app-v-51-reporting.md)읽고 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="5373d-106">독립 실행형 컴퓨터에 보고 서버를 설치 하 고 데이터베이스에 연결 하려면</span><span class="sxs-lookup"><span data-stu-id="5373d-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="5373d-107">설치 하려는 컴퓨터에 App-v 5.1 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="5373d-108">App-v 5.1 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="5373d-109">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-109">Click **Install**.</span></span>

2. <span data-ttu-id="5373d-110">**시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="5373d-111">**Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="5373d-112">Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="5373d-113">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-113">Click **Next**.</span></span>

4. <span data-ttu-id="5373d-114">**기능 선택** 페이지에서 **보고 서버** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="5373d-115">**설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="5373d-116">**기존 보고 데이터베이스 구성** 페이지에서 **원격 SQL server 사용**을 선택 하 고 Microsoft SQL server를 실행 하는 컴퓨터의 컴퓨터 이름 (예: **SqlServerMachine**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5373d-117">Microsoft SQL Server가 같은 서버에 배포 된 경우 **로컬 Sql Server 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="5373d-118">SQL Server 인스턴스의 경우 **기본 인스턴스 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="5373d-119">사용자 지정 Microsoft SQL Server 인스턴스를 사용 하는 경우 **사용자 지정 인스턴스 사용** 을 선택한 다음 인스턴스의 이름을 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="5373d-120">이 보고 서버에서 사용할 **SQL Server 데이터베이스 이름** (예: **AppvReporting**)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="5373d-121">" **보고 서버 구성 구성** " 페이지</span><span class="sxs-lookup"><span data-stu-id="5373d-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="5373d-122">보고 서비스에 사용할 웹 사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="5373d-123">사용자 지정 이름이 없는 경우 기본값을 변경 하지 않고 그대로 둡니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="5373d-124">**포트 바인딩에**대해 app-v 5.1 (예: **55555**)에서 사용 되는 고유 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="5373d-125">또한 지정한 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="5373d-126">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-126">Click **Install**.</span></span>

**<span data-ttu-id="5373d-127">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="5373d-127">Got an App-V issue?</span></span>** <span data-ttu-id="5373d-128">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5373d-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5373d-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5373d-129">Related topics</span></span>

[<span data-ttu-id="5373d-130">App-V 5.1 보고 정보</span><span class="sxs-lookup"><span data-stu-id="5373d-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="5373d-131">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="5373d-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="5373d-132">PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="5373d-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
