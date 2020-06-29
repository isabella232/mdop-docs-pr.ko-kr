---
title: 관리 및 모니터링 웹 사이트를 사용하는 방법
description: 관리 및 모니터링 웹 사이트를 사용하는 방법
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813044"
---
# 관리 및 모니터링 웹 사이트를 사용하는 방법


관리 및 모니터링 웹 사이트는 지원 센터 라고도 하며, BitLocker 드라이브 암호화를 위한 관리 인터페이스입니다. 다음 섹션에서 설명 하는 대로 웹 사이트를 사용 하 여 보고서를 검토 하 고, 최종 사용자의 드라이브를 복구 하 고, 최종 사용자의 Tpm을 관리 합니다.

**참고**  독립 실행형 토폴로지에서 MBAM을 사용 하는 경우 관리 및 모니터링 웹 사이트에서 모든 보고서를 볼 수 있습니다. Configuration Manager 통합 토폴로지를 사용 하는 경우 관리 및 모니터링 웹 사이트에서 계속 표시 되는 복구 감사 보고서를 제외한 Configuration Manager의 모든 보고서를 볼 수 있습니다. 보고서에 대 한 자세한 내용은 [MBAM 2.5 BitLocker 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)를 참조 하세요.

 

## 관리 및 모니터링 웹 사이트 사용을 위한 필수 역할


관리 및 모니터링 웹 사이트의 특정 영역에 액세스 하려면 Active Directory에서 만드는 그룹인 다음 역할 중 하나가 있어야 합니다. 이러한 그룹에 임의의 이름을 사용할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">계정</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 모든 영역에 대 한 액세스를 제공 합니다. 이 역할을 사용 하는 사용자는 최종 사용자의 도메인 및 사용자 이름 대신 복구 키만 입력할 수 있으며, 사용자가 드라이브를 복구 하는 데 도움이 됩니다. 사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 사용자 그룹 권한 보다 우선 합니다.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 대 한 액세스를 제공 합니다. 이 역할이 있는 개인은 두 영역 중 하나를 사용할 때 최종 사용자의 도메인 및 계정 이름을 포함 하 여 모든 필드를 채워야 합니다.</p>
<p>사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 사용자 그룹 권한 보다 우선 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 보고서 사용자</p></td>
<td align="left"><p><strong> </strong> 관리 및 모니터링 웹 사이트의 보고서 영역에 있는 보고서에 대 한 액세스를 제공 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관리 및 모니터링 웹 사이트에서 수행할 수 있는 작업


다음 표에서는 관리 및 모니터링 웹 사이트에서 수행할 수 있는 작업을 요약 하 고 각 작업에 대 한 자세한 정보에 대 한 링크를 제공 합니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">작업에 액세스 하는 웹 사이트 영역</th>
<th align="left">설명</th>
<th align="left">자세한 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>보고서 보기</p></td>
<td align="left"><p>보고</p></td>
<td align="left"><p>보고서를 실행 하 여 BitLocker 사용, 준수 및 키 복구 작업을 모니터링할 수 있습니다. 보고서는 엔터프라이즈 준수, 개별 컴퓨터 및 복구 키를 요청한 사용자, 그리고 특정 컴퓨터에 대 한 TPM 소유자 인증 패키지에 대 한 데이터를 제공 합니다.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">독립 실행형 토폴로지에 대한 MBAM 2.5 보고서 보기</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>분실 하거나 도난당 한 컴퓨터의 BitLocker 암호화 상태 확인</p></td>
<td align="left"><p>보고</p></td>
<td align="left"><p>컴퓨터를 분실 하거나 도난당 한 경우 볼륨이 암호화 되었는지 확인 합니다.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>손실 된 드라이브 복구</p></td>
<td align="left"><p>드라이브 복구</p></td>
<td align="left"><p>드라이브 복구 방법:</p>
<ul>
<li><p>복구 모드</p></li>
<li><p>님이 이동 했습니다</p></li>
<li><p>손상 된 경우</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">복구 모드에서 드라이브를 복구하는 방법</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">이동된 드라이브를 복구하는 방법</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">손상된 드라이브를 복구하는 방법</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>TPM 잠금 다시 설정</p></td>
<td align="left"><p>TPM 관리</p></td>
<td align="left"><p>MBAM 클라이언트에서 수집한 TPM 데이터에 대 한 액세스를 제공 합니다. TPM 잠금에서 관리 및 모니터링 웹 사이트를 사용 하 여 TPM 잠금을 해제 하는 데 필요한 암호 파일을 검색 합니다.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">TPM 잠금을 다시 설정하는 방법</a></p></td>
</tr>
</tbody>
</table>

 


## 관련 항목


[MBAM 2.5를 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





