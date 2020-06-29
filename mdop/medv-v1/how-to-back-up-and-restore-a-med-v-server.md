---
title: MED-V 서버를 백업 및 복원하는 방법
description: MED-V 서버를 백업 및 복원하는 방법
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823088"
---
# MED-V 서버를 백업 및 복원하는 방법


서버에 있는 XML 파일을 백업 하 고 서버에 데이터가 손실 되는 경우 복원할 수 있습니다.

**MED-V 서버를 백업 하려면**

-   * &lt; InstallDir &gt; \\Servers\\configurationserver*에 있는 다음 파일을 백업 합니다.

    **참고**  구성이 기본값에서 변경 된 경우 파일이 다른 위치에 저장 될 수 있습니다.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **참고**  또한 ServerSettings.xml 파일도 백업할 수 있습니다. 그러나 특정 구성이 변경 된 경우 (예: 원본 서버에서 MED-V VM 디렉터리는 "*c:\\vms*"에 있으며 해당 디렉터리가 새 서버에 존재 하지 않는 경우) 오류가 발생할 수 있습니다.

     

**MED-V 서버를 복원 하려면**

1.  새 MED-V 서버를 설치 합니다.

2.  백업 파일을 다음 디렉터리에 복사 합니다.

    *&lt;InstallDir &gt; \\Servers\\configurationserver*

3.  MED-V 서비스를 다시 시작 합니다.

 

 





