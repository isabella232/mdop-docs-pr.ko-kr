---
title: MED-V 작업 영역에 응용 프로그램 설치 및 제거
description: MED-V 작업 영역에 응용 프로그램 설치 및 제거
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827218"
---
# MED-V 작업 영역에 응용 프로그램 설치 및 제거


호스트 운영 체제와 호환 되지 않는 응용 프로그램은 MED-V 작업 영역에서 실행할 수 있으며 호스트 컴퓨터, **시작** 메뉴 또는 localhost 바로 가기 키를 사용 하 여 열 때와 같은 방식으로 med-v 작업 영역에서 열립니다.

MED-V 작업 영역을 배포한 후에는 MED-V 작업 영역에 응용 프로그램을 설치 하 고 제거 하는 데 사용할 수 있는 여러 가지 옵션이 있습니다. 이러한 옵션에는 다음이 포함 됩니다.

-   [그룹 정책 사용](#bkmk-grouppolicy)

-   [전자 소프트웨어 배포 시스템 사용](#bkmk-esd)

-   [Application Virtualization (APP-V) 사용](#bkmk-appv)

-   [핵심 이미지 업데이트](#bkmk-coreimage)

**중요**  설치 된 응용 프로그램이 호스트에 자동으로 게시 되도록 하려면 **모든 사용자**의 가상 컴퓨터에 응용 프로그램을 설치 합니다. 응용 프로그램 게시에 대 한 자세한 내용은 [Med-v 작업 영역에서 응용 프로그램 게시 및 게시 취소 하는 방법을](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)참조 하세요.

 

**팁**  MED-V는 MED-V 작업 영역의 Internet Explorer에서 Microsoft Word 문서를 두 번 클릭 하는 등의 콘텐츠 처리에 대 한 게스트 대 호스트 리디렉션을 지원 하지 않습니다. 따라서 Microsoft Word와 같은 필수 응용 프로그램을 MED-V 작업 영역에 설치 하 여 최종 사용자가 예상할 수 있는 기본 콘텐츠 처리 기능을 제공 해야 합니다.

 

## <a href="" id="bkmk-grouppolicy"></a> 그룹 정책을 사용 하 여 응용 프로그램 추가 및 제거


그룹 정책 및 그룹 정책 개체를 사용 하 여 엔터프라이즈의 MED-V 작업 영역 전체 또는 일부에 응용 프로그램을 할당 하거나 게시할 수 있습니다. 할당 된 응용 프로그램의 경우 최종 사용자가 컴퓨터에 로그온 하면 **시작** 메뉴에 해당 응용 프로그램이 표시 됩니다. 처음으로 새 응용 프로그램을 선택 하면 응용 프로그램이 설치 되 고 사용할 준비가 됩니다. 게시 된 응용 프로그램의 경우 **시작** 메뉴에 응용 프로그램이 나타나지 않습니다. **제어판** 의 **프로그램 추가/제거** 를 사용 하거나 응용 프로그램과 연결 된 파일을 열어 최종 사용자만 설치할 수 있습니다.

동일한 방법으로 그룹 정책 및 그룹 정책 개체를 사용 하 여 MED-V 작업 영역에서 응용 프로그램을 제거할 수도 있습니다.

그룹 정책을 사용 하 여 응용 프로그램을 추가 하 고 제거 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) (를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .

## <a href="" id="bkmk-esd"></a> ESD 시스템을 사용 하 여 응용 프로그램 추가 및 제거


ESD (전자 소프트웨어 배포) 시스템은 네트워크 연결을 통해 다양 한 컴퓨터에 소프트웨어 및 기타 정보를 효율적으로 배포 하도록 디자인 되었습니다. 조직에서 ESD 시스템을 사용 하 여 소프트웨어를 배포 하는 경우 물리적 컴퓨터에서 응용 프로그램을 추가 하 고 제거 하는 것 처럼이를 사용 하 여 MED-V 작업 영역에서 응용 프로그램을 추가 하 고 제거할 수 있습니다.

## <a href="" id="bkmk-appv"></a> 앱을 사용 하 여 응용 프로그램 추가 및 제거-V


Microsoft App-v (Application Virtualization)는 해당 컴퓨터에 직접 응용 프로그램을 설치할 필요 없이 최종 사용자 컴퓨터에서 응용 프로그램을 사용할 수 있도록 하는 관리 기능을 제공 합니다. 예를 들어, Windows XP에서 앱으로 시퀀싱 한 응용 프로그램이 조직에 있고,이를 다시 시퀀싱 하 여 Windows 7로 마이그레이션이 지연 되는 경우에는 MED-V와 App-v를 함께 사용할 수 있습니다.

MED-V와 앱-V를 함께 사용 하 여 배포 된 MED-V 작업 영역에서 가상 응용 프로그램을 추가 하 고 제거할 수 있습니다. 이 방법으로 응용 프로그램을 관리 하려면 먼저 MED-V 게스트 운영 체제에 App-v 에이전트를 설치 해야 합니다. 그런 다음 MED-V 작업 영역에서 App-v를 사용 하 여 가상 응용 프로그램을 추가 하 고 제거할 수 있습니다.

App-v를 설치 하 고 사용 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화](https://go.microsoft.com/fwlink/?LinkId=122939) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=122939) .

**중요**  MED-V 작업 영역에 게시 하는 앱-V 응용 프로그램에는 호스트 컴퓨터에서 게스트 가상 컴퓨터로 리디렉션할 수 없는 파일 형식 연결이 있습니다. 그러나 최종 사용자는 **파일**을 클릭 한 다음 게시 된 app-v 응용 프로그램에서 **열기** 를 클릭 하 여 이러한 파일 형식을 계속 액세스할 수 있습니다.

이러한 파일 형식 연결을 강제 전환 하려면 게스트 가상 컴퓨터의 명령 프롬프트에 다음을 입력 하 여 매핑된 파일 형식 연결에 대해 App-v 쿼리: **sftmime/QUERY OBJ: type**을 입력 합니다. 그런 다음 호스트 컴퓨터에서 해당 파일 형식 연결을 매핑합니다.

 

## <a href="" id="bkmk-coreimage"></a> 코어 이미지에서 응용 프로그램 추가 및 제거


MED-V 모범 사례로 간주 되지 않더라도 코어 이미지에서 직접 응용 프로그램을 추가 하 고 제거할 수 있습니다. 응용 프로그램을 추가 하거나 제거한 후에는 원래 배포 하는 것과 동일한 방법으로 엔터프라이즈에 MED-V 작업 영역을 다시 배포할 수 있습니다.

코어 이미지에서 응용 프로그램을 추가 하거나 제거 하는 방법에 대 한 자세한 내용은 [Windows 가상 PC 이미지에 응용 프로그램 설치](installing-applications-on-a-windows-virtual-pc-image.md)를 참조 하세요.

**중요**  이 방법은 응용 프로그램을 관리 하지 않는 것이 좋습니다. 코어 이미지에서 응용 프로그램을 추가 또는 제거 하 고 MED-V 작업 영역을 enterprise에 다시 배포 하는 경우 먼저 설치 프로그램이 다시 실행 되어야 하 고 가상 컴퓨터에 저장 된 모든 데이터가 손실 됩니다.

 

**참고**  응용 프로그램이 MED-V 작업 영역에 설치 되어 있는 경우에도 응용 프로그램이 최종 사용자에 게 제공 되기 전에 게시 해야 할 수 있습니다. 예를 들어 설치 시 **시작** 메뉴에 바로 가기가 자동으로 만들어지지 않은 경우 설치 된 응용 프로그램을 게시 해야 할 수 있습니다. 마찬가지로, 응용 프로그램의 게시를 취소 하려면 **시작** 메뉴에서 바로 가기를 수동으로 제거 해야 할 수 있습니다.

기본적으로 대부분의 응용 프로그램은 설치 된 시점에 게시 되며 바로 가기가 자동으로 만들어지고 활성화 됩니다.

 

## 관련 항목


[응용 프로그램 게시를 테스트하는 방법](how-to-test-application-publishing.md)

[MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





