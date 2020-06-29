---
title: 연결이 끊긴 작업 모드 설정을 사용 중지하거나 수정하는 방법
description: 연결이 끊긴 작업 모드 설정을 사용 중지하거나 수정하는 방법
author: dansimp
ms.assetid: 39f166d7-2d25-4899-8405-b45f051facb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 288c35c8d43352037c8514b4c060e847b456267c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817483"
---
# <span data-ttu-id="23082-103">연결이 끊긴 작업 모드 설정을 사용 중지하거나 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="23082-103">How to Disable or Modify Disconnected Operation Mode Settings</span></span>


<span data-ttu-id="23082-104">응용 프로그램 가상화 클라이언트에서 다음 절차를 사용 하 여 연결이 끊긴 작업 모드 설정을 사용 하지 않도록 설정 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-104">Use the following procedures in Application Virtualization Client to disable or modify disconnected operation mode settings.</span></span>

**<span data-ttu-id="23082-105">연결이 끊긴 작업을 비활성화 하려면</span><span class="sxs-lookup"><span data-stu-id="23082-105">To disable disconnected operation</span></span>**

1.  <span data-ttu-id="23082-106">콘솔에서 **Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-106">Right-click the **Application Virtualization** node in the console, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="23082-107">**연결** 탭을 클릭 한 다음 **연결이 끊긴 작업 허용** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-107">Click the **Connectivity** tab, and then clear **Allow disconnected operation** check box.</span></span>

3.  <span data-ttu-id="23082-108">**확인** 을 클릭 하 여 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-108">Click **OK** to accept the change.</span></span>

**<span data-ttu-id="23082-109">시간 초과를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="23082-109">To change the time-out</span></span>**

1.  <span data-ttu-id="23082-110">콘솔에서 **Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-110">Right-click the **Application Virtualization** node in the console, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="23082-111">**연결** 탭을 클릭 한 다음 **연결이 끊긴 작업을 다음으로 제한** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-111">Click the **Connectivity** tab, and then select the **Limit disconnected operation to** check box.</span></span>

3.  <span data-ttu-id="23082-112">필드에서 1 ~ 999999 (일을 나타냄) 사이의 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-112">In the field, enter a value from 1–999999 (representing days).</span></span> <span data-ttu-id="23082-113">기본값은 90 일입니다.</span><span class="sxs-lookup"><span data-stu-id="23082-113">The default value is 90 days.</span></span>

4.  <span data-ttu-id="23082-114">**확인** 을 클릭 하 여 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-114">Click **OK** to accept the change.</span></span>

**<span data-ttu-id="23082-115">오프 라인으로 작업 하려면</span><span class="sxs-lookup"><span data-stu-id="23082-115">To work offline</span></span>**

1.  <span data-ttu-id="23082-116">콘솔에서 **Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-116">Right-click the **Application Virtualization** node in the console, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="23082-117">**연결** 탭을 클릭 한 다음 **오프 라인으로 작업** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-117">Click the **Connectivity** tab, and then select the **Work offline** check box.</span></span>

3.  <span data-ttu-id="23082-118">**확인** 을 클릭 하 여 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23082-118">Click **OK** to accept the change.</span></span>

## <span data-ttu-id="23082-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="23082-119">Related topics</span></span>


[<span data-ttu-id="23082-120">연결이 끊긴 작업 모드</span><span class="sxs-lookup"><span data-stu-id="23082-120">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="23082-121">Application Virtualization를 사용하여 온라인 또는 오프라인으로 작업하는 방법</span><span class="sxs-lookup"><span data-stu-id="23082-121">How to Work Offline or Online with Application Virtualization</span></span>](how-to-work-offline-or-online-with-application-virtualization.md)

 

 





