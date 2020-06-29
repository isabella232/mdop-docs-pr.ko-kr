---
title: 템플릿 만들기 및 기본 템플릿 설정
description: 템플릿 만들기 및 기본 템플릿 설정
author: dansimp
ms.assetid: ffa72c2a-64eb-4492-8072-c3a66179b546
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0c415ab2fba994eff14caf9ec557e2ba8ccacfa5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821043"
---
# <span data-ttu-id="adcd4-103">템플릿 만들기 및 기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="adcd4-103">Creating a Template and Setting a Default Template</span></span>


<span data-ttu-id="adcd4-104">서식 파일을 만들면 새 Gpo를 만들기 위한 출발점으로 사용할 특정 버전의 GPO (그룹 정책 개체)에 대 한 모든 설정을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-104">Creating a template enables you to save all the settings of a particular version of a Group Policy Object (GPO) to use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="adcd4-105">편집기로 사용할 수 있는 서식 파일 중에서 새 Gpo를 만드는 모든 그룹 정책 관리자에 대 한 기본 서식 파일을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-105">As an Editor, you can also specify which of the available templates will be the default template for all Group Policy administrators creating new GPOs.</span></span>

<span data-ttu-id="adcd4-106">서식 파일의 몇 가지 사용 가능한 용도는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-106">Some potential uses for a template include the following:</span></span>

-   <span data-ttu-id="adcd4-107">조직에서 도메인 간에 다시 사용할 수 있는 보안 기준을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-107">Create a security baseline that your organization can reuse across domains.</span></span>

-   <span data-ttu-id="adcd4-108">조직에서 각 부서에 대해 사용자 지정할 수 있는 폴더 리디렉션 및 오프 라인 파일을 관리 하는 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-108">Create a template to manage folder redirection and offline files that your organization can customize for each department.</span></span>

-   <span data-ttu-id="adcd4-109">조직에서 여러 지리적 영역에 대 한 무선 네트워크 연결을 구성 하는 데 사용할 수 있는 무선 네트워킹 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-109">Create a wireless networking template that your organization can use to configure wireless network connections for different geographical areas.</span></span>

-   <span data-ttu-id="adcd4-110">로컬 네트워크 관리자를 위한 규제 준수 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-110">Create regulatory compliance templates for local network administrators.</span></span>

-   <span data-ttu-id="adcd4-111">기존 GPO의 읽기 전용 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-111">Create a read-only snapshot of an existing GPO.</span></span>

<span data-ttu-id="adcd4-112">**참고**  서식 파일은 편집할 수 없는 GPO의 정적 버전 이지만 편집 가능한 새 Gpo를 만들기 위한 시작 위치로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-112">**Note** A template is a static version of a GPO that cannot be edited, yet can be used as a starting point for creating new, editable GPOs.</span></span> <span data-ttu-id="adcd4-113">서식 파일을 삭제 하거나 이름을 변경 해도 해당 서식 파일에서 만든 Gpo에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adcd4-113">Renaming or deleting a template does not affect GPOs created from that template.</span></span>

 

-   [<span data-ttu-id="adcd4-114">템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="adcd4-114">Create a Template</span></span>](create-a-template-agpm40.md)

-   [<span data-ttu-id="adcd4-115">기본 템플릿 설정</span><span class="sxs-lookup"><span data-stu-id="adcd4-115">Set a Default Template</span></span>](set-a-default-template-agpm40.md)

 

 





