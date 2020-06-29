---
title: 로깅 및 추적 설정
description: 로깅 및 추적 설정
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820588"
---
# <span data-ttu-id="3d290-103">로깅 및 추적 설정</span><span class="sxs-lookup"><span data-stu-id="3d290-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="3d290-104">AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하면 이러한 설정의 GPO (그룹 정책 개체)가 적용 되는 AGPM 서버 및 클라이언트에 대 한 로깅 및 추적 옵션을 중앙에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d290-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="3d290-105">GPMC (그룹 정책 관리 콘솔)에서 GPO를 편집할 때 **그룹 정책 개체 편집기** 의 컴퓨터 Configuration\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d290-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="3d290-106">이 경로가 표시 되지 않으면 **관리 서식 파일**을 마우스 오른쪽 단추로 클릭 하 고 agpm 또는 agpm 템플릿을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d290-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="3d290-107">**추적 파일 위치**:</span><span class="sxs-lookup"><span data-stu-id="3d290-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="3d290-108">클라이언트:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="3d290-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="3d290-109">서버:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="3d290-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3d290-110">설정</span><span class="sxs-lookup"><span data-stu-id="3d290-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="3d290-111">효과</span><span class="sxs-lookup"><span data-stu-id="3d290-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3d290-112">AGPM 로깅</span><span class="sxs-lookup"><span data-stu-id="3d290-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3d290-113">이 설정을 사용 하면 추적 설정 여부와 세부 정보 수준을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d290-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="3d290-114">이 설정은 AGPM의 클라이언트 및 서버 구성 요소 모두에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d290-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="3d290-115">이 설정을 사용 하지 않거나 구성 하지 않으면이 설정이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d290-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3d290-116">추가 참조</span><span class="sxs-lookup"><span data-stu-id="3d290-116">Additional references</span></span>

-   [<span data-ttu-id="3d290-117">관리 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="3d290-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





