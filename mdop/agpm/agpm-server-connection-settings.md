---
title: AGPM 서버 연결 설정
description: AGPM 서버 연결 설정
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813020"
---
# <span data-ttu-id="8cba1-103">AGPM 서버 연결 설정</span><span class="sxs-lookup"><span data-stu-id="8cba1-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="8cba1-104">AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하 여 해당 설정의 GPO (그룹 정책 개체)가 적용 되는 그룹 정책 관리자에 대 한 AGPM 서버 연결을 중앙에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="8cba1-105">GPO를 편집할 때 사용자 Configuration\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="8cba1-106">이 경로가 표시 되지 않으면 **관리 서식 파일**을 마우스 오른쪽 단추로 클릭 하 고 agpm 또는 agpm 템플릿을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8cba1-107">설정</span><span class="sxs-lookup"><span data-stu-id="8cba1-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="8cba1-108">효과</span><span class="sxs-lookup"><span data-stu-id="8cba1-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8cba1-109">AGPM 서버 (모든 도메인)</span><span class="sxs-lookup"><span data-stu-id="8cba1-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8cba1-110">이 설정을 사용 하면 모든 도메인에서 사용할 수 있도록 하나의 AGPM 서버 연결을 중앙에서 구성 하 고 <strong> </strong> 그룹 정책 관리자 용 agpm 서버 탭의 설정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="8cba1-111">여러 AGPM 서버의 경우 기본 서버로이 설정을 구성한 다음 <strong> 관리 템플릿에서 AGPM 서버 설정을 구성 하 여 </strong> 다른 도메인에 대해이 서버를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="8cba1-112">이 기능을 사용 하지 않거나 구성 하지 않으면 각 그룹 정책 관리자가 agpm <strong> 의 Agpm 서버 탭에서 각 도메인에 대해 표시할 Agpm 서버를 선택 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="8cba1-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8cba1-113">AGPM 서버</span><span class="sxs-lookup"><span data-stu-id="8cba1-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8cba1-114">이 설정을 사용 하면 <strong> 관리 템플릿에서 AGPM 서버 (모든 도메인) 설정을 재정의 하 여 여러 도메인 관련 AGPM 서버를 중앙에서 구성 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="8cba1-115">환경에 단일 AGPM 서버만 필요한 경우 <strong> 관리 템플릿에서 Agpm 서버 (모든 도메인) 설정만 사용 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="8cba1-116">이 기능을 사용 하지 않거나 구성 하지 않으면 <strong> 관리 템플릿에서 Agpm 서버 (모든 도메인) </strong> 설정이 agpm 서버 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cba1-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="8cba1-117">추가 참조</span><span class="sxs-lookup"><span data-stu-id="8cba1-117">Additional references</span></span>

-   [<span data-ttu-id="8cba1-118">관리 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="8cba1-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="8cba1-119">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="8cba1-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





