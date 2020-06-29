---
title: App-V Server용 방화벽 구성
description: App-V Server용 방화벽 구성
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821818"
---
# <span data-ttu-id="6cf1a-103">App-V Server용 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="6cf1a-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="6cf1a-104">Microsoft App-v (Application Virtualization) 관리 서버 또는 스트리밍 서버를 설치 하 고 RTSP 또는 RTSPS 프로토콜을 사용 하도록 구성한 후에는 App-v 프로그램에 대 한 방화벽 예외를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="6cf1a-105">Application Virtualization 관리 서버에 대 한 방화벽 예외 구성</span><span class="sxs-lookup"><span data-stu-id="6cf1a-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="6cf1a-106">**sghwdsptr.exe** 및 **sghwsvr.exe**에 대 한 방화벽 예외를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="6cf1a-107">이러한 프로그램은 32 비트 운영 체제의 C:\\program files Files\\Microsoft System Center App Virt 관리 Server\\App Virt 관리 Server\\app 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="6cf1a-108">64 비트 운영 체제 버전을 사용 하는 경우 폴더는 C:\\program files Files (x86) \\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="6cf1a-109">Application Virtualization 스트리밍 서버용 방화벽 예외 구성</span><span class="sxs-lookup"><span data-stu-id="6cf1a-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="6cf1a-110">**sglwdsptr.exe** 및 **sglwsvr.exe**에 대 한 방화벽 예외를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="6cf1a-111">이러한 프로그램은 32 비트 운영 체제의 C:\\program files Files\\Microsoft System Center App Virt 스트리밍 Server\\App Virt 스트리밍 Server\\app 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="6cf1a-112">64 비트 운영 체제 버전을 사용 하는 경우 폴더는 C:\\program files Files (x86) \\Microsoft System 센터 앱 Virt Streaming Server\\App Virt 스트리밍 Server\\bina에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cf1a-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="6cf1a-113">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6cf1a-113">Related topics</span></span>


[<span data-ttu-id="6cf1a-114">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="6cf1a-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="6cf1a-115">기본 응용 프로그램을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="6cf1a-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 





