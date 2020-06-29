---
title: App-V 5.1 배포 검사 목록
description: App-V 5.1 배포 검사 목록
author: dansimp
ms.assetid: 44bed85a-e4f5-49d7-a308-a2b681f76372
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0864335e505996a3ea379b09de6a1aaa7fbe1676
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814772"
---
# <span data-ttu-id="5f5af-103">App-V 5.1 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="5f5af-103">App-V 5.1 Deployment Checklist</span></span>


<span data-ttu-id="5f5af-104">이 검사 목록을 사용 하 여 Microsoft App-v (Application Virtualization) 5.1 배포 중에 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

**<span data-ttu-id="5f5af-105">참고</span><span class="sxs-lookup"><span data-stu-id="5f5af-105">Note</span></span>**  
<span data-ttu-id="5f5af-106">이 검사 목록에서는 권장 단계 및 App-v 5.1 기능을 배포할 때 고려해 야 하는 항목의 상위 수준 목록을 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.1 features.</span></span> <span data-ttu-id="5f5af-107">이 검사 목록을 스프레드시트 프로그램에 복사 하 여 사용을 위해 사용자 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="5f5af-108">작업</span><span class="sxs-lookup"><span data-stu-id="5f5af-108">Task</span></span></th>
<th align="left"><span data-ttu-id="5f5af-109">참조</span><span class="sxs-lookup"><span data-stu-id="5f5af-109">References</span></span></th>
<th align="left"><span data-ttu-id="5f5af-110">참고</span><span class="sxs-lookup"><span data-stu-id="5f5af-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5f5af-111">계획 단계를 완료 하 여 App-v 5.1 배포에 대 한 컴퓨팅 환경을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-111">Complete the planning phase to prepare the computing environment for App-V 5.1 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-51-planning-checklist.md" data-raw-source="[App-V 5.1 Planning Checklist](app-v-51-planning-checklist.md)"><span data-ttu-id="5f5af-112">App-V 5.1 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="5f5af-112">App-V 5.1 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5f5af-113">App-v 5.1 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 App-v 5.1 기능 설치에 지원 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-113">Review the App-V 5.1 supported configurations information to make sure selected client and server computers are supported for App-V 5.1 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="5f5af-114">App-V 5.1 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="5f5af-114">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="5f5af-115">앱-V 5.1 설치 프로그램을 실행 하 여 환경에 필요한 App-v 5.1 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-115">Run App-V 5.1 Setup to deploy the required App-V 5.1 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5f5af-116">참고</span><span class="sxs-lookup"><span data-stu-id="5f5af-116">Note</span></span></strong><br/><p><span data-ttu-id="5f5af-117">설치 중에 생성 되는 서버 및 관련 URL의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="5f5af-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="5f5af-118">이 정보는 설치 과정에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f5af-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-51beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)"><span data-ttu-id="5f5af-119">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="5f5af-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="5f5af-120">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="5f5af-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="5f5af-121">App-V 5.1 Server 배포 방법</span><span class="sxs-lookup"><span data-stu-id="5f5af-121">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="5f5af-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5f5af-122">Related topics</span></span>


[<span data-ttu-id="5f5af-123">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="5f5af-123">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









