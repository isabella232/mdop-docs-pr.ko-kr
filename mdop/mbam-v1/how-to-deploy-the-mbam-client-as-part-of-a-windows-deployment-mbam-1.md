---
title: Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법
description: Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824913"
---
# <span data-ttu-id="5706f-103">Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="5706f-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="5706f-104">관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="5706f-105">컴퓨터 이미징 및 Windows 배포 프로세스 중에 클라이언트 컴퓨터에서 BitLocker 관리 및 암호화를 사용 하도록 설정 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="5706f-106">참고</span><span class="sxs-lookup"><span data-stu-id="5706f-106">Note</span></span>**  
<span data-ttu-id="5706f-107">MBAM 클라이언트 시스템 요구 사항을 검토 하려면 [mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5706f-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="5706f-108">Windows 배포의 초기 이미징 단계에서 BitLocker를 사용 하 여 클라이언트 컴퓨터를 암호화 하면 MBAM 구현의 관리 오버 헤드를 낮출 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="5706f-109">또한이 방법을 사용 하면 배포 된 모든 컴퓨터에 이미 BitLocker가 실행 되 고 있으며 올바르게 구성 되어 있는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="5706f-110">Warning</span><span class="sxs-lookup"><span data-stu-id="5706f-110">Warning</span></span>**  
<span data-ttu-id="5706f-111">이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="5706f-112">Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="5706f-113">레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="5706f-114">Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="5706f-115">레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="5706f-116">Windows 배포의 일부로 컴퓨터를 암호화 하려면</span><span class="sxs-lookup"><span data-stu-id="5706f-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="5706f-117">조직에서 TPM (신뢰할 수 있는 플랫폼 모듈) 보호기 또는 BitLocker의 TPM + PIN 보호기 옵션을 사용할 계획 이라면, MBAM을 처음 배포 하기 전에 TPM 칩을 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="5706f-118">TPM 칩을 정품 인증 하는 경우 프로세스에서 나중에 재부팅을 피하고 조직의 요구 사항에 따라 TPM 칩이 올바르게 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="5706f-119">컴퓨터의 BIOS에서 수동으로 TPM 칩을 정품 인증 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="5706f-120">TPM 칩을 구성 하는 방법에 대 한 자세한 내용은 제조업체 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5706f-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="5706f-121">MBAM 클라이언트 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="5706f-122">컴퓨터를 도메인에 참가 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="5706f-123">컴퓨터가 도메인에 가입 되어 있지 않으면 복구 암호가 MBAM 키 복구 서비스에 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="5706f-124">복구 키를 저장할 수 없는 경우 기본적으로 MBAM은 암호화를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="5706f-125">복구 키가 MBAM 서버에 저장 되기 전에 컴퓨터가 복구 모드에서 시작 되는 경우 컴퓨터를 reimaged 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="5706f-126">사용할 수 있는 복구 방법이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="5706f-127">관리자 권한으로 명령 프롬프트를 열고 MBAM 서비스를 중지 한 다음 서비스를 **수동** 또는 **요청에**맞게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="5706f-128">그러고 나서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="5706f-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="5706f-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="5706f-130">sc config mbamagent 시작 = 요청</span><span class="sxs-lookup"><span data-stu-id="5706f-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="5706f-131">MBAM 에이전트에 대 한 레지스트리 설정을 설정 하 여 **운영 체제 전용 암호화** 를 위해 TPM을 실행 합니다 .이 작업을 수행 하려면 **regedit**를 실행 한 다음 C:\\program files Files\\Microsoft\\MDOP Mbam\\mbamdeploymentkeytemplate .xreg에서 레지스트리 키 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="5706f-132">Regedit에서 HKLM\\SOFTWARE\\Microsoft\\MBAM으로 이동 하 여 다음 표에 나열 된 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="5706f-133">레지스트리 항목</span><span class="sxs-lookup"><span data-stu-id="5706f-133">Registry entry</span></span>

    <span data-ttu-id="5706f-134">구성 설정</span><span class="sxs-lookup"><span data-stu-id="5706f-134">Configuration settings</span></span>

    <span data-ttu-id="5706f-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="5706f-135">DeploymentTime</span></span>

    <span data-ttu-id="5706f-136">0 = 해제</span><span class="sxs-lookup"><span data-stu-id="5706f-136">0 = OFF</span></span>

    <span data-ttu-id="5706f-137">1 = 배포 시간 정책 설정 사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5706f-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="5706f-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="5706f-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="5706f-139">0 = key 에스크로를 사용 하지 않습니다 (이 경우 다음 두 레지스트리 항목은 필요 없음).</span><span class="sxs-lookup"><span data-stu-id="5706f-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="5706f-140">1 = 키 복구 시스템에서 키 에스크로 사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5706f-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="5706f-141">권장: 컴퓨터가 키 복구 서비스와 통신할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="5706f-142">계속 하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="5706f-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="5706f-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="5706f-144">0 = 복구 키만 업로드</span><span class="sxs-lookup"><span data-stu-id="5706f-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="5706f-145">1 = 복구 키 및 키 복구 패키지 업로드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5706f-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="5706f-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="5706f-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="5706f-147">키 복구 웹 서버의 URL로이 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="5706f-148">예: http:// &lt; computer name &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="5706f-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="5706f-149">Mbam 에이전트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="5706f-150">다시 부팅할 준비가 되 면 관리자 권한으로 명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="5706f-151">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="5706f-151">net start mbamagent</span></span>**

8. <span data-ttu-id="5706f-152">컴퓨터가 다시 시작 되 고 BIOS에서 TPM 변경을 수락 하 라는 메시지가 표시 되 면 변경 사항을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="5706f-153">Windows 클라이언트 운영 체제 이미징 프로세스가 진행 되는 동안 암호화를 시작할 준비가 되 면 MBAM 에이전트 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="5706f-154">그런 다음 **자동**으로 시작을 설정 하려면 관리자 권한으로 명령 프롬프트를 열고 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="5706f-155">sc config mbamagent 시작 = 자동</span><span class="sxs-lookup"><span data-stu-id="5706f-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="5706f-156">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="5706f-156">net start mbamagent</span></span>**

10. <span data-ttu-id="5706f-157">무시 레지스트리 값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-157">Remove the bypass registry values.</span></span> <span data-ttu-id="5706f-158">이렇게 하려면 regedit를 실행 하 고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목을 찾아 **Mbam** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5706f-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="5706f-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5706f-159">Related topics</span></span>


[<span data-ttu-id="5706f-160">MBAM 1.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="5706f-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









