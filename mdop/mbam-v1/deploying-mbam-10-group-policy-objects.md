---
title: MBAM 1.0 그룹 정책 개체 배포
description: MBAM 1.0 그룹 정책 개체 배포
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821218"
---
# <span data-ttu-id="d8eaa-103">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="d8eaa-103">Deploying MBAM 1.0 Group Policy Objects</span></span>


<span data-ttu-id="d8eaa-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 먼저 MBAM 구현에 사용할 그룹 정책을 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of MBAM.</span></span> <span data-ttu-id="d8eaa-105">사용할 수 있는 다양 한 정책에 대 한 자세한 내용은 [MBAM 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="d8eaa-106">사용할 정책을 결정 한 경우 mbam 1.0 그룹 정책 템플릿을 사용 하 여 MBAM 정책 설정을 포함 하는 하나 이상의 GPO (그룹 정책 개체)를 만들고 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-106">When you have determined the policies that you are going to use, you must use the MBAM 1.0 Group Policy template to create and deploy one or more Group Policy objects (GPO) that include the MBAM policy settings.</span></span>

## <span data-ttu-id="d8eaa-107">MBAM 1.0 그룹 정책 서식 파일 설치</span><span class="sxs-lookup"><span data-stu-id="d8eaa-107">Install the MBAM 1.0 Group Policy template</span></span>


<span data-ttu-id="d8eaa-108">MBAM의 서버 관련 기능을 제공 하는 것 외에도 서버 설정 응용 프로그램에는 MBAM 그룹 정책 서식 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-108">In addition to providing server-related features of MBAM, the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="d8eaa-109">GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 컴퓨터에이 서식 파일을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-109">You can install this template on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

[<span data-ttu-id="d8eaa-110">MBAM 1.0 그룹 정책 템플릿을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="d8eaa-110">How to Install the MBAM 1.0 Group Policy Template</span></span>](how-to-install-the-mbam-10-group-policy-template.md)

## <span data-ttu-id="d8eaa-111">MBAM 1.0 그룹 정책 설정 배포</span><span class="sxs-lookup"><span data-stu-id="d8eaa-111">Deploy MBAM 1.0 Group Policy settings</span></span>


<span data-ttu-id="d8eaa-112">필요한 Gpo를 만든 후에는 조직의 클라이언트 컴퓨터에 MBAM 그룹 정책 설정을 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-112">After you create the necessary GPOs, you must deploy the MBAM Group Policy settings to your organization’s client computers.</span></span>

[<span data-ttu-id="d8eaa-113">MBAM 1.0 GPO 설정을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="d8eaa-113">How to Edit MBAM 1.0 GPO Settings</span></span>](how-to-edit-mbam-10-gpo-settings.md)

## <span data-ttu-id="d8eaa-114">Windows에서 MBAM 제어판을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-114">Display the MBAM Control Panel in Windows</span></span>


<span data-ttu-id="d8eaa-115">MBAM은 기본 Windows BitLocker 제어판을 바꿀 수 있는 사용자 지정 된 MBAM 제어판을 제공 하기 때문에 그룹 정책을 사용 하 여 최종 사용자의 기본 BitLocker 제어판을 숨기도록 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-115">Because MBAM offers a customized MBAM control panel that can replace the default Windows BitLocker control panel, you can also choose to hide the default BitLocker Control Panel from end users by using Group Policy.</span></span>

[<span data-ttu-id="d8eaa-116">Windows 제어판에서 기본 BitLocker 암호화를 숨기는 방법</span><span class="sxs-lookup"><span data-stu-id="d8eaa-116">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## <span data-ttu-id="d8eaa-117">MBAM 1.0 그룹 정책 개체 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="d8eaa-117">Other resources for deploying MBAM 1.0 Group Policy Objects</span></span>


[<span data-ttu-id="d8eaa-118">MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="d8eaa-118">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





