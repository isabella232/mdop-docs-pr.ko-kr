---
title: MED-V 작업 영역에 응용 프로그램 설치 및 제거
description: MED-V 작업 영역에 응용 프로그램 설치 및 제거
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827218"
---
# <span data-ttu-id="edd71-103">MED-V 작업 영역에 응용 프로그램 설치 및 제거</span><span class="sxs-lookup"><span data-stu-id="edd71-103">Installing and Removing an Application on the MED-V Workspace</span></span>


<span data-ttu-id="edd71-104">호스트 운영 체제와 호환 되지 않는 응용 프로그램은 MED-V 작업 영역에서 실행할 수 있으며 호스트 컴퓨터, **시작** 메뉴 또는 localhost 바로 가기 키를 사용 하 여 열 때와 같은 방식으로 med-v 작업 영역에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-104">Applications that are incompatible with the host operating system can be run in the MED-V workspace and opened in the MED-V workspace in the same manner in which they are opened from the host computer, on the **Start** menu or by using a localhost shortcut.</span></span>

<span data-ttu-id="edd71-105">MED-V 작업 영역을 배포한 후에는 MED-V 작업 영역에 응용 프로그램을 설치 하 고 제거 하는 데 사용할 수 있는 여러 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-105">After you have deployed a MED-V workspace, you have several different options available to you for installing and removing applications in the MED-V workspace.</span></span> <span data-ttu-id="edd71-106">이러한 옵션에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-106">These options include the following:</span></span>

