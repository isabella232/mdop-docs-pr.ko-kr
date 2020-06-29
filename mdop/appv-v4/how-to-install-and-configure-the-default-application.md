---
title: 기본 응용 프로그램을 설치 및 구성하는 방법
description: 기본 응용 프로그램을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817368"
---
# 기본 응용 프로그램을 설치 및 구성하는 방법


기본 응용 프로그램은 설치의 일부로 제공 되며 설치 하는 동안 Microsoft Application Virtualization (App-v) 관리 서버에 자동으로 복사 됩니다. 관리 서버가 올바르게 설치 및 구성 되었는지 확인 하는 데 사용 되지만 사용자가 액세스할 수 있도록 Microsoft Application Virtualization (App-v) 클라이언트에 게시 해야 합니다.

다음 절차를 사용 하 여 기본 응용 프로그램을 게시 하 고 스트리밍합니다.

**기본 응용 프로그램을 게시 하려면**

1.  설치 중에 지정 된 App-v 관리자 그룹의 구성원 인 계정을 사용 하 여 App-v 관리 서버에 로그온 합니다.

2.  App-v 관리 서버에서 **시작**, **관리 도구**, **응용 프로그램 가상화 관리 콘솔**을 차례로 클릭 합니다.

3.  App-v 관리 콘솔에서 **작업**을 클릭 한 다음 **Application Virtualization System에 연결**을 클릭 합니다.

4.  **연결 구성** 페이지에서 **보안 연결 사용** 확인란의 선택을 취소 합니다.

5.  **웹 서비스 호스트 이름** 상자에 App-v 관리 서버의 FQDN (정규화 된 도메인 이름)을 입력 한 다음 **확인**을 클릭 합니다.

    **참고**  관리 서버에 설치 되어 있는 경우 웹 서비스 호스트 이름에 **localhost** 를 사용할 수도 있습니다.

     

6.  App-v 관리 콘솔에서 **서버** 노드를 마우스 오른쪽 단추로 클릭 하 고 **시스템 옵션**을 클릭 합니다.

7.  **일반** 탭의 **기본 콘텐츠 경로** 상자에 설치 하는 동안 서버에서 만든 콘텐츠 폴더의 UNC (범용 명명 규칙) 경로를 입력 합니다. 예를 들어 \\ Content (\ \ \ &lt; Server Name)를 &gt; 선택한 다음 **확인**을 클릭 합니다.

    **중요**  클라이언트가 이름을 올바르게 확인할 수 있도록 서버 이름에 대 한 FQDN을 사용 합니다.

     

8.  앱-V 관리 콘솔의 탐색 창에서 **서버** 노드를 확장 한 다음 **응용 프로그램**을 클릭 합니다.

9.  항목 창에서 **기본 응용 프로그램**을 클릭 한 다음 **작업** 창에서 **속성**을 클릭 합니다.

10. **속성** 대화 상자에서 **OSD 경로** 상자 옆에 있는 **찾아보기를**클릭 합니다.

11. **열기** 대화 상자에서 설치 하는 동안 서버에서 만든 콘텐츠 폴더의 UNC 경로를 입력 합니다. 예를 들어 \\/\ \ &lt; 서버 이름 \ \의 &gt; 콘텐츠를 입력 하 고 enter 키를 누릅니다. 실제 서버 이름을 사용 해야 하며이 위치에서 **localhost** 를 사용할 수 없습니다.

    **중요**  **OSD 경로** 상자와 **아이콘 경로** 상자의 값이 모두 UNC 형식 (예: \\ \ \ &lt; Server Name &gt; \\Content\\defaultapp.ico) 인지 확인 하 고 서버를 설치할 때 만든 콘텐츠 폴더를 가리킵니다. **Localhost** 또는 c:\\program files Files\\..와 같은 드라이브 문자를 포함 하는 파일 경로를 사용 하지 마세요. \\.. 콘텐트가.

     

12. DefaultApp .osd 파일을 선택 하 고 **열기**를 클릭 합니다.

13. 앞의 단계를 반복 하 여 아이콘 경로를 구성 합니다.

14. **액세스 권한** 탭을 클릭 하 고 앱-V 사용자 그룹에 게 응용 프로그램에 대 한 액세스 권한이 있는지 확인 합니다.

15. **바로 가기** 탭을 클릭 한 다음 **사용자의 바탕 화면에 게시를**클릭 합니다. **확인**을 클릭합니다.

16. Windows 탐색기를 열고 콘텐츠 디렉터리를 찾습니다.

17. DefaultApp 파일을 두 번 클릭 하 고 메모장에서 엽니다.

18. **HREF** 태그가 포함 된 줄을 찾아 다음 코드로 변경 합니다.

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    또는 RTSPS를 사용 하는 경우:

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. DefaultApp .osd 파일을 닫고 변경 내용을 저장 합니다.

**기본 응용 프로그램을 스트리밍하려면**

1.  App-v 클라이언트가 설치 된 컴퓨터에서 서버를 설치 하는 동안 지정 된 Application Virtualization Users 그룹의 구성원 인 사용자로 로그온 합니다.

2.  바탕 화면에 **기본 응용 프로그램 가상화 응용 프로그램** 바로 가기가 나타납니다. 바로 가기를 두 번 클릭 하 여 응용 프로그램을 시작 합니다.

3.  Windows 알림 영역 위에 표시 되는 상태 표시줄에는 응용 프로그램이 시작 됨을 보고 합니다. 응용 프로그램이 성공적으로 시작 되 면 기본 응용 프로그램의 제목 화면이 표시 됩니다. **확인** 을 클릭 하 여 대화 상자를 닫습니다. 이제 App-v 시스템이 올바르게 실행 되 고 있음을 확인 했습니다.

## 관련 항목


[서버 기반 배포용 서버를 구성하는 방법](how-to-configure-servers-for-server-based-deployment.md)

 

 





