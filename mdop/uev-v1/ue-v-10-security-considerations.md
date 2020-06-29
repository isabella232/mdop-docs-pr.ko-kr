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
# <span data-ttu-id="2651b-103">UE-V 1.0 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="2651b-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="2651b-104">이 항목에서는 계정 및 그룹, 로그 파일, Microsoft UE-V (User Experience Virtualization)에 대 한 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="2651b-105">자세한 내용은 여기에 나와 있는 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2651b-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="2651b-106">UE-V 구성에 대 한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="2651b-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="2651b-107">설정 저장소 공유를 만들 때 액세스가 필요한 사용자에 대 한 공유 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="2651b-108">설정 패키지에는 개인 정보가 포함 될 수 있으므로 가능 하면 보호 하는 것도 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="2651b-109">일반적으로 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-109">In general, do the following:</span></span>

-   <span data-ttu-id="2651b-110">공유를 액세스가 필요한 사용자로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="2651b-111">특정 공유에 리디렉션 폴더가 있는 사용자에 대 한 보안 그룹을 만들고 해당 사용자 에게만 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="2651b-112">공유를 만들 때 공유 이름 뒤에 $를 추가 하 여 공유를 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="2651b-113">이렇게 하면 일반 브라우저에서 공유를 숨기고 네트워크 위치에 공유가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="2651b-114">필요한 최소 사용 권한만 사용자에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="2651b-115">필요한 사용 권한은 아래 표에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="2651b-116">설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="2651b-117">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="2651b-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="2651b-118">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="2651b-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="2651b-119">모두</span><span class="sxs-lookup"><span data-stu-id="2651b-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="2651b-120">권한 없음</span><span class="sxs-lookup"><span data-stu-id="2651b-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="2651b-121">UE-V의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="2651b-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="2651b-122">모든 권한</span><span class="sxs-lookup"><span data-stu-id="2651b-122">Full Control</span></span></p></td>
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



