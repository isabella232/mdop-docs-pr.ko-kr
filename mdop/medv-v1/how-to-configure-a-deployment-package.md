---
title: 배포 패키지를 구성하는 방법
description: 배포 패키지를 구성하는 방법
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825948"
---
# 배포 패키지를 구성하는 방법


패키징 마법사는 로컬 컴퓨터에 폴더를 만들고 필요한 모든 설치 파일을 단일 폴더로 전송 하 여 패키지를 만드는 과정을 안내 합니다. 그런 다음 폴더의 콘텐츠를 배포를 위해 여러 이동식 미디어 드라이브로 이동할 수 있습니다.

**참고**  
단일 패키지는 x86 및 x64 시스템 모두에 대 한 설치 파일을 포함할 수 없습니다.



## 배포 패키지를 만드는 방법


**배포 패키지를 만들려면**

1. 하나 이상의 로컬 압축 이미지를 만들었는지 **이미지** 모듈에서 확인 합니다.

2. **도구** 메뉴에서 **패키징 마법사**를 선택 합니다.

3. **패키징 마법사** 시작 페이지에서 **다음**을 클릭 합니다.

4. **작업 영역 이미지** 페이지에서 패키지에 이미지 **포함 확인란을** 선택 합니다.

   **이미지** 필드를 사용할 수 있습니다.

   **참고**  
   MED-V 패키지에는 이미지가 필요 하지 않습니다. 이미지 없이 패키지를 만들 수 있습니다. 이러한 경우 이미지를 서버에 업로드 하 여 나중에 네트워크를 통해 클라이언트에 다운로드 하거나 이미지 프리 스테이지 폴더로 푸시할 수 있습니다.



5. **이미지** 목록을 클릭 하 여 사용 가능한 모든 이미지를 표시 합니다. 패키지에 복사할 이미지를 선택 합니다. **새로 고침** 을 클릭 하 여 사용 가능한 이미지 목록을 새로 고칩니다.

6. **다음**을 클릭합니다.

7. **Med-v 설치 설정** 페이지에서 다음 중 하나를 수행 하 여 med-v 설치 파일을 선택 합니다.

   -   **Med-v 설치 파일** 필드에 설치 파일이 있는 디렉터리의 전체 경로를 입력 합니다.

   -   설치 파일이 있는 디렉터리를 찾아보려면 **...** 을 클릭 합니다.

   **참고**  
   이 필드는 필수 이며, 마법사가 올바른 파일 이름 없이 계속 진행 되지 않습니다.



8. **서버 주소** 필드에 서버 이름 또는 IP 주소를 입력 합니다.

9. **서버 포트** 필드에 서버 포트를 입력 합니다.

10. 서버에 연결 하기 위해 https 연결이 필요한 경우 **https를 사용 하 여 서버에 액세스** 확인란을 선택 합니다.

11. 다음 중 하나를 수행합니다.

    -   **기본 설치 설정을**클릭 하 고 **다음** 을 클릭 하 여 계속 진행 하 고 기본 설정을 유지 합니다.

    -   **사용자 지정 설치 설정을**클릭 하 고 **다음** 을 클릭 하 여 설치 설정을 사용자 지정 합니다.

        1.  **Med-v 설치 사용자 지정 설정** 페이지의 **설치 폴더** 필드에 med-v 파일이 설치 될 호스트 컴퓨터의 폴더 경로를 입력 합니다.

            **참고**  
            상수 대신 경로에 변수를 사용 하는 것이 좋으며,이는 컴퓨터 마다 다를 수 있습니다.

            예를 들어 *c:\\MED-V*대신 *%ProgramFiles%\\MED-V* 를 사용 합니다.



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. **추가 설치** 페이지에서 **가상화 소프트웨어 설치 포함** 확인란을 선택 하 여 패키지에 가상 PC 설치를 포함 합니다.

    **설치 파일** 필드를 사용할 수 있습니다. 가상화 소프트웨어 설치 파일의 전체 경로를 입력 하거나 **...** 를 클릭 하 여 디렉터리를 찾습니다.

13. 가상 PC 업데이트 설치를 패키지에 포함 하려면 **가상 PC QFE 설치 포함** 확인란을 선택 합니다.

    **설치 파일** 필드를 사용할 수 있습니다. 가상 PC 업데이트 설치 파일의 전체 경로를 입력 하거나 **...** 를 클릭 하 여 디렉터리를 찾습니다.

14. Microsoft .net framework 2.0 설치를 패키지에 포함 하려면 **microsoft .Net framework 설치 포함 2.0** 확인란을 선택 합니다.

    **설치 파일** 필드를 사용할 수 있습니다. Microsoft .NET Framework 2.0 설치 파일의 전체 경로를 입력 하거나 **...** 를 클릭 하 여 디렉터리를 찾습니다.

15. **다음**을 클릭합니다.

16. **마무리** 페이지에서 다음 중 하나를 실행 하 여 패키지를 저장할 위치를 선택 합니다.

    -   **패키지 대상** 필드에 패키지를 저장할 디렉터리의 전체 경로를 입력 합니다.

    -   설치 파일을 저장 해야 하는 디렉터리를 찾아보려면 **...** 을 클릭 합니다.

    **참고**  
    패키지를 빌드하면 실제 패키지 크기 보다 많은 공간이 소모 될 것입니다. 따라서 하드 드라이브에 패키지를 작성 하는 것이 좋습니다. 패키지를 만든 후에는 USB에 복사할 수 있습니다.



17. **패키지 이름** 필드에 패키지의 이름을 입력 합니다.

18. **마침을** 클릭 하 여 패키지를 만듭니다.

    패키지가 생성 됩니다. 이 작업은 몇 분 정도 걸릴 수 있습니다.

    패키지를 만든 후에는 성공적으로 완료 되었음을 알리는 메시지가 표시 됩니다.

**참고**  
이동식 미디어에 직접 모든 파일을 저장 한 경우 폴더 자체를 제외 하 고 폴더의 내용만 복사 하 여 이동식 미디어에 복사할 수 있도록 해야 합니다.



**참고**  
이동식 미디어는 패키지 내용이 이동식 미디어의 메모리 중 최대 3/4을 소모 하도록 충분히 커야 합니다.



**참고**  
패키지를 만들 때 빌드가 완료 되 면 실제 패키지 크기의 크기를 두 배로 설정 해야 할 수 있습니다.



## 관련 항목


[MED-V 이미지 만들기](creating-a-med-v-image.md)









