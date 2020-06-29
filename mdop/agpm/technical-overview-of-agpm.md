---
title: AGPM 기술 개요
description: AGPM 기술 개요
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818298"
---
# <span data-ttu-id="be6f5-103">AGPM 기술 개요</span><span class="sxs-lookup"><span data-stu-id="be6f5-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="be6f5-104">Microsoft AGPM (고급 그룹 정책 관리)는 클라이언트/서버 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="be6f5-105">AGPM 서버는 AGPM이 서버의 파일 시스템에서 만든 보관 저장소에 오프 라인으로 Gpo (그룹 정책 개체)를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="be6f5-106">그룹 정책 관리자는 GPMC (그룹 정책 관리 콘솔) 용 AGPM 스냅인을 사용 하 여 보관 파일을 호스팅하는 서버의 Gpo와 함께 작업 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="be6f5-107">AGPM 및 관련 항목의 부분, 파일 시스템에 Gpo를 저장 하는 방법, 사용 권한이 각 사용자 역할에서 사용할 수 있는 작업을 제어 하는 방법에 대 한 이해는 AGPM에서 그룹 정책 관리자의 효율성을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="be6f5-108">용어</span><span class="sxs-lookup"><span data-stu-id="be6f5-108">Terminology</span></span>


<span data-ttu-id="be6f5-109">다음은 기본 AGPM 약관에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="be6f5-110">**AGPM 클라이언트:** GPMC (그룹 정책 관리 콘솔) 용 AGPM 스냅인을 실행 하 고 그룹 정책 관리자가 Gpo를 관리 하는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="be6f5-111">**AGPM 스냅인:** 사용자가 Gpo를 관리할 수 있도록 AGPM 클라이언트에 설치 되어 있는 AGPM의 소프트웨어 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="be6f5-112">**AGPM 서버:** AGPM 서비스를 실행 하 고 보관 파일을 관리 하는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="be6f5-113">각 AGPM 서버는 하나의 보관 파일만 관리할 수 있지만 하나의 AGPM 서버에서 하나의 보관 파일에 있는 여러 도메인에 대 한 보관 데이터를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="be6f5-114">AGPM 서버 이외의 컴퓨터에서 보관 파일을 호스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="be6f5-115">**AGPM 서비스:** AGPM 서버에서 서비스로 실행 되는 AGPM의 소프트웨어 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="be6f5-116">서비스는 해당 포리스트의 저장소와 프로덕션 환경에서 Gpo를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="be6f5-117">**보관:** AGPM에서 관련 AGPM 서버에서 관리 하는 제어 된 Gpo와 해당 Gpo 각각에 대 한 기록을 포함 하는 중앙 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="be6f5-118">여기에는 각 GPO의 모든 이전 제어 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="be6f5-119">아카이브는 여러 도메인의 Gpo에 대 한 데이터를 포함할 수 있는 보관 인덱스 파일 및 관련 보관 데이터로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="be6f5-120">AGPM 서버 이외의 컴퓨터에서 보관 파일을 호스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="be6f5-121">**제어 GPO:** AGPM에서 관리 하는 GPO입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="be6f5-122">AGPM은 보관 저장소에 저장 되어 있는 제어 된 Gpo의 기록 및 사용 권한을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="be6f5-123">**미제어 GPO:** 도메인에 대 한 프로덕션 환경의 GPO로, AGPM에서 관리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="be6f5-124">AGPM 설치, 생성 및 영향</span><span class="sxs-lookup"><span data-stu-id="be6f5-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="be6f5-125">Agpm 서버에서 AGPM 설치 프로그램이 AGPM 서비스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="be6f5-126">AGPM은 Active Directory® 디렉터리 서비스 또는 스키마를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="be6f5-127">기본적으로 AGPM 서버 프로그램 파일 은%ProgramFiles%\\Microsoft\\AGPM\\Server.에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="be6f5-128">필요 하면 도메인 컨트롤러에 AGPM 서비스를 설치할 수 있습니다. 그러나, 구성원 서버에 AGPM 서비스를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="be6f5-129">Agpm 클라이언트에서 AGPM 설치 프로그램은 AGPM 스냅인을 설치 하 고 GPMC에 표시 되는 각 도메인에 **변경 제어** 폴더를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="be6f5-130">기본적으로 AGPM 클라이언트 프로그램 파일 은%ProgramFiles%\\Microsoft\\AGPM\\Client.에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="be6f5-131">표 1에서는 AGPM에서 설치 하거나 만드는 항목 및 AGPM 작업에 영향을 주는 운영 체제 부분에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="be6f5-132">표 1: AGPM에서 설치, 생성 또는 영향을 받는 항목</span><span class="sxs-lookup"><span data-stu-id="be6f5-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be6f5-133">항목</span><span class="sxs-lookup"><span data-stu-id="be6f5-133">Item</span></span></th>
<th align="left"><span data-ttu-id="be6f5-134">설명</span><span class="sxs-lookup"><span data-stu-id="be6f5-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be6f5-135">AGPM 서비스</span><span class="sxs-lookup"><span data-stu-id="be6f5-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-136">AGPM 서비스는 AGPM 서버에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="be6f5-137">서비스는 프로덕션 환경에서 오프 라인 Gpo와 제어 된 Gpo가 포함 된 보관 파일을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="be6f5-138">AGPM 서비스의 기본 구성은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="be6f5-139">서비스 이름: </strong> AGPM 서비스</span><span class="sxs-lookup"><span data-stu-id="be6f5-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-140">표시 이름: </strong> AGPM 서비스</span><span class="sxs-lookup"><span data-stu-id="be6f5-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-141">실행 파일 경로: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="be6f5-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-142">시작: </strong> 자동</span><span class="sxs-lookup"><span data-stu-id="be6f5-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-143">다음 계정으로 로그온: </strong> <strong> 제어판에서 프로그램 및 기능을 사용 하 여 변경할 수 있는 agpm 서버를 설치 하는 동안 지정 된 Agpm 서비스 계정 </strong> <strong> </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be6f5-144">AGPM 보관</span><span class="sxs-lookup"><span data-stu-id="be6f5-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-145">기본적으로 AGPM은 AGPM 서버 에서%ProgramData%\Microsoft\AGPM에 아카이브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="be6f5-146">보관 파일은 오프 라인 Gpo에 대 한 저장소를 제공 하며 각 GPO의 여러 버전을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="be6f5-147">AGPM 관리자 또는 승인자가 GPO를 프로덕션 환경에 배포 하 고 GPO를 OU (조직 구성 단위)에 연결 하는 경우에만이 아카이브에 있는 Gpo에 대 한 변경 내용이 프로덕션 환경에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be6f5-148">Windows 방화벽</span><span class="sxs-lookup"><span data-stu-id="be6f5-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-149">설치 중에 AGPM은 AGPM 클라이언트가 AGPM 서버와 통신할 수 있도록 허용 하는 인바운드 Windows 방화벽 규칙을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="be6f5-150">기본 Windows 방화벽 규칙은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="be6f5-151">Name: </strong> AGPM 서비스</span><span class="sxs-lookup"><span data-stu-id="be6f5-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-152">작업: </strong> 연결을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-153">프로그램: </strong> 지정 된 조건을 충족 하는 모든 프로그램</span><span class="sxs-lookup"><span data-stu-id="be6f5-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-154">프로토콜 종류: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="be6f5-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-155">로컬 포트: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="be6f5-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-156">원격 포트: </strong> 모든 포트</span><span class="sxs-lookup"><span data-stu-id="be6f5-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-157">로컬 IP 주소: </strong> 모두</span><span class="sxs-lookup"><span data-stu-id="be6f5-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="be6f5-158">원격 IP 주소: </strong> 모두</span><span class="sxs-lookup"><span data-stu-id="be6f5-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be6f5-159">전자 메일 서버</span><span class="sxs-lookup"><span data-stu-id="be6f5-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-160">AGPM은 SMTP (Simple Mail Transfer Protocol)를 사용 하 여 도메인 위임 탭에서 구성한 주소로 전자 메일 요청을 보냅니다 <strong> </strong> . 예를 들어 편집기에서 새 GPO를 만들도록 요청할 때 AGPM은 도메인 위임 탭에 지정 된 각 전자 메일 주소를 알려 줍니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="be6f5-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be6f5-161">AGPM 스냅인</span><span class="sxs-lookup"><span data-stu-id="be6f5-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-162">GPMC의 AGPM 스냅인은 AGPM 클라이언트에서 실행 되며 그룹 정책 관리자가 Gpo를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="be6f5-163">이 스냅인은 <strong> 각 도메인의 변경 제어 폴더로 GPMC에 표시 됩니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="be6f5-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="be6f5-164">추가 참조</span><span class="sxs-lookup"><span data-stu-id="be6f5-164">Additional references</span></span>

