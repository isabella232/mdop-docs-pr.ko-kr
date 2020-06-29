---
title: MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법
description: MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법
author: dansimp
ms.assetid: fdb64505-6c66-4fdf-ad74-a6a161191e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 5bc5f8d536c113ccbc0a1931e6c7e4ed3c7a9a37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826918"
---
# MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법


그룹 정책 템플릿, admx 및 adml 파일을 사용 하 여 특정 Microsoft 데스크톱 최적화 팩 (MDOP) 기술 (예: App-v, UE-V 또는 MBAM)의 기능 설정을 관리할 수 있습니다. MDOP 그룹 정책 템플릿은 기술 및 버전별 그룹화 된 자동 압축 풀림 압축 파일에서 다운로드할 수 있습니다.

## MDOP 그룹 정책 서식 파일

**MDOP 그룹 정책 템플릿을 다운로드 하 고 배포 하는 방법**

1. 최신 [MDOP 그룹 정책 서식 파일](https://www.microsoft.com/download/details.aspx?id=55531) 다운로드 

2. 실행 하 여 다운로드 한 .cab 파일 확장 `expand <download_folder>\MDOP_ADMX_Templates.cab -F:* <destination_folder>`

   **Warning**  
   그룹 정책 배포 디렉터리로 직접 서식 파일의 압축을 풀지 마세요. 여러 기술과 버전이이 파일에 번들로 제공 됩니다.

3. 추출 된 폴더에서 기술-버전의 admx 파일을 찾습니다. 특정 MDOP 기술에는 그룹 정책 개체 (Gpo) 집합이 여러 개 있습니다. 예를 들어 MBAM에는 MBAM 관리 설정과 MBAM 사용자 설정이 포함 됩니다.

4. 언어 문화권에 따라 적절 한 adml 파일을 찾습니다 (즉, *en-us* 는 영어-미국에 해당).

5. Admx 및 adml 파일을 정책 정의 폴더에 복사 합니다. 템플릿을 저장 하는 위치에 따라 로컬 장치 또는 도메인의 컴퓨터에서 그룹 정책 설정을 구성할 수 있습니다.

   - **로컬 파일:** 로컬 장치에서 그룹 정책 설정을 구성 하려면 서식 파일을 다음 위치에 복사 합니다.

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

   - **도메인 중앙 스토어:** 도메인의 컴퓨터에서 그룹 정책 관리자가 그룹 정책 설정 구성을 사용 하도록 설정 하려면 도메인 컨트롤러의 다음 위치에 파일을 복사 합니다.

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
   <td align="left"><p><code>%systemroot%</code>&lt;강력한 &gt; sysvol\domain\policies\PolicyDefinitions</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>그룹 정책 언어 파일 (adml)</p></td>
   <td align="left"><p><code>%systemroot%</code>&lt;강력한 &gt; sysvol\domain\policies\PolicyDefinitions [MUIculture]</strong><code>[MUIculture]</code></p>
   <p>예를 들어 미국 영어 ADML 언어 관련 파일 은%systemroot%\sysvol\domain\policies\PolicyDefinitions\en-us.에 저장 됩니다.</p></td>
   </tr>
   </tbody>
   </table>

6. GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 사용 하 여 그룹 정책 설정을 편집 하 여 MDOP 기술에 대 한 그룹 정책 설정을 구성 합니다.

### 기술별 MDOP 그룹 정책

지원 되는 MDOP 그룹 정책에 대 한 자세한 내용은 해당 기술에 대 한 특정 설명서를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">MDOP 기술</th>
<th align="left">버전 번들</th>
<th align="left">참고</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>App-V(Application Virtualization)</strong></p></td>
<td align="left"><p>App-v 5.0 및 App-V 5.0 서비스 팩</p></td>
<td align="left"><p><a href="../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md" data-raw-source="[How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](../appv-v5/how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)">ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>UE-V(User Experience Virtualization)</strong></p></td>
<td align="left"><p>UE-V 2.0 및 UE-V 2.1</p></td>
<td align="left"><p><a href="../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md" data-raw-source="[Configuring UE-V 2.x with Group Policy Objects](../uev-v2/configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)">그룹 정책 개체를 사용 하 여 UE-V 2. x 구성</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>UE-V 1.0 (1.0 SP1 포함)</p></td>
<td align="left"><p><a href="../uev-v1/configuring-ue-v-with-group-policy-objects.md" data-raw-source="[Configuring UE-V with Group Policy Objects](../uev-v1/configuring-ue-v-with-group-policy-objects.md)">그룹 정책 개체를 사용하여 UE-V 구성</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>MBAM(Microsoft BitLocker Administration and Monitoring)</strong></p></td>
<td align="left"><p>MBAM 2.5</p></td>
<td align="left"><p><a href="../mbam-v25/planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](../mbam-v25/planning-for-mbam-25-group-policy-requirements.md)">MBAM 2.5 그룹 정책 요구 사항 계획</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 2.0 (2.0 SP1 포함)</p></td>
<td align="left"><p><a href="../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](../mbam-v2/planning-for-mbam-20-group-policy-requirements-mbam-2.md)">MBAM 2.0 그룹 정책 요구 사항 계획</a></p>
<p><a href="../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](../mbam-v2/deploying-mbam-20-group-policy-objects-mbam-2.md)">MBAM 2.0 그룹 정책 개체 배포</a></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>MBAM 1.0</p></td>
<td align="left"><p><a href="../mbam-v1/how-to-edit-mbam-10-gpo-settings.md" data-raw-source="[How to Edit MBAM 1.0 GPO Settings](../mbam-v1/how-to-edit-mbam-10-gpo-settings.md)">MBAM 1.0 GPO 설정을 편집하는 방법</a></p></td>
</tr>
</tbody>
</table>

 

 

 





