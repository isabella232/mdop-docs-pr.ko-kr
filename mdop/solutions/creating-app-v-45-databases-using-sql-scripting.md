---
title: SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기
description: SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825978"
---
# <span data-ttu-id="802c8-103">SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="802c8-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="802c8-104">이 솔루션의 용도는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="802c8-104">Who is this solution intended for?</span></span>** <span data-ttu-id="802c8-105">App-v (Application Virtualization) 4.5 데이터베이스를 관리 하는 정보 기술 전문가입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="802c8-106">이 가이드는 어떤 도움을 하나요?</span><span class="sxs-lookup"><span data-stu-id="802c8-106">How can this guide help you?</span></span>** <span data-ttu-id="802c8-107">이 솔루션에서는 관리자가 설치 될 때 SQL Server에 대 한 "sysadmin" 권한이 없는 경우 Microsoft Application Virtualization 서버를 설치 하는 절차에 대해 설명 하 고 문서화 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="802c8-108">개요</span><span class="sxs-lookup"><span data-stu-id="802c8-108">Overview</span></span>


<span data-ttu-id="802c8-109">Microsoft Application Virtualization 4.5 (App-v)을 설치 하는 경우의 문제 중 하나는 설치 프로그램에서 서버 기능을 설치 하는 사용자가 로컬 컴퓨터 관리자 뿐만 아니라 데이터 저장소를 호스팅할 SQL server에 대 한 SQL 관리자 권한이 있는 것으로 가정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="802c8-110">이 요구 사항은 설치의 일부로 데이터베이스와 적절 한 역할 및 권한이 모두 생성 된다는 사실에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="802c8-111">그러나 대부분의 기업은 SQL server가 App-v를 설치할 인프라 팀과 별도로 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="802c8-112">이러한 보안 요구 사항은 인프라 관리자에 게 App-v의 적절 한 권한을 설치 하는 SQL 관리자의 액세스를 어렵게 만드는 것입니다. 마찬가지로, SQL 관리자에 게는 인프라 팀을 위해 제품을 설치 하는 데 필요한 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="802c8-113">현재 App-v 설치를 시도 하는 관리자에 게는 SQL "sysadmin" 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="802c8-114">이전 버전의 제품에서는 "sysadmin" 권한이 있는 자격 증명을 제공 하기 위해 SQL 관리자가 임시 "sysadmin" 계정을 만들거나 설치 중에 나타날 수 있도록 설정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="802c8-115">이 릴리스에서 스크립트는 해당 인프라를 구현할 때 모든 관리자가 사용할 수 있도록 출시 된 제품에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="802c8-116">이 백서에서는 설치를 별도의 두 가지 작업으로 나누고 (SQL 데이터베이스 만들기 및 App-v server 기능 설치) 시나리오에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="802c8-117">SQL 관리자는 SQL 스크립트를 검토 하 고 다른 데이터베이스와의 충돌을 해결 하거나 다른 도구와의 통합을 지원 하기 위해 수정 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="802c8-118">이 스크립트의 결과는 인프라 관리자가 SQL server에 고급 권한을 부여할 필요가 없도록 SQL 관리자가 데이터베이스를 준비할 수 있도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="802c8-119">이는 보안 정책이이를 금지 하는 환경에서 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="802c8-120">SQL 데이터베이스 만들기 프로세스</span><span class="sxs-lookup"><span data-stu-id="802c8-120">SQL Database Creation Process</span></span>

<span data-ttu-id="802c8-121">Sql 스크립트를 사용 하 여 SQL 관리자는 필요한 데이터베이스를 만들고, 환경을 성공적으로 설치 하 고 관리 하기 위해 App-v 관리자에 대 한 권한을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="802c8-122">이러한 작업을 완료 하는 단계는이 문서의 뒷부분에 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="802c8-123">이 프로세스는 실제 App-v 설치와 데이터베이스 만들기 및 구성 작업을 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="802c8-124">SQL 관리자에 게 제공 되는 정보</span><span class="sxs-lookup"><span data-stu-id="802c8-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="802c8-125">App-v 관리자가 될 광고 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="802c8-126">App-v 관리 서버가 설치 될 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="802c8-127">인프라 관리자에 게 반환 되는 정보</span><span class="sxs-lookup"><span data-stu-id="802c8-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="802c8-128">데이터베이스 서버 또는 인스턴스의 이름과 App-v 데이터베이스의 이름</span><span class="sxs-lookup"><span data-stu-id="802c8-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="802c8-129">데이터베이스를 준비한 후에는 App-v 관리자가 SQL 관리자 권한 없이 App-v 설치를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="802c8-130">SQL 설치 스크립트 사용</span><span class="sxs-lookup"><span data-stu-id="802c8-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="802c8-131">요구 사항</span><span class="sxs-lookup"><span data-stu-id="802c8-131">Requirements</span></span>**

