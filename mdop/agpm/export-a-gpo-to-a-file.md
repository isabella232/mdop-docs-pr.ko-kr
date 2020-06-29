---
title: 파일로 GPO 내보내기
description: 파일로 GPO 내보내기
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820853"
---
# <span data-ttu-id="dfc34-103">파일로 GPO 내보내기</span><span class="sxs-lookup"><span data-stu-id="dfc34-103">Export a GPO to a File</span></span>


<span data-ttu-id="dfc34-104">제어 된 GPO (그룹 정책 개체)를 CAB 파일로 내보내 다른 포리스트의 도메인에 복사 하 고 해당 도메인의 AGPM (고급 그룹 정책 관리)으로 GPO를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="dfc34-105">GPO 설정을 새 또는 기존 GPO로 가져오는 방법에 대 한 자세한 내용은 [파일에서 Gpo 가져오기를](import-a-gpo-from-a-file-ed.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfc34-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="dfc34-106">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="dfc34-107">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfc34-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="dfc34-108">GPO를 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="dfc34-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="dfc34-109">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="dfc34-110">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="dfc34-111">GPO를 마우스 오른쪽 단추로 클릭 한 다음 **내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="dfc34-112">GPO를 내보낼 파일의 파일 이름을 입력 한 다음 **내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="dfc34-113">파일이 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="dfc34-114">이미 존재 하는 경우에는 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="dfc34-115">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="dfc34-115">Additional considerations</span></span>

-   <span data-ttu-id="dfc34-116">이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="dfc34-117">특히 GPO에 대 한 **콘텐츠 목록**보기, **설정 읽기**, **gpo 내보내기** 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc34-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="dfc34-118">추가 참조</span><span class="sxs-lookup"><span data-stu-id="dfc34-118">Additional references</span></span>

-   [<span data-ttu-id="dfc34-119">테스트 환경 사용</span><span class="sxs-lookup"><span data-stu-id="dfc34-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





