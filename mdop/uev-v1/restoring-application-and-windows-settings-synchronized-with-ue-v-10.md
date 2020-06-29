---
title: UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원
description: UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812377"
---
# <span data-ttu-id="74e9f-103">UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원</span><span class="sxs-lookup"><span data-stu-id="74e9f-103">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>


<span data-ttu-id="74e9f-104">Microsoft UE-V (User Experience Virtualization)의 WMI 및 PowerShell 기능은 설정 패키지를 복원할 수 있는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-104">WMI and PowerShell features of Microsoft User Experience Virtualization (UE-V) provide the ability to restore settings packages.</span></span> <span data-ttu-id="74e9f-105">WMI 및 PowerShell 명령을 사용 하면 UE-V Agent가 설치 된 후 처음으로 응용 프로그램을 시작할 때 컴퓨터에 있던 설정 값으로 응용 프로그램 및 Windows 설정을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-105">WMI and PowerShell commands allow you to restore application and Windows settings to the settings values that were on the computer the first time the application launched after the UE-V Agent was installed.</span></span> <span data-ttu-id="74e9f-106">이 복원 작업은 응용 프로그램 또는 Windows 설정 기준에 따라 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-106">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="74e9f-107">이 설정은 다음에 응용 프로그램을 실행 하거나 사용자가 운영 체제에 로그온 할 때 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-107">The settings are restored the next time that the application is run or when the user logs on to the operating system.</span></span>

**<span data-ttu-id="74e9f-108">PowerShell을 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="74e9f-108">To restore application settings and Windows settings with PowerShell</span></span>**

1.  <span data-ttu-id="74e9f-109">Windows PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-109">Open the Windows PowerShell window.</span></span> <span data-ttu-id="74e9f-110">Microsoft UE-V PowerShell 모듈을 가져오려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-110">To import the Microsoft UE-V PowerShell module, enter the following command:</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="74e9f-111">다음 PowerShell cmdlet을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-111">Enter the following PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="74e9f-112">PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74e9f-112">PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="74e9f-113">설명</span><span class="sxs-lookup"><span data-stu-id="74e9f-113">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="74e9f-114">Restore UevUserSetting</span><span class="sxs-lookup"><span data-stu-id="74e9f-114">Restore-UevUserSetting</span></span></p></td>
    <td align="left"><p><span data-ttu-id="74e9f-115">응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-115">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="74e9f-116">WMI를 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="74e9f-116">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="74e9f-117">PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-117">Open a PowerShell window.</span></span>

2.  <span data-ttu-id="74e9f-118">다음 WMI 명령을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-118">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="74e9f-119">WMI 명령</span><span class="sxs-lookup"><span data-stu-id="74e9f-119">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="74e9f-120">설명</span><span class="sxs-lookup"><span data-stu-id="74e9f-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="74e9f-121">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</span><span class="sxs-lookup"><span data-stu-id="74e9f-121">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="74e9f-122">응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74e9f-122">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="74e9f-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="74e9f-123">Related topics</span></span>


[<span data-ttu-id="74e9f-124">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="74e9f-124">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="74e9f-125">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="74e9f-125">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





