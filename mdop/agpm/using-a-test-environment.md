---
title: 테스트 환경 사용
description: 테스트 환경 사용
author: dansimp
ms.assetid: fc5fcc7c-1ac8-483a-a6bd-2279ae2ee3fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc3ad91747c755efe0576cc62473848094b72ed1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818173"
---
# <span data-ttu-id="e7699-103">테스트 환경 사용</span><span class="sxs-lookup"><span data-stu-id="e7699-103">Using a Test Environment</span></span>


<span data-ttu-id="e7699-104">GPO (그룹 정책 개체)를 프로덕션 환경에 배포 하도록 요청 하기 전에 랩 환경에서 GPO를 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7699-104">Before you request that a Group Policy Object (GPO) be deployed to the production environment, you should test the GPO in a lab environment.</span></span> <span data-ttu-id="e7699-105">테스트 포리스트의 도메인에서 GPO를 개발 하는 경우 GPO를 파일로 내보내고 파일을 프로덕션 포리스트의 도메인으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7699-105">If you develop the GPO in a domain in a test forest, you can export the GPO to a file and import the file to a domain in the production forest.</span></span> <span data-ttu-id="e7699-106">그런 다음 테스트 컴퓨터와 사용자를 포함 하는 OU (조직 구성 단위)에 GPO를 연결 하 여 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7699-106">You can then test the GPO by linking it to an organizational unit (OU) that contains test computers and users.</span></span>

-   [<span data-ttu-id="e7699-107">파일로 GPO 내보내기</span><span class="sxs-lookup"><span data-stu-id="e7699-107">Export a GPO to a File</span></span>](export-a-gpo-to-a-file.md)

-   [<span data-ttu-id="e7699-108">파일에서 GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="e7699-108">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-ed.md)

-   [<span data-ttu-id="e7699-109">별도 조직 구성 단위에서 GPO 테스트</span><span class="sxs-lookup"><span data-stu-id="e7699-109">Test a GPO in a Separate Organizational Unit</span></span>](test-a-gpo-in-a-separate-organizational-unit-agpm40.md)

<span data-ttu-id="e7699-110">**참고**  도메인의 프로덕션 환경에서 GPO를 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7699-110">**Note** You can also import a GPO from the production environment of the domain.</span></span> <span data-ttu-id="e7699-111">자세한 내용은 [프로덕션에서 GPO 가져오기를](import-a-gpo-from-production-agpm40-ed.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7699-111">For more information, see [Import a GPO from Production](import-a-gpo-from-production-agpm40-ed.md).</span></span>

 

 

 





