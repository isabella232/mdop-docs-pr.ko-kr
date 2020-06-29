---
title: PowerShell을 사용하여 클라이언트 구성을 수정하는 방법
description: PowerShell을 사용하여 클라이언트 구성을 수정하는 방법
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813812"
---
# <span data-ttu-id="46582-103">PowerShell을 사용하여 클라이언트 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="46582-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="46582-104">다음 절차를 사용 하 여 App-v 5.1 클라이언트 구성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="46582-104">Use the following procedure to configure the App-V 5.1 client configuration.</span></span>

**<span data-ttu-id="46582-105">PowerShell을 사용 하 여 App-v 5.1 클라이언트 구성을 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="46582-105">To modify App-V 5.1 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="46582-106">PowerShell을 사용 하 여 클라이언트 설정을 구성 하려면 **Set-AppvClientConfiguration** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46582-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span> <span data-ttu-id="46582-107">PowerShell을 설치 하는 방법에 대 한 자세한 내용과 cmdlet 목록에는 [Powershell cmdlet을 로드 하는 방법과 Cmdlet 도움말](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46582-107">For more information about installing PowerShell, and a list of cmdlets see, [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span></span>

2.  <span data-ttu-id="46582-108">클라이언트 구성을 수정 하려면 PowerShell 명령 프롬프트를 열고 필요한 매개 변수를 사용 하 여 다음 cmdlet **Set-AppvClientConfiguration** 를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="46582-108">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="46582-109">예:</span><span class="sxs-lookup"><span data-stu-id="46582-109">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="46582-110">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="46582-110">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="46582-111">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="46582-111">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="46582-112">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="46582-112">Got an App-V issue?</span></span>** <span data-ttu-id="46582-113">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46582-113">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="46582-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="46582-114">Related topics</span></span>


[<span data-ttu-id="46582-115">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="46582-115">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





