---
title: MED-V 작업 영역 패키지 관리자를 사용하여 URL 리디렉션을 관리하는 방법
description: MED-V 작업 영역 패키지 관리자를 사용하여 URL 리디렉션을 관리하는 방법
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824818"
---
# MED-V 작업 영역 패키지 관리자를 사용하여 URL 리디렉션을 관리하는 방법


MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역의 URL 리디렉션을 관리할 수 있습니다.

**MED-V 작업 영역에서 웹 주소 리디렉션을 관리 하려면**

1.  **Med-v 작업 영역 포장기**를 열려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 작업 영역 포장기**를 클릭 합니다.

2.  **Med-v 작업 영역 포장기** 기본 패널에서 **웹 리디렉션 관리**를 클릭 합니다.

3.  **웹 리디렉션 관리** 창에서 med-v 작업 영역의 Internet Explorer로 리디렉션되는 url 목록을 입력 하거나, 붙여 넣거나, 가져올 수 있습니다.

    **참고**  
    MED-V의 URL 리디렉션은 HTTP 및 HTTPS 프로토콜만 지원 합니다. MED-V는 FTP 또는 다른 프로토콜에 대 한 지원을 제공 하지 않습니다.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. **다른 이름으로 저장 ...** 을 클릭 합니다. 지정한 폴더에 업데이트 된 URL 리디렉션 파일을 저장 합니다. MED-V는 업데이트 된 URL 리디렉션 정보를 포함 하는 레지스트리 파일을 만듭니다. 그룹 정책을 사용 하 여 업데이트 된 레지스트리 키를 배포 합니다. 그룹 정책을 사용 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V는 또한 지정 된 폴더에 업데이트 된 MED-V 작업 영역 패키지를 다시 만드는 데 사용할 수 있는 Windows PowerShell 스크립트를 만듭니다.

## 관련 항목


[배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[MED-V URL 리디렉션 관리](manage-med-v-url-redirection.md)









