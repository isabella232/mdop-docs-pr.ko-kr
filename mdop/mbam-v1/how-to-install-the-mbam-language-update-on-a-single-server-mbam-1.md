---
title: 단일 서버에서 MBAM 언어 업데이트를 설치하는 방법
description: 단일 서버에서 MBAM 언어 업데이트를 설치하는 방법
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824753"
---
# <span data-ttu-id="6ed6e-103">단일 서버에서 MBAM 언어 업데이트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="6ed6e-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="6ed6e-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 하나 이상의 컴퓨터에서 실행할 수 있는 4 개의 서버 역할을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="6ed6e-105">그러나 mbam 1.0 언어 릴리스 및 MBAM 정책 템플릿의 설치를 지원 하기 위해 두 개의 MBAM 서버 기능만 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="6ed6e-106">컴퓨터 하나에 설치 되도록 필요한 세 가지 MBAM 기능을 모두 업데이트 하려면이 항목에서 설명 하는 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="6ed6e-107">단일 서버에 MBAM 언어 업데이트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="6ed6e-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="6ed6e-108">IIS (인터넷 정보 서비스) 관리 콘솔을 열고 **사이트로**이동한 다음 Microsoft BitLocker 관리 및 모니터링 웹 사이트를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="6ed6e-109">MBAM 웹 사이트의 바인딩을 편집한 다음 사이트의 바인딩을 일시적으로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="6ed6e-110">예를 들어 443에서 9443로 포트를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="6ed6e-111">MBAM 설정 마법사 (MBAMsetup.exe)를 찾아 실행 하 고 다음 세 가지 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="6ed6e-112">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="6ed6e-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="6ed6e-113">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="6ed6e-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="6ed6e-114">그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="6ed6e-114">Group Policy Templates</span></span>

    <span data-ttu-id="6ed6e-115">**중요**  MBAM 서버 기능은 먼저 준수 및 감사 보고서로 업데이트 한 다음 관리 및 모니터링 서버 순서 대로 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="6ed6e-116">그룹 정책 템플릿은 순서에 관계 없이 언제 든 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="6ed6e-117">서버 데이터베이스를 업그레이드 한 후에 IIS 관리 콘솔을 열고 Microsoft BitLocker 관리 및 모니터링 웹 사이트의 바인딩을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="6ed6e-118">바인딩 중 하나를 삭제 하 고 남아 있는 바인딩에 MBAM enterprise 구성에 대 한 올바른 호스트 이름, 인증서 및 포트 번호가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="6ed6e-119">MBAM 웹 사이트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="6ed6e-120">MBAM 웹 사이트 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="6ed6e-121">MBAM 웹 인터페이스를 열고 클라이언트에 대 한 복구 키를 반입할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="6ed6e-122">새 또는 수동으로 암호 해독 된 클라이언트 컴퓨터의 암호화를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="6ed6e-123">**참고**  MBAM 클라이언트는 복구 및 하드웨어 데이터베이스와 통신할 수 있는 경우에만 열립니다.</span><span class="sxs-lookup"><span data-stu-id="6ed6e-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="6ed6e-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6ed6e-124">Related topics</span></span>


[<span data-ttu-id="6ed6e-125">MBAM 1.0 언어 릴리스 업데이트 배포</span><span class="sxs-lookup"><span data-stu-id="6ed6e-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





