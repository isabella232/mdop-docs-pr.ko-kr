---
title: MED-V 자르기 전송 기술
description: MED-V 자르기 전송 기술
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826188"
---
# <span data-ttu-id="62f00-103">MED-V 자르기 전송 기술</span><span class="sxs-lookup"><span data-stu-id="62f00-103">MED-V Trim Transfer Technology</span></span>


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


<span data-ttu-id="62f00-104">MED-V 고급 트리밍 전송 제거 기술은 LAN 또는 WAN을 통해 초기 및 업데이트 된 가상 컴퓨터 이미지의 다운로드를 가속화 하므로 MED-V 작업 영역 가상 컴퓨터를 여러 최종 사용자에 게 전송 하는 데 필요한 네트워크 대역폭을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-104">The MED-V advanced Trim Transfer de-duplication technology accelerates the download of initial and updated virtual machine images over the LAN or WAN, thereby reducing the network bandwidth needed to transport a MED-V workspace virtual machine to multiple end users.</span></span>

<span data-ttu-id="62f00-105">이 혁신적인 기술은 기존 로컬 데이터를 사용 하 여 대부분의 경우 가상 컴퓨터 (예: 시스템 및 응용 프로그램 파일)가 최종 사용자의 디스크에 이미 존재 한다는 사실을 바탕으로 가상 컴퓨터 이미지를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-105">This breakthrough technology uses existing local data to build the virtual machine image, leveraging the fact that in many cases, much of the virtual machine (for example, system and application files) already exists on the end user's disk.</span></span> <span data-ttu-id="62f00-106">예를 들어, windowsxp를 포함 하는 가상 컴퓨터가 WindowsXP 로컬 복사본을 실행 하는 클라이언트에 게 전달 되는 경우 MED-V는 전송에서 중복 된 WindowsXP 요소를 자동으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-106">For example, if a virtual machine containing WindowsXP is delivered to a client running a local copy of WindowsXP, MED-V will automatically remove the redundant WindowsXP elements from the transfer.</span></span> <span data-ttu-id="62f00-107">유효 및 작동 작업 영역을 보장 하기 위해 MED-V 클라이언트의 암호화는 사용 하기 전에 로컬 데이터의 무결성을 확인 하 여, 데이터의 로컬 블록이 원하는 가상 컴퓨터 이미지에 있는 것과 동일한 비트 단위를 갖는 지를 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-107">To ensure a valid and functional workspace, the MED-V client cryptographically verifies the integrity of local data before it is utilized, guaranteeing that the local blocks of data are absolutely bit-by-bit identical to those in the desired virtual machine image.</span></span> <span data-ttu-id="62f00-108">일치 하지 않는 블록은 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-108">Blocks that do not match are not used.</span></span>

<span data-ttu-id="62f00-109">프로세스는 대역폭 효율적이 고 투명 하며 사용 되지 않는 네트워크 및 CPU 리소스를 활용 하 여 백그라운드에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-109">The process is bandwidth-efficient and transparent, and transfers run in the background, utilizing unused network and CPU resources.</span></span>

<span data-ttu-id="62f00-110">새 이미지 버전으로 업데이트 하는 경우 (예: 관리자가 새 응용 프로그램 또는 패치를 배포 하려는 경우), 전체 가상 컴퓨터가 아닌 변경 된 요소만 다운로드 되며 필요한 네트워크 대역폭과 배달 시간을 크게 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-110">When updating to a new image version (for example, when administrators want to distribute a new application or patch), only the elements that have changed ("deltas") are downloaded, and not the entire virtual machine, significantly reducing the required network bandwidth and delivery time.</span></span>

<span data-ttu-id="62f00-111">호스트 운영 체제에 따라 트리밍 전송 프로토콜의 일부로 호스트에서 색인화 되는 폴더를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-111">You can configure which folders are indexed on the host as part of the Trim Transfer protocol, based on the host operating system.</span></span> <span data-ttu-id="62f00-112">이러한 설정은 Server\\ 파일 *ClientSettings.xml* 에서 구성 되며,이 폴더에는 **servers\\entg\somyh** .</span><span class="sxs-lookup"><span data-stu-id="62f00-112">These settings are configured in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="62f00-113">새 설정을 적용할 때 서비스를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="62f00-113">When applying new settings, the service must be restarted.</span></span>

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





