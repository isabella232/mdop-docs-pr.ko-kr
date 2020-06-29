---
title: MED-V에 대한 Windows 가상 PC 이미지 구성
description: MED-V에 대한 Windows 가상 PC 이미지 구성
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826818"
---
# <span data-ttu-id="aab1f-103">MED-V에 대한 Windows 가상 PC 이미지 구성</span><span class="sxs-lookup"><span data-stu-id="aab1f-103">Configuring a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="aab1f-104">MED-V 이미지에 포함할 모든 내용을 설치한 후에는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에서 사용할 이미지를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-104">After you have installed everything that you want to include in your MED-V image, you can configure the image for use in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="aab1f-105">이 섹션의 항목에서는 MED-V 작업 영역 패키지를 만들기 전에 처음 설정에 따라 실행 되도록 MED-V 이미지를 구성 하기 위한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-105">The topics in this section provide guidance for configuring your MED-V image to run first time setup before you create your MED-V workspace package.</span></span>

<span data-ttu-id="aab1f-106">처음 설치 시 최종 사용자의 MED-V 작업 영역이 준비 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-106">First time setup prepares the MED-V workspace for an end user.</span></span> <span data-ttu-id="aab1f-107">이 프로세스는 MED-V 작업 영역에 패키지 된 이미지에서 가상 컴퓨터를 만든 다음 가상 컴퓨터에서 Windows 최소 설치를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-107">The process creates a virtual machine from the image packaged in the MED-V workspace and then runs Windows Mini-Setup on the virtual machine.</span></span> <span data-ttu-id="aab1f-108">여기에는 사용자 지정 설치 스크립트와 FtsCompletion.exe 처음 설치 완료 응용 프로그램의 실행이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-108">This includes the running of both custom setup scripts and the first time setup completion application, FtsCompletion.exe.</span></span>

<span data-ttu-id="aab1f-109">처음 설치할 때 실행할 MED-V 이미지를 구성 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="aab1f-109">Follow these steps to configure your MED-V image for running first time setup:</span></span>

1. <span data-ttu-id="aab1f-110">옵션으로 VHD (가상 하드 디스크)를 압축 하 여 빈 디스크 공간을 확보 하 고 VHD 크기를 줄인 다음 Windows 가상 PC 이미지를 계속 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-110">As an option, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you continue with configuring the Windows Virtual PC image.</span></span> <span data-ttu-id="aab1f-111">자세한 내용은 [Med-v 가상 하드 디스크 압축](compacting-the-med-v-virtual-hard-disk.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab1f-111">For more information, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

2. <span data-ttu-id="aab1f-112">가상 컴퓨터 설정 프로세스를 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-112">Customize the virtual machine setup process.</span></span>

3. <span data-ttu-id="aab1f-113">Sysprep를 사용 하 여 MED-V 이미지를 봉인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-113">Seal the MED-V image by using Sysprep.</span></span>

   **<span data-ttu-id="aab1f-114">가상 컴퓨터 설정 프로세스 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="aab1f-114">Customizing the Virtual Machine Setup Process</span></span>**

4. <span data-ttu-id="aab1f-115">MED-V와 함께 사용할 이미지를 준비 하는 과정에서 Windows 업데이트를 실행 하는 설정을 지정 하는 등 가상 컴퓨터에서 다양 한 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-115">As part of preparing your image for use with MED-V, you can configure various settings on the virtual machine, such as specifying the settings for running Windows Update.</span></span> <span data-ttu-id="aab1f-116">MED-V 작업 영역 패키지를 만들기 전에 필요한 모든 가상 컴퓨터 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-116">Specify all the necessary virtual machine settings before you create the MED-V workspace package.</span></span>

5. <span data-ttu-id="aab1f-117">MED-V 작업 영역 패키지를 만들기 전에 가상 컴퓨터에서 복원 지점을 사용 하지 않도록 설정 하 여 차이점 보관용 디스크에 대 한 무제한 연결을 방지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-117">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="aab1f-118">자세한 내용은 [WINDOWS XP ()에서 시스템 복원을 해제 하 고 설정 하는 방법](https://go.microsoft.com/fwlink/?LinkId=195927) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="aab1f-118">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

   **<span data-ttu-id="aab1f-119">참고</span><span class="sxs-lookup"><span data-stu-id="aab1f-119">Note</span></span>**  
   <span data-ttu-id="aab1f-120">설치 프로그램을 처음 실행할 때 복원 지점을 사용 하지 않도록 설정 하 여 Sysprep.inf 파일을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-120">You can set up your Sysprep.inf file to disable restore points when first time setup is run.</span></span> <span data-ttu-id="aab1f-121">이 GuiRunOnce 키를 설정 하는 예제는이 섹션의 뒷부분에 나오는 Sysprep .inf 파일 샘플을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab1f-121">For an example of setting this GuiRunOnce key, see the sample Sysprep.inf file later in this section.</span></span>



