---
title: 패키지 열기 명령을 사용하여 패키지를 업그레이드하는 방법
description: 패키지 열기 명령을 사용하여 패키지를 업그레이드하는 방법
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816518"
---
# <span data-ttu-id="141aa-103">패키지 열기 명령을 사용하여 패키지를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="141aa-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="141aa-104">패키지 열기 명령을 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 업그레이드 하거나 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="141aa-105">명령줄을 사용 하 여 기존 가상 응용 프로그램 패키지를 업그레이드 하면 원본 버전의 sft 파일이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="141aa-106">명령줄을 사용 하 여 패키지를 업그레이드 하기 전에 연결 된 sft 파일을 백업 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="141aa-107">패키지 열기 명령을 사용 하 여 패키지를 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="141aa-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="141aa-108">업그레이드할 패키지를 열려면 Application Virtualization (App-v) 콘솔에서 **파일**을 선택 하 고 **업그레이드를 위해 패키지를 엽니다**.</span><span class="sxs-lookup"><span data-stu-id="141aa-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="141aa-109">**열기** 대화 상자에서 업그레이드할 패키지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="141aa-110">**시퀀싱** 마법사를 시작 하려면 **도구**, **시퀀싱 마법사**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="141aa-111">구성 변경 내용을 적용 한 마법사를 완료 하 여 새 시퀀싱 된 응용 프로그램을 저장 하 고 **파일**, **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="141aa-112">패키지 이름에 버전 번호를 추가 하려면 Sequencer 콘솔에서 **도구**, **옵션**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="141aa-113">**패키지 버전을 파일 이름에 추가를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="141aa-114">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-114">Click **OK**.</span></span>

    <span data-ttu-id="141aa-115">**중요**  패키지 버전을 사용 하 여 파일 이름을 업데이트 하는 것은 업그레이드를 성공적으로 완료 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="141aa-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="141aa-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="141aa-116">Related topics</span></span>


[<span data-ttu-id="141aa-117">명령줄을 사용하여 가상 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="141aa-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





