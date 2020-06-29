---
title: 관리자 컴퓨터에 DaRT 8.0 배포
description: 관리자 컴퓨터에 DaRT 8.0 배포
author: dansimp
ms.assetid: f918ead8-742e-464a-8bf6-1fcedde66cae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0ab001f612f2257ecbd77c39319cc99c17d36197
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824123"
---
# <span data-ttu-id="40d9b-103">관리자 컴퓨터에 DaRT 8.0 배포</span><span class="sxs-lookup"><span data-stu-id="40d9b-103">Deploying DaRT 8.0 to Administrator Computers</span></span>


<span data-ttu-id="40d9b-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 배포를 시작 하기 전에 해당 환경에 대 한 요구 사항을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="40d9b-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, review the requirements for your environment.</span></span> <span data-ttu-id="40d9b-105">여기에는 DaRT 8.0을 설치 하기 위한 하드웨어 요구 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-105">This includes the hardware requirements for installing DaRT 8.0.</span></span> <span data-ttu-id="40d9b-106">DaRT 하드웨어 및 소프트웨어 요구 사항에 대 한 자세한 내용은 [dart 8.0 지원 구성을](dart-80-supported-configurations-dart-8.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40d9b-106">For more information about DaRT hardware and software requirements, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md).</span></span>

<span data-ttu-id="40d9b-107">이 섹션의 항목을 사용 하 여 환경 및 배포 전략에 따라 엔터프라이즈에 DaRT를 배포 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="40d9b-108">DaRT 8.0 배포</span><span class="sxs-lookup"><span data-stu-id="40d9b-108">Deploy DaRT 8.0</span></span>


<span data-ttu-id="40d9b-109">Dart 용 Windows Installer 파일을 사용 하 여 먼저 DaRT 복구 이미지를 만든 다음 최종 사용자 컴퓨터를 문제 해결 하 고 해결 하는 데 사용할 컴퓨터에 DaRT를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="40d9b-110">일반적으로 조직에서 DaRT 복구 이미지를 만드는 데 필요한 DaRT 기능만 관리자 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="40d9b-111">그런 다음 헬프 데스크 관리자의 컴퓨터에서 DaRT 원격 연결 뷰어와 충돌 분석기와 같은 문제 컴퓨터 문제를 해결 하는 데 필요한 DaRT 기능만 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="40d9b-112">Windows Installer 파일을 수동으로 실행 하 여 DaRT를 설치 하는 것 외에도 명령 프롬프트에서 DaRT를 설치 하 여 SystemCenterConfigurationManager2012 등의 엔터프라이즈 소프트웨어 배포 시스템을 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="40d9b-113">DaRT 8.0을 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="40d9b-113">How to Deploy DaRT 8.0</span></span>](how-to-deploy-dart-80-dart-8.md)

## <span data-ttu-id="40d9b-114">DaRT 8.0 변경, 복구 또는 제거</span><span class="sxs-lookup"><span data-stu-id="40d9b-114">Change, repair, or remove DaRT 8.0</span></span>


<span data-ttu-id="40d9b-115">Dart 설치 파일을 두 번 클릭 한 다음 수행 하려는 작업에 해당 하는 단추를 클릭 하거나 Windows 제어판을 통해 DaRT 설치를 변경, 복구 또는 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40d9b-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="40d9b-116">DaRT 8.0을 변경, 복구 또는 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="40d9b-116">How to Change, Repair, or Remove DaRT 8.0</span></span>](how-to-change-repair-or-remove-dart-80-dart-8.md)

## <span data-ttu-id="40d9b-117">DaRT 8.0를 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="40d9b-117">How to get DaRT 8.0</span></span>


<span data-ttu-id="40d9b-118">DaRT 소프트웨어를 다운로드 하려면 MDOP를 [얻는 방법을](https://go.microsoft.com/fwlink/?LinkId=322049)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40d9b-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="40d9b-119">DaRT 8.0을 관리자 컴퓨터에 배포 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="40d9b-119">Other resources for deploying the DaRT 8.0 to administrator computers</span></span>


[<span data-ttu-id="40d9b-120">DaRT 8.0 배포</span><span class="sxs-lookup"><span data-stu-id="40d9b-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





