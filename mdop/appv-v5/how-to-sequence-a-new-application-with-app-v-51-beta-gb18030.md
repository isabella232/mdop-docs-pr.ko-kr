---
title: App-V 5.1을 사용하여 새 응용 프로그램을 시퀀싱하는 방법
description: App-V 5.1을 사용하여 새 응용 프로그램을 시퀀싱하는 방법
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813716"
---
# <span data-ttu-id="8a090-103">App-V 5.1을 사용하여 새 응용 프로그램을 시퀀싱하는 방법</span><span class="sxs-lookup"><span data-stu-id="8a090-103">How to Sequence a New Application with App-V 5.1</span></span>


**<span data-ttu-id="8a090-104">시퀀싱을 시작 하기 전에 검토 하거나 수행 하려면</span><span class="sxs-lookup"><span data-stu-id="8a090-104">To review or do before you start sequencing</span></span>**

1.  <span data-ttu-id="8a090-105">만들려는 가상화 된 응용 프로그램 패키지의 유형을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-105">Determine the type of virtualized application package you want to create:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="8a090-106">응용 프로그램 종류</span><span class="sxs-lookup"><span data-stu-id="8a090-106">Application type</span></span></th>
    <th align="left"><span data-ttu-id="8a090-107">설명</span><span class="sxs-lookup"><span data-stu-id="8a090-107">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8a090-108">Standard</span><span class="sxs-lookup"><span data-stu-id="8a090-108">Standard</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8a090-109">응용 프로그램 또는 응용 프로그램 집합을 포함 하는 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-109">Creates a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="8a090-110">대부분의 응용 프로그램 유형에 기본 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-110">This is the preferred option for most application types.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8a090-111">추가 기능 또는 플러그 인</span><span class="sxs-lookup"><span data-stu-id="8a090-111">Add-on or plug-in</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8a090-112">표준 응용 프로그램의 기능 (예: Microsoft Excel 용 플러그 인)을 확장 하는 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-112">Creates a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="8a090-113">또한 기본적으로 설치 된 응용 프로그램 또는 연결 그룹을 사용 하 여 연결 된 다른 패키지에 대 한 플러그 인을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-113">Additionally, you can use plug-ins for natively installed applications, or for another package that is linked by using connection groups.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8a090-114">관점</span><span class="sxs-lookup"><span data-stu-id="8a090-114">Middleware</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8a090-115">Java와 같은 표준 응용 프로그램에 필요한 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-115">Creates a package that is required by a standard application, for example, Java.</span></span> <span data-ttu-id="8a090-116">미들웨어 패키지는 연결 그룹을 사용 하 여 다른 패키지에 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-116">Middleware packages are used for linking to other packages by using connection groups.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="8a090-117">필요한 모든 설치 파일을 sequencer를 실행 하는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-117">Copy all required installation files to the computer that is running the sequencer.</span></span>

3.  <span data-ttu-id="8a090-118">응용 프로그램을 시퀀싱 하기 전에 가상 환경의 백업 이미지를 만든 다음 응용 프로그램 시퀀싱을 완료 한 후에 해당 이미지로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-118">Make a backup image of your virtual environment before sequencing an application, and then revert to that image each time after you finish sequencing an application.</span></span>

4.  <span data-ttu-id="8a090-119">다음 항목을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-119">Review the following items:</span></span>

    -   <span data-ttu-id="8a090-120">응용 프로그램 설치 관리자가 새 또는 기존 파일 또는 디렉터리에 대 한 보안 액세스 권한을 변경 하는 경우 해당 변경 내용이 패키지에 캡처되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-120">If an application installer changes the security access to a new or existing file or directory, those changes are not captured in the package.</span></span>

    -   <span data-ttu-id="8a090-121">가상 패키지의 대상 볼륨에 대해 짧은 경로를 사용 하지 않도록 설정한 경우에는 만든 볼륨에 대해서도 패키지를 시퀀싱 해야 하며, 여전히 짧은 경로를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-121">If short paths have been disabled for the virtualized package’s target volume, you must also sequence the package to a volume that was created and still has short-paths disabled.</span></span> <span data-ttu-id="8a090-122">시스템 볼륨 일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-122">It cannot be the system volume.</span></span>

