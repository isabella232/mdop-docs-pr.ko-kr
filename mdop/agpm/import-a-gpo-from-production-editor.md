---
title: 프로덕션에서 GPO 가져오기
description: 프로덕션에서 GPO 가져오기
author: dansimp
ms.assetid: ffa02b2a-2a43-4fc0-a06e-7d4b59022cc3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 239ac6938645325292bfc647ef89a77710c5f074
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820678"
---
# <span data-ttu-id="c40b3-103">프로덕션에서 GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="c40b3-103">Import a GPO from Production</span></span>


<span data-ttu-id="c40b3-104">AGPM (고급 그룹 정책 관리) 외부에서 제어 된 GPO (그룹 정책 개체)를 변경한 경우 프로덕션 환경에서 GPO 복사본을 가져와 보관 저장소에 저장 하 여 보관 및 프로덕션 환경을 일관 된 상태로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-104">If changes are made to a controlled Group Policy object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="c40b3-105">제어 되지 않은 GPO를 가져오려면 GPO를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="c40b3-106">[이전에는 미제어 GPO에 대 한 요청 제어권을](request-control-of-a-previously-uncontrolled-gpo.md)참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="c40b3-106">See [Request Control of a Previously Uncontrolled GPO](request-control-of-a-previously-uncontrolled-gpo.md).)</span></span>

<span data-ttu-id="c40b3-107">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="c40b3-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="c40b3-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c40b3-109">프로덕션 환경에서 GPO를 가져오려면</span><span class="sxs-lookup"><span data-stu-id="c40b3-109">To import a GPO from the production environment</span></span>**

1.  <span data-ttu-id="c40b3-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c40b3-111">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="c40b3-112">GPO를 마우스 오른쪽 단추로 클릭 한 다음 **프로덕션에서 가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="c40b3-113">GPO의 감사 내역에 대 한 설명을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-113">Type a comment for the audit trail of the GPO, then click **OK**.</span></span>

### <span data-ttu-id="c40b3-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="c40b3-114">Additional considerations</span></span>

-   <span data-ttu-id="c40b3-115">이 절차를 수행 하려면 기본적으로 편집자, 승인자 또는 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c40b3-116">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집**, **gpo 배포**또는 gpo **삭제** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40b3-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="c40b3-117">추가 참조</span><span class="sxs-lookup"><span data-stu-id="c40b3-117">Additional references</span></span>

-   [<span data-ttu-id="c40b3-118">GPO 만들기, 제어 또는 가져오기</span><span class="sxs-lookup"><span data-stu-id="c40b3-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