### <span data-ttu-id="2651b-123">Windows Server 2003 이상 서버를 사용 하 여 리디렉션 파일 공유 호스팅</span><span class="sxs-lookup"><span data-stu-id="2651b-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="2651b-124">사용자 설정 패키지 파일에는 클라이언트 컴퓨터와 설정 패키지를 저장 하는 서버 간에 전송 되는 개인 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="2651b-125">이 때문에 데이터는 네트워크를 통해 이동 하는 동안 보호 되는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="2651b-126">사용자 설정 데이터는 네트워크를 통해 전달 되는 데이터 가로채기와 같은 잠재적인 위협에 취약해 집니다. 네트워크를 통해 전달 되는 데이터 훼손 데이터를 호스팅하는 서버에 대 한 및 스푸핑.</span><span class="sxs-lookup"><span data-stu-id="2651b-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="2651b-127">Windows Server 2003 이상의 몇 가지 기능은 사용자 데이터를 보호 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="2651b-128">**Kerberos** -kerberos는 모든 버전의 windows 2000 및 windows Server 2003 이상에서 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="2651b-129">Kerberos는 네트워크 리소스에 가장 높은 수준의 보안을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="2651b-130">NTLM은 클라이언트만 인증 합니다. Kerberos는 서버와 클라이언트를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="2651b-131">NTLM을 사용 하는 경우 클라이언트는 서버가 유효한 지 여부를 알지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="2651b-132">이는 로밍 프로필의 경우와 마찬가지로 클라이언트가 서버와 개인 파일을 교환 하는 경우 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="2651b-133">Kerberos는 NTLM 보다 더 나은 보안을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="2651b-134">Windows NT 버전 4.0 또는 이전 버전의 운영 체제에서는 Kerberos를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="2651b-135">**Ipsec** -IP 보안 프로토콜 (ipsec)은 네트워크 수준 인증, 데이터 무결성 및 암호화를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="2651b-136">IPsec은 다음을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="2651b-137">Roamed 데이터는 라우팅이 진행 되는 동안 데이터를 수정 하는 것이 안전 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="2651b-138">Roamed 데이터는 가로채기, 보기 또는 복사에서 안전 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="2651b-139">Roamed 데이터는 인증 되지 않은 사람이 액세스 하는 것을 안전 하 게 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="2651b-140">**Smb 서명** -Smb (서버 메시지 블록) 인증 프로토콜은 활성 메시지와 "중간자" 공격을 차단 하는 메시지 인증을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="2651b-141">SMB 서명은 각 SMB에 디지털 서명을 배치 하 여이 인증을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="2651b-142">그러면 클라이언트와 서버에서 디지털 서명을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="2651b-143">SMB 서명을 사용 하려면 먼저 SMB 클라이언트를 사용 하도록 설정 하거나 해당 서버에서 smb를 요청 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="2651b-144">SMB 서명은 성능 저하를 부과 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="2651b-145">네트워크 대역폭을 더 이상 사용 하지 않지만 클라이언트 및 서버 쪽에서 더 많은 CPU 주기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="2651b-146">사용자 데이터를 보유 한 볼륨에 항상 NTFS 파일 시스템 사용</span><span class="sxs-lookup"><span data-stu-id="2651b-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="2651b-147">가장 안전한 구성의 경우 NTFS 파일 시스템을 사용 하도록 UE-V 설정 파일을 호스팅하는 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="2651b-148">FAT와 달리 NTFS는 Dacl (임의 액세스 제어 목록) 및 Sacl (시스템 액세스 제어 목록)을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="2651b-149">Dacl 및 Sacl은 파일에 대 한 작업을 수행할 수 있는 사용자와 파일에서 수행 되는 작업의 로깅을 트리거하는 이벤트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="2651b-150">네트워크를 통해 전송 되는 사용자의 파일을 암호화 하기 위해 EFS에 의존 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="2651b-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="2651b-151">EFS (파일 시스템 암호화)를 사용 하 여 원격 서버에서 파일을 암호화 하면 네트워크를 통해 전송 하는 동안 암호화 된 데이터가 암호화 되지 않습니다. 디스크에 저장 된 경우에만 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="2651b-152">예외는 시스템에 IPsec (인터넷 프로토콜 보안) 또는 WebDAV (웹 분산 작성 및 버전 관리)가 포함 된 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="2651b-153">IPsec은 TCP/IP 네트워크를 통해 전송 되는 동안 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="2651b-154">파일을 서버의 WebDAV 폴더로 복사 하거나 이동 하기 전에 암호화 한 경우에는 전송 중에 암호화 된 상태로 유지 되 고 서버에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="2651b-155">오프 라인 파일 캐시 암호화</span><span class="sxs-lookup"><span data-stu-id="2651b-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="2651b-156">기본적으로 오프 라인 파일 캐시는 Acl에의 한 NTFS 파티션에서 보호 되지만, 캐시 암호화는 로컬 컴퓨터의 보안을 더욱 강화 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="2651b-157">기본적으로 로컬 컴퓨터의 캐시는 암호화 되지 않으므로 네트워크에서 캐시 된 모든 암호화 된 파일은 로컬 컴퓨터에서 암호화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="2651b-158">이는 일부 환경에서 보안 위험을 초래할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="2651b-159">암호화를 사용 하도록 설정 하면 오프 라인 파일 캐시의 모든 파일이 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="2651b-160">여기에는 기존 파일 암호화 및 나중에 추가 되는 파일도 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="2651b-161">로컬 컴퓨터의 캐시 된 복사본에는 영향을 미치지만 연결 된 네트워크 복사본은 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="2651b-162">캐시는 다음 두 가지 방법 중 하나로 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="2651b-163">그룹 정책을 통해</span><span class="sxs-lookup"><span data-stu-id="2651b-163">Via Group Policy.</span></span> <span data-ttu-id="2651b-164">-그룹 정책 편집기에서 컴퓨터 Configuration\\Administrative Templates\\Network\\Offline 파일에 있는 **오프 라인 파일 캐시 암호화** 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="2651b-165">일일이.</span><span class="sxs-lookup"><span data-stu-id="2651b-165">Manually.</span></span> <span data-ttu-id="2651b-166">-Windows 탐색기의 명령 메뉴에서 도구를 선택한 다음 폴더 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="2651b-167">오프 라인 파일 탭을 선택한 다음 **데이터 보호를 위해 오프 라인 파일 암호화** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="2651b-168">UE-V Agent가 각 사용자에 대 한 폴더를 만들도록 허용</span><span class="sxs-lookup"><span data-stu-id="2651b-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="2651b-169">UE-V가 최적으로 작동 하도록 하려면 서버에서 루트 공유만 만들고 UE-V Agent가 각 사용자에 대 한 폴더를 만들도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="2651b-170">UE-V를 사용 하면 적절 한 보안으로 이러한 사용자 폴더가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="2651b-171">이 사용 권한 구성에서는 사용자가 설정 저장소에 대 한 폴더를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="2651b-172">UE-V agent는 사용자 컨텍스트에서 실행 되는 동안 settingspackage 폴더를 만들고 보안 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="2651b-173">사용자는 자신의 settingspackage 폴더에 대 한 모든 권한을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="2651b-174">다른 사용자는이 폴더에 대 한 액세스 권한을 상속 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="2651b-175">개별 사용자 디렉토리를 생성 하 고 보호할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="2651b-176">이 작업은 사용자 컨텍스트에서 실행 되는 에이전트에 의해 자동으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="2651b-177">참고</span><span class="sxs-lookup"><span data-stu-id="2651b-177">Note</span></span>**  
<span data-ttu-id="2651b-178">Windows server가 설정 저장소 공유에 사용 되는 경우 추가 보안을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="2651b-179">로컬 관리자의 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 하도록 UE-V를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="2651b-180">추가 보안을 사용 하도록 설정 하려면 다음 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="2651b-181">"RepositoryOwnerCheckEnabled" 이라는 REG \ _DWORD 레지스트리 키를에 추가 `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="2651b-182">레지스트리 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-182">Set registry key value to 1.</span></span>

<span data-ttu-id="2651b-183">이 구성 설정이 설정 되어 있으면 UE-V agent가 로컬 관리자의 그룹 또는 현재 사용자가 settingspackage 폴더의 소유자 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="2651b-184">그렇지 않으면 UE-V agent가 폴더에 대 한 액세스를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="2651b-185">사용자에 대 한 폴더를 만들어야 하는 경우 올바른 사용 권한이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="2651b-186">폴더를 precreate 하는 대신 UE-V agent가 사용자에 대 한 폴더를 만들 수 있도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="2651b-187">사용자의 홈 디렉터리에 UE-V 설정을 저장할 때 올바른 권한이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="2651b-188">사용자의 홈 디렉터리로 UE-V 설정을 리디렉션하면 사용자의 홈 디렉터리에 대 한 사용 권한이 조직에 맞게 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2651b-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="2651b-189">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2651b-189">Related topics</span></span>


[<span data-ttu-id="2651b-190">UE-V 1.0에 대한 보안 및 개인 정보</span><span class="sxs-lookup"><span data-stu-id="2651b-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









