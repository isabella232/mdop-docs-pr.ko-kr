---
title: MED-V 작업 영역 패키지 관리자를 사용하여 URL 리디렉션을 관리하는 방법
description: MED-V 작업 영역 패키지 관리자를 사용하여 URL 리디렉션을 관리하는 방법
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824818"
---
# <span data-ttu-id="d8136-103">MED-V 작업 영역 패키지 관리자를 사용하여 URL 리디렉션을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="d8136-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="d8136-104">MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역의 URL 리디렉션을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="d8136-105">MED-V 작업 영역에서 웹 주소 리디렉션을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="d8136-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="d8136-106">**Med-v 작업 영역 포장기**를 열려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 작업 영역 포장기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="d8136-107">**Med-v 작업 영역 포장기** 기본 패널에서 **웹 리디렉션 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="d8136-108">**웹 리디렉션 관리** 창에서 med-v 작업 영역의 Internet Explorer로 리디렉션되는 url 목록을 입력 하거나, 붙여 넣거나, 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="d8136-109">참고</span><span class="sxs-lookup"><span data-stu-id="d8136-109">Note</span></span>**  
    <span data-ttu-id="d8136-110">MED-V의 URL 리디렉션은 HTTP 및 HTTPS 프로토콜만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="d8136-111">MED-V는 FTP 또는 다른 프로토콜에 대 한 지원을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="d8136-112">**다른 이름으로 저장 ...** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-112">Click **Save as…**</span></span> <span data-ttu-id="d8136-113">지정한 폴더에 업데이트 된 URL 리디렉션 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="d8136-114">MED-V는 업데이트 된 URL 리디렉션 정보를 포함 하는 레지스트리 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="d8136-115">그룹 정책을 사용 하 여 업데이트 된 레지스트리 키를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="d8136-116">그룹 정책을 사용 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="d8136-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="d8136-117">MED-V는 또한 지정 된 폴더에 업데이트 된 MED-V 작업 영역 패키지를 다시 만드는 데 사용할 수 있는 Windows PowerShell 스크립트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8136-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="d8136-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d8136-118">Related topics</span></span>


[<span data-ttu-id="d8136-119">배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="d8136-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="d8136-120">MED-V URL 리디렉션 관리</span><span class="sxs-lookup"><span data-stu-id="d8136-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)









