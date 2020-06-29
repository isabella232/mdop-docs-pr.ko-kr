---
title: 연결 그룹 관리
description: 연결 그룹 관리
author: dansimp
ms.assetid: 1a9c8f26-f421-4b70-b7e2-da8118e8198c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2e57b9dbe56072e6049e8fabef5705c374d022c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813580"
---
# <span data-ttu-id="9b3a1-103">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="9b3a1-103">Managing Connection Groups</span></span>


<span data-ttu-id="9b3a1-104">연결 그룹은 패키지 내의 응용 프로그램이 가상 환경에서 서로 상호 작용 하는 반면 나머지 시스템의 나머지 부분에서 격리 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="9b3a1-105">관리자는 연결 그룹을 사용 하 여 패키지를 독립적으로 관리할 수 있으며, 클라이언트 컴퓨터에 같은 응용 프로그램을 여러 번 추가 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="9b3a1-106">**참고**  이전 버전의 App-v 5.0에서 연결 그룹은 동적 도구 모음 컴퍼지션 이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-106">**Note** In previous versions of App-V 5.0, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="9b3a1-107">이 항목의 내용:</span><span class="sxs-lookup"><span data-stu-id="9b3a1-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md)"><span data-ttu-id="9b3a1-108">연결 그룹 가상 환경 정보</span><span class="sxs-lookup"><span data-stu-id="9b3a1-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9b3a1-109">연결 그룹 가상 환경에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file.md)"><span data-ttu-id="9b3a1-110">연결 그룹 파일 정보</span><span class="sxs-lookup"><span data-stu-id="9b3a1-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9b3a1-111">연결 그룹 파일에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group.md)"><span data-ttu-id="9b3a1-112">연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="9b3a1-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9b3a1-113">새 연결 그룹을 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="9b3a1-114">사용자가 게시한 패키지 및 전역적으로 게시된 패키지를 사용하여 연결 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="9b3a1-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9b3a1-115">사용자에 게 게시 되 고 전역적으로 게시 되는 패키지가 혼합 되어 있는 새 연결 그룹을 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group.md)"><span data-ttu-id="9b3a1-116">연결 그룹을 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="9b3a1-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9b3a1-117">연결 그룹을 삭제 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group.md)"><span data-ttu-id="9b3a1-118">연결 그룹을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="9b3a1-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="9b3a1-119">연결 그룹을 게시 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3a1-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="9b3a1-120">앱에 대 한 기타 리소스-V 5.0 연결 그룹</span><span class="sxs-lookup"><span data-stu-id="9b3a1-120">Other resources for App-V 5.0 connection groups</span></span>


-   [<span data-ttu-id="9b3a1-121">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="9b3a1-121">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





