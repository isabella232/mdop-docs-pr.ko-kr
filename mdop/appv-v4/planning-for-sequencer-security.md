---
title: Sequencer 보안 계획
description: Sequencer 보안 계획
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815913"
---
# <span data-ttu-id="9d9c1-103">Sequencer 보안 계획</span><span class="sxs-lookup"><span data-stu-id="9d9c1-103">Planning for Sequencer Security</span></span>


<span data-ttu-id="9d9c1-104">시퀀서 구현이 작동 하 고 더 안전 하 게 유지 되도록 Application Virtualization (App-v)을 구성할 때 권장 되는 구현 방법을 최대한 일찍 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-104">Incorporate recommended implementation practices as early as possible when configuring Application Virtualization (App-V) so that your Sequencer implementation is functional and more secure.</span></span> <span data-ttu-id="9d9c1-105">시퀀서를 이미 구성한 경우에는 다음 모범 사례 지침을 사용 하 여 디자인 결정을 다시 검토 하 고 보안 측면에서 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-105">If you have already configured the Sequencer, use the following best-practice guidelines to revisit your design decisions and analyze them from a security perspective.</span></span>

**<span data-ttu-id="9d9c1-106">중요</span><span class="sxs-lookup"><span data-stu-id="9d9c1-106">Important</span></span>**  
<span data-ttu-id="9d9c1-107">App-v 시퀀서는 Sequencer를 실행 하는 컴퓨터에 기록 된 모든 응용 프로그램 정보를 수집 하 고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-107">The App-V Sequencer collects and deploys all application information recorded on the computer running the sequencer.</span></span> <span data-ttu-id="9d9c1-108">시퀀서를 실행 하는 컴퓨터에 액세스 하는 모든 사용자에 게 관리 자격 증명이 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-108">You should ensure that all users accessing the computer running the Sequencer have administrative credentials.</span></span> <span data-ttu-id="9d9c1-109">사용자 계정 자격 증명을 사용 하는 사용자는 패키지 콘텐츠 및 패키지 파일을 제어 하는 데 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-109">Users with user account credentials should not have access to control package contents and package files.</span></span> <span data-ttu-id="9d9c1-110">원격 데스크톱 서비스 (이전의 터미널 서비스)를 실행 하는 컴퓨터에서 시퀀싱 하는 경우 시퀀싱을 전담 하는 컴퓨터이 고 사용자 계정 자격 증명이 있는 사용자가 시퀀싱 중에 연결 되지 않았는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-110">If you are sequencing on a computer running Remote Desktop Services (formerly Terminal Services), make sure it is a computer that is dedicated to sequencing and that users with user account credentials are not connected to it during sequencing.</span></span>



## <span data-ttu-id="9d9c1-111">Sequencer 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="9d9c1-111">Sequencer Security Best Practices</span></span>


<span data-ttu-id="9d9c1-112">App-v (Application Virtualization) Sequencer를 구현 하 고 사용할 때 다음과 같은 시나리오와 관련 모범 사례를 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-112">Consider the following scenarios and the associated best practices when implementing and using the Application Virtualization (App-V) Sequencer:</span></span>