> [!NOTE]  
> <span data-ttu-id="8a090-123">App-v 5. x 시퀀서는 파일 이름이 "CO_ x"가 일치 하는 응용 프로그램을 시퀀싱 할 수 없습니다 &lt; &gt; . 여기서 x는 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-123">The App-V 5.x Sequencer cannot sequence applications with filenames matching "CO_&lt;x&gt;" where x is any numeral.</span></span> <span data-ttu-id="8a090-124">오류 0x8007139F이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-124">Error 0x8007139F will be generated.</span></span>

**<span data-ttu-id="8a090-125">새 표준 응용 프로그램을 시퀀싱 하려면</span><span class="sxs-lookup"><span data-stu-id="8a090-125">To sequence a new standard application</span></span>**

1.  <span data-ttu-id="8a090-126">Sequencer를 실행 하는 컴퓨터에서 **모든 프로그램**을 클릭 한 다음 **microsoft application virtualization**을 클릭 한 다음 **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-126">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="8a090-127">Sequencer에서 **새 가상 응용 프로그램 패키지 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-127">In the sequencer, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="8a090-128">**패키지 만들기 (기본값)** 를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-128">Select **Create Package (default)**, and then click **Next**.</span></span>

3.  <span data-ttu-id="8a090-129">**컴퓨터 준비** 페이지에서 패키지 만들기에 실패 하거나 패키지에 불필요 한 데이터가 포함 될 수 있는 문제를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-129">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="8a090-130">계속 하기 전에 모든 잠재적인 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-130">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="8a090-131">수정한 후 **새로 고침** 을 클릭 하 여 업데이트 된 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-131">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="8a090-132">발생할 수 있는 모든 문제를 해결 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-132">After you have resolved all potential issues, click **Next**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8a090-133">바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우에는 먼저 sequencer를 실행 하는 컴퓨터를 검사 하 여 불필요 하거나 악의적인 파일이 패키지에 추가 되지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-133">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. <span data-ttu-id="8a090-134">**응용 프로그램 형식** 페이지에서 **표준 응용 프로그램 (기본값)** 확인란을 클릭 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-134">On the **Type of Application** page, click the **Standard Application (default)** check box, and then click **Next**.</span></span>

5. <span data-ttu-id="8a090-135">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 응용 프로그램의 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-135">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="8a090-136">지정 된 응용 프로그램 설치 관리자가 기존 또는 새 파일 또는 디렉터리에 대 한 보안 액세스를 수정 하는 경우 연결 된 변경 내용이 패키지에 캡처되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-136">If the specified application installer modifies security access to a file or directory, existing or new, the associated changes will not be captured into the package.</span></span>



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. <span data-ttu-id="8a090-137">**패키지 이름** 페이지에서 패키지와 연결 되는 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-137">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="8a090-138">패키지에 추가 되는 응용 프로그램의 용도와 버전을 식별 하는 데 도움이 되는 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-138">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="8a090-139">패키지 이름이 App-v 5.0 관리 콘솔에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-139">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="8a090-140">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-140">Click **Next**.</span></span>

7. <span data-ttu-id="8a090-141">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자가 준비 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 응용 프로그램 설치를 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-141">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-142">항상 안전한 위치에 응용 프로그램을 설치 하 고 모니터링 하는 동안 sequencer를 실행 하는 컴퓨터에 다른 사용자가 로그온 되어 있지 않은지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-142">You should always install applications to a secure location and make sure no other users are logged on to the computer running the sequencer during monitoring.</span></span>



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. <span data-ttu-id="8a090-143">**설치** 페이지에서 sequencer가 가상화 된 응용 프로그램 패키지를 구성 하는 동안 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-143">On the **Installation** page, wait while the sequencer configures the virtualized application package.</span></span>

9. <span data-ttu-id="8a090-144">**소프트웨어 구성** 페이지에서 패키지에 포함 된 프로그램을 선택적으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-144">On the **Configure Software** page, optionally run the programs contained in the package.</span></span> <span data-ttu-id="8a090-145">이 단계에서는 대상 컴퓨터에서 패키지를 배포 하 고 실행 하기 전에 필요한 라이선스 또는 구성 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-145">This step allows you to complete any necessary license or configuration tasks before you deploy and run the package on target computers.</span></span> <span data-ttu-id="8a090-146">한 번에 모든 프로그램을 실행 하려면 하나 이상의 프로그램을 선택한 다음 **모두 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-146">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="8a090-147">특정 프로그램을 실행 하려면 프로그램 또는 프로그램을 선택한 다음, 선택 된 **실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-147">To run specific programs, select the program or programs, and then click **Run Selected**.</span></span> <span data-ttu-id="8a090-148">필요한 구성 작업을 완료 한 다음 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-148">Complete the required configuration tasks and then close the applications.</span></span> <span data-ttu-id="8a090-149">모든 프로그램이 실행 될 때까지 몇 분 정도 기다려야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-149">You may need to wait several minutes for all programs to run.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="8a090-150">목록에서 사용할 수 없는 모든 응용 프로그램에 대해 처음 사용 작업을 실행 하려면 해당 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-150">To run first-use tasks for any application that is not available in the list, open the application.</span></span> <span data-ttu-id="8a090-151">이 단계에서는 관련 정보가 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-151">The associated information will be captured during this step.</span></span>



