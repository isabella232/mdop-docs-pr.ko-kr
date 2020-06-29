---
title: App-V Client에서 읽기 전용 캐시를 구성하는 방법(RDS)
description: App-V Client에서 읽기 전용 캐시를 구성하는 방법(RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817948"
---
# <span data-ttu-id="39394-103">App-V Client에서 읽기 전용 캐시를 구성하는 방법(RDS)</span><span class="sxs-lookup"><span data-stu-id="39394-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="39394-104">**중요**  이 절차를 사용 하려면 앱-V 4.6, SP1을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="39394-105">모든 사용자에 게 필요한 모든 응용 프로그램으로 채워진 공유 캐시를 사용 하 여 App-v 클라이언트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="39394-106">그런 다음 동일한 캐시 파일을 사용 하도록 App-v 원격 데스크톱 서비스 (RDS) 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="39394-107">사용자에 게 App-v 게시 프로세스를 사용 하 여 특정 응용 프로그램에 대 한 액세스 권한이 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39394-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="39394-108">캐시가 이미 모든 응용 프로그램을 사용 하 여 미리 로드 되었으므로 사용자가 응용 프로그램을 시작할 때 스트리밍이 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="39394-109">그러나 캐시를 미리 채우는 데 사용 되는 패키지는 RTSP (실시간 스트리밍 프로토콜) 스트리밍을 지 원하는 App-v 서버에 보관 하 고 App-v 클라이언트에 대 한 액세스 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="39394-110">App-v 관리 서버를 사용 하 여 응용 프로그램을 게시 하는 경우이 스트리밍 함수를 제공 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="39394-111">**참고**  이 절차에 설명 된 세부 정보는 예제로만 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39394-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="39394-112">다른 방법을 사용 하 여 전체 프로세스를 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="39394-113">RDS 시나리오에서 앱-V 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="39394-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="39394-114">배포 프로세스는 네 가지 주요 작업으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39394-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="39394-115">마스터 공유 캐시 파일 만들기 및 채우기</span><span class="sxs-lookup"><span data-stu-id="39394-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="39394-116">서버 저장소에 공유 캐시 파일 복사</span><span class="sxs-lookup"><span data-stu-id="39394-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="39394-117">App-v 클라이언트 소프트웨어 구성</span><span class="sxs-lookup"><span data-stu-id="39394-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="39394-118">초기 배포 후 공유 캐시 파일의 업데이트 배포 주기 관리</span><span class="sxs-lookup"><span data-stu-id="39394-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="39394-119">이러한 작업에는 신중한 계획이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-119">These tasks require careful planning.</span></span> <span data-ttu-id="39394-120">조직에서 팔 로우 하는 체계적이 고 재현할 수 있는 프로세스를 준비 하 고 문서화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="39394-121">이는 마스터 공유 캐시 파일을 준비 하 고 배포 하는 경우, 그리고 각각 마스터 공유 캐시를 업데이트 해야 하는 응용 프로그램 업데이트를 지속적으로 관리 하는 데 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="39394-122">다음 절차를 사용 하 여 이러한 기본 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="39394-123">**참고**  여러 가지 메서드를 사용 하 여 응용 프로그램을 게시할 수 있지만 다음 절차는 게시를 위해 App-v 관리 서버를 사용 하는 경우를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="39394-124">초기 배포에 대 한 읽기 전용 캐시를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="39394-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="39394-125">사용자 인증 및 게시 지원을 제공 하도록 App-v 관리 서버를 설정 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="39394-126">모든 사용자에 게 필요한 모든 응용 프로그램 패키지를 사용 하 여이 관리 서버의 콘텐츠 폴더를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="39394-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="39394-127">App-v 클라이언트가 설치 된 준비 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="39394-128">모든 응용 프로그램에 대 한 액세스 권한이 있는 계정을 사용 하 여 스테이징 컴퓨터에 로그온 한 다음 전체 응용 프로그램 집합을 컴퓨터에 게시 하 고 응용 프로그램을 스트리밍 하 여 캐시 하 여 완전히 로드 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="39394-129">중요</span><span class="sxs-lookup"><span data-stu-id="39394-129">Important</span></span>**  
   <span data-ttu-id="39394-130">준비 컴퓨터는 App-v 클라이언트가 실행 되는 Vm에서 사용 하는 것과 동일한 운영 체제 유형 및 시스템 아키텍처를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="39394-131">안전 모드에서 준비 컴퓨터를 다시 시작 하 여 캐시 파일을 잠금으로써 드라이버가 시작 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="39394-132">참고</span><span class="sxs-lookup"><span data-stu-id="39394-132">Note</span></span>**  
   <span data-ttu-id="39394-133">또는 응용 프로그램 가상화 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="39394-134">파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="39394-135">모든 RDS 서버에서 액세스할 수 있는 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더).</span><span class="sxs-lookup"><span data-stu-id="39394-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="39394-136">폴더 액세스 권한을 모든 사용자 그룹에 대해 읽기 전용으로 설정 하 고 캐시 파일 업데이트를 관리 하는 관리자에 대해 모든 권한으로 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="39394-137">캐시 파일의 위치는 registry AppFS\\FileName.에서 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="39394-138">중요</span><span class="sxs-lookup"><span data-stu-id="39394-138">Important</span></span>**  
   <span data-ttu-id="39394-139">FSD 파일은 로컬에 연결 된 저장소 성능 (예: SAN)과 응답성과 안정성이 같은 위치에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="39394-140">각 RDS 서버에 App-v RDS 클라이언트를 설치한 다음, 클라이언트의 AppFS 키에 다음 레지스트리 키 값을 추가 하 여 읽기 전용 캐시를 사용 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="39394-141">AppFS 키는 32 비트 컴퓨터의 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS에 있으며 64 비트 컴퓨터 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS에 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="39394-142">키</span><span class="sxs-lookup"><span data-stu-id="39394-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="39394-143">유형</span><span class="sxs-lookup"><span data-stu-id="39394-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="39394-144">값</span><span class="sxs-lookup"><span data-stu-id="39394-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="39394-145">목적</span><span class="sxs-lookup"><span data-stu-id="39394-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="39394-146">FileName</span><span class="sxs-lookup"><span data-stu-id="39394-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-147">문자열</span><span class="sxs-lookup"><span data-stu-id="39394-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-148">FSD 경로</span><span class="sxs-lookup"><span data-stu-id="39394-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-149">공유 캐시 파일의 경로를 지정 합니다 (예: \RDSServername\Sharefolder\SFTFS.). FSD (필수).</span><span class="sxs-lookup"><span data-stu-id="39394-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="39394-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="39394-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="39394-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-152">raid-1</span><span class="sxs-lookup"><span data-stu-id="39394-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-153">클라이언트가 읽기 전용 모드로 작동 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="39394-154">이렇게 하면 클라이언트가 패키지 캐시에 대 한 업데이트 스트리밍을 시도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="39394-155">(필수)</span><span class="sxs-lookup"><span data-stu-id="39394-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="39394-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="39394-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-157">문자열</span><span class="sxs-lookup"><span data-stu-id="39394-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-158">오류 로그 (.etl) 파일 경로</span><span class="sxs-lookup"><span data-stu-id="39394-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="39394-159">오류 로그 경로를 지정 하는 데 사용 되는 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="39394-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="39394-160">권장.</span><span class="sxs-lookup"><span data-stu-id="39394-160">(Recommended.</span></span> <span data-ttu-id="39394-161">C:\Logs\Sftfs.etl 같은 로컬 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="39394-162">팜에 게시 서버를 사용 하 고 사용자가 로그온 할 때 게시 업데이트를 사용 하도록 각 RDS 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="39394-163">사용자가 RDS 서버에 로그온 하면 게시 업데이트 사이클이 발생 하 고 계정이 승인 된 모든 응용 프로그램을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="39394-164">이러한 응용 프로그램은 공유 캐시에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39394-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="39394-165">패키지 업그레이드에 대 한 RDS 클라이언트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="39394-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="39394-166">응용 프로그램 패키지의 업그레이드 및 테스트를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="39394-167">앱-V 서버에서 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="39394-168">그런 다음 새 버전의 응용 프로그램을 스테이징 컴퓨터의 클라이언트에 게시 하 고 스트리밍 하 여 완전히 캐시에 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="39394-169">안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="39394-170">**참고**  또는 먼저 services.msc에서 Application Virtualization 서비스를 중지 한 다음 사용 하지 않도록 설정 하 고 컴퓨터를 다시 시작 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39394-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="39394-171">파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="39394-172">모든 RDS 서버에서 액세스할 수 있는 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더).</span><span class="sxs-lookup"><span data-stu-id="39394-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="39394-173">다른 파일 이름 (예: SFTFS \ _V2)을 사용할 수 있습니다. 새 버전을 구분 하는 FSD.</span><span class="sxs-lookup"><span data-stu-id="39394-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="39394-174">팜의 각 RDS 서버에서 업데이트 된 공유 캐시 파일을 사용 하도록 앱 V RDS 클라이언트를 구성 하려면 업데이트 된 파일의 위치 (예: \\\\RDSServername\\Sharefolder\\SFTFS\ _V2를 가리키도록 AppFS 레지스트리 키 파일 이름 값을 변경 합니다. FSD.</span><span class="sxs-lookup"><span data-stu-id="39394-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="39394-175">이렇게 하면 각 RDS 서버에서 앱-Vclient 드라이버가 다시 시작 될 때 업데이트 된 캐시 복사본을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="39394-176">**중요**  업데이트 된 공유 캐시 파일을 사용 하기 위해서는 RDS 서버를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="39394-177">캐시를 업그레이드할 때 기호화 된 링크를 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="39394-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="39394-178">새 또는 업그레이드 된 패키지를 포함 하는 새 캐시 파일이 배포 될 때마다 AppFS 키 파일 이름 값을 변경 하는 대신 Windows Vista, Windows 7 및 Windows Server 2008의 운영 체제에서 기호화 된 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="39394-179">기호화 된 링크에 대 한 자세한 내용은 [기호화 된 링크](https://go.microsoft.com/fwlink/?LinkId=157626) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="39394-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="39394-180">반대로, Windows XP는 심볼 링크의 사용을 지원 하지 않으며 대신 연결 지점을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="39394-181">연결에 대 한 자세한 내용은 Microsoft 기술 자료 [문서 205524](https://go.microsoft.com/fwlink/?LinkId=182553) ( https://go.microsoft.com/fwlink/?LinkId=182553) 및 도구 [연결 v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="39394-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="39394-182">캐시를 참조 하도록 기호화 된 링크를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="39394-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="39394-183">초기 배포 단계에서 명령 프롬프트 창을 RDS 서버 호스트 운영 체제의 로컬 관리자로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="39394-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="39394-184">MKLINK 명령을 사용 하 여 기호화 된 링크를 만든 다음 Sftfs. fsd 파일을 가리키도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="39394-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="39394-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="39394-186">VDI 마스터 VM 이미지에서 **관리자 권한으로 실행** 옵션을 사용 하 여 명령 프롬프트 창을 열고 VM이 VDI 호스트 운영 체제의 기호화 된 링크에 액세스할 수 있도록 원격 링크 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="39394-187">기본적으로 원격 링크 사용 권한은 비활성화 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="39394-188">fsutil behavior set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="39394-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="39394-189">**참고**  저장소 서버에서 적절 한 링크 사용 권한을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="39394-190">링크 위치 및 Sftfs. fsd 파일에 따라 사용 권한은 **L2L: 1** 또는 **L2R: 1** 또는 **R2L: 1** 또는 **R2R: 1**입니다.</span><span class="sxs-lookup"><span data-stu-id="39394-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="39394-191">App-v RDS 클라이언트를 구성할 때 AppFS 키 파일 이름 값을 기호화 된 링크를 사용 하는 FSD 파일의 UNC 경로와 동일 하 게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="39394-192">예를 들어 파일 이름을 \\\\VDIHostserver\\Symlinkname.로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="39394-193">App-v 클라이언트가 먼저 캐시에 액세스 하면 기호화 된 링크가 클라이언트에 캐시 파일에 대 한 핸들을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="39394-194">클라이언트가 실행 되는 동안에는 클라이언트가 계속 해당 핸들을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="39394-195">기존 클라이언트에 이전 공유 캐시가 열려 있는 경우에도 기호화 된 링크의 값을 안전 하 게 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="39394-196">패키지를 업그레이드 하거나 캐시에 새 패키지를 추가 해야 하는 경우 업그레이드 절차의 1 ~ 4 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="39394-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="39394-197">그런 다음 심볼 링크를 삭제 하 고 다시 만들어서 새 버전의 공유 캐시 파일을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="39394-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="39394-198">이렇게 하면 각 RDS 서버에서 App-v 클라이언트 드라이버가 다시 시작 될 때 업데이트 된 캐시 복사본을 받을 것을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="39394-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="39394-199">RDS 서버를 다시 시작 하면 클라이언트는 업데이트 된 심볼 링크를 포함 하는 경로를 사용 하기 때문에 App-v 클라이언트가 업데이트 된 캐시 복사본에 대 한 핸들을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="39394-200">그런 다음 사용자가 새 응용 프로그램 및 업데이트 된 애플리케이션을 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39394-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="39394-201">관련 항목</span><span class="sxs-lookup"><span data-stu-id="39394-201">Related topics</span></span>


[<span data-ttu-id="39394-202">Application Virtualization Management Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="39394-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="39394-203">Application Virtualization Client를 수동으로 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="39394-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="39394-204">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="39394-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





