---
title: 클라이언트 로그 파일을 구성하는 방법
description: 클라이언트 로그 파일을 구성하는 방법
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817798"
---
# <span data-ttu-id="3178f-103">클라이언트 로그 파일을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3178f-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="3178f-104">다음 절차를 사용 하 여 App-v (Application Virtualization) 클라이언트 로그 파일을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="3178f-105">로그 파일 위치를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3178f-105">To change the log file location</span></span>**

-   <span data-ttu-id="3178f-106">다음 레지스트리 키 값을 편집 하 여 로그 파일에 대 한 새 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="3178f-107">이 값을 변경한 후 **sftlist** 서비스를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="3178f-108">설치 후에도이 위치를 대화형으로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="3178f-109">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span><span class="sxs-lookup"><span data-stu-id="3178f-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="3178f-110">로그 보고 수준을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3178f-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="3178f-111">기본적으로 로그에 기록 되는 메시지 형식에는 심각도 수준 4 (알림) 이상의 모든 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="3178f-112">심각도 수준은 다음 키 값에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="3178f-113">자세한 로깅을 사용 하려면이 키 값을 5로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="3178f-114">매우 큰 메시지를 생성 하 고 로그가 빠르게 채워지기 때문에 문제 해결 중 짧은 기간 동안에만 자세한 정보 표시 로깅을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="3178f-115">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="3178f-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="3178f-116">로그 크기를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3178f-116">To change the log size</span></span>**

-   <span data-ttu-id="3178f-117">Application Virtualization (App-v) 4.5의 로그 크기는 다음 레지스트리 키 값으로 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="3178f-118">이 값은 기본적으로 256MB이 고 최대 크기 (MB)를 정의 하 여 로그를 다시 설정 하기 전까지 커질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="3178f-119">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="3178f-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="3178f-120">**주의**  사항 로그 파일이 다시 설정 되도록 하려면이 레지스트리 키 값을 0 보다 큰 값으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="3178f-121">백업 복사본 수를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="3178f-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="3178f-122">로그 파일이 최대 크기에 도달 하면 로그에 다음 쓰기가 발생할 때 재설정이 강제 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="3178f-123">다시 설정 하면 새 로그 파일이 만들어지고 이전 파일의 이름이 백업으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="3178f-124">다음 레지스트리 설정은 파일을 다시 설정할 때 보관 되는 로그 파일의 백업 복사본 수를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="3178f-125">기본값은 4입니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-125">The default value is 4.</span></span>

    <span data-ttu-id="3178f-126">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="3178f-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="3178f-127">백업 로그 파일 이름의 형식은 **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** 이며 재설정 시간 (Utc (협정 세계시))을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="3178f-128">다음 표에는 파일 이름과 설명을 만드는 데 사용 되는 기호가 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3178f-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="3178f-129">기호</span><span class="sxs-lookup"><span data-stu-id="3178f-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="3178f-130">설명</span><span class="sxs-lookup"><span data-stu-id="3178f-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3178f-131">년</span><span class="sxs-lookup"><span data-stu-id="3178f-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-132">4 자리 연도</span><span class="sxs-lookup"><span data-stu-id="3178f-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3178f-133">200</span><span class="sxs-lookup"><span data-stu-id="3178f-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-134">2 자리 월 (01 – 12)</span><span class="sxs-lookup"><span data-stu-id="3178f-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3178f-135">일</span><span class="sxs-lookup"><span data-stu-id="3178f-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-136">해당 달의 2 자리 일 (01-31)</span><span class="sxs-lookup"><span data-stu-id="3178f-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3178f-137">h:mm</span><span class="sxs-lookup"><span data-stu-id="3178f-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-138">시간 (00 – 23)</span><span class="sxs-lookup"><span data-stu-id="3178f-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3178f-139">200</span><span class="sxs-lookup"><span data-stu-id="3178f-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-140">분 (00 – 59)</span><span class="sxs-lookup"><span data-stu-id="3178f-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="3178f-141">ss</span><span class="sxs-lookup"><span data-stu-id="3178f-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-142">초 (00 – 59)</span><span class="sxs-lookup"><span data-stu-id="3178f-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="3178f-143">uuu</span><span class="sxs-lookup"><span data-stu-id="3178f-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="3178f-144">밀리초 (000-999)</span><span class="sxs-lookup"><span data-stu-id="3178f-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="3178f-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3178f-145">Related topics</span></span>


[<span data-ttu-id="3178f-146">명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3178f-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