~~~
Click **Next**.
~~~

10. <span data-ttu-id="8a090-152">**설치 보고서** 페이지에서 방금 시퀀싱 한 가상화 된 응용 프로그램 패키지에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-152">On the **Installation Report** page, you can review information about the virtualized application package you have just sequenced.</span></span> <span data-ttu-id="8a090-153">**추가 정보**에서 이벤트를 두 번 클릭 하 여 자세한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-153">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="8a090-154">계속 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-154">To proceed, click **Next**.</span></span>

11. <span data-ttu-id="8a090-155">**사용자 지정** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-155">The **Customize** page is displayed.</span></span> <span data-ttu-id="8a090-156">가상 응용 프로그램의 설치 및 구성을 완료 한 경우 **지금 중지** 를 선택 하 고이 절차의 14 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-156">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 14 of this procedure.</span></span> <span data-ttu-id="8a090-157">다음 사용자 지정 중 하나를 수행 하려면 **사용자 지정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-157">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="8a090-158">스트리밍을 위해 가상 패키지를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-158">Prepare the virtual package for streaming.</span></span> <span data-ttu-id="8a090-159">스트리밍을 통해 대상 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 때 환경이 개선 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-159">Streaming improves the experience when the virtual application package is run on target computers.</span></span>

    -   <span data-ttu-id="8a090-160">이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-160">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="8a090-161">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-161">Click **Next**.</span></span>

12. <span data-ttu-id="8a090-162">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-162">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="8a090-163">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-163">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="8a090-164">모든 응용 프로그램이 실행 된 후에 각 응용 프로그램을 닫고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-164">After all applications have run, close each of the applications, and then click **Next**.</span></span>

   > [!NOTE]  
   > <span data-ttu-id="8a090-165">이 단계 중에 응용 프로그램을 열지 않으면 기본 스트리밍 방법은 주문형 스트리밍 전달입니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-165">If you do not open any applications during this step, the default streaming method is on-demand streaming delivery.</span></span> <span data-ttu-id="8a090-166">즉, 응용 프로그램을 열 수 있을 때까지 비트 단위로 다운로드 되 고 백그라운드 로드 구성 방법에 따라 나머지 응용 프로그램이 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-166">This means applications will be downloaded bit by bit until it can be opened, and then depending on how the background loading is configured, will load the rest of the application.</span></span>



13. <span data-ttu-id="8a090-167">**대상 OS** 페이지에서이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-167">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="8a090-168">사용자 환경에서 지원 되는 모든 운영 체제에서이 패키지를 실행 하도록 허용 하려면 **모든 운영 체제에서이 패키지를 실행 하도록 허용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-168">To allow all supported operating systems in your environment to run this package, select **Allow this package to run on any operating system**.</span></span> <span data-ttu-id="8a090-169">특정 운영 체제 에서만 실행 되도록이 패키지를 구성 하려면 **다음 운영 체제 에서만이 패키지를 실행 하도록 허용** 을 선택 하 고이 패키지를 실행할 수 있는 운영 체제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-169">To configure this package to run only on specific operating systems, select **Allow this package to run only on the following operating systems** and select the operating systems that can run this package.</span></span> <span data-ttu-id="8a090-170">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-170">Click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-171">여기에서 지정 하는 운영 체제를 시퀀싱 하는 응용 프로그램에서 지원 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-171">Make sure that the operating systems you specify here are supported by the application you are sequencing.</span></span>



