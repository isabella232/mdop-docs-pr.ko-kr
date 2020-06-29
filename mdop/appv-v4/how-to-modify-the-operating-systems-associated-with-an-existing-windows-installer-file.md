---
title: 기존 Windows Installer 파일로 연결된 운영 체제를 수정하는 방법
description: 기존 Windows Installer 파일로 연결된 운영 체제를 수정하는 방법
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816953"
---
# <span data-ttu-id="35b1b-103">기존 Windows Installer 파일로 연결된 운영 체제를 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="35b1b-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="35b1b-104">다음 절차를 사용 하 여 App-v Sequencer를 사용 하 여 만든 기존 Windows Installer (**MSI**) 파일과 연결 된 운영 체제 버전을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="35b1b-105">기존 Windows Installer 파일의 운영 체제를 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="35b1b-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="35b1b-106">운영 체제만 설치 되어 있는 환경의 컴퓨터에 App-v 시퀀서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="35b1b-107">또는 가상 환경을 실행 하는 컴퓨터 (예: Microsoft 가상 PC)에 시퀀서를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="35b1b-108">이 방법은 최소한의 추가 구성으로 다시 사용할 수 있는 깨끗 한 시퀀싱 환경을 유지 관리 하는 것이 더 쉽기 때문에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="35b1b-109">App-v 시퀀서를 설치 하는 방법에 대 한 자세한 내용은 [Sequencer를 설치 하는 방법을](how-to-install-the-sequencer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35b1b-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="35b1b-110">수정 하려는 Windows Installer 파일이 포함 된 전체 가상 응용 프로그램 패키지를 Sequencer를 실행 하는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="35b1b-111">Windows installer 파일을 수정 하려면 Sequencer 콘솔을 열고 **패키지**  /  **열기**를 선택한 다음 Windows Installer 파일과 연결 된 가상 응용 프로그램 패키지가 저장 된 위치를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="35b1b-112">운영 체제를 추가 하거나 제거 하려면 Sequencer 콘솔에서 **배포** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="35b1b-113">Windows Installer 파일과 연결 될 추가 운영 체제를 지정 하려면 원하는 운영 체제를 선택한 다음 **선택한** 운영 체제 목록 컨트롤을 가리키는 화살표를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="35b1b-114">운영 체제 연결을 제거 하려면 제거 하려는 운영 체제를 선택 하 고 **사용 가능한** 운영 체제 목록 컨트롤을 가리키는 화살표를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="35b1b-115">가상 응용 프로그램 패키지와 연결 되는 새 Windows Installer를 만들려면 **Microsoft Windows installer (MSI) 패키지 생성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="35b1b-116">또는 **도구**  /  **MSI 만들기**를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="35b1b-117">**참고**  **Tools** / **MSI를 만들어** 새 Windows Installer 파일을 만드는 도구를 선택 하는 경우이 절차의 **6 단계** 를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="35b1b-118">가상 응용 프로그램 패키지를 저장 하려면 **패키지**  /  **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b1b-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="35b1b-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="35b1b-119">Related topics</span></span>


[<span data-ttu-id="35b1b-120">Application Virtualization Sequencer에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="35b1b-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