<span data-ttu-id="802c8-132">다음은 선택한 추출 위치 루트의 support\\createdb 폴더에 있는 스크립트를 사용 하기 위한 요구 사항 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="802c8-133">스크립트는 실행 되는 컴퓨터의 쓰기 가능한 위치 (복사한 후 이러한 스크립트에서 읽기 전용 특성을 제거 해야 함)로 복사 되 고 해당 컴퓨터에 SQL 클라이언트 도구가 로드 되어야 합니다 (osql은 로컬 컴퓨터에서 예제 배치 파일을 실행 하는 데만 필요 함).</span><span class="sxs-lookup"><span data-stu-id="802c8-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="802c8-134">SQL Server는 Windows 인증을 지원 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="802c8-135">SQL Server 인스턴스와 SQL 에이전트 서비스가 실행 중인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="802c8-136">스크립트가 수행 될 컴퓨터의 SQL 관리자 (sysadmin) 인 도메인 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="802c8-137">스크립트는 로그온 한 사용자의 도메인 자격 증명으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="802c8-138">SQL 스크립트를 사용 하 여 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="802c8-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="802c8-139">SQL 관리자가 수행할 작업:</span><span class="sxs-lookup"><span data-stu-id="802c8-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="802c8-140">선택 된 추출 위치의 루트에서 support\\createdb 폴더에 포함 된 스크립트를 스크립트가 실행 될 컴퓨터로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="802c8-141">다음 파일은 스크립트를 올바르게 실행 하는 데 필요 하며 아래에 표시 된 순서 대로 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="802c8-142">데이터베이스 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-142">database.sql</span></span>

    -   <span data-ttu-id="802c8-143">역할 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-143">roles.sql</span></span>

    -   <span data-ttu-id="802c8-144">테이블 \ _CODES</span><span class="sxs-lookup"><span data-stu-id="802c8-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="802c8-145">함수 \ _before \ _tables. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="802c8-146">테이블 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-146">tables.sql</span></span>

    -   <span data-ttu-id="802c8-147">함수 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-147">functions.sql</span></span>

    -   <span data-ttu-id="802c8-148">보기 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-148">views.sql</span></span>

    -   <span data-ttu-id="802c8-149">프로시저 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-149">procedures.sql</span></span>

    -   <span data-ttu-id="802c8-150">트리거 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-150">triggers.sql</span></span>

    -   <span data-ttu-id="802c8-151">데이터 \ _codes. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="802c8-152">데이터 \ _messages. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="802c8-153">데이터 \ _defaults. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="802c8-154">알림 \ _jobs. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="802c8-155">dbversion .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-155">dbversion.sql</span></span>

2.  <span data-ttu-id="802c8-156">필요한 경우 파일을 검토 하 고 수정 `database.sql` 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="802c8-157">기본 설정은 데이터베이스 이름을 "APPVIRTDB"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="802c8-158">필요한 경우 사용 되는의 인스턴스를 대체 합니다 `APPVIRTDB` `database name` .</span><span class="sxs-lookup"><span data-stu-id="802c8-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="802c8-159">데이터베이스를 `FILENAME` 만들 SQL Server의 적절 한 경로를 사용 하 여 스크립트의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="802c8-160">필요한 경우 `database name [APPVIRTDB]` `roles.sql` 데이터베이스 .sql 파일에서 사용 된 파일을 검토 하 고 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="802c8-161">일괄 처리 파일을 사용 하 여 프로세스를 자동화 하는 방법의 예</span><span class="sxs-lookup"><span data-stu-id="802c8-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="802c8-162">사용 하는 경우 다음 두 가지 일괄 처리 파일은 SQL 스크립트를 다음과 같은 방식으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="802c8-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="802c8-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="802c8-164">데이터베이스 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-164">database.sql</span></span>

    -   <span data-ttu-id="802c8-165">역할 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-165">roles.sql</span></span>

2.  **<span data-ttu-id="802c8-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="802c8-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="802c8-167">테이블 \ _CODES</span><span class="sxs-lookup"><span data-stu-id="802c8-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="802c8-168">함수 \ _before \ _tables. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="802c8-169">테이블 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-169">tables.sql</span></span>

    -   <span data-ttu-id="802c8-170">함수 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-170">functions.sql</span></span>

    -   <span data-ttu-id="802c8-171">보기 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-171">views.sql</span></span>

    -   <span data-ttu-id="802c8-172">프로시저 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-172">procedures.sql</span></span>

    -   <span data-ttu-id="802c8-173">트리거 .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-173">triggers.sql</span></span>

    -   <span data-ttu-id="802c8-174">데이터 \ _codes. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="802c8-175">데이터 \ _messages. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="802c8-176">데이터 \ _defaults. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="802c8-177">알림 \ _jobs. sql</span><span class="sxs-lookup"><span data-stu-id="802c8-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="802c8-178">dbversion .sql</span><span class="sxs-lookup"><span data-stu-id="802c8-178">dbversion.sql</span></span>

