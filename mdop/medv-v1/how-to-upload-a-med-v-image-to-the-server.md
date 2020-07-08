---
title: 서버에 MED-V 이미지를 업로드하는 방법
description: 서버에 MED-V 이미지를 업로드하는 방법
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825703"
---
# 서버에 MED-V 이미지를 업로드하는 방법


MED-V 이미지를 테스트 한 후에 압축 한 다음 서버로 업로드할 수 있습니다. 이미지 웹 배포 서버를 구성 하는 방법에 대 한 자세한 내용은 [이미지 웹 배포 서버를 구성 하는 방법을](how-to-configure-the-image-web-distribution-server.md)참조 하세요.

MED-V 이미지를 압축 하 여 서버에 업로드 한 후에는 엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 사용자에 게 배포 하거나 배포 패키지를 사용 하 여 사용자가 다운로드할 수 있습니다. 엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 배포 하는 방법에 대 한 자세한 내용은 [엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 Med-v 작업 영역 배포](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)를 참조 하세요. 패키지를 사용 하 여 배포 하는 방법에 대 한 자세한 내용은 [배포 패키지를 사용 하 여 Med-v 작업 영역 배포](deploying-a-med-v-workspace-using-a-deployment-package.md)를 참조 하세요.

**참고**  
이미지를 업로드 하기 전에 브라우저 설정에 웹 프록시가 정의 되어 있지 않으며 Windows 업데이트가 현재 실행 되 고 있지 않은지 확인 합니다.



**서버에 MED-V 이미지를 업로드 하려면**

1.  **로컬 압축 이미지** 창에서 만든 이미지를 선택 합니다.

2.  **업로드**를 클릭 합니다.

    이미지가 서버에 업로드 됩니다. 이는 시간이 오래 걸릴 수가 있습니다.

    서버에 있는 이미지는 다음 표에 나열 된 속성을 사용 하 여 정의 됩니다.

**서버 속성에 압축 된 이미지**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이미지 이름</p></td>
<td align="left"><p>관리자가 이미지를 만들었을 때 정의 된 압축 이미지의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>버전</p></td>
<td align="left"><p>표시 된 이미지의 버전입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이전 버전은 삭제 되지 않는 한 유지 됩니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>파일 크기 (압축)</p></td>
<td align="left"><p>이미지의 실제 압축 크기입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이미지 크기 (압축 되지 않음)</p></td>
<td align="left"><p>물리적으로 압축 되지 않은 이미지 크기입니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법](how-to-install-med-v-client-and-med-v-management-console.md)

[MED-V 관리 콘솔 사용자 인터페이스 사용](using-the-med-v-management-console-user-interface.md)

[MED-V에 대한 가상 PC 이미지 만들기](creating-a-virtual-pc-image-for-med-v.md)

[MED-V 이미지를 압축하는 방법](how-to-pack-a-med-v-image.md)









