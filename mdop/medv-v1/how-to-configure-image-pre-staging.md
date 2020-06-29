---
title: 이미지 사전 준비를 구성하는 방법
description: 이미지 사전 준비를 구성하는 방법
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826408"
---
# <span data-ttu-id="f9aa9-103">이미지 사전 준비를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9aa9-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="f9aa9-104">**참고**  이미지 사전 준비는 초기 이미지 다운로드에만 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="f9aa9-105">이미지 업데이트에는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="f9aa9-106">이미지 사전 준비를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9aa9-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="f9aa9-107">이미지 사전 준비를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="f9aa9-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="f9aa9-108">클라이언트 컴퓨터의 이미지 저장소 디렉터리 아래에서 준비 단계 이미지에 대 한 폴더를 만들고 *Med-v 이미지*의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="f9aa9-109">**참고**  이 폴더는 *Med-v 이미지*라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="f9aa9-110">MED-V 이미지 폴더 내에 하위 폴더를 만들고 이름 *에 해당 하*는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="f9aa9-111">**참고**  이 폴더는 *Prestageages*기간으로 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="f9aa9-112">*Med-v 이미지* 폴더에 Acl (액세스 제어 목록) 보안을 적용 하려면 다음 ACL을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="f9aa9-113">NT AUTHORITY\\Authenticated 사용자: (OI) (CI) (특별 액세스:)</span><span class="sxs-lookup"><span data-stu-id="f9aa9-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="f9aa9-114">파일 \ _APPEND \ _DATA</span><span class="sxs-lookup"><span data-stu-id="f9aa9-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="f9aa9-115">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="f9aa9-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="f9aa9-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="f9aa9-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="f9aa9-117">**참고**  ACL 보안을 *Med-v 이미지* 폴더에 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="f9aa9-118">*사전 Stageages 연령* 폴더에 acl 보안을 적용 하려면 다음 ACL을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="f9aa9-119">NT AUTHORITY\\Authenticated 사용자: (OI) (CI) (특별 액세스:)</span><span class="sxs-lookup"><span data-stu-id="f9aa9-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="f9aa9-120">READ\_CONTROL</span><span class="sxs-lookup"><span data-stu-id="f9aa9-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="f9aa9-121">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="f9aa9-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="f9aa9-122">파일 \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="f9aa9-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="f9aa9-123">파일 \ _READ \ _DATA</span><span class="sxs-lookup"><span data-stu-id="f9aa9-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="f9aa9-124">파일 \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="f9aa9-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="f9aa9-125">파일 \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="f9aa9-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="f9aa9-126">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="f9aa9-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="f9aa9-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="f9aa9-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="f9aa9-128">**참고**  *사전* 에 ACL 보안을 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="f9aa9-129">이미지 파일 (CKM 및 INDEX files)을 *Prestageages 연령* 폴더에 푸시합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="f9aa9-130">**참고**  이미지 파일을 스테이지 프리 폴더로 푸시한 후에는 데이터 무결성 검사를 실행 하 고 파일을 읽기 전용으로 표시 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="f9aa9-131">MED-V 클라이언트 설치: *Client.MSI VMSFOLDER = "C:\\MED-V Images"* 에 다음 매개 변수를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="f9aa9-132">단계 전 위치를 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9aa9-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="f9aa9-133">단계 전 위치 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9aa9-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="f9aa9-134">레지스트리 키 *PrestagedImagesPath*는 기본 이미지 위치를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="f9aa9-135">이 파일은 다음 디렉터리에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="f9aa9-136">X86-</span><span class="sxs-lookup"><span data-stu-id="f9aa9-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="f9aa9-137">X64-</span><span class="sxs-lookup"><span data-stu-id="f9aa9-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="f9aa9-138">이미지가 다른 위치에 있는 경우 경로를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9aa9-138">If the image is in a different location, change the path.</span></span>

 

 





