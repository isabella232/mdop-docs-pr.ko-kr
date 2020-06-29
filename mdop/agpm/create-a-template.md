---
title: 템플릿 만들기
description: 템플릿 만들기
author: dansimp
ms.assetid: 6992bd55-4a4f-401f-9815-c468bac598ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9ad57204170fc3f49b01b571d82b00e1faf62de0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821068"
---
# <span data-ttu-id="d3e71-103">템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="d3e71-103">Create a Template</span></span>


<span data-ttu-id="d3e71-104">서식 파일을 만들면 새 Gpo를 만들기 위한 출발점으로 사용할 특정 버전의 GPO (그룹 정책 개체)에 대 한 모든 설정을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="d3e71-105">**참고**  서식 파일은 편집 가능한 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="d3e71-106">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="d3e71-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3e71-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d3e71-108">기존 GPO를 기반으로 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="d3e71-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="d3e71-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d3e71-110">세부 정보 창의 **내용** 탭에서 **제어** **또는 제어** 되지 않음 탭을 클릭 하 여 사용 가능한 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="d3e71-111">서식 파일을 만들려는 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **서식 파일로 저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-111">Right-click the GPO from which you want to create a template, then click **Save as Template**.</span></span>

4.  <span data-ttu-id="d3e71-112">서식 파일과 메모의 이름을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-112">Type a name for the template and a comment, then click **OK**.</span></span>

5.  <span data-ttu-id="d3e71-113">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d3e71-114">**서식** 파일 탭에 새 서식 파일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="d3e71-115">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d3e71-115">Additional considerations</span></span>

-   <span data-ttu-id="d3e71-116">이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d3e71-117">특히, 도메인에 대 한 **목록 콘텐츠** 및 템플릿 사용 권한을 **만들어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="d3e71-118">서식 파일의 이름을 바꾸거나 삭제 해도 해당 서식 파일에서 만든 Gpo에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="d3e71-119">서식 파일에는 변경할 수 없으므로 기록 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d3e71-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="d3e71-120">추가 참조</span><span class="sxs-lookup"><span data-stu-id="d3e71-120">Additional references</span></span>

-   [<span data-ttu-id="d3e71-121">템플릿 만들기 및 기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="d3e71-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template.md)

-   [<span data-ttu-id="d3e71-122">새 제어된 GPO 만들기 요청</span><span class="sxs-lookup"><span data-stu-id="d3e71-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo.md)

 

 





