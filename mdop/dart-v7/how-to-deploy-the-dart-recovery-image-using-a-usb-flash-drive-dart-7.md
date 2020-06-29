---
title: USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법
description: USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823668"
---
# <span data-ttu-id="6915f-103">USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="6915f-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="6915f-104">**DaRT 복구 이미지 마법사**실행을 완료 한 후에는의 도구를 사용 하 여 <https://go.microsoft.com/fwlink/?LinkId=218888> ISO 이미지 파일을 UFD (USB 플래시 드라이브)에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="6915f-105">이 섹션에 설명 된 단계에 따라 수동으로 ISO 이미지 파일을 UFD에 복사할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="6915f-106">DaRT 복구 이미지를 USB 플래시 드라이브에 저장 하려면</span><span class="sxs-lookup"><span data-stu-id="6915f-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="6915f-107">USB 플래시 드라이브를 포맷 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="6915f-108">실행 중인 유효한 운영 체제 또는 WindowsPE 세션에서 UFD를 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="6915f-109">관리자 권한으로 명령 프롬프트에서 **DISKPART** 를 입력 하 고 **디스크 목록을**입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="6915f-110">명령 프롬프트 창에 UFD의 디스크 번호 (예: **디스크 1)** 가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="6915f-111">명령 프롬프트에서 다음 명령을 한 번에 하나씩 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="6915f-112">**참고**  앞의 코드 예제에서는 Disk1가 UFD 라고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="6915f-113">필요한 경우 디스크 1을 디스크 번호로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="6915f-114">회사의 선호 하는 이미지 탑재 방법을 사용 하 여 **DaRT 복구 이미지 마법사**의 **시작 이미지 만들기** 대화 상자에서 만든 ISO 이미지 파일을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="6915f-115">이를 위해서는 이미지 파일을 탑재할 수 있는 메서드가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="6915f-116">탑재 된 ISO 이미지 파일을 열고 모든 내용을 서식이 지정 된 USB 플래시 드라이브로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="6915f-117">**참고**  복구 이미지의 CD 또는 DVD를 구운 경우 CD 또는 DVD의 파일을 열고 콘텐츠를 UFD에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="6915f-118">이렇게 하면 이미지를 탑재할 필요를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6915f-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="6915f-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6915f-119">Related topics</span></span>


[<span data-ttu-id="6915f-120">DaRT 7.0 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="6915f-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





