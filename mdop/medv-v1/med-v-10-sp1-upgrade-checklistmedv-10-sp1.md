---
title: MED-V 1.0 SP1 업그레이드 검사 목록
description: MED-V 1.0 SP1 업그레이드 검사 목록
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827268"
---
# <span data-ttu-id="2bda2-103">MED-V 1.0 SP1 업그레이드 검사 목록</span><span class="sxs-lookup"><span data-stu-id="2bda2-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="2bda2-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 1.0을 MED-V 1.0 SP1(서비스 Pack1)으로 업그레이드 하려면 클라이언트를 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="2bda2-105">서버는 선택적으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="2bda2-106">서버 업그레이드</span><span class="sxs-lookup"><span data-stu-id="2bda2-106">Server Upgrade</span></span>


**<span data-ttu-id="2bda2-107">MED-V 1.0 서버를 MED-V 1.0 SP1로 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="2bda2-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="2bda2-108">\* &lt; InstallDir &gt; /Servers/configurationserver\* 디렉터리에 있는 다음 파일을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="2bda2-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="2bda2-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="2bda2-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="2bda2-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="2bda2-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="2bda2-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="2bda2-112">\* &lt; InstallDir &gt; /Servers/ServerSettings.xml\* 파일을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="2bda2-113">MED-V 1.0 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="2bda2-114">MED-V 1.0 SP1 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="2bda2-115">백업 파일을 적절 한 디렉터리로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="2bda2-116">MED-V 서버 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="2bda2-117">**참고**  서버 구성이 기본값에서 변경 된 경우 파일이 다른 위치에 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="2bda2-118">클라이언트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="2bda2-118">Client Upgrade</span></span>


<span data-ttu-id="2bda2-119">Med-v 1.0 클라이언트를 MED-V 1.0 SP1로 업그레이드 하려면 MED-V 1.0 클라이언트에 .msp 파일을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="2bda2-120">클라이언트와 MED-V는 자동으로 업그레이드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bda2-120">The client and MED-V are automatically upgraded.</span></span>

 

 





