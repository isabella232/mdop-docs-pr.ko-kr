---
title: Windows XP에 적합 한 자격 증명을 할당 하는 방법
description: Windows XP에 적합 한 자격 증명을 할당 하는 방법
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819323"
---
# <span data-ttu-id="068c7-103">Windows XP에 적합 한 자격 증명을 할당 하는 방법</span><span class="sxs-lookup"><span data-stu-id="068c7-103">How to Assign the Proper Credentials for Windows XP</span></span>


<span data-ttu-id="068c7-104">적절 한 WindowsXP 자격 증명을 사용 하도록 앱-V 데스크톱 클라이언트를 구성 하려면 다음 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsXP credentials.</span></span>

<span data-ttu-id="068c7-105">**참고**  이 절차를 완료 한 후 도메인에 가입 되지 않은 클라이언트는 도메인에 가입 하지 않고 게시 새로 고침을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-105">**Note** After finishing this procedure, the non-domain joined client can perform a publishing refresh without being joined to a domain.</span></span>

 

**<span data-ttu-id="068c7-106">WindowsXP를 실행 하는 App-v 클라이언트에 대 한 적절 한 자격 증명을 할당 하려면</span><span class="sxs-lookup"><span data-stu-id="068c7-106">To assign the proper credentials for App-V clients running WindowsXP</span></span>**

1.  <span data-ttu-id="068c7-107">WindowsXP를 실행 하는 App-v 클라이언트에 대 한 관리자 권한이 있으면 **사용자 계정** 제어판의 클래식 제어판을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-107">With administrator privileges on the App-V Client running WindowsXP, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="068c7-108">**고급 탭**을 클릭 하 고 **암호 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-108">Click the **Advanced Tab**, and select **Manage Passwords**.</span></span>

3.  <span data-ttu-id="068c7-109">저장 된 **사용자 이름 및 암호** 화면에서 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-109">On the **Stored User Names and Passwords** screen, click **Add**.</span></span>

4.  <span data-ttu-id="068c7-110">**로그온 정보 속성** 화면에서 app-v 인프라의 정보로 다음 필드를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-110">On the **Logon Information Properties** screen, fill out the following fields with information from the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="068c7-111">**서버:** 게시 서버 외부 이름의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-111">**Server:** Name of publishing server external name.</span></span>

    2.  <span data-ttu-id="068c7-112">**사용자 이름:** 양식 Domain\\username. 외부 사용자의 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="068c7-112">**User name:** User name for external user in the form Domain\\username.</span></span>

    3.  <span data-ttu-id="068c7-113">**비밀 번호:** **사용자 이름** 필드에 입력 한 사용자 계정의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-113">**Password:** Password for the user account entered in the **User name** field.</span></span>

5.  <span data-ttu-id="068c7-114">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-114">Click **OK**.</span></span> <span data-ttu-id="068c7-115">자격 증명이 클라이언트에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="068c7-115">The credentials will be stored on the client.</span></span>

## <span data-ttu-id="068c7-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="068c7-116">Related topics</span></span>


[<span data-ttu-id="068c7-117">도메인 가입 및 도메인에 가입되지 않은 클라이언트</span><span class="sxs-lookup"><span data-stu-id="068c7-117">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="068c7-118">Windows Vista에 적합 한 자격 증명을 할당 하는 방법</span><span class="sxs-lookup"><span data-stu-id="068c7-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





