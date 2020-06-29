---
title: 관리 서버 보안 사후 설치를 구성하는 방법
description: 관리 서버 보안 사후 설치를 구성하는 방법
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817938"
---
# <span data-ttu-id="a69d8-103">관리 서버 보안 사후 설치를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a69d8-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="a69d8-104">앱-V 관리 콘솔을 사용 하 여 인증서를 추가 하 고 앱-V 관리 서버를 구성 하 여 강화 된 보안을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="a69d8-105">다음 절차를 사용 하 여 보안 사후 설치를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="a69d8-106">관리 서버 보안을 구성 하려면 설치 후</span><span class="sxs-lookup"><span data-stu-id="a69d8-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="a69d8-107">App-v 관리 콘솔을 열고 앱-V 관리자 권한을 사용 하 여 **관리 서비스** 에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="a69d8-108">서버를 확장 하 고 **서버 그룹**을 확장 한 다음 관리 서버가 등록 된 적절 한 서버 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="a69d8-109">관리 서버 개체를 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="a69d8-110">**포트** 탭에서 **서버 인증서** 를 클릭 하 고 마법사를 완료 하 여 적절 하 게 프로 비전 된 인증서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="a69d8-111">**참고**  마법사에 인증서가 표시 되지 않으면 인증서가 구축 되지 않았거나 인증서가 App-v의 요구 사항을 충족 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="a69d8-112">**다음** 을 클릭 하 여 **인증서 시작 마법사** 페이지를 계속 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="a69d8-113">**사용 가능한 인증서** 화면에서 올바른 인증서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="a69d8-114">**마침**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="a69d8-115">마법사를 완료 한 후 사용 가능한 수신 대기 포트로 **RTSP** 를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="a69d8-116">이렇게 하면 비보안 통신 채널을 통해 연결이 이루어지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="a69d8-117">**적용**을 클릭 하 고 **Microsoft 가상 응용 프로그램 서버** 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="a69d8-118">서비스의 MMC 스냅인을 사용 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69d8-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="a69d8-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a69d8-119">Related topics</span></span>


[<span data-ttu-id="a69d8-120">Streaming Server 보안 사후 설치를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a69d8-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="a69d8-121">인증서 권한 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a69d8-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





