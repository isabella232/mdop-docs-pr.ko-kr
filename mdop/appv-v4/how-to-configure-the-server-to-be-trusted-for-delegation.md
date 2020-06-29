---
title: 위임을 위해 신뢰할 수 있는 서버를 구성하는 방법
description: 위임을 위해 신뢰할 수 있는 서버를 구성하는 방법
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817748"
---
# <span data-ttu-id="b700b-103">위임을 위해 신뢰할 수 있는 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="b700b-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="b700b-104">Microsoft App-v (Application Virtualization) 관리 서버 소프트웨어를 설치할 때 분산 시스템 아키텍처를 사용 하 여 설치 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="b700b-105">콘솔, 관리 웹 서비스 및 데이터베이스를 다른 컴퓨터에 설치 하는 경우 위임용으로 신뢰할 수 있도록 IIS (인터넷 정보 서비스) 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="b700b-106">이는 관리 웹 서비스가 콘솔을 사용 하는 App-v 관리자의 자격 증명을 사용 하 여 App-v 데이터 저장소에 연결 하려고 시도 하기 때문에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="b700b-107">IIS 서버를 위임용으로 신뢰 하도록 구성 하지 않은 경우 데이터 저장소가 설치 된 데이터베이스 서버에서 IIS 서버의 관리자 자격 증명을 받아들이지 않으므로 관리 웹 서비스에서 App-v 데이터 저장소에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="b700b-108">**참고**  단일 서버에 App-v 관리 서버 소프트웨어를 설치 하 고 별도의 서버에 데이터 저장소를 배치 하는 경우 관리 웹 서비스 및 관리 콘솔이 동일한 서버에 있더라도 위임에 대해 신뢰할 수 있는 상태로 서버를 구성 해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="b700b-109">이러한 상황은 **대체 자격 증명 사용** 옵션을 사용 하 여 콘솔의 관리 웹 서비스에 연결 해야 하는 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="b700b-110">사용할 수 있는 위임 유형은 Active Directory 도메인 서비스 (ADDS) 인프라에서 구성한 도메인 기능 수준에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="b700b-111">다음 표에는 App-v의 각 도메인 기능 수준에 대해 구성할 수 있는 위임 유형이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="b700b-112">자세한 지침은 표를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="b700b-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b700b-113">도메인 기능 수준</span><span class="sxs-lookup"><span data-stu-id="b700b-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="b700b-114">사용 가능한 위임 수준</span><span class="sxs-lookup"><span data-stu-id="b700b-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b700b-115">Windows 2000 네이티브</span><span class="sxs-lookup"><span data-stu-id="b700b-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b700b-116">대리인 없음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b700b-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="b700b-117">무제한 위임</span><span class="sxs-lookup"><span data-stu-id="b700b-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b700b-118">Windows Server 2003, Windows Server 2008 또는 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b700b-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b700b-119">대리인 없음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b700b-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="b700b-120">무제한 위임 ¹</span><span class="sxs-lookup"><span data-stu-id="b700b-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="b700b-121">제한 된 위임 (Kerberos 전용 프로토콜 사용)</span><span class="sxs-lookup"><span data-stu-id="b700b-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="b700b-122">제한 된 위임 (모든 인증 프로토콜 사용) ¹</span><span class="sxs-lookup"><span data-stu-id="b700b-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b700b-123">¹ 권장 하지 않음.</span><span class="sxs-lookup"><span data-stu-id="b700b-123">¹ Not recommended.</span></span>

## <span data-ttu-id="b700b-124">도메인 기능 수준이 Windows 2000 네이티브 인 경우 무제한 위임을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b700b-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="b700b-125">웹 서버의 도메인 컨트롤러에서 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="b700b-126">**시작**, **관리 도구**를 차례로 클릭 한 다음 **Active Directory 사용자 및 컴퓨터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="b700b-127">도메인을 확장 한 다음 컴퓨터 폴더를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="b700b-128">오른쪽 창에서 웹 서버의 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="b700b-129">**일반** 탭에서 **위임용으로 컴퓨터 트러스트** 확인란이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="b700b-130">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-130">Click **OK**.</span></span>

## <span data-ttu-id="b700b-131">도메인 기능 수준이 Windows Server 2003, Windows Server 2008 또는 Windows Server 2008 R2 인 경우 무제한 위임을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b700b-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="b700b-132">웹 서버의 도메인 컨트롤러에서 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="b700b-133">**시작**을 클릭 하 고 **관리 도구**를 클릭 한 다음 **Active Directory 사용자 및 컴퓨터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="b700b-134">도메인을 확장 하 고 컴퓨터 폴더를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="b700b-135">오른쪽 창에서 웹 서버의 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **위임** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="b700b-136">**모든 서비스에 대 한 위임용으로이 컴퓨터 신뢰 (Kerberos만)** 를 클릭 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="b700b-137">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-137">Click **OK**.</span></span>

## <span data-ttu-id="b700b-138">도메인 기능 수준이 Windows Server 2003, Windows Server 2008 또는 Windows Server 2008 R2 인 경우 제한 위임을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b700b-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="b700b-139">웹 서버의 도메인 컨트롤러에서 다음 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="b700b-140">**시작**을 클릭 하 고 **관리 도구**를 클릭 한 다음 **Active Directory 사용자 및 컴퓨터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="b700b-141">도메인을 확장 한 다음 컴퓨터 폴더를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="b700b-142">오른쪽 창에서 웹 서버의 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **위임** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="b700b-143">**지정 된 서비스에 대 한 위임용 으로만이 컴퓨터 신뢰**를 클릭 하 여 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="b700b-144">**Kerberos만 사용** 이 선택 되어 있는지 확인 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="b700b-145">**추가** 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-145">Click the **Add** button.</span></span> <span data-ttu-id="b700b-146">**서비스 추가** 대화 상자에서 **사용자 또는 컴퓨터**를 클릭 한 다음 앱-V 데이터 저장소가 있는 Microsoft SQL server의 이름을 찾아보거나 입력 하 고 IIS에서 사용자 자격 증명을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="b700b-147">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-147">Click **OK**.</span></span>

7.  <span data-ttu-id="b700b-148">**사용 가능한 서비스** 목록에서 Microsoft SQL Server가 app-v 데이터베이스에 대 한 연결을 허용 하는 포트 번호를 나열 하는 MSSQLSvc 서비스 (기본 포트는 1433)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="b700b-149">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-149">Click **OK**.</span></span>

### <span data-ttu-id="b700b-150">제한 된 위임을 위해 IIS 7을 구성 하는 추가 단계</span><span class="sxs-lookup"><span data-stu-id="b700b-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="b700b-151">IIS 7 서버에서 관리 웹 서비스를 실행 하는 경우에는 다음 단계를 완료 하 여 IIS 7 *Useapppoolcredentials* 변수를 True로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="b700b-152">관리자 권한 명령 프롬프트 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="b700b-153">관리자 권한 명령 프롬프트 창을 열려면 **시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **보조 프로그램**을 클릭 하 고 **명령 프롬프트**를 마우스 오른쪽 단추로 클릭 한 다음 **관리자 권한으로 실행**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="b700b-154">%Windir%\\system32\\inetsrv.로 이동</span><span class="sxs-lookup"><span data-stu-id="b700b-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="b700b-155">**appcmd.exe 설정 구성 섹션: system.webserver/security/authentication/windowsAuthentication-useAppPoolCredentials: true**를 입력 한 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="b700b-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





