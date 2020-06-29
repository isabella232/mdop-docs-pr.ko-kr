---
title: MBAM 1.0 정보
description: MBAM 1.0 정보
author: dansimp
ms.assetid: 99254aaa-2b30-4b2e-8365-0d4b67a89a0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f8cae83bb9c8d756d57766cbcf9a90febf53f54a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824103"
---
# <span data-ttu-id="3cc52-103">MBAM 1.0 정보</span><span class="sxs-lookup"><span data-stu-id="3cc52-103">About MBAM 1.0</span></span>


<span data-ttu-id="3cc52-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 드라이브 암호화에 대 한 간편한 관리 인터페이스를 제공 하 고 분실 하거나 도난당 한 컴퓨터에 대 한 데이터 절도 또는 데이터 노출에 대 한 향상 된 보호 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc52-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides a simplified administrative interface to BitLocker drive encryption and offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="3cc52-105">BitLocker는 windows 운영 체제 볼륨에 저장 된 모든 데이터와 Windows 운영 체제, 최대 절전 모드 및 페이징 파일, 응용 프로그램, 응용 프로그램에서 사용 하는 데이터를 포함 하는 구성 데이터 볼륨을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc52-105">BitLocker encrypts all data that is stored on the Windows operating system volume and configured data volumes, which includes the Windows operating system, hibernation and paging files, applications, and the data that is used by applications.</span></span>

<span data-ttu-id="3cc52-106">Microsoft BitLocker 관리 및 모니터링을 사용 하면 해당 정책으로 클라이언트 준수를 모니터링 하 고 엔터프라이즈 및 개별 컴퓨터 모두의 암호화 상태를 보고할 수 있도록 엔터프라이즈에 적합 한 BitLocker 암호화 정책 옵션을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc52-106">With Microsoft BitLocker Administration and Monitoring, you can select the BitLocker encryption policy options that are appropriate for your enterprise so that you can monitor the client compliance with those policies and then report the encryption status of both the enterprise and individual computers.</span></span> <span data-ttu-id="3cc52-107">또한 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc52-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

<span data-ttu-id="3cc52-108">**참고**  BitLocker에 대 한 자세한 내용은이 가이드에서 설명 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc52-108">**Note** BitLocker is not covered in detail in this guide.</span></span> <span data-ttu-id="3cc52-109">BitLocker에 대 한 개요는 [Bitlocker 드라이브 암호화 개요](https://go.microsoft.com/fwlink/p/?LinkId=225013)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cc52-109">For an overview of BitLocker, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

<span data-ttu-id="3cc52-110">다음 그룹은 MBAM을 사용 하 여 BitLocker를 관리 하는 데 관심이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc52-110">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="3cc52-111">권한 부여 없이 기밀 데이터가 공개 되지 않도록 하는 것을 담당 하는 관리자, IT 보안 전문가 및 규정 준수 책임자</span><span class="sxs-lookup"><span data-stu-id="3cc52-111">Administrators, IT security professionals, and compliance officers who are tasked with ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="3cc52-112">원격 또는 지사에서 컴퓨터 보안을 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="3cc52-112">Administrators who are responsible for securing computers in remote or branch offices</span></span>

-   <span data-ttu-id="3cc52-113">모바일 인 서버 또는 Windows 클라이언트 컴퓨터를 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="3cc52-113">Administrators who are responsible for servers or Windows client computers that are mobile</span></span>

-   <span data-ttu-id="3cc52-114">기밀 데이터를 포함 하는 서버 서비스 해제를 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="3cc52-114">Administrators who are responsible for decommissioning servers that contain confidential data</span></span>

## <span data-ttu-id="3cc52-115">MBAM 1.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="3cc52-115">MBAM 1.0 Release Notes</span></span>


<span data-ttu-id="3cc52-116">최신 업데이트에 대 한 자세한 내용은 [MBAM 1.0에 대 한 릴리스 정보](release-notes-for-mbam-10.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cc52-116">For more information and for latest updates, see [Release Notes for MBAM 1.0](release-notes-for-mbam-10.md).</span></span>

## <span data-ttu-id="3cc52-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3cc52-117">Related topics</span></span>


[<span data-ttu-id="3cc52-118">MBAM 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="3cc52-118">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





