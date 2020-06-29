---
title: 클라이언트 로그 파일을 구성하는 방법
description: 클라이언트 로그 파일을 구성하는 방법
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817798"
---
# 클라이언트 로그 파일을 구성하는 방법


다음 절차를 사용 하 여 App-v (Application Virtualization) 클라이언트 로그 파일을 구성할 수 있습니다.

**로그 파일 위치를 변경 하려면**

-   다음 레지스트리 키 값을 편집 하 여 로그 파일에 대 한 새 경로를 지정 합니다. 이 값을 변경한 후 **sftlist** 서비스를 다시 시작 해야 합니다. 설치 후에도이 위치를 대화형으로 변경할 수 있습니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName

**로그 보고 수준을 변경 하려면**

-   기본적으로 로그에 기록 되는 메시지 형식에는 심각도 수준 4 (알림) 이상의 모든 이벤트가 포함 됩니다. 심각도 수준은 다음 키 값에 저장 됩니다. 자세한 로깅을 사용 하려면이 키 값을 5로 설정 합니다. 매우 큰 메시지를 생성 하 고 로그가 빠르게 채워지기 때문에 문제 해결 중 짧은 기간 동안에만 자세한 정보 표시 로깅을 사용 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity

**로그 크기를 변경 하려면**

-   Application Virtualization (App-v) 4.5의 로그 크기는 다음 레지스트리 키 값으로 제어 됩니다. 이 값은 기본적으로 256MB이 고 최대 크기 (MB)를 정의 하 여 로그를 다시 설정 하기 전까지 커질 수 있습니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize

    **주의**  사항 로그 파일이 다시 설정 되도록 하려면이 레지스트리 키 값을 0 보다 큰 값으로 설정 해야 합니다.

     

**백업 복사본 수를 변경 하려면**

-   로그 파일이 최대 크기에 도달 하면 로그에 다음 쓰기가 발생할 때 재설정이 강제 적용 됩니다. 다시 설정 하면 새 로그 파일이 만들어지고 이전 파일의 이름이 백업으로 바뀝니다. 다음 레지스트리 설정은 파일을 다시 설정할 때 보관 되는 로그 파일의 백업 복사본 수를 제어 합니다. 기본값은 4입니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount

    백업 로그 파일 이름의 형식은 **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** 이며 재설정 시간 (Utc (협정 세계시))을 기준으로 합니다. 다음 표에는 파일 이름과 설명을 만드는 데 사용 되는 기호가 나열 되어 있습니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">기호</th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>년</p></td>
    <td align="left"><p>4 자리 연도</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>200</p></td>
    <td align="left"><p>2 자리 월 (01 – 12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>일</p></td>
    <td align="left"><p>해당 달의 2 자리 일 (01-31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>h:mm</p></td>
    <td align="left"><p>시간 (00 – 23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>200</p></td>
    <td align="left"><p>분 (00 – 59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>초 (00 – 59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>uuu</p></td>
    <td align="left"><p>밀리초 (000-999)</p></td>
    </tr>
    </tbody>
    </table>

     

## 관련 항목


[명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





