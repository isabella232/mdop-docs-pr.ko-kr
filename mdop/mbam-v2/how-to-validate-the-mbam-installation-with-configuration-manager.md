---
title: Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법
description: Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822638"
---
# <span data-ttu-id="f75d2-103">Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법</span><span class="sxs-lookup"><span data-stu-id="f75d2-103">How to Validate the MBAM Installation with Configuration Manager</span></span>


<span data-ttu-id="f75d2-104">Configuration Manager와 함께 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치한 후 다음 단계를 완료 하 여 해당 설치가 MBAM에 대해 필요한 모든 기능을 성공적으로 설정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-104">After installing Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, validate that the installation has successfully set up all the necessary features for MBAM by completing the following steps.</span></span>

**<span data-ttu-id="f75d2-105">구성 관리자를 사용 하 여 MBAM 서버 기능 설치의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="f75d2-105">To validate the MBAM Server feature installation with Configuration Manager</span></span>**

1.  <span data-ttu-id="f75d2-106">System Center Configuration Manager를 배포 하는 서버에서 **제어판**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-106">On the server where System Center Configuration Manager is deployed, open **Control Panel**.</span></span> <span data-ttu-id="f75d2-107">프로그램을 제거 하거나 변경 하는 데 사용 되는 프로그램을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-107">Select the program that is used to uninstall or change a program.</span></span> <span data-ttu-id="f75d2-108">**Microsoft BitLocker 관리 및 모니터링** 이 프로그램 및 기능 목록에 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-108">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the list of programs and features.</span></span>

    <span data-ttu-id="f75d2-109">**참고**  설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-109">**Note** To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

     

2.  <span data-ttu-id="f75d2-110">Configuration Manager 콘솔을 사용 하 여 "MBAM 지원 컴퓨터" 라는 새 컬렉션이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-110">Use the Configuration Manager console to confirm that a new collection, called “MBAM Supported Computers,” is displayed.</span></span>

    <span data-ttu-id="f75d2-111">Configuration Manager 2007에서 컬렉션을 보려면 **사이트 데이터베이스** ( &lt; **SiteCode** &gt;  -  &lt; **ServerName** &gt; , &lt; **SiteName** &gt; ), **컴퓨터 관리**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-111">To view the collection with Configuration Manager 2007: Click **Site Database** (&lt;**SiteCode**&gt; - &lt;**ServerName**&gt;, &lt;**SiteName**&gt;), **Computer Management**.</span></span>

    <span data-ttu-id="f75d2-112">SystemCenter2012 ConfigurationManager를 사용 하 여 컬렉션을 보려면 다음을 수행 합니다. **자산 및 준수** 작업 영역, **장치 모음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-112">To view the collection with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Device Collections**.</span></span>

3.  <span data-ttu-id="f75d2-113">Configuration Manager 콘솔을 사용 하 여 다음 보고서가 **Mbam** 폴더에 나열 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-113">Use the Configuration Manager console to verify that the following reports are listed in the **MBAM** folder:</span></span>

    -   <span data-ttu-id="f75d2-114">BitLocker 컴퓨터 준수</span><span class="sxs-lookup"><span data-stu-id="f75d2-114">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="f75d2-115">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="f75d2-115">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="f75d2-116">BitLocker 엔터프라이즈 준수 세부 정보</span><span class="sxs-lookup"><span data-stu-id="f75d2-116">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="f75d2-117">BitLocker Enterprise 규정 준수 요약</span><span class="sxs-lookup"><span data-stu-id="f75d2-117">BitLocker Enterprise Compliance Summary</span></span>

    <span data-ttu-id="f75d2-118">구성 관리자 2007를 사용 하 여 보고서를 보려면 **reporting**, **reporting Services**, \\ \ \ &lt; **서버 이름** &gt; , **보고서 폴더** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-118">To view the reports with Configuration Manager 2007: Click **Reporting**, **Reporting Services**, \\\\&lt;**ServerName**&gt;, **Report Folders**</span></span>

    <span data-ttu-id="f75d2-119">SystemCenter2012 ConfigurationManager를 사용 하 여 보고서를 보려면 **모니터링** 작업 영역, **보고**, **보고서**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-119">To view the reports with SystemCenter2012 ConfigurationManager: Click the **Monitoring** workspace, **Reporting**, **Reports**.</span></span>

4.  <span data-ttu-id="f75d2-120">Configuration Manager 콘솔을 사용 하 여 구성 기준 "BitLocker Protection"이 나열 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-120">Use the Configuration Manager console to confirm that the configuration baseline “BitLocker Protection” is listed.</span></span>

    <span data-ttu-id="f75d2-121">구성 관리자 2007를 사용 하 여 구성 기준을 보려면 **원하는 구성 관리**, **구성 기준을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-121">To view the configuration baselines with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Baselines**.</span></span>

    <span data-ttu-id="f75d2-122">SystemCenter2012 ConfigurationManager를 사용 하 여 구성 기준을 보려면 **자산 및 준수** 작업 영역, **준수 설정**, **구성 기준을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-122">To view the configuration baselines with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Baselines**.</span></span>

5.  <span data-ttu-id="f75d2-123">Configuration Manager 콘솔을 사용 하 여 다음과 같은 새 구성 항목이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-123">Use the Configuration Manager console to confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="f75d2-124">BitLocker 고정 데이터 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="f75d2-124">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="f75d2-125">BitLocker 운영 체제 드라이브 보호</span><span class="sxs-lookup"><span data-stu-id="f75d2-125">BitLocker Operating System Drive Protection</span></span>

    <span data-ttu-id="f75d2-126">구성 관리자 2007를 사용 하 여 구성 항목을 보려면 **원하는 구성 관리**인 **구성 항목**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-126">To view the configuration items with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Items**.</span></span>

    <span data-ttu-id="f75d2-127">SystemCenter2012 ConfigurationManager를 사용 하 여 구성 항목을 보려면 **자산 및 준수** 작업 영역, **준수 설정**, **구성 항목**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f75d2-127">To view the configuration items with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Items**.</span></span>

## <span data-ttu-id="f75d2-128">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f75d2-128">Related topics</span></span>


[<span data-ttu-id="f75d2-129">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="f75d2-129">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





