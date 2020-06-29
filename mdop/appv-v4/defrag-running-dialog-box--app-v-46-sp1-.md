---
title: Defrag 실행 대화 상자(App-V 4.6 SP1)
description: Defrag 실행 대화 상자(App-V 4.6 SP1)
author: dansimp
ms.assetid: 0ceb0897-377e-4754-a7ab-3bc2b5af1452
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ca56723dedb46ba87890ae62d476ca365b201c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821728"
---
# <span data-ttu-id="9d380-103">Defrag 실행 대화 상자(App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9d380-103">Defrag Running Dialog Box (App-V 4.6 SP1)</span></span>


<span data-ttu-id="9d380-104">디스크 조각 모음 서비스가 실행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-104">The Disk Defragmenter service is running.</span></span> <span data-ttu-id="9d380-105">디스크 조각 모음 서비스는 시스템 리소스를 사용 하 여 성능이 저하 되거나 가상 응용 프로그램 패키지를 만드는 데 걸리는 시간을 늘릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-105">The Disk Defragmenter service uses system resources and can cause degradation in performance or increase the time it takes to create virtual application package.</span></span>

<span data-ttu-id="9d380-106">시퀀싱 하는 동안 디스크 조각 모음 서비스가 실행 되지 않도록 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-106">Use the following procedure to stop the Disk Defragmenter service from running during sequencing.</span></span>

1.  <span data-ttu-id="9d380-107">App-v Sequencer를 실행 하는 컴퓨터에서 **시작**을 클릭 하 고 **컴퓨터**를 마우스 오른쪽 단추로 클릭 한 다음 **관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-107">On the computer running the App-V Sequencer, click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="9d380-108">**컴퓨터 관리** 콘솔에서 **서비스 및 응용 프로그램**을 두 번 클릭 한 다음 **서비스** 를 두 번 클릭 하 여 **서비스**를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-108">In the **Computer Management** console, double-click **Services and Applications**, and then double-click **Services** to expand **Services**,.</span></span>

3.  <span data-ttu-id="9d380-109">목록에서 해당 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-109">Locate it in the list.</span></span> <span data-ttu-id="9d380-110">**디스크 조각 모음**을 마우스 오른쪽 단추로 클릭 하 고 **기타 작업**을 클릭 한 다음 디스크 조각 **모음 중지를 클릭 하** 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d380-110">Right-click **Disk Defragmenter**, click **More Actions**, click **Stop** to stop Disk Defragmenter, and then click **OK**.</span></span>

## <span data-ttu-id="9d380-111">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9d380-111">Related topics</span></span>


[<span data-ttu-id="9d380-112">대화 상자(App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9d380-112">Dialog Boxes (AppV 4.6 SP1)</span></span>](dialog-boxes--appv-46-sp1-.md)

 

 





