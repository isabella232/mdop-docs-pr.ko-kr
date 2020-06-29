---
title: Sms \ _def .mof 파일 만들기 또는 편집
description: Sms \ _def .mof 파일 만들기 또는 편집
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823198"
---
# <span data-ttu-id="65775-103">Sms \ _def .mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="65775-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="65775-104">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면, Sms \ _def .mof 파일을 만들거나 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="65775-105">SystemCenter2012 ConfigurationManager를 사용 하는 경우에는 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="65775-106">최상위 계층 사이트에서 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65775-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="65775-107">변경 내용이 인프라의 다른 사이트에 복제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65775-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="65775-108">Configuration Manager 2007에서 파일이 이미 있으므로 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65775-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="65775-109">기존 파일을 덮어쓰지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="65775-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="65775-110">다음 섹션에서 사용 중인 구성 관리자 버전에 해당 하는 지침을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="65775-111">SystemCenter2012 ConfigurationManager에 대 한 Sms \ _def .mof 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="65775-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="65775-112">Configuration Manager 서버에서 Sms \ _def .mof 파일 (예: 데스크톱)을 만들어야 하는 위치를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="65775-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="65775-113">**Sms \ _def** 라는 텍스트 파일을 만들고 다음 코드를 복사 하 여 파일을 다음 Sms \ _def으로 채웁니다. MOF mbam 클래스:</span><span class="sxs-lookup"><span data-stu-id="65775-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="65775-114">다음을 수행 하 여 **Sms \ _def .mof** 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65775-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="65775-115">**SystemCenter2012 ConfigurationManager 콘솔** 을 열고 **관리** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="65775-116">**관리** 탭에서 **클라이언트 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="65775-117">**기본 클라이언트 설정을**마우스 오른쪽 단추로 클릭 한 다음 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="65775-118">**기본 설정** 창에서 **하드웨어 인벤토리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="65775-119">**클래스 설정을**클릭 한 다음 **가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="65775-120">열린 브라우저에서 **.mof** 파일을 선택한 다음 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="65775-121">**요약 가져오기** 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="65775-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="65775-122">**가져오기 요약** 창에서 하드웨어 인벤터리 클래스와 클래스 설정 모두를 가져오는 옵션이 선택 되어 있는지 확인 한 다음 **가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="65775-123">**하드웨어 인벤터리 클래스** 창과 **기본 설정** 창에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="65775-124">다음과 같이 **Win32 \ _Tpm** 클래스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="65775-125">**SystemCenter2012 ConfigurationManager 콘솔** 을 열고 **관리** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="65775-126">**관리** 탭에서 **클라이언트 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="65775-127">**기본 클라이언트 설정을**마우스 오른쪽 단추로 클릭 한 다음 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="65775-128">**기본 설정** 창에서 **하드웨어 인벤토리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="65775-129">**클래스 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="65775-130">주 창에서 아래로 스크롤한 다음 **TPM (Win32 \ _Tpm)** 클래스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="65775-131">**TPM**에서 **SpecVersion** 속성이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="65775-132">**하드웨어 인벤터리 클래스** 창과 **기본 설정** 창에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="65775-133">Configuration Manager 2007에 대 한 sms \ _def .mof 파일을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="65775-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="65775-134">Configuration Manager 서버에서 **sms \ _def .mof** 파일의 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="65775-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="65775-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="65775-136">기본 설치의 경우 설치 위치 는% 도시% \\Program Files (x86) \\Program 구성 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="65775-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="65775-137">다음 코드를 복사한 다음 **Sms \ _def .mof** 파일에 추가 하 여 다음 필수 mbam 클래스를 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="65775-138">**Win32 \ _Tpm** 클래스를 다음과 같이 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="65775-139">Class 특성에서 **SMS \ _REPORT** 를 **TRUE** 로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="65775-140">**SpecVersion** 속성 특성에서 **SMS \ _REPORT** 를 **TRUE** 로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="65775-141">**MBAM에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="65775-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="65775-142">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="65775-143">**MBAM 문제가 발생 하셨나요**?</span><span class="sxs-lookup"><span data-stu-id="65775-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="65775-144">[Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="65775-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="65775-145">Related topics</span></span>


[<span data-ttu-id="65775-146">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="65775-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="65775-147">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="65775-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="65775-148">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="65775-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="65775-149">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="65775-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="65775-150">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="65775-151">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65775-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




