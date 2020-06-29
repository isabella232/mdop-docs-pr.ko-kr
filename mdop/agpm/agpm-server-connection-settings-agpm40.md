---
title: AGPM 서버 연결 설정
description: AGPM 서버 연결 설정
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812833"
---
# <span data-ttu-id="54622-103">AGPM 서버 연결 설정</span><span class="sxs-lookup"><span data-stu-id="54622-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="54622-104">AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하 여 해당 설정의 GPO (그룹 정책 개체)가 적용 되는 그룹 정책 관리자에 대 한 AGPM 서버 연결을 중앙에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54622-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="54622-105">GPO를 편집할 때 사용자 Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54622-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54622-106">설정</span><span class="sxs-lookup"><span data-stu-id="54622-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="54622-107">효과</span><span class="sxs-lookup"><span data-stu-id="54622-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="54622-108">AGPM: 기본 AGPM 서버 (모든 도메인) 지정</span><span class="sxs-lookup"><span data-stu-id="54622-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="54622-109">이 정책 설정을 통해 모든 도메인에 대 한 기본 AGPM 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54622-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="54622-110">이는 AGPM 클라이언트 에서만 사용 되며 그룹 정책 관리자가 다른 보관 저장소에 연결 하는 것을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="54622-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="54622-111"><strong>Agpm: Agpm 서버 지정 설정을 사용 하 여 개별 도메인에 대해이 기본값을 재정의할 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="54622-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="54622-112">AGPM: AGPM 서버 지정</span><span class="sxs-lookup"><span data-stu-id="54622-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="54622-113">이 정책 설정을 통해 개별 도메인에 대해 AGPM 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54622-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="54622-114">이는 AGPM 클라이언트 에서만 사용 되며 그룹 정책 관리자가 지정 된 도메인의 다른 아카이브에 연결 하는 것을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="54622-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="54622-115">기본 AGPM 서버를 지정 하려면 <strong> agpm: 기본 Agpm 서버 (모든 도메인) 설정을 지정 하 </strong> 고이 정책 설정을 사용 하 여 도메인 별로 기본값을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="54622-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="54622-116">추가 참조</span><span class="sxs-lookup"><span data-stu-id="54622-116">Additional references</span></span>

-   [<span data-ttu-id="54622-117">관리 템플릿 폴더</span><span class="sxs-lookup"><span data-stu-id="54622-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

-   [<span data-ttu-id="54622-118">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="54622-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





