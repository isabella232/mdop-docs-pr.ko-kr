---
title: App-V 4.6 SP3 릴리스 정보
description: App-V 4.6 SP3 릴리스 정보
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819793"
---
# <span data-ttu-id="d6763-103">App-V 4.6 SP3 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="d6763-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="d6763-104">이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="d6763-105">이 릴리스 정보는 App-v (Microsoft Application Virtualization) 관리 시스템을 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="d6763-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="d6763-106">이 릴리스 정보에는 Application Virtualization (App-v) 4.6 SP3을 성공적으로 설치 하는 데 도움이 되는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="d6763-107">이 문서에는 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="d6763-108">이러한 릴리스 노트와 다른 App-v 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d6763-109">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="d6763-110">보안 취약점 및 바이러스 방지</span><span class="sxs-lookup"><span data-stu-id="d6763-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="d6763-111">보안 취약점과 바이러스 로부터 보호 하려면 설치 하는 새 소프트웨어에 대해 사용 가능한 최신 보안 업데이트를 설치 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="d6763-112">자세한 내용은 [Microsoft 보안 웹 사이트](https://go.microsoft.com/fwlink/?LinkId=3482) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="d6763-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="d6763-113">Application Virtualization 4.6 SP3의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="d6763-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="d6763-114">이 섹션에서는 Microsoft App-v (Application Virtualization) 4.6 SP3과 관련 된 문제에 대 한 최신 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="d6763-115">이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="d6763-116">가능 하면 이후 릴리스에서 문제가 해결 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="d6763-117">가상 환경 내에서 Microsoft Windows 8.1의 인터넷 Explorer11을 사용 하 여 하이퍼링크를 열 수 없음</span><span class="sxs-lookup"><span data-stu-id="d6763-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="d6763-118">가상 환경에서 하이퍼링크를 열려고 하는 경우 Internet Explorer 11을 사용 하 여 Windows 8.1에서 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="d6763-119">지금 Internet Explorer 11이 기본적으로 사용 하도록 설정 된 향상 된 보호 모드 (EPM)와 함께 제공 되기 때문에,이로 인해 App-v가 필요한 레지스트리 키, 파일 및 통신 포트 개체에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="d6763-120">해결 방법: App-v 패키지를 열기 전에 인터넷 Explorer11에서 EPM을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="d6763-121">이렇게 하면 가상 환경 내에서 Internet Explorer를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6763-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="d6763-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d6763-122">Related topics</span></span>


[<span data-ttu-id="d6763-123">Microsoft Application Virtualization 4.6 SP3 정보</span><span class="sxs-lookup"><span data-stu-id="d6763-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 