14. <span data-ttu-id="8a090-172">**패키지 만들기** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-172">The **Create Package** page is displayed.</span></span> <span data-ttu-id="8a090-173">패키지를 저장 하지 않고 수정 하려면 패키지 **편집기를 사용 하 여 저장 하지 않고 패키지를 계속 수정**합니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-173">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="8a090-174">이 옵션은 패키지를 저장 하기 전에 수정할 수 있도록 sequencer 콘솔에서 패키지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-174">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="8a090-175">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-175">Click **Next**.</span></span>

   <span data-ttu-id="8a090-176">패키지를 즉시 저장 하려면 **지금 패키지 저장** (기본값)을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-176">To save the package immediately, select **Save the package now** (default).</span></span> <span data-ttu-id="8a090-177">패키지와 연결할 선택적 **메모** 를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-177">Add optional **Comments** to be associated with the package.</span></span> <span data-ttu-id="8a090-178">메모는 프로그램 버전 및 패키지에 대 한 기타 정보를 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-178">Comments are useful for identifying the program version and other information about the package.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-179">시스템에서 **메모** 및 **설명**에 인쇄할 수 없는 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-179">The system does not support non-printable characters in **Comments** and **Descriptions**.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. <span data-ttu-id="8a090-180">**완료** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-180">The **Completion** page is displayed.</span></span> <span data-ttu-id="8a090-181">필요에 따라 **가상 응용 프로그램 패키지 보고서** 창에서 정보를 검토 한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-181">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="8a090-182">이 정보는 패키지를 만든 디렉터리에 있는 **Report.xml** 파일 에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-182">This information is also available in the **Report.xml** file that is located in the directory where the package was created.</span></span>

   <span data-ttu-id="8a090-183">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-183">The package is now available in the sequencer.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-184">가상 응용 프로그램 패키지를 성공적으로 만들었으면 sequencer를 실행 하는 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-184">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



**<span data-ttu-id="8a090-185">추가 기능 또는 플러그 인 응용 프로그램의 순서를 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="8a090-185">To sequence an add-on or plug-in application</span></span>**

1. > [!NOTE]  
   > <span data-ttu-id="8a090-186">다음 절차를 수행 하기 전에 sequencer를 실행 하는 컴퓨터에 부모 응용 프로그램을 로컬로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-186">Before performing the following procedure, install the parent application locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="8a090-187">또는 부모 응용 프로그램이 가상화 된 경우 추가 기능 또는 플러그 인 워크플로의 단계에 따라 컴퓨터에서 부모 응용 프로그램의 압축을 풀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-187">Or if you have the parent application virtualized, you can follow the steps in the add-on or plug-in workflow to unpack the parent application on the computer.</span></span>
   >
   > <span data-ttu-id="8a090-188">예를 들어 Microsoft Excel 용 플러그 인을 시퀀싱 하는 경우 시퀀서를 실행 하는 컴퓨터에 Microsoft Excel을 로컬로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-188">For example, if you are sequencing a plug-in for Microsoft Excel, install Microsoft Excel locally on the computer that is running the sequencer.</span></span> <span data-ttu-id="8a090-189">또한 대상 컴퓨터에 응용 프로그램이 설치 되어 있는 디렉터리에 부모 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-189">Also install the parent application in the same directory where the application is installed on target computers.</span></span> <span data-ttu-id="8a090-190">플러그 인 또는 추가 기능을 기존 가상 응용 프로그램 패키지와 함께 사용 하려는 경우 부모 가상 응용 프로그램 패키지를 만들 때 사용한 것과 동일한 가상 응용 프로그램 드라이브에 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-190">If the plug-in or add-on is going to be used with an existing virtual application package, install the application on the same virtual application drive that was used when you created the parent virtual application package.</span></span>



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="8a090-191">\*<strong><em>Sequencer에서 \* </em> 새 가상 응용 프로그램 패키지 만들기를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-191">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="8a090-192">**패키지 만들기 (기본값)** 를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-192">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="8a090-193">**컴퓨터 준비** 페이지에서 패키지 만들기에 실패 하거나 패키지에 불필요 한 데이터가 포함 될 수 있는 문제를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-193">On the **Prepare Computer** page, review the issues that might cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="8a090-194">계속 하기 전에 모든 잠재적인 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-194">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="8a090-195">수정한 후 **새로 고침** 을 클릭 하 여 업데이트 된 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-195">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="8a090-196">발생할 수 있는 모든 문제를 해결 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-196">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-197">바이러스 검색 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우에는 먼저 sequencer를 실행 하는 컴퓨터를 검사 하 여 불필요 하거나 악의적인 파일이 패키지에 추가 되지 않도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-197">If you are required to disable virus scanning software, you should first scan the computer that runs the sequencer in order to ensure that no unwanted or malicious files could be added to the package.</span></span>



