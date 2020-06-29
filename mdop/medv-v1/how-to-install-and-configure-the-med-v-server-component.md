---
title: MED-V 서버 구성 요소를 설치 및 구성하는 방법
description: MED-V 서버 구성 요소를 설치 및 구성하는 방법
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826978"
---
# <span data-ttu-id="58034-103">MED-V 서버 구성 요소를 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="58034-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="58034-104">이 섹션에서는 MED-V 서버를 [설치](#bkmk-howtoinstallthemedvserver) 하 고 [구성](#bkmk-howtoconfigurethemedvserver) 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="58034-105">MED-V 서버를 설치 하는 방법</span><span class="sxs-lookup"><span data-stu-id="58034-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="58034-106">MED-V 서버를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="58034-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="58034-107">MED-V 서버 .msi 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="58034-108">MED-V 서버 .msi 패키지는 *MED-V\_Server\_x.msi*호출 되며 여기서 x는 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="58034-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="58034-109">예를 들어 *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="58034-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="58034-110">**InstallShield 마법사 시작** 화면이 나타나면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="58034-111">**사용권 계약** 화면에서 사용권 계약을 **읽고 동의 함을 클릭 한**후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="58034-112">기본 설치 폴더가 표시 된 **대상 폴더** 화면이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58034-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="58034-113">기본 설치 폴더는 *%Systemdrive%\\Program Files\\Microsoft Enterprise 데스크톱 Virtualization\\*입니다.</span><span class="sxs-lookup"><span data-stu-id="58034-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="58034-114">MED-V가 설치 될 폴더를 변경 하려면 **변경을** 클릭 하 고 기존 폴더를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="58034-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="58034-115">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-115">Click **Next**.</span></span>

5.  <span data-ttu-id="58034-116">**프로그램 설치 준비 완료** 화면에서 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="58034-117">MED-V 서버 설치가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58034-117">The MED-V server installation starts.</span></span> <span data-ttu-id="58034-118">이 경우 몇 분 정도 걸릴 수 있으며 화면에 텍스트가 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58034-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="58034-119">설치 중에 몇 가지 진행 화면이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58034-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="58034-120">메시지가 표시 되 면 제공 된 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="58034-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="58034-121">**InstallShield 마법사 완료** 화면이 나타나면 **마침을** 클릭 하 여 마법사를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="58034-122">참고</span><span class="sxs-lookup"><span data-stu-id="58034-122">Note</span></span>**  
<span data-ttu-id="58034-123">Microsoft 원격 데스크톱을 통해 MED-V 서버를 설치 하는 경우 다음 구문을 사용 합니다. **mstsc/admin**. RDP 세션이 콘솔로 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="58034-124">MED-V 서버를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="58034-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="58034-125">다음 서버 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58034-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="58034-126">연결</span><span class="sxs-lookup"><span data-stu-id="58034-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="58034-127">이미지</span><span class="sxs-lookup"><span data-stu-id="58034-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="58034-128">사용 권한</span><span class="sxs-lookup"><span data-stu-id="58034-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="58034-129">보고</span><span class="sxs-lookup"><span data-stu-id="58034-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="58034-130">연결 구성</span><span class="sxs-lookup"><span data-stu-id="58034-130">Configuring Connections</span></span>

**<span data-ttu-id="58034-131">연결을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="58034-131">To configure connections</span></span>**

1.  <span data-ttu-id="58034-132">Windows 시작 메뉴에서 **모든 프로그램 ( &gt; med-v &gt; Med-v-v 서버 구성 관리자**)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="58034-133">참고</span><span class="sxs-lookup"><span data-stu-id="58034-133">Note</span></span>**  
    <span data-ttu-id="58034-134">참고: 서버 설치 중에 **Med-v 서버 구성 관리자 시작** 확인란을 선택한 경우 서버 설치가 완료 되 면 med-v 서버 구성 관리자가 자동으로 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58034-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="58034-135">**연결** 탭에서 다음 클라이언트 연결 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="58034-136">**포트를 사용 하 여 암호화 되지 않은 연결 (http) 사용**-지정 된 포트를 사용 하 여 암호화 되지 않은 연결을 설정 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="58034-137">포트 상자에 암호화 되지 않은 연결 (http)을 수락할 서버 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="58034-138">**포트를 사용 하 여 암호화 된 연결 (https) 사용**-지정 된 포트를 사용 하 여 암호화 된 연결을 사용 하도록 설정 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="58034-139">포트 상자에 암호화 된 연결을 수락할 서버 포트 (https)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="58034-140">Https는 MED-V 서버와 MED-V 클라이언트 간의 보안 트랜잭션을 보장 하도록 설정할 수 있는 선택적 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="58034-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="58034-141">Https를 구성 하려면 다음 절차를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="58034-142">서버에서 인증서를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="58034-143">Netsh를 사용 하 여 서버 인증서를 지정 된 포트와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="58034-144">자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58034-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="58034-145">하이퍼텍스트 전송 프로토콜 (HTTP) 용 Netsh 명령</span><span class="sxs-lookup"><span data-stu-id="58034-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="58034-146">방법: SSL 인증서를 사용 하 여 포트 구성</span><span class="sxs-lookup"><span data-stu-id="58034-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="58034-147">방법: SSL 인증서를 사용 하 여 포트 구성</span><span class="sxs-lookup"><span data-stu-id="58034-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="58034-148">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="58034-149">이미지 구성</span><span class="sxs-lookup"><span data-stu-id="58034-149">Configuring Images</span></span>

