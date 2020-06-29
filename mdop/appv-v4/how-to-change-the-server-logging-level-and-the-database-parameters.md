---
title: 서버 로깅 수준 및 데이터베이스 매개 변수를 변경하는 방법
description: 서버 로깅 수준 및 데이터베이스 매개 변수를 변경하는 방법
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818033"
---
# <span data-ttu-id="cbee3-103">서버 로깅 수준 및 데이터베이스 매개 변수를 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="cbee3-103">How to Change the Server Logging Level and the Database Parameters</span></span>


<span data-ttu-id="cbee3-104">다음 절차를 사용 하 여 응용 프로그램 가상화 서버 관리 콘솔에서 로그 수준과 데이터베이스 로그 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-104">You can use the following procedures to change the logging level and the database log parameters from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="cbee3-105">다음과 같은 로깅 수준을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-105">The following logging levels are available:</span></span>

-   <span data-ttu-id="cbee3-106">트랜잭션만</span><span class="sxs-lookup"><span data-stu-id="cbee3-106">Transaction Only</span></span>

-   <span data-ttu-id="cbee3-107">치명적 오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-107">Fatal Errors</span></span>

-   <span data-ttu-id="cbee3-108">오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-108">Errors</span></span>

-   <span data-ttu-id="cbee3-109">경고/오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-109">Warnings/Errors</span></span>

-   <span data-ttu-id="cbee3-110">Info/경고/오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-110">Info/Warnings/Errors</span></span>

-   <span data-ttu-id="cbee3-111">자세한 정보 표시</span><span class="sxs-lookup"><span data-stu-id="cbee3-111">Verbose</span></span>

<span data-ttu-id="cbee3-112">**참고**  **Verbose** 모드를 사용할 때 생성 되는 로그 파일의 크기 때문에이 수준의 로깅 설정으로 프로덕션 서버를 실행 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-112">**Note** Because of the size of the log file produced when you use **Verbose** mode, the recommendation is that you do not run production servers with this level of logging set.</span></span>

 

<span data-ttu-id="cbee3-113">데이터베이스 로깅 매개 변수는 데이터베이스 드라이버 형식, 액세스 자격 증명 및 로깅 데이터베이스의 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-113">The database logging parameters determine the database driver type, access credentials, and location of the logging database.</span></span>

**<span data-ttu-id="cbee3-114">관리 서버에 대 한 로깅 수준을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="cbee3-114">To change the logging level for Management Servers</span></span>**

1.  <span data-ttu-id="cbee3-115">서버 **그룹** 노드를 클릭 하 여 서버 그룹을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-115">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="cbee3-116">서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-116">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="cbee3-117">**속성** 대화 상자에서 **로깅** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-117">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="cbee3-118">**서버 그룹 속성** 대화 상자에서 서버를 선택한 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-118">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="cbee3-119">**로그 모듈 추가/편집** 대화 상자의 **이벤트 유형** 드롭다운 목록에서 로깅 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-119">In the **Add/Edit Log Module** dialog box, select the logging level from the **Event Type** drop-down list.</span></span>

6.  <span data-ttu-id="cbee3-120">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-120">Click **OK**.</span></span>

7.  <span data-ttu-id="cbee3-121">**서버 그룹 속성** 대화 상자에서 **확인** 또는 **적용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-121">In the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

**<span data-ttu-id="cbee3-122">스트리밍 서버의 로깅 수준을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="cbee3-122">To change the logging level for Streaming Servers</span></span>**

1.  <span data-ttu-id="cbee3-123">다음 레지스트리 키 값을 편집 하 여 로깅 수준을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-123">Edit the following registry key value to change the logging level:</span></span>

    -   <span data-ttu-id="cbee3-124">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span><span class="sxs-lookup"><span data-stu-id="cbee3-124">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span></span>

2.  <span data-ttu-id="cbee3-125">다음 값 중 하나를 선택 하 여 로깅 수준을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-125">Select one of the following values to set the logging level.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="cbee3-126">값</span><span class="sxs-lookup"><span data-stu-id="cbee3-126">Value</span></span></th>
    <th align="left"><span data-ttu-id="cbee3-127">로깅 수준</span><span class="sxs-lookup"><span data-stu-id="cbee3-127">Logging Level</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="cbee3-128">0</span><span class="sxs-lookup"><span data-stu-id="cbee3-128">0</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cbee3-129">트랜잭션만</span><span class="sxs-lookup"><span data-stu-id="cbee3-129">Transactions Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="cbee3-130">raid-1</span><span class="sxs-lookup"><span data-stu-id="cbee3-130">1</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cbee3-131">치명적 오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-131">Fatal Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="cbee3-132">2</span><span class="sxs-lookup"><span data-stu-id="cbee3-132">2</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cbee3-133">오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-133">Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="cbee3-134">3-4</span><span class="sxs-lookup"><span data-stu-id="cbee3-134">3</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cbee3-135">경고/오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-135">Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="cbee3-136">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="cbee3-136">4</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cbee3-137">정보/경고/오류</span><span class="sxs-lookup"><span data-stu-id="cbee3-137">Information/ Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="cbee3-138">5mb</span><span class="sxs-lookup"><span data-stu-id="cbee3-138">5</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cbee3-139">자세한 정보 표시</span><span class="sxs-lookup"><span data-stu-id="cbee3-139">Verbose</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="cbee3-140">데이터베이스 로그 매개 변수를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="cbee3-140">To change database log parameters</span></span>**

1.  <span data-ttu-id="cbee3-141">서버 **그룹** 노드를 클릭 하 여 서버 그룹을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-141">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="cbee3-142">서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-142">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="cbee3-143">**속성** 대화 상자에서 **로깅** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-143">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="cbee3-144">**서버 그룹 속성** 대화 상자에서 서버를 선택한 다음 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-144">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="cbee3-145">**로그 모듈 추가/편집** 대화 상자의 **데이터베이스 드라이버** 드롭다운 목록에서 데이터베이스 드라이버를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-145">In the **Add/Edit Log Module** dialog box, select a database driver from the **Database Driver** drop-down list.</span></span>

6.  <span data-ttu-id="cbee3-146">**DNS 호스트 이름을**입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-146">Enter a **DNS Host Name**.</span></span>

7.  <span data-ttu-id="cbee3-147">**동적으로 포트 결정** 확인란을 클릭 하거나 포트 필드에 포트 번호를 입력 **합니다.**</span><span class="sxs-lookup"><span data-stu-id="cbee3-147">Click the **Dynamically Determine Port** check box, or enter a port number in the **Port** field.</span></span>

8.  <span data-ttu-id="cbee3-148">해당 필드에 **서비스 이름을** 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-148">Enter a **Service Name** in the corresponding field.</span></span>

9.  <span data-ttu-id="cbee3-149">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-149">Click **OK**.</span></span>

10. <span data-ttu-id="cbee3-150">**서버 그룹 속성** 대화 상자에서 **확인** 또는 **적용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbee3-150">On the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

## <span data-ttu-id="cbee3-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cbee3-151">Related topics</span></span>


[<span data-ttu-id="cbee3-152">Server Management Console에서 Application Virtualization 시스템을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="cbee3-152">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





