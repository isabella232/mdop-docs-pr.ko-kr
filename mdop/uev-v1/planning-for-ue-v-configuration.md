---
title: UE-V 구성 계획
description: UE-V 구성 계획
author: dansimp
ms.assetid: db78dad4-78e0-45d6-a235-8b7345cb79f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce21afc7b7e8ee183b4fb86de7dea6eeaa58953e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826823"
---
# <span data-ttu-id="79f05-103">UE-V 구성 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-103">Planning for UE-V Configuration</span></span>


<span data-ttu-id="79f05-104">제공 되는 응용 프로그램 및 UE-V 동작을 정의 하는 구성을 정의 하 여 엔터프라이즈의 특정 요구에 맞게 Microsoft UE-V (사용자 환경 가상화)를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-104">You can configure Microsoft User Experience Virtualization (UE-V) to meet the specific needs of your enterprise by defining which applications are deployed and which configurations define the UE-V behavior.</span></span>

## <span data-ttu-id="79f05-105">UE-V를 사용 하 여 동기화 할 응용 프로그램 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-105">Plan which applications to synchronize with UE-V</span></span>


<span data-ttu-id="79f05-106">UE-V는 미리 정의 된 설정 위치 템플릿 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-106">UE-V includes a set of predefined settings location templates.</span></span> <span data-ttu-id="79f05-107">또한 UE-V를 사용 하면 관리자가 엔터프라이즈에서 사용 되는 타사 또는 lob (기간 업무) 응용 프로그램을 비롯 한 다른 응용 프로그램용 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-107">UE-V also allows administrators to create custom settings location templates for other applications, including third-party or line-of-business applications that are used in the enterprise.</span></span> <span data-ttu-id="79f05-108">이 항목에는 UE-V 클라이언트에 포함 된 응용 프로그램 목록과 사용자 지정 설정 위치 템플릿을 포함 하는 방법에 대 한 지침이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-108">This topic includes a list of applications that are included with the UE-V client and guidance on how to include custom settings location templates.</span></span>

[<span data-ttu-id="79f05-109">UE-V 1.0과 동기화할 응용 프로그램 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-109">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

## <span data-ttu-id="79f05-110">UE-V의 lob (기간 업무) 응용 프로그램 평가를 위한 검사 목록</span><span class="sxs-lookup"><span data-stu-id="79f05-110">Checklist for Evaluating Line-of-Business Applications for UE-V</span></span>


<span data-ttu-id="79f05-111">Lob (기간 업무) 응용 프로그램을 동기화할지 여부에 대 한 지침입니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-111">Guidance on whether a line-of-business application should be synchronized.</span></span>

[<span data-ttu-id="79f05-112">UE-V 1.0에 대한 기간 업무 응용 프로그램을 평가하기 위한 검사 목록</span><span class="sxs-lookup"><span data-stu-id="79f05-112">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md)

## <span data-ttu-id="79f05-113">사용자 지정 서식 파일 배포 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-113">Plan custom template deployment</span></span>


<span data-ttu-id="79f05-114">타사 응용 프로그램을 비롯 한 다른 응용 프로그램을 지원 하려면 UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들고 설정 템플릿 카탈로그에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-114">In order to support other applications, including third-party applications, you must create custom settings location templates by using the UE-V Generator, and deploy them to a settings template catalog.</span></span>

[<span data-ttu-id="79f05-115">UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-115">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

## <span data-ttu-id="79f05-116">UE-V 구성 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-116">Plan for UE-V configuration</span></span>


<span data-ttu-id="79f05-117">UE-V 구성은 엔터프라이즈 전체에서 설정을 동기화 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-117">UE-V configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="79f05-118">이러한 구성은 UE-V Agent를 배포 하기 전이나 후에 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-118">These configurations can be made before, during, or after the UE-V Agent is deployed.</span></span> <span data-ttu-id="79f05-119">UE-V는 다양 한 구성 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f05-119">UE-V provides a variety of configuration methods</span></span>

[<span data-ttu-id="79f05-120">UE-V 구성 방법 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-120">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

## <span data-ttu-id="79f05-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="79f05-121">Related topics</span></span>


[<span data-ttu-id="79f05-122">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="79f05-122">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





