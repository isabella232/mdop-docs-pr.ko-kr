---
title: 기본 응용 프로그램을 설치 및 구성하는 방법
description: 기본 응용 프로그램을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817368"
---
# <span data-ttu-id="b1b07-103">기본 응용 프로그램을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="b1b07-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="b1b07-104">기본 응용 프로그램은 설치의 일부로 제공 되며 설치 하는 동안 Microsoft Application Virtualization (App-v) 관리 서버에 자동으로 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="b1b07-105">관리 서버가 올바르게 설치 및 구성 되었는지 확인 하는 데 사용 되지만 사용자가 액세스할 수 있도록 Microsoft Application Virtualization (App-v) 클라이언트에 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="b1b07-106">다음 절차를 사용 하 여 기본 응용 프로그램을 게시 하 고 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="b1b07-107">기본 응용 프로그램을 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="b1b07-107">To publish the default application</span></span>**

1.  <span data-ttu-id="b1b07-108">설치 중에 지정 된 App-v 관리자 그룹의 구성원 인 계정을 사용 하 여 App-v 관리 서버에 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="b1b07-109">App-v 관리 서버에서 **시작**, **관리 도구**, **응용 프로그램 가상화 관리 콘솔**을 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="b1b07-110">App-v 관리 콘솔에서 **작업**을 클릭 한 다음 **Application Virtualization System에 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="b1b07-111">**연결 구성** 페이지에서 **보안 연결 사용** 확인란의 선택을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="b1b07-112">**웹 서비스 호스트 이름** 상자에 App-v 관리 서버의 FQDN (정규화 된 도메인 이름)을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="b1b07-113">**참고**  관리 서버에 설치 되어 있는 경우 웹 서비스 호스트 이름에 **localhost** 를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="b1b07-114">App-v 관리 콘솔에서 **서버** 노드를 마우스 오른쪽 단추로 클릭 하 고 **시스템 옵션**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="b1b07-115">**일반** 탭의 **기본 콘텐츠 경로** 상자에 설치 하는 동안 서버에서 만든 콘텐츠 폴더의 UNC (범용 명명 규칙) 경로를 입력 합니다. 예를 들어 \\ Content (\ \ \ &lt; Server Name)를 &gt; 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="b1b07-116">**중요**  클라이언트가 이름을 올바르게 확인할 수 있도록 서버 이름에 대 한 FQDN을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="b1b07-117">앱-V 관리 콘솔의 탐색 창에서 **서버** 노드를 확장 한 다음 **응용 프로그램**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="b1b07-118">항목 창에서 **기본 응용 프로그램**을 클릭 한 다음 **작업** 창에서 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="b1b07-119">**속성** 대화 상자에서 **OSD 경로** 상자 옆에 있는 **찾아보기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="b1b07-120">**열기** 대화 상자에서 설치 하는 동안 서버에서 만든 콘텐츠 폴더의 UNC 경로를 입력 합니다. 예를 들어 \\/\ \ &lt; 서버 이름 \ \의 &gt; 콘텐츠를 입력 하 고 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="b1b07-121">실제 서버 이름을 사용 해야 하며이 위치에서 **localhost** 를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="b1b07-122">**중요**  **OSD 경로** 상자와 **아이콘 경로** 상자의 값이 모두 UNC 형식 (예: \\ \ \ &lt; Server Name &gt; \\Content\\defaultapp.ico) 인지 확인 하 고 서버를 설치할 때 만든 콘텐츠 폴더를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="b1b07-123">**Localhost** 또는 c:\\program files Files\\..와 같은 드라이브 문자를 포함 하는 파일 경로를 사용 하지 마세요. \\.. 콘텐트가.</span><span class="sxs-lookup"><span data-stu-id="b1b07-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="b1b07-124">DefaultApp .osd 파일을 선택 하 고 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="b1b07-125">앞의 단계를 반복 하 여 아이콘 경로를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="b1b07-126">**액세스 권한** 탭을 클릭 하 고 앱-V 사용자 그룹에 게 응용 프로그램에 대 한 액세스 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="b1b07-127">**바로 가기** 탭을 클릭 한 다음 **사용자의 바탕 화면에 게시를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="b1b07-128">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-128">Click **OK**.</span></span>

16. <span data-ttu-id="b1b07-129">Windows 탐색기를 열고 콘텐츠 디렉터리를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="b1b07-130">DefaultApp 파일을 두 번 클릭 하 고 메모장에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="b1b07-131">**HREF** 태그가 포함 된 줄을 찾아 다음 코드로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="b1b07-132">또는 RTSPS를 사용 하는 경우:</span><span class="sxs-lookup"><span data-stu-id="b1b07-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="b1b07-133">DefaultApp .osd 파일을 닫고 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="b1b07-134">기본 응용 프로그램을 스트리밍하려면</span><span class="sxs-lookup"><span data-stu-id="b1b07-134">To stream the default application</span></span>**

1.  <span data-ttu-id="b1b07-135">App-v 클라이언트가 설치 된 컴퓨터에서 서버를 설치 하는 동안 지정 된 Application Virtualization Users 그룹의 구성원 인 사용자로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="b1b07-136">바탕 화면에 **기본 응용 프로그램 가상화 응용 프로그램** 바로 가기가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="b1b07-137">바로 가기를 두 번 클릭 하 여 응용 프로그램을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="b1b07-138">Windows 알림 영역 위에 표시 되는 상태 표시줄에는 응용 프로그램이 시작 됨을 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="b1b07-139">응용 프로그램이 성공적으로 시작 되 면 기본 응용 프로그램의 제목 화면이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="b1b07-140">**확인** 을 클릭 하 여 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="b1b07-141">이제 App-v 시스템이 올바르게 실행 되 고 있음을 확인 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b07-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="b1b07-142">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b1b07-142">Related topics</span></span>


[<span data-ttu-id="b1b07-143">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="b1b07-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





