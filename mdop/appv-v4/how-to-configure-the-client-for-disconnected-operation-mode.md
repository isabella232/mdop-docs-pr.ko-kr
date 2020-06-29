---
title: 연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법
description: 연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817818"
---
# <span data-ttu-id="1022c-103">연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="1022c-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="1022c-104">연결이 끊긴 작업 모드는 응용 프로그램 가상화 (App-v) 데스크톱 클라이언트 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 Application Virtualization (App-v) 클라이언트를 사용 하 여 클라이언트가 App-v 관리 서버에 연결할 수 없는 경우 클라이언트의 파일 시스템 캐시에 저장 된 응용 프로그램을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="1022c-105">**중요**  여러 사용자를 지원 하기 위해 RD ° (원격 데스크톱 세션 호스트) 서버 (이전의 터미널 서버)가 팜에 연결 된 대규모 조직의 경우 단일 App-v 관리 서버를 사용 하 여 팜 지원의 단일 지점 실패를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="1022c-106">RDSession Host 팜을 지원 하기 위해 고가용성을 제공 하려면 두 개 이상의 App-v 관리 서버를 연결 하 여 동일한 데이터베이스를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="1022c-107">연결이 끊긴 작업 모드를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="1022c-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="1022c-108">연결 되지 않은 작동 모드를 사용 하도록 다음 레지스트리 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="1022c-109">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="1022c-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="1022c-110">연결이 끊긴 작업 모드 사용에 시간 제한을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="1022c-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="1022c-111">다음 레지스트리 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="1022c-112">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="1022c-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="1022c-113">다음 레지스트리 키 값을 연결이 끊긴 작업 모드를 제한 하는 데 사용할 시간 (분)으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="1022c-114">유효한 값의 범위는 1 – 999999입니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="1022c-115">기본값은 90 일 또는 129600 분입니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="1022c-116">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="1022c-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="1022c-117">연결이 끊긴 작업 모드에 대해 원격 데스크톱 서비스에 맞게 클라이언트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1022c-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="1022c-118">연결 되지 않은 작동 모드를 사용 하도록 다음 레지스트리 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="1022c-119">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="1022c-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="1022c-120">다음 레지스트리 키 값을 0 (영)으로 설정 하 여 연결이 끊긴 작업 모드의 무제한 사용을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="1022c-121">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="1022c-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="1022c-122">성능을 개선 하기 위해 모든 패키지가 캐시에 미리 로드 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1022c-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="1022c-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1022c-123">Related topics</span></span>


[<span data-ttu-id="1022c-124">연결이 끊긴 작업 모드</span><span class="sxs-lookup"><span data-stu-id="1022c-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="1022c-125">명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="1022c-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





