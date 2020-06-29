---
title: 명령줄을 사용하여 클라이언트를 설치하는 방법
description: 명령줄을 사용하여 클라이언트를 설치하는 방법
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817323"
---
# <span data-ttu-id="b5e1f-103">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5e1f-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="b5e1f-104">이 섹션의 항목에는 setup.exe 또는 setup.msi를 사용 하 여 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트 또는 Application Virtualization (App-v) 데스크톱 클라이언트를 설치 하는 절차가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="b5e1f-105">설치 프로그램 중 하나를 실행 하려면 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="b5e1f-106">선택적 명령줄 매개 변수를 사용 하 여 설치 중에 앱-V 클라이언트에 특정 구성 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="b5e1f-107">매개 변수를 사용 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="b5e1f-108">클라이언트를 배포 하기 전에 컴퓨터에 레지스트리 설정을 적용 한 경우 (예: 그룹 정책을 사용 하는 경우) 이러한 설정이 유지 되 고 추가 명령줄 매개 변수가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="b5e1f-109">명령줄 매개 변수 값이 같은 설정의 기존 값을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="b5e1f-110">**참고**  VDI 서버 구현과 같이 읽기 전용 캐시와 함께 사용 하기 위해 App-v 클라이언트를 설치 하는 경우에는 클라이언트가 읽기 전용일 때 응용 프로그램을 업데이트 하지 않도록 *Autoloadtarget* 매개 변수를 no로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="b5e1f-111">설치 후 이러한 매개 변수 값을 설정 하는 방법에 대 한 자세한 내용은 Application Virtualization (App-v) 운영 가이드에서 [명령줄을 사용 하 여 App-v 클라이언트 레지스트리 설정을 구성 하는 방법을](https://go.microsoft.com/fwlink/?LinkId=169355) 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=169355) .</span><span class="sxs-lookup"><span data-stu-id="b5e1f-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="b5e1f-112">**참고**  사용자 컴퓨터의 구성 설정이 클라이언트 설치 경로에 종속 되는 경우 Application Virtualization (App-v) 4.5 클라이언트는 해당 설치 파일을 이전 버전이 아닌 다른 폴더에 복사 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="b5e1f-113">기본적으로 App-v 4.5 클라이언트의 새 설치는 설치 파일을 \\Program Files\\Microsoft Application 가상화 클라이언트 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="b5e1f-114">이전 버전의 클라이언트가 이미 설치 되어 있는 경우 App-v 4.5 클라이언트 설치 관리자를 실행 하면 기존 설치 폴더를 사용 하 여 기존 클라이언트의 업그레이드를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="b5e1f-115">\ [Template 토큰 값 \]</span><span class="sxs-lookup"><span data-stu-id="b5e1f-115">\[Template Token Value\]</span></span>

<span data-ttu-id="b5e1f-116">**참고**  App-v 버전 4.6 이상에서 App-v 클라이언트가 설치 되 면 SFTLDR.DLL Windows\\system32 디렉터리에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="b5e1f-117">64 비트 시스템에 App-v 클라이언트가 설치 되어 있으면 SFTLDR\_WOW64.DLL Windows\\SysWOW64 디렉터리에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="b5e1f-118">\ [Template 토큰 값 \]</span><span class="sxs-lookup"><span data-stu-id="b5e1f-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="b5e1f-119">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="b5e1f-119">In This Section</span></span>


<span data-ttu-id="b5e1f-120">다음 항목에서는 setup.exe 또는 setup.msi를 사용 하 여 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트, Application Virtualization (App-v) 데스크톱 클라이언트를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="b5e1f-121">Setup.exe를 사용하여 App-V Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5e1f-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="b5e1f-122">setup.exe 프로그램을 사용 하 여 App-v 클라이언트를 설치 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="b5e1f-123">Setup.msi를 사용하여 App-V Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5e1f-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="b5e1f-124">setup.msi 프로그램을 사용 하 여 필수 구성 요소 소프트웨어를 설치 하는 단계별 절차와 앱 V 클라이언트도 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e1f-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="b5e1f-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b5e1f-125">Related topics</span></span>


[<span data-ttu-id="b5e1f-126">Application Virtualization Client 설치 관리자 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b5e1f-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="b5e1f-127">Application Virtualization Client를 수동으로 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5e1f-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="b5e1f-128">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5e1f-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="b5e1f-129">App-V Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="b5e1f-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





