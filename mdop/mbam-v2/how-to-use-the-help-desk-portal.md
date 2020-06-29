---
title: 지원 센터 포털을 사용하는 방법
description: 지원 센터 포털을 사용하는 방법
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826328"
---
# 지원 센터 포털을 사용하는 방법


MBAM 관리 및 모니터링 웹 사이트는 지원 센터 포털이 라고도 하며, Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 인프라의 일부로 설치 된 BitLocker 드라이브 암호화에 대 한 관리 인터페이스입니다. 다음 섹션에서는이 웹 사이트를 사용 하 여 보고서를 검토 하 고, 최종 사용자의 드라이브를 복구 하 고, 최종 사용자의 Tpm을 관리 하는 방법에 대해 설명 합니다.

## <a href="" id="bkmk-reports"></a>보고


MBAM Active Directory 및 클라이언트 컴퓨터에서 정보를 수집 하 여 다양 한 보고서를 실행 하 여 BitLocker 사용 및 준수를 모니터링할 수 있습니다. 관리 및 모니터링 웹 사이트의 **보고서** 섹션을 사용 하 여 엔터프라이즈 준수, 개별 컴퓨터 및 키 복구 작업에 대 한 보고서를 생성할 수 있습니다. 각 보고서에 대 한 설명은 [MBAM 보고서 이해](understanding-mbam-reports-mbam-2.md)를 참조 하세요.

**보고서에 액세스 하려면**

1.  웹 브라우저를 열고 MBAM 관리 및 모니터링 웹 사이트로 이동 합니다.

2.  왼쪽 창에서 **보고서** 를 선택 합니다.

3.  상단 메뉴 모음에서 생성할 보고서 유형을 선택 합니다. 보고서를 저장 하려면 보고서 메뉴 모음에서 **내보내기** 단추를 클릭 합니다.

MBAM 보고서를 실행 하는 방법에 대 한 자세한 내용은 [Mbam 보고서를 생성 하는 방법을](how-to-generate-mbam-reports-mbam-2.md)참조 하세요.

## <a href="" id="bkmk-drirec"></a>드라이브 복구


관리 및 모니터링 웹 사이트의 **드라이브 복구** 기능을 통해 특정 관리자 역할 (예: 지원 센터 사용자)이 Mbam 클라이언트에서 수집한 복구 키 데이터에 액세스할 수 있습니다. 이 데이터는 BitLocker가 복구 모드로 전환 될 때 BitLocker로 보호 되는 드라이브에 액세스 하는 데 사용 될 수 있습니다. 복구 모드의 드라이브를 복구 하는 방법에 대 한 지침은 [복구 모드에서 드라이브를 복구 하는 방법을](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)참조 하세요.

또한 옮겨진 드라이브나 손상 된 드라이브는 복구할 수 있습니다.

-   [이동된 드라이브를 복구하는 방법](how-to-recover-a-moved-drive-mbam-2.md)

-   [손상된 드라이브를 복구하는 방법](how-to-recover-a-corrupted-drive-mbam-2.md)

BitLocker로 보호 되는 드라이브를 복구 하는 방법에 대 한 자세한 내용은 [MBAM을 사용 하 여 Bitlocker 관리 수행](performing-bitlocker-management-with-mbam-mbam-2.md)을 참조 하세요.

## <a href="" id="bkmk-manatpm"></a>TPM 관리


관리 및 모니터링 웹 사이트의 TPM 관리 기능은 사용자에 게 MBAM 클라이언트에서 수집한 TPM 데이터에 대 한 특정 관리자 역할 (예: "MBAM 헬프데스크 사용자")을 제공 합니다. TPM 잠금에서 관리자는 관리 및 모니터링 웹 사이트를 사용 하 여 TPM 잠금을 해제 하는 데 필요한 암호 파일을 검색할 수 있습니다. Tpm 잠금 후 TPM을 다시 설정 하는 방법에 대 한 지침은 [Tpm 잠금을 다시 설정](how-to-reset-a-tpm-lockout-mbam-2.md)하는 방법을 참조 하세요.

## <a href="" id="bkmk-helpdesk"></a> MBAM 지원 센터 작업


관리 및 모니터링 웹 사이트는 BitLocker로 보호 되는 하드웨어 관리, 드라이브 복구, 보고서 실행 등의 다양 한 관리 작업에 사용할 수 있습니다. &lt;설치 프로세스 중에 사용자 지정할 수 있지만 기본적으로 관리 및 모니터링 웹 사이트의 URL은 Http://*MBAMAdministrationServername*입니다 &gt; .

**참고**  관리 및 모니터링 웹 사이트에서 제공 하는 다양 한 기능에 액세스 하려면 해당 사용자 계정과 연결 된 적절 한 역할이 있어야 합니다. 사용자 역할을 이해 하는 방법에 대 한 자세한 내용은 [MBAM 관리자 역할을 관리 하는 방법을](how-to-manage-mbam-administrator-roles-mbam-2.md)참조 하세요.

 

다음 링크를 사용 하 여 관리 및 모니터링 웹 사이트를 사용 하 여 수행할 수 있는 작업에 대 한 정보를 찾습니다.

-   [TPM 잠금을 다시 설정하는 방법](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [복구 모드에서 드라이브를 복구하는 방법](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [이동된 드라이브를 복구하는 방법](how-to-recover-a-moved-drive-mbam-2.md)

-   [손상된 드라이브를 복구하는 방법](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





