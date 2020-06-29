---
title: MBAM 다국어 릴리스의 알려진 문제
description: MBAM 다국어 릴리스의 알려진 문제
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825788"
---
# <span data-ttu-id="ae752-103">MBAM 다국어 릴리스의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="ae752-103">Known Issues in the MBAM International Release</span></span>

<span data-ttu-id="ae752-104">이 섹션에는 Microsoft의 MBAM (BitLocker 관리 및 모니터링) 국가별 릴리스에 대 한 알려진 문제가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae752-104">This section contains known issues for Microsoft BitLocker Administration and Monitoring (MBAM) International Release.</span></span>

## <span data-ttu-id="ae752-105">MBAM 다국어 릴리스의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="ae752-105">Known Issues in the MBAM International Release</span></span>

### <span data-ttu-id="ae752-106">설치 프로세스가 업데이트를 지정 하지 않음</span><span class="sxs-lookup"><span data-stu-id="ae752-106">The Installation Process Does Not Specify Update</span></span>

<span data-ttu-id="ae752-107">Microsoft BitLocker 관리 및 모니터링 서버를 업데이트 하는 동안에는 설치 프로그램에서 업데이트가 설치 되 고 있음을 명시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae752-107">Upon updating the Microsoft BitLocker Administration and Monitoring server or servers, the Setup program does not state that an update is being installed.</span></span>

<span data-ttu-id="ae752-108">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="ae752-108">**Workaround**: None.</span></span>

### <span data-ttu-id="ae752-109">관리 및 모니터링 서버 역할에 사용 되는 인증서</span><span class="sxs-lookup"><span data-stu-id="ae752-109">Certificates Used for the Administration and Monitoring Server Role</span></span>

<span data-ttu-id="ae752-110">MBAM 서버 간 인증을 위해 인증서를 사용 하는 경우 MBAM 관리 및 모니터링 서버를 업데이트 한 후에는 인증서가 유효 하 고 해지 되지 않았거나 만료 되지 않았는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae752-110">If you are using a certificate for authentication between MBAM servers, after updating the MBAM Administration and Monitoring server you must ensure that the certificate is valid and not revoked or expired.</span></span>

<span data-ttu-id="ae752-111">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="ae752-111">**Workaround**: None.</span></span>

### <span data-ttu-id="ae752-112">MBAM Svclog 파일 채우기 디스크 공간</span><span class="sxs-lookup"><span data-stu-id="ae752-112">MBAM Svclog File Filling Disk Space</span></span>

<span data-ttu-id="ae752-113">[기술 자료 문서 2668170](https://go.microsoft.com/fwlink/?LinkID=247277)을 팔 로우 한 경우에는이 업데이트를 설치한 후 KB 단계를 반복 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae752-113">If you have followed [Knowledge Base article 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), you might have to repeat the KB steps after you install this update.</span></span>

<span data-ttu-id="ae752-114">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="ae752-114">**Workaround**: None.</span></span>

## <span data-ttu-id="ae752-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ae752-115">Related topics</span></span>

[<span data-ttu-id="ae752-116">MBAM 1.0 언어 릴리스 업데이트 배포</span><span class="sxs-lookup"><span data-stu-id="ae752-116">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





