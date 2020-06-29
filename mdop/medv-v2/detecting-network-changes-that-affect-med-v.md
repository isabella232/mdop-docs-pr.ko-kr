---
title: MED-V에 영향을 주는 네트워크 변경 검색
description: MED-V에 영향을 주는 네트워크 변경 검색
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823373"
---
# MED-V에 영향을 주는 네트워크 변경 검색


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 솔루션을 사용 하면 MED-V 작업 영역이 배포 되 고 MED-V에 영향을 줄 수 있는 경우 발생할 수 있는 특정 네트워크 변경을 감지 하도록 환경을 구성할 수 있습니다.

이 기능에는 호스트 컴퓨터에서 네트워크 구성 변경 사항에 대 한 알림을 받는 게스트 운영 체제에서 실행 되는 구성 요소가 포함 되어 있습니다. 이를 통해 게스트에서 실행 중인 비 Microsoft ESD 또는 다른 응용 프로그램을 사용 하 여 호스트 ESD 또는 응용 프로그램이 확인 하는 동일한 네트워크 끝점을 확인할 수 있습니다.

**참고**  이 기능은 가상 컴퓨터가 NAT (network address translation) 모드에 대해 구성 된 경우에만 사용할 수 있습니다. 가상 머신이 브리지 모드에 대해 구성 되어 있는 경우 변경 표시가 생성 되지 않습니다.

 

이 섹션에서는 MED-V에 영향을 줄 수 있는 네트워크 변경을 모니터링 하는 데 도움이 되는 정보와 지침을 제공 합니다.

## MED-V에 대 한 네트워크 변경을 감지 하려면


MED-V 작업 영역을 배포한 후에는 다음과 같은 작업을 수행 하 여 특정 네트워크 구성에 대 한 변경 내용을 모니터링할 수 있습니다.

1. 모니터링 하려는 네트워크 구성 변경 내용을 찾을 MOF (관리 개체 형식) 파일을 만듭니다. 다음 코드에서는 만들 수 있는 MOF 파일의 예를 보여 줍니다.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. MOF 파일을 컴파일합니다.

3. 게스트에 MOF 파일을 설치 합니다.

MOF 파일을 설치한 후에는 **CCM \ _NetworkAdapters** 클래스에 대 한 WMI (Windows Management Instrumentation) 만들기, 수정 또는 삭제 이벤트를 구독 하는 이벤트 구독을 만들 수 있습니다. 이렇게 하면 호스트에 대 한 다음과 같은 변경 내용이 감지 됩니다.

IP 주소 또는 네트워크 어댑터 변경 등 네트워크에 대 한 구성 변경 사항이 있나요?

네트워크를 사용할 수 있나요?

네트워크 설정이 브리지 모드에서 NAT 모드로 변경 되었습니까?

네트워크 설정이 NAT 모드에서 브리지 모드로 변경 되었습니까?

호스트의 MED-V 구성 요소는 이러한 변경 사항에 대 한 네트워크를 모니터링 하 고 게스트에 게 변경 내용을 알립니다. 게스트의 구성 요소는 이러한 변경 내용에 대 한 MED-V 작업 영역을 모니터링 하는 WMI 인스턴스를 만듭니다.

생성 된 이벤트 구독은 이러한 네트워크 변경 (만들기, 수정 또는 삭제) 중 하나 이상을 수행 하는 경우 WMI 시스템을 통해 알림을 제공 합니다.

## 관련 항목


[MED-V 작업 영역 모니터링](monitor-med-v-workspaces.md)

[MED-V 작업 영역 설정 관리](manage-med-v-workspace-settings.md)

 

 





