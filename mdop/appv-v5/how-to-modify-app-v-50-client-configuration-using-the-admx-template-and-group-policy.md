---
title: ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법
description: ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813841"
---
# <span data-ttu-id="65996-103">ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="65996-103">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="65996-104">앱-V 5.0 ADMX 템플릿을 사용 하 여 ADMX 템플릿 및 그룹 정책을 사용 하 여 App-v 5.0 클라이언트 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="65996-104">Use the App-V 5.0 ADMX template to configure App-V 5.0 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="65996-105">그룹 정책을 사용 하 여 앱-V 5.0 클라이언트 구성을 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="65996-105">To modify App-V 5.0 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="65996-106">App-v 5.0 클라이언트 구성을 수정 하려면 App-v 5.0와 함께 제공 되는 **ADMXTemplate** 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="65996-106">To modify the App-V 5.0 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.0.</span></span>

    <span data-ttu-id="65996-107">**참고**  앱-V 5.0 **ADMX 서식 파일**을 다운로드 하려면 다음 링크를 사용 <https://go.microsoft.com/fwlink/p/?LinkId=393941> 합니다.</span><span class="sxs-lookup"><span data-stu-id="65996-107">**Note** Use the following link to download the App-V 5.0 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="65996-108">그룹 정책을 관리 하는 컴퓨터 (일반적으로 도메인 컨트롤러)에서 다음 디렉터리에 **admx** 파일을 복사 합니다. \*\* &lt; 설치 드라이브 &gt; \ \ Windows \\ policydefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="65996-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="65996-109">그 다음, 같은 컴퓨터에서 **adml** 파일을 다음 디렉터리에 복사 합니다. \ \ \*\* &lt; &gt; \ Windows \\ policydefinitions \ \ en-US\*\*.</span><span class="sxs-lookup"><span data-stu-id="65996-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="65996-110">파일을 복사한 후 그룹 정책 관리 콘솔을 열고, 앱-v 5.0 클라이언트와 연결 된 정책을 수정 하려면 **컴퓨터 구성**  /  **정책**  /  **관리 템플릿**  /  **시스템**  /  **app-v**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="65996-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.0 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="65996-111">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="65996-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="65996-112">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="65996-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="65996-113">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="65996-113">Got an App-V issue?</span></span>** <span data-ttu-id="65996-114">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65996-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="65996-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="65996-115">Related topics</span></span>


[<span data-ttu-id="65996-116">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="65996-116">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="65996-117">클라이언트 구성 설정 정보</span><span class="sxs-lookup"><span data-stu-id="65996-117">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

 

 