6. <span data-ttu-id="aab1f-122">기본 Windows 시작 대신 최소 설치를 실행 하도록 설정 프로세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-122">Configure the setup process to run Mini-Setup instead of the default Windows Welcome.</span></span> <span data-ttu-id="aab1f-123">**-미니** 스위치를 사용 하 여 Sysprep 도구를 실행 하거나 그래픽 사용자 인터페이스에서 **미니 설정** 확인란을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-123">You must either run the Sysprep tool by using the **-mini** switch, or select the **MiniSetup** check box in the graphical user interface.</span></span> <span data-ttu-id="aab1f-124">자세한 내용은 [Sysprep를 사용 하 여 이미지를 봉인 하는 방법을](#bkmk-seal)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab1f-124">For more information, see [How to Seal the Image with Sysprep](#bkmk-seal).</span></span>

   **<span data-ttu-id="aab1f-125">처음 설치 완료 파일 호출</span><span class="sxs-lookup"><span data-stu-id="aab1f-125">Calling the First time setup Completion File</span></span>**

   1.  <span data-ttu-id="aab1f-126">FtsCompletion.exe 이라는 실행 파일은 MED-V 게스트 에이전트 설치의 일부로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-126">An executable called FtsCompletion.exe is included as part of the installation of the MED-V Guest Agent.</span></span> <span data-ttu-id="aab1f-127">기본적으로이 파일은 사용자의 MED-V 이미지의 시스템 드라이브 ( **Microsoft 엔터프라이즈 데스크톱 가상화**)에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-127">By default, it is located in the system drive of your MED-V image under **Program Files – Microsoft Enterprise Desktop Virtualization**.</span></span>

       **<span data-ttu-id="aab1f-128">중요</span><span class="sxs-lookup"><span data-stu-id="aab1f-128">Important</span></span>**  
       <span data-ttu-id="aab1f-129">처음 설치 프로세스의 마지막 단계로,이 실행 프로그램을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-129">As the final step in the first time setup process, you must run this executable program.</span></span> <span data-ttu-id="aab1f-130">실행 중인 프로그램이 호출 되는 사용자는 게스트 로컬 관리자 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-130">The user for whom the executable program is being called must be a member of the guest’s local administrator group.</span></span>



   2.  <span data-ttu-id="aab1f-131">이 실행 프로그램 (예: MED-V 작업 영역을 사용 하 여 배포 된 스크립트)을 호출할 방법을 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-131">You can decide how you want to call this executable program, for example, through a script that is deployed with the MED-V workspace.</span></span> <span data-ttu-id="aab1f-132">이 실행 파일은 Sysprep .inf 파일의 마지막 줄로 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-132">You can call this executable as the last line of your Sysprep.inf file.</span></span> <span data-ttu-id="aab1f-133">이 실행 프로그램을 Sysprep.inf 파일에서 호출 하는 방법에 대 한 예는이 섹션의 뒷부분에 있는 샘플 파일을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab1f-133">For an example of how to call this executable program in your Sysprep.inf file, see the sample file later in this section.</span></span>

<span data-ttu-id="aab1f-134">MED-V 이미지의 사용자 지정을 완료 한 후에는 Sysprep를 사용 하 여 이미지를 봉인할 준비가 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-134">After you have completed customization of your MED-V image, you are ready to seal the image by using Sysprep.</span></span>

<a href="" id="bkmk-seal"></a>**<span data-ttu-id="aab1f-135">Sysprep를 사용 하 여 MED-V 이미지 봉인</span><span class="sxs-lookup"><span data-stu-id="aab1f-135">Sealing the MED-V Image by Using Sysprep</span></span>**

1.  <span data-ttu-id="aab1f-136">시스템 준비 도구 (Sysprep)는 관리자 또는 IT 전문가의 개입 없이 네트워크를 통해 이미지 기반 설치를 수행 하는 데 사용할 수 있는 기술입니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-136">The System Preparation tool (Sysprep) is a technology that you can use to perform image-based installations throughout the network with minimal intervention by an administrator or IT-Professional.</span></span>

2.  <span data-ttu-id="aab1f-137">MED-V 환경에서는 Sysprep를 사용 하 여 처음 시작 될 때 각 MED-V 작업 영역에 고유한 SID (보안 식별자) 및 기타 설정을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-137">In a MED-V environment, you can use Sysprep to assign unique security IDs (SID) and other settings to each MED-V workspace the first time that they are started.</span></span>

    **<span data-ttu-id="aab1f-138">참고</span><span class="sxs-lookup"><span data-stu-id="aab1f-138">Note</span></span>**  
    <span data-ttu-id="aab1f-139">Sysprep를 사용 하는 방법에 대 한 자세한 내용은 [Sysprep 기술 참조](https://go.microsoft.com/fwlink/?LinkId=195930) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195930) .</span><span class="sxs-lookup"><span data-stu-id="aab1f-139">For more information about how to use Sysprep, see [Sysprep Technical Reference](https://go.microsoft.com/fwlink/?LinkId=195930) (https://go.microsoft.com/fwlink/?LinkId=195930).</span></span>



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## <span data-ttu-id="aab1f-140">예</span><span class="sxs-lookup"><span data-stu-id="aab1f-140">Example</span></span>


<span data-ttu-id="aab1f-141">다음은 Sysprep.inf 파일의 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="aab1f-141">Here is an example of a Sysprep.inf file.</span></span>

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## <span data-ttu-id="aab1f-142">관련 항목</span><span class="sxs-lookup"><span data-stu-id="aab1f-142">Related topics</span></span>


[<span data-ttu-id="aab1f-143">MED-V 작업 영역 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="aab1f-143">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

[<span data-ttu-id="aab1f-144">MED-V 이미지 준비</span><span class="sxs-lookup"><span data-stu-id="aab1f-144">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









