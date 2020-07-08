---
title: 명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법
description: 명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817898"
---
# 명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법


명령줄을 사용 하 여 설치 하는 동안 Application Virtualization (App-v) 클라이언트를 배포 하 고 구성한 후에는 클라이언트 구성 설정을 하나 이상 변경 해야 할 수 있습니다. 다음 방법 중 하나를 사용 하 여 적절 한 레지스트리 키를 편집 하 여이 작업을 수행 합니다.

-   레지스트리 편집기 직접 사용

-   .Reg 파일 사용

-   VBScript 또는 Windows PowerShell과 같은 스크립트 언어 사용

사용할 수 있는 ADM 서식 파일도 있습니다. ADM 템플릿에 대 한 자세한 내용은을 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=121835> .

**주의**  사항 오류가 발생 하 여 컴퓨터를 사용할 수 없는 상태가 되는 것 이기 때문에 레지스트리를 편집할 때는 주의를 기울여야 합니다. 레지스트리 편집과 관련 된 표준 비즈니스 관행을 준수 해야 합니다. 프로덕션 컴퓨터에 배포 하기 전에 테스트 환경에서 모든 제안 된 변경 내용을 철저히 테스트 합니다.

 

## 이 섹션의 내용


**중요**  64 비트 컴퓨터에서 다음 섹션에 설명 된 키와 값이 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client. 아래에 있습니다.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[FileSystem 캐시를 다시 설정하는 방법](how-to-reset-the-filesystem-cache.md)  
파일 시스템 캐시를 다시 설정 하는 데 필요한 정보를 제공 합니다.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[FileSystem 캐시의 크기를 변경하는 방법](how-to-change-the-size-of-the-filesystem-cache.md)  
캐시 크기를 변경할 수 있는 방법에 대해 설명 합니다.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[캐시 공간 관리 기능을 사용하는 방법](how-to-use-the-cache-space-management-feature.md)  
캐시 공간 관리 기능을 구성할 수 있는 방법에 대해 설명 합니다.

<a href="" id="how-to-configure-the-client-log-file"></a>[클라이언트 로그 파일을 구성하는 방법](how-to-configure-the-client-log-file.md)  
클라이언트 로그 파일을 제어 하는 다양 한 레지스트리 키 값과이를 변경할 수 있는 방법을 설명 합니다.

<a href="" id="how-to-configure-user-permissions"></a>[사용자 권한을 구성하는 방법](how-to-configure-user-permissions.md)  
사용자 권한을 제어 하는 레지스트리 키를 식별 하 고 일부 권한을 변경할 수 있는 방법의 예를 제공 합니다.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[응용 프로그램 패키지 검색에 대한 클라이언트를 구성하는 방법](how-to-configure-the-client-for-application-package-retrieval.md)  
여러 원본에서 패키지 콘텐츠, 아이콘 및 파일 형식 연결을 검색 하도록 클라이언트를 구성 하는 방법을 설명 하 고 올바른 경로 형식에 대 한 몇 가지 예제를 제공 합니다.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법](how-to-configure-the-client-for-disconnected-operation-mode.md)  
연결이 끊긴 작업 모드와 연결 된 다양 한 설정을 구성 하는 방법에 대 한 정보를 제공 합니다.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[바로 가기 및 파일 형식 연결 동작을 구성하는 방법](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
App-v 클라이언트의 바로 가기 및 파일 형식 연결을 제어 하는 레지스트리 키 값에 대해 설명 하 고이를 구성 하는 방법에 대 한 세부 정보를 제공 합니다.

## 관련 항목


[Application Virtualization Client](application-virtualization-client.md)

 

 





