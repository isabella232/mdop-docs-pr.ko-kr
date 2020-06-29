---
title: App-V 업그레이드 검사 목록
description: App-V 업그레이드 검사 목록
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819738"
---
# <span data-ttu-id="66594-103">App-V 업그레이드 검사 목록</span><span class="sxs-lookup"><span data-stu-id="66594-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="66594-104">Microsoft Application Virtualization (App-v) 4.5 이상 버전으로 업그레이드 하기 전에 앱-V 4.1 이전의 모든 버전을 App-v 4.1로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="66594-105">먼저 클라이언트를 업그레이드 한 다음 서버 구성 요소를 업그레이드 하도록 계획 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="66594-106">App-v 4.5으로 업그레이드 된 app-v 클라이언트는 아직 업그레이드 되지 않은 App-v 서버와 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="66594-107">이전 버전의 클라이언트는 App-v 4.5으로 업그레이드 된 서버에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="66594-108">단계</span><span class="sxs-lookup"><span data-stu-id="66594-108">Step</span></span></th>
<th align="left"><span data-ttu-id="66594-109">참고자료</span><span class="sxs-lookup"><span data-stu-id="66594-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-110">App-v 클라이언트를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="66594-111">Application Virtualization Client를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="66594-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-112">App-v 서버 및 데이터베이스를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="66594-113">중요</span><span class="sxs-lookup"><span data-stu-id="66594-113">Important</span></span></strong><br/><p><span data-ttu-id="66594-114">두 개 이상의 서버에서 App-v 데이터베이스에 대 한 액세스를 공유 하는 경우 데이터베이스를 업그레이드 하는 동안 해당 서버를 모두 오프 라인 상태로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="66594-115">데이터베이스 업그레이드에 대 한 일반적인 비즈니스 지침을 따르고 있지만 테스트 서버에서 먼저 데이터베이스의 백업 복사본을 사용 하 여 데이터베이스 업그레이드를 테스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="66594-116">그런 다음 데이터베이스 스키마를 업그레이드 하는 첫 번째 업그레이드에 대 한 서버 중 하나를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="66594-117">프로덕션 데이터베이스가 성공적으로 업그레이드 되 면 다른 서버의 App-v 소프트웨어를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="66594-118">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="66594-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-119">App-v 관리 웹 서비스를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="66594-120">이 단계는 관리 웹 서비스가 별도의 서버에 있는 경우에만 적용 되며,이 경우 관리 웹 서비스를 업그레이드 하려면 별도의 서버에서 서버 설치 관리자 프로그램을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="66594-121">그렇지 않으면 이전 서버 업그레이드 단계에서 관리 웹 서비스를 자동으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="66594-122">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="66594-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-123">App-v 관리 콘솔을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="66594-124">이 단계는 관리 콘솔이 별도의 컴퓨터에 있는 경우에만 적용 되 고 콘솔을 업그레이드 하려면 별도의 컴퓨터에서 서버 설치 관리자 프로그램을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="66594-125">그렇지 않은 경우에는 이전 서버 업그레이드 단계에서 관리 콘솔을 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="66594-126">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="66594-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-127">앱-V 시퀀서를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="66594-128">Application Virtualization Sequencer 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="66594-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="66594-129">추가 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="66594-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="66594-130">버전 4.2에서 시퀀싱 된 모든 가상 응용 프로그램 패키지는 버전 4.5에서 사용할 수 있도록 다시 시퀀싱 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66594-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="66594-131">그러나 기본 Acl (액세스 제어 목록)을 적용 하거나 Windows Installer 파일을 생성 하려면 가상 패키지를 Microsoft Application Virtualization 4.5 형식으로 업그레이드 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="66594-132">이는 간단한 프로세스 이며, 기존 가상 응용 프로그램 패키지를 열어서 App-v 4.5 Sequencer를 사용 하 여 저장할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="66594-133">이는 앱-VSequencer 명령줄 인터페이스를 사용 하 여 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="66594-134">자세한 내용은 [App-v 시퀀서를 사용 하 여 가상 응용 프로그램을 만들거나 업그레이드 하는 방법](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="66594-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="66594-135">4.5 시퀀서의 기능 중 하나는 Microsoft 끝점 구성 관리자와 같은 ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 가상 응용 프로그램 패키지의 제어 지점으로 Windows Installer (.msi) 파일을 만드는 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="66594-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="66594-136">앱-v 4.1 또는 4.2 4.5 클라이언트에 설치 된 응용 프로그램 가상화 용 MSI 도구를 사용 하 여 만든 이전 Windows Installer 파일은 App-v 4.5 클라이언트에 설치 되지 않지만 계속 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="66594-137">그러나 App-v 4.5 Sequencer에서 업그레이드 하지 않는 한 제거 하거나 업그레이드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="66594-138">4.5 이전의 원래 App-v 패키지는 App-v 4.5 Sequencer에서 열어야 하 고 Windows Installer 파일로 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="66594-139">참고</span><span class="sxs-lookup"><span data-stu-id="66594-139">Note</span></span>**  
    <span data-ttu-id="66594-140">App-v 4.2 클라이언트가 이미 App-v 4.5으로 업그레이드 한 경우 버전 4.5 클라이언트에 버전 4.2 패키지를 보존 하 고 관리 하도록 허용 하는 방법에 대 한 해결 방법을 스크립팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="66594-141">이 스크립트는 msvcp71.dll 및 msvcr71.dll의 두 파일을 App-v 설치 폴더에 복사 하 고 레지스트리 키 아래에 다음 레지스트리 키 값을 설정 해야 합니다. \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="66594-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="66594-142">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="66594-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="66594-143">"GlobalDataDirectory" = "C:\\\\Documents 및 Settings\\\\All Users\\\\Documents\\\\" (전역적으로 쓰기 가능한 위치)</span><span class="sxs-lookup"><span data-stu-id="66594-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="66594-144">App-v 4.5 Sequencer에서 생성 된 Windows Installer 파일은 App-v 4.6 클라이언트에서 실행 하려고 할 때 "이 패키지에 Microsoft Application Virtualization 클라이언트 4.5 이상"이 필요 합니다. 라는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66594-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="66594-145">App-v 4.5 SP1 Sequencer 또는 App-v 4.6 Sequencer를 사용 하 여 이전 패키지를 열고 패키지에 대 한 새 .msi 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="66594-146">서버를 버전 4.5으로 업그레이드 하면 생성 및 저장 된 모든 버전 4.2 보고서가 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="66594-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="66594-147">이러한 보고서를 유지 해야 하는 경우 서버의 SoftGrid 관리 콘솔 폴더에 있는 SftMMC .msc 파일의 백업 복사본을 저장 하 고 해당 복사본을 사용 하 여 업그레이드 중에 설치 된 새 SftMMC를 대체 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="66594-148">이전 버전에서 업그레이드 하는 방법에 대 한 자세한 내용은 [Microsoft Application Virtualization 4.5 질문과 대답 ()으로 업그레이드](https://go.microsoft.com/fwlink/?LinkId=120358) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="66594-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="66594-149">앱-V 4.6 클라이언트 패키지 지원</span><span class="sxs-lookup"><span data-stu-id="66594-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="66594-150">이전 버전의 App-v (app-v 4.6 클라이언트)에서 만든 패키지를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="66594-151">그러나 적절 한 운영 체제 및 칩 아키텍처 정보가 포함 되도록 관련 된 .osd 파일을 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="66594-152">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="66594-153">OS 값</span><span class="sxs-lookup"><span data-stu-id="66594-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-154">&lt;OS 값 = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-155">&lt;OS 값 = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-156">&lt;OS 값 = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-157">&lt;OS 값 = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-158">&lt;OS 값 = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-159">&lt;OS 값 = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-160">&lt;OS 값 = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-161">&lt;OS 값 = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-162">&lt;OS 값 = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-163">&lt;OS 값 = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-164">&lt;OS 값 = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="66594-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="66594-165">새로 만든 32 비트 패키지를 실행 하려면 App-v 4.6 Sequencer가 설치 된 32 비트 운영 체제를 실행 하는 컴퓨터에서 응용 프로그램을 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="66594-166">응용 프로그램을 시퀀싱 한 후에는 시퀀서 콘솔에서 **배포** 탭을 클릭 한 다음 필요에 따라 적절 한 운영 체제와 칩 아키텍처를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="66594-167">중요</span><span class="sxs-lookup"><span data-stu-id="66594-167">Important</span></span>**  
<span data-ttu-id="66594-168">64 비트 운영 체제를 실행 하는 컴퓨터에서 시퀀싱 된 응용 프로그램은 64 비트 운영 체제를 실행 하는 컴퓨터에 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="66594-169">새로운 32-app-v 4.6 Sequencer를 사용 하 여 만든 비트 패키지는 App-v 4.5 클라이언트를 실행 하는 컴퓨터에서 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="66594-170">App-v 4.6 클라이언트에서 새 64 비트 패키지를 실행 하려면 App-v 4.6 Sequencer를 실행 하는 컴퓨터에서 응용 프로그램을 시퀀싱 하 고 64 비트 운영 체제를 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="66594-171">응용 프로그램을 시퀀싱 한 후에는 시퀀서 콘솔에서 **배포** 탭을 클릭 한 다음 필요에 따라 적절 한 운영 체제와 칩 아키텍처를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66594-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="66594-172">다음 표에는 다양 한 버전의 시퀀서를 사용 하 여 만든 패키지를 실행 하는 클라이언트 버전이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66594-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="66594-173">App-V 4.2 Sequencer를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="66594-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="66594-174">App-V 4.5 Sequencer를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="66594-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="66594-175">32 비트 앱-V 4.6 시퀀서를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="66594-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="66594-176">64 비트 앱-V 4.6 시퀀서를 사용 하 여 시퀀싱</span><span class="sxs-lookup"><span data-stu-id="66594-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-177">4.2 클라이언트</span><span class="sxs-lookup"><span data-stu-id="66594-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-178">예</span><span class="sxs-lookup"><span data-stu-id="66594-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-179">아니오</span><span class="sxs-lookup"><span data-stu-id="66594-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-180">아니오</span><span class="sxs-lookup"><span data-stu-id="66594-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-181">아니오</span><span class="sxs-lookup"><span data-stu-id="66594-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-182">4.5 클라이언트 ¹</span><span class="sxs-lookup"><span data-stu-id="66594-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-183">예</span><span class="sxs-lookup"><span data-stu-id="66594-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-184">예</span><span class="sxs-lookup"><span data-stu-id="66594-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-185">아니오</span><span class="sxs-lookup"><span data-stu-id="66594-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-186">아니오</span><span class="sxs-lookup"><span data-stu-id="66594-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66594-187">4.6 클라이언트 (32 비트)</span><span class="sxs-lookup"><span data-stu-id="66594-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-188">예</span><span class="sxs-lookup"><span data-stu-id="66594-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-189">예</span><span class="sxs-lookup"><span data-stu-id="66594-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-190">예</span><span class="sxs-lookup"><span data-stu-id="66594-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-191">아니오</span><span class="sxs-lookup"><span data-stu-id="66594-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66594-192">4.6 클라이언트 (64 비트)</span><span class="sxs-lookup"><span data-stu-id="66594-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-193">예</span><span class="sxs-lookup"><span data-stu-id="66594-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-194">예</span><span class="sxs-lookup"><span data-stu-id="66594-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-195">예</span><span class="sxs-lookup"><span data-stu-id="66594-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="66594-196">예</span><span class="sxs-lookup"><span data-stu-id="66594-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="66594-197">¹ app-v 4.5, App-v 4.5 CU1, App-v 4.5 SP1을 비롯 한 모든 버전의 App-v 4.5 클라이언트에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66594-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









