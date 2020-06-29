---
title: Microsoft Application Virtualization 4.6 SP2 정보
description: Microsoft Application Virtualization 4.6 SP2 정보
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820018"
---
# <span data-ttu-id="77d7c-103">Microsoft Application Virtualization 4.6 SP2 정보</span><span class="sxs-lookup"><span data-stu-id="77d7c-103">About Microsoft Application Virtualization 4.6 SP2</span></span>


<span data-ttu-id="77d7c-104">Microsoft App-v (Application Virtualization) 4.6 SP2는이 항목에서 설명 하는 몇 가지 향상 된 기능과 새로운 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-104">Microsoft Application Virtualization (App-V)4.6 SP2 provides several enhancements and new features, which are described in this topic.</span></span>

<span data-ttu-id="77d7c-105">**주의**  사항 이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-105">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="77d7c-106">Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-106">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="77d7c-107">레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-107">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="77d7c-108">Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-108">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="77d7c-109">레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-109">Change the registry at your own risk.</span></span>

 

**<span data-ttu-id="77d7c-110">Windows 8 및 Windows Server 2012에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="77d7c-110">Support for Windows 8 and Windows Server 2012</span></span>**

<span data-ttu-id="77d7c-111">App-v 4.6 SP2는 Windows 8 및 Windows Server 2012 원격 데스크톱 서비스에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-111">App-V4.6SP2 adds support for Windows 8 and Windows Server 2012 Remote Desktop Services.</span></span>

**<span data-ttu-id="77d7c-112">앱-V 5.0 클라이언트와 공존 지원</span><span class="sxs-lookup"><span data-stu-id="77d7c-112">Support for coexistence with App-V 5.0 client</span></span>**

