---
title: 서버를 추가하는 방법
description: 서버를 추가하는 방법
author: dansimp
ms.assetid: 1f31678a-8edf-4d35-a812-e4a2abfd979b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d08b79bcbf34910ce357f39635431d11e3e99bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821388"
---
# <span data-ttu-id="fbee0-103">서버를 추가하는 방법</span><span class="sxs-lookup"><span data-stu-id="fbee0-103">How to Add a Server</span></span>


<span data-ttu-id="fbee0-104">응용 프로그램 가상화 관리 서버를 보다 효율적으로 관리 하는 데 도움이 되도록 서버 그룹으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-104">To help you manage your Application Virtualization Management Servers more efficiently, organize them into server groups.</span></span> <span data-ttu-id="fbee0-105">응용 프로그램 가상화 서버 관리 콘솔에서 서버 그룹을 만든 후 다음 절차를 사용 하 여 그룹에 서버를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-105">After you create a server group in the Application Virtualization Server Management Console, you can use the following procedure to add a server to the group.</span></span>

<span data-ttu-id="fbee0-106">**참고**  서버 그룹의 모든 서버는 동일한 데이터 저장소에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-106">**Note** All servers in a server group must be connected to the same data store.</span></span>

 

**<span data-ttu-id="fbee0-107">그룹에 서버를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="fbee0-107">To add a server to a group</span></span>**

1.  <span data-ttu-id="fbee0-108">왼쪽 창에서 **서버 그룹** 노드를 클릭 하 여 서버 그룹 목록을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-108">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="fbee0-109">원하는 서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **새 응용 프로그램 가상화 관리 서버**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-109">Right-click the desired server group, and select **New Application Virtualization Management Server**.</span></span>

3.  <span data-ttu-id="fbee0-110">**새 서버 그룹 마법사**에서 **표시 이름** 및 **DNS 호스트 이름을**입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-110">In the **New Server Group Wizard**, enter the **Display Name** and the **DNS Host Name**.</span></span>

4.  <span data-ttu-id="fbee0-111">서버 캐시에 대 한 **최대 메모리 할당** 필드에 기본값을 유지 하 고 **경고 메모리 할당** 필드에 임계값 경고 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-111">Leave the default values in the **Maximum Memory Allocation** field for the server cache and the **Warn Memory Allocation** field to specify the threshold warning level.</span></span>

5.  <span data-ttu-id="fbee0-112">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-112">Click **Next**.</span></span>

6.  <span data-ttu-id="fbee0-113">필요한 경우 **연결 보안 모드** 대화 상자에서 **고급 보안 사용** 확인란을 선택 하 여 고급 보안 모드를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-113">In the **Connection Security Mode** dialog, check the **Use enhanced security** box to select enhanced security mode, if desired.</span></span> <span data-ttu-id="fbee0-114">필요한 경우 **인증서 마법사** 를 완료 하거나 기존 인증서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-114">If necessary, complete the **Certificate Wizard** or view existing certificates.</span></span>

7.  <span data-ttu-id="fbee0-115">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-115">Click **Next**.</span></span>

8.  <span data-ttu-id="fbee0-116">**App Virt Port 설정** 대화 상자에서 **기본 포트 사용** 또는 **사용자 지정 포트** 라디오 단추를 선택 하 고 사용자 지정 포트 번호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-116">In the **App Virt Port Setting** dialog, select the **Use Default Port** or the **User Custom Port** radio button and enter the custom port number.</span></span>

9.  <span data-ttu-id="fbee0-117">**마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="fbee0-117">Click **Finish**.</span></span>

## <span data-ttu-id="fbee0-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fbee0-118">Related topics</span></span>


[<span data-ttu-id="fbee0-119">서버 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="fbee0-119">How to Create a Server Group</span></span>](how-to-create-a-server-group.md)

[<span data-ttu-id="fbee0-120">서버를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="fbee0-120">How to Remove a Server</span></span>](how-to-remove-a-server.md)

 

 