4. <span data-ttu-id="8a090-198">**응용 프로그램 종류** 페이지에서 **추가 기능 또는 플러그**인을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-198">On the **Type of Application** page, select **Add-on or Plug-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="8a090-199">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 추가 기능 또는 플러그 인의 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-199">On the **Select Installer** page, click **Browse** and specify the installation file for the add-on or plug-in.</span></span> <span data-ttu-id="8a090-200">추가 기능 또는 플러그 인에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행 하려는 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-200">If the add-on or plug-in does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="8a090-201">**기본 설치** 페이지에서 sequencer를 실행 하는 컴퓨터에 기본 응용 프로그램이 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-201">On the **Install Primary** page, ensure that the primary application is installed on the computer that runs the sequencer.</span></span> <span data-ttu-id="8a090-202">또는 시퀀서를 실행 하는 컴퓨터에 로컬로 저장 된 기존 패키지를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-202">Alternatively, you can expand an existing package that has been saved locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="8a090-203">이렇게 하려면 **패키지 확장**을 클릭 한 다음 패키지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-203">To do this, click **Expand Package**, and then select the package.</span></span> <span data-ttu-id="8a090-204">상위 프로그램을 확장 하거나 설치한 후 **기본 상위 프로그램을 설치**합니다를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-204">After you have expanded or installed the parent program, select **I have installed the primary parent program**.</span></span>

   <span data-ttu-id="8a090-205">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-205">Click **Next**.</span></span>

7. <span data-ttu-id="8a090-206">**패키지 이름** 페이지에서 패키지와 연결 되는 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-206">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="8a090-207">패키지에 추가 되는 응용 프로그램의 용도와 버전을 식별 하는 데 도움이 되는 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-207">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="8a090-208">패키지 이름이 App-v 5.0 관리 콘솔에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-208">The package name will be displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="8a090-209">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-209">Click **Next**.</span></span>

8. <span data-ttu-id="8a090-210">**설치** 페이지에서 sequencer 및 응용 프로그램 설치 관리자를 사용할 준비가 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 플러그 인 또는 추가 기능 응용 프로그램을 설치 하도록 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-210">On the **Installation** page, when the sequencer and application installer are ready you can proceed to install the plug-in or add-in application so the sequencer can monitor the installation process.</span></span> <span data-ttu-id="8a090-211">응용 프로그램의 설치 프로세스를 사용 하 여 설치를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-211">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="8a090-212">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행** 을 클릭 하 고 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-212">If additional installation files must be run as part of the installation, click **Run** and locate and run the additional installation files.</span></span> <span data-ttu-id="8a090-213">설치가 완료 되 면 **설치 완료**를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-213">When you are finished with the installation, select **I am finished installing**, and then click **Next**.</span></span>

9. <span data-ttu-id="8a090-214">**설치 보고서** 페이지에서 방금 시퀀싱 한 가상 응용 프로그램 패키지에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-214">On the **Installation Report** page, you can review information about the virtual application package that you just sequenced.</span></span> <span data-ttu-id="8a090-215">**추가 정보**에 표시 되는 정보에 대 한 자세한 설명을 보려면 이벤트를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-215">For a more detailed explanation about the information displayed in **Additional Information**, double-click the event.</span></span> <span data-ttu-id="8a090-216">정보를 검토 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-216">After you have reviewed the information, click **Next**.</span></span>

10. <span data-ttu-id="8a090-217">**사용자 지정** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-217">The **Customize** page is displayed.</span></span> <span data-ttu-id="8a090-218">가상 응용 프로그램의 설치 및 구성을 완료 한 경우 **지금 중지** 를 선택 하 고이 절차의 12 단계로 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-218">If you are finished installing and configuring the virtual application, select **Stop now** and skip to step 12 of this procedure.</span></span> <span data-ttu-id="8a090-219">다음 사용자 지정 중 하나를 수행 하려면 **사용자 지정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-219">To perform either of the following customizations, select **Customize**.</span></span>

    -   <span data-ttu-id="8a090-220">느리거나 불안정 한 네트워크에서 패키지가 실행 되는 방식을 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-220">Optimize how the package will run across a slow or unreliable network.</span></span>

    -   <span data-ttu-id="8a090-221">이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-221">Specify the operating systems that can run this package.</span></span>

    <span data-ttu-id="8a090-222">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-222">Click **Next**.</span></span>

