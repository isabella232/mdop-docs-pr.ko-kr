---
title: UE-V 2.x에 대한 보안 고려 사항
description: UE-V 2.x에 대한 보안 고려 사항
author: dansimp
ms.assetid: 9d5c3cae-9fcb-4dea-bd67-741b3dea63be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8e24e9e37de11053663bb90974fabf2ff369aeca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824663"
---
# <span data-ttu-id="53d2e-103">UE-V 2.x에 대한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="53d2e-103">Security Considerations for UE-V 2.x</span></span>


<span data-ttu-id="53d2e-104">이 항목에는 Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1에 대 한 계정 및 그룹, 로그 파일 및 기타 보안 관련 고려 사항에 대 한 간략 한 개요가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1.</span></span> <span data-ttu-id="53d2e-105">자세한 내용은 여기에 나와 있는 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53d2e-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="53d2e-106">UE-V 구성에 대 한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="53d2e-106">Security considerations for UE-V configuration</span></span>


<span data-ttu-id="53d2e-107">**중요**  설정 저장소 공유를 만들 때 액세스 권한이 필요한 사용자에 대 한 공유 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-107">**Important** When you create the settings storage share, limit the share access to users who require access.</span></span>

 

<span data-ttu-id="53d2e-108">설정 패키지에는 개인 정보가 포함 될 수 있기 때문에 가능한 한 안전 하 게 보호 하는 데 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-108">Because settings packages might contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="53d2e-109">일반적으로 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-109">In general, do the following:</span></span>

-   <span data-ttu-id="53d2e-110">액세스 권한이 필요한 사용자 만으로 공유를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-110">Restrict the share to only those users who require access.</span></span> <span data-ttu-id="53d2e-111">특정 공유에서 폴더를 리디렉션하고 해당 사용자 에게만 액세스를 제한 하는 사용자에 대 한 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-111">Create a security group for users who have redirected folders on a particular share and limit access to only those users.</span></span>

-   <span data-ttu-id="53d2e-112">공유를 만들 때 공유 이름 뒤에 $를 추가 하 여 공유를 숨깁니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="53d2e-113">이 추가 기능은 일반 브라우저에서 공유를 숨기 며, 네트워크 위치에 공유가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-113">This addition hides the share from casual browsers, and the share is not visible in My Network Places.</span></span>

