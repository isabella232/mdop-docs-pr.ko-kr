---
title: Microsoft 고급 그룹 정책 관리 4.0 릴리스 정보
description: Microsoft 고급 그룹 정책 관리 4.0 릴리스 정보
author: dansimp
ms.assetid: 44c19e61-c8e8-48aa-a2c2-20396d14d5bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c4a279893d4da4121e422af99e7c1708a0126b4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820393"
---
# Microsoft 고급 그룹 정책 관리 4.0 릴리스 정보


2009년 10월

## Microsoft 고급 그룹 정책 관리 4.0 정보


Microsoft AGPM (고급 그룹 정책 관리) 4.0는 GPMC (그룹 정책 관리) 콘솔의 기능을 확장 합니다. AGPM은 광범위 한 변경 제어와 Gpo (그룹 정책 개체)의 향상 된 관리를 제공 합니다.

다음 문서를 사용 하 여 AGPM 4.0을 시작 하는 데 도움을 받을 수 있습니다.

-   AGPM의 기능에 대 한 개요는 [Microsoft 고급 그룹 정책 관리 개요](https://go.microsoft.com/fwlink/?LinkID=162671) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=162671) .

-   AGPM 4.0이 AGPM 3.0과 어떻게 다른 지에 대 한 자세한 내용은 [agpm 4.0 ()의 새로운 기능](https://go.microsoft.com/fwlink/?LinkId=160058) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=160058) .

-   AGPM 4.0, AGPM 3.0 또는 AGPM 2.5이 사용자 환경에 적합 한지 여부를 확인 하는 방법에 대 한 지침은 [설치할 AGPM 버전 선택](https://go.microsoft.com/fwlink/?LinkId=145981) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=145981) .

-   Agpm을 설치 하는 방법과 AGPM을 사용 하기 위한 샘플 시나리오에 대 한 기본 지침은 [Microsoft 고급 그룹 정책 관리 4.0 ()에 대 한 단계별 가이드](https://go.microsoft.com/fwlink/?LinkID=153505) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=153505) . 이 가이드는 주로 평가자와 최초 사용자를 위한 것입니다.

-   이전 버전의 AGPM 또는 조직에서 AGPM 배포를 계획 하는 방법에 대 한 자세한 지침을 업그레이드 하는 방법에 대 한 자세한 내용은 [Microsoft 고급 그룹 정책 관리 4.0 ()에 대 한 계획 가이드](https://go.microsoft.com/fwlink/?LinkID=156883) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=156883) .

-   AGPM을 사용 하 여 특정 작업을 수행 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리 4.0 도움말을 참조 하세요 .이에 대 한 자세한 내용은 [agpm 4.0 ()에 대 한 운영 가이드](https://go.microsoft.com/fwlink/?LinkId=159872) 로 TechNet 에서도 사용할 수 있습니다 https://go.microsoft.com/fwlink/?LinkId=159872)

## 추가 정보


AGPM에 대 한 자세한 내용은 다음을 참고 하세요.

-   [고급 그룹 정책 관리 TechNet 라이브러리](https://go.microsoft.com/fwlink/?LinkID=146846) (https://go.microsoft.com/fwlink/?LinkID=146846)

-   [Microsoft 데스크톱 최적화 팩 TechCenter](https://go.microsoft.com/fwlink/?LinkId=159870) (https://www.microsoft.com/technet/mdop)

-   [그룹 정책 TechCenter](https://go.microsoft.com/fwlink/?LinkId=145531) (https://www.microsoft.com/gp)

## 사용자 의견 제공


AGPM에 대 한 피드백 또는 질문을 [그룹 정책 포럼](https://go.microsoft.com/fwlink/?LinkId=145532) ()에 게시할 수 있습니다 https://go.microsoft.com/fwlink/?LinkId=145532) .

## AGPM 4.0의 알려진 문제점


### 프로덕션에서 가져오기 명령은 체크 아웃 된 GPO로 설정을 가져오지 않습니다.

프로덕션 환경에서 GPO를 편집 하는 경우 프로덕션에서 GPO를 가져와 오프 라인 보관 파일의 GPO를 업데이트 해야 합니다. **프로덕션에서 가져오기** 명령을 사용 하면 편집을 마치기 전에 최종 프로덕션 백업을 수행 하 여 필요한 경우 프로덕션 백업으로 롤백할 수 있습니다.

**프로덕션에서 가져오기** 명령을 실행할 때 GPO가 체크 아웃 된 경우 프로덕션 변경 내용이 체크 아웃 된 GPO 버전에 통합 되지 않습니다. 그러나 해당 버전을 편집할 수 없는 경우에도 가져온 GPO 버전이 GPO의 기록에 추가 됩니다. GPO가 체크 인 되 면 해당 버전은 보관 된 가져오기 버전으로 대체 되지만 GPO의 기록에서 사용할 수 있습니다.

**해결 방법:** 프로덕션에서 가져오기 전에 GPO가 체크 되어 있는지 확인 합니다. 가져오기 전에 GPO가 체크 인 되지 않은 경우 **체크 아웃 취소** 명령을 사용 하 여 변경 내용을 취소 하 고 프로덕션에서 가져온 gpo 버전으로 롤백할 수 있습니다.

### 체크 아웃 된 Gpo는 여러 사이트의 Active Directory 토폴로지를 사용 하는 환경에서 몇 분 동안 편집할 수 없습니다.

AGPM은 클라이언트/서버 모델을 사용 합니다. AGPM 서버와 AGPM 클라이언트는 각각 그룹 정책 작업을 위해 가장 가까운 도메인 컨트롤러를 결정 합니다. AGPM 클라이언트를 사용 하 여 GPO를 체크 아웃 하는 경우 사실상 오프 라인 보관 함에서 SYSVOL 폴더의 임시 폴더로 GPO를 확인 하는 AGPM 서버입니다.

AGPM 서버와 AGPM 클라이언트가 서로 다른 사이트에 있는 경우 임시 체크 아웃 된 GPO가 로컬 사이트의 도메인 컨트롤러에 없거나, 몇 분 동안 또는 SYSVOL 복제 대기 시간으로 최대 30 분이 될 수 있습니다. 이러한 상황에서는 체크 아웃 된 GPO의 SYSVOL 복제가 발생할 때까지 AGPM 클라이언트의 GPMC를 사용 하 여 체크 아웃 된 GPO를 편집할 수 없습니다.

**해결 방법:** 가장 좋은 방법은 사용자가 해당 사용자가 연결 하는 AGPM 서버와 동일한 사이트에 AGPM 클라이언트를 배치 하 여 체크 아웃 된 GPO를 편집 하기 전에 SYSVOL 복제가 발생할 때까지 기다릴 필요가 없다는 것입니다.

### 계정에 보관에 대 한 사용 권한이 없으면 AGPM이 백업 제한을 읽을 수 없음

AGPM 클라이언트에서 AGPM 보관에 대 한 사용 권한이 위임 되지 않은 계정을 사용 하 여 로그온 하는 경우 GPMC (그룹 정책 관리 콘솔)를 시작한 다음 **제어권 변경을**클릭 하면 다음과 같은 오류가 나타납니다.

``` syntax
Failed to read backup purge limit for this domain. 

The following error occurred: 
You do not have sufficient permissions to perform this operation. 
Microsoft.Agpm.AccessDeniedException (80070005)
```

**해결 방법:** AGPM 관리자 (모든 권한)에 게 문의 하 여 계정에 대해 AGPM에 대 한 액세스 권한을 위임 하도록 요청 합니다. AGPM 관리자 인 경우, 추가 계정에 대 한 액세스를 위임할 수 있도록 AGPM 관리자 역할이 할당 된 계정을 사용 하 여 로그온 합니다. 자세한 내용은 AGPM 도움말의 "보관에 도메인 수준 액세스 위임"을 참조 하세요.

## 릴리스 노트 저작권 정보


URL 및 기타 인터넷 웹 사이트 참조를 포함 하 여,이 문서의 정보는 예 고 없이 변경 될 수 있으며, 정보 제공 목적 으로만 제공 됩니다. 이 문서의 사용 또는 결과에 따른 모든 위험은 사용자에 게 남아 있으며, Microsoft Corporation은 명시적 이거나 묵시적인 어떠한 보증도 하지 않습니다. 용례에 용례를 보여 주는 회사, 조직, 제품, 사람 및 이벤트는 실제 데이터가 아닙니다. 어떠한 실제 회사, 기관, 제품, 사람 또는 이벤트와도 연관 시킬 의도가 없으며 그렇게 유추 해서도 안 됩니다. 해당 저작권법을 준수하는 것은 사용자의 책임입니다. 저작권에서의 권리와는 별도로, 이 설명서의 어떠한 부분도 Microsoft의 명시적인 서면 승인 없이는 어떠한 형식이나 수단(전자적, 기계적, 복사기에 의한 복사, 디스크 복사 또는 다른 방법) 또는 목적으로도 복제되거나, 검색 시스템에 저장 또는 도입되거나, 전송될 수 없습니다.

Microsoft는 이 설명서 본안에 관련된 특허권, 상표권, 저작권, 또는 기타 지적 재산권 등을 보유할 수도 있습니다. 서면 사용권 계약에 따라 Microsoft로부터 귀하에게 명시적으로 제공된 권리 이외에, 이 설명서의 제공은 귀하에게 이러한 특허권, 상표권, 저작권, 또는 기타 지적 재산권 등에 대한 어떠한 사용권도 허용하지 않습니다.



Microsoft, MS-DOS, Windows, WindowsServer 및 Windows Vista는 U.S.A. 및/또는 기타 국가에서 MicrosoftCorporation의 등록 상표 또는 상표 중 하나입니다.

여기에 언급 된 실제 회사 및 제품의 이름은 해당 소유자의 상표일 수 있습니다.

 

 





