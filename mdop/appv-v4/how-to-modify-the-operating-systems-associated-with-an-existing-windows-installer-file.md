---
title: 기존 Windows Installer 파일로 연결된 운영 체제를 수정하는 방법
description: 기존 Windows Installer 파일로 연결된 운영 체제를 수정하는 방법
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816953"
---
# 기존 Windows Installer 파일로 연결된 운영 체제를 수정하는 방법


다음 절차를 사용 하 여 App-v Sequencer를 사용 하 여 만든 기존 Windows Installer (**MSI**) 파일과 연결 된 운영 체제 버전을 수정 합니다.

**기존 Windows Installer 파일의 운영 체제를 수정 하려면**

1.  운영 체제만 설치 되어 있는 환경의 컴퓨터에 App-v 시퀀서를 설치 합니다. 또는 가상 환경을 실행 하는 컴퓨터 (예: Microsoft 가상 PC)에 시퀀서를 설치할 수 있습니다. 이 방법은 최소한의 추가 구성으로 다시 사용할 수 있는 깨끗 한 시퀀싱 환경을 유지 관리 하는 것이 더 쉽기 때문에 유용 합니다. App-v 시퀀서를 설치 하는 방법에 대 한 자세한 내용은 [Sequencer를 설치 하는 방법을](how-to-install-the-sequencer.md)참조 하세요.

2.  수정 하려는 Windows Installer 파일이 포함 된 전체 가상 응용 프로그램 패키지를 Sequencer를 실행 하는 컴퓨터에 복사 합니다.

3.  Windows installer 파일을 수정 하려면 Sequencer 콘솔을 열고 **패키지**  /  **열기**를 선택한 다음 Windows Installer 파일과 연결 된 가상 응용 프로그램 패키지가 저장 된 위치를 찾습니다.

4.  운영 체제를 추가 하거나 제거 하려면 Sequencer 콘솔에서 **배포** 탭을 선택 합니다. Windows Installer 파일과 연결 될 추가 운영 체제를 지정 하려면 원하는 운영 체제를 선택한 다음 **선택한** 운영 체제 목록 컨트롤을 가리키는 화살표를 클릭 합니다.

    운영 체제 연결을 제거 하려면 제거 하려는 운영 체제를 선택 하 고 **사용 가능한** 운영 체제 목록 컨트롤을 가리키는 화살표를 클릭 합니다.

5.  가상 응용 프로그램 패키지와 연결 되는 새 Windows Installer를 만들려면 **Microsoft Windows installer (MSI) 패키지 생성**을 선택 합니다. 또는 **도구**  /  **MSI 만들기**를 선택할 수 있습니다.

    **참고**  **Tools** / **MSI를 만들어** 새 Windows Installer 파일을 만드는 도구를 선택 하는 경우이 절차의 **6 단계** 를 건너뛸 수 있습니다.

     

6.  가상 응용 프로그램 패키지를 저장 하려면 **패키지**  /  **저장**을 선택 합니다.

## 관련 항목


[Application Virtualization Sequencer에 대한 작업](tasks-for-the-application-virtualization-sequencer.md)

 

 





