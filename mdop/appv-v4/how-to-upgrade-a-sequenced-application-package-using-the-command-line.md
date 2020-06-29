---
title: 명령줄을 사용하여 시퀀싱된 응용 프로그램 패키지를 업그레이드하는 방법
description: 명령줄을 사용하여 시퀀싱된 응용 프로그램 패키지를 업그레이드하는 방법
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816488"
---
# <span data-ttu-id="9a982-103">명령줄을 사용하여 시퀀싱된 응용 프로그램 패키지를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="9a982-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="9a982-104">명령줄을 사용 하 여 가상 응용 프로그램을 업그레이드 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="9a982-105">명령줄을 사용 하 여 기존 가상 응용 프로그램 패키지를 업그레이드 하면 원본 버전의 sft 파일이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="9a982-106">명령줄을 사용 하 여 패키지를 업그레이드 하기 전에 연결 된 sft 파일을 백업 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="9a982-107">가상 응용 프로그램을 업그레이드 하려면</span><span class="sxs-lookup"><span data-stu-id="9a982-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="9a982-108">Application Virtualization (App-v) Sequencer를 실행 하는 컴퓨터에서 명령 프롬프트를 열려면 **시작**, **실행**을 선택 하 고 **cmd**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="9a982-109">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-109">Click **OK**.</span></span>

2.  <span data-ttu-id="9a982-110">명령 프롬프트에서 App-v Sequencer가 설치 되어 있는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="9a982-111">예를 들어 명령 프롬프트에서 다음을 입력할 수 있습니다. **cd C:\\program files Files\\Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="9a982-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="9a982-112">명령 프롬프트에서 다음 명령을 입력 하 고 따옴표 안에 있는 텍스트를 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="9a982-113">참고</span><span class="sxs-lookup"><span data-stu-id="9a982-113">Note</span></span>**  
    <span data-ttu-id="9a982-114">업그레이드 하는 응용 프로그램의 복잡도에 따라 명령줄을 사용 하 여 추가 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="9a982-115">App-v 시퀀서와 함께 사용할 수 있는 전체 매개 변수 목록은 명령줄 [매개 변수](command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a982-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



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
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="9a982-116">Enter **키를**누릅니다.</span><span class="sxs-lookup"><span data-stu-id="9a982-116">Press **Enter**.</span></span>

## <span data-ttu-id="9a982-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9a982-117">Related topics</span></span>


[<span data-ttu-id="9a982-118">명령줄을 사용하여 가상 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="9a982-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









