---
title: 스크립트 동작을 설정하는 방법
description: 스크립트 동작을 설정하는 방법
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812388"
---
# <span data-ttu-id="ef2a1-103">스크립트 동작을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="ef2a1-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="ef2a1-104">스크립트 작업 편집기에서는 관리자가 MED-V 작업 영역 설정 중 수행할 동작과 수행할 순서를 정의 하는 작업을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="ef2a1-105">다음은 도메인 설정 스크립트에 추가할 수 있는 작업의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="ef2a1-106">Windows **다시 시작**-windows를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="ef2a1-107">**도메인에 가입**— 도메인에 참가 하는 경우이 작업을 포함 하 고 사용자 이름, 암호, 정규화 된 도메인 이름, NetBIOS 도메인 이름 및 조직 단위를 구성 합니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="ef2a1-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="ef2a1-108">연결 **확인**-연결할 서버를 구성 하 고 med-v 작업 영역이 네트워크 리소스 (예: 도메인 서버)에 연결할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="ef2a1-109">**명령줄-med-v**작업 영역에서 스크립트를 구성 하 고 스크립트 경로와 스크립트 인수를 포함 하는 명령줄을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="ef2a1-110">**컴퓨터 이름 바꾸기**— 정의 된 설정을 기반으로 가상 컴퓨터 컴퓨터의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="ef2a1-111">**자동 로그온 사용 안 함**-Windows 자동 로그온을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="ef2a1-112">이 작업은 컴퓨터를 도메인에 추가 하는 스크립트의 끝에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="ef2a1-113">스크립트 동작을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="ef2a1-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="ef2a1-114">스크립트 동작을 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="ef2a1-114">To set up script actions</span></span>**

