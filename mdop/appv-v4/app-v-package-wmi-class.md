---
title: App-V 패키지 WMI 클래스
description: App-V 패키지 WMI 클래스
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819798"
---
# App-V 패키지 WMI 클래스


Application Virtualization (App-v) 클라이언트에서 **Package** 클래스는 클라이언트의 모든 가상 패키지를 나타내는 WMI (Windows Management Instrumentation) 클래스입니다. 가상 패키지에는 여러 가상 응용 프로그램이 포함 될 수 있습니다.

## 구문


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## 특성


<a href="" id="name"></a>**이름**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

사용자에 게 친숙 한 가상 패키지 이름입니다.

<a href="" id="version"></a>**버전**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

가상 패키지의 버전입니다.

<a href="" id="packageguid"></a>**PackageGUID**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 키

패키지 구성 및 원본 파일의 GUID 식별자입니다.

<a href="" id="sftpath"></a>**SftPath**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

SFT 파일의 파일 경로입니다.

<a href="" id="totalsize"></a>**TotalSize**  
데이터 형식: **UInt64**

Access 형식: 읽기 전용

한정자: 없음

가상 패키지의 총 크기 (kb)입니다.

<a href="" id="cachedsize"></a>**CachedSize**  
데이터 형식: **UInt64**

Access 형식: 읽기 전용

한정자: 없음

가상 패키지에 대 한 캐시의 총 크기 (kb)입니다.

<a href="" id="launchsize"></a>**LaunchSize**  
데이터 형식: **UInt64**

Access 형식: 읽기 전용

한정자: 없음

가상 패키지의 기본 기능 블록의 총 크기 (kb)입니다.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
데이터 형식: **UInt64**

Access 형식: 읽기 전용

한정자: 없음

캐시 된 가상 패키지의 기본 기능 블록의 총 크기 (kb)입니다.

<a href="" id="inuse"></a>**InUse**  
데이터 형식: **Boolean**

Access 형식: 읽기 전용

한정자: 없음

가상 패키지의 가상 응용 프로그램이 실행 되 고 있으면 **true** 이 고, 그렇지 않으면 false입니다. 그렇지 않으면 **false**입니다.

<a href="" id="locked"></a>**잠김**  
데이터 형식: **Boolean**

Access 형식: 읽기 전용

한정자: 없음

가상 패키지가 잠겨 있으면 **true** 이 고, 그렇지 않으면 false입니다. 그렇지 않으면 **false**입니다.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
데이터 형식: **UInt16**

Access 형식: 읽기 전용

한정자: 없음

캐시 파일의 백분율입니다. 다음 공식을 기준으로 합니다. CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**버전 Guid**  
데이터 형식: **문자열**

Access 형식: 읽기 전용

한정자: 없음

패키지 버전의 GUID 식별자입니다.

 

 





