---
title: 이미지 웹 배포 서버를 구성하는 방법
description: 이미지 웹 배포 서버를 구성하는 방법
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825158"
---
# 이미지 웹 배포 서버를 구성하는 방법


이미지 저장소는 이미지 배포에 사용 되는 선택적 서버 (관리자가 새 이미지 및 클라이언트 컴퓨터를 15 분 마다 확인 하 고 새 이미지를 사용할 수 있는 경우에는 서버를 업데이트 하는 경우)입니다.

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


이미지 배포 서버에는 다음이 필요 합니다.

-   IIS (인터넷 정보 서비스)-자세한 내용은 [인터넷 정보 서비스](https://go.microsoft.com/fwlink/?LinkId=142995)를 참조 하세요.

    IIS를 설치 하는 동안 역할 서비스를 추가할 때 다음과 같은 지원 되는 인증 방법을 선택 합니다.

    -   **기본 인증**

    -   **Windows 인증**

    -   **클라이언트 인증서 매핑 인증**

    IIS를 구성할 때 다음을 포함 합니다.

    -   **MEDVImages**라는 별칭을 사용 하 여 가상 디렉터리를 추가 합니다. 실제 경로는 이미지의 위치를 가리켜야 합니다.

    -   비트를 사용 합니다.

    -   다음 MIME 형식을 추가 합니다.

        -   **ckm (응용 프로그램/8 진수-스트림)**

        -   **. index (응용 프로그램/8 진수-스트림**)

    -   MED-V 사이트에서 **모든 사용자**에 게 읽기 권한을 추가 합니다.

    -   IIS를 다시 시작 합니다.

-   IIS 용 BITS Server Extensions-자세한 내용은 [Bits Server Extensions 설치](https://go.microsoft.com/fwlink/?LinkId=142996)를 참조 하세요.

## 관련 항목


[지원되는 구성](supported-configurationsmedv-orientation.md)

[MED-V 이미지 리포지토리 디자인](design-the-med-v-image-repositories.md)

 

 





