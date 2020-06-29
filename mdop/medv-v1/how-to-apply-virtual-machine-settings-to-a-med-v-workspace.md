---
title: MED-V 작업 영역에 가상 컴퓨터 설정을 적용하는 방법
description: MED-V 작업 영역에 가상 컴퓨터 설정을 적용하는 방법
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825973"
---
# <span data-ttu-id="ba2e8-103">MED-V 작업 영역에 가상 컴퓨터 설정을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="ba2e8-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="ba2e8-104">모든 MED-V 작업 영역에는 Microsoft 가상 PC 이미지가 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="ba2e8-105">가상 컴퓨터 설정을 사용 하면 가상 PC 이미지를 할당할 수 있을 뿐만 아니라 다른 가상 컴퓨터 속성을 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="ba2e8-106">모든 가상 컴퓨터 설정은 **정책** 모듈의 **가상 컴퓨터 설정** 탭에서 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="ba2e8-107">MED-V 작업 영역에 가상 컴퓨터 설정을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="ba2e8-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="ba2e8-108">MED-V 작업 영역을 클릭 하 여 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="ba2e8-109">다음 표에 설명 된 대로 가상 컴퓨터 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="ba2e8-110">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="ba2e8-111">가상 컴퓨터 속성</span><span class="sxs-lookup"><span data-stu-id="ba2e8-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="ba2e8-112">속성 설명 *가상 컴퓨터 설정*</span><span class="sxs-lookup"><span data-stu-id="ba2e8-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="ba2e8-113">할당 된 이미지</span><span class="sxs-lookup"><span data-stu-id="ba2e8-113">Assigned Image</span></span>

<span data-ttu-id="ba2e8-114">MED-V 작업 영역에 할당 된 실제 Microsoft 가상 PC 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="ba2e8-115">메뉴에는 사용 가능한 모든 가상 PC 이미지 목록이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="ba2e8-116">**활성** 이미지 목록에는 다음과 같은 이미지 종류가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="ba2e8-117">**로컬 테스트 이미지**-아직 압축 되지 않은 로컬 컴퓨터의 이미지</span><span class="sxs-lookup"><span data-stu-id="ba2e8-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="ba2e8-118">이러한 이미지 이름 다음에는 괄호 (테스트)의 "test" 라는 단어가 오며 테스트 목적 으로만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="ba2e8-119">**로컬 컴퓨터**에 압축 된 이미지</span><span class="sxs-lookup"><span data-stu-id="ba2e8-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="ba2e8-120">이러한 이미지 다음에는 괄호 (로컬)의 "local" 이라는 단어가 오며, 관리자가 서버에 업로드할 때까지 클라이언트가 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="ba2e8-121">이동식 미디어 (예: USB 또는 DVD)를 통해 클라이언트에 배포 되는 패키지를 만드는 경우 로컬 이미지를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="ba2e8-122">서버 **에 압축 된 이미지**-서버에 있고 클라이언트가 다운로드할 수 있는 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="ba2e8-123">새로 고침을 클릭 하 여 이미지 목록을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="ba2e8-124">**참고**  각 MED-V 작업 영역 이미지는 한 Windows 사용자만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="ba2e8-125">작업 영역이 영구적입니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-125">Workspace is persistent</span></span>

<span data-ttu-id="ba2e8-126">MED-V 작업 영역을 영구적으로 구성 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="ba2e8-127">영구 MED-V 작업 영역에서 MED-V 작업 영역을 중지할 때 MED-V 작업 영역에 대 한 변경 및 추가 내용이 MED-V 작업 영역에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="ba2e8-128">도메인 MED-V 작업 영역의 경우이 옵션을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="ba2e8-129">**참고**  MED-V 작업 영역이 사용자에 게 배포 된 후에는이 설정을 변경 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="ba2e8-130">작업 영역을 중지할 때 VM 종료</span><span class="sxs-lookup"><span data-stu-id="ba2e8-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="ba2e8-131">MED-V 작업 영역을 중지할 때 가상 컴퓨터를 종료 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="ba2e8-132">이 확인란을 선택 취소 하면 각 세션이 완료 될 때 가상 머신이 종료 되지 않고 가상 컴퓨터의 스냅샷이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="ba2e8-133">새 세션이 시작 되 면 Windows가 스냅숏에서 시작 됩니다 (즉, Windows는 다시 시작 되지 않으며 로그인이 필요 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="ba2e8-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="ba2e8-134">**참고**  이 속성은 **작업 영역이 영구적** 으로 선택 된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="ba2e8-135">SSO (MED-V 자격 증명)를 사용 하 여 VM의 Windows에 로그온</span><span class="sxs-lookup"><span data-stu-id="ba2e8-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="ba2e8-136">MED-V 클라이언트에 로그인 할 때 입력 하는 MED-V 자격 증명을 사용 하 여 가상 컴퓨터에 Windows에 로그인 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="ba2e8-137">**참고**  이 속성은 **작업 영역이 영구적** 으로 선택 된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="ba2e8-138">작업 영역을 revertible</span><span class="sxs-lookup"><span data-stu-id="ba2e8-138">Workspace is revertible</span></span>

