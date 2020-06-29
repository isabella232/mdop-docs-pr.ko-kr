---
title: 바로 가기 및 파일 형식 연결 동작을 구성하는 방법
description: 바로 가기 및 파일 형식 연결 동작을 구성하는 방법
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817913"
---
# <span data-ttu-id="42a3b-103">바로 가기 및 파일 형식 연결 동작을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="42a3b-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="42a3b-104">바로 가기 및 파일 형식 연결 (FTA) 게시 정책은 게시 새로 고침 작업을 수행 하는 동안 게시 서버에 의해 클라이언트로 전송 되는 게시 XML 파일에 의해 정의 및 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="42a3b-105">클라이언트는이 정보를 받을 때 아이콘과 FTAs와 같은 응용 프로그램에 대 한 새로 게시 된 데이터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="42a3b-106">그런 다음 오래 된 게시 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="42a3b-107">App-v 버전 4.6에서 관리자가이 동작을 제어할 수 있도록 두 개의 레지스트리 키 값이 정의 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="42a3b-108">기본적으로 클라이언트 콘솔을 사용 하 여 로컬로 만든 바로 가기가 이제 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="42a3b-109">바로 가기 및 FTA 동작을 변경 하는 방법</span><span class="sxs-lookup"><span data-stu-id="42a3b-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="42a3b-110">클라이언트 구성 레지스트리 키, "FileTypePolicy" 및 "ShortcutPolicy"에 대해 새로운 DWORD 레지스트리 값 두 개가 정의 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="42a3b-111">이러한 DWORD 레지스트리 값은 기본적으로 제공 되지 않지만 수동으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="42a3b-112">구성 레지스트리 키는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="42a3b-113">다음 표에는 4 개의 정책 값이 정의 되어 있으며,이는 두 레지스트리 키 값에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="42a3b-114">다음 목록에는 레지스트리 설정에 대 한 숫자 값과 게시 새로 고침 작업의 파일 형식 또는 바로 가기에 적용 되는 동작이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42a3b-115">이름</span><span class="sxs-lookup"><span data-stu-id="42a3b-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-116">유형</span><span class="sxs-lookup"><span data-stu-id="42a3b-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-117">데이터 (예제)</span><span class="sxs-lookup"><span data-stu-id="42a3b-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-118">설명</span><span class="sxs-lookup"><span data-stu-id="42a3b-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42a3b-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="42a3b-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="42a3b-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-121">기본값 = 0x2 (App-V 4.6)</span><span class="sxs-lookup"><span data-stu-id="42a3b-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-122">(0x0) – 동일한 게시 정보 원본에서 기존 항목을 제거 하 고 로컬에 추가 된 항목만 유지</span><span class="sxs-lookup"><span data-stu-id="42a3b-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="42a3b-123">(0x1) – "ServerOnly"-동일한 게시 정보 원본 및 로컬에 추가 된 모든 항목에서 오래 된 항목을 제거 하 고 새 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="42a3b-124">(0x2)-"ClientAndServer"-동일한 게시 정보 원본에서 오래 된 항목을 제거 하 고, 로컬에 추가 된 항목을 유지 하 고, 새 항목을 추가 합니다 (App-v 4.6 용이 없는 경우 기본값).</span><span class="sxs-lookup"><span data-stu-id="42a3b-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="42a3b-125">(0x3) – "NoChange"-파일 형식 또는 바로 가기를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42a3b-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="42a3b-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="42a3b-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-128">기본값 = 0x2</span><span class="sxs-lookup"><span data-stu-id="42a3b-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="42a3b-129">(0x0) – 동일한 게시 정보 원본에서 기존 항목을 제거 하 고 로컬에 추가 된 항목만 유지</span><span class="sxs-lookup"><span data-stu-id="42a3b-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="42a3b-130">(0x1) – "ServerOnly"-동일한 게시 정보 원본에 있는 오래 된 항목 및 로컬로 추가 된 항목을 제거 하 고 새 항목을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="42a3b-131">(0x2)-"ClientAndServer"-동일한 게시 정보 원본에서 오래 된 항목을 제거 하 고, 로컬로 추가 된 항목을 유지 하 고, 새 항목을 추가 합니다 (기본값은 없는 경우).</span><span class="sxs-lookup"><span data-stu-id="42a3b-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="42a3b-132">(0x3) – "NoChange"-파일 형식 또는 바로 가기를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="42a3b-133">**참고**  텍스트 값은 게시 XML 파일의 XML 특성에 대 한 값을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="42a3b-134">사용자 지정 HTTP 게시 솔루션을 구현한 경우 이러한 값을 수동으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42a3b-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





