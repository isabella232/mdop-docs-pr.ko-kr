---
title: UE-V 1.0 보안 고려 사항
description: UE-V 1.0 보안 고려 사항
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823998"
---
# UE-V 1.0 보안 고려 사항


이 항목에서는 계정 및 그룹, 로그 파일, Microsoft UE-V (User Experience Virtualization)에 대 한 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 제공 합니다. 자세한 내용은 여기에 나와 있는 링크를 참조 하세요.

## UE-V 구성에 대 한 보안 고려 사항


**설정 저장소 공유를 만들 때 액세스가 필요한 사용자에 대 한 공유 액세스를 제한 합니다.**

설정 패키지에는 개인 정보가 포함 될 수 있으므로 가능 하면 보호 하는 것도 주의 해야 합니다. 일반적으로 다음을 수행 합니다.

-   공유를 액세스가 필요한 사용자로만 제한 합니다. 특정 공유에 리디렉션 폴더가 있는 사용자에 대 한 보안 그룹을 만들고 해당 사용자 에게만 액세스를 제한 합니다.

-   공유를 만들 때 공유 이름 뒤에 $를 추가 하 여 공유를 숨깁니다. 이렇게 하면 일반 브라우저에서 공유를 숨기고 네트워크 위치에 공유가 표시 되지 않습니다.

-   필요한 최소 사용 권한만 사용자에 게 부여 합니다. 필요한 사용 권한은 아래 표에 나와 있습니다.

    1.  설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left">사용자 계정</th>
        <th align="left">권장 되는 사용 권한</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>모두</p></td>
        <td align="left"><p>권한 없음</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>UE-V의 보안 그룹</p></td>
        <td align="left"><p>모든 권한</p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### Windows Server 2003 이상 서버를 사용 하 여 리디렉션 파일 공유 호스팅

사용자 설정 패키지 파일에는 클라이언트 컴퓨터와 설정 패키지를 저장 하는 서버 간에 전송 되는 개인 정보가 포함 됩니다. 이 때문에 데이터는 네트워크를 통해 이동 하는 동안 보호 되는지 확인 해야 합니다.

사용자 설정 데이터는 네트워크를 통해 전달 되는 데이터 가로채기와 같은 잠재적인 위협에 취약해 집니다. 네트워크를 통해 전달 되는 데이터 훼손 데이터를 호스팅하는 서버에 대 한 및 스푸핑.

Windows Server 2003 이상의 몇 가지 기능은 사용자 데이터를 보호 하는 데 도움이 될 수 있습니다.

-   **Kerberos** -kerberos는 모든 버전의 windows 2000 및 windows Server 2003 이상에서 표준입니다. Kerberos는 네트워크 리소스에 가장 높은 수준의 보안을 보장 합니다. NTLM은 클라이언트만 인증 합니다. Kerberos는 서버와 클라이언트를 인증 합니다. NTLM을 사용 하는 경우 클라이언트는 서버가 유효한 지 여부를 알지 못합니다. 이는 로밍 프로필의 경우와 마찬가지로 클라이언트가 서버와 개인 파일을 교환 하는 경우 특히 중요 합니다. Kerberos는 NTLM 보다 더 나은 보안을 제공 합니다. Windows NT 버전 4.0 또는 이전 버전의 운영 체제에서는 Kerberos를 사용할 수 없습니다.

-   **Ipsec** -IP 보안 프로토콜 (ipsec)은 네트워크 수준 인증, 데이터 무결성 및 암호화를 제공 합니다. IPsec은 다음을 보장 합니다.

    -   Roamed 데이터는 라우팅이 진행 되는 동안 데이터를 수정 하는 것이 안전 합니다.

    -   Roamed 데이터는 가로채기, 보기 또는 복사에서 안전 합니다.

    -   Roamed 데이터는 인증 되지 않은 사람이 액세스 하는 것을 안전 하 게 보호 합니다.

-   **Smb 서명** -Smb (서버 메시지 블록) 인증 프로토콜은 활성 메시지와 "중간자" 공격을 차단 하는 메시지 인증을 지원 합니다. SMB 서명은 각 SMB에 디지털 서명을 배치 하 여이 인증을 제공 합니다. 그러면 클라이언트와 서버에서 디지털 서명을 확인 합니다. SMB 서명을 사용 하려면 먼저 SMB 클라이언트를 사용 하도록 설정 하거나 해당 서버에서 smb를 요청 해야 합니다. SMB 서명은 성능 저하를 부과 합니다. 네트워크 대역폭을 더 이상 사용 하지 않지만 클라이언트 및 서버 쪽에서 더 많은 CPU 주기를 사용 합니다.

### 사용자 데이터를 보유 한 볼륨에 항상 NTFS 파일 시스템 사용

가장 안전한 구성의 경우 NTFS 파일 시스템을 사용 하도록 UE-V 설정 파일을 호스팅하는 서버를 구성 합니다. FAT와 달리 NTFS는 Dacl (임의 액세스 제어 목록) 및 Sacl (시스템 액세스 제어 목록)을 지원 합니다. Dacl 및 Sacl은 파일에 대 한 작업을 수행할 수 있는 사용자와 파일에서 수행 되는 작업의 로깅을 트리거하는 이벤트를 제어 합니다.

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a>네트워크를 통해 전송 되는 사용자의 파일을 암호화 하기 위해 EFS에 의존 하지 마세요.

