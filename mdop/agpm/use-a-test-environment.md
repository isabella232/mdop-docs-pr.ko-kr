---
title: 테스트 환경 사용
description: 테스트 환경 사용
author: dansimp
ms.assetid: b8d7b3ee-030a-4b5b-8223-4a3276fd47a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2299fb6eaf7c75f6841056f67a05fe025ea19bb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818233"
---
# <span data-ttu-id="84d97-103">테스트 환경 사용</span><span class="sxs-lookup"><span data-stu-id="84d97-103">Use a Test Environment</span></span>


<span data-ttu-id="84d97-104">프로덕션 환경에 배포 하기 전에 OU (조직 구성 단위)를 사용 하 여 Gpo (그룹 정책 개체)를 테스트 하는 경우 테스트 OU에 액세스 하는 데 필요한 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-104">If you use a testing organizational unit (OU) to test Group Policy objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="84d97-105">테스트 OU의 사용은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="84d97-106">테스트 OU를 사용 하려면</span><span class="sxs-lookup"><span data-stu-id="84d97-106">To use a test OU</span></span>**

1.  <span data-ttu-id="84d97-107">편집할 GPO를 체크 아웃 한 경우 **그룹 정책 관리 콘솔**에서 gpo를 관리 하는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="84d97-108">테스트할 GPO의 체크 아웃 된 복사본을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="84d97-109">이름 앞에 **\ [AGPM \]** 이 붙습니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-109">The name will be preceded with **\[AGPM\]**.</span></span> <span data-ttu-id="84d97-110">(나열 되지 않은 경우 **작업**을 클릭 한 다음 **새로 고침**).</span><span class="sxs-lookup"><span data-stu-id="84d97-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="84d97-111">이름을 알파벳순으로 정렬 하면 **\ [AGPM \]** gpo가 일반적으로 목록 맨 위에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="84d97-112">GPO를 테스트 OU로 끌어서 놓습니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="84d97-113">테스트 OU에서 GPO에 대 한 링크를 만들지 여부를 묻는 대화 상자에서 **확인을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="84d97-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="84d97-114">Additional considerations</span></span>

-   <span data-ttu-id="84d97-115">테스트가 완료 되 면 GPO를 체크 인하면 GPO의 체크 아웃 된 복사본에 대 한 링크가 자동으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84d97-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="84d97-116">추가 참조</span><span class="sxs-lookup"><span data-stu-id="84d97-116">Additional references</span></span>

-   [<span data-ttu-id="84d97-117">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="84d97-117">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