11. <span data-ttu-id="8a090-223">**스트리밍** 페이지에서 각 프로그램을 실행 하 여 대상 컴퓨터에서 최적화 하 고 더 효율적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-223">On the **Streaming** page, run each program so that it can be optimized and run more efficiently on target computers.</span></span> <span data-ttu-id="8a090-224">스트리밍는 가상 응용 프로그램 패키지가 대기 시간이 긴 네트워크의 대상 컴퓨터에서 실행 되는 경우 환경을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-224">Streaming improves the experience when the virtual application package is run on target computers on high-latency networks.</span></span> <span data-ttu-id="8a090-225">모든 응용 프로그램이 실행 되는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-225">It can take several minutes for all the applications to run.</span></span> <span data-ttu-id="8a090-226">모든 응용 프로그램을 실행 한 후에는 각각의 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-226">After all applications have run, close each of the applications.</span></span> <span data-ttu-id="8a090-227">또한 시작 하기 **위해 응용 프로그램을 다운로드 하도록 강제** 확인란을 선택 하 여 패키지를 열기 전에 완전히 다운로드 되도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-227">You can also configure the package to be required to be fully downloaded before opening by selecting the **Force applications to be downloaded** check-box.</span></span> <span data-ttu-id="8a090-228">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-228">Click **Next**.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="8a090-229">필요한 경우이 단계에서 응용 프로그램이 로드 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-229">If necessary, you can stop an application from loading during this step.</span></span> <span data-ttu-id="8a090-230">**응용 프로그램 실행** 대화 상자에서 **중지** 를 클릭 하 고 다음 확인란 중 하나를 선택 합니다. **모든 응용 프로그램을 중지** 하거나 **이 응용 프로그램을 중지**합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-230">In the **Application Launch** dialog box, click **Stop** and select one of the check boxes: **Stop all applications** or **Stop this application only**.</span></span>



12. <span data-ttu-id="8a090-231">**대상 OS** 페이지에서이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-231">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="8a090-232">사용자 환경에서 지원 되는 모든 운영 체제에서이 패키지를 실행 하도록 허용 하려면 **모든 운영 체제에서이 패키지를 실행 하도록 허용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-232">To allow all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="8a090-233">특정 운영 체제 에서만이 패키지를 실행 하도록 구성 하려면 **다음 운영 체제 에서만이 패키지를 실행 하도록 허용** 확인란을 선택한 다음이 패키지를 실행할 수 있는 운영 체제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-233">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box, and then select the operating systems that can run this package.</span></span> <span data-ttu-id="8a090-234">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-234">Click **Next**.</span></span>

13. <span data-ttu-id="8a090-235">**패키지 만들기** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-235">The **Create Package** page is displayed.</span></span> <span data-ttu-id="8a090-236">패키지를 저장 하지 않고 수정 하려면 패키지 **편집기를 사용 하 여 저장 하지 않고 패키지 계속 수정** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-236">To modify the package without saving it, select **Continue to modify package without saving using the package editor** check box.</span></span> <span data-ttu-id="8a090-237">이 옵션은 패키지를 저장 하기 전에 수정할 수 있도록 sequencer 콘솔에서 패키지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-237">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="8a090-238">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-238">Click **Next**.</span></span>

    <span data-ttu-id="8a090-239">패키지를 즉시 저장 하려면 **지금 패키지 저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-239">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="8a090-240">필요에 따라 패키지와 연결 되는 **설명을** 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-240">Optionally, add a **Description** that will be associated with the package.</span></span> <span data-ttu-id="8a090-241">설명은 패키지에 대 한 버전 및 기타 정보를 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-241">Descriptions are useful for identifying the version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8a090-242">시스템에서 메모 및 설명에 인쇄할 수 없는 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-242">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**<span data-ttu-id="8a090-243">미들웨어 응용 프로그램을 시퀀싱 하려면</span><span class="sxs-lookup"><span data-stu-id="8a090-243">To sequence a middleware application</span></span>**

1. <span data-ttu-id="8a090-244">Sequencer를 실행 하는 컴퓨터에서 **모든 프로그램**을 클릭 한 다음 **microsoft application virtualization**을 클릭 한 다음 **microsoft application virtualization sequencer**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-244">On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="8a090-245">\*<strong><em>Sequencer에서 \* </em> 새 가상 응용 프로그램 패키지 만들기를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-245">\*<strong><em>In the sequencer, click \*</em>Create a New Virtual Application Package</strong>.</span></span> <span data-ttu-id="8a090-246">**패키지 만들기 (기본값)** 를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-246">Select **Create Package (default)**, and then click **Next**.</span></span>

