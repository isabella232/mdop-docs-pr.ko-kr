---
title: 웹 기반 응용 프로그램에 대한 가상 환경을 만드는 방법
description: 웹 기반 응용 프로그램에 대한 가상 환경을 만드는 방법
author: dansimp
ms.assetid: d2b16e9d-369c-4bd6-b2a0-16dd24c0e32c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a53bec6869b3af9666775600b181c57eec3be93
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817663"
---
# <span data-ttu-id="6fd25-103">웹 기반 응용 프로그램에 대한 가상 환경을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="6fd25-103">How to Create a Virtual Environment for a Web-Based Application</span></span>


<span data-ttu-id="6fd25-104">격리 하려는 웹 응용 프로그램에 대해 별도의 가상 환경을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-104">You can create separate virtual environments for web applications you want to isolate.</span></span> <span data-ttu-id="6fd25-105">웹 기반 응용 프로그램에 서로 충돌 하는 구성이 있는 플러그 인이 필요한 경우 별도의 웹 환경을 만드는 것이 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-105">Creating separate web environments is useful if the web-based applications require plug-ins of have configurations that conflict with each other.</span></span>

**<span data-ttu-id="6fd25-106">웹 기반 응용 프로그램의 가상 환경을 만들려면</span><span class="sxs-lookup"><span data-stu-id="6fd25-106">To create a virtual environment for a Web-based application</span></span>**

1.  <span data-ttu-id="6fd25-107">시퀀싱 마법사를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-107">Open the sequencing wizard.</span></span> <span data-ttu-id="6fd25-108">응용 프로그램 시퀀싱에 대 한 자세한 내용은 [새 응용 프로그램의 순서를 만드는 방법을](how-to-sequence-a-new-application.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fd25-108">For more information about sequencing an application see [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span>

2.  <span data-ttu-id="6fd25-109">**모니터 설치** 페이지에서 응용 프로그램 설치 모니터링을 시작 하려면 **모니터링 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-109">On the **Monitor Installation** page, to start monitoring the installation of the application, click **Begin Monitoring**.</span></span> <span data-ttu-id="6fd25-110">웹 브라우저를 열고 응용 프로그램과 연결 된 설치 관리자 파일로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-110">Open a web browser and navigate to the installer file associated with the application.</span></span> <span data-ttu-id="6fd25-111">응용 프로그램을 설치 하 고 필요한 모든 사후 설치 구성 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-111">Install the application, and perform any required post installation configuration tasks.</span></span>

3.  <span data-ttu-id="6fd25-112">응용 프로그램이 시작 되도록 하려면 응용 프로그램을 세 번 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-112">To ensure the applications starts, open the application three times.</span></span>

4.  <span data-ttu-id="6fd25-113">동일한 가상 환경에 있어야 하는 추가 응용 프로그램을 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-113">Install and configure any additional applications that need to reside in the same virtual environment.</span></span>

5.  <span data-ttu-id="6fd25-114">시퀀싱 마법사의 나머지 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-114">Complete the remainder of the Sequencing Wizard.</span></span>

6.  <span data-ttu-id="6fd25-115">응용 프로그램을 저장 하려면 **파일**을 선택 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fd25-115">To save the application, select **File**, and click **Save**.</span></span>

## <span data-ttu-id="6fd25-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6fd25-116">Related topics</span></span>


[<span data-ttu-id="6fd25-117">Application Virtualization Sequencer에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="6fd25-117">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





