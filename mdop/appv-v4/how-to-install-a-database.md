---
title: 데이터베이스 설치 방법
description: 데이터베이스 설치 방법
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817378"
---
# <span data-ttu-id="31496-103">데이터베이스 설치 방법</span><span class="sxs-lookup"><span data-stu-id="31496-103">How to Install a Database</span></span>


<span data-ttu-id="31496-104">데이터베이스를 아직 사용할 수 없는 경우 다음 절차를 사용 하 여 응용 프로그램 가상화의 서버 기반 배포를 위해 데이터베이스를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31496-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="31496-105">일반적으로 프로덕션 환경에서는 기존 데이터베이스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="31496-106">**중요**  데이터베이스를 설치 하려면 적절 한 사용 권한이 있는 네트워크 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="31496-107">조직에서 데이터베이스 관리자만 데이터베이스 업그레이드를 만들고 수행할 수 있도록 요구 하는 경우에는이 작업을 수행할 수 있는 스크립트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31496-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="31496-108">데이터베이스를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="31496-108">To install a database</span></span>**

1.  <span data-ttu-id="31496-109">네트워크에서 응용 프로그램 가상화 시스템 설정 프로그램의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 **Setup.exe**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="31496-110">**시작 페이지**에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="31496-111">사용권 **계약** 페이지에서 사용권 계약에 동의 하는 경우 **동의 함을**선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="31496-112">**정보 등록** 페이지에서 **사용자 이름** 및 **조직** 정보를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="31496-113">**설치 유형** 페이지에서 **사용자 지정** 을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="31496-114">**사용자 지정 설정** 페이지에서 **응용 프로그램 가상화 서버**를 제외한 모든 application virtualization 시스템 구성 요소를 선택 취소 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="31496-115">**참고**  컴퓨터에 이미 설치 되어 있는 구성 요소는 **사용자 지정 설정** 화면에서 선택을 취소 하 여 자동으로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31496-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="31496-116">**데이터베이스 서버** 페이지에서 암호를 입력 하 고, 설치 경로를 지정 하 고, 정보를 저장 하 고, **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="31496-117">데이터베이스의 이름을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="31496-118">**참고**  이 단계를 완료 하려고 할 때 오류 25109이 표시 되 면 데이터베이스를 설치 하는 데 필요한 사용 권한을 잘못 설정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="31496-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="31496-119">필요한 SQL 권한을 설정 하는 방법에 대 한 자세한 내용은을 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="31496-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="31496-120">**디렉터리 서버** 화면에서 응용 프로그램 가상화 서버와 관리 웹 서비스가 도메인 컨트롤러에 액세스 하는 데 사용할 도메인 이름과 자격 증명을 입력 하 고 다음 정보를 저장 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="31496-121">**참고**  현재 컴퓨터의 도메인이 기본값으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31496-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="31496-122">**관리자 그룹** 페이지에서 관리자 권한을 가지는 그룹의 이름을 입력 하 고이 정보를 저장 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="31496-123">**참고**  관리 권한을 부여할 그룹 이름의 처음 몇 개의 문자를 입력 하 고 다음을 클릭 한 **다음** **관리자 그룹 선택** 화면의 결과 목록에서 그룹을 선택 해도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31496-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="31496-124">그런 다음이 정보를 저장 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="31496-125">**기본 공급자 그룹** 페이지에서 응용 프로그램에 대 한 액세스를 제어 하는 그룹의 전체 이름을 입력 하 고이 정보를 저장 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="31496-126">**참고**  또한 응용 프로그램에 대 한 액세스를 제어 하는 그룹 이름의 처음 몇 글자를 입력 하 고 **다음**을 클릭 한 다음 **기본 공급자 그룹 선택** 화면의 목록에서 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="31496-127">그런 다음이 정보를 저장 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="31496-128">**설치 마법사 완료** 페이지에서 마법사를 닫으려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="31496-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="31496-129">**중요**  설치를 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31496-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="31496-130">상태 메시지가 Windows 바탕 화면 알림 영역 위에 깜박입니다. 설치에 성공 했는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="31496-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="31496-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="31496-131">Related topics</span></span>


[<span data-ttu-id="31496-132">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="31496-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





