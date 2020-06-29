---
title: Setup.msi를 사용하여 App-V Client를 설치하는 방법
description: Setup.msi를 사용하여 App-V Client를 설치하는 방법
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817333"
---
# <span data-ttu-id="4f898-103">Setup.msi를 사용하여 App-V Client를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="4f898-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="4f898-104">이 항목에서는 setup.msi 프로그램을 사용 하 여 앱 V 클라이언트를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="4f898-105">setup.msi 프로그램을 사용 하 여 App-v 클라이언트를 설치 하기 전에 먼저 필수 구성 요소 소프트웨어를 설치 해야 하는지 확인 한 다음 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="4f898-106">필수 구성 요소 소프트웨어를 설치 하려면이 항목의 [필수 구성 요소 소프트웨어 설치](#prereq-sw) 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f898-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="4f898-107">클라이언트 소프트웨어를 설치 하려면이 항목의 [Setup.msi 프로그램 섹션을 사용 하 여 App-v 클라이언트 설치](#msi-setup) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f898-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="4f898-108">필수 소프트웨어 설치</span><span class="sxs-lookup"><span data-stu-id="4f898-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="4f898-109">다음 절차를 사용 하 여 필수 구성 요소 소프트웨어를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="4f898-110">명령 파일을 만들고 명령 프롬프트에서 명령을 실행 하거나, VBScript 또는 Windows PowerShell 같은 스크립트 언어를 사용 하 여 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="4f898-111">**참고**  X86 및 x64 버전의 App-v 클라이언트에는 다음 소프트웨어의 x86 버전이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="4f898-112">Microsoft VisualC + + 2005SP1 재배포 가능 패키지 (x86)를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="4f898-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="4f898-113">Microsoft 다운로드 센터 ()에서 [Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) 소프트웨어 패키지를 다운로드 <https://go.microsoft.com/fwlink/?LinkId=119961> 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="4f898-114">\ [Template Token Value \] 버전 4.5 SP2 이상의 App-v 클라이언트의 경우 [Microsoft Visual c + + 2005 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [Template token Value \])에서 vcredist\_x86.exe를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f898-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="4f898-115">자동으로 설치 하려면 명령줄 옵션 "/Q"를 vcredist\_x86.exe와 함께 사용 합니다 (예: **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="4f898-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="4f898-116">vcredist\_x86.msi 파일을 사용 하 여 소프트웨어를 설치 하려면 명령줄 옵션인 "/C/T: &lt; fullpathtofolder &gt; "를 사용 하 여 vcredist.msi 파일을 추출 하 고 vcredist\_x86.exe에서 임시 폴더로 vcredis1.cab 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="4f898-117">자동으로 설치 하려면 명령줄 옵션/quiet (예: **msiexec/i vcredist.msi** /quiet.를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="4f898-118">Microsoft VisualC + + 2008을 설치 하려면 SP1 재배포 가능 패키지 (x86)</span><span class="sxs-lookup"><span data-stu-id="4f898-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="4f898-119">**중요**  App-v 클라이언트의 버전 4.6 이상에서는 Microsoft Visual c + + 2008 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트도 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="4f898-120">Microsoft 다운로드 센터 [2008 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트](https://go.microsoft.com/fwlink/?LinkId=150700) 소프트웨어 패키지를 다운로드 합니다 ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="4f898-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="4f898-121">자동으로 설치 하려면 명령줄 옵션 "/Q"를 vcredist\_x86.exe와 함께 사용 합니다 (예: **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="4f898-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="4f898-122">MSXML (Microsoft Core XML Services) 6.0 SP1 (x86)을 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="4f898-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="4f898-123">Microsoft 다운로드 센터 ()에서 [MICROSOFT MSXML (CORE XML Services) 6.0 sp1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) 소프트웨어 패키지를 다운로드 https://go.microsoft.com/fwlink/?LinkId=63266) 합니다 (.</span><span class="sxs-lookup"><span data-stu-id="4f898-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="4f898-124">자동으로 설치 하려면 명령줄 옵션/quiet (예: **msiexec/i msxml6\_x86.msi/quiet**)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="4f898-125">Microsoft 응용 프로그램 오류 보고를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="4f898-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="4f898-126">Microsoft 응용 프로그램 오류 보고를 설치할 때 *Appguid* 매개 변수를 사용 하 여 app-v 제품 코드를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="4f898-127">제품 코드는 각 App-v 클라이언트 유형 및 버전에 대해 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="4f898-128">다음 표에서 올바른 제품 코드를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="4f898-129">**중요**  App-v 4.6 SP2 이상 버전에서는 더 이상 Microsoft 응용 프로그램 오류 보고 (dw20shared.msi)를 설치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="4f898-130">이제 app-v에서 Microsoft 오류 보고를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4f898-131">버전</span><span class="sxs-lookup"><span data-stu-id="4f898-131">Version</span></span></th>
<th align="left"><span data-ttu-id="4f898-132">데스크톱 클라이언트용 제품 코드</span><span class="sxs-lookup"><span data-stu-id="4f898-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="4f898-133">원격 데스크톱 서비스용 클라이언트에 대 한 제품 코드</span><span class="sxs-lookup"><span data-stu-id="4f898-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f898-134">App-V 4.5 CU1</span><span class="sxs-lookup"><span data-stu-id="4f898-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="4f898-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="4f898-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f898-137">App-v 4.5 SP1</span><span class="sxs-lookup"><span data-stu-id="4f898-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="4f898-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="4f898-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f898-140">App-v 4.5 SP2</span><span class="sxs-lookup"><span data-stu-id="4f898-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="4f898-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="4f898-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f898-143">App-v 4.6 x86</span><span class="sxs-lookup"><span data-stu-id="4f898-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="4f898-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="4f898-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f898-146">App-v 4.6 x64</span><span class="sxs-lookup"><span data-stu-id="4f898-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="4f898-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="4f898-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f898-149">App-v 4.6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="4f898-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="4f898-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="4f898-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f898-152">App-v 4.6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="4f898-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="4f898-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="4f898-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4f898-155">App-v 4.6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="4f898-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="4f898-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="4f898-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4f898-158">App-v 4.6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="4f898-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="4f898-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="4f898-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="4f898-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4f898-161">¹ App-V "언어" 릴리스.</span><span class="sxs-lookup"><span data-stu-id="4f898-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="4f898-162">**참고**  제품 코드를 찾아야 하는 경우 Orca.exe 데이터베이스 편집기 또는 유사한 도구를 사용 하 여 Windows Installer 파일을 검사 하 고 *ProductCode* 속성 값을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="4f898-163">Orca.exe 사용에 대 한 자세한 내용은 [Windows Installer 개발 도구](https://go.microsoft.com/fwlink/?LinkId=150008) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="4f898-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="4f898-164">Release media의 **Support\\watson** 폴더에서 찾을 수 있는 dw20shared.msi Microsoft 응용 프로그램 오류 보고 설치 프로그램을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="4f898-165">소프트웨어를 설치 하려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="4f898-166">Setup.msi 프로그램을 사용 하 여 앱 V 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="4f898-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="4f898-167">다음 절차를 사용 하 여 App-v 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="4f898-168">필수 구성 요소 소프트웨어가 모두 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="4f898-169">\ [Template Token Value \] 버전 4.6 클라이언트의 경우 setup.msi 프로그램이 시스템을 확인 하 고 필수 구성 요소 소프트웨어가 설치 되어 있지 않은 경우 설치를 계속할 수 없다는 오류 메시지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="4f898-170">\ [Template 토큰 값 \]</span><span class="sxs-lookup"><span data-stu-id="4f898-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="4f898-171">Setup.msi를 사용 하 여 응용 프로그램 가상화 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="4f898-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="4f898-172">컴퓨터에 대 한 관리자 권한이 있는 계정으로 로그온 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="4f898-173">승격 된 권한을 사용 하 여 명령 프롬프트 창을 연 다음 디렉터리를 설치 파일이 포함 된 폴더로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="4f898-174">App-v 클라이언트의 버전 4.6 또는 이후 버전을 설치할 때 컴퓨터의 운영 체제 32 비트 또는 64 비트에 대 한 올바른 설치 관리자를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="4f898-175">설치에 실패 하 고 잘못 된 설치 관리자를 사용 하는 경우 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="4f898-176">명령 프롬프트에 설치 명령 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="4f898-177">또는 명령 파일을 만들어 명령 프롬프트에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="4f898-178">VBScript 또는 Windows PowerShell 같은 스크립트 언어를 사용 하 여 명령을 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="4f898-179">다음 명령줄 예제에서는 여러 개의 선택적 매개 변수를 사용 하 여 setup.msi를 사용할 수 있는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="4f898-180">이러한 매개 변수에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f898-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="4f898-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "프로덕션 시스템" SWIPUBSVRTYPE = "HTTP/secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "SWIGLOBALDATA" D:\\AppVirt\\Global = "SWIUSERDATA" LOCALAPPDATA = "SWIFSDRIVE ^%\\Windows\\Application 가상화 Client" = "S"/q</span><span class="sxs-lookup"><span data-stu-id="4f898-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="4f898-182">중요</span><span class="sxs-lookup"><span data-stu-id="4f898-182">Important</span></span>**  
    -   <span data-ttu-id="4f898-183">Windows Installer 스위치 "**/q**"를 사용 하 여 자동 설치를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="4f898-184">" **%** **% HomeDrive%**"의 "" 문자는 "" 이스케이프 문자 앞에와 야 합니다 **^** .</span><span class="sxs-lookup"><span data-stu-id="4f898-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="4f898-185">그렇지 않으면 Windows 명령 셸에서는 설치를 수행 하는 사용자의 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="4f898-186">설치 로깅을 설정 하려면 msiexec 스위치 **/l\ \* v 파일 이름 .log**를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f898-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="4f898-187">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4f898-187">Related topics</span></span>


[<span data-ttu-id="4f898-188">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="4f898-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





