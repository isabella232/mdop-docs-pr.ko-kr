---
title: 사용자 권한을 구성하는 방법
description: 사용자 권한을 구성하는 방법
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817733"
---
# 사용자 권한을 구성하는 방법


**권한** 레지스트리 키 (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions) 아래의 키 값을 편집 하 여 관리 권한이 없는 사용자에 대 한 일부 작업을 사용 하도록 설정 하거나 해제할 수 있습니다. 이 키는 관리자 권한이 있는 사용자가 이러한 키 값을 편집할 수 있기 때문에 특별 한 보안을 제공 하는 것이 아니라 사용자가 실수를 하지 않도록 하는 데 주로 사용 되는 것입니다. 다음 절차에서는 키 값을 변경 하는 방법의 예를 보여 줍니다. App-v (Application Virtualization) 클라이언트 레지스트리 키 및 값에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=121528> 하세요.

**사용자 권한을 변경 하려면**

1.  사용자가 오프 라인 모드에서 클라이언트를 실행 하도록 선택할 수 있도록 하려면 다음 키 값을 1로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode

2.  사용자가 사용자 인터페이스를 통해 모든 응용 프로그램을 볼 수 있도록 하려면 다음 키 값을 1로 설정 합니다. 값을 0으로 설정 하면 사용자가 사용할 수 있는 응용 프로그램만 볼 수 있습니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications

## 관련 항목


[명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Application Virtualization Client의 사용자 액세스 권한](user-access-permissions-in-application-virtualization-client.md)

 

 





