---
title: 패키지를 추가하는 방법
description: 패키지를 추가하는 방법
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821398"
---
# <span data-ttu-id="dcacb-103">패키지를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="dcacb-103">How to Add a Package</span></span>


<span data-ttu-id="dcacb-104">다음과 같은 방법으로 응용 프로그램 가상화 서버 관리 콘솔에서 패키지를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="dcacb-105">프로세스에서 자동으로 패키지를 만드는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="dcacb-106">수동으로 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-106">Add a package manually.</span></span>

<span data-ttu-id="dcacb-107">수동으로 추가 하는 대신 응용 프로그램을 가져오는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="dcacb-108">응용 프로그램을 가져오는 방법에 대 한 자세한 내용은 [응용 프로그램을 가져오는 방법을](how-to-import-an-applicationserver.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dcacb-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="dcacb-109">패키지를 수동으로 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="dcacb-109">To add a package manually</span></span>**

1.  <span data-ttu-id="dcacb-110">Application Virtualization Server Management Console의 왼쪽 창에서 **패키지** 노드를 마우스 오른쪽 단추로 클릭 하 고 **새 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="dcacb-111">**새 패키지** 대화 상자에서 **패키지 이름** 필드에 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="dcacb-112">**패키지 파일의 전체 경로** 필드에서 경로 이름을 찾아보거나 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="dcacb-113">SFT 파일 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-113">This must be an SFT file.</span></span>

    <span data-ttu-id="dcacb-114">**참고**  SFT 파일로 이동 하는 경우 C:\\program files Files\\User\ _Apps \\Virtual\ _App \ _Server \\content와 같은 로컬 경로를 서버의 고정 호스트 이름 또는 IP 주소로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="dcacb-115">변수 *% SFT \ _SOFTGRIDSERVER%* 를 사용 하는 경우 클라이언트 단위 컴퓨터 구성이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="dcacb-116">가상 응용 프로그램 서버를 참조 하는 대화 상자에서 서버의 정적 호스트 이름 또는 IP 주소와 같이 사용자가 액세스할 수 있는 네트워크 위치를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="dcacb-117">응용 프로그램의 OSD (개방형 소프트웨어 설명자) 파일이 서버의 고정 호스트 이름 또는 IP 주소를 사용 하 여 개체 틀 변수 *% SFT \ _SOFTGRIDSERER%* 를 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="dcacb-118">자리 표시자 변수를 남겨둘 경우 해당 서버에 액세스할 각 클라이언트 컴퓨터에서이 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="dcacb-119">SFT \ _SOFTGRIDSERVER의 각 컴퓨터에서 사용자 또는 시스템 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="dcacb-120">변수 값은 서버의 정적 호스트 이름 또는 IP 주소 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="dcacb-121">변수를 설정 하는 경우 클라이언트 세션을 종료 하 고 Microsoft Windows에 로그 아웃 한 다음 세션을 실행 중이 고 변수가 설정 된 각 컴퓨터에서 세션을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="dcacb-122">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-122">Click **Next**.</span></span>

5.  <span data-ttu-id="dcacb-123">**요약** 대화 상자에 파일 위치가 표시 되며 아직 파일을 복사 하지 않은 경우 해당 위치에 복사할 것인지 묻는 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="dcacb-124">정보를 확인 한 후 **마침을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="dcacb-125">**참고**  원격 서버의 응용 프로그램을 관리 하는 경우 다음 대화 상자에서 서버의 콘텐츠 루트에 상대적인 파일 경로만 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcacb-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="dcacb-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dcacb-126">Related topics</span></span>


[<span data-ttu-id="dcacb-127">응용 프로그램을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="dcacb-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="dcacb-128">Server Management Console에서 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="dcacb-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





