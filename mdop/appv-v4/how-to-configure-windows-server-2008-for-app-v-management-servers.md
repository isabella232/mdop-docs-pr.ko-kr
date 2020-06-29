---
title: App-V Management Server용 Windows Server 2008을 구성 방법
description: App-V Management Server용 Windows Server 2008을 구성 방법
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817723"
---
# <span data-ttu-id="f386b-103">App-V Management Server용 Windows Server 2008을 구성 방법</span><span class="sxs-lookup"><span data-stu-id="f386b-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="f386b-104">Microsoft App-v (Application Virtualization) 관리 웹 서비스를 설치 하는 Windows Server 2008 서버에서 서버에 역할을 하는 IIS (인터넷 정보 서비스)를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="f386b-105">Vserver 설치를 지원 하도록 Windows Server 2008를 구성 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="f386b-106">Windows Server2008 컴퓨터에 IIS를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="f386b-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="f386b-107">Windows Server2008 컴퓨터에서 **시작**을 클릭 하 고 **모든 프로그램**, **관리 도구**를 차례로 클릭 한 다음 **서버 관리자** 를 클릭 하 여 서버 관리자를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="f386b-108">서버 관리자에서 **역할** 노드를 마우스 오른쪽 단추로 클릭 하 고 **역할 추가** 를 클릭 하 여 **역할 추가 마법사**를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="f386b-109">**역할 추가 마법사**의 **서버 역할 선택** 페이지에서 **웹 서버 (IIS)** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="f386b-110">메시지가 표시 되 면 **필수 기능 추가** 를 클릭 하 여 종속 기능을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="f386b-111">**서버 역할 선택** 페이지에서 **다음**을 클릭 하 고 **다음** 을 다시 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="f386b-112">역할 **추가 마법사**의 **역할 서비스 선택** 페이지에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="f386b-113">**응용 프로그램 개발**에서 **ASP.NET** 를 선택 하 고 메시지가 표시 되 면 **필수 역할 서비스 추가** 를 클릭 하 여 종속 역할 서비스 및 기능을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="f386b-114">**보안**에서 **Windows 인증**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="f386b-115">**관리 도구** 노드에서 **IIS 관리 스크립트 및 도구**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="f386b-116">**IIS6 관리 호환성**에서 **IIS6 메타 베이스 호환성** 및 **IIS6 WMI 호환성** 이 모두 선택 되어 있는지 확인 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="f386b-117">**설치 선택 확인** 페이지에서 **설치**를 클릭 한 다음 마법사의 나머지 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="f386b-118">**닫기를** 클릭 하 여 **역할 추가 마법사**를 종료 한 다음 서버 관리자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="f386b-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="f386b-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f386b-119">Related topics</span></span>


[<span data-ttu-id="f386b-120">Application Virtualization 배포 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f386b-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="f386b-121">Application Virtualization 배포 및 업그레이드 검사 목록</span><span class="sxs-lookup"><span data-stu-id="f386b-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





