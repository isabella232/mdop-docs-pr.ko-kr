---
title: MED-V 1.0 릴리스 정보
description: MED-V 1.0 릴리스 정보
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826593"
---
# <span data-ttu-id="d9202-103">MED-V 1.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="d9202-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="d9202-104">MED-V의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="d9202-104">Known Issues with MED-V</span></span>


<span data-ttu-id="d9202-105">이 섹션에서는 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 플랫폼의 일반적인 문제에 대 한 최신 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="d9202-106">이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="d9202-107">이러한 문제는 가능한 경우 이후 릴리스에서 해결 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="d9202-108">파일 다운로드는 웹 리디렉션 규칙을 따르지 않음</span><span class="sxs-lookup"><span data-stu-id="d9202-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="d9202-109">파일 다운로드는 MED-V 작업 영역 정책에 설정 된 웹 리디렉션 규칙을 따르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="d9202-110">콘솔에서 게시 된 응용 프로그램 창을 전체 화면으로 확장 하면 사라집니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="d9202-111">원활한 통합 모드에서 구성 된 MED-V 작업 영역 내에서 콘솔에서 게시 된 응용 프로그램 (예: cmd.exe) 창을 전체 화면으로 확장 하면 응용 프로그램 창이 사라지거나 응답 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="d9202-112">전체 데스크톱 모드에서 작업 하는 경우 데스크톱의 아이콘 위치는 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="d9202-113">전체 데스크톱 모드로 작업할 때 데스크톱의 아이콘에 대 한 수동 위치 변경은 MED-V 작업 영역 세션 간에 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="d9202-114">동일한 도메인에 이름이 같은 로컬 이미지 및 테스트 이미지가 있을 수 없음</span><span class="sxs-lookup"><span data-stu-id="d9202-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="d9202-115">로컬 이미지가 도메인에 가입 되어 있고 관리자가 테스트 이미지와 컴퓨터 이름이 같은 새 버전의 동일한 이미지를 만드는 경우 테스트 이미지가 도메인에 가입 하면 도메인 참가 작업이 실패 하거나, 로컬 이미지가 도메인에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="d9202-116">MED-V는 Windows Aero 기능을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="d9202-117">MED-V는 Windows Aero 기능 (예: Aero 플립 3D)을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="d9202-118">관리 콘솔은 컴퓨터 당 하나의 Windows 사용자만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="d9202-119">MED-V 관리 콘솔은 관리자와 관리 응용 프로그램을 설치한 Windows 사용자만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="d9202-120">MED-V 서버 구성 유틸리티는 MED-V 서버 서비스 컨텍스트가 아닌 사용자 컨텍스트에서 Microsoft SQL Server 연결을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="d9202-121">MED-V는 Microsoft SQL Server 보고서 데이터베이스에서 보고서를 수집 하는 데 MED-V 서버 서비스 컨텍스트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="d9202-122">MED-V 서버 구성 유틸리티는 데이터베이스를 확인 하 고 데이터베이스 연결 문자열을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="d9202-123">데이터베이스에 대해 MED-V 서버 서비스에 대 한 액세스를 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9202-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





