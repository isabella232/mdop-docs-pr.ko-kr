---
title: 원격 네트워크용 MED-V 구성
description: 원격 네트워크용 MED-V 구성
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826723"
---
# <span data-ttu-id="1f835-103">원격 네트워크용 MED-V 구성</span><span class="sxs-lookup"><span data-stu-id="1f835-103">Configuring MED-V for Remote Networks</span></span>


<span data-ttu-id="1f835-104">네트워크 내에서 또는 네트워크 내부에서 원격으로 또는 둘 다에서 작동 하도록 MED-V를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-104">You can configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**<span data-ttu-id="1f835-105">네트워크 내에서 작동 하도록 MED-V를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1f835-105">To configure MED-V to work from inside a network</span></span>**

-   <span data-ttu-id="1f835-106">네트워크 내에서 MED-V 서버와 이미지 배포를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-106">Configure a MED-V server and image distribution inside the network.</span></span>

**<span data-ttu-id="1f835-107">MED-V를 원격으로 작동 하도록 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1f835-107">To configure MED-V to work remotely</span></span>**

1.  <span data-ttu-id="1f835-108">MED-V 서버와 인터넷에서 액세스할 수 있는 이미지 배포 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-108">Configure a MED-V server and an image distribution server that are accessible from the Internet.</span></span>

2.  <span data-ttu-id="1f835-109">필요한 경우 경계 네트워크 (DMZ 라고도 함)를 리버스 프록시로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-109">If needed, configure a perimeter network (also called a DMZ) reverse proxy.</span></span>

3.  <span data-ttu-id="1f835-110">인증 방법을 Set **Server\\** 폴더에서 찾을 수 있는 *ClientSettings.xml* 파일에 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-110">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

**<span data-ttu-id="1f835-111">네트워크 내부와 원격에서 모두 작동 하도록 MED-V를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1f835-111">To configure MED-V to work both from inside a network and remotely</span></span>**

1.  <span data-ttu-id="1f835-112">네트워크 내에서 MED-V 서버와 이미지 배포 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-112">Configure a MED-V server and image distribution server inside the network.</span></span>

2.  <span data-ttu-id="1f835-113">인터넷에서 서버에 액세스할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-113">Ensure that the servers are accessible from the Internet.</span></span>

3.  <span data-ttu-id="1f835-114">클라이언트가 서버에 연결 하려고 할 때 클라이언트 위치를 기반으로 올바른 서버 (네트워크 내 또는 인터넷)에 자동으로 연결 되도록 DNS 확인을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-114">Configure the DNS resolution so that when the client attempts to connect to a server, it automatically connects to the correct server (within the network or over the Internet) based on the client location.</span></span>

4.  <span data-ttu-id="1f835-115">필요한 경우 경계 네트워크 역방향 프록시를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-115">If needed, configure a perimeter network reverse proxy.</span></span>

5.  <span data-ttu-id="1f835-116">인증 방법을 Set **Server\\** 폴더에서 찾을 수 있는 *ClientSettings.xml* 파일에 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-116">Set the authentication method, in the *ClientSettings.xml* file, which can be found in the **Servers\\Configuration Server\\** folder.</span></span>

<span data-ttu-id="1f835-117">**참고**  새 설정을 적용할 때 서비스를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-117">**Note** When applying new settings, the service must be restarted.</span></span>

 

-   <span data-ttu-id="1f835-118">IIS 인증 구성표를 기본, 다이제스트, NTLM 또는 협상 중 하나로 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-118">You can change the IIS authentication scheme to one of the following: BASIC, DIGEST, NTLM, or NEGOTIATE.</span></span> <span data-ttu-id="1f835-119">기본값은 NEGOTIATE이 고 다음 항목을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f835-119">The default is NEGOTIATE and uses the following entry:</span></span>

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## <span data-ttu-id="1f835-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1f835-120">Related topics</span></span>


[<span data-ttu-id="1f835-121">MED-V 인프라 계획 및 디자인</span><span class="sxs-lookup"><span data-stu-id="1f835-121">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





