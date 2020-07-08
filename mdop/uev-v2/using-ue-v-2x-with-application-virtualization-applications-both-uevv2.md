---
title: UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램
description: UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827273"
---
# UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1은 App-v 패키지 또는 UE-V 템플릿에 대 한 필수 수정 없이 Microsoft Application Virtualization (App-v) 응용 프로그램을 지원 합니다. 그러나 UE-V 생성기를 가상화 된 App-v 응용 프로그램에서 직접 실행할 수 없기 때문에 추가 단계가 필요 합니다. 대신 응용 프로그램을 로컬로 설치 하 고 템플릿을 생성 한 다음 해당 템플릿을 가상화 된 응용 프로그램에 적용 해야 합니다. UE-V를 통해 앱-V 4.5, App-v 4.6 및 App-v 5.0 패키지를 지원 합니다.

## App-v 응용 프로그램에 대 한 UE-V 설정 동기화


UE-V를 사용 하 여 응용 프로그램이 로컬로 설치 되는지 여부와 상관 없이 응용 프로그램이 프로그램 이름으로 열리거나, 선택적으로 파일 버전 번호와 제품 버전 번호로 열리는 시점을 모니터 합니다. 응용 프로그램이 시작 되 면 UE-V 프로세스를 모니터링 하 고 사용자 설정 저장소 경로에 저장 된 설정을 적용 한 다음 응용 프로그램을 정상적으로 시작할 수 있습니다. UE-V를 통해 app-v 응용 프로그램을 모니터 하 고, App-v 컴퓨팅 환경 외부의 실제 위치가 아닌 가상화 된 위치로 관련 파일 및 레지스트리 경로를 자동으로 변환 합니다.

 **가상화 된 응용 프로그램에 대 한 설정 동기화를 구현 하려면**

1.  UE-V Generator를 실행 하 여 컴퓨터 간에 동기화 할 설정을 포함 하는 로컬로 설치 된 응용 프로그램의 설정을 수집 합니다. 이 프로세스는 설정 위치 템플릿을 만듭니다. Microsoft Office 2010 서식 파일과 같은 기본 제공 서식 파일을 사용 하는 경우에는이 단계를 건너뛰십시오. UE-V 생성기를 실행 하는 방법에 대 한 자세한 내용은 [사용자 지정 응용 프로그램에 ue-v: x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates)를 참조 하세요.

2.  아직 수행 하지 않은 경우 App-v 응용 프로그램 패키지를 설치 합니다.

3.  설정 서식 파일 카탈로그의 위치에 서식 파일을 게시 하거나 Windows PowerShell cmdlet을 사용 하 여 수동으로 서식 파일을 설치 `Register-UEVTemplate` 합니다.

    **참고**  새로 만든 서식 파일을 설정 서식 파일 카탈로그에 게시 하는 경우 클라이언트는 동기화 공급자가 설정을 업데이트할 때까지 해당 템플릿을 받지 않습니다. 이 프로세스를 수동으로 시작 하려면 **작업 스케줄러**를 열고, **작업 스케줄러 라이브러리**를 확장 하 고, **Microsoft**를 확장 하 고, **ue-v**를 확장 합니다. 결과 창에서 **서식 파일 자동 업데이트**를 마우스 오른쪽 단추로 클릭 한 다음 **실행**을 클릭 합니다.

     

4.  App-v 패키지를 시작 합니다.






## 관련 항목


[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

 

 





