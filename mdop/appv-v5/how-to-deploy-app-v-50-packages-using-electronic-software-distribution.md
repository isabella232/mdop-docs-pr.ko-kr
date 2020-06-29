---
title: 전자 소프트웨어 배포를 사용하여 App-V 5.0 패키지를 배포하는 방법
description: 전자 소프트웨어 배포를 사용하여 App-V 5.0 패키지를 배포하는 방법
author: dansimp
ms.assetid: 08e5e05b-dbb8-4be7-b2d8-721ef627da81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 33af02c5e9fad7408f9719ecd1a7fa90eacfeb29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814188"
---
# 전자 소프트웨어 배포를 사용하여 App-V 5.0 패키지를 배포하는 방법


ESD (전자 소프트웨어 배포) 시스템을 사용 하 여 app-v 클라이언트에 App-v 5.0 가상 응용 프로그램을 배포할 수 있습니다. 자세한 내용은 사용 중인 ESD와 함께 제공 되는 설명서를 참조 하세요.

ESD를 사용 하 여 App-v 패키지를 배포 하는 구성 요소 요구 사항 및 옵션은 [전자 소프트웨어 배포 시스템을 사용 하 여 app-v 5.0 배포 계획](planning-to-deploy-app-v-50-with-an-electronic-software-distribution-system.md)을 참조 하세요.

다음 방법 중 하나를 사용 하 여 패키지를 ESD (앱-V 클라이언트 컴퓨터)에 게시 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>타사 ESD에서 제공 하는 기능</p></td>
<td align="left"><p>타사 ESD의 기능을 사용 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>독립 실행형 Windows Installer</p></td>
<td align="left"><p>처음으로 응용 프로그램을 시퀀싱 할 때 생성 되는 연결 된 Windows Installer (.msi) 파일을 사용 하 여 대상 클라이언트 컴퓨터에 응용 프로그램을 설치 합니다. Windows Installer 파일에는 패키지를 구성 하 고 필요한 패키지 파일을 클라이언트에 복사 하는 데 사용 되는 관련 앱-V 5.0 패키지 파일 정보가 포함 되어 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>PowerShell cmdlet을 사용 하 여 가상화 된 응용 프로그램을 배포 합니다. PowerShell 및 App-v 5.0 사용에 대 한 자세한 내용은 <a href="administering-app-v-by-using-powershell.md" data-raw-source="[Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md)"> powershell을 사용 하 여 App-v 관리를 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>

 

**ESD를 사용 하 여 앱-V 5.0 패키지를 배포 하려면**

1.  환경의 컴퓨터에 App-v 5.0 Sequencer를 설치 합니다. Sequencer 설치에 대 한 자세한 내용은 Sequencer를 [설치 하는 방법을](how-to-install-the-sequencer-beta-gb18030.md)참조 하세요.

2.  앱-V 5.0 시퀀서를 사용 하 여 가상 응용 프로그램을 만듭니다. 가상 응용 프로그램을 만드는 방법에 대 한 자세한 내용은 [app-v 5.0 가상화 된 응용 프로그램 만들기 및 관리](creating-and-managing-app-v-50-virtualized-applications.md)를 참조 하세요.

3.  가상 응용 프로그램을 만든 후 ESD 솔루션을 사용 하 여 패키지를 배포 합니다.

    System Center Configuration Manager를 사용 하는 경우 먼저 [구성 관리자의 응용 프로그램 관리 소개](https://go.microsoft.com/fwlink/?LinkId=281816) 에서 앱-V 5.0 및 시스템 Center2012 구성 관리자 사용에 대 한 정보를 검토 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





