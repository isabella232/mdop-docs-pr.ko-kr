---
title: MED-V 작업 영역을 다시 시작하고 다시 설정
description: MED-V 작업 영역을 다시 시작하고 다시 설정
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825423"
---
# <span data-ttu-id="db698-103">MED-V 작업 영역을 다시 시작하고 다시 설정</span><span class="sxs-lookup"><span data-stu-id="db698-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="db698-104">문제를 해결 하는 동안 MED-V 작업 영역을 다시 시작 하거나 초기화 해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db698-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="db698-105">MED-V 작업 영역을 다시 시작 하는 것은 기본적으로 물리적 컴퓨터를 다시 시작 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="db698-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="db698-106">MED-V 작업 영역을 다시 설정 하면 처음 설치 하는 동안, 가상 컴퓨터에 저장 된 모든 데이터가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db698-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="db698-107">저장 된 모든 데이터는 삭제 되므로 대부분의 심각한 문제 해결 문제를 해결 하거나 이전에 작업 하는 MED-V 작업 영역을 작업 상태로 복원 하기 위해 MED-V 작업 영역만을 다시 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db698-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="db698-108">MED-V 관리 도구 키트를 여는 방법에 대 한 자세한 내용은 [관리 도구 키트를 사용 하 여 Med-v 문제 해결](troubleshooting-med-v-by-using-the-administration-toolkit.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db698-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="db698-109">MED-V 작업 영역 다시 시작</span><span class="sxs-lookup"><span data-stu-id="db698-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="db698-110">**Med-v 관리 툴킷** 창에서 **Med-v 작업 영역 다시 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db698-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="db698-111">MED-V 작업 영역을 다시 시작할지 확인 하는 대화 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="db698-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="db698-112">**다시 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db698-112">Click **Restart**.</span></span>

    <span data-ttu-id="db698-113">열려 있는 웹 사이트를 실행 중이거나 리디렉션되는 모든 게시 된 응용 프로그램은 MED-V 작업 영역이 다시 시작 될 때 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="db698-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="db698-114">MED-V 작업 영역 다시 설정</span><span class="sxs-lookup"><span data-stu-id="db698-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="db698-115">**Med-v 관리 도구 키트** 창에서 **Med-v 작업 영역 다시 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db698-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="db698-116">MED-V 작업 영역을 다시 설정 하도록 확인 해야 하는 대화 창이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="db698-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="db698-117">**경고가**  MED-V 작업 영역을 다시 설정 하면 처음 설치 프로그램이 다시 실행 되 고 원래 가상 하드 디스크를 로드 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db698-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="db698-118">처음 설치를 실행 한 후 MED-V 작업 영역에 저장 된 모든 데이터는 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db698-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="db698-119">**초기화**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="db698-119">Click **Reset**.</span></span>

    <span data-ttu-id="db698-120">열려 있는 웹 사이트를 실행 중이거나 리디렉션되는 게시 된 모든 응용 프로그램은 MED-V 작업 영역이 다시 설정 될 때 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="db698-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="db698-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="db698-121">Related topics</span></span>


[<span data-ttu-id="db698-122">MED-V 로그 보기 및 구성</span><span class="sxs-lookup"><span data-stu-id="db698-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="db698-123">MED-V 작업 영역 구성 보기</span><span class="sxs-lookup"><span data-stu-id="db698-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





