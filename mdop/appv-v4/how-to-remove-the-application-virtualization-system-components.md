---
title: Application Virtualization 시스템 구성 요소를 제거하는 방법
description: Application Virtualization 시스템 구성 요소를 제거하는 방법
author: dansimp
ms.assetid: 45bb1e43-8708-48b7-9169-e3659f32686f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 450357bd682c1a6801f40a76a75f25516f55e7bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816773"
---
# <span data-ttu-id="7de7f-103">Application Virtualization 시스템 구성 요소를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="7de7f-103">How to Remove the Application Virtualization System Components</span></span>


<span data-ttu-id="7de7f-104">다음 절차를 사용 하 여 대상 컴퓨터에서 모든 또는 선택한 응용 프로그램 가상화 소프트웨어 구성 요소를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-104">You can use the following procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

**<span data-ttu-id="7de7f-105">단일 컴퓨터에서 모든 구성 요소를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="7de7f-105">To remove all components from a single computer</span></span>**

1.  <span data-ttu-id="7de7f-106">Windows 바탕 화면에서 \*\* &gt; 설정 시작 &gt; \*\*제어판을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-106">From the Windows desktop, click **Start &gt; Settings &gt; Control Panel**.</span></span>

2.  <span data-ttu-id="7de7f-107">제어판 창에서 **프로그램 추가/제거**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-107">In the Control Panel window, double-click **Add or Remove Programs**.</span></span>

3.  <span data-ttu-id="7de7f-108">**프로그램 추가/제거** 페이지에서 **Microsoft System Center 응용 프로그램 가상 관리 서버** 또는 **Microsoft System center 응용 프로그램 스트리밍 서버**를 선택 하 고 **제거**를 클릭 한 다음 프롬프트에서 **예** 를 클릭 하 여 컴퓨터에서 모든 응용 프로그램 가상화 소프트웨어 구성 요소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-108">On the **Add or Remove Programs** page, select **Microsoft System Center Application Virtual Management Server** or **Microsoft System Center Application Streaming Server**, click **Remove**, and then click **Yes** at the prompt to remove all Application Virtualization software components from the computer.</span></span>

**<span data-ttu-id="7de7f-109">컴퓨터에서 하나 이상의 구성 요소 제거</span><span class="sxs-lookup"><span data-stu-id="7de7f-109">To remove one or more components from a computer</span></span>**

1.  <span data-ttu-id="7de7f-110">네트워크에서 응용 프로그램 가상화 시스템 설정 프로그램의 위치로 이동 하 여 네트워크에서이 프로그램을 실행 하거나 해당 디렉터리를 대상 컴퓨터로 복사한 다음 **Setup.exe**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-110">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="7de7f-111">**시작** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-111">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="7de7f-112">**프로그램 유지 관리** 페이지에서 **수정을** 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-112">On the **Program Maintenance** page, select **Modify** and then click **Next**.</span></span>

4.  <span data-ttu-id="7de7f-113">**사용자 지정 설정** 페이지에서 제거 하려는 응용 프로그램 가상화 구성 요소를 선택 취소 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-113">On the **Custom Setup** page, deselect the Application Virtualization component or components you want to remove, and then click **Next**.</span></span>

5.  <span data-ttu-id="7de7f-114">**프로그램 수정 준비** 페이지에서 선택한 구성 요소를 제거 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-114">On the **Ready to Modify the Program** page, to remove the selected components, click **Install**.</span></span>

6.  <span data-ttu-id="7de7f-115">**설치 마법사 완료** 페이지에서 마법사를 닫으려면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-115">On the **Installation Wizard Completed** page, to close the wizard click **Finish**.</span></span> <span data-ttu-id="7de7f-116">**예** 를 클릭 하 여 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de7f-116">Click **Yes** to restart the computer.</span></span>

## <span data-ttu-id="7de7f-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7de7f-117">Related topics</span></span>


[<span data-ttu-id="7de7f-118">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="7de7f-118">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





