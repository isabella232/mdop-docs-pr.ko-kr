---
title: 인증서를 구성하여 보안 스트리밍 지원
description: 인증서를 구성하여 보안 스트리밍 지원
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821893"
---
# 인증서를 구성하여 보안 스트리밍 지원


기본적으로 App-v 서비스는 네트워크 서비스 계정에서 실행 됩니다. 그러나 Active Directory 도메인 서비스에서 서비스 계정을 만들고 네트워크 서비스 계정을 Active Directory 도메인 계정으로 바꿀 수 있습니다.

서비스를 실행 하는 보안 컨텍스트는 보안 강화 통신을 구성 하는 데 중요 합니다. 이 보안 컨텍스트에는 인증서 개인 키에 대 한 읽기 권한이 있어야 합니다. App-v 서버에 대 한 PKCS #10 CSR ( *인증서 서명 요청* )이 생성 되 면 Windows *암호화 서비스 공급자* 가 호출 되 고 개인 키가 생성 됩니다. 개인 키는 시스템 및 관리자 계정에만 부여 된 사용 권한으로 보안이 유지 됩니다.

TLS 보안 통신에 필요한 개인 키에 대 한 액세스 제어 목록 (Acl)을 앱-V 관리 또는 스트리밍 서버에서 수정 하도록 허용 해야 합니다.

## 인증서 구하기 및 설치


App-v에 대 한 인증서를 구하고 설치 하는 시나리오는 다음과 같습니다.

-   내부 PKI (공개 키 인프라).

-   타사 인증서 발급 CA (인증 기관)

    **참고**  타사 CA에서 인증서를 구해야 하는 경우 해당 CA의 웹 사이트에서 제공 하는 설명서를 따르세요.

     

PKI 인프라를 배포한 경우 PKI 관리자에 게 문의 하 여이 항목에서 설명 하는 요구 사항을 준수 하는 인증서를 획득 합니다. PKI 인프라를 사용할 수 없는 경우 타사 CA를 사용 하 여 유효한 인증서를 얻습니다.

인증서를 구하고 설치 하는 단계별 지침은을 참조 <https://go.microsoft.com/fwlink/?LinkId=151969> 하세요.

## 관련 항목


보안 스트리밍을 지원 하도록 인증서 구성 [관리 서버 또는 스트리밍 서버를 지원 하기 위해 개인 키 사용 권한을 수정 하는 방법](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





