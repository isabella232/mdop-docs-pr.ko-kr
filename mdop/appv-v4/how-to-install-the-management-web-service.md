---
title: Management Web Service 설치 방법
description: Management Web Service 설치 방법
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817278"
---
# <span data-ttu-id="7f24b-103">Management Web Service 설치 방법</span><span class="sxs-lookup"><span data-stu-id="7f24b-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="7f24b-104">로컬 관리자 권한이 있는 로그온 계정으로 네트워크의 대상 컴퓨터에 응용 프로그램 가상화 관리 웹 서비스를 설치 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="7f24b-105">필요 하지는 않지만 웹 서버에이 구성 요소를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="7f24b-106">관리 웹 서비스를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="7f24b-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="7f24b-107">대상 컴퓨터에 이전 버전의 Application Virtualization 웹 서비스가 설치 되어 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="7f24b-108">네트워크에서 응용 프로그램 가상화 시스템 설정 프로그램의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 **Setup.exe**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="7f24b-109">설치 마법사가 열리면 **시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="7f24b-110">사용권 **계약** 페이지에서 사용권 계약에 동의 하는 경우 **동의 함을**선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="7f24b-111">**등록 정보** 페이지에서 **사용자 이름** 및 조직 정보를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="7f24b-112">**설치 유형** 페이지에서 **사용자 지정**을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="7f24b-113">**참고**  이 컴퓨터에 설치 된 첫 번째 구성 요소가 아닌 경우 **프로그램 유지 관리** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="7f24b-114">**프로그램 유지 관리** 페이지에서 **수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="7f24b-115">**사용자 지정 설정** 페이지에서 **App Virt 관리 서비스**를 제외한 모든 응용 프로그램 가상화 시스템 구성 요소를 선택 취소 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="7f24b-116">**참고**  컴퓨터에 이미 설치 되어 있는 구성 요소를 제거 하 여 **사용자 지정 설정** 페이지에서 선택 취소 하면 자동으로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="7f24b-117">**데이터베이스 서버** 페이지에서 **사용 가능한 데이터베이스에 연결**을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="7f24b-118">**참고**  프로덕션 환경에서 Microsoft는 기존 데이터베이스에 연결 하는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="7f24b-119">데이터베이스를 설치 하려는 경우 데이터베이스를 설치 하 [는 방법을](how-to-install-a-database.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f24b-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="7f24b-120">데이터베이스를 설치한 후 13 단계로 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="7f24b-121">**데이터베이스 서버 유형** 페이지의 목록에서 데이터베이스 유형을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="7f24b-122">**데이터베이스 서버 위치** 페이지의 사용 가능한 서버 목록에서 데이터베이스 서버를 선택 하 고 **다음 호스트 이름 사용** 확인란을 선택 하 고 **서버 이름** 및 **포트 번호** 상자에 정보를 입력 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="7f24b-123">**데이터베이스 선택** 페이지에서 원하는 데이터베이스를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="7f24b-124">**데이터베이스 사용자 구성** 페이지에서 관리 웹 서비스가 데이터 저장소에 액세스 하는 데 사용할 자격 증명을 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="7f24b-125">프로그램을 **수정할 준비가 되었습니다** 페이지에서 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="7f24b-126">**참고**  첫 번째 구성 요소를 설치 하는 경우 **프로그램을 설치할 준비가** 되었습니다 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="7f24b-127">페이지에서 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="7f24b-128">**설치 마법사 완료** 페이지에서 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f24b-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="7f24b-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7f24b-129">Related topics</span></span>


[<span data-ttu-id="7f24b-130">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="7f24b-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





