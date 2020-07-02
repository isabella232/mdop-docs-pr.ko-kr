---
title: 진단 및 복구 도구 집합 8 관리자 가이드
description: 진단 및 복구 도구 집합 8 관리자 가이드
author: dansimp
ms.assetid: 33685dd7-844f-4864-b504-3ef384ef01de
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2017
ms.openlocfilehash: c4f4e7cb49b89759acc4c3c738ff74a4a197b120
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795738"
---
# 진단 및 복구 도구 집합 8 관리자 가이드


Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0을 통해 시작할 수 없거나 예상 대로 시작 하는 데 문제가 있는 컴퓨터를 진단 하 고 복구할 수 있습니다. DaRT 8.0를 사용 하 여 사용할 수 없게 되는 최종 사용자 컴퓨터를 복구 하 고, 문제의 예상 되는 원인을 진단 하 고, 부팅 불가능 또는 잠긴 컴퓨터를 빠르게 복구 합니다. 필요한 경우 컴퓨터가 온라인 상태가 아닌 경우에도 중요 한 손실 된 파일을 빠르게 복원 하 고 맬웨어를 검색 및 제거할 수도 있습니다.

DaRT 8.0에서는 ISO (국제 표준화 기구) 및 WIM (Windows Imaging) 파일 형식으로 DaRT 복구 이미지를 만들고 이미지를 CD, DVD 또는 USB에 구울 수 있습니다. 그런 다음 복구 이미지 파일을 사용 하 여 로컬 또는 원격 파티션이나 복구 파티션에 배포할 수 있습니다.

DaRT 8.0는 소프트웨어 설치 비용을 줄이고, 응용 프로그램을 서비스로 제공 하 고, 엔터프라이즈 데스크톱 환경을 관리 하 고 제어 하는 데 도움이 되는 소프트웨어 보증 고객에 게 제공 되는 동적인 솔루션 인 MDOP (Microsoft 데스크톱 최적화 팩)의 중요 한 부분입니다.

<a href="" id="getting-started-with-dart-8-0"></a>[DaRT 8.0 시작](getting-started-with-dart-80-dart-8.md)  

[DaRT 8.0 정보](about-dart-80-dart-8.md) **|** [DaRT 8.0](release-notes-for-dart-80--dart-8.md) **|** 릴리스 정보 [DaRT 8.0 SP1 정보](about-dart-80-sp1.md) **|** [DaRT 8.0 SP1](release-notes-for-dart-80-sp1.md) **|** 릴리스 정보 [DaRT 8.1 정보](about-dart-81.md) **|** [DaRT 8.1](release-notes-for-dart-81.md) **|** 릴리스 정보 [DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md) **|** 의 도구 개요 [DaRT 8.0의 접근성](accessibility-for-dart-80-dart-8.md)

<a href="" id="planning-for-dart-8-0"></a>[DaRT 8.0 계획](planning-for-dart-80-dart-8.md)  

[DaRT 8.0](planning-to-deploy-dart-80-dart-8.md) **|** 배포 계획 [DaRT 8.0 지원 되는 구성](dart-80-supported-configurations-dart-8.md) **|** [DaRT 8.0 복구 이미지](planning-to-create-the-dart-80-recovery-image-dart-8.md) **|** 만들기 계획 [DaRT 8.0 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md) **|** [DaRT 8.0 계획 점검 목록](dart-80-planning-checklist-dart-8.md)

<a href="" id="deploying-dart-8-0"></a>[DaRT 8.0 배포](deploying-dart-80-dart-8.md)  

[관리자 컴퓨터](deploying-dart-80-to-administrator-computers-dart-8.md) **|** 에 DaRT 8.0 배포 [DaRT 8.0 복구 이미지 만들기](creating-the-dart-80-recovery-image-dart-8.md) **|** [DaRT 복구 이미지 배포](deploying-the-dart-recovery-image-dart-8.md) **|** [DaRT 8.0 배포 검사 목록](dart-80-deployment-checklist-dart-8.md)

<a href="" id="operations-for-dart-8-0"></a>[DaRT 8.0 작업](operations-for-dart-80-dart-8.md)  

[DaRT 8.0](recovering-computers-using-dart-80-dart-8.md) **|** 를 사용 하 여 컴퓨터 복구 [충돌 분석기](diagnosing-system-failures-with-crash-analyzer--dart-8.md) **|** 를 사용 하 여 시스템 오류 진단 [DaRT 8.0](security-and-privacy-for-dart-80-dart-8.md) **|** 보안 및 개인 정보 취급 방침 [PowerShell을 사용 하 여 DaRT 8.0 관리](administering-dart-80-using-powershell-dart-8.md)

<a href="" id="technical-reference-for-dart-8-0"></a>[DaRT 8.0에 대한 기술 참조](technical-reference-for-dart-80-new-ia.md)  

[Microsoft 진단 및 복구 도구 집합 (DaRT) 사용자는 맬웨어 감지를 위해 Microsoft Defender Offline (WDO)을 사용 해야 합니다-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md)

<a href="" id="troubleshooting-dart-8-0"></a>[DaRT 8.0 문제 해결](troubleshooting-dart-80-dart-8.md)  

### 추가 정보

<a href="" id="how-do-i-get-mdop"></a>[MDOP를 얻는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)  
DaRT를 다운로드 하는 방법에 대 한 정보를 얻을 수 있습니다.

<a href="" id="release-notes-for-dart-8-0"></a>[DaRT 8.0 릴리스 정보](release-notes-for-dart-80--dart-8.md)  
업데이트 된 제품 정보 및 DaRT 8.0에 대 한 알려진 문제점을 확인 합니다.

<a href="" id="mdop-techcenter-page"></a>[MDOP TechCenter 페이지](https://go.microsoft.com/fwlink/p/?LinkId=225286)  
최신 MDOP 정보 및 리소스에 대해 알아보세요.

<a href="" id="mdop-information-experience"></a>[MDOP 정보 환경](https://go.microsoft.com/fwlink/p/?LinkId=236032)  
MDOP 기술에 대 한 설명서, 비디오 및 기타 리소스를 찾습니다. 또한 [사용자 의견을 보내거나](mailto:MDOPDocs@microsoft.com) [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)에서 팔 로우 하 여 업데이트에 대해 알아볼 수 있습니다.

 

 





