---
title: PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법
description: PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814073"
---
# PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법


다음 절차를 사용 하 여 보고용 앱-V 5.1를 구성 합니다.

**보고를 위해 App-v 5.1 클라이언트를 실행 하는 컴퓨터를 구성 하려면**

1. App-v 5.1 클라이언트를 설치 합니다. 클라이언트를 설치 하는 방법에 대 한 자세한 내용은 [App-v 클라이언트를 배포 하는 방법을](how-to-deploy-the-app-v-client-51gb18030.md)참조 하세요.

2. App-v 5.1 클라이언트를 설치한 후 **Set AppvClientConfiguration** PowerShell을 사용 하 여 적절 한 보고 구성 설정을 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">설정</th>
   <th align="left">설명</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>클라이언트가 보고 서버로 정보를 반환할 수 있도록 합니다. 클라이언트가 클라이언트에서 보고 데이터를 수집 하려면이 설정이 필요 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>클라이언트 정보가 저장 되는 보고 서버의 위치를 지정 합니다. 예를 들어 http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt;</p>
   <div class="alert">
   <strong>참고</strong><br/><p>보고 서버 설정 중에 지정 된 포트 번호입니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>보고 시작 시간</p></td>
   <td align="left"><p>이는 클라이언트가 서버에 데이터를 자동으로 보내도록 예약 하도록 설정 되어 있습니다. 이 설정은 보고 데이터 보내기를 시작 하는 시간을 나타냅니다. 24 시간 형식으로 표시 되며 0-23 사이의 숫자가 사용 됩니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>보고 서버로 데이터를 보낼 최대 지연 시간 (분)을 지정 합니다. 예약 된 작업이 시작 되 면 클라이언트는 0과 ReportingRandomDelay 사이의 임의 지연 시간을 생성 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>클라이언트가 보고 서버에 데이터를 재전송 하는 데 사용할 다시 시도 간격을 지정 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다. 크기는 메모리의 캐시에 적용 됩니다. 제한에 도달 하면 로그 파일이 롤오버 됩니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다. 크기는 메모리의 캐시에 적용 됩니다. 제한에 도달 하면 로그 파일이 롤오버 됩니다.</p></td>
   </tr>
   </tbody>
   </table>



3. 적절 한 설정이 구성 되 면 App-v 5.1 클라이언트를 실행 하는 컴퓨터가 데이터를 자동으로 수집 하 고 데이터를 보고 서버로 다시 보냅니다.

   또한 관리자는 **AppvClientReport** PowerShell cmdlet을 사용 하 여 요청 하는 방식으로 데이터를 수동으로 다시 보낼 수 있습니다.

   **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[PowerShell을 사용하여 App-V 5.1 관리](administering-app-v-51-by-using-powershell.md)









