---
title: MED-V 작업 영역 패키지 관리자를 사용하여 MED-V 작업 영역 설정 관리
description: MED-V 작업 영역 패키지 관리자를 사용하여 MED-V 작업 영역 설정 관리
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826123"
---
# MED-V 작업 영역 패키지 관리자를 사용하여 MED-V 작업 영역 설정 관리


MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역의 특정 설정을 관리할 수 있습니다.

**MED-V 작업 영역의 설정을 관리 하려면**

1. **Med-v 작업 영역 포장기**를 열려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**를 차례로 클릭 한 다음 **med-v 작업 영역 포장기**를 클릭 합니다.

2. **Med-v 작업 영역 포장기** 기본 패널에서 **설정 관리**를 클릭 합니다.

3. **설정 관리** 창에서 다음과 같은 med-v 작업 영역 설정을 구성할 수 있습니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>MED-V 작업 영역 시작</strong></p></td>
   <td align="left"><p>사용자가 로그온 할 때 MED-V 작업 영역을 시작할지, 처음 사용할 때 또는 최종 사용자가 MED-V 작업 영역이 시작 되는 시점을 결정할 수 있도록 할지 선택 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>MED-V 작업 영역은 최종 사용자가 로그온 할 때 또는 게시 된 응용 프로그램 열기와 같은 MED-V가 필요한 작업을 수행 하거나 리디렉션이 필요한 URL을 입력 하는 등 두 가지 방법 중 하나로 시작 됩니다.</p>
   <p>최종 사용자에 대해이 설정을 정의 하거나 최종 사용자가 MED-V를 시작 하는 방법을 제어할 수 있습니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>최종 사용자가 결정 하는 경우 기본 동작은 기본적으로 로그온 할 때 MED-V 작업 영역을 시작 하는 것입니다. 알림 영역에서 MED-V 아이콘을 마우스 오른쪽 단추로 클릭 하 고 Med-v 사용자 설정을 선택 하 여 기본값을 변경할 수 있습니다 <strong> </strong> . 최종 사용자에 대해이 설정을 정의 하는 경우 MED-V가 시작 되는 방식을 변경할 수 없습니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>네트워킹</strong></p></td>
   <td align="left"><p><strong> </strong> <strong> </strong> 네트워킹 설정에 대 한 공유 또는 브리지를 선택 합니다. 기본값은 <strong> 공유 </strong> 입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>공유 </strong> - med-v 작업 영역은 NAT (Network Address Translation)를 사용 하 여 송신 트래픽에 대 한 호스트&#39;s IP를 공유 합니다.</p>
   <p><strong>브리지 </strong> - 된 med-v 작업 영역에는 일반적으로 DHCP를 통해 얻은 고유한 네트워크 주소가 있습니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>스토어 자격 증명</strong></p></td>
   <td align="left"><p>최종 사용자 자격 증명을 저장할지 여부를 선택 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>기본 동작은 자격 증명 저장을 사용 하지 않도록 설정 하 여 최종 사용자가 로그온 할 때마다 인증을 받아야 한다는 것입니다.</p>
   <div class="alert">
   <strong>중요</strong><br/><p>최종 사용자의 자격 증명을 캐시 하는 것이 최상의 사용자 환경을 제공 하는 경우에도 관련 된 위험에 유의 해야 합니다.</p>
   <p>최종 사용자의 도메인 자격 증명은 Windows 자격 증명 관리자의 해독 가능한 형식으로 저장 됩니다. 공격자는 암호를 검색 하 여 사용자의 자격 증명에 액세스 하는 프로그램을 작성할 수 있습니다. 최종 사용자 자격 증명을 저장 하지 않도록 설정 하 여이 위험을 줄일 수 있습니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. **다른 이름으로 저장 ...** 을 클릭 합니다. 지정한 폴더에 업데이트 된 구성 설정을 저장 합니다. MED-V는 업데이트 된 설정을 포함 하는 레지스트리 파일을 만듭니다. 그룹 정책을 사용 하 여 업데이트 된 레지스트리 파일을 배포 합니다. 그룹 정책을 사용 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .

   또한 MED-V는이 업데이트 된 레지스트리 파일을 다시 만드는 데 사용할 수 있는 Windows PowerShell 스크립트를 지정한 폴더에 만듭니다.

## 관련 항목


[MED-V 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)

[MED-V 작업 영역 설정 관리](manage-med-v-workspace-settings.md)









