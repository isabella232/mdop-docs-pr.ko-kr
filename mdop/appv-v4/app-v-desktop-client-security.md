---
title: App-V 데스크톱 클라이언트 보안
description: App-V 데스크톱 클라이언트 보안
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822318"
---
# <span data-ttu-id="57cbc-103">App-V 데스크톱 클라이언트 보안</span><span class="sxs-lookup"><span data-stu-id="57cbc-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="57cbc-104">App-v 데스크톱 클라이언트는 이전 버전의 제품에서는 사용할 수 없었던 다양 한 보안 향상 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="57cbc-105">이러한 변경 사항은 기본적으로 높은 수준의 보안을 제공 하 고 클라이언트 설정 구성을 통해 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="57cbc-106">**참고**  컴퓨터에 App-v 데스크톱 클라이언트를 설치 하면 기본적으로 가장 안전한 설정이 소프트웨어에 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="57cbc-107">그러나 업그레이드할 때는 클라이언트의 이전 설정이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="57cbc-108">기본적으로 App-v 데스크톱 클라이언트는 비관리자 사용자가 게시 새로 고침 및 스트림 응용 프로그램을 수행 하도록 허용 하는 데 필요한 사용 권한 으로만 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="57cbc-109">App-v 데스크톱 클라이언트에 제공 되는 추가 보안 향상 기능에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="57cbc-110">기본적으로 OSD 캐시 업데이트는 게시 새로 고침 프로세스 에서만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="57cbc-111">로그 파일 ( `sftlog.txt` )은 클라이언트에 대 한 로컬 관리 액세스 권한이 있는 계정 으로만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="57cbc-112">이제 로그 파일의 크기가 최대입니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="57cbc-113">로그 파일은 보관 설정을 통해 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="57cbc-114">이제 시스템 이벤트 로깅이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="57cbc-115">사용 권한</span><span class="sxs-lookup"><span data-stu-id="57cbc-115">Permissions</span></span>


<span data-ttu-id="57cbc-116">데스크톱 클라이언트를 설치한 후에는 MMC 또는 Microsoft에서 제공 하는 ADM 서식 파일을 사용 하 여 개별 클라이언트에서 다른 보안 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="57cbc-117">App-v 데스크톱 클라이언트는 관리자가 아닌 사용자가 데스크톱 클라이언트의 모든 기능에 액세스 하지 못하도록 제한 하도록 설정할 수 있는 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="57cbc-118">전체 사용 권한 목록은 App-v 클라이언트 도움말 파일 또는 App-v 운영 가이드를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57cbc-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="57cbc-119">**중요**  특히 터미널 서버와 같이 여러 사용자가 공유 하는 시스템에서 액세스 권한 변경의 결과를 신중 하 게 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="57cbc-120">**참고**  환경의 사용자에 게 해당 컴퓨터에 대 한 로컬 관리자 권한이 있는 경우 해당 사용 권한은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="57cbc-121">ADM 템플릿</span><span class="sxs-lookup"><span data-stu-id="57cbc-121">ADM Template</span></span>

<span data-ttu-id="57cbc-122">Microsoft App-v (Application Virtualization)는 그룹 정책을 통해 가장 일반적인 클라이언트 설정을 구성 하는 데 사용할 수 있는 ADM 템플릿을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="57cbc-123">관리자는이 템플릿을 사용 하 여 중앙 관리 모델을 통해 다양 한 클라이언트 설정을 구현 하 고 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="57cbc-124">ADM 템플릿에서 사용할 수 있는 설정 중 일부는 보안 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="57cbc-125">**중요**  ADM 템플릿을 사용 하는 경우 설정이 그룹 정책 기본 설정 이며 완전히 관리 되는 그룹 정책이 아니라는 것을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="57cbc-126">ADM 서식 파일에 대 한 자세한 설명과 환경에서 클라이언트를 성공적으로 배포 하기 위한 지침에 대해서는의 App-v ADM 서식 파일 백서를 참조 하세요 [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="57cbc-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="57cbc-127">OSD 파일 형식 연결 제거</span><span class="sxs-lookup"><span data-stu-id="57cbc-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="57cbc-128">조직에서 사용자가 OSD 파일에서 직접 응용 프로그램을 열 필요가 없는 경우 클라이언트에서 파일 형식 연결을 제거 하 여 보안을 강화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="57cbc-129">`HKEY_CURRENT_USERS`OSD 및 `Softgird.osd.file` 레지스트리 편집기를 사용 하 여 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="57cbc-130">이 프로세스를 로그온 스크립트 또는 사후 설치 스크립트에 넣어 변경 하는 것을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57cbc-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





