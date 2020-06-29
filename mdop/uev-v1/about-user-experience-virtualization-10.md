---
title: User Experience Virtualization 1.0 정보
description: User Experience Virtualization 1.0 정보
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822713"
---
# <span data-ttu-id="46765-103">User Experience Virtualization 1.0 정보</span><span class="sxs-lookup"><span data-stu-id="46765-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="46765-104">Microsoft UE-V (User Experience Virtualization)는 사용자가 응용 프로그램 설정 및 Windows 운영 체제 설정에 변경한 내용을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="46765-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="46765-105">설정 저장소 위치에 대 한 사용자 설정이 캡처 및 중앙 집중화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46765-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="46765-106">그런 다음 데스크톱 컴퓨터, 랩톱 컴퓨터, VDI (가상 데스크톱 인프라) 세션을 비롯 하 여 사용자가 액세스 하는 다른 컴퓨터에 이러한 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46765-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="46765-107">사용자 환경 가상화는 설정 위치 템플릿을 사용 하 여 모니터링 하 고 중앙 집중화 하는 사용자 컴퓨터의 응용 프로그램 및 Windows 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46765-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="46765-108">설정 위치 템플릿은 각 응용 프로그램 또는 운영 체제 설정과 연결 되는 파일 및 레지스트리 위치를 지정 하는 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="46765-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="46765-109">서식 파일에는 설정 값이 포함 되어 있지 않습니다. 이 파일에는 모니터링할 설정의 위치만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46765-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="46765-110">사용자가 컴퓨터에서 작업 하는 경우 응용 프로그램 설정 및 Windows 설정이 UE-V를 통해 모니터링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46765-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="46765-111">응용 프로그램 설정의 값은 사용자가 응용 프로그램을 닫을 때 설정 저장소 서버에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46765-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="46765-112">Windows 설정에 대 한 값은 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있는 경우 또는 컴퓨터에서 원격으로 연결이 끊어질 때 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46765-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="46765-113">관리자는 UE-V 설정 위치 템플릿을 만들어 로밍 하는 엔터프라이즈 응용 프로그램 설정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46765-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="46765-114">UE-V는 일부 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치 템플릿 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="46765-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="46765-115">UE-V의 기본 응용 프로그램 및 설정 목록은 [ue-v 1.0를 사용 하 여 동기화 할 응용 프로그램 계획](planning-which-applications-to-synchronize-with-ue-v-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46765-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="46765-116">UEV 1.0 릴리스 노트</span><span class="sxs-lookup"><span data-stu-id="46765-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="46765-117">이 문서에 대 한 자세한 내용 및 최신 뉴스에 대 한 자세한 내용은 [MICROSOFT ue-v (User Experience Virtualization) 1.0 릴리스 정보](microsoft-user-experience-virtualization--ue-v--10-release-notes.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46765-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="46765-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="46765-118">Related topics</span></span>


[<span data-ttu-id="46765-119">User Experience Virtualization 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="46765-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="46765-120">Microsoft User Experience Virtualization(UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="46765-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="46765-121">UE-V 1.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="46765-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





