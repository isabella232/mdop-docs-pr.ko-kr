---
title: App-V용 Windows Server 2008 방화벽을 구성하는 방법
description: App-V용 Windows Server 2008 방화벽을 구성하는 방법
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817718"
---
# <span data-ttu-id="9e1f0-103">App-V용 Windows Server 2008 방화벽을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="9e1f0-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="9e1f0-104">Windows Server2008 도입으로 방화벽과 IPsec 구성 요소가 하나의 서비스에 통합 되어이 서비스의 기능이 향상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="9e1f0-105">새 방화벽 서비스는 수신 및 발신 상태 저장 검사를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="9e1f0-106">또한 그룹 정책을 통해 특정 방화벽 규칙과 IPsec 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="9e1f0-107">Windows Server2008의 Windows 방화벽에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=151980> 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="9e1f0-108">다음 절차에서는 SMB 또는 HTTP/HTTPS를 통해 .ICO 및 OSD 게시에 대 한 예외 추가를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="9e1f0-109">이러한 예외는 Windows Server 2008 방화벽에 설치 된 네트워크 프로필 및 역할에 따라 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="9e1f0-110">**참고**  관리 서버가 RTSP를 사용 하도록 구성 된 경우이 절차를 반복 하 여 `sghwsvr.exe` 프로그램을 예외로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="9e1f0-111">App-v 스트리밍 서버에는 `sglwdsptr.exe` RTSPS 통신을 위한 프로그램 예외가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="9e1f0-112">통신을 위해 RTSP를 사용 하는 App-v 스트리밍 서버에도에 대 한 프로그램 예외가 필요 `sglwsvr.exe` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="9e1f0-113">App-v 용 Windows Server2008 방화벽을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="9e1f0-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="9e1f0-114">제어판을 통해 **고급 보안 관리 콘솔을 사용 하 여 Windows 방화벽** 을 열거나 `wf.msc` 실행 줄에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="9e1f0-115">새 인바운드 규칙을 만들고 **프로그램**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="9e1f0-116">프로그램 경로를 선택 하 고 `sghwdsptr.exe` 기본적으로에 있는을 찾습니다 `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="9e1f0-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="9e1f0-117">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-117">Click **Next**.</span></span>

5.  <span data-ttu-id="9e1f0-118">**작업** 페이지에서 **연결 허용**을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="9e1f0-119">적절 한 **프로필** 을 선택 하 여 인바운드 규칙에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="9e1f0-120">규칙의 이름과 설명을 입력 하 고 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e1f0-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="9e1f0-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9e1f0-121">Related topics</span></span>


[<span data-ttu-id="9e1f0-122">App-V용 Windows Server 2003 방화벽을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="9e1f0-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





