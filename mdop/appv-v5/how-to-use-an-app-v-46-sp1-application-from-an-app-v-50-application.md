---
ms.reviewer: ''
title: App-v 5.0 응용 프로그램에서 앱-V 4.6 응용 프로그램을 사용 하는 방법
description: App-v 5.0 응용 프로그램에서 앱-V 4.6 응용 프로그램을 사용 하는 방법
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813644"
---
# <span data-ttu-id="81f35-103">App-v 5.0 응용 프로그램에서 앱-V 4.6 응용 프로그램을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="81f35-103">How to Use an App-V 4.6 Application From an App-V 5.0 Application</span></span>

<span data-ttu-id="81f35-104">*참고:*\* app-v 4.6에는 메인스트림 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="81f35-105">다음은 App-v 4.6 SP3 패키지에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="81f35-106">독립 실행형 클라이언트에서 App-v 5.0 응용 프로그램을 사용 하 여 App-v 4.6 응용 프로그램을 실행 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-106">Use the following procedure to run an App-V4.6 application with App-V 5.0 applications on a standalone client.</span></span>

**<span data-ttu-id="81f35-107">독립 실행형 클라이언트에서 응용 프로그램을 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="81f35-107">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="81f35-108">환경에서 서로 열 수 있는 두 개의 응용 프로그램을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-108">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="81f35-109">예를 들어 Microsoft Outlook 및 Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="81f35-109">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="81f35-110">Adobe Acrobat을 사용 하 여 만든 전자 메일 첨부 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-110">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="81f35-111">패키지를 변환 하거나 App-v 5.0 형식을 사용 하는 응용 프로그램 중 하나에 대 한 새 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-111">Convert the packages, or create a new package for either of the applications using the App-V 5.0 format.</span></span> <span data-ttu-id="81f35-112">패키지를 변환 하는 방법에 대 한 자세한 내용은 [특정 컴퓨터의 모든 사용자에 대 한 앱-v 4.6 패키지의 확장 지점을 변환 된 app-v 5.0 패키지로 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) 또는 [특정 사용자 용 App-v 4.6 5.0 패키지의 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81f35-112">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="81f35-113">App-v 5.0 관리 콘솔을 사용 하 여 패키지를 추가 하 고 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-113">Add and provision the package using the App-V 5.0 management console.</span></span> <span data-ttu-id="81f35-114">패키지 추가 및 배포에 대 한 자세한 내용은 [관리 콘솔을 사용 하 여 패키지를 추가 하거나 업그레이드 하는 방법](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) 및 [관리 콘솔을 사용 하 여 패키지에 대 한 액세스를 구성](how-to-configure-access-to-packages-by-using-the-management-console-50.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81f35-114">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span></span>

4.  <span data-ttu-id="81f35-115">이제 변환 된 응용 프로그램이 App-v 5.0를 사용 하 여 실행 되며 다른 응용 프로그램을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-115">The converted application now runs using App-V 5.0 and you can open one application from the other.</span></span> <span data-ttu-id="81f35-116">예를 들어 Microsoft Office 패키지를 App-v 5.0 패키지로 변환 하 고 Adobe Acrobat이 App-v 4.6 패키지로 계속 실행 되 고 있는 경우 Microsoft Outlook을 사용 하 여 Adobe Acrobat Reader 첨부 파일을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-116">For example, if you converted a Microsoft Office package to an App-V 5.0 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="81f35-117">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="81f35-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="81f35-118">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="81f35-119">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="81f35-119">Got an App-V issue?</span></span>** <span data-ttu-id="81f35-120">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81f35-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="81f35-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="81f35-121">Related topics</span></span>


[<span data-ttu-id="81f35-122">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="81f35-122">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 








