---
title: DaRT 10 지원되는 구성
description: DaRT 10 지원되는 구성
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813137"
---
# DaRT 10 지원되는 구성


이 항목에서는 환경에서 Microsoft 진단 및 복구 도구 집합 (DaRT) 10을 설치 하 고 실행 하는 데 필요한 필수 구성 요구 사항 및 지원 되는 구성을 지정 합니다. 운영 체제 요구 사항과 DaRT 10을 실행 하는 데 필요한 시스템 요구 사항이 모두 지정 되었습니다. DaRT 복구 이미지를 만들기 위해 고려해 야 하는 필수 구성 요소에 대 한 자세한 내용은 [dart 10 복구 이미지 만들기 계획 수립](planning-to-create-the-dart-10-recovery-image.md)을 참조 하세요.

이후 릴리스에 적용 되는 지원 되는 구성에 대해서는 해당 릴리스에 대 한 설명서를 참조 하세요.

두 가지 방법 중 하나로 DaRT를 설치할 수 있습니다. 모든 기능을 IT 관리자 컴퓨터에 설치 하 여 DaRT 실행과 관련 된 모든 작업을 수행할 수 있습니다. 또는 관리자 컴퓨터에 복구 이미지를 만드는 DaRT 기능만 설치한 다음 헬프 데스크 컴퓨터에서 DaRT (DaRT 원격 연결 뷰어)를 실행 하는 데 사용 되는 기능을 설치할 수 있습니다.

## DaRT 10 필수 소프트웨어


DaRT를 설치 하기 전에 다음 선행 조건이 충족 되는지 확인 합니다.

### 관리자 컴퓨터 필수 구성 요소

다음 표에는 DaRT 10 및 모든 DaRT 도구를 설치 하는 경우 관리자 컴퓨터의 설치 필수 구성 요소가 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows ADK (평가 및 개발 키트)</strong></p></td>
<td align="left"><p>DaRT 복구 이미지 마법사에 필요 합니다. Windows 이미지를 사용자 지정, 배포 및 서비스 하는 데 사용 되며 windows 사전 설치 환경 (Windows PE)이 포함 된 배포 도구가 포함 됩니다. 원격 연결 뷰어 및/또는 충돌 분석기만 설치 하는 경우에는 ADK가 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows 개발 키트 또는 소프트웨어 개발 키트 (선택 사항)</strong></p></td>
<td align="left"><p>충돌 분석기에는 Windows 드라이버 키트의 Windows 10 디버깅 도구가 있어야 메모리 덤프 파일을 분석할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows 10 64 비트 또는 32 비트 ISO 이미지</strong></p></td>
<td align="left"><p>DaRT에는 Windows 10 미디어의 windows RE (Windows 복구 환경) 이미지가 필요 합니다. 만들려는 DaRT 복구 이미지 형식에 따라 32 비트 또는 64 비트 버전의 Windows 10을 다운로드 합니다. 환경에서 두 시스템 유형을 모두 지 원하는 경우 두 버전의 Windows 10을 다운로드 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 지원 센터 컴퓨터 필수 구성 요소

다음 표에는 DaRT 10 원격 연결 뷰어를 실행 하는 경우 지원 센터 컴퓨터용 설치 필수 구성 요소가 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>DaRT 10 원격 연결 뷰어</strong></p></td>
<td align="left"><p>Windows 10 운영 체제에 설치 되어 있어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows용 디버깅 도구</strong></p></td>
<td align="left"><p>충돌 분석기 도구를 설치 하는 경우에만 필요 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 최종 사용자 컴퓨터 필수 구성 요소

Windows 10 운영 체제 이외의 최종 사용자 컴퓨터에 설치 해야 하는 필수 소프트웨어는 없습니다.

## <a href="" id="---------dart-10-operating-system-requirements"></a> DaRT 10 운영 체제 요구 사항


### 관리자 컴퓨터 시스템 요구 사항

다음 표에는 DaRT 10 관리자 컴퓨터 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  관리자 컴퓨터에 설치 하려는 추가 도구에 충분 한 공간을 할당 했는지 확인 합니다.

 

**참고**  Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
<th align="left">운영 체제 요구 사항</th>
<th align="left">DaRT를 실행 하기 위한 RAM 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>2GB</p></td>
<td align="left"><p>2.5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>1.5 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> DaRT 지원 센터 컴퓨터 시스템 요구 사항

지원 센터에서 원격으로 컴퓨터 문제를 해결할 수 있도록 허용 하는 경우 지원 센터 컴퓨터에 원격 연결 뷰어가 설치 되어 있어야 합니다. 선택적으로 지원 센터 컴퓨터에 크래시 분석기 도구를 설치할 수 있습니다.

DaRT 10 헬프 데스크 근로자는 DaRT 7.0, DaRT 8.0, DaRt 8.1 또는 DaRT 10 원격 연결 뷰어를 사용 하 여 DaRT 10 컴퓨터에 연결할 수 있습니다. Dart 7.0, DaRT 8.0 및 DaRt 8.1, 원격 연결 뷰어에는 각각 Windows 7, Windows 8 또는 Windows 8.1 운영 체제가 필요 하지만, DaRT 10 원격 연결 뷰어에는 Windows 10이 필요 합니다. DaRT 10 원격 연결 뷰어와 기타 모든 DaRT 10 도구는 Windows 10을 실행 하는 컴퓨터에만 설치할 수 있습니다.

다음 표에는 DaRT 헬프 데스크 컴퓨터 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
<th align="left">운영 체제 요구 사항</th>
<th align="left">DaRT를 실행 하기 위한 RAM 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>2GB</p></td>
<td align="left"><p>2.5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows10 (원격 연결 뷰어 10.0에만 해당)</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>1.5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>2GB</p></td>
<td align="left"><p>2.5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (원격 연결 뷰어 8.0에만 해당)</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>1.5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (원격 연결 뷰어 7.0에만 해당)</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 비트 또는 32 비트</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>해당 없음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>2GB</p></td>
<td align="left"><p>1.0 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>2GB</p></td>
<td align="left"><p>1.0 GB</p></td>
</tr>
</tbody>
</table>

 

DaRT에는 최종 사용자 컴퓨터에 대해 다음과 같은 최소 하드웨어 요구 사항이 있습니다.

Cd, dvd 또는 USB를 사용 하 여 엔터프라이즈에서 DaRT를 배포 하는 경우에만 필요 합니다.

CD 또는 DVD, USB 플래시 드라이브 또는 원격 또는 복구 파티션에서 컴퓨터를 시작 하기 위한 BIOS 지원입니다.

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> DaRT 10 최종 사용자 컴퓨터 시스템 요구 사항

DaRT 10의 진단 및 복구 도구 집합 창에서는 최종 사용자 컴퓨터가 DaRT에 사용할 수 있는 지정 된 시스템 메모리 크기와 함께 다음 운영 체제 중 하나를 사용 해야 합니다.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
<th align="left">운영 체제 요구 사항</th>
<th align="left">RAM 요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>2GB</p></td>
<td align="left"><p>2.5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>모든 버전</p></td>
<td align="left"><p>해당 없음</p></td>
<td align="left"><p>32비트</p></td>
<td align="left"><p>1GB</p></td>
<td align="left"><p>1.5 GB</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[DaRT 10 배포 계획](planning-to-deploy-dart-10.md)

 

 