EFS (파일 시스템 암호화)를 사용 하 여 원격 서버에서 파일을 암호화 하면 네트워크를 통해 전송 하는 동안 암호화 된 데이터가 암호화 되지 않습니다. 디스크에 저장 된 경우에만 암호화 됩니다.

예외는 시스템에 IPsec (인터넷 프로토콜 보안) 또는 WebDAV (웹 분산 작성 및 버전 관리)가 포함 된 경우에 발생 합니다. IPsec은 TCP/IP 네트워크를 통해 전송 되는 동안 데이터를 암호화 합니다. 파일을 서버의 WebDAV 폴더로 복사 하거나 이동 하기 전에 암호화 한 경우에는 전송 중에 암호화 된 상태로 유지 되 고 서버에 저장 됩니다.

### 오프 라인 파일 캐시 암호화

기본적으로 오프 라인 파일 캐시는 Acl에의 한 NTFS 파티션에서 보호 되지만, 캐시 암호화는 로컬 컴퓨터의 보안을 더욱 강화 합니다. 기본적으로 로컬 컴퓨터의 캐시는 암호화 되지 않으므로 네트워크에서 캐시 된 모든 암호화 된 파일은 로컬 컴퓨터에서 암호화 되지 않습니다. 이는 일부 환경에서 보안 위험을 초래할 수 있습니다.

암호화를 사용 하도록 설정 하면 오프 라인 파일 캐시의 모든 파일이 암호화 됩니다. 여기에는 기존 파일 암호화 및 나중에 추가 되는 파일도 포함 됩니다. 로컬 컴퓨터의 캐시 된 복사본에는 영향을 미치지만 연결 된 네트워크 복사본은 적용 되지 않습니다.

캐시는 다음 두 가지 방법 중 하나로 암호화할 수 있습니다.

1.  그룹 정책을 통해 -그룹 정책 편집기에서 컴퓨터 Configuration\\Administrative Templates\\Network\\Offline 파일에 있는 **오프 라인 파일 캐시 암호화** 설정을 사용 하도록 설정 합니다.

2.  일일이. -Windows 탐색기의 명령 메뉴에서 도구를 선택한 다음 폴더 옵션을 선택 합니다. 오프 라인 파일 탭을 선택한 다음 **데이터 보호를 위해 오프 라인 파일 암호화** 확인란을 선택 합니다.

### UE-V Agent가 각 사용자에 대 한 폴더를 만들도록 허용

UE-V가 최적으로 작동 하도록 하려면 서버에서 루트 공유만 만들고 UE-V Agent가 각 사용자에 대 한 폴더를 만들도록 합니다. UE-V를 사용 하면 적절 한 보안으로 이러한 사용자 폴더가 만들어집니다.

이 사용 권한 구성에서는 사용자가 설정 저장소에 대 한 폴더를 만들 수 있습니다. UE-V agent는 사용자 컨텍스트에서 실행 되는 동안 settingspackage 폴더를 만들고 보안 합니다. 사용자는 자신의 settingspackage 폴더에 대 한 모든 권한을 받습니다. 다른 사용자는이 폴더에 대 한 액세스 권한을 상속 받지 않습니다. 개별 사용자 디렉토리를 생성 하 고 보호할 필요는 없습니다. 이 작업은 사용자 컨텍스트에서 실행 되는 에이전트에 의해 자동으로 수행 됩니다.

**참고**  
Windows server가 설정 저장소 공유에 사용 되는 경우 추가 보안을 구성할 수 있습니다. 로컬 관리자의 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 하도록 UE-V를 구성할 수 있습니다. 추가 보안을 사용 하도록 설정 하려면 다음 명령을 사용 합니다.

1.  "RepositoryOwnerCheckEnabled" 이라는 REG \ _DWORD 레지스트리 키를에 추가 `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` 합니다.

2.  레지스트리 키 값을 1로 설정 합니다.

이 구성 설정이 설정 되어 있으면 UE-V agent가 로컬 관리자의 그룹 또는 현재 사용자가 settingspackage 폴더의 소유자 인지 확인 합니다. 그렇지 않으면 UE-V agent가 폴더에 대 한 액세스를 허용 하지 않습니다.



사용자에 대 한 폴더를 만들어야 하는 경우 올바른 사용 권한이 설정 되어 있는지 확인 합니다.

폴더를 precreate 하는 대신 UE-V agent가 사용자에 대 한 폴더를 만들 수 있도록 하는 것이 좋습니다.

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a>사용자의 홈 디렉터리에 UE-V 설정을 저장할 때 올바른 권한이 설정 되어 있는지 확인 합니다.

사용자의 홈 디렉터리로 UE-V 설정을 리디렉션하면 사용자의 홈 디렉터리에 대 한 사용 권한이 조직에 맞게 설정 되어 있는지 확인 합니다.

## 관련 항목


[UE-V 1.0에 대한 보안 및 개인 정보](security-and-privacy-for-ue-v-10.md)