-   <span data-ttu-id="53d2e-114">사용자에 게 필요한 최소 사용 권한만 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-114">Only give users the minimum amount of permissions that they must have.</span></span> <span data-ttu-id="53d2e-115">다음 표에서는 필수 권한을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-115">The following tables show the required permissions.</span></span>

    1.  <span data-ttu-id="53d2e-116">설정 저장소 위치 폴더에 대해 다음과 같은 공유 수준 SMB 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-116">Set the following share-level SMB permissions for the setting storage location folder.</span></span>

        | <span data-ttu-id="53d2e-117">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="53d2e-117">User account</span></span> | <span data-ttu-id="53d2e-118">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-118">Recommended permissions</span></span> |
        | - | - |
        | <span data-ttu-id="53d2e-119">모두</span><span class="sxs-lookup"><span data-stu-id="53d2e-119">Everyone</span></span> | <span data-ttu-id="53d2e-120">권한 없음</span><span class="sxs-lookup"><span data-stu-id="53d2e-120">No permissions</span></span> |
        |<span data-ttu-id="53d2e-121">UE-V의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="53d2e-121">Security group of UE-V</span></span> | <span data-ttu-id="53d2e-122">모든 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-122">Full control</span></span> |

    2.  <span data-ttu-id="53d2e-123">설정 저장소 위치 폴더에 대해 다음 NTFS 파일 시스템 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-123">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        | <span data-ttu-id="53d2e-124">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="53d2e-124">User account</span></span> | <span data-ttu-id="53d2e-125">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-125">Recommended permissions</span></span> | <span data-ttu-id="53d2e-126">Folder</span><span class="sxs-lookup"><span data-stu-id="53d2e-126">Folder</span></span> |
        | - | - | - |
        | <span data-ttu-id="53d2e-127">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="53d2e-127">Creator/Owner</span></span> | <span data-ttu-id="53d2e-128">모든 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-128">Full control</span></span> | <span data-ttu-id="53d2e-129">하위 폴더 및 파일만</span><span class="sxs-lookup"><span data-stu-id="53d2e-129">Subfolders and files only</span></span>|
        | <span data-ttu-id="53d2e-130">도메인 관리자</span><span class="sxs-lookup"><span data-stu-id="53d2e-130">Domain Admins</span></span> | <span data-ttu-id="53d2e-131">모든 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-131">Full control</span></span> | <span data-ttu-id="53d2e-132">다음 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="53d2e-132">This folder, subfolders, and files</span></span> |
        | <span data-ttu-id="53d2e-133">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="53d2e-133">Security group of UE-V users</span></span> | <span data-ttu-id="53d2e-134">폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</span><span class="sxs-lookup"><span data-stu-id="53d2e-134">List folder/read data, create folders/append data</span></span> | <span data-ttu-id="53d2e-135">이 폴더만</span><span class="sxs-lookup"><span data-stu-id="53d2e-135">This folder only</span></span> |
        | <span data-ttu-id="53d2e-136">모두</span><span class="sxs-lookup"><span data-stu-id="53d2e-136">Everyone</span></span> | <span data-ttu-id="53d2e-137">모든 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="53d2e-137">Remove all permissions</span></span> | <span data-ttu-id="53d2e-138">권한 없음</span><span class="sxs-lookup"><span data-stu-id="53d2e-138">No permissions</span></span> |

    3.  <span data-ttu-id="53d2e-139">설정 템플릿 카탈로그 폴더에 대해 다음과 같은 공유 수준 SMB 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-139">Set the following share-level SMB permissions for the settings template catalog folder.</span></span>

        | <span data-ttu-id="53d2e-140">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="53d2e-140">User account</span></span> | <span data-ttu-id="53d2e-141">권장 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-141">Recommend permissions</span></span> |
        | - | - |
        | <span data-ttu-id="53d2e-142">모두</span><span class="sxs-lookup"><span data-stu-id="53d2e-142">Everyone</span></span> | <span data-ttu-id="53d2e-143">권한 없음</span><span class="sxs-lookup"><span data-stu-id="53d2e-143">No permissions</span></span> |
        | <span data-ttu-id="53d2e-144">도메인 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="53d2e-144">Domain computers</span></span> | <span data-ttu-id="53d2e-145">읽기 사용 권한 수준</span><span class="sxs-lookup"><span data-stu-id="53d2e-145">Read permission Levels</span></span> |
        | <span data-ttu-id="53d2e-146">관리자</span><span class="sxs-lookup"><span data-stu-id="53d2e-146">Administrators</span></span> | <span data-ttu-id="53d2e-147">읽기/쓰기 권한 수준</span><span class="sxs-lookup"><span data-stu-id="53d2e-147">Read/write permission levels</span></span> |
         
    4.  <span data-ttu-id="53d2e-148">설정 서식 파일 카탈로그 폴더에 대해 다음 NTFS 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-148">Set the following NTFS permissions for the settings template catalog folder.</span></span>

        | <span data-ttu-id="53d2e-149">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="53d2e-149">User account</span></span> | <span data-ttu-id="53d2e-150">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-150">Recommended permissions</span></span> | <span data-ttu-id="53d2e-151">적용 대상</span><span class="sxs-lookup"><span data-stu-id="53d2e-151">Apply to</span></span> |
        | - | - | - |
        | <span data-ttu-id="53d2e-152">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="53d2e-152">Creator/Owner</span></span> | <span data-ttu-id="53d2e-153">모든 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-153">Full control</span></span> | <span data-ttu-id="53d2e-154">다음 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="53d2e-154">This folder, subfolders, and files</span></span> |
        | <span data-ttu-id="53d2e-155">도메인 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="53d2e-155">Domain Computers</span></span> | <span data-ttu-id="53d2e-156">폴더 내용 목록 및 사용 권한 읽기</span><span class="sxs-lookup"><span data-stu-id="53d2e-156">List folder contents and Read permissions</span></span> | <span data-ttu-id="53d2e-157">다음 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="53d2e-157">This folder, subfolders, and files</span></span>|
        | <span data-ttu-id="53d2e-158">모두</span><span class="sxs-lookup"><span data-stu-id="53d2e-158">Everyone</span></span>| <span data-ttu-id="53d2e-159">권한 없음</span><span class="sxs-lookup"><span data-stu-id="53d2e-159">No permissions</span></span>| <span data-ttu-id="53d2e-160">권한 없음</span><span class="sxs-lookup"><span data-stu-id="53d2e-160">No permissions</span></span>|
        | <span data-ttu-id="53d2e-161">관리자</span><span class="sxs-lookup"><span data-stu-id="53d2e-161">Administrators</span></span>| <span data-ttu-id="53d2e-162">모든 권한</span><span class="sxs-lookup"><span data-stu-id="53d2e-162">Full Control</span></span>| <span data-ttu-id="53d2e-163">다음 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="53d2e-163">This folder, subfolders, and files</span></span>|

