---
title: 배포 문제 해결
description: 배포 문제 해결
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822898"
---
# 배포 문제 해결


이 항목에서는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에서 배포 문제를 해결 하는 데 도움이 되는 정보를 제공 합니다.

## MED-V 배포의 문제 해결


MED-V를 배포 하는 경우 다음 문제가 발생할 수 있습니다. 이 솔루션은이 문제를 해결 하는 데 도움이 됩니다.

**현재 사용자 에게만 MED-V를 설치 하는 경우 문제가 발생 합니다.** MED-V는 MED-V 작업 영역 포장기, MED-V 호스트 에이전트, 모든 사용자에 대 한 MED-V 작업 영역의 설치만 지원 합니다. 현재 사용자 용으로 설치 하면 구성 요소 설치와 MED-V 작업 영역의 설정에 오류가 발생 합니다.

**해결 방법**

MED-V 구성 요소를 설치할 때 **ALLUSERS = ""** 옵션을 사용 하지 마세요.

**MED-V는 가상화 스택의 독점적 사용이 필요 합니다.** 컴퓨터에서 한 번에 하나의 가상화 스택을 실행할 수 있습니다. Windows 가상 PC는 가상 스택을 사용 해야 하며 MED-V는 Windows 가상 PC에 종속 됩니다. 따라서 가상 스택을 사용 하는 다른 응용 프로그램을 실행 중인 경우 med-v를 배포 하거나 사용 하려고 하면 MED-V가 실행 되거나 성공적으로 설치 될 수 없습니다.

**해결 방법**

MED-V를 설치 또는 실행 하기 전에 가상화 스택을 사용 하는 실행 중인 응용 프로그램을 닫습니다.

**바로 가기는 제거 후에도 유지 됩니다.** 기본적으로 MED-V를 제거 하면 최종 사용자의 **시작** 메뉴에 있는 바로 가기가 제거 됩니다. 그러나 로밍 프로필을 실행 하는 최종 사용자와 같은 특정 상황에서는 MED-V 게시 된 응용 프로그램의 바로 가기가 최종 사용자의 **시작** 메뉴에 남아 있습니다.

**해결 방법**

**시작** 메뉴에서 나머지 바로 가기를 수동으로 삭제 하려면 바로 가기를 마우스 오른쪽 단추로 클릭 한 다음 **제거**를 클릭 합니다.

**MED-V 작업 영역에서 로그온 메시지 그룹 정책 설정을 사용 하지 않도록 설정 합니다.** MED-V 작업 영역에서 Windows XP 로그온 메시지를 사용할 수 있는 경우에는 최종 사용자가 MED-V 가상 응용 프로그램을 열려고 할 때마다 로그온 해야 합니다. 이렇게 하면 사용자 환경이 떨어집니다.

**해결 방법**

MED-V 가상 머신에서 다음 그룹 정책 설정을 사용 하지 않도록 설정 합니다.

**대화형 로그온: 로그온을 시도하는 사용자에 대한 메시지 텍스트**

**대화형 로그온: 로그온을 시도하는 사용자에 대한 메시지 제목**

## 관련 항목


[작업 문제 해결](operations-troubleshooting-medv2.md)

 

 