**<span data-ttu-id="58034-150">이미지를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="58034-150">To configure images</span></span>**

1.  <span data-ttu-id="58034-151">**이미지** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="58034-152">다음과 같은 이미지 관리 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="58034-153">**Vm 디렉터리**-가상 컴퓨터 디렉터리 (이미지가 저장 되는 디렉터리)</span><span class="sxs-lookup"><span data-stu-id="58034-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="58034-154">이 필드에는 MED-V 서버에서 액세스할 수 있어야 하는 image 배포 서버의 이미지 디렉터리에 대 한 UNC 경로가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58034-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="58034-155">**VM URL**-이미지가 저장 된 서버의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="58034-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="58034-156">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="58034-157">사용 권한 구성</span><span class="sxs-lookup"><span data-stu-id="58034-157">Configuring Permissions</span></span>

**<span data-ttu-id="58034-158">사용 권한을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="58034-158">To configure permissions</span></span>**

1.  <span data-ttu-id="58034-159">**사용 권한** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="58034-160">로그인 할 수 있는 모든 사용자의 목록이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58034-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="58034-161">사용자에 게 읽기 및 쓰기 권한을 적용 하려면 사용자 옆에 있는 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="58034-162">사용자에 게 읽기 전용 권한을 적용 하려면 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="58034-163">도메인 사용자 또는 그룹을 추가 하려면 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="58034-164">**사용자 또는 그룹 이름 입력** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="58034-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="58034-165">다음 중 하나를 수행 하 여 도메인 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="58034-166">**사용자 또는 그룹 이름 입력** 필드에 도메인에 존재 하는 사용자 또는 그룹을 입력 하거나 컴퓨터의 로컬 사용자 또는 그룹으로 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="58034-167">그런 다음 **이름 확인** 을 클릭 하 여 기존 이름으로 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="58034-168">**찾기를** 클릭 하 여 표준 **사용자 또는 그룹 선택** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="58034-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="58034-169">그런 다음 도메인 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="58034-170">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-170">Click **OK**.</span></span>

4.  <span data-ttu-id="58034-171">도메인 사용자 또는 그룹을 제거 하려면 사용자 또는 그룹을 선택 하 고 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="58034-172">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="58034-173">보고서 구성</span><span class="sxs-lookup"><span data-stu-id="58034-173">Configuring Reports</span></span>

**<span data-ttu-id="58034-174">보고서를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="58034-174">To configure reports</span></span>**

1.  <span data-ttu-id="58034-175">**보고서** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="58034-176">보고서를 지원 하려면 **보고서 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="58034-177">**연결 문자열** 상자에 MSSQL 데이터베이스에 대 한 연결 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="58034-178">원격 서버에 SQL Server가 설치 되어 있는 경우 다음 연결 문자열을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="58034-179">참고</span><span class="sxs-lookup"><span data-stu-id="58034-179">Note</span></span>**  
        <span data-ttu-id="58034-180">참고: SQL Express에 연결 하려면 다음을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="58034-181">데이터베이스를 만들려면 **데이터베이스 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="58034-182">연결을 테스트 하려면 **연결 테스트**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="58034-183">데이터베이스 지우기 옵션을 구성 하려면 **지우기 옵션**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="58034-184">**데이터베이스 옵션 지우기** 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="58034-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="58034-185">다음 옵션 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="58034-186">다음 **보다 오래 된 데이터 지우기**— 지정한 날짜 수보다 이전의 모든 데이터를 지웁니다. 번호 상자에 일 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="58034-187">**데이터베이스에서 모든 데이터 지우기**-데이터베이스에서 존재 하는 모든 데이터를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="58034-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="58034-188">**데이터베이스 놓기**-데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="58034-189">**확인** 을 클릭 하 여 변경 내용을 적용 하 고 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="58034-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="58034-190">**확인** 을 클릭 하 여 변경 내용을 저장 하거나 **취소** 를 클릭 하 여 변경 내용을 저장 하지 않고 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="58034-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="58034-191">메시지가 표시 되 면 MED-V 서버 서비스를 다시 시작 하 여 네트워크 설정에 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58034-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="58034-192">관련 항목</span><span class="sxs-lookup"><span data-stu-id="58034-192">Related topics</span></span>


[<span data-ttu-id="58034-193">지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="58034-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="58034-194">MED-V 서버 인프라 디자인</span><span class="sxs-lookup"><span data-stu-id="58034-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









