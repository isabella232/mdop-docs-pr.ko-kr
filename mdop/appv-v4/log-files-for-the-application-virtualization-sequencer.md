---
title: Application Virtualization Sequencer에 대한 로그 파일
description: Application Virtualization Sequencer에 대한 로그 파일
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816218"
---
# <span data-ttu-id="c8545-103">Application Virtualization Sequencer에 대한 로그 파일</span><span class="sxs-lookup"><span data-stu-id="c8545-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="c8545-104">App-v (Application Virtualization) Sequencer 용 로그 파일은 시퀀싱 하는 응용 프로그램에 대 한 자세한 정보를 제공 하며 기능을 확인 하거나 문제를 해결할 때 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8545-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="c8545-105">다음 표에서는 Sequencer를 사용할 때 만들어지는 로그 파일 및 해당 기본 위치에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8545-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c8545-106">로그 파일 이름</span><span class="sxs-lookup"><span data-stu-id="c8545-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="c8545-107">설명</span><span class="sxs-lookup"><span data-stu-id="c8545-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c8545-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="c8545-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c8545-109">응용 프로그램 시퀀싱에 대 한 일반적인 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8545-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="c8545-110">이 로그를 시작 점으로 사용 하 여 Sequencer 오류 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8545-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="c8545-111">로그 파일 위치: <em> %Windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="c8545-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="c8545-112">[Template 토큰 값] 앱-V 4.6 로그 파일 위치: <em> %Windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [Template 토큰 값]</span><span class="sxs-lookup"><span data-stu-id="c8545-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c8545-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="c8545-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c8545-114">시퀀서에서 다시 시작 하는 동안 발생 하는 컴퓨터 다시 시작 작업에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8545-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="c8545-115">로그 파일 위치: <em> %Windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="c8545-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="c8545-116">[Template 토큰 값] 앱-V 4.6 로그 파일 위치: <em> %Windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [Template 토큰 값]</span><span class="sxs-lookup"><span data-stu-id="c8545-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c8545-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="c8545-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c8545-118">시퀀싱 중 사용 되는 프로세스에 대 한 일반적인 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8545-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="c8545-119">로그 파일 위치: <em> %Windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="c8545-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="c8545-120">[Template 토큰 값] 앱-V 4.6 로그 파일 위치: <em> %Windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [Template 토큰 값]</span><span class="sxs-lookup"><span data-stu-id="c8545-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c8545-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c8545-121">Related topics</span></span>


[<span data-ttu-id="c8545-122">Application Virtualization Sequencer 참조</span><span class="sxs-lookup"><span data-stu-id="c8545-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





