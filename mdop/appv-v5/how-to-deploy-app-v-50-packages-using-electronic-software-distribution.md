---
title: 전자 소프트웨어 배포를 사용하여 App-V 5.0 패키지를 배포하는 방법
description: 전자 소프트웨어 배포를 사용하여 App-V 5.0 패키지를 배포하는 방법
author: dansimp
ms.assetid: 08e5e05b-dbb8-4be7-b2d8-721ef627da81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 33af02c5e9fad7408f9719ecd1a7fa90eacfeb29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814188"
---
# <span data-ttu-id="db94c-103">전자 소프트웨어 배포를 사용하여 App-V 5.0 패키지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="db94c-103">How to deploy App-V 5.0 Packages Using Electronic Software Distribution</span></span>


<span data-ttu-id="db94c-104">ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 app-v 클라이언트에 App-v 5.0 가상 응용 프로그램을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-104">You can use an electronic software distribution (ESD) system to deploy App-V 5.0 virtual applications to App-V clients.</span></span> <span data-ttu-id="db94c-105">자세한 내용은 사용 중인 ESD와 함께 제공 되는 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db94c-105">For details, see the documentation available with the ESD you are using.</span></span>

<span data-ttu-id="db94c-106">ESD를 사용 하 여 App-v 패키지를 배포 하는 구성 요소 요구 사항 및 옵션은 [전자 소프트웨어 배포 시스템을 사용 하 여 app-v 5.0 배포 계획](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db94c-106">For component requirements and options for using an ESD to deploy App-V packages, see [Planning to Deploy App-V 5.0 with an Electronic Software Distribution System](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md).</span></span>

<span data-ttu-id="db94c-107">다음 방법 중 하나를 사용 하 여 패키지를 ESD (앱-V 클라이언트 컴퓨터)에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-107">Use one of the following methods to publish packages to App-V client computers with an ESD:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db94c-108">메서드</span><span class="sxs-lookup"><span data-stu-id="db94c-108">Method</span></span></th>
<th align="left"><span data-ttu-id="db94c-109">설명</span><span class="sxs-lookup"><span data-stu-id="db94c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db94c-110">타사 ESD에서 제공 하는 기능</span><span class="sxs-lookup"><span data-stu-id="db94c-110">Functionality provided by a third-party ESD</span></span></p></td>
<td align="left"><p><span data-ttu-id="db94c-111">타사 ESD의 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-111">Use the functionality in a third-party ESD.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db94c-112">독립 실행형 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="db94c-112">Stand-alone Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="db94c-113">처음으로 응용 프로그램을 시퀀싱 할 때 생성 되는 연결 된 Windows Installer (.msi) 파일을 사용 하 여 대상 클라이언트 컴퓨터에 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-113">Install the application on the target client computer by using the associated Windows Installer (.msi) file that is created when you initially sequence an application.</span></span> <span data-ttu-id="db94c-114">Windows Installer 파일에는 패키지를 구성 하 고 필요한 패키지 파일을 클라이언트에 복사 하는 데 사용 되는 관련 앱-V 5.0 패키지 파일 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-114">The Windows Installer file contains the associated App-V 5.0 package file information used to configure a package and copies the required package files to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db94c-115">PowerShell</span><span class="sxs-lookup"><span data-stu-id="db94c-115">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="db94c-116">PowerShell cmdlet을 사용 하 여 가상화 된 응용 프로그램을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-116">Use PowerShell cmdlets to deploy virtualized applications.</span></span> <span data-ttu-id="db94c-117">PowerShell 및 App-v 5.0 사용에 대 한 자세한 내용은 <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)"> powershell을 사용 하 여 App-v 관리를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db94c-117">For more information about using PowerShell and App-V 5.0, see <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)">Administering App-V by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="db94c-118">ESD를 사용 하 여 앱-V 5.0 패키지를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="db94c-118">To deploy App-V 5.0 packages by using an ESD</span></span>**

1.  <span data-ttu-id="db94c-119">환경의 컴퓨터에 App-v 5.0 Sequencer를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-119">Install the App-V 5.0 Sequencer on a computer in your environment.</span></span> <span data-ttu-id="db94c-120">Sequencer 설치에 대 한 자세한 내용은 Sequencer를 [설치 하는 방법을](how-to-install-the-sequencer-beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db94c-120">For more information about installing the sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="db94c-121">앱-V 5.0 시퀀서를 사용 하 여 가상 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-121">Use the App-V 5.0 Sequencer to create virtual application.</span></span> <span data-ttu-id="db94c-122">가상 응용 프로그램을 만드는 방법에 대 한 자세한 내용은 [app-v 5.0 가상화 된 응용 프로그램 만들기 및 관리](creating-and-managing-app-v-50-virtualized-applications.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db94c-122">For information about creating a virtual application, see [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

3.  <span data-ttu-id="db94c-123">가상 응용 프로그램을 만든 후 ESD 솔루션을 사용 하 여 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-123">After you create the virtual application, deploy the package by using your ESD solution.</span></span>

    <span data-ttu-id="db94c-124">System Center Configuration Manager를 사용 하는 경우 먼저 [구성 관리자의 응용 프로그램 관리 소개](https://go.microsoft.com/fwlink/?LinkId=281816) 에서 앱-V 5.0 및 시스템 Center2012 구성 관리자 사용에 대 한 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-124">If you are using System Center Configuration Manager, start by reviewing [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) for information about using App-V 5.0 and System Center2012 Configuration Manager.</span></span>

    <span data-ttu-id="db94c-125">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="db94c-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="db94c-126">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="db94c-127">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="db94c-127">Got an App-V issue?</span></span>** <span data-ttu-id="db94c-128">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db94c-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="db94c-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="db94c-129">Related topics</span></span>


[<span data-ttu-id="db94c-130">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="db94c-130">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





