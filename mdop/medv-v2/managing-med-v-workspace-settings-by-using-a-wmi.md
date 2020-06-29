---
title: WMI를 사용하여 MED-V 작업 영역 설정 관리
description: WMI를 사용하여 MED-V 작업 영역 설정 관리
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826133"
---
# <span data-ttu-id="630f5-103">WMI를 사용하여 MED-V 작업 영역 설정 관리</span><span class="sxs-lookup"><span data-stu-id="630f5-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="630f5-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에서 WMI (Windows Management Instrumentation)를 사용 하 여 현재 구성 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="630f5-105">WMI를 사용 하 여 MED-V 작업 영역 설정을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="630f5-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="630f5-106">WMI 검색 도구를 사용 하 여 MED-V 작업 영역의 설정을 보고 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="630f5-107">WMI 공급자는 Microsoft .Net Framework 3.5에서 WMI 공급자 확장 프레임 워크를 사용 하 여 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="630f5-108">WMI 공급자는 **root\\microsoft\\medv** 네임 스페이스에서 구현 되며 클래스 **설정을**구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="630f5-109">Class (클래스) **설정** 에는 HKEY \\ _LOCAL \ _MACHINE \\software\\microsoft\\medv 레지스트리 키 아래의 시스템 레지스트리 설정에 해당 하는 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="630f5-110">**주의**  사항 WMI 검색 도구를 사용 하 여 클래스와 인스턴스를 삭제 하거나 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="630f5-111">특정 클래스와 인스턴스를 삭제 하거나 수정 하면 귀중 한 데이터가 손실 될 수 있으며 MED-V가 예기치 않게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="630f5-112">다음 단계에 따라 기본 설정 된 WMI 탐색 도구를 사용 하 여 MED-V 구성 설정을 보고 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="630f5-113">관리자 권한으로 기본 설정 WMI 탐색 도구를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="630f5-114">네임 스페이스 **root\\microsoft\\medv**에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="630f5-115">인스턴스를 열거 하 여 실행 중인 인스턴스에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="630f5-116">클래스 **설정**의 인스턴스에 연결 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="630f5-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="630f5-117">**개체 편집기** 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="630f5-118">MED-V 구성 설정이 **속성**으로 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="630f5-119">WMI에서 MED-V 구성 설정을 편집 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="630f5-120">**개체 편집기** 창의 **속성** 목록에서 편집 하려는 구성 설정의 이름을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="630f5-121">예를 들어 MED-V URL 리디렉션 정보를 편집 하려면 **UxRedirectUrls**속성을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="630f5-122">**속성 편집기** 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="630f5-123">값을 편집 하 여 구성 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="630f5-124">예를 들어 MED-V URL 리디렉션 정보를 편집 하려면 목록에서 웹 주소를 추가 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="630f5-125">업데이트 된 속성 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-125">Save the updated property settings.</span></span>

<span data-ttu-id="630f5-126">MED-V 구성 설정 보기 또는 편집을 완료 한 후 WMI 브라우징 도구를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="630f5-127">**중요**  경우에 따라 med-v 구성 설정을 적용 하기 위해 MED-V 작업 영역을 다시 시작 해야 하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="630f5-128">다음 코드에서는 **설정** 클래스를 정의 하는 MOF (관리 개체 형식) 파일을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="630f5-129">**Setting** 클래스는 **configvalueprovider** 클래스에서 상속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="630f5-130">다음 코드에서는 **Configvalueprovider** 클래스를 정의 하는 MOF (관리 개체 형식) 파일을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="630f5-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## <span data-ttu-id="630f5-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="630f5-131">Related topics</span></span>


[<span data-ttu-id="630f5-132">MED-V 작업 영역 구성 설정 관리</span><span class="sxs-lookup"><span data-stu-id="630f5-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="630f5-133">MED-V 작업 영역 설정 관리</span><span class="sxs-lookup"><span data-stu-id="630f5-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