<span data-ttu-id="77d7c-113">App-v 4.6 SP2는 Microsoft Application Virtualization 5.0 클라이언트와 공존을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-113">App-V4.6SP2 provides support for coexistence with the Microsoft Application Virtualization 5.0 client.</span></span> <span data-ttu-id="77d7c-114">App-v 클라이언트와 함께 사용할 App-v 5.0 클라이언트를 구성 하는 방법에 대 한 지침은 app-v 5.0 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77d7c-114">Review the App-V 5.0 documentation for instructions on how to configure the App-V 5.0 client for coexistence with the App-V4.6SP2 client.</span></span> <span data-ttu-id="77d7c-115">앱-V 5.0에 대 한 자세한 내용은 TechNet의 [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77d7c-115">For more information about App-V 5.0, see [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) on TechNet.</span></span>

**<span data-ttu-id="77d7c-116">보호 모드를 사용 하 여 Adobe Reader X를 가상화 할 수 있는 기능</span><span class="sxs-lookup"><span data-stu-id="77d7c-116">Ability to virtualize Adobe Reader X with Protected Mode</span></span>**

<span data-ttu-id="77d7c-117">다음 절차를 사용 하 여 보호 모드 기능을 켠 상태로 Adobe Reader X를 가상화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-117">You can virtualize Adobe Reader X with its Protected Mode feature turned on by using the following procedures.</span></span> <span data-ttu-id="77d7c-118">이전에는 Adobe Reader X를 가상화 하기 위해 보호 모드를 비활성화 했습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-118">Previously you had to disable Protected Mode in order to virtualize Adobe Reader X.</span></span>

<span data-ttu-id="77d7c-119">App-v 시퀀서를 시작 하기 전에 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides 아래에 다음 레지스트리 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-119">Before launching the App-V Sequencer, create the following registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="77d7c-120">이름</span><span class="sxs-lookup"><span data-stu-id="77d7c-120">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="77d7c-121">종류</span><span class="sxs-lookup"><span data-stu-id="77d7c-121">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="77d7c-122">데이터</span><span class="sxs-lookup"><span data-stu-id="77d7c-122">Data</span></span></p></td>
<td align="left"><p><span data-ttu-id="77d7c-123">설명</span><span class="sxs-lookup"><span data-stu-id="77d7c-123">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="77d7c-124">EnableVFSPassthrough</span><span class="sxs-lookup"><span data-stu-id="77d7c-124">EnableVFSPassthrough</span></span></p></td>
<td align="left"><p><span data-ttu-id="77d7c-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="77d7c-125">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="77d7c-126">raid-1</span><span class="sxs-lookup"><span data-stu-id="77d7c-126">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="77d7c-127"><strong> </strong> 실행 단계 중에 보호 모드에서 Adobe Reader X를 시작 하려면이 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-127">Set this value to <strong>1</strong> in order to start Adobe Reader X in Protected Mode during the launch phase.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="77d7c-128">**참고**  64 비트 운영 체제를 실행 하는 컴퓨터에서 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides. 아래에 레지스트리 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-128">**Note** On a computer running a 64-bit operating system, create the registry value under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.</span></span>

 

<span data-ttu-id="77d7c-129">Adobe Reader X 패키지의 각 OSD-파일에 대해 정책 요소 아래에 다음 항목을 추가 합니다 &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="77d7c-129">For each OSD-file in your Adobe Reader X package, add the following items under the &lt;POLICIES&gt; element:</span></span>

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**<span data-ttu-id="77d7c-130">새 Sequencer 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="77d7c-130">New Sequencer command-line parameter</span></span>**

<span data-ttu-id="77d7c-131">시퀀서 GUI를 통해 패키지 가속기 (PA)를 만들 때 패키지 가속기를 적용 하는 관리자에 게 패키징 및 배포 지침을 제공 하는 RTF 또는 TXT 파일을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-131">When you create a Package Accelerator (PA) through the Sequencer GUI, you can select an RTF or TXT file that provides packaging and deployment guidance to the administrators who will apply the Package Accelerator.</span></span> <span data-ttu-id="77d7c-132">이제 시퀀서 CLI를 사용 하 여이 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-132">This functionality is now available using the Sequencer CLI.</span></span>

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

<span data-ttu-id="77d7c-133">패키지 가속기를 만들 때 패키징 및 배포 지침을 제공 하는 RTF 또는 TXT 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-133">Specify a path to an RTF or TXT file that provides packaging and deployment guidance when creating a Package Accelerator.</span></span>

**<span data-ttu-id="77d7c-134">Microsoft 응용 프로그램 오류 보고 기능을 더 이상 설치 하지 않아도 됨</span><span class="sxs-lookup"><span data-stu-id="77d7c-134">Microsoft Application Error Reporting no longer needs to be installed</span></span>**

<span data-ttu-id="77d7c-135">setup.msi를 사용 하 여 App-v 4.6 SP2 클라이언트를 설치 하는 경우에는 더 이상 Microsoft 응용 프로그램 오류 보고 (dw20shared.msi)를 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-135">When you are installing the App-V4.6SP2 client by using setup.msi, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="77d7c-136">앱-V 4.6 SP2는 이제 Microsoft 오류 보고를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-136">App-V4.6SP2 now uses Microsoft Error Reporting.</span></span> <span data-ttu-id="77d7c-137">자세한 내용은 [Setup.msi를 사용 하 여 App-v 클라이언트를 설치 하는 방법을 ](https://go.microsoft.com/fwlink/?LinkId=267237)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77d7c-137">For more information, see [How to Install the App-V Client by Using Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).</span></span>

**<span data-ttu-id="77d7c-138">고객 의견 및 핫픽스 롤업</span><span class="sxs-lookup"><span data-stu-id="77d7c-138">Customer feedback and hotfix rollup</span></span>**

<span data-ttu-id="77d7c-139">App-v 4.6 SP2에는 App-v 4.6 SP1 릴리스 이후 발견 된 문제를 해결 하기 위한 해결 롤업이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-139">App-V4.6SP2 includes a rollup of fixes to address issues found since the App-V 4.6 SP1 release.</span></span> <span data-ttu-id="77d7c-140">App-v 4.6 SP2에는 Microsoft Application Virtualization 4.6 SP1 핫픽스 6에 대 한 최신 수정 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-140">App-V4.6SP2 contains the latest fixes up to and including Microsoft Application Virtualization 4.6 SP1 Hotfix 6.</span></span>

## <span data-ttu-id="77d7c-141">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="77d7c-141">In This Section</span></span>


<a href="" id="app-v-4-6-sp2-release-notes"></a>[<span data-ttu-id="77d7c-142">App-V 4.6 SP2 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="77d7c-142">App-V 4.6 SP2 Release Notes</span></span>](https://go.microsoft.com/fwlink/?LinkId=267600)  
<span data-ttu-id="77d7c-143">앱-V 4.6 SP2의 알려진 문제에 대 한 최신 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="77d7c-143">Provides the most up-to-date information about known issues with App-V4.6SP2.</span></span>

 

 





