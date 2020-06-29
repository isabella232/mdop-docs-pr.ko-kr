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
# 원격 네트워크용 MED-V 구성


네트워크 내에서 또는 네트워크 내부에서 원격으로 또는 둘 다에서 작동 하도록 MED-V를 구성할 수 있습니다.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**네트워크 내에서 작동 하도록 MED-V를 구성 하려면**

-   네트워크 내에서 MED-V 서버와 이미지 배포를 구성 합니다.

**MED-V를 원격으로 작동 하도록 구성 하려면**

1.  MED-V 서버와 인터넷에서 액세스할 수 있는 이미지 배포 서버를 구성 합니다.

2.  필요한 경우 경계 네트워크 (DMZ 라고도 함)를 리버스 프록시로 구성 합니다.

3.  인증 방법을 Set **Server\\** 폴더에서 찾을 수 있는 *ClientSettings.xml* 파일에 설정 합니다.

**네트워크 내부와 원격에서 모두 작동 하도록 MED-V를 구성 하려면**

1.  네트워크 내에서 MED-V 서버와 이미지 배포 서버를 구성 합니다.

2.  인터넷에서 서버에 액세스할 수 있는지 확인 합니다.

3.  클라이언트가 서버에 연결 하려고 할 때 클라이언트 위치를 기반으로 올바른 서버 (네트워크 내 또는 인터넷)에 자동으로 연결 되도록 DNS 확인을 구성 합니다.

4.  필요한 경우 경계 네트워크 역방향 프록시를 구성 합니다.

5.  인증 방법을 Set **Server\\** 폴더에서 찾을 수 있는 *ClientSettings.xml* 파일에 설정 합니다.

**참고**  새 설정을 적용할 때 서비스를 다시 시작 해야 합니다.

 

-   IIS 인증 구성표를 기본, 다이제스트, NTLM 또는 협상 중 하나로 변경할 수 있습니다. 기본값은 NEGOTIATE이 고 다음 항목을 사용 합니다.

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

## 관련 항목


[MED-V 인프라 계획 및 디자인](med-v-infrastructure-planning-and-design.md)

 

 





