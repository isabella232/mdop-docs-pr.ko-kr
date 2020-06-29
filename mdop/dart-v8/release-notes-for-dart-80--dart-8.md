---
title: DaRT 8.0 릴리스 정보
description: DaRT 8.0 릴리스 정보
author: dansimp
ms.assetid: e8b373c8-7aa5-4930-a8f9-743d26145dad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 894708585ff4006c37085e71f365690b8424d43e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824788"
---
# DaRT 8.0 릴리스 정보


**이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.**

Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0을 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요.

이 릴리스 정보에는 DaRT 8.0를 성공적으로 설치 하는 데 필요한 정보가 들어 있습니다. 릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다. 이러한 릴리스 정보와 기타 DaRT 설명서가 서로 다르면 최신 변경 내용을 정식으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

DaRT 소프트웨어를 다운로드 하려면 MDOP를 [얻는 방법을](https://go.microsoft.com/fwlink/?LinkId=322049)참조 하세요.

## 제품 설명서 정보


DaRT 설명서에 대 한 자세한 내용은 Microsoft TechNet의 [DaRT 홈페이지](https://go.microsoft.com/fwlink/?LinkID=252096) 를 참조 하세요.

다운로드 가능한 DaRT 문서의 복사본을 얻으려면 <https://go.microsoft.com/fwlink/?LinkID=267420> Microsoft 다운로드 센터에서 참조 하세요.

## 사용자 의견 제공


DaRT 8.0에 대 한 피드백에 관심이 있습니다. 귀하의 의견을 보낼 수 있습니다 <mdopdocs@microsoft.com> .

**참고**  이 전자 메일 주소는 지원 채널이 아니지만, 귀하의 의견은 설명서 및 제품 릴리스에 대 한 향후 변경 사항을 계획 하는 데 도움이 됩니다.

 

MDOP 및 추가 학습 리소스에 대 한 최신 정보는 [Mdop 정보 경험](https://go.microsoft.com/fwlink/p/?LinkId=236032) 페이지를 참조 하세요.

새 업데이트 또는 피드백을 제공 하는 방법에 대 한 자세한 내용은 [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 참조 하세요.

## DaRT 8.0의 알려진 문제점


### Locksmith 또는 레지스트리 편집기를 실행 하면 시스템 복원이 실패 함

Locksmith, 레지스트리 편집기 및 기타 도구를 실행 하면 시스템 복원이 실패 합니다.

**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 시스템 복원을 시작 합니다.

### Locksmith 또는 컴퓨터 관리를 시작 하 고 닫은 후 SFC scan이 실행 되지 않음

Locksmith 또는 컴퓨터 관리 도구를 시작 하 고 닫으면 시스템 파일 검사기가 실행 되지 않습니다.

**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 SFC를 시작 합니다.

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> ADK가 설치 되지 않은 경우 DaRT 설치 프로그램이 실패 하지 않음

명령줄을 사용 하 여 MSI를 실행 하 여 DaRT 8.0를 설치 하는 경우에는 DaRT가 설치 되지 않은 것이 좋습니다 설치에 실패 합니다. 현재 DaRT 8.0 설치 관리자는 DaRT 8.0 복구 이미지를 제외한 모든 구성 요소를 설치 합니다.

**해결 방법:** 않아야.

### Locksmith, RegEdit, 크래시 분석기, 컴퓨터 관리가 실행 된 후에는 Defender를 실행할 수 없습니다.

Locksmith, RegEdit, 충돌 분석기 및 컴퓨터 관리를 이미 실행 한 경우에는 Defender가 실행 되지 않습니다.

**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 Defender를 시작 합니다.

### Defender가 시작 하는 데 오랜 시간이 걸릴 수 있음

Defender를 실행 하는 데 몇 분이 소요 될 수 있습니다. 진행률 표시줄에 현재 로드 상태가 표시 됩니다.

**해결 방법:** 않아야.

## 릴리스 노트 저작권 정보


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune 및 WindowsPowerShell는 Microsoft의 회사 그룹의 상표입니다. 다른 모든 상표는 해당 소유자의 재산입니다.



## 관련 항목


[DaRT 8.0 정보](about-dart-80-dart-8.md)

 

 





