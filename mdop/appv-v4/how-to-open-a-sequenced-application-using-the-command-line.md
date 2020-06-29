---
title: 명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법
description: 명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816918"
---
# <span data-ttu-id="3b2de-103">명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법</span><span class="sxs-lookup"><span data-stu-id="3b2de-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="3b2de-104">명령줄을 사용 하 여 가상 응용 프로그램 패키지를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="3b2de-105">관리자 권한으로 **cmd** 프롬프트를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="3b2de-106">명령줄을 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 열려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="3b2de-107">명령줄을 사용 하 여 시퀀싱 된 응용 프로그램을 열려면</span><span class="sxs-lookup"><span data-stu-id="3b2de-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="3b2de-108">명령 프롬프트를 열려면 **시작**을 클릭 하 고 **실행**을 선택 하 고 **Cmd**를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="3b2de-109">명령 프롬프트에서 **cd\\** 를 입력 하 고 Sequencer가 설치 된 디렉터리의 경로를 지정한 다음 enter 키를 누릅니다 **.**</span><span class="sxs-lookup"><span data-stu-id="3b2de-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="3b2de-110">명령 프롬프트에서 다음 명령을 입력 하 고 기울임꼴로 표시 된 텍스트를 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="3b2de-111">SFTSequencer/OPEN:*"열려고 하는 sprj 파일을 지정 합니다."*</span><span class="sxs-lookup"><span data-stu-id="3b2de-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="3b2de-112">Enter **키를**누릅니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="3b2de-113">다음 선택적 매개 변수를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="3b2de-114">명령 프롬프트에서 다음 명령을 입력 하 고 기울임꼴로 표시 된 텍스트를 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="3b2de-115">/PACKAGENAME: "*패키지 이름을 지정 합니다."*</span><span class="sxs-lookup"><span data-stu-id="3b2de-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="3b2de-116">/MSI-연결 된 Microsoft Windows Installer를 생성 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="3b2de-117">/COMPRESS – 패키지의 압축 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="3b2de-118">기본적으로 패키지는 압축 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="3b2de-119">Enter **키를**누릅니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-119">Press **Enter**.</span></span>

    <span data-ttu-id="3b2de-120">**참고**  설치 관리자 또는 Windows Installer 패키지에 그래픽 사용자 인터페이스가 있으면 명령줄 매개 변수를 지정한 후에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b2de-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="3b2de-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3b2de-121">Related topics</span></span>


[<span data-ttu-id="3b2de-122">명령줄을 사용하여 가상 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="3b2de-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





