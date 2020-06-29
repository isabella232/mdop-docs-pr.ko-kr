---
title: 클라이언트에 가상 응용 프로그램을 게시하는 방법
description: 클라이언트에 가상 응용 프로그램을 게시하는 방법
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816873"
---
# <span data-ttu-id="3507c-103">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="3507c-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="3507c-104">전자 소프트웨어 배포 시스템을 사용 하 여 응용 프로그램 가상화를 배포 하는 경우 다음 절차 중 하나를 사용 하 여 사용자에 게 응용 프로그램 패키지를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="3507c-105">독립 실행형 Windows Installer 파일을 사용 하 여 패키지를 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="3507c-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="3507c-106">클라이언트는 *Requireauthorizationifcached* 매개 변수를 0 (영)으로 설정 하 여 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="3507c-107">이 매개 변수를 설정 하는 방법에 대 한 자세한 내용은 [Application Virtualization 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3507c-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="3507c-108">Windows Installer 파일 및 SFT 파일을 대상 컴퓨터의 동일한 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="3507c-109">컴퓨터에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="3507c-110">Windows Installer 및 패키지 매니페스트를 사용 하 여 패키지를 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="3507c-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="3507c-111">Windows Installer 파일을 대상 컴퓨터와 SFT 파일을 스트리밍 서버의 콘텐츠 공유에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="3507c-112">각 사용자의 컴퓨터에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="3507c-113">**중요**  OVERRIDEURL의 경우 모든 백슬래시 문자는 앞의 백슬래시를 사용 하 여 이스케이프 되어야 하며, OVERRIDEURL 경로가 올바르게 구문 분석 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="3507c-114">또한 값이 파일의 경로인 경우를 제외 하 고 속성 및 값을 대문자로 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="3507c-115">SFTMIME을 사용 하 여 패키지를 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="3507c-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="3507c-116">컴퓨터의 모든 사용자에 대해 응용 프로그램을 게시 하는 방법의 예는 사용자 컴퓨터에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3507c-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="3507c-117">이러한 및 다른 SFTMIME 명령에 대 한 자세한 내용은 [Sftmime 명령 참조](sftmime--command-reference.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3507c-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="3507c-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3507c-118">Related topics</span></span>


[<span data-ttu-id="3507c-119">게시 방법 결정</span><span class="sxs-lookup"><span data-stu-id="3507c-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="3507c-120">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="3507c-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="3507c-121">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="3507c-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="3507c-122">Application Virtualization Client에 대한 독립 실행형 배달 시나리오</span><span class="sxs-lookup"><span data-stu-id="3507c-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





