---
title: 분산된 환경에 대한 App-V 관리 구성
description: 분산된 환경에 대한 App-V 관리 구성
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821913"
---
# 분산된 환경에 대한 App-V 관리 구성


특정 조직의 인프라를 설계할 때 app-v 관리 서버를 설치 하는 컴퓨터 이외의 컴퓨터에 App-v 관리 웹 서비스를 설치할 수 있습니다. 이러한 App-v 구성 요소를 구분 하는 일반적인 이유는 다음과 같습니다.

-   성능

-   안정성

-   가용성

-   확장성

관리 서버와 관리 웹 서비스를 분리 하려면 인프라가 올바르게 작동 하기 위해 추가 구성이 필요 합니다. 이러한 두 기능을 분리 했지만이 항목에 설명 된 절차를 완료 하지 않으면 관리 콘솔이 관리 웹 서비스에 연결 되지만 데이터 저장소를 통해 제대로 인증 되지 않습니다. 관리 콘솔이 제대로 로드 되지 않으며 관리자가 관리 작업을 완료할 수 없습니다.

관리 콘솔에서 전달 된 자격 증명을 사용 하 여 데이터 저장소에 액세스할 수 없기 때문에이 문제가 발생 합니다. 해결 방법은 관리 웹 서비스 서버를 "위임용으로 트러스트" 하도록 구성 하는 것입니다.

## Active Directory 도메인 서비스 구성


또한 Active Directory 도메인 서비스를 분산 환경에서 제대로 작동 하도록 구성 해야 합니다. 이 섹션에서는 Active Directory 도메인 서비스를 구성 하는 데 필요한 정보를 제공 합니다.

### SQL 서비스에서 로컬 시스템 계정을 사용 하는 경우

SQL 서비스에서 로컬 시스템 계정을 사용 하는 환경을 설정 하려면 위임용으로 신뢰할 수 있는 관리 웹 서비스의 컴퓨터 계정 속성을 변경 합니다. 이 작업을 수행 하는 방법에 대 한 자세한 절차는 [위임용으로 트러스트 되도록 서버를 구성 하는 방법](how-to-configure-the-server-to-be-trusted-for-delegation.md) 을 참조 하세요.

### SQL 서비스에서 도메인 기반 계정을 사용 하는 경우

SQL Server에서 도메인 기반 서비스 계정을 사용 하는 환경을 설정 하려면 다음을 포함 하 여 다양 한 요소가 적용 되는지 여부를 고려해 야 합니다.

-   SQL Server의 클러스터링

-   복제

-   자동화 된 작업

-   연결 된 서버

SQL 서비스가 도메인 기반 계정을 사용 하는 경우 Active Directory 도메인 서비스를 구성 하는 방법에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=151968> 하세요.

 

 