<span data-ttu-id="ba2e8-139">MED-V 작업 영역을 revertible로 구성 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="ba2e8-140">Revertible MED-V 작업 영역에서 각 세션이 완료 되 면 (즉, 사용자가 MED-V 작업 영역을 중지할 때) MED-V 작업 영역이 배포 중에 있던 원래 상태로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="ba2e8-141">사용자가 변경한 내용이 나 추가 사항은 세션 간에 MED-V 작업 영역에 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="ba2e8-142">**참고**  MED-V 작업 영역이 사용자에 게 배포 된 후에는이 설정을 변경 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="ba2e8-143">호스트와 작업 영역 표준 시간대 동기화</span><span class="sxs-lookup"><span data-stu-id="ba2e8-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="ba2e8-144">MED-V 작업 영역의 표준 시간대를 호스트와 동기화 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="ba2e8-145">동기화는 다음과 같이 MED-V 작업 영역이 영구 인지 아니면 revertible에 따라 다르게 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="ba2e8-146">영구 MED-V 작업 영역에서 표준 시간대는 먼저 서버와 동기화 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="ba2e8-147">이 작업에 실패 하면 호스트와 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="ba2e8-148">Revertible MED-V 작업 영역에서 표준 시간대는 호스트와 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="ba2e8-149">잠금 설정</span><span class="sxs-lookup"><span data-stu-id="ba2e8-149">Lock Settings</span></span>*

<span data-ttu-id="ba2e8-150">호스트 대기/최대 절전 모드 이벤트에서 작업 영역 잠금</span><span class="sxs-lookup"><span data-stu-id="ba2e8-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="ba2e8-151">이 확인란을 선택 하면 호스트 컴퓨터가 대기 모드나 최대 절전 모드로 전환할 때 MED-V 작업 영역이 자동으로 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="ba2e8-152">후에 작업 영역 잠금</span><span class="sxs-lookup"><span data-stu-id="ba2e8-152">Lock the Workspace after</span></span>

<span data-ttu-id="ba2e8-153">지정 된 시간 동안 MED-V 작업 영역이 유휴 상태일 때 MED-V 작업 영역을 잠그려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="ba2e8-154">이 확인란을 선택 하면 번호 상자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="ba2e8-155">MED-V 작업 영역을 잠그기 전 까지의 유휴 시간 (분)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="ba2e8-156">**참고**  유휴 시간은 MED-V 작업 영역 응용 프로그램 (호스트 응용 프로그램이 아님)을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="ba2e8-157">이미지 업데이트 설정</span><span class="sxs-lookup"><span data-stu-id="ba2e8-157">Image Update Settings</span></span>*

<span data-ttu-id="ba2e8-158">유지</span><span class="sxs-lookup"><span data-stu-id="ba2e8-158">Keep only</span></span>

<span data-ttu-id="ba2e8-159">유지할 이전 이미지 버전의 수를 제한 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="ba2e8-160">이 확인란을 선택 하면 번호 상자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="ba2e8-161">유지할 이전 버전 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="ba2e8-162">새 버전을 사용할 수 있는 경우 업데이트 제안</span><span class="sxs-lookup"><span data-stu-id="ba2e8-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="ba2e8-163">새 버전의 이미지를 사용할 수 있는 경우 업데이트를 제안 (강요 하지는 않음) 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="ba2e8-164">클라이언트가이 작업 영역에 대 한 이미지를 다운로드할 때 트리밍 전송을 사용 해야 함</span><span class="sxs-lookup"><span data-stu-id="ba2e8-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="ba2e8-165">이 MED-V 작업 영역과 관련 된 이미지를 다운로드 하는 경우 트리밍 이전 (자세한 내용은 [Med-v 자르기 전환 기술](med-v-trim-transfer-technology-medvv2.md)참조)을 사용 하도록 설정 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="ba2e8-166">이 확인란의 선택을 취소 하면 전체 이미지가 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="ba2e8-167">**참고**  Trim Transfer에서는 하드 드라이브의 인덱싱이 필요 하며,이는 시간이 오래 걸릴 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="ba2e8-168">하드 드라이브 인덱싱이 기존 버전과 유사한 이미지 버전을 다운로드 하는 경우와 같이 새 이미지 버전을 다운로드 하는 것 보다 더 효율적일 때 트리밍 전송을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ba2e8-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="ba2e8-169">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ba2e8-169">Related topics</span></span>


[<span data-ttu-id="ba2e8-170">MED-V 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="ba2e8-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="ba2e8-171">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="ba2e8-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="ba2e8-172">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="ba2e8-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





