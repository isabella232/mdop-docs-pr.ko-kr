---
title: App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법
description: App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817933"
---
# <span data-ttu-id="ac09e-103">App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="ac09e-103">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>


<span data-ttu-id="ac09e-104">다음 절차를 사용 하 여 microsoft SQL Server 데이터베이스 미러링을 사용 하도록 Microsoft Application Virtualization (App-v) 환경을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-104">You can use the following procedure to configure your Microsoft Application Virtualization (App-V) environment to use Microsoft SQL Server database mirroring.</span></span> <span data-ttu-id="ac09e-105">데이터베이스 미러링을 구성 하면 재해 복구 및 장애 조치 시나리오에 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-105">Configuring database mirroring can help with disaster recovery and failover scenarios.</span></span> <span data-ttu-id="ac09e-106">App-v 4.5 SP2는 현재 Microsoft SQL Server 2005 및 SQL Server 2008에서 사용할 수 있는 모든 데이터베이스 미러링 모드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-106">App-V 4.5 SP2 supports all modes of database mirroring currently available for Microsoft SQL Server 2005 and SQL Server 2008.</span></span>

**<span data-ttu-id="ac09e-107">참고</span><span class="sxs-lookup"><span data-stu-id="ac09e-107">Note</span></span>**  
<span data-ttu-id="ac09e-108">이 절차는 Microsoft SQL Server를 사용 하 여 SQL Server 데이터베이스 및 데이터베이스 미러링을 설정 하 고 구성 하는 데 익숙한 관리자를 위해 작성 되었으며, 따라서 App-v에 고유한 특정 구성 설정만 다룹니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-108">This procedure is written for administrators who are familiar with setting up and configuring SQL Server databases and database mirroring with Microsoft SQL Server, and therefore covers only the specific configuration settings that are unique to App-V.</span></span>



**<span data-ttu-id="ac09e-109">Microsoft SQL Server 데이터베이스 미러링을 사용 하도록 앱-V 환경을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="ac09e-109">To configure your App-V environment to use Microsoft SQL Server database mirroring</span></span>**

