---
title: App-V 응용 프로그램 WMI 클래스
description: App-V 응용 프로그램 WMI 클래스
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822323"
---
# App-V 응용 프로그램 WMI 클래스


Application Virtualization (App-v) 클라이언트에서 **응용 프로그램** 클래스는 클라이언트의 모든 가상 응용 프로그램을 나타내는 WMI (Windows Management Instrumentation) 클래스입니다.

다음 구문은 MOF (관리 개체 형식) 코드에서 간소화 되었습니다. 코드에는 상속 된 속성이 모두 포함 됩니다.

## 구문


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## 요구 사항


## 특성


<a href="" id="name"></a>**이름**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 키

가상 응용 프로그램의 표시 이름입니다.

<a href="" id="version"></a>**버전**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 키

가상 응용 프로그램의 버전입니다.

<a href="" id="packageguid"></a>**PackageGUID**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

가상 응용 프로그램이 연결 된 패키지의 GUID입니다.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
데이터 형식: **날짜/시간**

Access 형식: 읽기 전용

한정자: 없음

가상 응용 프로그램을 마지막으로 시작한 날짜와 시간입니다.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
데이터 형식: **UInt32**

Access 형식: 읽기 전용

한정자: 없음

직접 시작 된 가상 응용 프로그램의 실행 중인 인스턴스 수입니다.

<a href="" id="loading"></a>**불러오는 중**  
데이터 형식: **Boolean**

Access 형식: 읽기 전용

한정자: 없음

가상 응용 프로그램이 시작 되는 경우 **true** 이 고, 그렇지 않으면 false입니다. 그렇지 않으면 **false**입니다.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

App-v 클라이언트에 등록 된 OSD 파일의 원래 파일 경로입니다.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

App-v 클라이언트가 OSD 파일을 로컬로 캐시 한 경우 OSD 파일의 파일 경로입니다.

 

 





