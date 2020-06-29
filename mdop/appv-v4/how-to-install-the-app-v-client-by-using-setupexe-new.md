---
title: Setup.exe를 사용하여 App-V Client를 설치하는 방법
description: Setup.exe를 사용하여 App-V Client를 설치하는 방법
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817338"
---
# <span data-ttu-id="4bb78-103">Setup.exe를 사용하여 App-V Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="4bb78-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="4bb78-104">이 항목에서는 setup.exe 프로그램을 사용 하 여 앱 V 클라이언트를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="4bb78-105">setup.exe 프로그램을 사용 하 여 App-v 클라이언트를 설치 하는 경우 설치 관리자는 필요한 필수 구성 요소 소프트웨어를 확인 하 고 클라이언트를 설치 하기 전에 자동으로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="4bb78-106">Setup.exe를 사용 하 여 응용 프로그램 가상화 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="4bb78-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="4bb78-107">컴퓨터에 대 한 관리자 권한이 있는 계정으로 로그온 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="4bb78-108">명령 프롬프트 창을 열고 설치 파일이 들어 있는 폴더로 디렉터리를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="4bb78-109">App-v 클라이언트의 버전 4.6 또는 이후 버전을 설치할 때 컴퓨터의 운영 체제 32 비트 또는 64 비트에 대 한 올바른 설치 관리자를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="4bb78-110">설치에 실패 하 고 잘못 된 설치 관리자를 사용 하는 경우 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="4bb78-111">명령 프롬프트에 설치 명령 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="4bb78-112">또는 명령 파일을 만들어 명령 프롬프트에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="4bb78-113">VBScript 또는 Windows PowerShell 같은 스크립트 언어를 사용 하 여 명령을 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="4bb78-114">다음 명령줄 예제에서는 여러 개의 선택적 매개 변수를 사용 하 여 setup.exe를 사용할 수 있는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="4bb78-115">이러한 매개 변수에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4bb78-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="4bb78-116">"setup.exe"/s/v "/qn SWICACHESIZE = \\" 10240 \\ "SWIPUBSVRDISPLAY = \\" 프로덕션 System\\ "SWIPUBSVRTYPE = \\" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \\ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \\" D:\\AppVirt\\Global\\ "SWIUSERDATA = \" "^% LOCALAPPDATA = \\" ^ Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""</span><span class="sxs-lookup"><span data-stu-id="4bb78-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="4bb78-117">중요</span><span class="sxs-lookup"><span data-stu-id="4bb78-117">Important</span></span>**  
    -   <span data-ttu-id="4bb78-118">"**/V**" 섹션에 표시 되는 인용 부호는 특수 문자로 처리 하 고 앞에 ""를 입력 해야 합니다 **\\** .</span><span class="sxs-lookup"><span data-stu-id="4bb78-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="4bb78-119">큰따옴표는 값에 공백이 포함 된 경우에만 필요 합니다. 그러나 일관성을 위해 이전 예제의 모든 인스턴스가 인용 부호로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="4bb78-120">" **%** **% HomeDrive%**"의 "" 문자는 "" 이스케이프 문자 앞에와 야 합니다 **^** .</span><span class="sxs-lookup"><span data-stu-id="4bb78-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="4bb78-121">그렇지 않으면 Windows 명령 셸에서는 설치를 수행 하는 사용자의 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="4bb78-122">자동 설치를 위해 **InstallShield** 스위치 **/s** 및 **/qn** 이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="4bb78-123">**/Qn** 스위치는 **/v** 스위치 뒤에 공백이 없는 인용 문자로 구분 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="4bb78-124">**SWIGLOBALDATA** 값에 지정 된 폴더가 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="4bb78-125">설치가 완료 되 면 Microsoft 업데이트 검사를 실행 하 여 최신 업데이트가 설치 되어 있는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4bb78-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="4bb78-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4bb78-126">Related topics</span></span>


[<span data-ttu-id="4bb78-127">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="4bb78-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





