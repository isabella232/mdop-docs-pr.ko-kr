---
title: Management Console 설치 방법
description: Management Console 설치 방법
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817303"
---
# Management Console 설치 방법


다음 절차를 사용 하 여 네트워크의 대상 컴퓨터에 응용 프로그램 가상화 관리 콘솔을 설치할 수 있습니다. 대상 컴퓨터에 대 한 관리자 권한이 있는 네트워크 계정을 사용 해야 합니다. 콘솔을 사용 하 여 응용 프로그램 가상화 시스템 플랫폼을 구성 하 고 관리할 수 있습니다.

이 절차를 완료 하려면 먼저이 컴퓨터나 다른 컴퓨터에 Application Virtualization Management 웹 서비스를 설치 해야 합니다. 관리 웹 서비스를 사용 하 여 데이터 저장소와 도메인 컨트롤러에 액세스할 수 있습니다. 웹 서비스를 설치 하는 방법에 대 한 자세한 내용은 [관리 웹 서비스를 설치 하는 방법을](how-to-install-the-management-web-service.md)참조 하세요.

**관리 콘솔을 설치 하려면**

1.  대상 컴퓨터에 이전 버전의 관리 콘솔이 설치 되어 있지 않은지 확인 합니다.

2.  네트워크에서 응용 프로그램 가상화 시스템 설정 프로그램의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 **Setup.exe**를 두 번 클릭 합니다.

3.  **시작 페이지**에서 **다음**을 클릭 합니다.

4.  사용권 **계약** 페이지에서 사용권 계약에 동의 하는 경우 **동의 함을**선택 하 고 **다음**을 클릭 합니다.

5.  **등록 정보** 페이지에서 **사용자 이름** 및 **조직** 정보를 지정 하 고 **다음**을 클릭 합니다.

6.  **설치 유형** 페이지에서 **사용자 지정** 을 클릭 하 고 **다음**을 클릭 합니다.

7.  **사용자 지정 설정** 페이지에서 **관리 콘솔**을 제외한 모든 Application Virtualization 시스템 구성 요소를 선택 취소 하 고 **다음**을 클릭 합니다.

    **참고**  컴퓨터에 이미 설치 된 구성 요소를 사용자 지정 설정 화면에서 선택 취소 하 여 자동으로 제거 됩니다.

     

8.  프로그램을 **수정할 준비가 되었습니다** 화면에서 **설치**를 클릭 합니다.

    **참고**  첫 번째 구성 요소를 설치 하는 경우 **프로그램을 설치할 준비가** 되었습니다 페이지가 표시 됩니다. 설치를 시작 하려면 **설치**를 클릭 합니다.

     

9.  **설치 마법사 완료** 화면에서 **마침을**클릭 합니다. 확인 **을 클릭 하 여 컴퓨터** 를 다시 시작 하 고 설치를 완료 합니다.

10. Windows 제어판에서 **관리 도구** 를 두 번 클릭 한 다음 **응용 프로그램 가상화 관리 콘솔** 을 클릭 하 여 관리 콘솔을 표시 합니다.

11. **연결** 아이콘을 클릭 하거나 **응용 프로그램 가상화 시스템** 컨테이너를 마우스 오른쪽 단추로 클릭 한 다음 **application virtualization System에 연결**을 클릭 합니다.

12. **Application Virtualization System에 연결** 화면에서 관리 웹 서비스 컴퓨터의 호스트 이름 및 포트를 입력 하 고, 필요한 경우 보안 정보 및 로그인 자격 증명을 변경한 다음 **확인**을 클릭 합니다.

13. 관리 웹 서비스 컴퓨터에 연결한 후 **콘솔** 메뉴에서 **파일** 을 클릭 한 다음 **끝내기**를 클릭 합니다. **예** 를 클릭 하 여 콘솔 설정을 저장 합니다.

## 관련 항목


[서버 및 시스템 구성 요소 설치 방법](how-to-install-the-servers-and-system-components.md)

 

 





