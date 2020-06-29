---
title: App-V용 Windows Server 2003 방화벽을 구성하는 방법
description: App-V용 Windows Server 2003 방화벽을 구성하는 방법
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817728"
---
# <span data-ttu-id="d07e5-103">App-V용 Windows Server 2003 방화벽을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d07e5-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="d07e5-104">App-v 용 WindowsServer 2003 방화벽을 구성 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="d07e5-105">앱 용 WindowsServer 2003 방화벽을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d07e5-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="d07e5-106">**제어판**에서 **Windows 방화벽**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="d07e5-107">**참고**  이 단계를 수행 하기 전에 서버에서 방화벽 서비스를 실행 하도록 구성 하지 않은 경우 방화벽 서비스를 시작 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="d07e5-108">.ICO 및 OSD 파일이 SMB를 통해 게시 되는 경우 **예외** 탭에서 **파일 및 프린터 공유** 를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="d07e5-109">**참고**  .ICO 및 OSD 파일이 관리 서버에서 HTTP/HTTPS를 통해 게시 되는 경우 HTTP 또는 HTTPS에 대 한 예외를 추가 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="d07e5-110">.ICO 및 OSD 파일을 호스트 하는 IIS 서버가 관리 서버와 별개인 컴퓨터에서 호스팅되는 경우 해당 컴퓨터에 예외를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="d07e5-111">성능을 최대화 하려면 관리 서버와는 별도의 서버에서 .ICO 및 OSD 파일을 호스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="d07e5-112">관리 서버 서비스 실행 파일인 경우에 대 한 프로그램 예외를 추가 `sghwdsptr.exe` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="d07e5-113">이 실행 파일의 기본 경로는 `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="d07e5-114">**참고**  관리 서버에서 통신을 위해 RTSP를 사용 하는 경우에도 프로그램 예외를 추가 해야 합니다 `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="d07e5-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="d07e5-115">App-v 스트리밍 서버에는 `sglwdsptr.exe` RTSPS 통신을 위한 프로그램 예외가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="d07e5-116">통신을 위해 RTSP를 사용 하는 App-v 스트리밍 서버에도에 대 한 프로그램 예외가 필요 `sglwsvr.exe` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="d07e5-117">각 예외에 대해 적절 한 범위가 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="d07e5-118">위험을 줄이려면 컴퓨터를 제거 하 고 서버가 응답 하는 IP 주소를 엄격 하 게 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07e5-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="d07e5-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d07e5-119">Related topics</span></span>


[<span data-ttu-id="d07e5-120">App-V용 Windows Server 2008 방화벽을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d07e5-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