<span data-ttu-id="be6f5-165">AGPM에서 설치 하는 파일에 대 한 자세한 내용은 [Agpm 계획 가이드](https://go.microsoft.com/fwlink/?LinkId=160060)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be6f5-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="be6f5-166">Archive</span><span class="sxs-lookup"><span data-stu-id="be6f5-166">Archive</span></span>


<span data-ttu-id="be6f5-167">기본적으로 AGPM 서버 설치 프로세스 는%ProgramData%\\Microsoft\\AGPM.에서 AGPM 서버의 로컬 하드 디스크에 아카이브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="be6f5-168">그러나 설치 하는 동안 경로를 변경 하거나 AGPM 서버 이외의 서버에서 보관 파일을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="be6f5-169">보관 파일에는 보관 파일에 포함 된 각 GPO의 각 버전에 대 한 하위 폴더가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="be6f5-170">각 하위 폴더의 이름은 GPO의 버전을 식별 하는 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="be6f5-171">gpostate.xml 파일은 아카이브에 있는 각 GPO의 상태를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="be6f5-172">파일은 아카이브의 콘텐츠를 설명 하는 매니페스트입니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="be6f5-173">예를 들어 GPO에는 여러 버전이 있을 수 있으며, 각 버전은 보관 저장소의 고유한 하위 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="be6f5-174">gpostate.xml 파일은 서로 다른 버전의 단일 GPO를 포함 하는 하위 폴더를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="be6f5-175">또한 GPO 템플릿은 보관 파일에 하위 폴더를 포함 하지만, gpostate.xml는 해당 Gpo를 제어할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="be6f5-176">마찬가지로, 그룹 정책 관리자가 Gpo를 삭제 하면 AGPM이 해당 사용자의 상태를 gpostate.xml에서 변경 하 여 **휴지통** 에 있는 것을 나타내지만 실제로는 보관 함의 하위 폴더를 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="be6f5-177">**주의**  사항 보관 파일에 포함 된 gpostate.xml 또는 Gpo를 수동으로 편집 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="be6f5-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="be6f5-178">이 정보는 AGPM 보관에 대 한 이해를 향상 시키기 위해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="be6f5-179">대신 AGPM 스냅인을 사용 하 여 Gpo를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="be6f5-180">AGPM에서 보관 파일을 만들면 시스템, 관리자 및 agpm 서비스 계정 (AGPM 서버의 설정에 지정)에 모든 권한이 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="be6f5-181">Agpm 스냅인에서 AGPM 사용자 인터페이스를 사용 하 여 사용 권한을 변경 해도 로그온 한 사용자를 대신 하 여 AGPM 서비스 계정이 모든 작업을 수행 하기 때문에 보관에 대 한 사용 권한은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="be6f5-182">추가 참조</span><span class="sxs-lookup"><span data-stu-id="be6f5-182">Additional references</span></span>

<span data-ttu-id="be6f5-183">보관 파일을 백업 하는 방법, 백업에서 보관 파일을 복원 하거나 AGPM 서버와 보관 파일을 모두 이동 하는 방법에 대 한 자세한 내용은 [agpm의 운영 가이드](https://go.microsoft.com/fwlink/?LinkId=160061)에 있는 "Agpm 관리자 작업 수행" 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be6f5-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="be6f5-184">역할 및 권한</span><span class="sxs-lookup"><span data-stu-id="be6f5-184">Roles and permissions</span></span>


<span data-ttu-id="be6f5-185">역할은 위임을 간소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-185">Roles simplify delegation.</span></span> <span data-ttu-id="be6f5-186">AGPM 관리자는 그룹 정책 관리자에 대 한 자세한 사용 권한을 할당 하는 대신 그룹 정책 관리자에 게 다음 네 가지 역할 중 하나를 할당 하 여 해당 역할과 관련 된 작업을 수행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="be6f5-187">**AGPM 관리자:** AGPM 관리자 (모든 권한) 역할이 할당 한 그룹 정책 관리자는 AGPM에서 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="be6f5-188">AGPM 관리자는 도메인 전체 옵션을 구성 하 고 다른 그룹 정책 관리자에 게 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="be6f5-189">**승인자:** 승인자 역할에 할당 된 그룹 정책 관리자는 도메인의 프로덕션 환경에 Gpo를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="be6f5-190">또한 승인자는 Gpo를 만들고 삭제 하며 편집자의 요청을 승인 하거나 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="be6f5-191">승인자는 도메인의 Gpo 목록을 보고 gpo의 정책 설정을 보고 GPO의 정책 설정에 대 한 보고서를 만들고 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="be6f5-192">편집자 역할을 할당 하지 않는 한 Gpo의 정책 설정은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="be6f5-193">**편집자:** 편집자 역할이 할당 한 그룹 정책 관리자는 도메인의 Gpo 목록을 보고, gpo의 정책 설정을 보고, gpo의 정책 설정을 편집 하 고, GPO의 정책 설정에 대 한 보고서를 만들고 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="be6f5-194">승인자 역할을 할당 하지 않는 한, 편집자는 Gpo를 만들거나 배포 하거나 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="be6f5-195">그러나 Gpo를 만들거나 배포 하거나 삭제 하도록 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="be6f5-196">**검토자:** 검토자 역할이 지정 된 그룹 정책 관리자는 도메인의 Gpo 목록을 보고 GPO의 정책 설정에 대 한 보고서를 만들고 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="be6f5-197">편집기 역할에 할당 된 경우에만 GPO에서 정책 설정을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="be6f5-198">Agpm 관리자가 agpm 스냅인을 사용 하 여 역할 보다 더 세부적인 수준에서 권한을 구성할 수 있는 유연성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="be6f5-199">표 2에서는 이러한 사용 권한에 대해 설명 하 고 기본적으로 각 역할에 부여 된 사용 권한을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be6f5-200">권한</span><span class="sxs-lookup"><span data-stu-id="be6f5-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="be6f5-201">설명</span><span class="sxs-lookup"><span data-stu-id="be6f5-201">Description</span></span></th>
<th align="left"><span data-ttu-id="be6f5-202">AGPM 관리자</span><span class="sxs-lookup"><span data-stu-id="be6f5-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="be6f5-203">승인자</span><span class="sxs-lookup"><span data-stu-id="be6f5-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="be6f5-204">편집기</span><span class="sxs-lookup"><span data-stu-id="be6f5-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="be6f5-205">구분</span><span class="sxs-lookup"><span data-stu-id="be6f5-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be6f5-206">모든 권한</span><span class="sxs-lookup"><span data-stu-id="be6f5-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-207">모든 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-208">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be6f5-209">GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="be6f5-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-210">도메인에서 Gpo를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-211">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-212">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be6f5-213">콘텐츠 나열</span><span class="sxs-lookup"><span data-stu-id="be6f5-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-214">도메인의 Gpo를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-215">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-216">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-217">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-218">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be6f5-219">설정 읽기</span><span class="sxs-lookup"><span data-stu-id="be6f5-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-220">GPO 내의 정책 설정을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-221">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-222">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-223">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-224">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be6f5-225">설정 편집</span><span class="sxs-lookup"><span data-stu-id="be6f5-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-226">GPO의 정책 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-227">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be6f5-228">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be6f5-229">GPO 삭제</span><span class="sxs-lookup"><span data-stu-id="be6f5-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-230">GPO를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-231">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-232">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be6f5-233">보안 수정</span><span class="sxs-lookup"><span data-stu-id="be6f5-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-234">도메인 수준 액세스를 위임 하 고, 단일 GPO에 대 한 액세스 권한을 위임 하 고, 프로덕션 환경에 대 한 액세스를 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-235">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be6f5-236">GPO 배포</span><span class="sxs-lookup"><span data-stu-id="be6f5-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-237">보관 저장소에서 프로덕션 환경으로 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-238">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-239">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be6f5-240">서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="be6f5-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-241">AGPM에서 GPO 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-242">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be6f5-243">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be6f5-244">옵션 수정</span><span class="sxs-lookup"><span data-stu-id="be6f5-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-245">AGPM 전자 메일 알림을 구성 하 고 보관 저장소에 저장 된 GPO 버전을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-246">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="be6f5-247">GPO 내보내기</span><span class="sxs-lookup"><span data-stu-id="be6f5-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-248">GPO를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-249">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be6f5-250">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="be6f5-251">GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="be6f5-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="be6f5-252">파일에서 GPO를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="be6f5-253">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="be6f5-254">예</span><span class="sxs-lookup"><span data-stu-id="be6f5-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="be6f5-255">**참고** 
 AGPM 3.0 또는 2.5에서는 **Gpo 내보내기** 및 **gpo 가져오기** 권한을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="be6f5-256">도메인에 대 한 프로덕션 환경에서 Gpo에 대 한 액세스를 위임 하는 기능과 저장 된 GPO 버전의 수를 제한 하는 기능은 AGPM 2.5에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="be6f5-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="be6f5-257">추가 참조</span><span class="sxs-lookup"><span data-stu-id="be6f5-257">Additional references</span></span>

<span data-ttu-id="be6f5-258">특정 역할을 할당 하거나 특정 작업을 수행 하는 데 필요한 권한에 대해 그룹 정책 관리자가 수행할 수 있는 작업에 대 한 자세한 내용은 [AGPM의 운영 가이드](https://go.microsoft.com/fwlink/?LinkId=160061)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be6f5-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





