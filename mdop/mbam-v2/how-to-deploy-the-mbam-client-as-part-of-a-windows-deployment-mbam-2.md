---
title: Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법
description: Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824623"
---
# <span data-ttu-id="8690a-103">Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="8690a-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="8690a-104">관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="8690a-105">TPM (신뢰할 수 있는 플랫폼 모듈) 칩이 있는 컴퓨터의 경우 이미징 및 Windows 배포 프로세스의 일부로 클라이언트 컴퓨터에서 BitLocker 관리 및 암호화를 사용 하도록 설정 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="8690a-106">참고</span><span class="sxs-lookup"><span data-stu-id="8690a-106">Note</span></span>**  
<span data-ttu-id="8690a-107">Microsoft BitLocker 관리 및 클라이언트 시스템 요구 사항 모니터링을 검토 하려면 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8690a-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="8690a-108">Windows 배포의 초기 이미징 단계 동안 BitLocker로 클라이언트 컴퓨터를 암호화 하면 조직에 MBAM을 구현 하는 데 필요한 관리 오버 헤드가 낮아질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="8690a-109">또한 배포 된 모든 컴퓨터에 이미 BitLocker가 실행 되 고 있으며 올바르게 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="8690a-110">참고</span><span class="sxs-lookup"><span data-stu-id="8690a-110">Note</span></span>**  
<span data-ttu-id="8690a-111">이 항목의 절차에서는 Windows 레지스트리를 수정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="8690a-112">레지스트리 편집기를 잘못 사용 하면 심각한 문제가 발생할 수 있으며,이 경우 Windows를 다시 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="8690a-113">Microsoft는 레지스트리 편집기의 잘못 된 사용으로 인해 발생 하는 문제에 대 한 해결을 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="8690a-114">레지스트리 편집기 사용에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="8690a-115">Windows 배포의 일부로 컴퓨터를 암호화 하려면</span><span class="sxs-lookup"><span data-stu-id="8690a-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="8690a-116">조직이 TPM (신뢰할 수 있는 플랫폼 모듈) 보호기 또는 BitLocker의 TPM + PIN 보호기 옵션을 사용할 계획 이라면, MBAM을 배포 하기 전에 TPM 칩을 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="8690a-117">TPM 칩을 정품 인증 하는 경우 프로세스에서 나중에 재부팅을 피하고 조직의 요구 사항에 따라 TPM 칩이 올바르게 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="8690a-118">컴퓨터의 BIOS에서 수동으로 TPM 칩을 정품 인증 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="8690a-119">참고</span><span class="sxs-lookup"><span data-stu-id="8690a-119">Note</span></span>**  
    <span data-ttu-id="8690a-120">일부 공급 업체는 운영 체제 내에서 BIOS의 TPM 칩을 켜고 정품 인증 하는 도구를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="8690a-121">TPM 칩을 구성 하는 방법에 대 한 자세한 내용은 제조업체 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8690a-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="8690a-122">Microsoft BitLocker 관리 및 모니터링 클라이언트 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="8690a-123">컴퓨터를 도메인에 가입 (권장)</span><span class="sxs-lookup"><span data-stu-id="8690a-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="8690a-124">컴퓨터가 도메인에 가입 되어 있지 않으면 복구 암호가 MBAM 키 복구 서비스에 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="8690a-125">복구 키를 저장할 수 없는 경우 기본적으로 MBAM은 암호화를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="8690a-126">복구 키가 MBAM 서버에 저장 되기 전에 컴퓨터가 복구 모드에서 시작 되는 경우 컴퓨터를 reimaged 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="8690a-127">사용할 수 있는 복구 방법이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="8690a-128">관리자 권한으로 명령 프롬프트를 실행 하 고, MBAM 서비스를 중지 한 다음 서비스를 **수동** 또는 **요청에**맞게 설정한 후 다음 명령을 입력 하 여 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="8690a-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="8690a-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="8690a-130">sc config mbamagent 시작 = 요청</span><span class="sxs-lookup"><span data-stu-id="8690a-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="8690a-131">MBAM 에이전트에 대 한 레지스트리 설정을 설정 하 여 그룹 정책을 무시 하 고, **Regedit**를 실행 하 여 **운영 체제 전용 암호화** 용 TPM을 실행 한 다음 C:\\program files Files\\Microsoft\\MDOP Mbam\\mbamdeploymentkeytemplate에서 레지스트리 키 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="8690a-132">Regedit에서 HKLM\\SOFTWARE\\Microsoft\\MBAM로 이동 하 여 다음 표에 나열 된 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="8690a-133">레지스트리 항목</span><span class="sxs-lookup"><span data-stu-id="8690a-133">Registry entry</span></span>

    <span data-ttu-id="8690a-134">구성 설정</span><span class="sxs-lookup"><span data-stu-id="8690a-134">Configuration settings</span></span>

    <span data-ttu-id="8690a-135">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="8690a-135">DeploymentTime</span></span>

    <span data-ttu-id="8690a-136">0 = 해제</span><span class="sxs-lookup"><span data-stu-id="8690a-136">0 = OFF</span></span>

    <span data-ttu-id="8690a-137">1 = 배포 시간 정책 설정 사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8690a-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="8690a-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="8690a-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="8690a-139">0 = key 에스크로를 사용 하지 않음 (이 경우 다음 두 레지스트리 항목은 필요 없음)</span><span class="sxs-lookup"><span data-stu-id="8690a-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="8690a-140">1 = 키 복구 시스템에서 키 에스크로 사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8690a-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="8690a-141">권장: 컴퓨터가 키 복구 서비스와 통신할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="8690a-142">계속 하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="8690a-143">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="8690a-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="8690a-144">0 = 복구 키만 업로드</span><span class="sxs-lookup"><span data-stu-id="8690a-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="8690a-145">1 = 복구 키 및 키 복구 패키지를 업로드 합니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="8690a-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="8690a-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="8690a-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="8690a-147">이 값을 키 복구 웹 서버의 URL (예: http:// &lt; computer name/MBAMRecoveryAndHardwareService/CoreService.svc.)으로 설정 합니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="8690a-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="8690a-148">Mbam 에이전트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="8690a-149">다시 부팅할 준비가 되 면 관리자 권한으로 명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="8690a-150">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="8690a-150">net start mbamagent</span></span>**

8. <span data-ttu-id="8690a-151">컴퓨터가 다시 시작 되 고 BIOS에서 TPM 변경을 수락 하 라는 메시지가 표시 되 면 변경 사항을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="8690a-152">Windows 클라이언트 운영 체제 이미징 프로세스 중에 암호화를 시작할 준비가 되 면, MBAM 에이전트 서비스를 다시 시작 하 고 관리자 권한으로 명령 프롬프트를 실행 하 고 다음 명령을 입력 하 여 **자동** 으로 시작을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="8690a-153">sc config mbamagent 시작 = 자동</span><span class="sxs-lookup"><span data-stu-id="8690a-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="8690a-154">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="8690a-154">net start mbamagent</span></span>**

10. <span data-ttu-id="8690a-155">Regedit를 실행 하 고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목으로 이동해 서 bypass 레지스트리 값을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="8690a-156">**Mbam** 노드를 삭제 하려면 노드를 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8690a-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="8690a-157">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8690a-157">Related topics</span></span>


[<span data-ttu-id="8690a-158">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="8690a-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









