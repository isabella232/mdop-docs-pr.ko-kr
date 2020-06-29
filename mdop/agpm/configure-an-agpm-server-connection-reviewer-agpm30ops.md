---
title: AGPM 서버 연결 구성
description: AGPM 서버 연결 구성
author: dansimp
ms.assetid: ae78dc74-111d-4509-b0a6-e8b8b451c22a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 50968d8b1b1eb5d464c6dbdb251354a9dc691d62
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819008"
---
# <span data-ttu-id="d36e1-103">AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="d36e1-103">Configure an AGPM Server Connection</span></span>


<span data-ttu-id="d36e1-104">올바른 중앙 보관 저장소에 연결 되어 있는지 확인 하려면 AGPM 서버 연결의 구성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="d36e1-105">AGPM 관리자 (모든 권한)가 사용자를 위해 AGPM 서버 연결을 구성 하지 않은 경우 수동으로 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-105">If an AGPM Administrator (Full Control) has not configured an AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="d36e1-106">AGPM 서버를 선택 하려면</span><span class="sxs-lookup"><span data-stu-id="d36e1-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="d36e1-107">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d36e1-108">세부 정보 창에서 **AGPM 서버** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="d36e1-109">**Agpm 서버** 탭의 옵션을 사용할 수 없는 경우 agpm 관리자가 중앙에서 구성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="d36e1-110">**Agpm 서버** 탭의 옵션을 사용할 수 있는 경우 agpm 서버의 정규화 된 컴퓨터 이름 (예: server.contoso.com)과 agpm 서비스가 수신 대기 하는 포트 (기본적으로 포트 4600)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="d36e1-111">**적용**을 클릭 한 다음 **예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="d36e1-112">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d36e1-112">Additional considerations</span></span>

-   <span data-ttu-id="d36e1-113">선택 된 AGPM 서버는 **콘텐츠** 탭에 표시 되는 Gpo와 **도메인 위임** 탭 설정이 적용 되는 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="d36e1-114">관리 템플릿을 통해 중앙에서 관리 되지 않는 경우 각 그룹 정책 관리자는 해당 도메인의 AGPM 서버를 가리키도록이 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d36e1-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="d36e1-115">추가 참조</span><span class="sxs-lookup"><span data-stu-id="d36e1-115">Additional references</span></span>

-   [<span data-ttu-id="d36e1-116">편집기 작업 수행</span><span class="sxs-lookup"><span data-stu-id="d36e1-116">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="d36e1-117">승인자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="d36e1-117">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="d36e1-118">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="d36e1-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





