---
title: 명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법
description: 명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816688"
---
# 명령줄을 사용하여 새 응용 프로그램을 시퀀싱하는 방법


명령줄을 사용 하 여 새 응용 프로그램의 순서를 지정할 수 있습니다. 명령줄을 사용 하면 많은 수의 가상 응용 프로그램을 만들어야 하거나, 반복적으로 시퀀싱 된 응용 프로그램을 만들어야 할 때 유용 합니다.

**중요**  
명령줄 시퀀싱을 사용 하면 기본 시퀀싱만 가능 합니다. 시퀀싱 하는 응용 프로그램의 기본 설치 설정을 변경 해야 하는 경우 수동으로 가상 응용 프로그램을 수정 하거나 Application Virtualization (App-v) Sequencer를 사용 하 여 가상 응용 프로그램을 업데이트 해야 합니다. App-v 시퀀서를 사용 하 여 가상 응용 프로그램을 업데이트 하는 방법에 대 한 자세한 내용은 [기존 가상 응용 프로그램을 업그레이드 하는 방법을](how-to-upgrade-an-existing-virtual-application.md)참조 하세요.



명령줄을 사용 하 여 가상 응용 프로그램을 만들려면 다음 절차를 사용 합니다.

**명령줄을 사용 하 여 응용 프로그램을 시퀀싱 하려면**

1.  App-v Sequencer를 실행 하는 컴퓨터에서 **시작**, **실행**을 선택 하 고 **cmd**를 입력 하 여 명령 프롬프트를 엽니다. **확인**을 클릭합니다.

2.  명령 프롬프트를 사용 하 여 App-v Sequencer가 설치 되어 있는 위치를 지정 합니다. 예를 들어 명령 프롬프트에서 다음을 입력할 수 있습니다. **cd C:\\program files Files\\Microsoft Application Virtualization Sequencer**.

3.  명령 프롬프트에서 다음 명령을 입력 하 고 따옴표 안에 있는 텍스트를 값으로 바꿉니다.

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **참고**  
    시퀀싱 하는 응용 프로그램의 복잡도에 따라 명령줄을 사용 하 여 추가 매개 변수를 지정할 수 있습니다. App-v 시퀀서와 함께 사용할 수 있는 전체 매개 변수 목록은 [Sequencer 명령줄 매개 변수](sequencer-command-line-parameters.md)를 참조 하세요.



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Enter **키를**누릅니다.

## 관련 항목


[앱-V 시퀀서를 사용 하 여 가상 응용 프로그램을 만들거나 업그레이드 하는 방법](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Sequencer 명령줄 오류 코드](sequencer-command-line-error-codes.md)

[Sequencer 명령줄 매개 변수](sequencer-command-line-parameters.md)









