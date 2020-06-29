---
title: Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법
description: Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법
author: dansimp
ms.assetid: 48503b04-0de7-48de-98ee-4623a712a341
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ca9ab54c8b4cee06e0b17d8b5dee3d3ca7ce69c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817223"
---
# <span data-ttu-id="b76e8-103">Server Management Console에서 응용 프로그램 라이선스를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-103">How to Manage Application Licenses in the Server Management Console</span></span>


<span data-ttu-id="b76e8-104">Application Virtualization Server 관리 콘솔은 응용 프로그램 가상화 플랫폼을 관리 하는 데 사용 하는 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-104">The Application Virtualization Server Management Console is the interface you use to manage the Application Virtualization platform.</span></span> <span data-ttu-id="b76e8-105">여기서는 응용 프로그램 라이선스 그룹을 추가, 제거, 구성 및 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-105">From it, you can add, remove, configure, and control application license groups.</span></span>

<span data-ttu-id="b76e8-106">**중요**  앱-V 클라이언트 응용 프로그램 원본 루트 (ASR) 설정이 관리 서버 이외의 모든 유형의 스트리밍 원본 (예: 스트리밍 서버, IIS 서버 또는 파일 서버)을 사용 하도록 구성 된 경우 관리 서버는 라이선스 정책을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-106">**Important** If the App-V client Application Source Root (ASR) setting is configured to use any type of streaming source other than the Management Server, for example a Streaming Server, an IIS server, or a File server, then the Management Server is unable to enforce its licensing policy.</span></span>

 

## <span data-ttu-id="b76e8-107">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="b76e8-107">In This Section</span></span>


<a href="" id="how-to-create-an-application-license-group"></a>[<span data-ttu-id="b76e8-108">응용 프로그램 라이선스 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-108">How to Create an Application License Group</span></span>](how-to-create-an-application-license-group.md)  
<span data-ttu-id="b76e8-109">라이선스 그룹에서 새 응용 프로그램을 만드는 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-109">Provides a procedure for creating a new application in a license group.</span></span>

<a href="" id="how-to-associate-an-application-with-a-license-group"></a>[<span data-ttu-id="b76e8-110">라이선스 그룹을 사용하여 응용 프로그램을 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-110">How to Associate an Application with a License Group</span></span>](how-to-associate-an-application-with-a-license-group.md)  
<span data-ttu-id="b76e8-111">라이선스 그룹에 응용 프로그램을 추가 하는 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-111">Provides a procedure for adding an application to a license group.</span></span>

<a href="" id="how-to-remove-an-application-from-a-license-group"></a>[<span data-ttu-id="b76e8-112">라이선스 그룹에서 응용 프로그램을 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-112">How to Remove an Application from a License Group</span></span>](how-to-remove-an-application-from-a-license-group.md)  
<span data-ttu-id="b76e8-113">라이선스 그룹에서 응용 프로그램을 제거 하는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-113">Provides a procedure for removing an application from a license group.</span></span>

<a href="" id="how-to-remove-an-application-license-group"></a>[<span data-ttu-id="b76e8-114">응용 프로그램 라이선스 그룹을 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-114">How to Remove an Application License Group</span></span>](how-to-remove-an-application-license-group.md)  
<span data-ttu-id="b76e8-115">이 섹션에는 응용 프로그램 라이선스 그룹을 삭제 하는 데 필요한 단계가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-115">This section includes the steps necessary to delete an application license group.</span></span>

<a href="" id="how-to-set-up-an-unlimited-license-group"></a>[<span data-ttu-id="b76e8-116">제한 없는 라이선스 그룹을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-116">How to Set Up an Unlimited License Group</span></span>](how-to-set-up-an-unlimited-license-group.md)  
<span data-ttu-id="b76e8-117">그룹의 응용 프로그램에 액세스 하는 데 무제한의 사용자를 허용 하는 새 라이선스 그룹을 만드는 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-117">Provides a procedure for creating a new unlimited license group, allowing an unlimited number of users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-concurrent-license-group"></a>[<span data-ttu-id="b76e8-118">동시 라이선스 그룹을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-118">How to Set Up a Concurrent License Group</span></span>](how-to-set-up-a-concurrent-license-group.md)  
<span data-ttu-id="b76e8-119">특정 개수의 동시 사용자가 그룹의 응용 프로그램에 액세스할 수 있도록 새 동시 라이선스 그룹을 만드는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-119">Provides a procedure for creating a new concurrent license group, allowing a specific number of concurrent users to access the applications in the group.</span></span>

<a href="" id="how-to-set-up-a-named-license-group"></a>[<span data-ttu-id="b76e8-120">명명된 라이선스 그룹을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-120">How to Set Up a Named License Group</span></span>](how-to-set-up-a-named-license-group.md)  
<span data-ttu-id="b76e8-121">특정 사용자가 그룹의 응용 프로그램에 액세스할 수 있도록 허용 하는 새로운 무제한 라이선스 그룹을 만드는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b76e8-121">Provides a procedure for creating a new unlimited license group, allowing specific users to access the applications in the group.</span></span>

## <span data-ttu-id="b76e8-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b76e8-122">Related topics</span></span>


[<span data-ttu-id="b76e8-123">Application Virtualization Server Management Console에서 관리 작업을 수행하는 방법</span><span class="sxs-lookup"><span data-stu-id="b76e8-123">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





