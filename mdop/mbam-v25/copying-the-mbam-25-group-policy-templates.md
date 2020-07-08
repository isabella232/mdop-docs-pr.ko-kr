---
title: MBAM 2.5 그룹 정책 템플릿 복사
description: MBAM 2.5 그룹 정책 템플릿 복사
author: dansimp
ms.assetid: e526ecec-07ff-435e-bc90-3084b617b84b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/28/2017
ms.openlocfilehash: a3436552256b1632a11037dc94751207cde89d5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825223"
---
# MBAM 2.5 그룹 정책 템플릿 복사


MBAM 클라이언트 설치를 배포 하기 전에 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정이 포함 된 MBAM 그룹 정책 템플릿을 다운로드 해야 합니다. 서식 파일을 다운로드 한 후에는 그룹 정책 설정을 엔터프라이즈에서 구현 하도록 설정 합니다.

## MDOP 그룹 정책 템플릿 다운로드 및 배포


MDOP 그룹 정책 템플릿은 기술 및 버전별 그룹화 된 자동 압축 풀림 압축 파일에서 다운로드할 수 있습니다.

**MDOP 그룹 정책 템플릿을 다운로드 하 고 배포 하는 방법**

1. [Microsoft 데스크톱 최적화 팩 그룹 정책 관리 템플릿에서](https://www.microsoft.com/download/details.aspx?id=55531)MDOP 그룹 정책 서식 파일을 다운로드 합니다.

2. 다운로드 한 파일을 실행 하 여 서식 파일 폴더의 압축을 풉니다.

   **Warning**  
   그룹 정책 배포 디렉터리로 직접 서식 파일의 압축을 풀지 마세요. 여러 기술과 버전이이 파일에 번들로 제공 됩니다.



3. 추출 된 폴더에서 기술-버전의 admx 파일을 찾습니다. 특정 MDOP 기술에는 그룹 정책 개체 (Gpo) 집합이 여러 개 있습니다. 예를 들어 MBAM에는 MBAM 관리 설정과 MBAM 사용자 설정이 포함 됩니다.

4. 언어 문화권에 따라 적절 한 adml 파일을 찾습니다 (영어-미국에 해당 하는 *en-us* ).

5. Admx 및 adml 파일을 정책 정의 폴더에 복사 합니다. 템플릿을 저장 하는 위치에 따라 로컬 장치 또는 도메인의 컴퓨터에서 그룹 정책 설정을 구성할 수 있습니다.

   **로컬 파일** 로컬 장치에서 그룹 정책 설정을 구성 하려면 서식 파일을 다음 위치에 복사 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">파일 형식</th>
   <th align="left">파일 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>그룹 정책 템플릿 (admx)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;강력한 &gt; policydefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>그룹 정책 언어 파일 (adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;강력한 &gt; policydefinitions</strong><code>[MUIculture]</code></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Domain central store.** To enable Group Policy settings configuration by a Group Policy administrator from any computer on the domain, copy files to the following locations on the domain controller:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File type</th>
<th align="left">File location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Group Policy template (.admx)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Group Policy language file (.adml)</p></td>
<td align="left"><p><code>%systemroot%</code>\<strong>sysvol\domain\policies\PolicyDefinitions\[MUIculture]</strong><code>\[MUIculture]</code></p>
<p>For example, the U.S. English ADML language-specific file will be stored in %systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.</p></td>
</tr>
</tbody>
</table>
~~~



6. GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 사용 하 여 그룹 정책 설정을 편집 하 여 MDOP 기술에 대 한 그룹 정책 설정을 구성 합니다. 자세한 내용은 [MBAM 2.5 그룹 정책 설정을 편집](editing-the-mbam-25-group-policy-settings.md) 을 참조 하세요.

   그룹 정책 설정에 대 한 설명은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.


## 관련 항목


[MBAM 2.5 그룹 정책 개체 배포](deploying-mbam-25-group-policy-objects.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.






