---
title: AGPM에 대한 전자 메일 보안 구성
description: AGPM에 대한 전자 메일 보안 구성
author: dansimp
ms.assetid: b9c48894-0a10-4d03-8027-50ed3b02485a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a384c2a21f912ca7ec55a5e4c74ca7062bfe864c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818993"
---
# <span data-ttu-id="f0893-103">AGPM에 대한 전자 메일 보안 구성</span><span class="sxs-lookup"><span data-stu-id="f0893-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="f0893-104">기본적으로 AGPM (고급 그룹 정책 관리)의 작업으로 인해 전송 되는 전자 메일 알림은 암호화 되지 않고 SMTP 포트 25를 통해 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="f0893-105">그러나 레지스트리 설정을 사용 하 여 SSL (Secure Sockets Layer) 암호화를 사용할지 여부와 사용할 SMTP 포트를 지정 하 여 AGPM에 대 한 전자 메일 보안을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="f0893-106">AGPM 전자 메일 알림을 암호화 하 여 조직의 보안에 대 한 중요 한 정보를 표시할 수 있는 보호 기능을 보다 효과적으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="f0893-107">원격 메일 서버를 통해 릴레이 되는 경우 전자 메일 알림을 암호화 하는 것이 좋으며, 일부 준수 규정이 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="f0893-108">**주의**  사항 레지스트리를 잘못 편집 하면 시스템에 심각한 손상을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="f0893-109">레지스트리를 변경 하기 전에 컴퓨터에 있는 중요 한 데이터를 백업 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="f0893-110">AGPM 관리자 (전체 제어) 역할을 갖는 사용자 계정, 이러한 절차에 사용 되는 GPO (그룹 정책 개체)를 만든 승인자의 사용자 계정 또는이 절차를 완료 하는 데 AGPM에서 필요한 사용 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="f0893-111">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0893-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f0893-112">그룹 정책 기본 설정을 사용 하 여 AGPM 용 전자 메일 보안 구성</span><span class="sxs-lookup"><span data-stu-id="f0893-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="f0893-113">**그룹 정책 관리 콘솔** 트리에서 전자 메일 보안을 구성 하려는 모든 AGPM 서버에 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="f0893-114">(자세한 내용은 [GPO 편집](editing-a-gpo-agpm40.md)을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="f0893-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="f0893-115">**그룹 정책 관리 편집기** 창에서 **컴퓨터 구성**, **기본 설정**, **Windows 설정**, **레지스트리** 폴더를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="f0893-116">콘솔 트리에서 **레지스트리**를 마우스 오른쪽 단추로 클릭 하 고 **새로 만들기**, **모음 항목**, **AGPM 전자 메일 보안**을 차례로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="f0893-117">레지스트리 기본 설정 항목을 만들어 암호화를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="f0893-118">콘솔 트리에서 **AGPM 전자 메일 보안**을 마우스 오른쪽 단추로 클릭 하 고 **새로 만들기**를 가리킨 다음 **레지스트리 항목**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="f0893-119">**새 레지스트리 속성** 대화 상자에서 **업데이트** 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="f0893-120">**하이브에서** **HKEY \ _LOCAL \ _MACHINE**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="f0893-121">**키 경로**에 **SOFTWARE\\Microsoft\\AGPM**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="f0893-122">**값 이름**에 **EncryptSmtp**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="f0893-123">**값 형식**에서 **REG \ _DWORD**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="f0893-124">**Base**의 경우 **10 진수**를 선택 하 고, **값 데이터**의 경우 **1** 을 입력 하 여 SSL 암호화를 사용 하 고, **0** 은 암호화 하지 않고 전자 메일을 보낼 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="f0893-125">기본적으로 전자 메일은 암호화 되지 않은 상태로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-125">By default, e-mail is sent without encryption.</span></span> <span data-ttu-id="f0893-126">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-126">Click **OK**.</span></span>

5.  <span data-ttu-id="f0893-127">다음과 같이 SMTP 포트를 지정 하는 레지스트리 기본 설정 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="f0893-128">콘솔 트리에서 **AGPM 전자 메일 보안**을 마우스 오른쪽 단추로 클릭 하 고 **새로 만들기**를 가리킨 다음 **레지스트리 항목**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="f0893-129">**새 레지스트리 속성** 대화 상자에서 **업데이트** 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="f0893-130">**하이브에서** **HKEY \ _LOCAL \ _MACHINE**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="f0893-131">**키 경로** 대화 상자에 **SOFTWARE\\Microsoft\\AGPM**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="f0893-132">**값 이름**에 **SmtpPort**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="f0893-133">**값 형식**에서 **REG \ _DWORD**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="f0893-134">**Base**의 경우 **10 진수**를 선택 하 고, **값 데이터**의 경우 SMTP 포트의 포트 번호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="f0893-135">기본적으로 SMTP 포트는 암호화를 사용 하도록 설정 되지 않은 경우 포트 25이 고 SSL 암호화가 설정 된 경우 포트 587입니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span> <span data-ttu-id="f0893-136">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-136">Click **OK**.</span></span>

6.  <span data-ttu-id="f0893-137">**그룹 정책 관리 편집기** 창을 닫은 다음 GPO를 체크 인하고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="f0893-138">자세한 내용은 [GPO 배포](deploy-a-gpo-agpm40.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0893-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="f0893-139">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="f0893-139">Additional considerations</span></span>

-   <span data-ttu-id="f0893-140">그룹 정책 기본 설정을 사용 하 여 구성 된 GPO를 편집 하 고 배포 하는 것이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0893-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="f0893-141">추가 세부 정보는 [Gpo 편집](editing-a-gpo-agpm40.md) 및 [gpo 배포](deploy-a-gpo-agpm40.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0893-141">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="f0893-142">추가 참조</span><span class="sxs-lookup"><span data-stu-id="f0893-142">Additional references</span></span>

-   [<span data-ttu-id="f0893-143">고급 그룹 정책 관리 구성</span><span class="sxs-lookup"><span data-stu-id="f0893-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





