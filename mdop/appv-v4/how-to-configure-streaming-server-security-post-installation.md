---
title: Streaming Server 보안 사후 설치를 구성하는 방법
description: Streaming Server 보안 사후 설치를 구성하는 방법
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817903"
---
# Streaming Server 보안 사후 설치를 구성하는 방법


레지스트리를 통해 강화 된 보안을 위해 App-v 스트리밍 서버를 구성 합니다. App-v 관리 서버와 마찬가지로, 다음과 같은 사후 설치 절차를 완료 하기 전에 인증서를 서버 인증을 위한 올바른 EKU 식별자로 올바르게 프로 비전 해야 합니다.

**설치 후 스트리밍 서버 보안을 구성 하려면**

1.  MMC를 만들고 **인증서** 스냅인을 추가한 다음 **로컬 컴퓨터 인증서 저장소**를 선택 합니다.

2.  컴퓨터에 대 한 **개인** 인증서를 열고 app-v 용으로 프로 비전 된 인증서를 엽니다.

3.  **세부 정보** 탭에서 아래로 스크롤하여 세부 정보 창에서 해시를 복사 합니다.

4.  레지스트리 편집기를 열고을 탐색 `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` 합니다.

5.  값을 편집 `X509CertHash` 하 고 값 필드에 지문 해시를 붙여 넣은 다음 모든 공백을 제거 합니다. **확인** 을 클릭 하 여 편집을 수락 합니다.

6.  레지스트리 편집기에서을 탐색 `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` 합니다.

7.  "322" 이라는 새 **DWORD** 값을 만든 다음 10 진수 값을 322 또는 16 진수 값 (142)으로 입력 합니다.

8.  스트리밍 서비스를 다시 시작 합니다.

## 관련 항목


[관리 서버 보안 사후 설치를 구성하는 방법](how-to-configure-management-server-security-post-installation.md)

[인증서 권한 문제 해결](troubleshooting-certificate-permission-issues.md)

 

 





