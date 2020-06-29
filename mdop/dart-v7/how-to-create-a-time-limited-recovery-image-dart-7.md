---
title: 시간 제한 복구 이미지를 만드는 방법
description: 시간 제한 복구 이미지를 만드는 방법
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812633"
---
# <span data-ttu-id="42cc5-103">시간 제한 복구 이미지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="42cc5-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="42cc5-104">특정 일 수만 생성 된 후에만 사용할 수 있는 DaRT 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42cc5-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="42cc5-105">이렇게 하려면 명령 프롬프트에서 **DaRT 복구 이미지 마법사** 를 실행 하 고 일 수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42cc5-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="42cc5-106">시간 제한이 있는 복구 이미지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="42cc5-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="42cc5-107">관리자 자격 증명을 사용 하 여 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="42cc5-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="42cc5-108">디렉터리를 ERDC.exe 프로그램의 위치로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="42cc5-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="42cc5-109">다음 구문을 사용 하 여 **DaRT 복구 이미지 마법사**를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="42cc5-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="42cc5-110">*Numberofdays* 는 DaRT 복구 이미지를 사용할 수 있는 일 수를 나타내는 양의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="42cc5-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="42cc5-111">관련 항목</span><span class="sxs-lookup"><span data-stu-id="42cc5-111">Related topics</span></span>


[<span data-ttu-id="42cc5-112">DaRT 7.0 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="42cc5-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