-   [<span data-ttu-id="edd71-107">그룹 정책 사용</span><span class="sxs-lookup"><span data-stu-id="edd71-107">Using Group Policy</span></span>](#bkmk-grouppolicy)

-   [<span data-ttu-id="edd71-108">전자 소프트웨어 배포 시스템 사용</span><span class="sxs-lookup"><span data-stu-id="edd71-108">Using an Electronic Software Distribution System</span></span>](#bkmk-esd)

-   [<span data-ttu-id="edd71-109">Application Virtualization (APP-V) 사용</span><span class="sxs-lookup"><span data-stu-id="edd71-109">Using Application Virtualization (APP-V)</span></span>](#bkmk-appv)

-   [<span data-ttu-id="edd71-110">핵심 이미지 업데이트</span><span class="sxs-lookup"><span data-stu-id="edd71-110">Updating the Core Image</span></span>](#bkmk-coreimage)

<span data-ttu-id="edd71-111">**중요**  설치 된 응용 프로그램이 호스트에 자동으로 게시 되도록 하려면 **모든 사용자**의 가상 컴퓨터에 응용 프로그램을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-111">**Important** To make sure that an installed application is automatically published to the host, install the application on the virtual machine for **All Users**.</span></span> <span data-ttu-id="edd71-112">응용 프로그램 게시에 대 한 자세한 내용은 [Med-v 작업 영역에서 응용 프로그램 게시 및 게시 취소 하는 방법을](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="edd71-112">For more information about application publishing, see [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span>

 

<span data-ttu-id="edd71-113">**팁**  MED-V는 MED-V 작업 영역의 Internet Explorer에서 Microsoft Word 문서를 두 번 클릭 하는 등의 콘텐츠 처리에 대 한 게스트 대 호스트 리디렉션을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-113">**Tip** MED-V does not support guest-to-host redirection for content handling, such as double-clicking a Microsoft Word document in Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="edd71-114">따라서 Microsoft Word와 같은 필수 응용 프로그램을 MED-V 작업 영역에 설치 하 여 최종 사용자가 예상할 수 있는 기본 콘텐츠 처리 기능을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-114">Therefore, the required applications, such as Microsoft Word, must be installed in MED-V workspace to provide the default content handling functionality that an end user might expect.</span></span>

 

## <a href="" id="bkmk-grouppolicy"></a> <span data-ttu-id="edd71-115">그룹 정책을 사용 하 여 응용 프로그램 추가 및 제거</span><span class="sxs-lookup"><span data-stu-id="edd71-115">Adding and Removing Applications by Using Group Policy</span></span>


<span data-ttu-id="edd71-116">그룹 정책 및 그룹 정책 개체를 사용 하 여 엔터프라이즈의 MED-V 작업 영역 전체 또는 일부에 응용 프로그램을 할당 하거나 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-116">You can use Group Policy and Group Policy objects to assign or publish applications to all or some MED-V workspaces in your enterprise.</span></span> <span data-ttu-id="edd71-117">할당 된 응용 프로그램의 경우 최종 사용자가 컴퓨터에 로그온 하면 **시작** 메뉴에 해당 응용 프로그램이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-117">For assigned applications, when an end user logs on to their computer, the application appears on the **Start** menu.</span></span> <span data-ttu-id="edd71-118">처음으로 새 응용 프로그램을 선택 하면 응용 프로그램이 설치 되 고 사용할 준비가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-118">When they select the new application for the first time, the application installs and is ready for use.</span></span> <span data-ttu-id="edd71-119">게시 된 응용 프로그램의 경우 **시작** 메뉴에 응용 프로그램이 나타나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-119">For published applications, the application does not appear on the **Start** menu.</span></span> <span data-ttu-id="edd71-120">**제어판** 의 **프로그램 추가/제거** 를 사용 하거나 응용 프로그램과 연결 된 파일을 열어 최종 사용자만 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-120">It is only available for the end user to install by using **Add or Remove Programs** in **Control Panel** or by opening a file that is associated with the application.</span></span>

<span data-ttu-id="edd71-121">동일한 방법으로 그룹 정책 및 그룹 정책 개체를 사용 하 여 MED-V 작업 영역에서 응용 프로그램을 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-121">You can also use Group Policy and Group Policy objects in the same manner to remove applications from the MED-V workspace.</span></span>

<span data-ttu-id="edd71-122">그룹 정책을 사용 하 여 응용 프로그램을 추가 하 고 제거 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) (를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="edd71-122">For more information about how to add and remove applications by using Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

## <a href="" id="bkmk-esd"></a> <span data-ttu-id="edd71-123">ESD 시스템을 사용 하 여 응용 프로그램 추가 및 제거</span><span class="sxs-lookup"><span data-stu-id="edd71-123">Adding and Removing Applications by Using an ESD System</span></span>


<span data-ttu-id="edd71-124">ESD (전자 소프트웨어 배포) 시스템은 네트워크 연결을 통해 다양 한 컴퓨터에 소프트웨어 및 기타 정보를 효율적으로 배포 하도록 디자인 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-124">An electronic software distribution (ESD) system is designed to efficiently deploy software and other information to many different computers over network connections.</span></span> <span data-ttu-id="edd71-125">조직에서 ESD 시스템을 사용 하 여 소프트웨어를 배포 하는 경우 물리적 컴퓨터에서 응용 프로그램을 추가 하 고 제거 하는 것 처럼이를 사용 하 여 MED-V 작업 영역에서 응용 프로그램을 추가 하 고 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-125">If your organization uses an ESD system to deploy software, you can use it to add and remove applications on MED-V workspaces just as you add and remove applications on physical computers.</span></span>

## <a href="" id="bkmk-appv"></a> <span data-ttu-id="edd71-126">앱을 사용 하 여 응용 프로그램 추가 및 제거-V</span><span class="sxs-lookup"><span data-stu-id="edd71-126">Adding and Removing Applications by Using APP-V</span></span>


<span data-ttu-id="edd71-127">Microsoft App-v (Application Virtualization)는 해당 컴퓨터에 직접 응용 프로그램을 설치할 필요 없이 최종 사용자 컴퓨터에서 응용 프로그램을 사용할 수 있도록 하는 관리 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-127">Microsoft Application Virtualization (App-V) provides the administrative capability to make applications available to end-user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="edd71-128">예를 들어, Windows XP에서 앱으로 시퀀싱 한 응용 프로그램이 조직에 있고,이를 다시 시퀀싱 하 여 Windows 7로 마이그레이션이 지연 되는 경우에는 MED-V와 App-v를 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-128">You might want to use MED-V and App-V together if, for example, your organization has applications that you sequenced with App-V in Windows XP, and re-sequencing them would delay your migration to Windows 7.</span></span>

<span data-ttu-id="edd71-129">MED-V와 앱-V를 함께 사용 하 여 배포 된 MED-V 작업 영역에서 가상 응용 프로그램을 추가 하 고 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-129">You can use MED-V together with App-V to add and remove virtual applications on a deployed MED-V workspace.</span></span> <span data-ttu-id="edd71-130">이 방법으로 응용 프로그램을 관리 하려면 먼저 MED-V 게스트 운영 체제에 App-v 에이전트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-130">To manage applications in this manner, you must first install the App-V agent on the MED-V guest operating system.</span></span> <span data-ttu-id="edd71-131">그런 다음 MED-V 작업 영역에서 App-v를 사용 하 여 가상 응용 프로그램을 추가 하 고 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-131">You can then use App-V in the MED-V workspace to add and remove the virtual applications.</span></span>

<span data-ttu-id="edd71-132">App-v를 설치 하 고 사용 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화](https://go.microsoft.com/fwlink/?LinkId=122939) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="edd71-132">For information about how to install and use App-V, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

<span data-ttu-id="edd71-133">**중요**  MED-V 작업 영역에 게시 하는 앱-V 응용 프로그램에는 호스트 컴퓨터에서 게스트 가상 컴퓨터로 리디렉션할 수 없는 파일 형식 연결이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-133">**Important** App-V applications that you publish to the MED-V workspace have file-type associations that cannot redirect from the host computer to the guest virtual machine.</span></span> <span data-ttu-id="edd71-134">그러나 최종 사용자는 **파일**을 클릭 한 다음 게시 된 app-v 응용 프로그램에서 **열기** 를 클릭 하 여 이러한 파일 형식을 계속 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-134">However, the end user can still access these file types by clicking **File**, and then by clicking **Open** on the published App-V application.</span></span>

<span data-ttu-id="edd71-135">이러한 파일 형식 연결을 강제 전환 하려면 게스트 가상 컴퓨터의 명령 프롬프트에 다음을 입력 하 여 매핑된 파일 형식 연결에 대해 App-v 쿼리: **sftmime/QUERY OBJ: type**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-135">To force redirection of those file-type associations, query App-V for mapped file type associations by typing the following at a command prompt in the guest virtual machine: **sftmime /QUERY OBJ:TYPE**.</span></span> <span data-ttu-id="edd71-136">그런 다음 호스트 컴퓨터에서 해당 파일 형식 연결을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-136">Then, map those file type associations in the host computer.</span></span>

 

## <a href="" id="bkmk-coreimage"></a> <span data-ttu-id="edd71-137">코어 이미지에서 응용 프로그램 추가 및 제거</span><span class="sxs-lookup"><span data-stu-id="edd71-137">Adding and Removing Applications on the Core Image</span></span>


<span data-ttu-id="edd71-138">MED-V 모범 사례로 간주 되지 않더라도 코어 이미지에서 직접 응용 프로그램을 추가 하 고 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-138">Although not considered a MED-V best practice, you can add and remove applications directly on the core image.</span></span> <span data-ttu-id="edd71-139">응용 프로그램을 추가 하거나 제거한 후에는 원래 배포 하는 것과 동일한 방법으로 엔터프라이즈에 MED-V 작업 영역을 다시 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-139">After you have added or removed an application, you can redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

<span data-ttu-id="edd71-140">코어 이미지에서 응용 프로그램을 추가 하거나 제거 하는 방법에 대 한 자세한 내용은 [Windows 가상 PC 이미지에 응용 프로그램 설치](installing-applications-on-a-windows-virtual-pc-image.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="edd71-140">For more information about how to add or remove applications on the core image, see [Installing Applications on a Windows Virtual PC Image](installing-applications-on-a-windows-virtual-pc-image.md).</span></span>

<span data-ttu-id="edd71-141">**중요**  이 방법은 응용 프로그램을 관리 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-141">**Important** We do not recommend this method of managing applications.</span></span> <span data-ttu-id="edd71-142">코어 이미지에서 응용 프로그램을 추가 또는 제거 하 고 MED-V 작업 영역을 enterprise에 다시 배포 하는 경우 먼저 설치 프로그램이 다시 실행 되어야 하 고 가상 컴퓨터에 저장 된 모든 데이터가 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-142">If you add or remove applications on the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved on the virtual machine is lost.</span></span>

 

<span data-ttu-id="edd71-143">**참고**  응용 프로그램이 MED-V 작업 영역에 설치 되어 있는 경우에도 응용 프로그램이 최종 사용자에 게 제공 되기 전에 게시 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-143">**Note** Even though an application is installed into a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="edd71-144">예를 들어 설치 시 **시작** 메뉴에 바로 가기가 자동으로 만들어지지 않은 경우 설치 된 응용 프로그램을 게시 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-144">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span> <span data-ttu-id="edd71-145">마찬가지로, 응용 프로그램의 게시를 취소 하려면 **시작** 메뉴에서 바로 가기를 수동으로 제거 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-145">Likewise, to unpublish an application, you might have to manually remove a shortcut from the **Start** menu.</span></span>

<span data-ttu-id="edd71-146">기본적으로 대부분의 응용 프로그램은 설치 된 시점에 게시 되며 바로 가기가 자동으로 만들어지고 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="edd71-146">By default, most applications are published at the time that they are installed, when shortcuts are automatically created and enabled.</span></span>

 

## <span data-ttu-id="edd71-147">관련 항목</span><span class="sxs-lookup"><span data-stu-id="edd71-147">Related topics</span></span>


[<span data-ttu-id="edd71-148">응용 프로그램 게시를 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="edd71-148">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="edd71-149">MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="edd71-149">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





