---
title: MBAM 1.0 평가
description: MBAM 1.0 평가
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825253"
---
# <span data-ttu-id="95ddc-103">MBAM 1.0 평가</span><span class="sxs-lookup"><span data-stu-id="95ddc-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="95ddc-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 프로덕션 환경에 배포 하기 전에 랩 환경에서 평가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="95ddc-105">이 항목의 정보를 사용 하 여 평가 목적 으로만 단일 서버 랩 환경에서 MBAM을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="95ddc-106">실제 배포 단계는 [단일 서버에서 MBAM을 설치 하 고 구성](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)하는 방법에 설명 된 시나리오와 매우 유사 하지만이 항목에는 최소 시간 동안 mbam 평가 환경을 설정 하는 데 사용할 수 있는 추가 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="95ddc-107">랩 환경 설정</span><span class="sxs-lookup"><span data-stu-id="95ddc-107">Set up the Lab Environment</span></span>


<span data-ttu-id="95ddc-108">랩 환경에서 평가할 MBAM의 비프로덕션 인스턴스를 설정 하는 경우에도 배포 선행 조건과 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 여전히 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="95ddc-109">자세한 내용은 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95ddc-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="95ddc-110">MBAM 평가 배포를 시작 하기 전에 [mbam 1.0에 대 한 환경 준비](preparing-your-environment-for-mbam-10.md) 도 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="95ddc-111">MBAM 평가 배포 계획</span><span class="sxs-lookup"><span data-stu-id="95ddc-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="95ddc-112">작업</span><span class="sxs-lookup"><span data-stu-id="95ddc-112">Task</span></span></th>
<th align="left"><span data-ttu-id="95ddc-113">참조</span><span class="sxs-lookup"><span data-stu-id="95ddc-113">References</span></span></th>
<th align="left"><span data-ttu-id="95ddc-114">참고</span><span class="sxs-lookup"><span data-stu-id="95ddc-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-115">MBAM에 대 한 시작 정보를 검토 하 여 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 지식을 얻으십시오.</span><span class="sxs-lookup"><span data-stu-id="95ddc-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="95ddc-116">MBAM 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="95ddc-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="95ddc-117">MBAM 설치에 대 한 컴퓨팅 환경을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="95ddc-118">이렇게 하려면 MBAM 데이터베이스를 호스트 하는 SQL Server 인스턴스에서 TDE (투명 한 데이터 암호화)를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="95ddc-119">랩 환경에서 TDE를 사용 하도록 설정 하려면 MBAM이 사용 하는 SQL Server 인스턴스에서 호스팅되는 마스터 데이터베이스에 대해 실행할 .sql 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="95ddc-120">참고</span><span class="sxs-lookup"><span data-stu-id="95ddc-120">Note</span></span></strong><br/><p><span data-ttu-id="95ddc-121">다음 예제를 사용 하 여 MBAM 데이터베이스를 호스팅할 SQL Server 인스턴스에서 TDE를 빠르게 사용 하도록 설정 하는 랩 환경의 .sql 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="95ddc-122">이러한 SQL Server 명령은 로컬 서명 된 SQL Server 인증서를 사용 하 여 TDE를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="95ddc-123">TDE 인증서 및 관련 암호화 키를 C:\Backup의 로컬 백업 경로 예제에 백업 해야 합니다 <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="95ddc-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="95ddc-124">데이터베이스를 복구 하거나 인증서와 키를 입력 하는 다른 서버로 이동 하는 경우 TDE 인증서와 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="95ddc-125">MBAM 1.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="95ddc-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="95ddc-126">SQL Server 2008 Enterprise Edition의 데이터베이스 암호화</span><span class="sxs-lookup"><span data-stu-id="95ddc-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-127">MBAM 그룹 정책 요구 사항 계획 및 구성</span><span class="sxs-lookup"><span data-stu-id="95ddc-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="95ddc-128">MBAM 1.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="95ddc-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-129">필요한 Active Directory 도메인 서비스 보안 그룹을 계획 하 고 만들고 MBAM 로컬 보안 그룹 구성원 요구 사항에 대 한 계획을 수립 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="95ddc-130">MBAM 1.0 관리자 역할 계획</span><span class="sxs-lookup"><span data-stu-id="95ddc-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-131">MBAM 서버 기능 배포 계획.</span><span class="sxs-lookup"><span data-stu-id="95ddc-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="95ddc-132">MBAM 1.0 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="95ddc-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-133">MBAM 클라이언트 배포 계획.</span><span class="sxs-lookup"><span data-stu-id="95ddc-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="95ddc-134">MBAM 1.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="95ddc-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="95ddc-135">MBAM 평가 배포 수행</span><span class="sxs-lookup"><span data-stu-id="95ddc-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="95ddc-136">MBAM 설치에 대 한 컴퓨팅 환경을 준비 하는 데 필요한 계획 및 소프트웨어 필수 구성 요소 설치를 완료 한 후에는 MBAM 평가 배포를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-137">MBAM 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치에 대해 지원 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="95ddc-138">MBAM 1.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="95ddc-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-139">평가판을 위해 MBAM 설치를 실행 하 여 단일 서버에 MBAM 서버 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="95ddc-140">단일 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="95ddc-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-141">계획 단계 중에 만든 Active Directory 도메인 서비스 보안 그룹을 새 MBAM 서버의 적절 한 로컬 MBAM 서버 기능 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="95ddc-142">MBAM 1.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="95ddc-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-143">필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="95ddc-144">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="95ddc-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="95ddc-145">MBAM 클라이언트 소프트웨어를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="95ddc-146">MBAM 1.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="95ddc-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="95ddc-147">MBAM 평가에 대 한 Lab 컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="95ddc-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="95ddc-148">레지스트리 편집기를 사용 하 여 MBAM 클라이언트 상태 보고의 빈도 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="95ddc-149">그러나 이러한 수정은 테스트 목적 으로만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="95ddc-150">Warning</span><span class="sxs-lookup"><span data-stu-id="95ddc-150">Warning</span></span>**  
<span data-ttu-id="95ddc-151">이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="95ddc-152">Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="95ddc-153">레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="95ddc-154">Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="95ddc-155">레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="95ddc-156">MBAM 클라이언트 상태 보고에서 주파수 설정 수정</span><span class="sxs-lookup"><span data-stu-id="95ddc-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="95ddc-157">그룹 정책을 사용 하도록 설정 하는 경우 MBAM 클라이언트 웨이크업 및 상태 보고 주파수는 최소 90 분의 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="95ddc-158">Windows 레지스트리를 더 낮은 값으로 편집 하 여 MBAM 클라이언트 컴퓨터에서 이러한 주파수를 변경할 수 있으며,이 경우 테스트 속도가 빨라집니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="95ddc-159">MBAM 클라이언트 상태 보고에서 주파수 설정을 수정 하려면 레지스트리 편집기를 사용 하 여 **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**를 탐색 하 고 **ClientWakeupFrequency** 및 **StatusReportingFrequency** 의 값을 최소 클라이언트 지원 **값으로 변경한** 다음 BitLocker 관리 클라이언트 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="95ddc-160">이 설정을 변경 하면 MBAM 클라이언트가 1 분 마다 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="95ddc-161">이 값을 레지스트리에서 수동으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="95ddc-162">MBAM 클라이언트 서비스에서 시작 지연 수정</span><span class="sxs-lookup"><span data-stu-id="95ddc-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="95ddc-163">Mbam 클라이언트 웨이크업 및 상태 보고 빈도 외에도 클라이언트 컴퓨터에서 MBAM 클라이언트 에이전트 서비스가 시작 될 때 최대 90 분의 지연이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="95ddc-164">임의 지연을 원하지 않으면 **HKLM\\Software\\Microsoft\\MBAM**에서 a 2의 **DWORD** 값을 만들고 해당 **NoStartupDelay** 값을 **1**로 설정한 다음 BitLocker 관리 클라이언트 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ddc-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="95ddc-165">관련 항목</span><span class="sxs-lookup"><span data-stu-id="95ddc-165">Related topics</span></span>


[<span data-ttu-id="95ddc-166">MBAM 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="95ddc-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)









