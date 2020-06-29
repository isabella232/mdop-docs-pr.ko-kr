---
title: 다른 SQL Server로 App-V SQL 데이터베이스를 마이그레이션하는 방법
description: 다른 SQL Server로 App-V SQL 데이터베이스를 마이그레이션하는 방법
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817073"
---
# <span data-ttu-id="fb959-103">다른 SQL Server로 App-V SQL 데이터베이스를 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="fb959-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="fb959-104">다음 절차에서는 App-v (Microsoft Application Virtualization) 관리 서버의 SQL 데이터베이스를 다른 SQL Server로 마이그레이션하는 방법에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="fb959-105">**중요**  이 절차를 수행 하려면 App-v 서버 서비스가 중지 되어 최종 사용자가 해당 응용 프로그램을 사용 하지 못하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="fb959-106">App-v SQL 데이터베이스를 백업 하려면</span><span class="sxs-lookup"><span data-stu-id="fb959-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="fb959-107">서비스 .msc 프로그램을 열고 마이그레이션할 데이터베이스를 사용 하는 모든 관리 서버에서 App-v 관리 서버 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="fb959-108">App-v 데이터베이스가 있는 컴퓨터에서 SQL Server Management Studio를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="fb959-109">**데이터베이스** 노드를 확장 하 여 app-v 데이터베이스를 찾습니다 (기본 이름은 APPVIRT입니다).</span><span class="sxs-lookup"><span data-stu-id="fb959-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="fb959-110">데이터베이스를 마우스 오른쪽 단추로 클릭 하 고 **작업** 을 선택한 다음 **백업을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="fb959-111">**복구 모델이** **SIMPLE** 으로 설정 되어 있고 **백업 유형이** **Full**로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="fb959-112">필요한 경우 **백업 집합과** **대상** 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="fb959-113">**확인** 을 클릭 하 여 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="fb959-114">백업이 성공적으로 완료 되 면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="fb959-115">Windows 탐색기를 열고 데이터베이스 백업 파일 (예: APPVIRT)이 포함 된 폴더를 찾습니다. K.</span><span class="sxs-lookup"><span data-stu-id="fb959-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="fb959-116">데이터베이스 백업 파일을 SQL Server를 실행 하는 대상 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="fb959-117">대상 컴퓨터로 App-v SQL 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="fb959-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="fb959-118">대상 컴퓨터에서 SQL Server Management Studio를 열고 **데이터베이스** 노드를 마우스 오른쪽 단추로 클릭 하 고 **데이터베이스 복원을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="fb959-119">**복원할 원본**에서 **장치에서** 를 선택한 다음 "**...**"를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="fb959-120">단추를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-120">button.</span></span>