1.  <span data-ttu-id="ef2a1-115">**VM 설정** 탭에서 **스크립트 편집기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="ef2a1-116">**스크립트 작업** 대화 상자에서 **추가**를 클릭 하 고 하위 메뉴에서 원하는 작업을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="ef2a1-117">다음 표에 설명 된 대로 작업을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="ef2a1-118">**참고** 
     **컴퓨터 이름 바꾸기** 는 **VM 설정** 탭에서 구성 합니다. 자세한 내용은 [VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="ef2a1-119">작업을 선택 하 고 **위쪽** 또는 **아래**를 클릭 하 여 작업 순서를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="ef2a1-120">**OK**(확인)를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-120">Click **OK**.</span></span>

**<span data-ttu-id="ef2a1-121">참고</span><span class="sxs-lookup"><span data-stu-id="ef2a1-121">Note</span></span>**  
<span data-ttu-id="ef2a1-122">도메인 가입 스크립트를 실행할 때 스크립트 작동을 위해 MED-V 작업 영역 가상 컴퓨터에 로그인 한 사용자에 게 로컬 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="ef2a1-123">참고</span><span class="sxs-lookup"><span data-stu-id="ef2a1-123">Note</span></span>**  
<span data-ttu-id="ef2a1-124">자동 로그온 사용 안 함 스크립트를 실행 하는 경우 초기 설정이 완료 되 면 자동 로그온에 사용 되는 로컬 게스트 계정을 사용 하지 않도록 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="ef2a1-125">도메인 속성 참가</span><span class="sxs-lookup"><span data-stu-id="ef2a1-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef2a1-126">속성</span><span class="sxs-lookup"><span data-stu-id="ef2a1-126">Property</span></span></th>
<th align="left"><span data-ttu-id="ef2a1-127">설명</span><span class="sxs-lookup"><span data-stu-id="ef2a1-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-128">VM을 도메인에 참가할 때 사용할 자격 증명</span><span class="sxs-lookup"><span data-stu-id="ef2a1-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-129">VM을 도메인에 참가할 때 사용할 다음 자격 증명 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="ef2a1-130">MED-V 자격 증명 </strong> -최종 사용자 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="ef2a1-131">지정 된 자격 증명으로 다음 자격 증명을 사용 합니다. </strong> 해당 필드에 사용자 이름 및 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="ef2a1-132">참고</span><span class="sxs-lookup"><span data-stu-id="ef2a1-132">Note</span></span></strong><br/><p><span data-ttu-id="ef2a1-133">입력 하는 자격 증명은 모든 MED-V 작업 영역 사용자에 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="ef2a1-134">도메인 관리자 자격 증명을 제공 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-135">가입할 도메인</span><span class="sxs-lookup"><span data-stu-id="ef2a1-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-136">다음 중 하나를 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="ef2a1-137">작업 영역을 시작 하는 데 사용 된 도메인 이름 </strong> , 즉 med-v 클라이언트에 로그인 할 때 최종 사용자가 입력 한 도메인에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="ef2a1-138">NetBIOS에서 정규화 된 도메인 이름으로의 매핑을 정의 하려면 <strong> 전역 도메인 매핑 테이블을 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="ef2a1-139">전역 도메인 매핑 테이블에서 <strong> 추가 </strong> 를 클릭 하 고 <strong> NetBIOS 도메인 이름 </strong> 및 정규화 된 <strong> 도메인 이름을 입력 </strong> 한 다음 확인을 클릭 <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="ef2a1-140">다음 도메인 이름 사용 </strong> -지정 된 도메인에 참가 합니다. 도메인 이름 및 NetBIOS 도메인 이름을 해당 필드에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-141">조직 구성 단위</span><span class="sxs-lookup"><span data-stu-id="ef2a1-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-142">OU (조직 구성 단위)는 컴퓨터를 특정 OU에 가입 하도록 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="ef2a1-143">형식은 ou 고유 이름 다음에와 야 합니다. OU = &lt; 조직 구성 단위 &gt; , &lt; 도메인 컨트롤러 &gt; (예: OU = QATest, DC = IL, DC = med-v, dc = com).</span><span class="sxs-lookup"><span data-stu-id="ef2a1-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ef2a1-144">Warning</span><span class="sxs-lookup"><span data-stu-id="ef2a1-144">Warning</span></span></strong><br/><p><span data-ttu-id="ef2a1-145">위의 예제에 나와 있는 것 처럼 단일 수준 OU만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="ef2a1-146">연결 속성 확인</span><span class="sxs-lookup"><span data-stu-id="ef2a1-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef2a1-147">속성</span><span class="sxs-lookup"><span data-stu-id="ef2a1-147">Property</span></span></th>
<th align="left"><span data-ttu-id="ef2a1-148">설명</span><span class="sxs-lookup"><span data-stu-id="ef2a1-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-149">IP 주소</span><span class="sxs-lookup"><span data-stu-id="ef2a1-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-150">연결을 확인 하는 서버의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-151">Port</span><span class="sxs-lookup"><span data-stu-id="ef2a1-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-152">연결을 확인 하는 서버의 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-153">시간 제한</span><span class="sxs-lookup"><span data-stu-id="ef2a1-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-154">제한 시간 전에 응답을 기다리는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="ef2a1-155">명령줄 속성</span><span class="sxs-lookup"><span data-stu-id="ef2a1-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef2a1-156">속성</span><span class="sxs-lookup"><span data-stu-id="ef2a1-156">Property</span></span></th>
<th align="left"><span data-ttu-id="ef2a1-157">설명</span><span class="sxs-lookup"><span data-stu-id="ef2a1-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-158">경로</span><span class="sxs-lookup"><span data-stu-id="ef2a1-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-159">명령줄의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-160">인수</span><span class="sxs-lookup"><span data-stu-id="ef2a1-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-161">명령줄 인수</span><span class="sxs-lookup"><span data-stu-id="ef2a1-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-162">끝내기 대기</span><span class="sxs-lookup"><span data-stu-id="ef2a1-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-163">스크립트 작업을 계속 하기 전에 반환 될 때까지 대기 하는 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-164">오류 발생 시 실패</span><span class="sxs-lookup"><span data-stu-id="ef2a1-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-165">반환 내용이 지정 된 값인 경우에는이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="ef2a1-166">명령이 성공으로 표시 되는 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="ef2a1-167">기본값: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="ef2a1-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-168">한 번만 수행</span><span class="sxs-lookup"><span data-stu-id="ef2a1-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-169">명령줄을 한 번만 실행 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="ef2a1-170">스크립트가 실패 하거나 취소 되 면이 명령은 다시 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-171">이 명령줄을 실행 하면 작업 영역에서 Windows가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-172">명령줄에 완료 후 다시 시작이 발생 하는 경우이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-173">조작 허용</span><span class="sxs-lookup"><span data-stu-id="ef2a1-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-174">명령에 사용자 조작이 필요한 경우이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-175">진행률 메시지</span><span class="sxs-lookup"><span data-stu-id="ef2a1-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-176">명령이 실행 되는 동안 사용자에 게 표시할 메시지</span><span class="sxs-lookup"><span data-stu-id="ef2a1-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-177">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="ef2a1-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-178">명령이 실패 하는 경우 사용자에 게 표시 되는 메시지</span><span class="sxs-lookup"><span data-stu-id="ef2a1-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ef2a1-179">명령줄 작업을 구성할 때 다음 표에 정의 된 대로 여러 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef2a1-180">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef2a1-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ef2a1-181">값</span><span class="sxs-lookup"><span data-stu-id="ef2a1-181">Value</span></span></th>
<th align="left"><span data-ttu-id="ef2a1-182">설명</span><span class="sxs-lookup"><span data-stu-id="ef2a1-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-183">% MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="ef2a1-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-184">인증 된 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-185">MED-V 인증 된 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-185">MED-V authenticated user name.</span></span> <span data-ttu-id="ef2a1-186">사용자 이름 및 암호는 도메인 VM 설치 스크립트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-187">% MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="ef2a1-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-188">인증 된 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-189">MED-V 인증 된 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-189">MED-V authenticated password.</span></span> <span data-ttu-id="ef2a1-190">사용자 이름 및 암호는 도메인 VM 설치 스크립트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef2a1-191">% MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="ef2a1-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-192">도메인을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-193">MED-V 인증에서 구성 된 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="ef2a1-194">VM 설치 스크립트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef2a1-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="ef2a1-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-196">컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef2a1-197">관리 응용 프로그램에 구성 된 고유한 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="ef2a1-198">VM 설치 스크립트에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2a1-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ef2a1-199">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ef2a1-199">Related topics</span></span>


[<span data-ttu-id="ef2a1-200">MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="ef2a1-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="ef2a1-201">VM 컴퓨터 이름 패턴 속성을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="ef2a1-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





