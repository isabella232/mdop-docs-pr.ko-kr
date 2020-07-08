---
title: 인증서 권한 문제 해결
description: 인증서 권한 문제 해결
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815208"
---
# 인증서 권한 문제 해결


App-v 4.5 설치 후 개인 키가 네트워크 서비스에 대 한 적절 한 ACL로 구성 되지 않은 경우 NT 이벤트 로그에 이벤트가 기록 되 고 항목이 파일에 저장 됩니다 `Sft-server.log` .

## 오류 메시지


### Windows Server2003

이벤트 ID 36870-SSL 서버 자격 증명 개인 키에 액세스 하려고 할 때 심각한 오류가 발생 했습니다. 암호화 모듈에서 반환 된 오류 코드는 0x80090016입니다.

### Windows Server2008

이벤트 ID 36870-SSL 서버 자격 증명 개인 키에 액세스 하려고 할 때 심각한 오류가 발생 했습니다. 암호화 모듈에서 반환 된 오류 코드는 0x8009030d입니다.

## Sft-server


다음 오류는 `sft-server.log` 디렉터리에 있는 파일에 저장 됩니다 `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` .

인증서를 로드할 수 없습니다. 오류 코드 \ [-2146893043 \]. 네트워크 서비스 계정에 인증서 및 해당 개인 키 파일에 대 한 적절 한 액세스 권한이 있는지 확인 합니다.

 

 





