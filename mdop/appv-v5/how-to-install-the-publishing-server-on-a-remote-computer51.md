---
title: 원격 컴퓨터에 게시 서버를 설치하는 방법
description: 원격 컴퓨터에 게시 서버를 설치하는 방법
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813980"
---
# 원격 컴퓨터에 게시 서버를 설치하는 방법


다음 절차를 사용 하 여 별도의 컴퓨터에 게시 서버를 설치 합니다. 다음 절차를 수행 하기 전에 데이터베이스 및 관리 서버를 사용할 수 있는지 확인 합니다.

**게시 서버를 별도의 컴퓨터에 설치 하려면**

1. 설치 하려는 컴퓨터에 App-v 5.1 서버 설치 파일을 복사 합니다. App-v 5.1 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다. **설치**를 클릭합니다.

2. **시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.

3. **Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다. Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다. **다음**을 클릭합니다.

4. **기능 선택** 페이지에서 **게시 서버** 확인란을 선택 하 고 **다음**을 클릭 합니다.

5. **설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.

6. **게시 서버 구성 구성** 페이지에서 다음 항목을 지정 합니다.

   -   게시 서버가 연결 하는 관리 서비스의 URL입니다. 예를 들어 **http://ManagementServerName:12345** .

   -   게시 서비스에 사용할 웹 사이트 이름을 지정 합니다. 사용자 지정 이름이 없는 경우 기본값을 그대로 사용 합니다.

   -   **포트 바인딩에**대해 app-v 5.1 (예: **54321**)에서 사용 되는 고유 포트 번호를 지정 합니다.

7. **설치 준비** 페이지에서 **설치**를 클릭 합니다.

8. 설치가 완료 되 면 게시 서버를 관리 서버에 등록 해야 합니다. App-v 5.1 관리 콘솔에서 다음 단계를 사용 하 여 서버를 등록 합니다.

   1.  App-v 5.1 관리 서버 콘솔을 엽니다.

   2.  왼쪽 창에서 **서버**를 선택한 다음 **새 서버 등록**을 선택 합니다.

   3.  이 서버의 이름과 설명 (필요한 경우)을 입력 하 고 **추가**를 클릭 합니다.

9. 게시 서버가 올바르게 실행 되 고 있는지 확인 하려면 패키지를 관리 서버로 가져오고 패키지를 광고 그룹으로 entitle 패키지를 게시 해야 합니다. 인터넷 브라우저를 사용 하 여 다음 URL을 엽니다 <strong> . http://publishingserver:pubport </strong> 서버가 올바르게 실행 되는 경우 다음과 유사한 정보가 표시 됩니다.

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 배포](deploying-app-v-51.md)

 

 





