---
title: DaRT 10 릴리스 정보
description: DaRT 10 릴리스 정보
author: dansimp
ms.assetid: eb996980-f9c4-42cb-bde9-6b3d4b82b58c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ae5865538155f3c9ecf8b5f23b0d9e23232833
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822953"
---
# <span data-ttu-id="e9a0c-103">DaRT 10 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="e9a0c-103">Release Notes for DaRT 10</span></span>


**<span data-ttu-id="e9a0c-104">이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="e9a0c-105">Microsoft 진단 및 복구 도구 집합 (DaRT) 10을 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span></span>

<span data-ttu-id="e9a0c-106">이 릴리스 정보에는 진단 및 복구 도구 집합 10을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 10.</span></span> <span data-ttu-id="e9a0c-107">릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="e9a0c-108">이러한 릴리스 정보와 기타 DaRT 설명서가 서로 다르면 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="e9a0c-109">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="e9a0c-110">DaRT 10의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="e9a0c-110">Known issues with DaRT 10</span></span>


### <span data-ttu-id="e9a0c-111">Windows 10의 실제 파티션에서 손상 된 마스터 부팅 레코드를 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-111">Disk Commander is unable to repair a corrupt master boot record in a physical partition in Windows 10</span></span>

<span data-ttu-id="e9a0c-112">Windows 10에서 디스크 책임자의 "MBR (마스터 부트 레코드) 또는 GPT (GUID 파티션 테이블)" 옵션의 헤더가 실제 파티션에서 손상 된 마스터 부팅 레코드를 복구할 수 없으므로 클라이언트 컴퓨터를 부팅할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-112">In Windows 10, the “Restore the Master Boot Record (MBR) or the header of the GUID Partition Table (GPT)” option in Disk Commander is unable to repair a corrupt master boot record in a physical partition, and therefore is unable to boot the client computer.</span></span>

<span data-ttu-id="e9a0c-113">**해결 방법:** **시동 복구**를 시작 하 **고 문제 해결**을 클릭 한 다음 **고급 옵션**을 클릭 하 고 **복구 시작**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-113">**Workaround:** Start **Startup Repair**, click **Troubleshoot**, click **Advanced options**, and then click **Start repair**.</span></span>

### <span data-ttu-id="e9a0c-114">같은 드라이브를 대상으로 하는 디스크 지우기의 여러 인스턴스는 오류를 보고 하기 위해 마지막 하나를 제외한 모든 인스턴스를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-114">Multiple instances of Disk Wipe that target the same drive cause all instances except the last one to report a failure</span></span>

<span data-ttu-id="e9a0c-115">디스크 지우기의 여러 인스턴스를 시작한 다음 두 개의 별도 디스크 지우기 인스턴스를 사용 하 여 같은 드라이브를 초기화 하려고 하면 마지막 레코드를 제외한 모든 인스턴스가 드라이브를 지우는 데 실패 한 것으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-115">If you start multiple instances of Disk Wipe, and then try to wipe the same drive by using two separate Disk Wipe instances, all instances except the last one report a failure to wipe the drive.</span></span>

<span data-ttu-id="e9a0c-116">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-116">**Workaround:** None.</span></span>

### <span data-ttu-id="e9a0c-117">플래시 메모리가 있는 고체 드라이브의 모든 데이터를 지울 수 없는 경우 디스크 지우기</span><span class="sxs-lookup"><span data-stu-id="e9a0c-117">Disk Wipe may not clear all data on solid-state drives that have flash memory</span></span>

<span data-ttu-id="e9a0c-118">플래시 메모리가 있는 SSD (고체 드라이브)에서 디스크 지우기를 사용 하 여 데이터를 지우는 경우 모든 데이터가 지워지지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-118">If you use Disk Wipe to clear data on a solid-state drive (SSD) that has flash memory, all of the data may not be erased.</span></span> <span data-ttu-id="e9a0c-119">이 문제는 SSD 펌웨어가 디스크 정리가 실행 되는 동안 쓰기의 실제 위치를 제어 하기 때문에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-119">This issue occurs because the SSD firmware controls the physical location of writes while Disk Wipe is running.</span></span>

<span data-ttu-id="e9a0c-120">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-120">**Workaround:** None.</span></span>

### <span data-ttu-id="e9a0c-121">Locksmith 마법사 또는 레지스트리 편집기를 실행할 때 시스템 복원이 실패 함</span><span class="sxs-lookup"><span data-stu-id="e9a0c-121">System restore fails when you run Locksmith Wizard or Registry Editor</span></span>

<span data-ttu-id="e9a0c-122">Locksmith 마법사, 레지스트리 편집기 및 기타 도구를 실행 하면 시스템 복원이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-122">If you run Locksmith Wizard, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="e9a0c-123">**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 시스템 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-123">**Workaround:** Close and restart DaRT, and then start System Restore.</span></span>

### <span data-ttu-id="e9a0c-124">Locksmith 마법사 또는 컴퓨터 관리를 시작 하 고 닫은 후 SFC (시스템 파일 검사기) 검사가 실행 되지 않음</span><span class="sxs-lookup"><span data-stu-id="e9a0c-124">System File Checker (SFC) Scan fails to run after you start and close Locksmith Wizard or Computer Management</span></span>

<span data-ttu-id="e9a0c-125">Locksmith 마법사 또는 컴퓨터 관리에서 도구를 시작 하 고 닫으면 시스템 파일 검사기가 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-125">If you start and then close Locksmith Wizard or tools in Computer Management, System File Checker fails to run.</span></span>

<span data-ttu-id="e9a0c-126">**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 시스템 파일 검사기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-126">**Workaround:** Close and restart DaRT, and then start System File Checker.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> <span data-ttu-id="e9a0c-127">Windows 평가 및 배포 키트가 설치 되어 있지 않으면 DaRT 설치 프로그램이 실패 하지 않음</span><span class="sxs-lookup"><span data-stu-id="e9a0c-127">DaRT installer does not fail when the Windows Assessment and Deployment Kit is not installed</span></span>

<span data-ttu-id="e9a0c-128">명령줄을 사용 하 여 Windows Installer (.msi)를 실행 하 여 DaRT 10을 설치 하 고 Windows Adk (평가 및 배포 키트)가 설치 되지 않은 경우 DaRT 설치는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-128">If you install DaRT 10 by using the command line to run the Windows Installer (.msi), and the Windows Assessment and Deployment Kit (WindowsADK) has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="e9a0c-129">현재 DaRT 10 설치자는 DaRT 복구 이미지를 제외한 모든 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-129">Currently, the DaRT 10 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="e9a0c-130">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="e9a0c-130">**Workaround:** None.</span></span>

## <span data-ttu-id="e9a0c-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e9a0c-131">Related topics</span></span>


[<span data-ttu-id="e9a0c-132">DaRT 10 정보</span><span class="sxs-lookup"><span data-stu-id="e9a0c-132">About DaRT 10</span></span>](about-dart-10.md)

 

 





