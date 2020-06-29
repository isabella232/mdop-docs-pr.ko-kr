---
title: 단일 서버에서 MBAM을 설치 및 구성하는 방법
description: 단일 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824098"
---
# <span data-ttu-id="eadf3-103">단일 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="eadf3-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="eadf3-104">이 항목의 절차에서는 단일 서버에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능을 완전히 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="eadf3-105">각 서버 기능에는 특정 필수 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="eadf3-106">필수 구성 요소와 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eadf3-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="eadf3-107">또한 일부 기능에는 설치 프로세스가 기능을 성공적으로 배포 하는 동안 제공 해야 하는 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="eadf3-108">MBAM 배포를 시작 하기 전에 [mbam 1.0에 대 한 환경 준비](preparing-your-environment-for-mbam-10.md) 도 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="eadf3-109">**참고**  설치 로그 파일을 얻으려면 **msiexec** 패키지 및 **/l** 위치 옵션을 사용 하 여 mbam을 설치 해야 합니다 &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="eadf3-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="eadf3-110">로그 파일은 사용자가 지정한 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="eadf3-111">추가 설치 로그 파일은 MBAM을 설치 하는 사용자 의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="eadf3-112">단일 서버에 MBAM 서버 기능을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="eadf3-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="eadf3-113">다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="eadf3-114">**참고**  32 비트 서버와 64 비트 서버에서 64 비트 설정으로 32 비트 설치를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="eadf3-115">MBAM 서버 기능 설치를 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="eadf3-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="eadf3-116">MBAM 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="eadf3-117">시작 페이지에서 **설치** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="eadf3-118">Microsoft 소프트웨어 사용 조건을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="eadf3-119">기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="eadf3-120">같은 컴퓨터에 설치 되는 기능은 동시에 함께 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="eadf3-121">다른 곳에 설치 하려는 기능을 선택 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="eadf3-122">다음과 같은 순서로 MBAM 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="eadf3-123">복구 및 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="eadf3-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="eadf3-124">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="eadf3-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="eadf3-125">준수 감사 및 보고서</span><span class="sxs-lookup"><span data-stu-id="eadf3-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="eadf3-126">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="eadf3-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="eadf3-127">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="eadf3-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="eadf3-128">**참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="eadf3-129">모든 필수 조건이 충족 되 면 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="eadf3-130">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="eadf3-131">모든 전제 조건을 충족 하면 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="eadf3-132">네트워크 통신 보안을 구성 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="eadf3-133">MBAM은 복구 및 하드웨어 데이터베이스, 관리 및 모니터링 서버, 클라이언트 간의 통신을 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="eadf3-134">통신을 암호화 하기로 결정 한 경우, 암호화에 사용할 기관 프로 비전 된 인증서를 선택 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="eadf3-135">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="eadf3-136">MBAM 설정 마법사가 선택한 기능에 대 한 설치 페이지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="eadf3-137">MBAM 서버 기능을 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="eadf3-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="eadf3-138">**복구 및 하드웨어 데이터베이스 구성** 창에서 SQL Server 인스턴스와 복구 및 하드웨어 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="eadf3-139">또한 데이터베이스 파일 위치와 로그 정보 위치를 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="eadf3-140">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="eadf3-141">**준수 및 감사 데이터베이스 구성** 창에서 SQL Server의 인스턴스와 준수 및 감사 데이터를 저장할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="eadf3-142">그런 다음 데이터베이스 파일 위치와 로그 정보 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="eadf3-143">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="eadf3-144">**준수 및 감사 보고서** 창에서 사용할 보고서 서비스 인스턴스를 지정 하 고 데이터베이스에 액세스할 수 있는 도메인 사용자 계정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="eadf3-145">이는 특별히이 용도로 프로 비전 되는 사용자 계정 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="eadf3-146">사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="eadf3-147">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="eadf3-148">**관리 및 모니터링 서버 구성** 창에서 **포트 바인딩**, **호스트 이름** (선택 사항), Mbam 관리 및 모니터링 서버의 **설치 경로** 를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="eadf3-149">**경고가**  고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="eadf3-150">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="eadf3-151">Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="eadf3-152">Microsoft 업데이트 옵션은 Windows의 자동 업데이트를 설정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="eadf3-153">설치 마법사가 필요한 기능 정보를 수집 하면 MBAM 설치를 시작할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="eadf3-154">설치 설정을 검토 하거나 변경 하려는 경우 **뒤로** 를 클릭 하 여 마법사에서 뒤로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="eadf3-155">설치를 **클릭 하 여 설치를 시작** 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="eadf3-156">설치를 종료 하려면 **취소** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="eadf3-157">설치 프로그램이 MBAM 기능을 설치 하 고 설치가 완료 되었음을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="eadf3-158">**마침을** 클릭 하 여 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="eadf3-159">MBAM 서버 기능을 설치한 후에는 MBAM 역할에 사용자를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="eadf3-160">자세한 내용은 [MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eadf3-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="eadf3-161">설치 후 구성을 수행 하려면</span><span class="sxs-lookup"><span data-stu-id="eadf3-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="eadf3-162">설치가 완료 되 면 사용자에 게 MBAM 관리 웹 사이트의 기능에 대 한 액세스 권한을 부여할 수 있도록 사용자 역할을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="eadf3-163">관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="eadf3-164">**Mbam 하드웨어 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 하드웨어 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="eadf3-165">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="eadf3-166">드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="eadf3-167">**Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="eadf3-168">고급 헬프데스크 사용자의 경우 드라이브 복구에 키 ID 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="eadf3-169">TPM 사용자 관리의 경우 컴퓨터 도메인 필드 및 컴퓨터 이름 필드만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="eadf3-170">관리 및 모니터링 서버, 준수 및 감사 데이터베이스에서 준수 및 감사 보고서를 호스팅하는 컴퓨터에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 웹 사이트의 보고서 기능에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="eadf3-171">**Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 보고서 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="eadf3-172">**참고**  **Mbam 보고서** 의 동일한 사용자 구성원 자격 또는 그룹 구성원 관리, 모니터링 서버 기능, 준수 및 감사 데이터베이스, 준수 및 감사 보고서가 설치 된 모든 컴퓨터에서 사용자 로컬 그룹을 유지 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="eadf3-173">모든 컴퓨터에서 동일한 구성원 자격을 유지 하려면 도메인 보안 그룹을 만들고 해당 도메인 그룹을 각 로컬 MBAM 보고서 사용자 그룹에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="eadf3-174">이렇게 하면 도메인 그룹을 사용 하 여 그룹 구성원을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="eadf3-175">MBAM 서버 기능 설치 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="eadf3-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="eadf3-176">MBAM 설치가 완료 되 면 설치에서 BitLocker 관리에 필요한 모든 필요한 MBAM 기능을 성공적으로 설정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="eadf3-177">MBAM 서비스가 작동 하는지 확인 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="eadf3-178">MBAM 서버 기능 설치의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="eadf3-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="eadf3-179">MBAM 기능이 배포 된 각 서버에서 **제어판**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="eadf3-180">**프로그램**을 클릭 한 다음 **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="eadf3-181">**Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="eadf3-182">참고</span><span class="sxs-lookup"><span data-stu-id="eadf3-182">Note</span></span>**  
   <span data-ttu-id="eadf3-183">설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="eadf3-184">복구 및 하드웨어 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="eadf3-185">준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 및 감사 데이터베이스가** 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="eadf3-186">준수 및 감사 보고서가 설치 된 서버에서 관리자 권한이 있는 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="eadf3-187">SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.입니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="eadf3-188">실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="eadf3-189">**몰타 호환성 보고서** 가 나열 되어 있고 다섯 개의 보고서와 하나의 데이터 원본을 포함 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="eadf3-190">참고</span><span class="sxs-lookup"><span data-stu-id="eadf3-190">Note</span></span>**  
   <span data-ttu-id="eadf3-191">SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; srsinstancename &gt; \*</span><span class="sxs-lookup"><span data-stu-id="eadf3-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="eadf3-192">관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾아 **웹 서버 (IIS)** 를 선택한 다음 **iis (인터넷 정보 서비스) 관리자** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="eadf3-193">**연결**에서 \* &lt; computername &gt; \*으로 이동 하 여 **사이트**를 선택 하 고 **Microsoft BitLocker 관리 및 모니터링**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="eadf3-194">**MBAMAdministrationService**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="eadf3-195">관리 및 모니터링 기능이 설치 된 서버에서 관리자 권한이 있는 웹 브라우저를 열고 MBAM 웹 사이트에서 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="eadf3-196">*http:// &lt; computername &gt; /default.aspx* 및 탐색 및 보고서에 대 한 각 링크 확인</span><span class="sxs-lookup"><span data-stu-id="eadf3-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="eadf3-197">http:// &lt; computername &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="eadf3-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="eadf3-198">http:// &lt; computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="eadf3-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="eadf3-199">http:// &lt; computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="eadf3-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="eadf3-200">참고</span><span class="sxs-lookup"><span data-stu-id="eadf3-200">Note</span></span>**  
   <span data-ttu-id="eadf3-201">일반적으로 서비스는 네트워크 암호화 없이 기본 포트 80에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="eadf3-202">서비스가 다른 포트에 설치 되어 있는 경우 해당 포트를 포함 하도록 Url을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="eadf3-203">예를 들어 http://\* &lt; computername &gt; : &lt; port &gt; \*/default.aspx 또는 http:// <em> &lt; hostheadername &gt; / </em> default.aspx.</span><span class="sxs-lookup"><span data-stu-id="eadf3-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="eadf3-204">네트워크 암호화를 사용 하 여 서비스를 설치 하는 경우 http://를 https://로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadf3-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="eadf3-205">관련 항목</span><span class="sxs-lookup"><span data-stu-id="eadf3-205">Related topics</span></span>


[<span data-ttu-id="eadf3-206">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="eadf3-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





