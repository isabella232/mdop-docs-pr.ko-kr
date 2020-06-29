---
title: 시퀀싱 하는 응용 프로그램 유형을 확인 하는 방법 (App-v 4.6 SP1)
description: 시퀀싱 하는 응용 프로그램 유형을 확인 하는 방법 (App-v 4.6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817488"
---
# <span data-ttu-id="6e81f-103">시퀀싱 하는 응용 프로그램 유형을 확인 하는 방법 (App-v 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="6e81f-103">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>


<span data-ttu-id="6e81f-104">Microsoft Application Virtualization (App-v) Sequencer를 사용 하 여 세 가지 기본 유형의 응용 프로그램을 시퀀싱 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-104">You can sequence three basic types of applications by using Microsoft Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="6e81f-105">시퀀싱 하려는 응용 프로그램 유형을 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="6e81f-105">To determine which type of application to sequence</span></span>


<span data-ttu-id="6e81f-106">다음 표를 사용 하 여 시퀀싱 해야 하는 응용 프로그램 유형을 결정 하 고 응용 프로그램의 순서를 지정 하는 방법에 대 한 자세한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-106">Use the following table to determine which type of application you should sequence and to obtain more information about how to sequence the application.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e81f-107">응용 프로그램 종류</span><span class="sxs-lookup"><span data-stu-id="6e81f-107">Application Type</span></span></th>
<th align="left"><span data-ttu-id="6e81f-108">설명</span><span class="sxs-lookup"><span data-stu-id="6e81f-108">Description</span></span></th>
<th align="left"><span data-ttu-id="6e81f-109">추가 정보</span><span class="sxs-lookup"><span data-stu-id="6e81f-109">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e81f-110">Standard</span><span class="sxs-lookup"><span data-stu-id="6e81f-110">Standard</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e81f-111">이 옵션을 선택 하면 응용 프로그램 또는 응용 프로그램 집합을 포함 하는 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-111">Select this option to create a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="6e81f-112">순서를 계획 하는 대부분의 응용 프로그램에이 옵션을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-112">You should select this option for most applications that you plan to sequence.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)"><span data-ttu-id="6e81f-113">새 표준 응용 프로그램(App-V 4.6 SP1)을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e81f-113">How to Sequence a New Standard Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e81f-114">추가 기능 또는 플러그 인</span><span class="sxs-lookup"><span data-stu-id="6e81f-114">Add-on or Plug-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e81f-115">Microsoft Excel 용 플러그 인과 같은 표준 응용 프로그램의 기능을 확장 하는 패키지를 만들려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-115">Select this option to create a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="6e81f-116">또한 플러그 인을 기본적으로 설치 된 응용 프로그램 또는 동적 Suite 컴퍼지션을 사용 하 여 연결 되는 다른 패키지에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-116">Additionally, you can use plug-ins for natively installed applications, or another package that is linked by using Dynamic Suite Composition.</span></span> <span data-ttu-id="6e81f-117">동적 도구 모음 컴퍼지션에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> 동적 Suite 컴퍼지션 ()을 사용 하는 방법을 참조 하세요 </a> <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> .</span><span class="sxs-lookup"><span data-stu-id="6e81f-117">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)"><span data-ttu-id="6e81f-118">새 추가 기능 또는 플러그 인 응용 프로그램(App-V 4.6 SP1)을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e81f-118">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e81f-119">관점</span><span class="sxs-lookup"><span data-stu-id="6e81f-119">Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e81f-120">표준 응용 프로그램에 필요한 패키지를 만들려면이 옵션을 선택 합니다 (예: Microsoft .NET Framework).</span><span class="sxs-lookup"><span data-stu-id="6e81f-120">Select this option to create a package that is required by a standard application, for example, the Microsoft .NET Framework.</span></span> <span data-ttu-id="6e81f-121">미들웨어 패키지는 동적 도구 모음 컴퍼지션을 사용 하 여 다른 패키지에 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e81f-121">Middleware packages are used for linking to other packages by using Dynamic Suite Composition.</span></span> <span data-ttu-id="6e81f-122">동적 도구 모음 컴퍼지션에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> 동적 Suite 컴퍼지션 ()을 사용 하는 방법을 참조 하세요 </a> <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> .</span><span class="sxs-lookup"><span data-stu-id="6e81f-122">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)"><span data-ttu-id="6e81f-123">새 미들웨어 응용 프로그램(App-V 4.6 SP1)을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e81f-123">How to Sequence a New Middleware Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6e81f-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6e81f-124">Related topics</span></span>


[<span data-ttu-id="6e81f-125">Application Virtualization Sequencer(App-V 4.6 SP1)에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="6e81f-125">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





