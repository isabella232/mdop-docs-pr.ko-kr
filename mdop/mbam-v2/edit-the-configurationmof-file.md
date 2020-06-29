---
title: Configuration.mof 파일 편집
description: Configuration.mof 파일 편집
author: dansimp
ms.assetid: 23e50ec9-4083-4b12-ad96-626cf30960bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/03/2017
ms.openlocfilehash: 3873467d7909c0da09c274a647029b999383e6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823433"
---
# <span data-ttu-id="09060-103">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="09060-103">Edit the Configuration.mof File</span></span>


<span data-ttu-id="09060-104">클라이언트 컴퓨터에서 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면 Configuration Manager 2007 또는 SystemCenter2012 ConfigurationManager를 사용 중인지 여부에 따라 **구성 .mof** 파일을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09060-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, whether you are using Configuration Manager 2007 or SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="09060-105">사용 중인 구성 관리자 버전에 대해 다음 지침을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="09060-105">Complete the following instructions for the version of Configuration Manager that you are using.</span></span>

<span data-ttu-id="09060-106">**중요**  새 설치를 수행 하거나 이전 버전에서 업그레이드 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)을 설치 하는 경우 다음 글머리 기호에 설명 된 대로 [약 MBAM 2.0 SP1](about-mbam-20-sp1.md) 의 해당 항목을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09060-106">**Important** If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1), either by doing a new installation or by upgrading from a previous version, see the appropriate item in [About MBAM 2.0 SP1](about-mbam-20-sp1.md) as described in the following bullets:</span></span>

-   <span data-ttu-id="09060-107">새 MBAM 2.0 SP1 설치의 경우 **구성 관리자에서 mbam을 사용 하는 경우 mbam 2.0 sp1을 설치 하는 데 필요한 파일**을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09060-107">For a new MBAM 2.0 SP1 installation, see **Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager**.</span></span>

-   <span data-ttu-id="09060-108">MBAM 2.0 SP1로 업그레이드 하는 경우에는 **mbam 2.0 sp1로 업그레이드 하 고 구성 관리자 2007에서 MBAM을 사용 하는 경우에는 구성 .mof 파일 업데이트**를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09060-108">For an upgrade to MBAM 2.0 SP1, see **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**.</span></span>

 

**<span data-ttu-id="09060-109">Configuration Manager에서 MBAM 2.0 SP1을 사용 하는 경우 구성 .mof 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="09060-109">To create the configuration.mof file if you are using MBAM 2.0 SP1 with Configuration Manager</span></span>**

-   <span data-ttu-id="09060-110">[Mbam 2.0 sp1에 대 한 자세한](about-mbam-20-sp1.md)내용은이 항목의 앞부분에 나오는 mbam 2.0 sp1에 대 한 "중요" 참고를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09060-110">See the “Important” note about MBAM 2.0 SP1 earlier in this topic for the appropriate instructions to follow in [About MBAM 2.0 SP1](about-mbam-20-sp1.md).</span></span>

**<span data-ttu-id="09060-111">SystemCenter2012 ConfigurationManager에 대 한 구성 .mof 파일을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="09060-111">To edit the Configuration.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="09060-112">Configuration Manager 서버에서 **configuration .mof** 파일의 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="09060-112">On the Configuration Manager Server, browse to the location of the **Configuration.mof** file:</span></span>

    <span data-ttu-id="09060-113">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="09060-113">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="09060-114">기본 설치의 경우 설치 위치 는%systemdrive%\\Program Files \\Microsoft 구성 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="09060-114">On a default installation, the installation location is %systemdrive%\\Program Files \\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="09060-115">다음 MBAM 클래스를 추가 하도록 **구성 .mof** 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="09060-115">Edit the **Configuration.mof** file to append the following MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================
    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;
        
        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
    KeyName="BitLocker policy";
        
        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;
        
        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

**<span data-ttu-id="09060-116">Configuration Manager 2007에 대 한 구성 .mof 파일을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="09060-116">To edit the Configuration.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="09060-117">Configuration Manager 서버에서 **configuration .mof** 파일의 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="09060-117">On the Configuration Manager Server, browse to the location of the **Configuration.mof** file:</span></span>

    <span data-ttu-id="09060-118">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="09060-118">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="09060-119">기본 설치의 경우 설치 위치 는%systemdrive%\\Program Files (x86) \\Microsoft 구성 관리자입니다.</span><span class="sxs-lookup"><span data-stu-id="09060-119">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="09060-120">다음 MBAM 클래스를 추가 하도록 **구성 .mof** 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="09060-120">Edit the **Configuration.mof** file to append the following MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 
    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;
        
        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;
        
        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";
        
        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;
        
        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;
        
        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;
        
        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy";
        
        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;
        
        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    #pragma namespace ("\\\\.\\root\\cimv2")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

## <span data-ttu-id="09060-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="09060-121">Related topics</span></span>


[<span data-ttu-id="09060-122">mof 파일을 만들거나 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="09060-122">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

[<span data-ttu-id="09060-123">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="09060-123">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





