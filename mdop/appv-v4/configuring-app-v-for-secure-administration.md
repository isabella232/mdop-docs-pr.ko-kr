---
title: 보안 관리를 위한 App-V 구성
description: 보안 관리를 위한 App-V 구성
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821903"
---
# <span data-ttu-id="2c698-103">보안 관리를 위한 App-V 구성</span><span class="sxs-lookup"><span data-stu-id="2c698-103">Configuring App-V for Secure Administration</span></span>


<span data-ttu-id="2c698-104">관리 작업 보안이 중요 한 환경에서 App-v 웹 관리 서비스와 App-v 관리 콘솔 간의 보안 통신을 허용 하는 앱-V를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-104">In an environment where securing administrative operations is important, App-V allows for secure communication between the App-V Web Management Service and the App-V Management Console.</span></span> <span data-ttu-id="2c698-105">관리 서비스는 웹 기반 응용 프로그램이 기 때문에 관리 서비스를 호스트 하는 웹 서버에서 App-v 관리 서버 응용 프로그램을 보호 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-105">Because the Management Service is a Web-based application, it requires securing the App-V Management Server application on the Web server that hosts the Management Service.</span></span> <span data-ttu-id="2c698-106">다음 그림과 같이이 프로세스에서는 통신에 HTTPS를 사용 하 고 Windows 통합 인증만 허용 하도록 IIS 서버를 구성 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-106">As shown in the following illustration, this process includes using HTTPS for communication and configuring the IIS server to allow only Windows Integrated Authentication.</span></span>

![app-v 웹 서비스 네트워크 구성](images/appvmgmtwebservice.gif)

<span data-ttu-id="2c698-108">앱-V 웹 관리 서비스는 IIS에 웹 기반 응용 프로그램으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-108">The App-V Web Management Service is installed as a Web-based application on IIS.</span></span> <span data-ttu-id="2c698-109">웹 관리 서비스에서 App-v 관리 콘솔과 웹 관리 서비스 간에 보안 (SSL) 연결을 지원 하려면 웹 관리 서비스가 설치 된 IIS 서버를 구성 하 고 App-v 관리 콘솔을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-109">For the Web Management Service to support secure (SSL) connections between the App-V Management Console and the Web Management Service, you will need to configure the IIS server where the Web Management Service is installed and configure the App-V Management Console.</span></span>

## <span data-ttu-id="2c698-110">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="2c698-110">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[<span data-ttu-id="2c698-111">App-V 웹 관리 서비스를 지원하기 위해 인증서 구성</span><span class="sxs-lookup"><span data-stu-id="2c698-111">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)  
<span data-ttu-id="2c698-112">SSL 기반 연결을 지원 하도록 인증서를 구성 하는 데 유용한 정보를 제공 하 여 App-v 웹 관리 서비스에 대 한 통신을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-112">Provides helpful information about configuring certificates to support SSL-based connections, to help secure communication for the App-V Web Management Service.</span></span>

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[<span data-ttu-id="2c698-113">더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="2c698-113">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
<span data-ttu-id="2c698-114">보안 연결을 사용 하 여 앱-V 웹 관리 서비스에 연결 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c698-114">Provides a step-by-step procedure for connecting to an App-V Web Management Service by using a secure connection.</span></span>

 

 





