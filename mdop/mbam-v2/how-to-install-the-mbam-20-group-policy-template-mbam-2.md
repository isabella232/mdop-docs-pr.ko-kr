---
title: MBAM 2.0 그룹 정책 템플릿을 설치하는 방법
description: MBAM 2.0 그룹 정책 템플릿을 설치하는 방법
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826253"
---
# <span data-ttu-id="472ec-103">MBAM 2.0 그룹 정책 템플릿을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="472ec-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="472ec-104">서버와 관련 된 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능 외에도, 서버 설정 응용 프로그램에는 Microsoft BitLocker 관리 및 모니터링 그룹 정책 서식 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="472ec-105">이 서식 파일은 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행 하는 모든 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="472ec-106">다음 단계에서는 MBAM 그룹 정책 템플릿을 설치 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="472ec-107">**참고**  32 비트 서버와 64 비트 서버에서 64 비트 설정으로 32 비트 설치를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="472ec-108">MBAM 그룹 정책 서식 파일을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="472ec-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="472ec-109">MBAM을 설치 하려는 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="472ec-110">**시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="472ec-111">Microsoft 소프트웨어 사용 조건을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="472ec-112">기본적으로 모든 Microsoft BitLocker 관리 및 모니터링 기능이 설치 되도록 선택 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="472ec-113">**정책 템플릿을**제외한 모든 기능 옵션의 선택을 취소 하 고 **다음** 을 클릭 하 여 설치를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="472ec-114">**참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="472ec-115">모든 필수 조건이 충족 되 면 설치가 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="472ec-116">누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="472ec-117">모든 전제 조건을 충족 하면 설치가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="472ec-118">서식 파일을 설치 하는 방법 및 위치에 대 한 구체적인 단계는 [MDOP 그룹 정책 (admx) 템플릿을 다운로드 하 고 배포 하는 방법을](https://technet.microsoft.com/library/dn659707.aspx)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="472ec-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="472ec-119">Microsoft BitLocker 관리 및 모니터링 설정 마법사가 선택한 기능에 대 한 설치 페이지를 표시 한 후 **마침을** 클릭 하 여 Mbam 설정을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="472ec-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="472ec-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="472ec-120">Related topics</span></span>


[<span data-ttu-id="472ec-121">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="472ec-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





