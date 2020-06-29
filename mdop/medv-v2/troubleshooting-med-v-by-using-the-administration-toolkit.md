---
title: 관리 도구 키트를 사용하여 MED-V 문제 해결
description: 관리 도구 키트를 사용하여 MED-V 문제 해결
author: dansimp
ms.assetid: 6c096a1c-b9ce-4ec7-8dfd-5286e3b9a617
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1eaa493e5603e8a1275a6ff5f189739b168f319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825373"
---
# <span data-ttu-id="6c7f9-103">관리 도구 키트를 사용하여 MED-V 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6c7f9-103">Troubleshooting MED-V by Using the Administration Toolkit</span></span>


<span data-ttu-id="6c7f9-104">Med-v 관리 도구 키트를 사용 하 여 MED-V 작업 영역의 특정 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-104">Use the MED-V Administration Toolkit to troubleshoot certain problems in a MED-V workspace.</span></span> <span data-ttu-id="6c7f9-105">MED-V 관리 도구 키트를 사용 하 여 이벤트 로그에 액세스 하 고, MED-V 작업 영역을 다시 시작 하거나, 다시 설정 하 고, MED-V 작업 영역에서 게시 된 응용 프로그램 및 리디렉션 웹 주소를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-105">The MED-V Administration Toolkit lets you access and configure event logs, restart or reset the MED-V workspace, and view the published applications and redirected web addresses in the MED-V workspace.</span></span> <span data-ttu-id="6c7f9-106">MED-V 관리 도구 키트를 사용 하 여 전체 화면 모드로 MED-V 작업 영역 가상 컴퓨터를 열 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-106">You can also use the MED-V Administration Toolkit to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="6c7f9-107">MED-V 관리 도구 키트를 열려면</span><span class="sxs-lookup"><span data-stu-id="6c7f9-107">To Open the MED-V Administration Toolkit</span></span>


<span data-ttu-id="6c7f9-108">MED-V 관리 도구 키트를 열려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-108">Perform the following steps to open the MED-V Administration Toolkit:</span></span>

1.  <span data-ttu-id="6c7f9-109">문제 해결 하려는 MED-V 작업 영역이 포함 된 호스트 컴퓨터에서 명령 프롬프트 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-109">On the host computer that contains the MED-V workspace you are troubleshooting, open a Command Prompt window.</span></span>

2.  <span data-ttu-id="6c7f9-110">%Systemdrive%\\Program Files\\Microsoft Enterprise 데스크톱 가상화를 찾아 보세요.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-110">Browse to %systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization.</span></span>

3.  <span data-ttu-id="6c7f9-111">명령 프롬프트에 **Medvhost/toolkit**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-111">At the command prompt, type **MedvHost /toolkit**.</span></span>

<span data-ttu-id="6c7f9-112">MED-V 관리 도구 키트가 열리면 도구 키트를 사용 하 여 문제 해결 중에 발견 되는 MED-V 작업 영역의 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-112">After the MED-V Administration Toolkit opens, you can use the toolkit to help resolve issues in the MED-V workspace found during troubleshooting.</span></span>

## <span data-ttu-id="6c7f9-113">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="6c7f9-113">In this Section</span></span>


<a href="" id="viewing-and-configuring-med-v-logs"></a>[<span data-ttu-id="6c7f9-114">MED-V 로그 보기 및 구성</span><span class="sxs-lookup"><span data-stu-id="6c7f9-114">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)  
<span data-ttu-id="6c7f9-115">MED-V 관리 도구 키트를 사용 하 여 호스트 컴퓨터와 게스트 가상 컴퓨터에서 MED-V 이벤트 로그를 수집 하 고 관리 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-115">Describes how to use the MED-V Administration Toolkit to collect and manage MED-V event logs in the host computer and the guest virtual machine.</span></span>

<a href="" id="restarting-and-resetting-a-med-v-workspace"></a>[<span data-ttu-id="6c7f9-116">MED-V 작업 영역을 다시 시작하고 다시 설정</span><span class="sxs-lookup"><span data-stu-id="6c7f9-116">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)  
<span data-ttu-id="6c7f9-117">MED-V 관리 도구 키트를 사용 하 여 MED-V 작업 영역을 다시 시작 하 고 초기화 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-117">Describes how to restart and reset MED-V workspaces by using the MED-V Administration Toolkit.</span></span>

<a href="" id="viewing-med-v-workspace-configurations"></a>[<span data-ttu-id="6c7f9-118">MED-V 작업 영역 구성 보기</span><span class="sxs-lookup"><span data-stu-id="6c7f9-118">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)  
<span data-ttu-id="6c7f9-119">Med-v 관리 도구 키트를 사용 하 여 MED-V 작업 영역에서 게시 된 응용 프로그램 및 리디렉션된 웹 주소를 확인 하는 방법과 MED-V 작업 영역 가상 컴퓨터를 전체 화면 모드로 여는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c7f9-119">Describes how to use the MED-V Administration Toolkit to view the published applications and redirected web addresses in a MED-V workspace and how to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="6c7f9-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6c7f9-120">Related topics</span></span>


[<span data-ttu-id="6c7f9-121">MED-V 이벤트 로그 메시지</span><span class="sxs-lookup"><span data-stu-id="6c7f9-121">MED-V Event Log Messages</span></span>](med-v-event-log-messages.md)

[<span data-ttu-id="6c7f9-122">MED-V 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6c7f9-122">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





