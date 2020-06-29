---
title: MBAM 1.0 그룹 정책 템플릿을 설치하는 방법
description: MBAM 1.0 그룹 정책 템플릿을 설치하는 방법
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825338"
---
# <span data-ttu-id="66320-103">MBAM 1.0 그룹 정책 템플릿을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="66320-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="66320-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)의 서버 관련 기능 외에도 서버 설정 응용 프로그램에는 MBAM 그룹 정책 서식 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66320-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="66320-105">GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 컴퓨터에이 서식 파일을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66320-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="66320-106">다음 단계에서는 MBAM 그룹 정책 템플릿을 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="66320-107">**참고**  32 비트 서버와 64 비트 서버에서 64 비트 설정으로 32 비트 설치를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="66320-108">MBAM 그룹 정책 서식 파일을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="66320-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="66320-109">MBAM 설치 마법사를 시작 합니다. 시작 페이지에서 **설치** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="66320-110">Microsoft 소프트웨어 사용 조건을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="66320-111">기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66320-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="66320-112">**정책 템플릿을**제외한 모든 기능 옵션의 선택을 취소 하 고 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="66320-113">**참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="66320-114">모든 필수 조건이 충족 되 면 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66320-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="66320-115">누락 된 필수 조건이 발견 되 면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66320-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="66320-116">모든 전제 조건을 충족 하면 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66320-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="66320-117">MBAM 설정 마법사가 선택한 기능에 대 한 설치 페이지를 표시 한 후 **마침을** 클릭 하 여 mbam 설정을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="66320-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="66320-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="66320-118">Related topics</span></span>


[<span data-ttu-id="66320-119">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="66320-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





