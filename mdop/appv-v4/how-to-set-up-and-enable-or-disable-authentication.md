---
title: 인증을 설정하고 사용 또는 사용 중지하는 방법
description: 인증을 설정하고 사용 또는 사용 중지하는 방법
author: dansimp
ms.assetid: 1e43d0c5-a467-4a8b-b656-93f75d7deb82
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0eb69cf58db245e34b3455c8ef09758d38d8860
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816593"
---
# <span data-ttu-id="a9b89-103">인증을 설정하고 사용 또는 사용 중지하는 방법</span><span class="sxs-lookup"><span data-stu-id="a9b89-103">How to Set Up and Enable or Disable Authentication</span></span>


<span data-ttu-id="a9b89-104">응용 프로그램 가상화 서버 관리 콘솔을 사용 하 여 시스템에 액세스할 수 있는 사용자를 정의 하는 Windows 인증을 설정 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-104">The Application Virtualization Server Management Console lets you enable or disable Windows authentication, which lets you to define who has access to the system.</span></span> <span data-ttu-id="a9b89-105">콘솔의 **공급자 정책 결과** 창에서 다음 절차를 사용 하 여 인증을 설정 하 고 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-105">You can use the following procedures to set up and disable authentication from the **Provider Policies Results** pane of the console.</span></span>

<span data-ttu-id="a9b89-106">**참고**  일반적으로 새 공급자 정책 마법사를 통해 공급자 정책을 추가할 때 인증을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-106">**Note** Normally, you set up authentication when you add a provider policy through the New Provider Policy Wizard.</span></span>

 

**<span data-ttu-id="a9b89-107">인증 설정</span><span class="sxs-lookup"><span data-stu-id="a9b89-107">To set up authentication</span></span>**

1.  <span data-ttu-id="a9b89-108">**공급자 정책** 노드를 클릭 하 여 **결과** 창에 공급자 정책 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-108">Click the **Provider Policies** node to display the list of provider policies in the **Results** pane.</span></span>

2.  <span data-ttu-id="a9b89-109">공급자 정책을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-109">Right-click the provider policy, and select **Properties**.</span></span>

3.  <span data-ttu-id="a9b89-110">**공급자 파이프라인** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-110">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="a9b89-111">**인증** 확인란이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-111">Make sure the **Authentication** check box is selected.</span></span>

5.  <span data-ttu-id="a9b89-112">드롭다운 목록에서 인증 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-112">Select the authentication level from the drop-down list.</span></span>

6.  <span data-ttu-id="a9b89-113">**적용** 또는 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-113">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="a9b89-114">인증을 사용 하거나 사용 하지 않으려면</span><span class="sxs-lookup"><span data-stu-id="a9b89-114">To enable or disable authentication</span></span>**

1.  <span data-ttu-id="a9b89-115">**공급자 정책** 노드를 클릭 하 여 **결과** 창에 공급자 정책 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-115">Click the **Provider Policies** node to display the list of provider policies in the **Results** pane.</span></span>

2.  <span data-ttu-id="a9b89-116">공급자 정책을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-116">Right-click the provider policy, and select **Properties**.</span></span>

3.  <span data-ttu-id="a9b89-117">**공급자 파이프라인** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-117">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="a9b89-118">인증 확인란 **을 선택 하 여 인증** 을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-118">Select the **Authentication** check box to enable authentication.</span></span> <span data-ttu-id="a9b89-119">확인란의 선택을 취소 하 여 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9b89-119">Clear the box to disable it.</span></span>

## <span data-ttu-id="a9b89-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a9b89-120">Related topics</span></span>


[<span data-ttu-id="a9b89-121">Server Management Console에서 Application Virtualization 시스템을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="a9b89-121">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





