---
title: Application Virtualization 시스템에 연결하는 방법
description: Application Virtualization 시스템에 연결하는 방법
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817713"
---
# Application Virtualization 시스템에 연결하는 방법


관리 콘솔을 사용 하 여 응용 프로그램, 파일 형식 연결, 패키지, 응용 프로그램 라이선스, 서버 그룹, 공급자 정책 및 관리자를 관리할 수 있으려면 먼저 Application Virtualization Server Management Console을 Application Virtualization 시스템에 연결 해야 합니다. 다음 절차에서는 콘솔을 Application Virtualization System에 연결 하기 위해 수행 해야 하는 단계를 간략하게 설명 합니다.

**Application Virtualization System에 연결 하려면**

1. **범위** 창에서 Application virtualization system 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **application Virtualization system에 연결을** 선택 합니다.

   **참고**  
   Application Virtualization server management에는 응용 프로그램 가상화 관리 콘솔, 관리 웹 서비스 및 SQL 데이터 저장소의 세 가지 구성 요소가 있습니다. 이러한 구성 요소가 여러 물리적 컴퓨터에 걸쳐 분산 되어 있는 경우 구성 요소가 시스템에서 통신 하도록 적절 하 게 보안을 구성 해야 합니다. 자세한 내용은 다음 설명서와 문서를 참조 하세요.

   [위임용으로 트러스트 되도록 서버를 구성 하는 방법](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)

   [Application Virtualization System에 대 한 계획 및 배포 가이드](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)

   [Application Virtualization System에 대 한 운영 가이드](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)

   Microsoft 기술 자료 [문서 930472](https://go.microsoft.com/fwlink/?LinkId=114647) (https://go.microsoft.com/fwlink/?LinkId=114647)

   Microsoft 기술 자료 [문서 930565](https://go.microsoft.com/fwlink/?LinkId=114648) (https://go.microsoft.com/fwlink/?LinkId=114648)

     

2. **Application Virtualization System에 연결** 대화 상자에서 필드를 완성 합니다.

   1. **웹 서비스 호스트 이름**-연결 하려는 Application Virtualization 시스템의 이름을 입력 하거나 **localhost** 를 입력 하 여 로컬 서버에 연결 합니다.

   2. 보안 **연결 사용**— 보안 연결을 사용 하 여 서버에 연결 하려면이 확인란을 선택 합니다.

   3. **포트 (port**)-연결에 사용할 포트 번호를 입력 합니다. **80** 는 기본 일반 포트 번호이 고 **443** 는 보안 포트 번호입니다.

   4. **현재 Windows 계정 사용**— 현재 windows 계정 자격 증명을 사용 하려면이 라디오 단추를 선택 합니다.

   5. **Windows 계정 지정**— 다른 사용자로 서버에 연결 하려는 경우이 라디오 단추를 선택 합니다.

   6. **이름 (Name**)- *DOMAIN\\username* 또는 username@domain 형식을 사용 하 여 새 사용자의 이름을 입력 합니다 <em> </em> .

   7. **비밀 번호**— 새 사용자에 게 해당 하는 비밀 번호를 입력 합니다.

3. **확인**을 클릭합니다.

## 관련 항목


[Application Virtualization Server Management Console에서 관리 작업을 수행하는 방법](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