-   <span data-ttu-id="9d9c1-113">**Sequencer를 실행 하는 컴퓨터에서 바이러스를 검색**하는 경우, sequencer를 실행 하는 컴퓨터에서 바이러스를 검색 한 다음 시퀀싱 프로세스 중 시퀀서를 실행 하는 컴퓨터에서 모든 바이러스 백신 및 맬웨어 감지 소프트웨어를 사용 하지 않도록 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-113">**Virus scanning on the computer running the Sequencer**—It is recommended that you scan the computer running the Sequencer for viruses and then disable all antivirus and malware detection software on the computer running the Sequencer during the sequencing process.</span></span> <span data-ttu-id="9d9c1-114">이렇게 하면 시퀀싱 프로세스가 속도를 빠르게 하 고 바이러스 백신 및 맬웨어 방지 소프트웨어 구성 요소가 시퀀싱 프로세스를 방해 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-114">This will speed the sequencing process and prevent the antivirus and anti-malware software components from interfering with the sequencing process.</span></span> <span data-ttu-id="9d9c1-115">다음으로 시퀀서를 실행 하지 않는 컴퓨터에 시퀀싱 된 패키지를 설치 하 고 설치가 완료 되 면 해당 컴퓨터에서 바이러스를 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-115">Next install the sequenced package on a computer not running the Sequencer, and after successful installation, scan that computer for viruses.</span></span> <span data-ttu-id="9d9c1-116">바이러스가 발견 되 면 감염 된 원본 파일을 알리기 위해 소프트웨어 제조업체에 문의 하 고 바이러스 없이 업데이트 된 설치 원본을 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-116">If viruses are found, the manufacturer of the software should be contacted to inform them of the infected source files and request an updated installation source without viruses.</span></span> <span data-ttu-id="9d9c1-117">선택적으로 설치 단계 후에 시퀀서를 검색할 수 있으며, 바이러스가 발견 되는 경우 소프트웨어 제조업체에는 위에서 설명한 대로 연락 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-117">Optionally, the Sequencer could be scanned after the installation phase and if a virus is found, the software manufacturer should be contacted as mentioned above.</span></span>

    **<span data-ttu-id="9d9c1-118">참고</span><span class="sxs-lookup"><span data-stu-id="9d9c1-118">Note</span></span>**  
    <span data-ttu-id="9d9c1-119">응용 프로그램에서 바이러스가 검색 되는 경우 대상 컴퓨터에 응용 프로그램을 배포할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-119">If a virus is detected in an application, the application should not be deployed to target computers.</span></span>



-   <span data-ttu-id="9d9c1-120">**Ntfs 파일에서 acl (액세스 제어 목록)을 캡처하**는 경우 App-v 시퀀서는 제품을 설치 하는 동안 모니터링 되는 파일에 대 한 ntfs 파일 시스템 권한을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-120">**Capturing access control lists (ACLs) on NTFS files**—The App-V Sequencer captures NTFS file system permissions for the files that are monitored during the installation of the product.</span></span> <span data-ttu-id="9d9c1-121">이 접근 권한 값을 통해 응용 프로그램의 의도 된 동작을 로컬로 설치 하 고 가상화 되지 않은 것 처럼 정확 하 게 복제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-121">This capability allows you to more accurately replicate the intended behavior of the application, as if it were installed locally and not virtualized.</span></span> <span data-ttu-id="9d9c1-122">일부 시나리오에서는 응용 프로그램에서 사용자가 응용 프로그램 파일 내에서 액세스 하지 않은 정보를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-122">In some scenarios, an application might store information that users were not intended to access within the application files.</span></span> <span data-ttu-id="9d9c1-123">예를 들어 응용 프로그램은 응용 프로그램 내의 파일에 자격 증명 정보를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-123">For example, an application could store credentials information in a file inside of the application.</span></span> <span data-ttu-id="9d9c1-124">패키지에 Acl이 적용 되지 않으면 사용자가 볼 수 있으며,이 정보를 응용 프로그램 외부에서 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-124">If ACLs are not enforced on the package, a user could potentially view and then use this information outside of the application.</span></span>

    **<span data-ttu-id="9d9c1-125">참고</span><span class="sxs-lookup"><span data-stu-id="9d9c1-125">Note</span></span>**  
    <span data-ttu-id="9d9c1-126">암호 등의 암호화 되지 않은 보안 관련 정보를 저장 하는 응용 프로그램은 시퀀싱 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-126">You should not sequence applications that store unencrypted security-specific information, such as passwords, and so on.</span></span>



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   <span data-ttu-id="9d9c1-127">**Sequencer는 레지스트리 acl을 캡처하지**않지만, 시퀀싱을 설치 하는 동안 NTFS 파일 시스템 acl을 캡처 하더라도 레지스트리에 대 한 acl을 캡처하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-127">**Sequencer doesn’t capture registry ACLs**—Although the Sequencer captures the NTFS file system ACLs during the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="9d9c1-128">사용자는 서비스를 제외 하 고 가상 응용 프로그램의 모든 레지스트리 키에 대 한 전체 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-128">Users will have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="9d9c1-129">그러나 사용자가 가상 응용 프로그램의 레지스트리를 수정 하는 경우, 변경 내용이 특정 매장 (**uservol \ _v1 _sftfs installer.pkg**)에 저장 되며 다른 사용자에 게 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-129">However, if a user modifies the registry of a virtual application, the change will be stored in a specific store (**uservol\_sftfs\_v1.pkg**) and will not affect other users.</span></span>