3.  <span data-ttu-id="fb959-121">**백업 지정** 대화 상자에서 **백업 미디어가** **파일로** 설정 되어 있는지 확인 한 다음 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="fb959-122">SQL Server를 실행 하는 원래 컴퓨터에서 복사한 백업 파일을 선택한 다음 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="fb959-123">**확인** 을 클릭 한 다음 복원에 대 한 백업 집합을 클릭 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="fb959-124">**복원할 대상**에서 **데이터베이스에** 대 한 드롭다운을 클릭 하 고 app-v 데이터베이스 이름 (예: APPVIRT을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="fb959-125">**확인** 을 클릭 하 여 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="fb959-126">복원이 성공적으로 완료 되 면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="fb959-127">**보안** 노드를 확장 하 고 **로그인** 을 마우스 오른쪽 단추로 클릭 한 다음 **새 로그인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="fb959-128">**로그인 이름** 필드에 DOMAIN\\SERVERNAME $의 형식으로 App-v 관리 서버에 대 한 네트워크 서비스 계정 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="fb959-129">**기본 데이터베이스** 아래의 **일반** 페이지에서 app-v 데이터베이스 이름 (예: APPVIRT)을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="fb959-130">**페이지 선택**에서 **사용자 매핑** 페이지를 클릭 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="fb959-131">**이 로그인에 매핑된 사용자**에서 **지도** 열의 확인란을 클릭 하 여 app-v 데이터베이스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="fb959-132">\*\*데이터베이스 역할 구성원: &lt; Appvdatabasename &gt; \*\*에서 **SFTEveryone** 을 클릭 하 여 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="fb959-133">SQL Server를 실행 하는 새 컴퓨터의 Windows 방화벽이 App-v 관리 서버에서 시스템에 액세스할 수 있도록 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="fb959-134">**관리 도구**아래에서 **고급 보안이 포함 된 Windows 방화벽** 프로그램을 사용 하 여 SQL Server에서 사용 되는 포트에 대 한 **인바운드 규칙** 을 만듭니다 (기본값은 포트 1433).</span><span class="sxs-lookup"><span data-stu-id="fb959-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="fb959-135">App-v SQL Server 에이전트 작업을 마이그레이션하려면</span><span class="sxs-lookup"><span data-stu-id="fb959-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="fb959-136">SQL Server를 실행 하는 원래 컴퓨터의 SQL server Management Studio에서 **Sql Server 에이전트** 노드를 확장 한 다음 **작업** 노드를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="fb959-137">다음 4 개의 App-v 작업을 마우스 오른쪽 단추로 클릭 하 고 작업 스크립트를 선택 합니다. \*\* 만들기 | 파일\*\*을 열고 각 스크립트를 폴더에 저장 하 고 각 스크립트에 설명적인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="fb959-138">Appvdbname (Softgrid 데이터베이스) 사용 내역 확인</span><span class="sxs-lookup"><span data-stu-id="fb959-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="fb959-139">Appvdbname (Softgrid 데이터베이스) 고아 세션 닫기</span><span class="sxs-lookup"><span data-stu-id="fb959-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="fb959-140">Appvdbname (Softgrid 데이터베이스) 크기 제한 적용</span><span class="sxs-lookup"><span data-stu-id="fb959-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="fb959-141">Appvdbname (Softgrid 데이터베이스)의 알림/작업 상태 모니터링</span><span class="sxs-lookup"><span data-stu-id="fb959-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="fb959-142">4 개의 스크립트 파일 (.sql)을 SQL Server를 실행 하는 대상 컴퓨터에 복사 하 고 SQL Server Management Studio를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="fb959-143">Windows 탐색기에서 각 .sql 파일을 마우스 오른쪽 단추로 클릭 한 다음 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="fb959-144">각 스크립트는 SQL Server Management Studio의 쿼리 창에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="fb959-145">각 스크립트에 대해 **실행** 을 클릭 하 고 각 스크립트가 성공적으로 완료 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="fb959-146">**SQL Server 에이전트** 노드에서 **작업** 노드를 새로 고치고 4 개의 작업이 성공적으로 생성 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="fb959-147">App-v 관리 서버의 구성을 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="fb959-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="fb959-148">App-v 관리 서버에서 다음 레지스트리 키를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="fb959-149">**Sqlservername**  =  &lt; newservername&gt;</span><span class="sxs-lookup"><span data-stu-id="fb959-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="fb959-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="fb959-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="fb959-151">그런 다음 App-v 서버 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="fb959-152">App-V 관리 서버 설치 디렉터리 아래에 있는 파일을 찾아서 찾습니다 (기본값은 C:\\program files Files\\Microsoft System Center App Virt Management Server\\App Virt 관리 서비스).</span><span class="sxs-lookup"><span data-stu-id="fb959-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="fb959-153">파일을 마우스 오른쪽 단추로 클릭 하 고 **열기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="fb959-154">**연결** 탭에서 SQL Server를 실행 하는 대상 컴퓨터의 이름을 입력 한 다음 **연결 테스트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="fb959-155">테스트에 성공 하면 **확인** 을 클릭 한 다음 **확인** 을 다시 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="fb959-156">4.5 SP2 이전의 App-v 관리 서버 버전의 경우 SQL 로깅 설정을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="fb959-157">**서버 그룹**에서 서버가 구성원으로 속해 있는 서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="fb959-158">**로깅** 탭에서 **SQL 데이터베이스** 항목을 클릭 하 여 선택한 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="fb959-159">**DNS 호스트 이름을** SQL Server를 실행 하는 새 컴퓨터의 호스트 이름으로 변경한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="fb959-160">**확인** 을 두 번 클릭 한 다음 app-v 서버 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="fb959-161">App-v 관리 콘솔을 열고 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새로 고침**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="fb959-162">응용 프로그램 목록은 이전과 같이 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb959-162">The list of applications should be displayed as before.</span></span>

 

 