3. <span data-ttu-id="8a090-247">**컴퓨터 준비** 페이지에서 패키지 만들기에 실패 하거나 패키지에 불필요 한 데이터가 포함 될 수 있는 문제를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-247">On the **Prepare Computer** page, review the issues that could cause the package creation to fail or could cause the package to contain unnecessary data.</span></span> <span data-ttu-id="8a090-248">계속 하기 전에 모든 잠재적인 문제를 해결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-248">You should resolve all potential issues before you continue.</span></span> <span data-ttu-id="8a090-249">수정한 후 **새로 고침** 을 클릭 하 여 업데이트 된 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-249">After making any corrections, click **Refresh** to display the updated information.</span></span> <span data-ttu-id="8a090-250">발생할 수 있는 모든 문제를 해결 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-250">After you have resolved all potential issues, click **Next**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-251">바이러스 검사 소프트웨어를 사용 하지 않도록 설정 해야 하는 경우에는 먼저 App-v 5.0 Sequencer를 실행 하는 컴퓨터를 검사 하 여 불필요 하거나 악의적인 파일이 패키지에 추가 될 수 없도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-251">If you are required to disable virus scanning software, you should first scan the computer that runs the App-V 5.0 Sequencer in order to ensure that no unwanted or malicious files can be added to the package.</span></span>



4. <span data-ttu-id="8a090-252">**응용 프로그램 형식** 페이지에서 **미들웨어**를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-252">On the **Type of Application** page, select **Middleware**, and then click **Next**.</span></span>

5. <span data-ttu-id="8a090-253">**설치 관리자 선택** 페이지에서 **찾아보기를** 클릭 하 고 응용 프로그램의 설치 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-253">On the **Select Installer** page, click **Browse** and specify the installation file for the application.</span></span> <span data-ttu-id="8a090-254">응용 프로그램에 연결 된 설치 관리자 파일이 없고 모든 설치 단계를 수동으로 실행 하려는 경우 **이 옵션을 선택 하 여 사용자 지정 설치 수행** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-254">If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Select this option to perform a custom installation** check box, and then click **Next**.</span></span>

6. <span data-ttu-id="8a090-255">**패키지 이름** 페이지에서 패키지와 연결 되는 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-255">On the **Package Name** page, type a name that will be associated with the package.</span></span> <span data-ttu-id="8a090-256">패키지에 추가 되는 응용 프로그램의 용도와 버전을 식별 하는 데 도움이 되는 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-256">Use a name that helps identify the purpose and version of the application that will be added to the package.</span></span> <span data-ttu-id="8a090-257">패키지 이름이 App-v 5.0 관리 콘솔에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-257">The package name is displayed in the App-V 5.0 Management Console.</span></span>

   <span data-ttu-id="8a090-258">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-258">Click **Next**.</span></span>

7. <span data-ttu-id="8a090-259">**설치** 페이지에서 sequencer 및 미들웨어 응용 프로그램 설치 관리자가 준비 되 면 sequencer에서 설치 프로세스를 모니터링할 수 있도록 응용 프로그램 설치를 계속할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-259">On the **Installation** page, when the sequencer and middleware application installer are ready you can proceed to install the application so that the sequencer can monitor the installation process.</span></span> <span data-ttu-id="8a090-260">응용 프로그램의 설치 프로세스를 사용 하 여 설치를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-260">Use the application's installation process to perform the installation.</span></span> <span data-ttu-id="8a090-261">설치의 일부로 추가 설치 파일을 실행 해야 하는 경우 **실행**을 클릭 하 여 추가 설치 파일을 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-261">If additional installation files must be run as part of the installation, click **Run**, to locate and run the additional installation files.</span></span> <span data-ttu-id="8a090-262">설치가 완료 되 면 **설치 완료** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-262">When you are finished with the installation, select the **I am finished installing** check box, and then click **Next**.</span></span>

8. <span data-ttu-id="8a090-263">**설치** 페이지에서 sequencer가 가상 응용 프로그램 패키지를 구성 하는 동안 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-263">On the **Installation** page, wait while the sequencer configures the virtual application package.</span></span>

