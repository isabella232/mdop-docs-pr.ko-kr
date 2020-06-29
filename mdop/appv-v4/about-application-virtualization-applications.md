---
title: Application Virtualization 응용 프로그램 정보
description: Application Virtualization 응용 프로그램 정보
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820088"
---
# <span data-ttu-id="c6932-103">Application Virtualization 응용 프로그램 정보</span><span class="sxs-lookup"><span data-stu-id="c6932-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="c6932-104">Application Virtualization에서 응용 *프로그램* 은 Microsoft Visio와 같은 실행 프로그램으로, 응용 프로그램 가상화 데스크톱 클라이언트 또는 이전 터미널 서비스에 대 한 원격 데스크톱 서비스에 대 한 클라이언트에는 Application Virtualization Management Server의 클라이언트로 스트리밍됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="c6932-105">응용 프로그램을 클라이언트로 스트림할 수 있으려면 먼저 응용 프로그램 가상화 시퀀서를 사용 하 여 응용 프로그램을 처리 하 여 스트리밍을 준비 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="c6932-106">응용 프로그램 관리</span><span class="sxs-lookup"><span data-stu-id="c6932-106">Managing Applications</span></span>


<span data-ttu-id="c6932-107">사용자가 응용 프로그램을 사용할 수 있도록 하려면 먼저 시스템에 응용 프로그램을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="c6932-108">시스템에 응용 프로그램을 추가 하는 가장 일반적인 방법은 파일을 가져오는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="c6932-109">이 기능에 액세스 하려면 응용 프로그램 가상화 서버 관리 콘솔에서 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 하 고 **응용 프로그램 가져오기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="c6932-110">두 개 이상의 OSD (개방형 소프트웨어 설명자) 파일을 동시에 가져오거나 여러 OSD 파일을 포함할 수 있는 Sequencer 프로젝트 파일 (SPRJ)을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="c6932-111">이 기능을 통해 관련 응용 프로그램을 유사 하 게 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="c6932-112">다음과 같은 기능을 사용 하 여 응용 프로그램을 관리 하는 데 도움이 될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="c6932-113">**응용 프로그램 그룹**-간소화 된 관리를 위해 응용 프로그램의 논리적 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="c6932-114">그룹이 변경 되는 경우 (예: 액세스 권한) 해당 변경 내용이 그룹의 모든 응용 프로그램에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="c6932-115">그룹의 응용 프로그램은 다양 한 패키지에서 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="c6932-116">**다중 선택**-응용 프로그램 속성을 수정할 수 있도록 CTRL 키를 누른 상태로 여러 응용 프로그램을 한 번에 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="c6932-117">그러나 응용 프로그램 간의 관계를 유지 하려는 경우에는 응용 프로그램을 저장 하는 응용 프로그램 그룹을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="c6932-118">**시스템 간 복사**-한 단계에서 동일한 버전의 app-v를 실행 하는 다른 환경으로 응용 프로그램을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="c6932-119">예를 들어 응용 프로그램을 처음 배포 하 고 구성 하는 사용자 수용 테스트 환경이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="c6932-120">테스트 단계를 완료 한 후에는 같은 응용 프로그램 집합 (권한을 포함)을 프로덕션 환경에 복제 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c6932-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="c6932-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c6932-121">Related topics</span></span>


[<span data-ttu-id="c6932-122">Application Virtualization 패키지 정보</span><span class="sxs-lookup"><span data-stu-id="c6932-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="c6932-123">Application Virtualization Server Management Console 정보</span><span class="sxs-lookup"><span data-stu-id="c6932-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="c6932-124">Server Management Console에서 응용 프로그램 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="c6932-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="c6932-125">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="c6932-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





