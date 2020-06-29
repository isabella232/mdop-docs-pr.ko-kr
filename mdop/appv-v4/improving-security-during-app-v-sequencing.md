---
title: App-V를 시퀀싱하는 동안 보안 향상
description: App-V를 시퀀싱하는 동안 보안 향상
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816358"
---
# <span data-ttu-id="e36e6-103">App-V를 시퀀싱하는 동안 보안 향상</span><span class="sxs-lookup"><span data-stu-id="e36e6-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="e36e6-104">시퀀싱을 위한 응용 프로그램 패키지는 App-v 인프라에서 가장 많이 진행 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="e36e6-105">이 작업은 진행 중 이므로 응용 프로그램을 시퀀싱 할 때 수행할 정책과 절차를 신중 하 게 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="e36e6-106">App-v 4.5에서는 시퀀싱 하는 동안 가상화 된 응용 프로그램의 파일 자산에 대 한 Acl (액세스 제어 목록)을 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="e36e6-107">Sequencer의 바이러스 검색</span><span class="sxs-lookup"><span data-stu-id="e36e6-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="e36e6-108">시퀀싱 컴퓨터에 스캔 소프트웨어를 설치 하 고 컴퓨터에서 바이러스와 맬웨어를 검색 하는 것이 가장 좋은 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="e36e6-109">시퀀싱 하는 컴퓨터를 검색 하 고 바이러스 또는 맬웨어를 해제 한 후에는 응용 프로그램을 시퀀싱 하기 전에 시퀀싱 하는 컴퓨터에서 모든 바이러스 백신 및 맬웨어 감지 소프트웨어를 포함 하 여 스캐닝 소프트웨어를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="e36e6-110">이렇게 하면 시퀀싱 프로세스가 속도를 향상 시킬 수 있으며 시퀀싱 하는 동안 스캔 소프트웨어 구성 요소가 검색 되지 않고 가상 응용 프로그램 패키지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="e36e6-111">파일의 Acl (NTFS) 캡처</span><span class="sxs-lookup"><span data-stu-id="e36e6-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="e36e6-112">시퀀서는 시퀀싱 설치 단계 중 모니터링 되는 파일에 대 한 NTFS 권한 (Acl)을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="e36e6-113">(App-v 4.5 릴리스 이전에는 시퀀싱 프로세스의 일부로 Acl을 캡처할 수 없었습니다.) 이 새로운 기능은 일반적으로 관리 권한이 필요한 낮은 수준의 권한을 가진 사용자를 위해 특정 응용 프로그램을 실행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="e36e6-114">이 기능을 사용 하면 시퀀싱 엔지니어가 공급 업체에서 식별 한 보안 설정을 캡처할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="e36e6-115">공급 업체에서 권장 하는 설정을 적용 하지 않으면 사용자가 응용 프로그램을 공격 또는 오용 하기 위해 열려 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="e36e6-116">개방형 Acl을 사용 하 여 응용 프로그램을 배포할지 여부에 대 한 자세한 내용은 응용 프로그램 지원 그룹 또는 소프트웨어 공급 업체를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e36e6-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="e36e6-117">**중요**  시퀀서는 시퀀싱의 설치 단계를 모니터링 하는 동안 NTFS Acl을 캡처 하지만 레지스트리에 대 한 Acl을 캡처하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="e36e6-118">사용자는 서비스를 제외 하 고 가상 응용 프로그램의 모든 레지스트리 키에 대 한 전체 액세스 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="e36e6-119">그러나 사용자가 가상 응용 프로그램의 레지스트리를 수정 하는 경우 해당 변경 내용이 특정 위치 ()에 저장 `uservol_sftfs_v1.pkg` 되며 다른 사용자에 게 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="e36e6-120">설치 단계에서 시퀀싱 엔지니어는 필요한 경우 파일의 기본 사용 권한을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="e36e6-121">시퀀싱 프로세스가 완료 된 후 패키지를 저장 하기 전에 시퀀싱 엔지니어가 설치 단계 중에 캡처한 보안 설명자를 적용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="e36e6-122">다른 솔루션을 사용 하는 경우 응용 프로그램을 가상화 한 번만 제대로 실행할 수 없는 경우 보안 설명자를 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e36e6-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





