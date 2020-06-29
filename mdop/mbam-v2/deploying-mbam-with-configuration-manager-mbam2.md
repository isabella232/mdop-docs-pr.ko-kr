---
title: Configuration Manager에서 MBAM 배포
description: Configuration Manager에서 MBAM 배포
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823453"
---
# <span data-ttu-id="ad1ca-103">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="ad1ca-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="ad1ca-104">다음 절차에서는 microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager을 사용 하 여 microsoft BitLocker 관리 및 모니터링 (MBAM)을 배포 하는 방법을 설명 [합니다. usingthe](getting-started---using-mbam-with-configuration-manager.md)권장 구성</span><span class="sxs-lookup"><span data-stu-id="ad1ca-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="ad1ca-105">권장 되는 구성은 하나 이상의 Microsoft BitLocker 관리 및 모니터링 서버에 관리 및 모니터링 기능을 설치 하 고 별도의 서버에 Microsoft System Center Configuration Manager 2007 또는 MicrosoftSystemCenter2012 ConfigurationManager를 설치 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="ad1ca-106">설치를 시작 하기 전에 [Configuration manager를 사용 하 여 Mbam 배포 계획](planning-to-deploy-mbam-with-configuration-manager-2.md)을 검토 하 여 configuration manager에서 mbam을 설치 하기 위한 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항을 충족 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="ad1ca-107">Configuration Manager 토폴로지로 MBAM을 다시 설치 해야 하는 경우 먼저 특정 Configuration Manager 개체를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="ad1ca-108">자세한 내용은 [기술 자료 문서](https://go.microsoft.com/fwlink/?LinkId=286306) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="ad1ca-109">Configuration Manager를 사용 하 여 MBAM을 설치 하는 단계는 다음 범주로 분류 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="ad1ca-110">각 범주에 대 한 단계를 완료 하 여 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="ad1ca-111">mof 파일을 만들거나 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad1ca-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="ad1ca-112">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 하려면, **구성 .mof** 파일을 편집 하 고 사용 중인 configuration Manager 버전에 따라 Sms \ _def .mof 파일을 편집 하거나 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="ad1ca-113">mof 파일을 만들거나 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad1ca-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="ad1ca-114">Configuration Manager를 사용하여 MBAM을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad1ca-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="ad1ca-115">이 섹션에서는 다음을 설치 하는 방법에 대 한 단계를 제공 합니다. MBAM이 Configuration Manager 서버에 있습니다. 데이터베이스 서버의 복구 및 감사 데이터베이스 관리 및 모니터링 서버에서 관리 및 모니터링 서버 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="ad1ca-116">Configuration Manager를 사용하여 MBAM을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad1ca-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="ad1ca-117">Configuration Manager 서버에서 MBAM 서버 기능 설치의 유효성을 검사 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad1ca-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="ad1ca-118">Microsoft BitLocker 관리 및 모니터링 설치가 완료 되 면 설치에서 Configuration Manager 서버에 필요한 모든 MBAM 기능을 성공적으로 설정 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1ca-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="ad1ca-119">Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법</span><span class="sxs-lookup"><span data-stu-id="ad1ca-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="ad1ca-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ad1ca-120">Related topics</span></span>


[<span data-ttu-id="ad1ca-121">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="ad1ca-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