**<span data-ttu-id="802c8-179">참고</span><span class="sxs-lookup"><span data-stu-id="802c8-179">Note</span></span>**  
<span data-ttu-id="802c8-180">스크립트를 수정할 때는 신중 하 게 고려 하 고 적절 한 정보가 있는 사용자만이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="802c8-181">또한 샘플 파일 중에는 **create\_schema.bat**, **create\_tables.bat**, **데이터베이스 .sql**, **roles**등의 데이터만 변경 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="802c8-182">다른 모든 파일은 데이터베이스를 잘못 만들 수 있으므로 어떤 방식으로든 수정 되어서는 안 되며,이로 인해 App-v services가 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="802c8-183">두 개의 예제 배치 파일은 컴퓨터에서 나머지 SQL 스크립트를 복사한 동일한 디렉터리에 배치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="802c8-184">예제 **create\_schema.bat** 파일을 실행 하 여 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="802c8-185">이 스크립트는 완료 하는 데 몇 초 정도 소요 되며 중단 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="802c8-186">복사 된 디렉터리에서 create schema.bat 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="802c8-187">구문은 "Create\_schema.bat"입니다. `SQLSERVERNAME`</span><span class="sxs-lookup"><span data-stu-id="802c8-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="802c8-189">새 "APPVIRTDB" 데이터베이스를 만드는 동안이 스크립트에 실패 하는 경우 표시 된 대로 로그를 확인 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="802c8-190">이후 시도가 제대로 작동 하는지 확인 하기 위해 스크립트의 일부를 실행 하 여 만든 데이터베이스를 삭제 해야 할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="802c8-191">파일을 실행 `create_tables.bat` 하 여 데이터베이스에서 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="802c8-192">이 스크립트는 완료 하는 데 몇 초 정도 소요 되며 중단 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="802c8-193">복사한 디렉터리에서 create\_tables.bat 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="802c8-194">구문은 "create\_tables.bat"입니다. `SQLSERVERNAME DBNAME`</span><span class="sxs-lookup"><span data-stu-id="802c8-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![앱-v 4.6 sql create\-table.bat](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="802c8-196">테이블을 만드는 동안 스크립트가 실패 하는 경우 표시 된 대로 로그를 확인 하 여 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="802c8-197">모든 후속 시도에서 create\_tables.bat 파일을 실행 하기 전에 데이터베이스를 삭제 하 고 create\_schema.bat을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="802c8-198">App-v 데이터베이스에 대 한 사용 권한 설정</span><span class="sxs-lookup"><span data-stu-id="802c8-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="802c8-199">다음 계정은 앱-V 환경의 설치, 배포 및 진행 관리를 위해 새 데이터베이스에 대 한 특정 사용 권한 및 역할을 사용 하 여 SQL server에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="802c8-200">SQL Server의 앱-V 관리자 그룹에 대 한 로그인과 "domain\\App-V Admins" (여기서 "도메인" 및 "App-v 관리자")가 자신의 환경을 반영 하도록 변경 되 게 하 고이를 SFTAdmin 및 SFTEveryone 데이터베이스 역할에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![앱-v 4.6 sql 스크립트에서 사용 권한 및 역할 설정](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="802c8-202">전역 수준에서이 그룹에 "모든 정의 보기" 사용 권한을 부여 합니다 (이는 Microsoft Application Virtualization Management Server 설치 프로세스가 관리 서버 로그인이 이미 있는지 확인 하는 것을 허용 합니다).</span><span class="sxs-lookup"><span data-stu-id="802c8-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="802c8-203">MS-SQL 2005 이상에는 master. db에 포함 된 메타 데이터에 대 한 액세스 제한 제한이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="802c8-204">이전 단계에서 만든 사용자는 기본적으로 서버 설치에 필요한 권한을가지고 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="802c8-205">이전에 만든 로그인, 로그인 속성-Securables의 속성을 엽니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="802c8-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="802c8-206">아래 스크린샷에 표시 된 대로 데이터베이스 인스턴스를 추가 하 고 "정의 보기"에 대해 "부여"를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![app-v 4.6 sql 스크립트는 모든 def를 볼 때 perm을 허용 합니다.](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="802c8-208">이전 단계에서 만든 로그인에 대 한 역할 \ _ASSIGNMENTS 테이블에 역할을 추가 하 여 앱-V 관리자가 응용 프로그램 가상화 관리 콘솔에 액세스 하도록 허용 합니다. role = "관리자" 및 그룹 \ _ref = "domain\\App-V 관리자" ("domain" 및 "App-V 관리자"는 자신의 환경을 반영 하도록 변경 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="802c8-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![앱-v 4.6 sql 스크립트 역할 할당](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="802c8-210">관리 서버용 SQL Server 및 App-v 데이터베이스에 대 한 로그인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="802c8-211">이 계정은 Microsoft Application Virtualization 관리 서버가 데이터 저장소에 연결 하는 데 사용 되며 스트리밍된 응용 프로그램에 대 한 클라이언트 요청 서비스를 담당 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="802c8-212">SQL Server 및 관리 서버가 설치 되는 위치에 따라 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="802c8-213">관리 서버와 SQL Server가 동일한 컴퓨터에 설치 되는 경우 NT AUTHORITY\\NETWORK 서비스에 대 한 로그인을 추가 하 고 SFTUser 및 SFTEveryone 데이터베이스 역할에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="802c8-214">관리 서버 및 SQL Server를 다른 컴퓨터에 설치 하는 경우 "domain\\App-V Server Name $" ("App-v server Name")에 대 한 로그인을 추가 하 여 App-v 관리 서버가 설치 되는 서버의 이름이 며 SFTUser 및 SFTEveryone 데이터베이스 역할에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="802c8-215">SQL 창에서 쿼리 창을 열고 다음 SQL을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="802c8-216">여기에서 APPVIRTDB는 이전 단계에서 SQL Server에 만든 App-v 데이터베이스의 이름이 고, App-v Server를 설치 하려고 하는 사용자는 "domain\\App-V Admins"의 구성원 이어야 하며 (여기서 "domain" 및 "App-V 관리자"는 자신의 환경을 반영 하도록 변경 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="802c8-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="802c8-217">인프라 관리자가 수행할 작업</span><span class="sxs-lookup"><span data-stu-id="802c8-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="802c8-218">"App-V Admins" 그룹의 관리자는 App-v를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="802c8-219">SQL 관리자의 정보를 사용 하 여 이전 단계에서 만든 SQL Server 및 데이터베이스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="802c8-220">"App-v Admins" 그룹의 관리자는 응용 프로그램 가상화 관리 콘솔에 로그인 하 고 관리 콘솔에서 다음 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="802c8-221">Warning</span><span class="sxs-lookup"><span data-stu-id="802c8-221">Warning</span></span>**  
    <span data-ttu-id="802c8-222">기존 데이터베이스에 대해 설치를 실행 하는 경우 데이터베이스에서 채워지지 않은 특정 레코드를 채우기 때문에이는 일반 설정에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="802c8-223">다음 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="802c8-224">"서버 그룹"의 "기본 서버 그룹"에서 "응용 프로그램 가상화 관리 서버" 삭제</span><span class="sxs-lookup"><span data-stu-id="802c8-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="802c8-225">"서버 그룹"에서 "기본 서버 그룹" 삭제</span><span class="sxs-lookup"><span data-stu-id="802c8-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="802c8-226">"공급자 정책"에서 "Default Provider"를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="802c8-227">그러면 App-v admins 그룹의 관리자가 다음을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="802c8-228">"공급자 정책"에서 새 공급자 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="802c8-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="802c8-229">"기본 서버 그룹 만들기"</span><span class="sxs-lookup"><span data-stu-id="802c8-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="802c8-230">참고</span><span class="sxs-lookup"><span data-stu-id="802c8-230">Note</span></span>**  
        <span data-ttu-id="802c8-231">사용할 수 없는 경우에도 "기본 서버" 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="802c8-232">서버 설치 관리자는 서버를 추가 하려고 할 때 "기본 서버 그룹"만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="802c8-233">"기본 서버 그룹"이 없는 경우 설치에 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="802c8-234">적절 하지 않은 기본 서버 그룹을 사용 하는 경우에는 인프라에 후속 App-v 관리 서버를 추가 하려는 경우 "기본 서버 그룹"을 유지 하는 것이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="802c8-235">결론</span><span class="sxs-lookup"><span data-stu-id="802c8-235">Conclusion</span></span>


<span data-ttu-id="802c8-236">결론적으로이 문서의 정보를 통해 관리자는 SQL 관리자와 협력 하 여 조직의 보안 및 관리 디비전에 대해 작동 하는 배포 경로를 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="802c8-237">이 문서를 읽고 문서화 된 작업을 테스트 한 후에는 관리자가이 환경 유형에 서 App-v 인프라를 구현할 준비가 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="802c8-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