### <span data-ttu-id="53d2e-164">WindowsServer2003로 WindowsServer를 사용 하 여 리디렉션 파일 공유 호스팅</span><span class="sxs-lookup"><span data-stu-id="53d2e-164">Use WindowsServer as of WindowsServer2003 to host redirected file shares</span></span>

<span data-ttu-id="53d2e-165">사용자 설정 패키지 파일에는 클라이언트 컴퓨터와 설정 패키지를 저장 하는 서버 간에 전송 되는 개인 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-165">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="53d2e-166">이 프로세스 때문에 데이터는 네트워크를 통해 이동 하는 동안 보호 되는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-166">Because of this process, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="53d2e-167">사용자 설정 데이터는 네트워크를 통해 전달 되는 데이터 가로채기, 네트워크를 통해 전달 되는 데이터 훼손, 데이터를 호스팅하는 서버의 스푸핑 등의 잠재적인 위협에 취약해 집니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-167">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network, tampering with the data as it passes over the network, and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="53d2e-168">Windows Server2003에서 Windows Server 운영 체제의 여러 기능을 통해 사용자 데이터를 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-168">As of Windows Server2003, several features of the Windows Server operating system can help secure user data:</span></span>

-   <span data-ttu-id="53d2e-169">**Kerberos** -Kerberos는 WindowsServer2003로 시작 하는 Microsoft Windows2000Server 및 windowsserver의 모든 버전에 대 한 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-169">**Kerberos** - Kerberos is standard on all versions of Microsoft Windows2000Server and WindowsServer beginning with WindowsServer2003.</span></span> <span data-ttu-id="53d2e-170">Kerberos는 네트워크 리소스에 가장 높은 수준의 보안을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-170">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="53d2e-171">NTLM은 클라이언트만 인증 합니다. Kerberos는 서버와 클라이언트를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-171">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="53d2e-172">NTLM을 사용 하는 경우 클라이언트는 서버가 유효한 지 여부를 알지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-172">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="53d2e-173">이 차이점은 사용자 로밍 프로필의 경우와 마찬가지로 클라이언트가 서버와 개인 파일을 교환 하는 경우 특히 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-173">This difference is particularly important if the client exchanges personal files with the server, as is the case with Roaming User Profiles.</span></span> <span data-ttu-id="53d2e-174">Kerberos는 NTLM 보다 더 나은 보안을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-174">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="53d2e-175">Microsoft WindowsNTServer 4.0 또는 이전 버전의 운영 체제에서는 Kerberos를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-175">Kerberos is not available on the Microsoft WindowsNTServer 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="53d2e-176">**Ipsec** -IP 보안 프로토콜 (ipsec)은 네트워크 수준 인증, 데이터 무결성 및 암호화를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-176">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="53d2e-177">IPsec은 다음을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-177">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="53d2e-178">Roamed 데이터는 데이터가 회람 되는 동안 데이터를 수정 하는 것이 안전 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-178">Roamed data is safe from data modification while data is en route.</span></span>

    -   <span data-ttu-id="53d2e-179">Roamed 데이터는 가로채기, 보기 또는 복사에서 안전 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-179">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="53d2e-180">Roamed 데이터는 인증 되지 않은 사람이 액세스 하는 것을 안전 하 게 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-180">Roamed data is safe from access by unauthenticated parties.</span></span>