1.  <span data-ttu-id="ac09e-110">데이터베이스 미러링에 대 한 표준 비즈니스 지침에 따라 App-v 데이터베이스의 SQL Server 데이터베이스 미러링을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-110">Set up SQL Server database mirroring of the App-V database following your standard business practices for database mirroring.</span></span> <span data-ttu-id="ac09e-111">Microsoft SQL Server 데이터베이스 미러링 구현에 대 한 일반적인 정보를 보려면 다음 링크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-111">Use the following links for general information about implementing Microsoft SQL Server database mirroring:</span></span>

    -   <span data-ttu-id="ac09e-112">**MICROSOFT SQL 2005**—[데이터베이스 미러링 설정](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span><span class="sxs-lookup"><span data-stu-id="ac09e-112">**Microsoft SQL 2005**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span></span>

    -   <span data-ttu-id="ac09e-113">**MICROSOFT SQL 2008**—[데이터베이스 미러링 설정](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span><span class="sxs-lookup"><span data-stu-id="ac09e-113">**Microsoft SQL 2008**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span></span>

    <span data-ttu-id="ac09e-114">또한 최상의 방법 정보는 [데이터베이스 미러링 모범 사례 및 성능 고려 사항](https://go.microsoft.com/fwlink/?LinkId=190270) ()에서 확인할 수 있습니다 https://go.microsoft.com/fwlink/?LinkId=190270) .</span><span class="sxs-lookup"><span data-stu-id="ac09e-114">In addition, you can find Best Practices information in [Database Mirroring Best Practices and Performance Considerations](https://go.microsoft.com/fwlink/?LinkId=190270) (https://go.microsoft.com/fwlink/?LinkId=190270).</span></span>

2.  <span data-ttu-id="ac09e-115">미러링이 설정 된 후에는 App-v 데이터베이스가 상태 **(주도자, 동기화 됨)** 를 표시 하 고 미러된 데이터베이스에 상태 **(미러, 동기화 됨/복원 중)** 가 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-115">After mirroring has been set up, verify that the App-V database shows a status of **(Principal, Synchronized)**, and the mirrored database shows a status of **(Mirror, Synchronized / Restoring)**.</span></span> <span data-ttu-id="ac09e-116">다음 단계를 진행 하기 전에 모든 미러링 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-116">Resolve any mirroring issues before proceeding to the next step.</span></span> <span data-ttu-id="ac09e-117">상태 모니터링에 대 한 자세한 내용은 [미러링 상태 모니터링](https://go.microsoft.com/fwlink/?LinkId=190279) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=190279) .</span><span class="sxs-lookup"><span data-stu-id="ac09e-117">For additional information about monitoring the status, see [Monitoring Mirroring Status](https://go.microsoft.com/fwlink/?LinkId=190279) (https://go.microsoft.com/fwlink/?LinkId=190279).</span></span>

3.  <span data-ttu-id="ac09e-118">App-v 데이터베이스의 미러를 호스트 하는 sql server 컴퓨터에서 계정 이름 \*\* &lt; 도메인 &gt; \\ &lt; managementserverhostname &gt; $ \*\*을 사용 하 여 app-v 관리 서버의 네트워크 서비스 계정에 대 한 SQL Server 로그인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-118">On the SQL Server computer that hosts the mirror of the App-V database, create the SQL Server Login for the network service account of the App-V Management Server by using the account name **&lt;domain&gt;\\&lt;ManagementServerHostName&gt;$**.</span></span>

4.  <span data-ttu-id="ac09e-119">Microsoft SQL Server 네이티브 클라이언트를 App-v 관리 서버에 설치 하 고, 다른 컴퓨터에 설치 되어 있는 경우 App-v 관리 웹 서비스를 실행 하는 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-119">Install the Microsoft SQL Server Native Client on the App-V Management Server, and on the computer running the App-V Management Web Service if installed on a different computer.</span></span> <span data-ttu-id="ac09e-120">부하 분산을 위해 추가 App-v 관리 서버를 미러된 SQL 데이터베이스에 연결 하려는 경우 해당 컴퓨터에도 Microsoft SQL Server 기본 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-120">If you plan to have additional App-V Management Servers connect to the mirrored SQL database for load balancing, you must install the Microsoft SQL Server Native Client on those computers as well.</span></span> <span data-ttu-id="ac09e-121">Microsoft [sql server 2008 기능 팩](https://go.microsoft.com/fwlink/?LinkId=187479) 페이지의 Microsoft 다운로드 센터 ()에서 Microsoft Sql Server 기본 클라이언트를 다운로드할 수 있습니다 https://go.microsoft.com/fwlink/?LinkId=187479) .</span><span class="sxs-lookup"><span data-stu-id="ac09e-121">You can download the Microsoft SQL Server Native Client from the [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) page in the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=187479).</span></span>

5.  <span data-ttu-id="ac09e-122">레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** 을 확인 하 고 SQL Server의 호스트 이름만 포함 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-122">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerName** and make sure that it contains only the host name of the SQL Server.</span></span> <span data-ttu-id="ac09e-123">인스턴스 이름 (예: *serverhostname\\instancename*을 포함 하는 경우 인스턴스 이름을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-123">If it includes an instance name, for example *serverhostname\\instancename*, the instance name must be removed.</span></span>

    **<span data-ttu-id="ac09e-124">중요</span><span class="sxs-lookup"><span data-stu-id="ac09e-124">Important</span></span>**  
    <span data-ttu-id="ac09e-125">데이터베이스 미러링이 사용 되는 경우 App-v 관리 서버는 TCP/IP 네트워킹 라이브러리를 사용 하 여 SQL Server와 통신 하므로 인스턴스 이름을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-125">The App-V Management Server uses the TCP/IP networking library to communicate with the SQL Server when database mirroring is enabled, and therefore instance names cannot be used.</span></span> <span data-ttu-id="ac09e-126">포트 번호는 대신 레지스트리 키에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-126">The port numbers must be specified in the registry keys instead.</span></span>



6.  <span data-ttu-id="ac09e-127">레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** 을 확인 하 고 sql Server 컴퓨터의 sql에 사용 되는 포트 번호가 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-127">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerPort** and make sure that it contains the port number that is used for SQL on the SQL Server computer.</span></span> <span data-ttu-id="ac09e-128">명명 된 인스턴스를 사용 하는 경우이 키 값을 명명 된 인스턴스에 사용 되는 포트로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-128">If you are using a named instance this key value must be set to the port that is used for the named instance.</span></span>

7.  <span data-ttu-id="ac09e-129">레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\MICROSOFT\\SOFTGRID\\4.5\\SERVER\\SQLFAILOVERSERVERNAME** REG \ _SZ으로 만든 다음 해당 값을 미러를 호스팅하는 SQL Server의 호스트 이름으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-129">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerName** as REG\_SZ and then set the value to the host name of the SQL Server that hosts the mirror.</span></span>

8.  <span data-ttu-id="ac09e-130">레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\MICROSOFT\\SOFTGRID\\4.5\\SERVER\\SQLFAILOVERSERVERPORT** DWORD로 만든 다음 해당 값을 sql Server를 실행 하는 컴퓨터의 sql에서 미러를 호스팅하기 위해 사용 하는 포트 번호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-130">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerPort** as DWORD and then set the value to the port number that is used for SQL on the computer that is running SQL Server to host the mirror.</span></span> <span data-ttu-id="ac09e-131">미러에 대해 명명 된 인스턴스를 사용 하는 경우이 키 값은 명명 된 인스턴스에 사용 되는 포트 번호로 설정 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-131">If you are using a named instance for the mirror this key value must be set to the port number that is used for the named instance.</span></span>

9.  <span data-ttu-id="ac09e-132">앱-V 관리 웹 서비스를 실행 하는 컴퓨터에서 UDL (유니버설 데이터 링크) 텍스트 파일을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-132">On the computer that is running the App-V Management Web Service, configure the Universal Data Link (UDL) text file.</span></span> <span data-ttu-id="ac09e-133">App-v가 설치 된 디렉터리에서 **Sftmgmt** 를 두 번 클릭 하 고 다음 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-133">In the directory where App-V is installed, double-click **SftMgmt.udl** and specify the following values:</span></span>

    -   <span data-ttu-id="ac09e-134">**공급자** 탭에서 OLE DB 공급자 **SQL Server Native Client 10.0**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-134">On the **Provider** tab, select the OLE DB provider **SQL Server Native Client 10.0**.</span></span>

    -   <span data-ttu-id="ac09e-135">**다음** 을 클릭 하 여 **연결** 탭을 선택 합니다. **서버 이름** 상자에 SQL server의 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-135">Click **Next** to select the **Connection** tab. In the **Server Name** box, enter the server name of the SQL Server.</span></span> <span data-ttu-id="ac09e-136">다음으로, **WINDOWS NT의 통합 보안 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-136">Next, select **Use Windows NT Integrated Security**.</span></span> <span data-ttu-id="ac09e-137">마지막으로 목록을 클릭 하 여 **데이터베이스를 선택한**다음 app-v 데이터베이스 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-137">Finally, click the list **Select the database**, and then select the App-V database name.</span></span>

    -   <span data-ttu-id="ac09e-138">**모두** 탭을 클릭 한 다음 항목 **장애 조치 파트너**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-138">Click the **All** tab, and then select the entry **Failover Partner**.</span></span> <span data-ttu-id="ac09e-139">**값 편집**을 클릭 한 다음 장애 조치 SQL server의 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-139">Click **Edit Value**, and then enter the server name of the failover SQL Server.</span></span> <span data-ttu-id="ac09e-140">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-140">Click **OK**.</span></span>

    **<span data-ttu-id="ac09e-141">중요</span><span class="sxs-lookup"><span data-stu-id="ac09e-141">Important</span></span>**  
    <span data-ttu-id="ac09e-142">App-v 시스템은 Kerberos 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-142">The App-V system uses Kerberos authentication.</span></span> <span data-ttu-id="ac09e-143">따라서 sql Server에서 Kerberos 인증을 사용 하도록 설정 하 고 도메인 사용자 계정에서 SQL Server 서비스를 실행 하는 SQL 미러링을 구성할 때는 수동으로 SPN을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-143">Therefore, when you configure SQL mirroring where Kerberos Authentication is enabled on the SQL Server and the SQL Server service runs under a domain user account, you must manually configure an SPN.</span></span> <span data-ttu-id="ac09e-144">자세한 내용은 [분산 환경에 대 한 App-v 관리 구성](https://go.microsoft.com/fwlink/?LinkId=203186) () 문서의 "SQL 서비스에서 도메인 기반 계정을 사용 하는 경우"를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=203186) .</span><span class="sxs-lookup"><span data-stu-id="ac09e-144">For more information, see “When SQL Service Uses Domain-Based Account” in the article [Configuring App-V Administration for a Distributed Environment](https://go.microsoft.com/fwlink/?LinkId=203186) (https://go.microsoft.com/fwlink/?LinkId=203186).</span></span>



10. <span data-ttu-id="ac09e-145">데이터베이스 미러링이 제대로 실행 되 고 있는지 확인 하려면 장애 조치를 테스트 하 고 App-v 관리 서버가 계속 올바르게 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-145">To verify that database mirroring is running correctly, test the failover and confirm that the App-V Management Server continues to function correctly.</span></span>

    **<span data-ttu-id="ac09e-146">중요</span><span class="sxs-lookup"><span data-stu-id="ac09e-146">Important</span></span>**  
    <span data-ttu-id="ac09e-147">주의를 기울여, 표준 비즈니스 관행에 따라 오류가 발생 했을 때 시스템 작업이 중단 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac09e-147">Proceed with care, and follow your standard business practices to ensure that system operations are not disrupted in the event of a failure.</span></span>



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## <span data-ttu-id="ac09e-148">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ac09e-148">Related topics</span></span>


[<span data-ttu-id="ac09e-149">Application Virtualization Server Management Console에서 관리 작업을 수행하는 방법</span><span class="sxs-lookup"><span data-stu-id="ac09e-149">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









