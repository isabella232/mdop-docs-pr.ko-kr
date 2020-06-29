---
title: 동시 라이선스 그룹을 설정하는 방법
description: 동시 라이선스 그룹을 설정하는 방법
author: dansimp
ms.assetid: 031abcf6-d8ed-49be-bddb-91b2c695d411
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e3035362cd645b6488b07408d6a9444f632fc88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816628"
---
# <span data-ttu-id="d00ae-103">동시 라이선스 그룹을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="d00ae-103">How to Set Up a Concurrent License Group</span></span>


<span data-ttu-id="d00ae-104">응용 프로그램 가상화 서버 관리 콘솔에서 다음 절차를 사용 하 여 동시 라이선스 그룹을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-104">You can use the following procedure in the Application Virtualization Server Management Console to set up a concurrent license group.</span></span> <span data-ttu-id="d00ae-105">동시 라이선스 그룹을 설정 하는 경우 특정 개수의 동시 사용자에 대 한 응용 프로그램 액세스를 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-105">When you set up a concurrent license group, you can limit access to applications to a specific number of concurrent users.</span></span>

**<span data-ttu-id="d00ae-106">동시 라이선스 그룹을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="d00ae-106">To set up a concurrent license group</span></span>**

1.  <span data-ttu-id="d00ae-107">Application Virtualization Server 관리 콘솔의 왼쪽 창에서 **응용 프로그램 라이선스** 노드를 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-107">In the left pane of the Application Virtualization Server Management Console, right-click the **Application Licenses** node.</span></span>

2.  <span data-ttu-id="d00ae-108">**새 동시 라이선스**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-108">Select **New Concurrent License**.</span></span>

3.  <span data-ttu-id="d00ae-109">**응용 프로그램 라이선스 그룹 이름** 필드에 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-109">Enter a name in the **Application License Group Name** field.</span></span>

4.  <span data-ttu-id="d00ae-110">**라이선스 만료 경고** 필드에 값 (분)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-110">Enter a value (in minutes) in the **License Expiration Warning** field.</span></span>

5.  <span data-ttu-id="d00ae-111">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-111">Click **Next**.</span></span>

6.  <span data-ttu-id="d00ae-112">**라이선스 설명** 필드에 설명 텍스트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-112">Enter descriptive text in the **License Description** field.</span></span>

7.  <span data-ttu-id="d00ae-113">**동시 라이선스 수량** 필드에 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-113">Enter a value in the **Concurrent License Quantity** field.</span></span>

8.  <span data-ttu-id="d00ae-114">**사용** 확인란을 선택 하 여 라이선스를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-114">Select the **Enabled** check box to enable the license.</span></span>

9.  <span data-ttu-id="d00ae-115">**만료 날짜** 를 설정 하도록 선택 하 고 만료 날짜를 입력 하거나 일정 유틸리티를 사용 하 여 날짜를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-115">Select the **Expiration Date** check box (if you want to set an expiration date), and enter the expiration date or use the calendar utility to select a date.</span></span>

10. <span data-ttu-id="d00ae-116">키를 라이선스와 연결 해야 하는 경우 **라이선스 키** 필드에 라이선스 키 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-116">If you need to associate a key with the license, enter the license key information in the **License Key** field.</span></span>

11. <span data-ttu-id="d00ae-117">**마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="d00ae-117">Click **Finish**.</span></span>

## <span data-ttu-id="d00ae-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d00ae-118">Related topics</span></span>


[<span data-ttu-id="d00ae-119">라이선스 그룹을 사용하여 응용 프로그램을 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="d00ae-119">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)

[<span data-ttu-id="d00ae-120">응용 프로그램 라이선스 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="d00ae-120">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)

[<span data-ttu-id="d00ae-121">라이선스 그룹에서 응용 프로그램을 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="d00ae-121">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)

[<span data-ttu-id="d00ae-122">명명된 라이선스 그룹을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="d00ae-122">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)

[<span data-ttu-id="d00ae-123">제한 없는 라이선스 그룹을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="d00ae-123">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)

 

 





