---
title: MED-V 2.0 업데이트
description: MED-V 2.0 업데이트
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823733"
---
# <span data-ttu-id="09827-103">MED-V 2.0 업데이트</span><span class="sxs-lookup"><span data-stu-id="09827-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="09827-104">MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에 적절 한 보안 업데이트를 적용 하 여 시스템을 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09827-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="09827-105">업데이트 MED-V</span><span class="sxs-lookup"><span data-stu-id="09827-105">Updating MED-V</span></span>


<span data-ttu-id="09827-106">일반 사용자 또는 전자 소프트웨어 배포 시스템을 사용 하 여 자동으로 MED-V를 업데이트 하거나 대화형으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09827-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="09827-107">MED-V 호스트 에이전트의 설치는 MED-V 호스트 에이전트를 업그레이드 한 다음 필요한 경우 MED-V 작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="09827-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="09827-108">MED-V 호스트 에이전트와 게스트 에이전트는 동기화 상태를 유지 합니다. MED-V 호스트 에이전트를 업데이트 하는 동안 MED-V 작업 영역에서 응용 프로그램을 실행 하는 경우 업데이트를 완료 하려면 호스트 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09827-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="09827-109">실행 중인 응용 프로그램이 없는 경우 MED-V가 자동으로 다시 시작 되 고 호스트 컴퓨터를 다시 시작 하지 않고 업그레이드가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="09827-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="09827-110">전자 소프트웨어 배포 시스템을 사용 하 여 MED-V를 업데이트 하는 경우 다시 시작 동작을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09827-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="09827-111">이렇게 하려면 MED-V\_HostAgent\_Setup.exe를 설치할 때 명령 프롬프트에서 **REBOOT = "ReallySuppress"** 를 입력 하 여 다시 시작 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="09827-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="09827-112">그런 다음 전자 소프트웨어 배포 시스템을 구성 하 여 3010 반환 코드 (다시 시작 필요)를 캡처하여 설정 다시 시작 동작을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="09827-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="09827-113">관련 항목</span><span class="sxs-lookup"><span data-stu-id="09827-113">Related topics</span></span>


[<span data-ttu-id="09827-114">MED-V에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="09827-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