9. <span data-ttu-id="8a090-264">**설치 보고서** 페이지에서 방금 시퀀싱 한 가상 응용 프로그램 패키지에 대 한 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-264">On the **Installation Report** page, you can review information about the virtual application package that you have just sequenced.</span></span> <span data-ttu-id="8a090-265">**추가 정보**에서 이벤트를 두 번 클릭 하 여 자세한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-265">In **Additional Information**, double-click an event to obtain more detailed information.</span></span> <span data-ttu-id="8a090-266">계속 하려면 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-266">To proceed, click **Next**.</span></span>

10. <span data-ttu-id="8a090-267">**대상 OS** 페이지에서이 패키지를 실행할 수 있는 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-267">On the **Target OS** page, specify the operating systems that can run this package.</span></span> <span data-ttu-id="8a090-268">해당 환경에서 지원 되는 모든 운영 체제에서이 패키지를 실행 하도록 설정 하려면 **모든 운영 체제에서이 패키지를 실행 하도록 허용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-268">To enable all supported operating systems in your environment to run this package, select the **Allow this package to run on any operating system** check box.</span></span> <span data-ttu-id="8a090-269">특정 운영 체제 에서만이 패키지를 실행 하도록 구성 하려면 **다음 운영 체제 에서만이 패키지를 실행 하도록 허용** 확인란을 선택 하 고이 패키지를 실행할 수 있는 운영 체제를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-269">To configure this package to run only on specific operating systems, select the **Allow this package to run only on the following operating systems** check box and select the operating systems that can run this package.</span></span> <span data-ttu-id="8a090-270">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-270">Click **Next**.</span></span>

11. <span data-ttu-id="8a090-271">**패키지 만들기** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-271">On the **Create Package** page is displayed.</span></span> <span data-ttu-id="8a090-272">패키지를 저장 하지 않고 수정 하려면 패키지 **편집기를 사용 하 여 저장 하지 않고 패키지를 계속 수정**합니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-272">To modify the package without saving it, select **Continue to modify package without saving using the package editor**.</span></span> <span data-ttu-id="8a090-273">이 옵션은 패키지를 저장 하기 전에 수정할 수 있도록 sequencer 콘솔에서 패키지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-273">This option opens the package in the sequencer console so that you can modify the package before it is saved.</span></span> <span data-ttu-id="8a090-274">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-274">Click **Next**.</span></span>

    <span data-ttu-id="8a090-275">패키지를 즉시 저장 하려면 **지금 패키지 저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-275">To save the package immediately, select **Save the package now**.</span></span> <span data-ttu-id="8a090-276">필요에 따라 패키지와 연결할 **설명을** 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-276">Optionally, add a **Description** to be associated with the package.</span></span> <span data-ttu-id="8a090-277">설명은 패키지에 대 한 프로그램 버전 및 기타 정보를 식별 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-277">Descriptions are useful for identifying the program version and other information about the package.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8a090-278">시스템에서 메모 및 설명에 인쇄할 수 없는 문자를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-278">The system does not support non-printable characters in Comments and Descriptions.</span></span>



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. <span data-ttu-id="8a090-279">**완료** 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-279">The **Completion** page is displayed.</span></span> <span data-ttu-id="8a090-280">필요에 따라 **가상 응용 프로그램 패키지 보고서** 창에서 정보를 검토 한 다음 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-280">Review the information in the **Virtual Application Package Report** pane as needed, then click **Close**.</span></span> <span data-ttu-id="8a090-281">이 정보는이 절차의 11 단계에서 지정한 디렉터리에 있는 **Report.xml** 파일 에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-281">This information is also available in the **Report.xml** file that is located in the directory specified in step 11 of this procedure.</span></span>

   <span data-ttu-id="8a090-282">이제 시퀀서에서 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-282">The package is now available in the sequencer.</span></span> <span data-ttu-id="8a090-283">패키지 속성을 편집 하려면 **\ [패키지 이름 \] 편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-283">To edit the package properties, click **Edit \[Package Name\]**.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="8a090-284">가상 응용 프로그램 패키지를 성공적으로 만들었으면 sequencer를 실행 하는 컴퓨터에서 가상 응용 프로그램 패키지를 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8a090-284">After you have successfully created a virtual application package, you cannot run the virtual application package on the computer that is running the sequencer.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="8a090-285">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8a090-285">Related topics</span></span>


[<span data-ttu-id="8a090-286">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="8a090-286">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









