---
title: Windows Vista에 적합 한 자격 증명을 할당 하는 방법
description: Windows Vista에 적합 한 자격 증명을 할당 하는 방법
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821368"
---
# <span data-ttu-id="536cc-103">Windows Vista에 적합 한 자격 증명을 할당 하는 방법</span><span class="sxs-lookup"><span data-stu-id="536cc-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="536cc-104">다음 절차를 사용 하 여 올바른 WindowsVista 자격 증명을 사용할 수 있도록 App-v 데스크톱 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="536cc-105">**참고**  이 절차는 비도메인에 연결 된 각 컴퓨터에서 완료 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="536cc-106">환경에서 도메인에 연결 되지 않은 컴퓨터 수에 따라 매우 지루한 작업을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="536cc-107">스크립트와 자격 증명 관리자의 명령줄 인터페이스를 사용 하 여 관리자가이 프로세스를 자동화 하는 데 도움을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="536cc-108">Windows Vista를 실행 하는 App-v 클라이언트에 대 한 적절 한 자격 증명을 할당 하려면</span><span class="sxs-lookup"><span data-stu-id="536cc-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="536cc-109">Windows Vista를 실행 하는 App-v 데스크톱 클라이언트에 대 한 관리자 권한이 있으면 **사용자 계정** 제어판의 클래식 제어판을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="536cc-110">왼쪽 작업 창의 **사용자 계정** 에서 **네트워크 암호 관리** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="536cc-111">**저장 된 사용자 이름 및 암호** 화면에서 **추가** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="536cc-112">**저장 된 자격 증명 속성** 화면에서 앱-V 인프라에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="536cc-113">**로그온 대상:** 게시 서버의 외부 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="536cc-114">**사용자 이름:** 양식 Domain\\Username. 외부 사용자의 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="536cc-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="536cc-115">**비밀 번호:** **사용자 이름** 필드에 입력 한 사용자 계정의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="536cc-116">**자격 증명 유형** 유지를 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="536cc-117">**닫기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-117">Click **Close**.</span></span> <span data-ttu-id="536cc-118">자격 증명은 앱 V 인프라에 대 한 적절 한 인증을 위해 자격 증명 저장소에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="536cc-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="536cc-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="536cc-119">Related topics</span></span>


[<span data-ttu-id="536cc-120">도메인 가입 및 도메인에 가입되지 않은 클라이언트</span><span class="sxs-lookup"><span data-stu-id="536cc-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="536cc-121">Windows XP에 적합 한 자격 증명을 할당 하는 방법</span><span class="sxs-lookup"><span data-stu-id="536cc-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





