---
title: App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)
description: App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817943"
---
# <span data-ttu-id="7a986-103">App-V Client에서 읽기 전용 캐시를 구성하는 방법(VDI)</span><span class="sxs-lookup"><span data-stu-id="7a986-103">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>


<span data-ttu-id="7a986-104">Microsoft Application Virtualization (App-v) 4.6에서 클라이언트가 공유 읽기 전용 캐시 사용을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-104">In Microsoft Application Virtualization (App-V) 4.6 the Client supports using a shared read-only cache.</span></span> <span data-ttu-id="7a986-105">공유 읽기 전용 캐시는 클라이언트가 VDI (가상 데스크톱 인프라) 시스템에서 디스크 공간을 효율적으로 사용할 수 있도록 하며,이는 사용자가 데이터 센터 서버 환경에서 호스트 되는 VM (가상 컴퓨터)에서 응용 프로그램을 실행 하 고 SAN (저장 영역 네트워크)에서 네트워크 저장소를 공유 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-105">The shared read-only cache enables the Client to use disk space efficiently in a Virtual Desktop Infrastructure (VDI) system, where users run applications on Virtual Machines (VM) that are hosted in a data center server environment and share network storage on a Storage Area Network (SAN).</span></span> <span data-ttu-id="7a986-106">다음 절차에서는 "풀링된 VM" 또는 "정적 VM" 이라고 하는 기본 VDI 아키텍처 중 하나에서 App-v 클라이언트를 구현 하는 데 필요한 프로세스의 개요를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-106">The following procedures provide an overview of the process that is required to implement the App-V Client in either of the primary VDI architectures, known as “Pooled VM” or “Static VM”.</span></span> <span data-ttu-id="7a986-107">이는 App-v 시스템 및 해당 구성 요소에 대 한 계획, 배포 및 운영 및 VDI 서버의 작업 및 관리에 익숙한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-107">It is assumed that you are familiar with the planning, deployment, and operation of the App-V system and its components, and also the operation and management of the VDI server.</span></span> <span data-ttu-id="7a986-108">App-v에 대 한 자세한 내용은 [응용 프로그램 가상화](https://go.microsoft.com/fwlink/?LinkId=122939) 를 참조 하세요 (https://go.microsoft.com/fwlink/?LinkId=122939)</span><span class="sxs-lookup"><span data-stu-id="7a986-108">For more information about App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)</span></span>

<span data-ttu-id="7a986-109">**참고**  이 절차에 설명 된 세부 정보는 예제로만 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-109">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="7a986-110">다른 방법을 사용 하 여 전체 프로세스를 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-110">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="7a986-111">VDI 시나리오에서 App-v 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="7a986-111">Deploying the App-V Client in a VDI Scenario</span></span>


<span data-ttu-id="7a986-112">모든 사용자에 게 필요한 모든 응용 프로그램으로 채워진 공유 읽기 전용 캐시를 사용 하 여 VDI 시나리오에서 App-v 클라이언트를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-112">You can deploy the App-V Client in a VDI scenario by using a shared read-only cache that has been populated with all the applications required for all users.</span></span> <span data-ttu-id="7a986-113">그런 다음 모든 App-v 클라이언트가 동일한 캐시 파일을 사용 하도록 VDI 마스터 VM 이미지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-113">You then configure the VDI Master VM Image so that all the App-V Clients use the same cache file.</span></span> <span data-ttu-id="7a986-114">사용자에 게 App-v 게시 프로세스를 사용 하 여 특정 응용 프로그램에 대 한 액세스 권한이 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-114">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="7a986-115">캐시가 이미 모든 응용 프로그램을 사용 하 여 미리 로드 되었으므로 사용자가 응용 프로그램을 시작할 때 스트리밍이 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-115">Since the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="7a986-116">그러나 캐시를 미리 채우는 데 사용 되는 패키지는 RTSP (실시간 스트리밍 프로토콜) 스트리밍을 지 원하는 App-v 서버에 보관 하 고 App-v 클라이언트에 대 한 액세스 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-116">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="7a986-117">App-v 관리 서버를 사용 하 여 응용 프로그램을 게시 하는 경우이 스트리밍 함수를 제공 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-117">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="7a986-118">배포 프로세스는 네 가지 주요 작업으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-118">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="7a986-119">마스터 공유 캐시 파일 만들기 및 채우기</span><span class="sxs-lookup"><span data-stu-id="7a986-119">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="7a986-120">VDI server 저장소에 공유 캐시 파일 복사</span><span class="sxs-lookup"><span data-stu-id="7a986-120">Copying the shared cache file to the VDI server storage</span></span>

-   <span data-ttu-id="7a986-121">VDI 마스터 이미지에서 App-v 클라이언트 소프트웨어 구성</span><span class="sxs-lookup"><span data-stu-id="7a986-121">Configuring the App-V client software on the VDI Master Image</span></span>

-   <span data-ttu-id="7a986-122">초기 배포 후 공유 캐시 파일의 업데이트 배포 주기 관리</span><span class="sxs-lookup"><span data-stu-id="7a986-122">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="7a986-123">이러한 작업에는 신중한 계획이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-123">These tasks require careful planning.</span></span> <span data-ttu-id="7a986-124">조직에서 팔 로우 하는 체계적이 고 재현할 수 있는 프로세스를 준비 하 고 문서화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-124">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="7a986-125">이는 마스터 공유 캐시 파일의 초기 준비 및 배포, 각각 마스터 공유 캐시에 대 한 업데이트를 필요로 하는 응용 프로그램 업데이트의 지속적인 관리에 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-125">This is especially important for the initial preparation and deployment of the master shared cache file, and for the on-going management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="7a986-126">다음 절차를 사용 하 여 이러한 기본 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-126">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="7a986-127">**참고**  여러 가지 메서드를 사용 하 여 응용 프로그램을 게시할 수 있지만, 다음 절차는 게시를 위한 App-v Management Server의 사용에 기반을 둔 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-127">**Note** Although you can publish the applications by using several different methods, the following procedures are based on the use of an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="7a986-128">풀링된 VM VDI 또는 정적 VM VDI 시나리오에서 초기 배포에 대 한 읽기 전용 캐시를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="7a986-128">To configure the read-only cache for initial deployment in a Pooled VM VDI or Static VM VDI scenario</span></span>**

1. <span data-ttu-id="7a986-129">VDI 서버의 VM에서 앱 V 관리 서버를 설정 하 고 구성 하 여 사용자 인증 및 게시 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-129">Set up and configure an App-V Management Server in a VM on the VDI server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="7a986-130">모든 사용자에 게 필요한 모든 응용 프로그램 패키지를 사용 하 여이 관리 서버의 콘텐츠 폴더를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-130">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="7a986-131">App-v 클라이언트가 설치 된 준비 컴퓨터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-131">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="7a986-132">모든 응용 프로그램에 대 한 액세스 권한이 있는 계정을 사용 하 여 스테이징 컴퓨터에 로그온 한 다음 전체 응용 프로그램 집합을 컴퓨터에 게시 하 고 응용 프로그램을 스트리밍 하 여 캐시 하 여 완전히 로드 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-132">Log on to the staging computer with an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="7a986-133">중요</span><span class="sxs-lookup"><span data-stu-id="7a986-133">Important</span></span>**  
   <span data-ttu-id="7a986-134">준비 컴퓨터는 App-v 클라이언트가 실행 되는 Vm에서 사용 하는 것과 동일한 운영 체제 유형 및 시스템 아키텍처를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-134">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="7a986-135">안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않도록 하 여 캐시 파일을 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-135">Restart the staging computer in Safe Mode to ensure the drivers are not started, which would lock the cache file.</span></span>

   **<span data-ttu-id="7a986-136">참고</span><span class="sxs-lookup"><span data-stu-id="7a986-136">Note</span></span>**  
   <span data-ttu-id="7a986-137">또는 응용 프로그램 가상화 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-137">Alternatively, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="7a986-138">파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-138">After the file has been copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="7a986-139">모든 Vm이 액세스할 수 있는 VDI 서버의 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더).</span><span class="sxs-lookup"><span data-stu-id="7a986-139">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="7a986-140">폴더 액세스 권한을 모든 사용자 그룹에 대해 읽기 전용으로 설정 하 고 캐시 파일 업데이트를 관리 하는 관리자에 대해 모든 권한으로 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-140">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="7a986-141">캐시 파일의 위치는 registry AppFS\\FileName.에서 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-141">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="7a986-142">중요</span><span class="sxs-lookup"><span data-stu-id="7a986-142">Important</span></span>**  
   <span data-ttu-id="7a986-143">FSD 파일은 로컬에 연결 된 저장소 성능 (예: SAN)과 응답성과 신뢰도가 같은 위치에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-143">You must put the FSD file in a location that has the responsiveness and reliability equivalent to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="7a986-144">VDI 마스터 VM 이미지에 App-v 데스크톱 클라이언트를 설치한 다음, 클라이언트의 AppFS 키에 다음 레지스트리 키 값을 추가 하 여 읽기 전용 캐시를 사용 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-144">Install the App-V Desktop Client on the VDI Master VM Image, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="7a986-145">AppFS 키는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-145">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="7a986-146">키</span><span class="sxs-lookup"><span data-stu-id="7a986-146">Key</span></span></th>
   <th align="left"><span data-ttu-id="7a986-147">유형</span><span class="sxs-lookup"><span data-stu-id="7a986-147">Type</span></span></th>
   <th align="left"><span data-ttu-id="7a986-148">값</span><span class="sxs-lookup"><span data-stu-id="7a986-148">Value</span></span></th>
   <th align="left"><span data-ttu-id="7a986-149">목적</span><span class="sxs-lookup"><span data-stu-id="7a986-149">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7a986-150">FileName</span><span class="sxs-lookup"><span data-stu-id="7a986-150">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-151">문자열</span><span class="sxs-lookup"><span data-stu-id="7a986-151">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-152">FSD 경로</span><span class="sxs-lookup"><span data-stu-id="7a986-152">path to FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-153">공유 캐시 파일의 경로를 지정 합니다 (예: \VDIServername\Sharefolder\SFTFS.). FSD (필수).</span><span class="sxs-lookup"><span data-stu-id="7a986-153">Specifies the path to the shared cache file, for example, \VDIServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="7a986-154">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="7a986-154">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="7a986-155">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-156">raid-1</span><span class="sxs-lookup"><span data-stu-id="7a986-156">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-157">클라이언트가 읽기 전용 모드로 작동 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-157">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="7a986-158">이렇게 하면 클라이언트가 패키지 캐시에 대 한 업데이트 스트리밍을 시도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-158">This ensures that the client will not attempt to stream updates to the package cache.</span></span> <span data-ttu-id="7a986-159">(필수)</span><span class="sxs-lookup"><span data-stu-id="7a986-159">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="7a986-160">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="7a986-160">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-161">문자열</span><span class="sxs-lookup"><span data-stu-id="7a986-161">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-162">오류 로그 (.etl) 파일 경로</span><span class="sxs-lookup"><span data-stu-id="7a986-162">path to error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="7a986-163">오류 로그 경로를 지정 하는 데 사용 되는 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-163">Entry used to specify the path to the error log.</span></span> <span data-ttu-id="7a986-164">권장.</span><span class="sxs-lookup"><span data-stu-id="7a986-164">(Recommended.</span></span> <span data-ttu-id="7a986-165">C:\Logs\Sftfs.etl 같은 로컬 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-165">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="7a986-166">게시 서버를 사용 하 고 로그온 할 때 게시 새로 고침을 사용 하도록 마스터 VM 이미지 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-166">Configure the Master VM Image client to use the publishing server and to use publishing refresh at logon.</span></span> <span data-ttu-id="7a986-167">사용자가 VDI 시스템에 로그온 하 고 해당 VM이 마스터 VM 이미지에서 빌드되기 때문에 게시 새로 고침 주기가 발생 하 고 계정이 승인 된 모든 응용 프로그램을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-167">As users log on to the VDI system and their VM is built from the Master VM Image, a publishing refresh cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="7a986-168">이러한 응용 프로그램은 공유 캐시에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-168">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="7a986-169">풀링된 VM 시나리오에서 패키지 업그레이드에 맞게 클라이언트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="7a986-169">To configure the client for package upgrade in a Pooled VM scenario</span></span>**

