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
# WMI를 사용하여 MED-V 작업 영역 설정 관리


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에서 WMI (Windows Management Instrumentation)를 사용 하 여 현재 구성 설정을 관리할 수 있습니다.

## WMI를 사용 하 여 MED-V 작업 영역 설정을 관리 하려면


WMI 검색 도구를 사용 하 여 MED-V 작업 영역의 설정을 보고 편집할 수 있습니다. WMI 공급자는 Microsoft .Net Framework 3.5에서 WMI 공급자 확장 프레임 워크를 사용 하 여 구현 됩니다.

WMI 공급자는 **root\\microsoft\\medv** 네임 스페이스에서 구현 되며 클래스 **설정을**구현 합니다. Class (클래스) **설정** 에는 HKEY \\ _LOCAL \ _MACHINE \\software\\microsoft\\medv 레지스트리 키 아래의 시스템 레지스트리 설정에 해당 하는 속성이 포함 됩니다.

**주의**  사항 WMI 검색 도구를 사용 하 여 클래스와 인스턴스를 삭제 하거나 수정할 수 있습니다. 특정 클래스와 인스턴스를 삭제 하거나 수정 하면 귀중 한 데이터가 손실 될 수 있으며 MED-V가 예기치 않게 작동 합니다.

 

다음 단계에 따라 기본 설정 된 WMI 탐색 도구를 사용 하 여 MED-V 구성 설정을 보고 편집할 수 있습니다.

1.  관리자 권한으로 기본 설정 WMI 탐색 도구를 엽니다.

2.  네임 스페이스 **root\\microsoft\\medv**에 연결 합니다.

3.  인스턴스를 열거 하 여 실행 중인 인스턴스에 연결 합니다. 클래스 **설정**의 인스턴스에 연결 하려는 경우

    **개체 편집기** 창이 열립니다. MED-V 구성 설정이 **속성**으로 나열 됩니다.

WMI에서 MED-V 구성 설정을 편집 하려면 다음 단계를 수행 합니다.

1.  **개체 편집기** 창의 **속성** 목록에서 편집 하려는 구성 설정의 이름을 두 번 클릭 합니다. 예를 들어 MED-V URL 리디렉션 정보를 편집 하려면 **UxRedirectUrls**속성을 두 번 클릭 합니다.

    **속성 편집기** 창이 열립니다.

2.  값을 편집 하 여 구성 정보를 업데이트 합니다. 예를 들어 MED-V URL 리디렉션 정보를 편집 하려면 목록에서 웹 주소를 추가 하거나 제거 합니다.

3.  업데이트 된 속성 설정을 저장 합니다.

MED-V 구성 설정 보기 또는 편집을 완료 한 후 WMI 브라우징 도구를 닫습니다.

**중요**  경우에 따라 med-v 구성 설정을 적용 하기 위해 MED-V 작업 영역을 다시 시작 해야 하는 경우도 있습니다.

 

다음 코드에서는 **설정** 클래스를 정의 하는 MOF (관리 개체 형식) 파일을 보여 줍니다.

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

**Setting** 클래스는 **configvalueprovider** 클래스에서 상속 됩니다. 다음 코드에서는 **Configvalueprovider** 클래스를 정의 하는 MOF (관리 개체 형식) 파일을 보여 줍니다.

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

## 관련 항목


[MED-V 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)

[MED-V 작업 영역 설정 관리](manage-med-v-workspace-settings.md)

 

 





