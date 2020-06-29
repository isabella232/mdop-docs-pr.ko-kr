---
title: FileSystem 캐시의 크기를 변경하는 방법
description: FileSystem 캐시의 크기를 변경하는 방법
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818003"
---
# <span data-ttu-id="56d36-103">FileSystem 캐시의 크기를 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="56d36-103">How to Change the Size of the FileSystem Cache</span></span>


<span data-ttu-id="56d36-104">명령줄을 사용 하 여 파일 시스템 캐시의 크기를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56d36-104">You can change the size of the FileSystem cache by using the command line.</span></span> <span data-ttu-id="56d36-105">이 작업을 수행 하려면 캐시를 완전히 다시 설정 해야 하며, 관리 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="56d36-105">This action requires a complete reset of the cache, and it requires administrative rights.</span></span>

**<span data-ttu-id="56d36-106">파일 시스템 캐시의 크기를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="56d36-106">To change the size of the FileSystem cache</span></span>**

1.  <span data-ttu-id="56d36-107">다음 레지스트리 값을 0 (영)으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56d36-107">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="56d36-108">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="56d36-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="56d36-109">다음 레지스트리 값을 패키지를 보유 하는 데 필요한 최대 캐시 크기인 MB (예: 8192 MB)로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56d36-109">Set the following registry value to the maximum cache size, in MB, that is necessary to hold the packages—for example, 8192 MB:</span></span>

    <span data-ttu-id="56d36-110">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span><span class="sxs-lookup"><span data-stu-id="56d36-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize</span></span>

3.  <span data-ttu-id="56d36-111">컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="56d36-111">Restart the computer.</span></span>

## <span data-ttu-id="56d36-112">관련 항목</span><span class="sxs-lookup"><span data-stu-id="56d36-112">Related topics</span></span>


[<span data-ttu-id="56d36-113">명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="56d36-113">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





