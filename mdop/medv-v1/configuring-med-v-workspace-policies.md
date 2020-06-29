---
title: MED-V 작업 영역 정책 구성
description: MED-V 작업 영역 정책 구성
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824858"
---
# MED-V 작업 영역 정책 구성


MED-V 작업 영역 정책은 호스트 컴퓨터에서 가상화 된 환경과 응용 프로그램이 수행 하는 방법을 정의 하는 구성 가능한 설정 그룹입니다. 이 섹션의 항목에서는 MED-V 작업 영역 정책의 구성 가능한 모든 설정과이 설정이 MED-V 작업 영역에 어떤 영향을 미치는지 설명 합니다.

다음과 같은 MED-V 작업 영역 유형을 사용할 수 있습니다.

-   **Persistent**-영구 med-v 작업 영역에서 사용자가 med-v 작업 영역에 대해 변경한 모든 내용이 med-v 작업 영역에 세션 간에 저장 됩니다. 또한 영구 MED-V 작업 영역은 도메인 환경에서 일반적으로 사용 됩니다.

-   **Revertible**-Revertible med-v 작업 영역에서 각 세션을 완료 하면 (즉 med-v 작업 영역이 중지 되는 경우) med-v 작업 영역은 배포 중에 원래 상태로 돌아갑니다. 사용자가 변경한 내용이 나 추가 사항은 세션 간에 MED-V 작업 영역에 저장 되지 않습니다. 도메인 환경에서는 revertible MED-V 작업 영역을 사용할 수 없습니다.

정책이 사용자에 게 배포 된 후 MED-V 작업 영역의 유형을 다시 구성 하지 않는 것이 좋지만 MED-V 작업 영역을 배포 하기 전에 만들려는 MED-V 작업 영역의 유형을 결정 하는 것이 중요 합니다.

**참고**  정책을 구성할 때 채워지지 않은 필수 필드 옆에는 경고 기호가 표시 됩니다. 필수 필드를 입력 하지 않은 경우에는 해당 기호도 탭에 표시 됩니다.

 

## 이 섹션의 내용


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[MED-V 작업 영역에 일반 설정을 적용하는 방법](how-to-apply-general-settings-to-a-med-v-workspace.md)  
MED-V 작업 영역의 일반적인 설정과이를 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[MED-V 작업 영역에 가상 컴퓨터 설정을 적용하는 방법](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
MED-V 작업 영역에 대 한 가상 컴퓨터 설정 및 정책을 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[도메인 사용자 또는 그룹을 구성하는 방법](how-to-configure-a-domain-user-or-groupmedvv2.md)  
도메인 사용자 및 그룹을 구성 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-configure-published-applications"></a>[게시된 응용 프로그램을 구성하는 방법](how-to-configure-published-applicationsmedvv2.md)  
게시 된 응용 프로그램 및 메뉴 및이를 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[MED-V 작업 영역에 대한 웹 설정을 구성하는 방법](how-to-configure-web-settings-for-a-med-v-workspace.md)  
MED-V 작업 영역에 사용할 수 있는 웹 설정과이를 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
MED-V 작업 영역에 대 한 가상 컴퓨터 설정 및 정책을 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[MED-V 작업 영역에 네트워크 설정을 적용하는 방법](how-to-apply-network-settings-to-a-med-v-workspace.md)  
MED-V 작업 영역의 네트워크 설정 및 정책을 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[MED-V 작업 영역에 성능 설정을 적용하는 방법](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
MED-V 작업 영역의 성능 설정과이를 정책에 적용 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-import-and-export-a-policy"></a>[정책을 가져오고 내보내는 방법](how-to-import-and-export-a-policy.md)  
정책을 가져오고 내보내는 방법에 대해 설명 합니다.

 

 





