---
title: App-V Client 제거 방법
description: App-V Client 제거 방법
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816523"
---
# <span data-ttu-id="d3d41-103">App-V Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="d3d41-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="d3d41-104">컴퓨터에서 응용 프로그램 가상화 클라이언트를 제거 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="d3d41-105">Application Virtualization 데스크톱 클라이언트를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="d3d41-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="d3d41-106">제어판에서 **프로그램 추가/제거** (또는 Windows Vista에서 **프로그램 및 기능**)를 두 번 클릭 한 다음 **Microsoft Application Virtualization 데스크톱 클라이언트**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="d3d41-107">표시 되는 대화 상자에서 **예** 를 클릭 하 여 제거 프로세스를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="d3d41-108">**중요**  제거 프로세스는 취소 또는 중단할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="d3d41-109">계속 하기 전에 Microsoft Application Virtualization 클라이언트 트레이 응용 프로그램을 닫아야 한다는 메시지가 나타나면 알림 영역의 App-v 아이콘을 마우스 오른쪽 단추로 클릭 하 고 **끝내기** 를 선택 하 여 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="d3d41-110">그런 다음 **다시 시도** 를 클릭 하 여 제거 과정을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="d3d41-111">**중요**  하나 이상의 가상 응용 프로그램을 사용 하 고 있다는 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="d3d41-112">계속 하기 전에 열려 있는 응용 프로그램을 닫고 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="d3d41-113">그런 다음 **확인** 을 클릭 하 여 제거 과정을 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="d3d41-114">진행률 표시줄에 남은 시간이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="d3d41-115">이 단계가 완료 되 면 제거 프로세스를 완료 하기 위해 모든 관련 드라이버를 중지할 수 있도록 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="d3d41-116">**참고**  제거 프로세스가 완료 된 후 다음 레지스트리 키가 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3d41-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="d3d41-117">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="d3d41-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="d3d41-118">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="d3d41-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="d3d41-119">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "Client" = dword: 00000000</span><span class="sxs-lookup"><span data-stu-id="d3d41-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="d3d41-120">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span><span class="sxs-lookup"><span data-stu-id="d3d41-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="d3d41-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d3d41-121">Related topics</span></span>


[<span data-ttu-id="d3d41-122">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3d41-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="d3d41-123">Application Virtualization Client를 수동으로 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3d41-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="d3d41-124">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3d41-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





