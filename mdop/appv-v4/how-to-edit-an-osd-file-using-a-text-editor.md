---
title: 텍스트 편집기를 사용하여 OSD 파일을 편집하는 방법
description: 텍스트 편집기를 사용하여 OSD 파일을 편집하는 방법
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817443"
---
# <span data-ttu-id="f4207-103">텍스트 편집기를 사용하여 OSD 파일을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="f4207-103">How to Edit an OSD File Using a Text Editor</span></span>


<span data-ttu-id="f4207-104">텍스트 편집기를 사용 하 여 OSD (개방형 소프트웨어 설명자) 파일을 편집 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-104">Use the following procedure to edit an Open Software Descriptor (OSD) file by using a text editor.</span></span>

**<span data-ttu-id="f4207-105">텍스트 편집기를 사용 하 여 OSD 파일을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="f4207-105">To edit an OSD file by using a text editor</span></span>**

1.  <span data-ttu-id="f4207-106">모든 XML 또는 ASCII 텍스트 편집기 (예: Microsoft 메모장)를 사용 하 여 OSD 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-106">Open the OSD file using any XML or ASCII text editor—for example, Microsoft Notepad.</span></span>

    <span data-ttu-id="f4207-107">**참고**  OSD 파일을 수정 하기 전에 설치 디렉터리에서 XSD 파일에 의해 규정 된 스키마를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-107">**Note** Before modifying the OSD file, read the schema prescribed by the XSD file in the install directory.</span></span> <span data-ttu-id="f4207-108">이 스키마를 따르지 않으면 시퀀싱 된 응용 프로그램이 성공적으로 시작 되지 않도록 하는 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-108">Failing to follow this schema might introduce errors that prevent a sequenced application from starting successfully.</span></span>

     

2.  <span data-ttu-id="f4207-109">선택한 XML 또는 ASCII 텍스트 편집기를 사용 하 여 OSD 파일을 편집 하 고, 지정 된 스키마를 준수 하 고 다음 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-109">Edit the OSD file using your XML or ASCII text editor of choice, adhering to the prescribed schema and the following guidelines:</span></span>

    1.  <span data-ttu-id="f4207-110">명명 된 요소가 SOFTPKG root 요소 내에 중첩 되어 있는지 확인 &lt; &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-110">Ensure that named elements are nested within the &lt;SOFTPKG&gt; root element.</span></span>

    2.  <span data-ttu-id="f4207-111">요소 이름이 모두 대문자로 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-111">Ensure that element names are in all uppercase letters.</span></span>

    3.  <span data-ttu-id="f4207-112">특성 값은 대/소문자를 구분 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4207-112">Be aware that attribute values are case sensitive.</span></span>

    4.  <span data-ttu-id="f4207-113">신중 하 게 입력 하 고 XML 사양을 관찰 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4207-113">Type carefully, and observe the XML specifications.</span></span>

## <span data-ttu-id="f4207-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f4207-114">Related topics</span></span>


[<span data-ttu-id="f4207-115">OSD 탭 정보</span><span class="sxs-lookup"><span data-stu-id="f4207-115">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="f4207-116">OSD 파일을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="f4207-116">How to Edit an OSD File</span></span>](how-to-edit-an-osd-file.md)

[<span data-ttu-id="f4207-117">OSD 파일 요소</span><span class="sxs-lookup"><span data-stu-id="f4207-117">OSD File Elements</span></span>](osd-file-elements.md)

 

 





