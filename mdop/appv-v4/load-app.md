---
title: LOAD APP
description: LOAD APP
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816248"
---
# <span data-ttu-id="51f8e-103">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="51f8e-103">LOAD APP</span></span>


<span data-ttu-id="51f8e-104">지정 된 응용 프로그램과 패키지의 다른 모든 응용 프로그램을 파일 시스템 캐시로 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="51f8e-105">**참고**  **앱 로드** 명령을 실행 하면 로드 프로세스가 시작 되 고 바탕 화면 알림 영역에 진행률 표시줄이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="51f8e-106">이 프로세스가 시작 되 면 명령이 바로 종료 되므로 로드 오류는 동일한 위치에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="51f8e-107">바탕 화면 알림 영역을 사용 하지 않고 명령줄에서 로드 프로세스를 시작 하려면 **패키지 로드** 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="51f8e-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51f8e-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="51f8e-109">설명</span><span class="sxs-lookup"><span data-stu-id="51f8e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="51f8e-110">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="51f8e-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f8e-111">로드할 응용 프로그램의 이름과 버전 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="51f8e-112">/LOG</span><span class="sxs-lookup"><span data-stu-id="51f8e-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f8e-113">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="51f8e-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="51f8e-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f8e-115">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="51f8e-116">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="51f8e-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="51f8e-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="51f8e-118">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51f8e-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="51f8e-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="51f8e-119">Related topics</span></span>


[<span data-ttu-id="51f8e-120">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="51f8e-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