-   <span data-ttu-id="9d9c1-130">**응용 프로그램 서비스**-app-v는 가상화 된 응용 프로그램의 일부인 응용 프로그램 서비스에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-130">**Application services**—App-V provides support for application services that are part of a virtualized application.</span></span> <span data-ttu-id="9d9c1-131">그러나 가상 환경에서는 해당 환경이 실행 되는 보안 컨텍스트가 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-131">However, in the virtual environment, the security context that they will run as is limited.</span></span> <span data-ttu-id="9d9c1-132">가상 환경에서 지원 되는 유일한 보안 컨텍스트는 로컬 시스템, 로컬 서비스 및 네트워크 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-132">The only security contexts supported in a virtual environment are Local System, Local Service, and Network Service.</span></span> <span data-ttu-id="9d9c1-133">시퀀싱 하는 동안 3 가지 지원 되지 않는 응용 프로그램 서비스에 대해 보안 컨텍스트를 지정한 경우 로컬 시스템 보안 컨텍스트가 가상 환경에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-133">During sequencing, if a security context is specified for an application service other than the three supported, the Local System security context will be applied in the virtual environment.</span></span> <span data-ttu-id="9d9c1-134">응용 프로그램 서비스가 로컬 서비스 또는 네트워크 서비스를 사용 하도록 구성 된 경우에는 가상 환경에서 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-134">If the application service is configured to use either Local Service or Network Service, it will be honored in the virtual environment.</span></span> <span data-ttu-id="9d9c1-135">이 세 가지 보안 컨텍스트를 사용 하 여 시퀀싱 프로세스 중에 서비스 계정을 구성 하는 작업이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-135">Configuring the service account can be done during the sequencing process using these three security contexts.</span></span>

-   <span data-ttu-id="9d9c1-136">**유지 된 보안 정보**— 응용 프로그램을 시퀀싱 하는 경우 사용자가 응용 프로그램을 설치할 수 있으며, 모니터링 하는 동안 응용 프로그램을 설치 하기 위한 자동화 된 방법을 개발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-136">**Persisted security information**—When sequencing applications, you can install the application as a user would or you can develop an automated method for installing the application while being monitored.</span></span> <span data-ttu-id="9d9c1-137">패키지에서 제외 되지 않는 모든 내용은 해당 패키지의 일부로 캡처 되어 응용 프로그램에 가상화 된 환경에서 실행 하는 데 필요한 자산을 포함 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-137">Everything that is not being excluded from the package will be captured as part of that package so that the application will have the necessary assets to run in a virtualized environment.</span></span> <span data-ttu-id="9d9c1-138">일부 응용 프로그램은 설치 중에 중요 한 보안 정보 (예: 암호)를 저장 합니다. 보호 되지 않은 상태로 유지 되는 경우 해당 패키지에 대 한 액세스 권한이 있는 다른 사용자가이 보안 정보에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-138">Some applications store sensitive security information (such as passwords) during the installation; if persisted unprotected, this security information could be accessed by other users with access to the package.</span></span> <span data-ttu-id="9d9c1-139">설치 중에 응용 프로그램 설치가 암호 또는 기타 보안 관련 정보를 요청 하는 경우 설명서를 참조 하 여 유지 되지 않았거나 (설치 후 제거 됨), 유지 되는 경우 보호 (암호화) 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-139">During installation, if an application installation asks for a password or other security-sensitive information, check with the documentation to ensure that it is either not persisted (removed after installation) or, if persisted, that it is protected (encrypted).</span></span>

-   <span data-ttu-id="9d9c1-140">**가상 응용 프로그램 패키지 보안**-패키지가 무단으로 또는 손상 되는 것을 방지 하기 위해 항상 네트워크의 안전한 위치에 가상 응용 프로그램 패키지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d9c1-140">**Securing virtual application packages**—Always save virtual application packages in a secure location on the network to protect the package from being tampered with or corrupted.</span></span>

## <span data-ttu-id="9d9c1-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9d9c1-141">Related topics</span></span>


[<span data-ttu-id="9d9c1-142">보안 및 보호 계획</span><span class="sxs-lookup"><span data-stu-id="9d9c1-142">Planning for Security and Protection</span></span>](planning-for-security-and-protection.md)









