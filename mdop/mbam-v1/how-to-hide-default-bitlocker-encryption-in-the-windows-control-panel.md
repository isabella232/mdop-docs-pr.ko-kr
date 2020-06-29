---
title: Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법
description: Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824508"
---
# <span data-ttu-id="0e334-103">Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법</span><span class="sxs-lookup"><span data-stu-id="0e334-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="0e334-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 암호화 옵션 이라고 하는 MBAM 클라이언트 컴퓨터에 대해 사용자 지정 제어판을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="0e334-105">이 사용자 지정 제어판은 BitLocker 드라이브 암호화 라는 기본 Windows BitLocker 제어판을 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="0e334-106">Windows 제어판의 시스템 및 보안 아래에 있는 BitLocker 암호화 옵션 제어판은 사용자가 PIN 및 암호를 관리 하 고, 드라이브 잠금을 해제 하 고, 관리자가 드라이브를 해독 하거나 BitLocker 암호화를 일시 중단 하거나 다시 시작할 수 있는 인터페이스를 숨길 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="0e334-107">Windows 제어판에서 기본 BitLocker 암호화를 숨기려면</span><span class="sxs-lookup"><span data-stu-id="0e334-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="0e334-108">GPMC (그룹 정책 관리 콘솔), AGPM (고급 그룹 정책 관리) 또는 BitLocker 그룹 정책 컴퓨터의 로컬 그룹 정책 편집기를 사용 하 여 **사용자 구성을** 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="0e334-109">**정책을**클릭 하 고 **관리 템플릿을**선택한 다음 **제어판**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="0e334-110">**세부 정보** 창에서 **지정 된 제어판 항목 숨기기**를 두 번 클릭 한 다음 **사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="0e334-111">**표시**를 클릭 하 고 **추가 ...를 클릭**한 다음 Microsoft. Bitlocker드라이브 암호화를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="0e334-112">이 정책은 windows 제어판에서 기본 Windows BitLocker 관리 도구를 숨기고 사용자가 Windows 제어판에서 업데이트 된 MBAM BitLocker 암호화 옵션 도구를 열 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e334-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="0e334-113">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0e334-113">Related topics</span></span>


[<span data-ttu-id="0e334-114">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="0e334-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





