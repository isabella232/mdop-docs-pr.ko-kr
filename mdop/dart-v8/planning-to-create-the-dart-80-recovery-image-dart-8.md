---
title: DaRT 8.0 복구 이미지 만들기 계획
description: DaRT 8.0 복구 이미지 만들기 계획
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824808"
---
# DaRT 8.0 복구 이미지 만들기 계획


이 섹션의 정보를 사용 하 여 Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지를 만들 수 있습니다.

## DaRT 8.0 복구 이미지 만들기 계획


DaRT 복구 이미지를 만들 때는 이미지에 포함할 도구를 결정 해야 합니다. 이를 결정 하려면 최종 사용자가 해당 도구에 액세스할 수 있다는 것을 고려해 야 합니다. 지원 엔지니어가 최종 사용자의 컴퓨터에 복구 이미지 미디어를 사용 하 여 문제를 진단 하는 경우 복구 이미지에 모든 도구를 설치 하는 것이 필요할 수 있습니다. 최종 사용자의 컴퓨터를 원격으로 진단할 계획 이라면 디스크 지우기 및 레지스트리 편집기와 같은 일부 도구를 사용 하지 않도록 설정 하 고 원격 연결을 비롯 한 다른 도구를 사용 하도록 설정할 수 있습니다.

DaRT 복구 이미지를 만들 때 추가 드라이버 또는 파일을 포함할 것인지 여부도 지정 합니다. DaRT 복구 이미지에 포함 하려는 추가 드라이버 또는 파일의 위치를 확인 합니다.

DaRT 도구에 대 한 자세한 내용은 [dart 8.0의 도구 개요](overview-of-the-tools-in-dart-80-dart-8.md)를 참조 하세요. 보안 복구 이미지를 만드는 데 도움이 되는 방법에 대 한 자세한 내용은 [DaRT 8.0의 보안 고려 사항을](security-considerations-for-dart-80--dart-8.md)참조 하세요.

## 복구 이미지에 대 한 필수 조건


DaRT 복구 이미지를 만들려면 다음 항목이 필요 하거나 권장 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>요소일</strong></p></td>
<td align="left"><p><strong>세부 정보</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 원본 파일</p></td>
<td align="left"><p>DaRT 복구 이미지를 만드는 데 필요 합니다. Windows 8 DVD 또는 Windows 8 원본 파일의 경로를 제공 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>플랫폼용 Windows 디버깅 도구</p></td>
<td align="left"><p><strong>충돌 분석기를 실행 </strong> 하 여 컴퓨터 오류의 원인을 확인할 때 필요 합니다. DaRT 복구 이미지를 만들 때 Windows 디버깅 도구의 경로를 지정 하는 것이 좋습니다. Windows 디버깅 도구를 다운로드 <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> 하 고 windows 용 디버깅 도구를 설치할 수 있습니다. </a></p></td>
</tr>
<tr class="even">
<td align="left"><p>선택 사항: <strong> Defender </strong> 정의</p></td>
<td align="left"><p>Defender를 <strong> 실행할 때 defender에 대 한 최신 정의가 </strong> 필요 합니다 <strong> </strong> . Defender를 실행할 때 정의를 다운로드할 수 있지만 <strong> </strong> , 문제가 있는 컴퓨터에 네트워크 연결이 없는 경우에도 최신 정의로 도구를 계속 실행할 수 있도록 DaRT 복구 이미지를 만들 때 최신 정의를 다운로드 하는 것이 좋습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>선택 사항: 충돌 분석기에서 사용할 Windows 기호 파일 <strong></strong></p></td>
<td align="left"><p>일반적으로 디버깅 정보는 프로그램과는 별도의 기호 파일에 저장 됩니다. 작업이 중지 된 경우와 같이 응답을 중지 한 응용 프로그램을 디버깅 하는 경우 기호 정보에 액세스할 수 있어야 합니다. 자세한 내용은 <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> 충돌 분석기를 사용 하 여 시스템 오류 진단을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[DaRT 8.0 배포 계획](planning-to-deploy-dart-80-dart-8.md)

 

 





