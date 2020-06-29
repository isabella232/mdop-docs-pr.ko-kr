---
title: 응용 프로그램 가상화 속성 일반 탭
description: 응용 프로그램 가상화 속성 일반 탭
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819688"
---
# <span data-ttu-id="303ce-103">Application Virtualization 속성: 일반 탭</span><span class="sxs-lookup"><span data-stu-id="303ce-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="303ce-104">**응용 프로그램 가상화 속성** 대화 상자의 **일반** 탭을 사용 하 여 로그 설정과 데이터 위치를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="303ce-105">이 탭에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="303ce-106">로그 수준</span><span class="sxs-lookup"><span data-stu-id="303ce-106">Log Level</span></span>**  
<span data-ttu-id="303ce-107">드롭다운 목록에서 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="303ce-108">기본 수준은 **정보**입니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="303ce-109">로그 다시 설정</span><span class="sxs-lookup"><span data-stu-id="303ce-109">Reset Log</span></span>**  
<span data-ttu-id="303ce-110">현재 로그 파일을 백업 하 고 즉시 새 로그 파일을 시작 하려면이 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="303ce-111">위치</span><span class="sxs-lookup"><span data-stu-id="303ce-111">Location</span></span>**  
<span data-ttu-id="303ce-112">로그 파일 sftlog.txt를 저장할 위치를 입력 하거나 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="303ce-113">기본 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="303ce-114">WindowsXP, Windows Server2003 —*C:\\documents 및 Settings\\All Users\\Application Data\\Microsoft\\Application 가상화 클라이언트*</span><span class="sxs-lookup"><span data-stu-id="303ce-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="303ce-115">Windows Vista, Windows 7, Windows Server2008-*C:\\ProgramData\\Microsoft\\Application 가상화 클라이언트*</span><span class="sxs-lookup"><span data-stu-id="303ce-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="303ce-116">시스템 로그 수준</span><span class="sxs-lookup"><span data-stu-id="303ce-116">System Log Level</span></span>**  
<span data-ttu-id="303ce-117">드롭다운 목록에서 수준을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="303ce-118">기본 수준에는 **경고가**표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-118">The default level is **Warning**.</span></span>

<span data-ttu-id="303ce-119">**참고**  **시스템 로그 수준** 설정은 시스템 이벤트 로그에 전송 되는 메시지의 수준을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="303ce-120">기록 된 메시지는 클라이언트 이벤트 로그에 기록 되는 메시지와 동일 하지만 클라이언트 이벤트 로그의 공간 제한이 없는 다른 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="303ce-121">시스템 이벤트 로그에는 공간 제한이 없기 때문에 자세한 로깅이 필요한 상황에 가장 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="303ce-122">전역 데이터 디렉터리</span><span class="sxs-lookup"><span data-stu-id="303ce-122">Global Data Directory</span></span>**  
<span data-ttu-id="303ce-123">로그 파일 디렉터리의 위치를 입력 하거나 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="303ce-124">기본 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="303ce-125">WindowsXP, Windows Server2003 —*C:\\documents 및 Settings\\All Users\\Application Data\\Microsoft\\Application 가상화 클라이언트*</span><span class="sxs-lookup"><span data-stu-id="303ce-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="303ce-126">Windows Vista, Windows 7, Windows Server2008-*C:\\ProgramData\\Microsoft\\Application 가상화 클라이언트*</span><span class="sxs-lookup"><span data-stu-id="303ce-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="303ce-127">사용자 데이터 디렉터리</span><span class="sxs-lookup"><span data-stu-id="303ce-127">User Data Directory</span></span>**  
<span data-ttu-id="303ce-128">사용자 관련 데이터가 저장 되는 디렉터리의 위치를 입력 하거나 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="303ce-129">기본값 은% APPDATA%입니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-129">The default is %APPDATA%.</span></span> <span data-ttu-id="303ce-130">이 경로는 클라이언트 컴퓨터의 유효한 환경 변수 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="303ce-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="303ce-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="303ce-131">Related topics</span></span>


[<span data-ttu-id="303ce-132">Client Management Console: 응용 프로그램 가상화 속성</span><span class="sxs-lookup"><span data-stu-id="303ce-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





