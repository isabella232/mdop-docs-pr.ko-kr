---
title: FileSystem 캐시를 다시 설정하는 방법
description: FileSystem 캐시를 다시 설정하는 방법
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816713"
---
# <span data-ttu-id="cc8a0-103">FileSystem 캐시를 다시 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="cc8a0-103">How to Reset the FileSystem Cache</span></span>


<span data-ttu-id="cc8a0-104">파일 시스템 캐시를 다시 설정 하는 것은 일반적으로 필요한 사항이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="cc8a0-104">Resetting the FileSystem cache is not something that should usually be necessary.</span></span> <span data-ttu-id="cc8a0-105">그러나 문제 해결을 위해 파일 시스템 캐시를 완전히 다시 설정 해야 하는 경우 다음 절차를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc8a0-105">However if you need to completely reset the FileSystem cache, perhaps for troubleshooting purposes, you can use the following procedure.</span></span> <span data-ttu-id="cc8a0-106">이 작업을 수행 하려면 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8a0-106">Administrative rights are required to perform this action.</span></span>

**<span data-ttu-id="cc8a0-107">파일 시스템 캐시를 다시 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="cc8a0-107">To reset the FileSystem cache</span></span>**

1.  <span data-ttu-id="cc8a0-108">다음 레지스트리 값을 0 (영)으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8a0-108">Set the following registry value to 0 (zero):</span></span>

    <span data-ttu-id="cc8a0-109">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span><span class="sxs-lookup"><span data-stu-id="cc8a0-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State</span></span>

2.  <span data-ttu-id="cc8a0-110">컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc8a0-110">Restart the computer.</span></span>

## <span data-ttu-id="cc8a0-111">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cc8a0-111">Related topics</span></span>


[<span data-ttu-id="cc8a0-112">명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cc8a0-112">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





