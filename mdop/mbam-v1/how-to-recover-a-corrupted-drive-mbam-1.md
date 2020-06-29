---
title: 손상된 드라이브를 복구하는 방법
description: 손상된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812945"
---
# 손상된 드라이브를 복구하는 방법


BitLocker로 보호 되는 손상 된 드라이브를 복구 하려면 Microsoft BitLocker 관리 및 모니터링 (MBAM) 지원 센터 사용자가 복구 키 패키지 파일을 만들어야 합니다. 손상 된 드라이브를 포함 하는 컴퓨터에이 패키지 파일을 복사한 다음 드라이브를 복구 하는 데 사용할 수 있습니다. 이 작업을 수행 하려면 다음 절차를 사용 합니다.

**손상 된 드라이브 복구**

1.  MBAM 관리 웹 사이트를 엽니다.

2.  탐색 창에서 **드라이브 복구** 를 선택 합니다. 사용자의 도메인 이름과 사용자 이름, 드라이브 잠금 해제 이유, 사용자의 복구 암호 ID를 입력 합니다.

    **참고**  지원 센터 관리자 역할의 구성원 인 경우 사용자의 도메인 이름 또는 사용자 이름을 입력할 필요가 없습니다.

     

3.  **제출**을 클릭합니다. 복구 키가 표시 됩니다.

4.  **저장**을 클릭 한 다음 **복구 키 패키지**를 선택 합니다. 컴퓨터에 복구 키 패키지가 생성 됩니다.

5.  복구 키 패키지를 손상 된 드라이브가 있는 컴퓨터에 복사 합니다.

6.  관리자 권한 명령 프롬프트를 엽니다. 이렇게 하려면 **시작** 을 클릭 하 고 `cmd` **프로그램 및 파일 검색** 상자에 입력 합니다. 검색 결과 목록에서 **cmd.exe** 를 마우스 오른쪽 단추로 클릭 하 고 **관리자 권한으로 실행**을 선택 합니다.

7.  명령 프롬프트에서 다음을 입력 합니다.

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **참고**  &lt;명령에 있는 고정 드라이브에는 &gt; 손상 된 드라이브의 데이터 보다 더 크거나 같은 여유 공간이 있는 사용 가능한 저장소 장치를 지정 합니다. 손상 된 드라이브의 데이터를 복구 하 고 지정한 고정식 드라이브로 이동 합니다.

     

## 관련 항목


[MBAM을 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam.md)

 

 





