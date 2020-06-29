---
title: 이미지 사전 준비를 구성하는 방법
description: 이미지 사전 준비를 구성하는 방법
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826408"
---
# 이미지 사전 준비를 구성하는 방법


**참고**  이미지 사전 준비는 초기 이미지 다운로드에만 유용 합니다. 이미지 업데이트에는 지원 되지 않습니다.

 

## 이미지 사전 준비를 구성하는 방법


**이미지 사전 준비를 구성 하려면**

1.  클라이언트 컴퓨터의 이미지 저장소 디렉터리 아래에서 준비 단계 이미지에 대 한 폴더를 만들고 *Med-v 이미지*의 이름을 지정 합니다.

    **참고**  이 폴더는 *Med-v 이미지*라고 합니다.

     

2.  MED-V 이미지 폴더 내에 하위 폴더를 만들고 이름 *에 해당 하*는 이름을 지정 합니다.

    **참고**  이 폴더는 *Prestageages*기간으로 호출 해야 합니다.

     

3.  *Med-v 이미지* 폴더에 Acl (액세스 제어 목록) 보안을 적용 하려면 다음 ACL을 설정 합니다.

    **NT AUTHORITY\\Authenticated 사용자: (OI) (CI) (특별 액세스:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 파일 \ _APPEND \ _DATA**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **참고**  ACL 보안을 *Med-v 이미지* 폴더에 적용 하는 것이 좋습니다.

     

4.  *사전 Stageages 연령* 폴더에 acl 보안을 적용 하려면 다음 ACL을 설정 합니다.

    **NT AUTHORITY\\Authenticated 사용자: (OI) (CI) (특별 액세스:)**

    **READ\_CONTROL**

    **SYNCHRONIZE**

    **파일 \ _GENERIC \ _READ**

    **파일 \ _READ \ _DATA**

    **파일 \ _READ \ _EA**

    **파일 \ _READ \ _ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **참고**  *사전* 에 ACL 보안을 적용 하는 것이 좋습니다.

     

5.  이미지 파일 (CKM 및 INDEX files)을 *Prestageages 연령* 폴더에 푸시합니다.

    **참고**  이미지 파일을 스테이지 프리 폴더로 푸시한 후에는 데이터 무결성 검사를 실행 하 고 파일을 읽기 전용으로 표시 하는 것이 좋습니다.

     

6.  MED-V 클라이언트 설치: *Client.MSI VMSFOLDER = "C:\\MED-V Images"* 에 다음 매개 변수를 포함 합니다.

## 단계 전 위치를 업데이트 하는 방법


**단계 전 위치 업데이트**

1.  레지스트리 키 *PrestagedImagesPath*는 기본 이미지 위치를 가리킵니다. 이 파일은 다음 디렉터리에 있습니다.

    -   X86- `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   X64- `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  이미지가 다른 위치에 있는 경우 경로를 변경 합니다.

 

 





