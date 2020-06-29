---
title: App-V 5.0 배포 검사 목록
description: App-V 5.0 배포 검사 목록
author: dansimp
ms.assetid: d6d93152-82b4-4b02-8b11-ed21d3331f00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f213271a6d4b90961846b49553c07f1eb6e4c03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814844"
---
# <span data-ttu-id="ebd03-103">App-V 5.0 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="ebd03-103">App-V 5.0 Deployment Checklist</span></span>


<span data-ttu-id="ebd03-104">이 검사 목록을 사용 하 여 Microsoft App-v (Application Virtualization) 5.0 배포 중에 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

**<span data-ttu-id="ebd03-105">참고</span><span class="sxs-lookup"><span data-stu-id="ebd03-105">Note</span></span>**  
<span data-ttu-id="ebd03-106">이 검사 목록에서는 권장 단계 및 App-v 5.0 기능을 배포할 때 고려해 야 하는 항목의 상위 수준 목록을 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.0 features.</span></span> <span data-ttu-id="ebd03-107">이 검사 목록을 스프레드시트 프로그램에 복사 하 여 사용을 위해 사용자 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="ebd03-108">작업</span><span class="sxs-lookup"><span data-stu-id="ebd03-108">Task</span></span></th>
<th align="left"><span data-ttu-id="ebd03-109">참조</span><span class="sxs-lookup"><span data-stu-id="ebd03-109">References</span></span></th>
<th align="left"><span data-ttu-id="ebd03-110">참고</span><span class="sxs-lookup"><span data-stu-id="ebd03-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ebd03-111">계획 단계를 완료 하 여 App-v 5.0 배포에 대 한 컴퓨팅 환경을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-111">Complete the planning phase to prepare the computing environment for App-V 5.0 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-50-planning-checklist.md" data-raw-source="[App-V 5.0 Planning Checklist](app-v-50-planning-checklist.md)"><span data-ttu-id="ebd03-112">App-V 5.0 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="ebd03-112">App-V 5.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ebd03-113">App-v 5.0 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 App-v 5.0 기능 설치에 지원 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-113">Review the App-V 5.0 supported configurations information to make sure selected client and server computers are supported for App-V 5.0 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-50-supported-configurations.md" data-raw-source="[App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md)"><span data-ttu-id="ebd03-114">App-V 5.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="ebd03-114">App-V 5.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ebd03-115">앱-V 5.0 설치 프로그램을 실행 하 여 환경에 필요한 App-v 5.0 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-115">Run App-V 5.0 Setup to deploy the required App-V 5.0 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ebd03-116">참고</span><span class="sxs-lookup"><span data-stu-id="ebd03-116">Note</span></span></strong><br/><p><span data-ttu-id="ebd03-117">설치 중에 생성 되는 서버 및 관련 URL의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebd03-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="ebd03-118">이 정보는 설치 과정에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebd03-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"><span data-ttu-id="ebd03-119">Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="ebd03-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="ebd03-120">App-V Client 배포 방법</span><span class="sxs-lookup"><span data-stu-id="ebd03-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="ebd03-121">App-V 5.0 Server 배포 방법</span><span class="sxs-lookup"><span data-stu-id="ebd03-121">How to Deploy the App-V 5.0 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="ebd03-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ebd03-122">Related topics</span></span>


[<span data-ttu-id="ebd03-123">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="ebd03-123">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









