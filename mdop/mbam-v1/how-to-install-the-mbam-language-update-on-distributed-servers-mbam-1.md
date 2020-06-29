---
title: 분산 서버에 MBAM 언어 업데이트를 설치하는 방법
description: 분산 서버에 MBAM 언어 업데이트를 설치하는 방법
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825698"
---
# <span data-ttu-id="d0748-103">분산 서버에 MBAM 언어 업데이트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="d0748-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="d0748-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 하나 이상의 컴퓨터에서 실행할 수 있는 4 개의 서버 역할을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="d0748-105">그러나 두 개의 MBAM 서버 기능만이 MBAM 1.0 언어 릴리스 및 MBAM 정책 템플릿의 설치를 지원 하기 위해 업데이트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="d0748-106">여러 컴퓨터에 MBAM 서버 기능이 설치 된 구성에서는 다음 서버 기능만 업데이트 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="d0748-107">MBAM 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="d0748-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="d0748-108">MBAM 관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="d0748-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="d0748-109">**중요**  MBAM 서버 기능은 먼저 준수 및 감사 보고서와 관리 및 모니터링 서버 순서 대로 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="d0748-110">MBAM 그룹 정책 템플릿은 순서에 관계 없이 언제 든 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="d0748-111">MBAM 준수 및 감사 보고서 서버 기능에 MBAM 언어 업데이트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="d0748-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="d0748-112">MBAM 준수 및 감사 보고서 기능을 실행 하는 컴퓨터에서 MBAM 언어 업데이트 설정 마법사 (MBAMsetup.exe)를 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="d0748-113">준수 및 감사 보고서에 대 한 마법사를 완료 한 다음 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="d0748-114">MBAM 관리 및 모니터링 서버 기능에 MBAM 언어 업데이트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="d0748-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="d0748-115">MBAM 관리 및 모니터링 기능을 실행 하는 컴퓨터에서 IIS (인터넷 정보 서비스) 관리 콘솔을 열고 **사이트로**이동한 다음 Microsoft BitLocker 관리 및 모니터링 웹 사이트를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="d0748-116">MBAM 웹 사이트의 바인딩을 편집 하도록 선택한 다음 사이트의 바인딩을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="d0748-117">예를 들어 443에서 9443로 포트를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="d0748-118">MBAM 언어 업데이트 설정 마법사 (MBAMsetup.exe)를 찾아 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="d0748-119">관리 및 모니터링 서버 기능에 대 한 마법사를 완료 한 다음 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="d0748-120">서버 데이터베이스를 업그레이드 한 후에 IIS 관리 콘솔을 열고 Microsoft BitLocker 관리 및 모니터링 웹 사이트의 바인딩을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="d0748-121">이전 바인딩을 삭제 하 고 남아 있는 바인딩에 MBAM enterprise 구성에 대 한 올바른 호스트 이름, 인증서 및 포트 번호가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="d0748-122">MBAM 웹 사이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="d0748-123">MBAM 웹 사이트 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="d0748-124">MBAM 웹 인터페이스를 열고 클라이언트에 대 한 복구 키를 얻을 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="d0748-125">새 또는 수동으로 암호 해독 된 클라이언트 컴퓨터의 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="d0748-126">**참고**  MBAM 클라이언트는 복구 및 하드웨어 데이터베이스와 통신할 수 있는 경우에만 열립니다.</span><span class="sxs-lookup"><span data-stu-id="d0748-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="d0748-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d0748-127">Related topics</span></span>


[<span data-ttu-id="d0748-128">MBAM 1.0 언어 릴리스 업데이트 배포</span><span class="sxs-lookup"><span data-stu-id="d0748-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





