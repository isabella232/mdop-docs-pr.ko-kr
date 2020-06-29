---
title: MBAM 2.5 그룹 정책 개체 배포
description: MBAM 2.5 그룹 정책 개체 배포
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824388"
---
# <span data-ttu-id="16d5f-103">MBAM 2.5 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="16d5f-103">Deploying MBAM 2.5 Group Policy Objects</span></span>


<span data-ttu-id="16d5f-104">MBAM을 배포 하려면 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-104">To deploy MBAM, you have to set Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="16d5f-105">이 작업을 완료 하려면 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 실행할 수 있는 서버 또는 워크스테이션에 MBAM 그룹 정책 템플릿을 복사한 다음 설정을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-105">To complete this task, you must copy the MBAM Group Policy Templates to a server or workstation that are capable of running Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM), and then edit the settings.</span></span>

<span data-ttu-id="16d5f-106">**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-106">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="16d5f-107">**MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-107">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

## <span data-ttu-id="16d5f-108">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="16d5f-108">Copying the MBAM 2.5 Group Policy Templates</span></span>


<span data-ttu-id="16d5f-109">MBAM 클라이언트를 설치 하기 전에, 관리 워크스테이션에 MBAM Gpo (그룹 정책 개체)를 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-109">Before you install the MBAM Client, you must copy MBAM-specific Group Policy Objects (GPOs) to the Management Workstation.</span></span> <span data-ttu-id="16d5f-110">이러한 Gpo는 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-110">These GPOs define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="16d5f-111">그룹 정책 템플릿을 지원 되는 Windows server 또는 클라이언트 컴퓨터인 모든 서버 또는 워크스테이션에 복사 하 여 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-111">You can copy the Group Policy templates to any server or workstation that is a supported Windows server or client computer and that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="16d5f-112">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="16d5f-112">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

## <span data-ttu-id="16d5f-113">MBAM 2.0 GPO 설정 편집</span><span class="sxs-lookup"><span data-stu-id="16d5f-113">Editing MBAM 2.0 GPO settings</span></span>


<span data-ttu-id="16d5f-114">필요한 Gpo를 만든 후에는 조직의 클라이언트 컴퓨터에 MBAM 그룹 정책 설정을 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-114">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span> <span data-ttu-id="16d5f-115">Gpo를 보고 만들려면 GPMC (그룹 정책 관리) 콘솔 또는 AGPM (고급 그룹 정책 관리)이 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-115">To view and create GPOs, you must have Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM) installed.</span></span>

[<span data-ttu-id="16d5f-116">MBAM 2.5 그룹 정책 설정 편집</span><span class="sxs-lookup"><span data-stu-id="16d5f-116">Editing the MBAM 2.5 Group Policy Settings</span></span>](editing-the-mbam-25-group-policy-settings.md)

## <span data-ttu-id="16d5f-117">Windows 제어판에서 MBAM 제어판 표시 또는 숨기기</span><span class="sxs-lookup"><span data-stu-id="16d5f-117">Showing or hiding the MBAM Control Panel in Windows Control Panel</span></span>


<span data-ttu-id="16d5f-118">MBAM은 기본 Windows BitLocker 제어판을 바꿀 수 있는 사용자 지정 된 MBAM 제어판을 제공 하므로 그룹 정책 설정을 사용 하 여 최종 사용자의 기본 BitLocker 제어판을 표시 하거나 숨길 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-118">Since MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to show or hide the default BitLocker Control Panel from end users by using Group Policy settings.</span></span>

[<span data-ttu-id="16d5f-119">제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기</span><span class="sxs-lookup"><span data-stu-id="16d5f-119">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## <span data-ttu-id="16d5f-120">MBAM 2.0 그룹 정책 개체 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="16d5f-120">Other Resources for deploying MBAM 2.0 Group Policy Objects</span></span>


[<span data-ttu-id="16d5f-121">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="16d5f-121">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

## <span data-ttu-id="16d5f-122">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="16d5f-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="16d5f-123">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="16d5f-124">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16d5f-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





