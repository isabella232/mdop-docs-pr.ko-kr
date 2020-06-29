---
title: MED-V 작업 영역에서 프린터 관리
description: MED-V 작업 영역에서 프린터 관리
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826118"
---
# <span data-ttu-id="009e4-103">MED-V 작업 영역에서 프린터 관리</span><span class="sxs-lookup"><span data-stu-id="009e4-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="009e4-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에서 프린터 리디렉션은 최종 사용자에 게 MED-V 가상 컴퓨터와 호스트 컴퓨터 간에 일관 된 인쇄 환경을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="009e4-105">이 항목에서는 MED-V 작업 영역에서 인쇄를 관리 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="009e4-106">MED-V 작업 영역에서 프린터 관리</span><span class="sxs-lookup"><span data-stu-id="009e4-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="009e4-107">대부분의 경우 MED-V는 프린터 리디렉션을 자동으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="009e4-108">처음 설치가 완료 되 면 MED-V는 호스트에 설치 된 모든 네트워크 프린터를 식별 하 고, 네트워크 인쇄 서버에서 해당 드라이버를 검색 하 고, 검색 된 경우 MED-V 작업 영역에 관련 드라이버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="009e4-109">모든 드라이버가 검색 되 고 설치 되 면 MED-V가 MED-V 작업 영역을 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="009e4-110">MED-V 작업 영역이 다시 시작 된 후에만 호스트 프린터가 있고 일반적으로 몇 분 내에 게스트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="009e4-111">**참고**  MED-V 작업 영역에서 응용 프로그램이 실행 되는 경우 최종 사용자에 게 다시 시작을 계속할지 또는 나중에 연기할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="009e4-112">실행 중인 응용 프로그램이 없는 경우 다시 시작이 자동 이며 최종 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="009e4-113">MED-V가 다시 시작 될 때마다 호스트에 새 프린터가 설치 되어 있는지 확인 하 고, 발견 되 면 네트워크 인쇄 서버에서 해당 드라이버를 검색 하 여 게스트에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="009e4-114">그런 다음 처음 설치를 완료 했을 때와 마찬가지로 MED-V 작업 영역을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="009e4-115">**중요**  게스트에 관련 드라이버를 설치 하면 다시 시작 하는 경우에만 해당 프린터가 게스트에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="009e4-116">드라이버를 찾을 수 없거나 설치할 수 없는 경우, 최종 사용자가 네트워크 프린터를 사용할 수 있도록 게스트에 수동으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="009e4-117">다음 목록에서는 몇 가지 추가 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="009e4-118">**Med-v는 네트워크 프린터만 관리**합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="009e4-119">호스트에 로컬로 설치 된 프린터용 드라이버는 자동으로 게스트에 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="009e4-120">**Med-v는 인쇄 서버에 있는 경우 프린터 드라이버만 설치**합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="009e4-121">찾을 수 없는 경우 프린터 드라이버를 수동으로 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="009e4-122">**게스트에 수동으로 설치 된 프린터에는 호스트에서 액세스할 수 없습니다**.</span><span class="sxs-lookup"><span data-stu-id="009e4-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="009e4-123">기본적으로 MED-V는 게스트에서 호스트로의 프린터 리디렉션만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="009e4-124">**경고가**  게스트에 프린터를 수동으로 설치 하 고 나중에 호스트에 동일한 프린터가 설치 되는 경우 게스트에 프린터가 두 번 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="009e4-125">이 문제를 방지 하기 위해 MED-V는 리디렉션을 사용 하지 않도록 설정 하 고 게스트에 수동으로 프린터를 설치 하거나 리디렉션을 사용 하도록 설정 하 고 게스트에 수동으로 프린터를 설치 하지 않는 등 한 가지 방법 으로만 프린터 리디렉션을 관리 하는 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="009e4-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="009e4-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="009e4-126">Related topics</span></span>


[<span data-ttu-id="009e4-127">MED-V 작업 영역 설정 관리</span><span class="sxs-lookup"><span data-stu-id="009e4-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





