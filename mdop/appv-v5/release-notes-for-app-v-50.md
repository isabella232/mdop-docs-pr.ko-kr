---
title: App-V 5.0 릴리스 정보
description: App-V 5.0 릴리스 정보
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813321"
---
# App-V 5.0 릴리스 정보


**이러한 릴리스 노트에서 특정 문제를 검색 하려면 CTRL + F를 누릅니다.**

App-v 5.0을 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요.

이 릴리스 정보에는 App-v 5.0을 설치 하는 데 필요한 정보가 포함 되어 있습니다. 릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다. 이러한 릴리스 노트와 다른 앱-V 5.0 설명서 사이에 차이가 있는 경우 최신 변경 내용을 신뢰할 수 있는 것으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## 제품 설명서 정보


App-v 5.0 설명서에 대 한 자세한 내용은 Microsoft TechNet의 App-v 5.0 홈 페이지를 참조 하세요.

## 피드백 제공


앱-V 5.0에 대 한 피드백에 관심이 있습니다. 귀하의 의견을 보낼 수 있습니다 <mdopdocs@microsoft.com> .

**참고**  이 이메일 주소는 지원 채널이 아니지만, 귀하의 문서와 제품 릴리스에서 향후에 변경 사항을 계획 하는 데 도움이 될 것입니다.

 

MDOP 및 추가 학습 리소스에 대 한 최신 정보는 [Mdop 정보 경험](https://go.microsoft.com/fwlink/p/?LinkId=236032) 페이지를 참조 하세요.

새 업데이트 또는 피드백을 제공 하는 방법에 대 한 자세한 내용은 [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 참조 하세요.

## 앱과 관련 하 여 알려진 문제점-V 5.0


이 섹션에서는 앱-V 5.0의 알려진 문제에 대 한 릴리스 정보를 소개 합니다.

### Server PowerShell cmdlet을 사용 하는 경우 패키지 추가를 종료할 수 없음

PowerShell을 사용 하 여 패키지를 추가 하는 경우 새 패키지 추가를 종료할 수 있는 방법이 없습니다.

해결 방법: 패키지 추가를 중지 하려면 마지막 패키지를 **추가한 후 enter 키를 누릅니다** .

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> 앱-V 5.0 클라이언트가 SSL 인증서가 해지 된 서버의 패키지를 거부 합니다.

HTTPS 프로토콜을 사용 하는 경우 App-v 5.0 클라이언트는 SSL 인증서가 해지 된 서버에서 패키지를 기본적으로 거부 합니다. 이 동작은 **VerifyCertificateRevocationList** 설정을 수정 하 여 구성을 통해 해제할 수 있습니다. 이 설정에 대 한 새 구성 적용은 App-v 5.0 서비스를 다시 시작할 때까지 적용 되지 않습니다.

해결 방법: App-v 5.0 서비스를 다시 시작 합니다.

## 릴리스 노트 저작권 정보


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune 및 WindowsPowerShell는 Microsoft의 회사 그룹의 상표입니다. 다른 모든 상표는 해당 소유자의 재산입니다.








## 관련 항목


[App-V 5.0 정보](about-app-v-50.md)

 

 





