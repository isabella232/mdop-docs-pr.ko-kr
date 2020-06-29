---
title: 기본 템플릿 설정
description: 기본 템플릿 설정
author: dansimp
ms.assetid: 07208b6b-cb3a-4f6c-9c84-36d4dc1486d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51a13c2c57e38adca883a6eb962d8c5eae4316db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820233"
---
# <span data-ttu-id="4335c-103">기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="4335c-103">Set a Default Template</span></span>


<span data-ttu-id="4335c-104">편집기로, 새 Gpo (그룹 정책 개체)를 만드는 모든 그룹 정책 관리자가 사용할 수 있는 기본 서식 파일을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="4335c-105">**참고**  서식 파일은 편집 가능한 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="4335c-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="4335c-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="4335c-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="4335c-108">새 Gpo를 만들 때 사용할 기본 서식 파일 설정</span><span class="sxs-lookup"><span data-stu-id="4335c-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="4335c-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4335c-110">세부 정보 창의 **콘텐츠** 탭에서 **서식 파일** 탭을 클릭 하 여 사용 가능한 서식 파일을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="4335c-111">기본값으로 설정할 서식 파일을 마우스 오른쪽 단추로 클릭 한 다음 **기본값으로 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="4335c-112">**예** 를 클릭 하 여 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="4335c-113">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="4335c-114">기본 서식 파일은 파란색 아이콘을 포함 하며, 상태 **는 서식 파일 탭의** **서식 파일 (기본값)** 으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="4335c-115">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="4335c-115">Additional considerations</span></span>

-   <span data-ttu-id="4335c-116">이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="4335c-117">특히, 도메인에 대 한 **목록 콘텐츠** 및 템플릿 사용 권한을 **만들어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="4335c-118">서식 파일을 기본값으로 설정 하면 그룹 정책 관리자가 새 Gpo를 만들 때 **새 제어 된 gpo** 대화 상자에서 처음에 선택 된 서식 파일이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="4335c-119">그러나 모든 설정을 포함 하지 않는 \*\* &lt; 빈 gpo &gt; \*\*를 포함 하 여 다른 gpo 템플릿을 선택 하는 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="4335c-120">서식 파일의 이름을 바꾸거나 삭제 해도 해당 서식 파일에서 만든 Gpo에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="4335c-121">서식 파일에는 변경할 수 없으므로 기록 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4335c-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="4335c-122">추가 참조</span><span class="sxs-lookup"><span data-stu-id="4335c-122">Additional references</span></span>

-   [<span data-ttu-id="4335c-123">템플릿 만들기 및 기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="4335c-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="4335c-124">새 제어된 GPO 만들기 요청</span><span class="sxs-lookup"><span data-stu-id="4335c-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





