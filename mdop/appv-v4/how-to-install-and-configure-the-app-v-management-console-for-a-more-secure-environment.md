---
title: 더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법
description: 더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817373"
---
# <span data-ttu-id="2fe52-103">더욱 안전한 환경을 위해 App-V Management Console을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="2fe52-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="2fe52-104">App-v 관리 콘솔의 기본 설치에는 보안 통신에 대 한 지원이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="2fe52-105">각 관리 콘솔은 콘솔을 처음 시작 하거나 추가 App-v 웹 관리 서비스에 연결할 때 각 연결 별로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="2fe52-106">기본 구성은 TCP 포트 443를 통해 SSL을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="2fe52-107">포트 번호가 서버에서 수정 된 경우 포트 번호를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="2fe52-108">보안 연결을 사용 하 여 다음 절차를 사용 하 여 App-v 웹 관리 서비스에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="2fe52-109">SSL 연결을 사용 하 여 앱-V 관리 서비스에 연결 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2fe52-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="2fe52-110">Application Virtualization 관리 콘솔을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="2fe52-111">콘솔의 작업 창에서 **연결 구성을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="2fe52-112">**웹 서비스 호스트 이름을**입력 하 고 **보안 연결 사용** 이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="2fe52-113">**중요**  웹 서비스 호스트 이름에 제공 된 이름은 인증서의 일반 이름과 일치 해야 하며, 그렇지 않으면 연결이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="2fe52-114">적절 한 로그인 자격 증명을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fe52-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="2fe52-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2fe52-115">Related topics</span></span>


[<span data-ttu-id="2fe52-116">App-V 웹 관리 서비스를 지원하기 위해 인증서 구성</span><span class="sxs-lookup"><span data-stu-id="2fe52-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





