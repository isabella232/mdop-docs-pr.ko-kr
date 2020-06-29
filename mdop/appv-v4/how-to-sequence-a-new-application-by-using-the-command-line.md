---
title: 명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법
description: 명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816688"
---
# <span data-ttu-id="baf22-103">명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="baf22-103">How to Sequence a New Application by Using the Command Line</span></span>


<span data-ttu-id="baf22-104">명령줄을 사용 하 여 새 응용 프로그램의 순서를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="baf22-105">명령줄을 사용 하면 많은 수의 가상 응용 프로그램을 만들어야 하거나, 반복적으로 시퀀싱 된 응용 프로그램을 만들어야 할 때 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="baf22-106">중요</span><span class="sxs-lookup"><span data-stu-id="baf22-106">Important</span></span>**  
<span data-ttu-id="baf22-107">명령줄 시퀀싱을 사용 하면 기본 시퀀싱만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="baf22-108">시퀀싱 하는 응용 프로그램의 기본 설치 설정을 변경 해야 하는 경우 수동으로 가상 응용 프로그램을 수정 하거나 Application Virtualization (App-v) Sequencer를 사용 하 여 가상 응용 프로그램을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="baf22-109">App-v 시퀀서를 사용 하 여 가상 응용 프로그램을 업데이트 하는 방법에 대 한 자세한 내용은 [기존 가상 응용 프로그램을 업그레이드 하는 방법을](how-to-upgrade-an-existing-virtual-application.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="baf22-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="baf22-110">명령줄을 사용 하 여 가상 응용 프로그램을 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="baf22-111">명령줄을 사용 하 여 응용 프로그램을 시퀀싱 하려면</span><span class="sxs-lookup"><span data-stu-id="baf22-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="baf22-112">App-v Sequencer를 실행 하는 컴퓨터에서 **시작**, **실행**을 선택 하 고 **cmd**를 입력 하 여 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="baf22-113">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-113">Click **OK**.</span></span>

2.  <span data-ttu-id="baf22-114">명령 프롬프트를 사용 하 여 App-v Sequencer가 설치 되어 있는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="baf22-115">예를 들어 명령 프롬프트에서 다음을 입력할 수 있습니다. **cd C:\\program files Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="baf22-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="baf22-116">명령 프롬프트에서 다음 명령을 입력 하 고 따옴표 안에 있는 텍스트를 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="baf22-117">참고</span><span class="sxs-lookup"><span data-stu-id="baf22-117">Note</span></span>**  
    <span data-ttu-id="baf22-118">시퀀싱 하는 응용 프로그램의 복잡도에 따라 명령줄을 사용 하 여 추가 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="baf22-119">App-v 시퀀서와 함께 사용할 수 있는 전체 매개 변수 목록은 [Sequencer 명령줄 매개 변수](sequencer-command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="baf22-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="baf22-120">Enter **키를**누릅니다.</span><span class="sxs-lookup"><span data-stu-id="baf22-120">Press **Enter**.</span></span>

## <span data-ttu-id="baf22-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="baf22-121">Related topics</span></span>


[<span data-ttu-id="baf22-122">앱-V 시퀀서를 사용 하 여 가상 응용 프로그램을 만들거나 업그레이드 하는 방법</span><span class="sxs-lookup"><span data-stu-id="baf22-122">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="baf22-123">Sequencer 명령줄 오류 코드</span><span class="sxs-lookup"><span data-stu-id="baf22-123">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="baf22-124">Sequencer 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="baf22-124">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









