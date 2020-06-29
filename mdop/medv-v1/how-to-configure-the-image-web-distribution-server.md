---
title: 이미지 웹 배포 서버를 구성하는 방법
description: 이미지 웹 배포 서버를 구성하는 방법
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825158"
---
# <span data-ttu-id="51197-103">이미지 웹 배포 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="51197-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="51197-104">이미지 저장소는 이미지 배포에 사용 되는 선택적 서버 (관리자가 새 이미지 및 클라이언트 컴퓨터를 15 분 마다 확인 하 고 새 이미지를 사용할 수 있는 경우에는 서버를 업데이트 하는 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="51197-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="51197-105">이미지 배포 서버에는 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="51197-106">IIS (인터넷 정보 서비스)-자세한 내용은 [인터넷 정보 서비스](https://go.microsoft.com/fwlink/?LinkId=142995)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51197-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="51197-107">IIS를 설치 하는 동안 역할 서비스를 추가할 때 다음과 같은 지원 되는 인증 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="51197-108">기본 인증</span><span class="sxs-lookup"><span data-stu-id="51197-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="51197-109">Windows 인증</span><span class="sxs-lookup"><span data-stu-id="51197-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="51197-110">클라이언트 인증서 매핑 인증</span><span class="sxs-lookup"><span data-stu-id="51197-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="51197-111">IIS를 구성할 때 다음을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="51197-112">**MEDVImages**라는 별칭을 사용 하 여 가상 디렉터리를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="51197-113">실제 경로는 이미지의 위치를 가리켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="51197-114">비트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-114">Enable BITS.</span></span>

    -   <span data-ttu-id="51197-115">다음 MIME 형식을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="51197-116">ckm (응용 프로그램/8 진수-스트림)</span><span class="sxs-lookup"><span data-stu-id="51197-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="51197-117">**. index (응용 프로그램/8 진수-스트림**)</span><span class="sxs-lookup"><span data-stu-id="51197-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="51197-118">MED-V 사이트에서 **모든 사용자**에 게 읽기 권한을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="51197-119">IIS를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="51197-119">Restart IIS.</span></span>

-   <span data-ttu-id="51197-120">IIS 용 BITS Server Extensions-자세한 내용은 [Bits Server Extensions 설치](https://go.microsoft.com/fwlink/?LinkId=142996)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51197-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="51197-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="51197-121">Related topics</span></span>


[<span data-ttu-id="51197-122">지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="51197-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="51197-123">MED-V 이미지 리포지토리 디자인</span><span class="sxs-lookup"><span data-stu-id="51197-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 