-   <span data-ttu-id="53d2e-181">**Smb 서명** -Smb (서버 메시지 블록) 인증 프로토콜은 활성 메시지와 "중간자" 공격을 차단 하는 메시지 인증을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-181">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication, which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="53d2e-182">SMB 서명은 각 SMB에 디지털 서명을 배치 하 여이 인증을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-182">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="53d2e-183">그러면 클라이언트와 서버에서 디지털 서명을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-183">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="53d2e-184">SMB 서명을 사용 하려면 먼저 사용 하도록 설정 하거나 SMB 클라이언트와 SMB 서버 모두에서 요구 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-184">In order to use SMB signing, you must first either enable it, or you must require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="53d2e-185">SMB 서명은 성능 저하를 부과 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-185">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="53d2e-186">네트워크 대역폭을 더 이상 사용 하지 않지만 클라이언트 및 서버 쪽에서 더 많은 CPU 주기를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-186">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="53d2e-187">항상 사용자 데이터를 보유 하는 볼륨에 NTFS 파일 시스템 사용</span><span class="sxs-lookup"><span data-stu-id="53d2e-187">Always use the NTFS file system for volumes that hold user data</span></span>

<span data-ttu-id="53d2e-188">가장 안전한 구성의 경우 NTFS 파일 시스템을 사용 하도록 UE-V 설정 파일을 호스팅하는 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-188">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS file system.</span></span> <span data-ttu-id="53d2e-189">FAT 파일 시스템과 달리 NTFS는 Dacl (임의 액세스 제어 목록) 및 Sacl (시스템 액세스 제어 목록)을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-189">Unlike the FAT file system, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="53d2e-190">Dacl 및 Sacl은 파일에 대 한 작업을 수행할 수 있는 사용자와 파일에서 수행 되는 작업에 대 한 로깅을 트리거하는 이벤트를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-190">DACLs and SACLs control who can perform operations on a file and what events trigger the logging of actions that is performed on a file.</span></span>

### <span data-ttu-id="53d2e-191">네트워크를 통해 전송 되는 사용자 파일을 암호화 하는 데 EFS에 의존 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="53d2e-191">Do not rely on EFS to encrypt user files when they are transmitted over the network</span></span>

<span data-ttu-id="53d2e-192">EFS (파일 시스템 암호화)를 사용 하 여 원격 서버에서 파일을 암호화할 때 암호화 된 데이터는 네트워크를 통해 전송 되는 동안 암호화 되지 않습니다. 디스크에 저장 된 경우에만 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-192">When you use the Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; it only becomes encrypted when it is stored on disk.</span></span>

<span data-ttu-id="53d2e-193">시스템에 IPsec (인터넷 프로토콜 보안) 또는 WebDAV (웹 분산 작성 및 버전 관리)가 포함 된 경우에는이 암호화 프로세스가 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-193">This encryption process does not apply when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="53d2e-194">IPsec은 TCP/IP 네트워크를 통해 전송 되는 동안 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-194">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="53d2e-195">파일을 암호화 하 여 서버의 WebDAV 폴더로 복사 하거나 이동 하면 전송 중에는 암호화 된 상태로 유지 되 고 서버에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-195">If the file is encrypted before it is copied or moved to a WebDAV folder on a server, it remains encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="53d2e-196">UE-V Agent가 각 사용자에 대 한 폴더를 만들도록 허용</span><span class="sxs-lookup"><span data-stu-id="53d2e-196">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="53d2e-197">UE-V가 최적으로 작동 하도록 하려면 서버에서 루트 공유만 만들고 UE-V Agent가 각 사용자에 대 한 폴더를 만들도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-197">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="53d2e-198">UE-V를 사용 하면 적절 한 보안으로 이러한 사용자 폴더가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-198">UE-V creates these user folders with the appropriate security.</span></span>

