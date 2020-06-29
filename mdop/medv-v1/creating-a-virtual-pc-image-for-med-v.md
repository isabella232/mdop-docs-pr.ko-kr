---
title: MED-V에 대한 가상 PC 이미지 만들기
description: MED-V에 대한 가상 PC 이미지 만들기
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823663"
---
# MED-V에 대한 가상 PC 이미지 만들기


MED-V에 대 한 VPC (가상 PC) 이미지를 만들려면 다음을 수행 해야 합니다.

1.  [VPC 이미지를 만듭니다](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).

2.  [Med-v 작업 영역 .msi 패키지를 VPC 이미지에 설치](#bkmk-howtoinstallthemedvworkspacemsipackage)합니다.

3.  [VPC 이미지에서 med-v 가상 컴퓨터 필수 구성 요소 도구를 실행](#bkmk-howtorunthevirtualmachineprerequisitestool)합니다.

4.  [VPC 이미지에서 가상 컴퓨터 필수 구성 요소를 수동으로 구성](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites)합니다.

5.  [Med-v 이미지에 대 한 Sysprep을 구성](#bkmk-howtoconfiguresysprepformedvimages) 합니다 (선택 사항).

6.  [Microsoft 가상 PC를 끄십시오](#bkmk-turningoffmicrosoftvirtualpc).

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Microsoft Virtual PC를 사용 하 여 가상 PC 이미지 만들기


Microsoft Virtual PC를 사용 하 여 가상 PC 이미지를 만들려면 가상 PC 설명서를 참조 하세요.

자세한 내용은 다음을 참조하십시오.

-   [Windows 가상 PC 도움말](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [가상 컴퓨터 만들기 및 게스트 운영 체제 설치](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a>MED-V 작업 영역의 msi 패키지를 설치 하는 방법


가상 PC 이미지를 만든 후에 MED-V 작업 영역 .msi 패키지를 이미지에 설치 합니다.

**MED-V 작업 영역 이미지를 설치 하려면**

1.  가상 컴퓨터를 시작 하 고, 내부에서 MED-V 작업 영역의 msi 패키지를 복사 합니다.

    MED-V 작업 영역의 .msi 패키지는 *MED-V\_workspace\_x.msi*호출 되며 여기서 *x* 는 버전 번호입니다.

    예를 들어 *MED-V\_workspace\_1.0.65.msi*.

2.  MED-V 작업 영역 .msi 패키지를 두 번 클릭 하 고 설치 마법사 지침을 따릅니다.

    **참고**  
    새 MED-V 버전이 출시 되 고 기존 가상 PC 이미지가 업데이트 되 면 기존 MED-V 작업 영역 .msi 패키지를 제거 하 고 컴퓨터를 다시 부팅 한 다음 새 MED-V 작업 영역 .msi 패키지를 설치 합니다.



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a>가상 컴퓨터 필수 구성 요소 도구를 실행 하는 방법


VM (가상 컴퓨터) 필수 구성 요소 도구는 몇 가지 필수 구성 요소를 자동화 하는 마법사입니다.

**참고**  
마법사에서 많은 매개 변수를 구성할 수 있지만, MED-V의 적절 한 작동에 필요한 속성은 구성할 수 없습니다.



**가상 컴퓨터 필수 구성 요소 도구를 실행 하려면**

1.  MED-V 작업 영역 .msi 패키지가 설치 된 후 Windows **시작** 메뉴에서 **모든 프로그램의 &gt; Med-v &gt; VM 필수 구성 요소 도구**를 선택 합니다.

    **참고**  
    가상 컴퓨터 필수 구성 요소 도구를 실행 하는 사용자는 로컬 관리자 권한이 있어야 하며 사용자만 로그인 해야 합니다.



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. **다음**을 클릭합니다.

3. **Windows 설정** 페이지의 다음과 같은 구성 가능한 속성에서 구성할 구성을 선택 합니다.

   -   **사용자의 개인 기록 정보 지우기**

   -   **로컬 프로필 임시 디렉터리 지우기**

   -   **다음 Windows 이벤트에서 소리 사용 안 함: 시작, 로그온, 로그 오프**

   **참고**  
   그룹 정책에서 Windows 페이지 보호기를 사용 하도록 설정 하지 마세요.



4. **다음**을 클릭합니다.

5. **Internet Explorer 설정** 페이지의 구성 가능한 다음 속성에서 구성할 구성을 선택 합니다.

   -   **자동 완성 기능을 사용 하지 않음**

   -   **바로 가기를 실행 하는 데 창을 다시 사용할 수 없도록 설정**

   -   **검색 기록 지우기**

   -   **Internet Explorer 7에서 탭 브라우저 사용**

6. **다음**을 클릭합니다.

7. **Windows 서비스** 페이지의 다음과 같은 구성 가능한 속성에서 구성할 구성을 선택 합니다.

   -   **보안 센터 서비스**

   -   **작업 스케줄러 서비스**

   -   **자동 업데이트 서비스**

   -   **시스템 복원 서비스**

   -   **인덱싱 서비스**

   -   **무선 제로 구성**

   -   **빠른 사용자 전환 호환성**

8. **다음**을 클릭합니다.

9. **Windows 자동 로그온** 페이지에서 다음을 수행 합니다.

   1.  **Windows 자동 로그온 사용** 확인란을 선택 합니다.

   2.  **사용자 이름** 및 **암호**를 할당 합니다.

10. **적용**을 클릭 하 고 표시 되는 확인 상자에서 **예**를 클릭 합니다.

11. **요약** 페이지에서 **마침을** 클릭 하 여 마법사를 종료 합니다.

**참고**  
그룹 정책이 필수 구성 요소 도구에 설정 된 필수 설정을 덮어쓰지 않는지 확인 합니다.



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a>MED-V 가상 컴퓨터 수동 설치 선행 조건을 구성 하는 방법


가상 컴퓨터 필수 구성 요소 도구를 통해 몇 가지 구성을 구성할 수 없으며 수동으로 수행 해야 합니다.

-   가상 컴퓨터 설정

    Microsoft Virtual PC 콘솔에서 다음 가상 컴퓨터 설정을 구성 하는 것이 좋습니다.

    -   플로피 디스크 드라이브를 비활성화 합니다.

    -   실행 취소-디스크 (**설정 &gt; 실행 취소-디스크**)를 비활성화 합니다.

    -   이미지에 가상 CPU가 하나만 있는지 확인 합니다.

    -   가상 컴퓨터와 사용자가 게시 된 응용 프로그램 (예: 사용자 입력이 필요한 메시지)과 관련이 없는 경우 상호 작용을 제거 합니다.

-   이미지 설정

    이미지 내에서 다음의 수동 설정을 구성 합니다.

    1.  **전원 옵션 속성** 창에서 최대 절전 모드 및 절전 모드를 사용 하지 않도록 설정 합니다.

    2.  최신 Windows 업데이트를 적용 합니다.

    3.  **Windows 시작 및 복구** 대화 상자의 **시스템 오류** 섹션에서 **자동으로 다시 시작** 확인란의 선택을 취소 합니다.

    4.  이미지가 VLK 라이선스 키를 사용 하는지 확인 합니다.

-   VPC 추가 설치

    **작업** 메뉴에서 **가상 컴퓨터 추가 설치 또는 업데이트**를 선택 합니다.

-   인쇄 구성

    다음 방법 중 하나를 통해 MED-V 작업 영역에서 인쇄를 구성할 수 있습니다.

    -   가상 컴퓨터에 프린터를 추가 합니다.

    -   호스트 컴퓨터에 구성 된 프린터를 사용 하 여 인쇄를 허용 합니다.

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a>MED-V 이미지에 대해 Sysprep를 구성 하는 방법


MED-V 작업 영역에서 여러 개의 MED-V 작업 영역이 단일 컴퓨터에서 실행 되는 경우에는 Sysprep를 구성 하 여 고유한 SID (보안 식별자)를 할당할 수 있습니다. Sysprep를 사용 하 여 도메인에 가입 하지 않는 것이 좋습니다. 대신, [스크립트 동작을 설정 하는 방법](how-to-set-up-script-actions.md)에 설명 된 대로 med-v 조인 도메인 스크립트 작업을 사용 합니다.

**참고**  
Sysprep는 Windows 운영 체제에 대 한 Microsoft 시스템 준비 유틸리티입니다.



**MED-V 작업 영역에서 Sysprep를 구성 하려면**

1.  *Sysprep*이라는 시스템 드라이브의 루트에 디렉터리를 만듭니다.

2.  Windows 설치 CD에서 시스템 드라이브의 루트로 *deploy.cab* 를 추출 하거나 Microsoft 웹 사이트에서 최신 배포 도구 업데이트를 다운로드 합니다.

    -   Windows 2000의 경우 [windows 2000 용 배포 도구 업데이트](https://go.microsoft.com/fwlink/?LinkId=143001)를 참조 하세요.

    -   Windows XP의 경우 [WINDOWS xp 용 배포 도구 업데이트](https://go.microsoft.com/fwlink/?LinkId=143000)를 참조 하세요.

3.  **설치 관리자** (setupmgr.exe)를 실행 합니다.

4.  설치 관리자 마법사를 따릅니다.

Sysprep을 구성 하 고 MED-V 작업 영역을 만든 후에는 Sysprep을 실행 해야 합니다.

**Sysprep를 실행 하려면**

1.  시스템 드라이브의 루트에 있는 Sysprep 폴더에서 시스템 준비 도구 (Sysprep.exe)를 실행 합니다.

2.  경고 메시지 상자가 나타나면 **확인**을 클릭 합니다.

3.  **Sysprep 속성** 대화 상자에서 활성화 및 **최소 설정 사용** **에 대 한 유예 기간 다시 설정** 확인란을 선택 합니다.

4.  다시 **봉인**을 클릭 합니다.

5.  표시 되는 확인 메시지 상자에 나열 된 정보가 마음에 들지 않으면 **취소** 를 클릭 하 고 선택 항목을 변경 합니다.

6.  **확인** 을 클릭 하 여 시스템 준비 프로세스를 완료 합니다.

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a>Microsoft Virtual PC를 끄는 중


모든 구성 요소를 설치 하 고 구성한 후에는 Microsoft 가상 PC를 닫고 **끄기를**선택 합니다.

## 관련 항목


MED-V 이미지 만들기 [스크립트 작업을 설정 하는 방법](how-to-set-up-script-actions.md)









