---
title: mof 파일을 만들거나 편집하는 방법
description: mof 파일을 만들거나 편집하는 방법
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825323"
---
# <span data-ttu-id="a2e87-103">mof 파일을 만들거나 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="a2e87-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="a2e87-104">Configuration Manager를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하기 전에 구성 .mof 파일을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e87-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="a2e87-105">또한 사용 중인 구성 관리자 버전에 따라 Sms \ _def .mof 파일을 편집 하거나 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e87-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="a2e87-106">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="a2e87-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="a2e87-107">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서를 통해 BitLocker 준수 세부 정보를 보고할 수 있도록 하려면 Microsoft System Center Configuration Manager 2007 및 SystemCenter2012 ConfigurationManager에 대 한 구성. mof 파일을 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e87-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="a2e87-108">Configuration.mof 파일 편집</span><span class="sxs-lookup"><span data-stu-id="a2e87-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="a2e87-109">Sms \ _def .mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="a2e87-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="a2e87-110">클라이언트 컴퓨터가 MBAM Configuration Manager 보고서에서 BitLocker 준수 세부 정보를 보고할 수 있도록 설정 하려면, Sms \ _def .mof 파일을 만들거나 편집 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e87-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="a2e87-111">Configuration Manager 2007에서 파일이 이미 있으므로 기존 파일을 편집 하 고 덮어쓰지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2e87-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="a2e87-112">SystemCenter2012 ConfigurationManager를 사용 하는 경우에는 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2e87-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="a2e87-113">Sms \ _def .mof 파일 만들기 또는 편집</span><span class="sxs-lookup"><span data-stu-id="a2e87-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="a2e87-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a2e87-114">Related topics</span></span>


[<span data-ttu-id="a2e87-115">Configuration Manager에서 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="a2e87-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