<span data-ttu-id="53d2e-199">이 사용 권한 구성에서는 사용자가 설정 저장소에 대 한 폴더를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-199">This permission configuration enables users to create folders for settings storage.</span></span> <span data-ttu-id="53d2e-200">UE-V Agent는 사용자 컨텍스트에서 실행 되는 동안 설정 패키지 폴더를 만들고 보안 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-200">The UE-V Agent creates and secures a settings package folder while it runs in the context of the user.</span></span> <span data-ttu-id="53d2e-201">사용자가 설정 패키지 폴더에 대 한 모든 권한을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-201">Users receive full control to their settings package folder.</span></span> <span data-ttu-id="53d2e-202">다른 사용자는이 폴더에 대 한 액세스 권한을 상속 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-202">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="53d2e-203">개별 사용자 디렉토리를 생성 하 고 보호할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-203">You do not have to create and secure individual user directories.</span></span> <span data-ttu-id="53d2e-204">사용자 컨텍스트에서 실행 되는 에이전트는 자동으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-204">The agent that runs in the context of the user does it automatically.</span></span>

<span data-ttu-id="53d2e-205">**참고**  Windows Server가 설정 저장소 공유에 사용 되는 경우 추가 보안을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-205">**Note** Additional security can be configured when a Windows Server is used for the settings storage share.</span></span> <span data-ttu-id="53d2e-206">UE-V를 구성 하 여 로컬 관리자 그룹 또는 현재 사용자가 설정 패키지를 저장 한 폴더의 소유자 인지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-206">UE-V can be configured to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="53d2e-207">추가 보안을 사용 하도록 설정 하려면 다음 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-207">To enable additional security, use the following command:</span></span>

1.  <span data-ttu-id="53d2e-208">REG \ _DWORD 레지스트리 키 RepositoryOwnerCheckEnabled를에 추가 `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-208">Add the REG\_DWORD registry key RepositoryOwnerCheckEnabled to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="53d2e-209">레지스트리 키 값을 *1*로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-209">Set the registry key value to *1*.</span></span>

<span data-ttu-id="53d2e-210">이 구성 설정이 설정 되어 있으면 UE-V Agent가 로컬 관리자 그룹 또는 현재 사용자가 설정 패키지 폴더의 소유자 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-210">When this configuration setting is in place, the UE-V Agent verifies that the local Administrators group or current user is the owner of the settings package folder.</span></span> <span data-ttu-id="53d2e-211">그렇지 않으면 UE-V Agent가 폴더에 대 한 액세스 권한을 부여 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-211">If not, then the UE-V Agent does not grant access to the folder.</span></span>

 

<span data-ttu-id="53d2e-212">사용자에 대 한 폴더를 만들어야 하는 경우 올바른 사용 권한이 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-212">If you must create folders for the users, ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="53d2e-213">폴더를 미리 만들지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-213">We strongly recommend that you do not pre-create folders.</span></span> <span data-ttu-id="53d2e-214">대신, UE-V Agent가 사용자에 대 한 폴더를 만들도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-214">Instead, let the UE-V Agent create the folder for the user.</span></span>

### <span data-ttu-id="53d2e-215">Home directory 또는 사용자 지정 디렉터리에 UE-V 2 설정을 저장 하는 올바른 권한이 있는지 확인</span><span class="sxs-lookup"><span data-stu-id="53d2e-215">Ensure correct permissions to store UE-V 2 settings in a home directory or custom directory</span></span>

<span data-ttu-id="53d2e-216">사용자의 홈 디렉터리 또는 사용자 지정 Active Directory (AD) 디렉터리로 UE-V 설정을 리디렉션하면 해당 디렉터리에 대 한 사용 권한이 조직에 맞게 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="53d2e-216">If you redirect UE-V settings to a user’s home directory or a custom Active Directory (AD) directory, ensure that the permissions on the directory are set appropriately for your organization.</span></span>






## <span data-ttu-id="53d2e-217">관련 항목</span><span class="sxs-lookup"><span data-stu-id="53d2e-217">Related topics</span></span>


[<span data-ttu-id="53d2e-218">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="53d2e-218">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