1.  <span data-ttu-id="7a986-170">응용 프로그램 패키지의 업그레이드 및 테스트를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-170">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="7a986-171">앱-V 서버에서 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-171">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="7a986-172">그런 다음 새 버전의 응용 프로그램을 스테이징 컴퓨터의 클라이언트에 게시 하 고 스트리밍 하 여 완전히 캐시에 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-172">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="7a986-173">안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-173">Restart the staging computer in Safe Mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="7a986-174">**참고**  또는 services.msc에서 Application Virtualization 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-174">**Note** Alternatively, you can stop and disable the Application Virtualization service in the Services.msc, and then restart the computer.</span></span> <span data-ttu-id="7a986-175">파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-175">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="7a986-176">모든 Vm이 액세스할 수 있는 VDI 서버의 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더).</span><span class="sxs-lookup"><span data-stu-id="7a986-176">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="7a986-177">다른 파일 이름을 사용할 수 있습니다 (예: SFTFS \ _V2). 새 버전을 구분 하는 FSD.</span><span class="sxs-lookup"><span data-stu-id="7a986-177">You can use a different filename, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="7a986-178">업데이트 된 공유 캐시 파일을 사용 하도록 VDI 마스터 VM 이미지에서 App-v 데스크톱 클라이언트를 구성 하려면 업데이트 된 파일의 위치 (예: \\\\VDIServername\\Sharefolder\\SFTFS\ _V2를 가리키도록 AppFS 레지스트리 키 파일 이름 값을 변경 합니다. FSD.</span><span class="sxs-lookup"><span data-stu-id="7a986-178">To configure the App-V Desktop Client on the VDI Master VM Image to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="7a986-179">사용자가 로그 오프 한 다음 다시 로그온 하면 업데이트 된 마스터 이미지를 사용 하 여 새 VM이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-179">When users log off and then log on again, a new VM is created for them by using the updated Master Image.</span></span> <span data-ttu-id="7a986-180">모든 사용자 설정은 유지 되며 새 VM에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-180">All their user settings will be retained and applied to the new VM.</span></span> <span data-ttu-id="7a986-181">그런 다음 업데이트 된 응용 프로그램에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-181">Then they have access to the updated applications.</span></span>

**<span data-ttu-id="7a986-182">정적 VM 시나리오에서 패키지 업그레이드에 맞게 클라이언트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="7a986-182">To configure the client for package upgrade in a Static VM scenario</span></span>**

1.  <span data-ttu-id="7a986-183">응용 프로그램 패키지의 업그레이드 및 테스트를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-183">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="7a986-184">앱-V 서버에서 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-184">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="7a986-185">그런 다음 응용 프로그램이 캐시에 완전히 로드 되도록 새 버전의 응용 프로그램을 스테이징 컴퓨터의 클라이언트에 게시 하 고 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-185">Then, publish and stream the new version of the applications to the client on the staging computer so that the applications are fully loaded into cache.</span></span>

3.  <span data-ttu-id="7a986-186">안전 모드에서 준비 컴퓨터를 다시 시작 하 여 드라이버가 시작 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-186">Restart the staging computer in Safe Mode to ensure that the drivers are not started.</span></span>

    <span data-ttu-id="7a986-187">**참고**  또는 services.msc에서 Application Virtualization 서비스를 중지 하 고 사용 하지 않도록 설정한 다음 컴퓨터를 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-187">**Note** Alternatively, you can stop and disable the Application Virtualization service in the Services.msc, and then restart the computer.</span></span> <span data-ttu-id="7a986-188">파일을 복사한 후에는 서비스를 사용 하도록 설정 하 고 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-188">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="7a986-189">모든 Vm이 액세스할 수 있는 VDI 서버의 SAN에 Sftfs fsd 캐시 파일을 복사 합니다 (예: 공유 폴더).</span><span class="sxs-lookup"><span data-stu-id="7a986-189">Copy the Sftfs.fsd cache file to the VDI server’s SAN where all the VMs can access it, such as in a shared folder.</span></span> <span data-ttu-id="7a986-190">다른 파일 이름을 사용할 수 있습니다 (예: SFTFS \ _V2). 새 버전을 구분 하는 FSD.</span><span class="sxs-lookup"><span data-stu-id="7a986-190">You can use a different filename, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="7a986-191">업데이트 된 공유 캐시 파일을 사용 하도록 VDI 마스터 VM 이미지에서 App-v 데스크톱 클라이언트를 구성 하려면 업데이트 된 파일의 위치 (예: \\\\VDIServername\\Sharefolder\\SFTFS\ _V2를 가리키도록 AppFS 레지스트리 키 파일 이름 값을 변경 합니다. FSD.</span><span class="sxs-lookup"><span data-stu-id="7a986-191">To configure the App-V Desktop Client on the VDI Master VM Image to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="7a986-192">이렇게 하면 새 사용자가 새 버전을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-192">This ensures that new users get the new version.</span></span>

6.  <span data-ttu-id="7a986-193">AppFS 키 파일 이름 값을 편집 하 여 \\\\VDIServername\\Sharefolder\\SFTFS\ _V2와 같은 업데이트 된 캐시의 위치로 설정 하는 스크립트를 만듭니다. FSD.</span><span class="sxs-lookup"><span data-stu-id="7a986-193">Create a script that edits the AppFS key FILENAME value to set it to the location of the updated cache, for example, \\\\VDIServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="7a986-194">이 스크립트는 사용자가 로그 오프할 때 (예: 그룹 정책 설정을 사용 하 여) App-v 클라이언트 드라이버가 시작 되기 전에 실행 되도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-194">Configure this script to run when the user logs off or logs on so that it runs before the App-V client drivers start, for example, by using Group Policy settings.</span></span> <span data-ttu-id="7a986-195">사용자가 로그 오프 한 다음 다시 로그온 하면 기존 VM이 업데이트 되 고 캐시의 업데이트 된 복사본을 사용 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-195">When users log off and log on again, their existing VM is updated, and they will use the updated copy of the cache.</span></span> <span data-ttu-id="7a986-196">업데이트 된 응용 프로그램에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-196">Then, they have access to the updated applications.</span></span>

## <span data-ttu-id="7a986-197">캐시를 업그레이드할 때 기호화 된 링크를 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7a986-197">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="7a986-198">새 또는 업그레이드 된 패키지를 포함 하는 새 캐시 파일이 배포 될 때마다 AppFS 키 파일 이름 값을 수정 하는 대신 Windows Vista, Windows 7 및 Windows Server 2008의 운영 체제에서 기호화 된 링크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-198">Instead of modifying the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="7a986-199">기호화 된 링크에 대 한 자세한 내용은 [기호화 된 링크](https://go.microsoft.com/fwlink/?LinkId=157626) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="7a986-199">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="7a986-200">반대로, Windows XP는 심볼 링크의 사용을 지원 하지 않으며 대신 연결 지점을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-200">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="7a986-201">연결에 대 한 자세한 내용은 Microsoft 기술 자료 [문서 205524](https://go.microsoft.com/fwlink/?LinkId=182553) ( https://go.microsoft.com/fwlink/?LinkId=182553) 및 도구 [연결 v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="7a986-201">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="7a986-202">캐시를 참조 하도록 기호화 된 링크를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="7a986-202">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="7a986-203">초기 배포 단계에서 명령 프롬프트 창을 VDI 서버 호스트 운영 체제의 로컬 관리자로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-203">During the initial deployment stage, open a Command Prompt window as a local administrator on the VDI server host operating system.</span></span>

2.  <span data-ttu-id="7a986-204">MKLINK 명령을 사용 하 여 기호화 된 링크를 만든 다음 Sftfs. fsd 파일을 가리키도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-204">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="7a986-205">mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="7a986-205">mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="7a986-206">VDI 마스터 VM 이미지에서 **관리자 권한으로 실행** 옵션을 사용 하 여 명령 프롬프트 창을 열고 VM이 VDI 호스트 운영 체제의 기호화 된 링크에 액세스할 수 있도록 원격 링크 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-206">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="7a986-207">기본적으로 원격 링크 사용 권한은 비활성화 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-207">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="7a986-208">fsutil behavior set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="7a986-208">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="7a986-209">**참고**  저장소 서버에서 적절 한 링크 사용 권한을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-209">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="7a986-210">링크 위치 및 Sftfs. fsd 파일에 따라 사용 권한은 **L2L: 1** 또는 **L2R: 1** 또는 **R2L: 1** 또는 **R2R: 1**입니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-210">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="7a986-211">VDI 마스터 VM 이미지에서 App-v 데스크톱 클라이언트를 구성할 때 AppFS 키 파일 이름 값을 기호화 된 링크를 사용 하는 FSD 파일의 UNC 경로와 동일 하 게 설정 합니다. 예를 들어 \\\\VDIHostserver\\Symlinkname.로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-211">When you configure the App-V Desktop Client on the VDI Master VM Image, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link; for example, set it to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="7a986-212">App-v 클라이언트가 먼저 캐시에 액세스 하면 기호화 된 링크가 클라이언트에 캐시 파일에 대 한 핸들을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-212">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="7a986-213">클라이언트가 실행 되는 동안에는 클라이언트가 계속 해당 핸들을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-213">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="7a986-214">기존 클라이언트에 이전 공유 캐시가 열려 있는 경우에도 기호화 된 링크의 값을 안전 하 게 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-214">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="7a986-215">패키지를 업그레이드 하거나 캐시에 새 패키지를 추가 해야 하는 경우 정적 VM 또는 풀링된 VM 시나리오에 대 한 업그레이드 절차의 1 ~ 5 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-215">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 5 of the upgrade procedure for either the Static VM or Pooled VM scenario.</span></span> <span data-ttu-id="7a986-216">그런 다음 심볼 링크를 삭제 하 고 다시 만들어서 새 버전의 공유 캐시 파일을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-216">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="7a986-217">Vm이 업데이트 된 심볼 링크를 포함 하는 경로를 사용 하기 때문에, VM이 다시 시작 되 면 클라이언트는 업데이트 된 캐시 복사본에 대 한 핸들을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-217">When the VM is restarted, the client receives a handle to the updated copy of the cache because the VM uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="7a986-218">그런 다음 사용자가 새 응용 프로그램 및 업데이트 된 애플리케이션을 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a986-218">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="7a986-219">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7a986-219">Related topics</span></span>


[<span data-ttu-id="7a986-220">Application Virtualization Management Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="7a986-220">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="7a986-221">Application Virtualization Client를 수동으로 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="7a986-221">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="7a986-222">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="7a986-222">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





