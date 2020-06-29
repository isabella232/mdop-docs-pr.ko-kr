---
title: MED-V 작업 영역에 대한 소프트웨어 업데이트 관리
description: MED-V 작업 영역에 대한 소프트웨어 업데이트 관리
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824813"
---
# <span data-ttu-id="8168a-103">MED-V 작업 영역에 대한 소프트웨어 업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="8168a-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="8168a-104">배포 된 MED-V 작업 영역의 응용 프로그램에 소프트웨어 업데이트를 제공 하는 데 사용할 수 있는 여러 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="8168a-105">**참고**  MED-V가 자동 업데이트를 수신 하는 방법을 정의 하는 구성 설정을 지정 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역의 자동 업데이트 관리](managing-automatic-updates-for-med-v-workspaces.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8168a-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="8168a-106">MED-V 작업 영역의 소프트웨어 업데이트</span><span class="sxs-lookup"><span data-stu-id="8168a-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="8168a-107">전자 소프트웨어 배포 시스템 사용</span><span class="sxs-lookup"><span data-stu-id="8168a-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="8168a-108">조직에서 ESD (전자 소프트웨어 배포 시스템) 시스템을 사용 하 여 소프트웨어를 배포 하는 경우 물리적 컴퓨터의 응용 프로그램에 대 한 업데이트를 제공 하는 것 처럼이 기능을 사용 하 여 MED-V 작업 영역의 응용 프로그램에 대 한 소프트웨어 업데이트를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="8168a-109">그룹 정책 사용</span><span class="sxs-lookup"><span data-stu-id="8168a-109">Using Group Policy</span></span>**

    <span data-ttu-id="8168a-110">조직에서 그룹 정책을 사용 하 여 소프트웨어를 배포 하는 경우 물리적 컴퓨터의 응용 프로그램에 대 한 업데이트를 제공 하는 것 처럼이를 사용 하 여 MED-V 작업 영역의 응용 프로그램에 소프트웨어 업데이트를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="8168a-111">Application Virtualization (APP-V) 사용</span><span class="sxs-lookup"><span data-stu-id="8168a-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="8168a-112">MED-V와 App-v를 함께 사용 하는 경우 소프트웨어 업데이트를 위해 App-v에 필요한 단계에 따라 MED-V 작업 영역의 응용 프로그램에 소프트웨어 업데이트를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="8168a-113">자세한 내용은 [응용 프로그램 가상화](https://go.microsoft.com/fwlink/?LinkId=122939) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="8168a-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="8168a-114">코어 이미지의 소프트웨어 업데이트</span><span class="sxs-lookup"><span data-stu-id="8168a-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="8168a-115">MED-V 모범 사례로 간주 되지 않더라도 코어 이미지의 응용 프로그램에 소프트웨어 업데이트를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="8168a-116">업데이트를 설치한 후에는 원래 배포 하는 것과 동일한 방법으로 엔터프라이즈에 MED-V 작업 영역을 다시 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="8168a-117">**중요**  소프트웨어 업데이트를 관리 하는 방법은이 방법을 권장 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="8168a-118">또한 핵심 이미지의 소프트웨어를 업데이트 하 고 MED-V 작업 영역을 enterprise에 다시 배포 하는 경우 먼저 설치 프로그램이 다시 실행 되어야 하 고 가상 컴퓨터에 저장 된 모든 데이터가 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8168a-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="8168a-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8168a-119">Related topics</span></span>


[<span data-ttu-id="8168a-120">MED-V 작업 영역에 대한 자동 업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="8168a-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="8168a-121">응용 프로그램 게시를 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="8168a-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="8168a-122">MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="8168a-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





