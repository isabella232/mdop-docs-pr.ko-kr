---
title: UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록
description: UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826458"
---
# <span data-ttu-id="c9956-103">UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록</span><span class="sxs-lookup"><span data-stu-id="c9956-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="c9956-104">UE-V 배포에 포함할 lob (기간 업무) 응용 프로그램을 평가 하려면 다음 사항을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9956-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="c9956-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9956-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-106">이 응용 프로그램에 사용자가 사용자 지정할 수 있는 설정이 포함 되어 있습니까?</span><span class="sxs-lookup"><span data-stu-id="c9956-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-107">이 설정을 로밍 하는 사용자에 게 중요 한가요?</span><span class="sxs-lookup"><span data-stu-id="c9956-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-108">이러한 사용자 설정이 응용 프로그램 관리 또는 설정 정책 솔루션에 의해 이미 관리 되나요?</span><span class="sxs-lookup"><span data-stu-id="c9956-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="c9956-109">UE-V는 로그온, 잠금 해제 또는 원격 연결 이벤트에 대 한 응용 프로그램 시작 및 Windows 설정에 응용 프로그램 설정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="c9956-110">UE-V를 다른 설정 정책 솔루션과 함께 사용 하는 경우 사용자가 roamed 설정 간에 일관성 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-111">컴퓨터에 대 한 응용 프로그램 설정이 있나요?</span><span class="sxs-lookup"><span data-stu-id="c9956-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="c9956-112">하드웨어 또는 특정 컴퓨터 구성과 관련 된 응용 프로그램 기본 설정 및 사용자 지정은 세션 간에 일관 되 게 로밍하지 않으며 응용 프로그램 환경이 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-113">응용 프로그램이 Program Files 디렉터리 또는 <strong> 사용자 </strong> \ [사용자 이름] \ <strong> AppData </strong>  \  <strong> </strong> lochdirectory에 있는 파일 디렉터리에 있는 설정을 사용 합니까?</span><span class="sxs-lookup"><span data-stu-id="c9956-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="c9956-114">이러한 위치 중 하나에 저장 된 응용 프로그램 데이터는 해당 컴퓨터에 대 한 정보 이거나 데이터가 너무 커서 로밍할 수 없기 때문에 일반적으로 사용자와 로밍할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-115">응용 프로그램에서 로밍 하지 않아야 하는 다른 응용 프로그램 데이터를 포함 하는 파일의 설정을 저장 합니까?</span><span class="sxs-lookup"><span data-stu-id="c9956-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="c9956-116">UE-V는 파일을 단일 단위로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="c9956-117">설정이 아닌 다른 응용 프로그램 데이터를 포함 하는 파일에 설정을 저장 한 경우이 추가 데이터를 동기화 하면 응용 프로그램 환경이 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c9956-118">설정이 포함 된 파일의 크기</span><span class="sxs-lookup"><span data-stu-id="c9956-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="c9956-119">설정 동기화의 성능은 크기가 큰 파일의 영향을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="c9956-120">큰 파일을 포함 하면 설정 동기화의 성능에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9956-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c9956-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c9956-121">Related topics</span></span>


[<span data-ttu-id="c9956-122">UE-V 구성 방법 계획</span><span class="sxs-lookup"><span data-stu-id="c9956-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="c9956-123">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="c9956-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





