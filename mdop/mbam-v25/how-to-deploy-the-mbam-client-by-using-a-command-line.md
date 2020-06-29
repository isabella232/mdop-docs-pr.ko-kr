---
title: 명령줄을 사용하여 MBAM 클라이언트를 배포하는 방법
description: 명령줄을 사용하여 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824488"
---
# <span data-ttu-id="e2500-103">명령줄을 사용하여 MBAM 클라이언트를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="e2500-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="e2500-104">명령줄을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트 소프트웨어를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="e2500-105">MBAM 클라이언트 소프트웨어를 배포 하는 명령줄</span><span class="sxs-lookup"><span data-stu-id="e2500-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="e2500-106">명령 프롬프트에서 다음 명령을 입력 하 여 MBAM 클라이언트 소프트웨어를 배포할 때 최종 사용자 사용권 계약을 자동으로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="e2500-107">MBAMClientSetup.exe/acceptEula = 예</span><span class="sxs-lookup"><span data-stu-id="e2500-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="e2500-108">**참고**  **/Ju** 및 **/jm** 명령줄 옵션은 지원 되지 않으며 mbam 클라이언트 소프트웨어를 설치 하는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="e2500-109">명령 프롬프트에서 다음 명령을 입력 하 여 MSP의 압축을 풀고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="e2500-110">MBAMClientSetup.exe/extract &lt; 경로 MSI &gt; /AcceptEula = Yes를 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="e2500-111">다음 명령을 실행 하 여 MSI를 자동으로 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="e2500-112">msiexec/i &lt; 경로를 추출한 MSI &gt; /qb ALLUSERS = 1 재부팅 = ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="e2500-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="e2500-113">**참고**  MBAM 2.5 SP1 부터는 별도의 MSI가 MBAM 제품에 더 이상 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="e2500-114">그러나 EULA를 수락 하면 제품에 포함 되어 있는 실행 파일 (.exe)에서 MSI를 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="e2500-115">OPTIN \\ _FOR \ _MICROSOFT \ _UPDATES = 1 명령줄 옵션</span><span class="sxs-lookup"><span data-stu-id="e2500-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="e2500-116">선택적으로 클라이언트 소프트웨어 설치 중 명령줄 옵션을 지정 `OPTIN_FOR_MICROSOFT_UPDATES=1` 하 여 클라이언트 컴퓨터에 Microsoft 업데이트를 자동으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="e2500-117">이 옵션을 지정 하면 Microsoft Update가 자동으로 시작 되 고 클라이언트 소프트웨어 설치가 완료 된 후 설치할 수 있는 업데이트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="e2500-118">다음 설치 방법 중 하 나와 함께이 명령줄 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e2500-119">다음을 사용 하 여 MBAM 클라이언트 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="e2500-120">예</span><span class="sxs-lookup"><span data-stu-id="e2500-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e2500-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="e2500-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="e2500-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="e2500-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e2500-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="e2500-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="e2500-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="e2500-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="e2500-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e2500-125">Related topics</span></span>


[<span data-ttu-id="e2500-126">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="e2500-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="e2500-127">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="e2500-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e2500-128">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e2500-129">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2500-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




