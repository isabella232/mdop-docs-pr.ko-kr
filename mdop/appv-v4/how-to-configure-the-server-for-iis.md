---
title: IIS용 서버를 구성하는 방법
description: IIS용 서버를 구성하는 방법
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817743"
---
# <span data-ttu-id="2f6a3-103">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="2f6a3-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="2f6a3-104">가상 응용 프로그램을 응용 프로그램 가상화 데스크톱 클라이언트로 스트림 하 고 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 클라이언트로 스트림할 수 있으려면 먼저 IIS 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="2f6a3-105">서버를 구성할 때 SFT 파일이 로드 되 고 저장 되는 콘텐츠 디렉터리를 설정 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="2f6a3-106">SFT 파일에는 가상 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="2f6a3-107">IIS 서버에서 콘텐츠 디렉터리를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="2f6a3-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="2f6a3-108">IIS를 실행 하는 서버에서 콘텐츠 디렉터리로 사용할 디렉터리를 찾거나 디렉터리가 없는 경우 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="2f6a3-109">이 디렉터리를 표준 파일 공유로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="2f6a3-110">IIS를 실행 하는 서버에서 **Iis 관리자**를 열고 기본 웹 사이트에서 서버에서 만든 콘텐츠 디렉터리에 해당 하는 가상 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="2f6a3-111">**읽기가** 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="2f6a3-112">새로 만든 가상 디렉터리에 별칭 **콘텐츠**를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="2f6a3-113">이 가상 디렉터리의 다른 모든 기본 설정을 그대로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="2f6a3-114">이전에 정의한 Active Directory 도메인 서비스의 보안 그룹을 사용 하 여 콘텐츠 디렉터리 아래의 콘텐츠 디렉터리와 패키지 폴더에 대 한 NTFS 파일 시스템 사용 권한을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="2f6a3-115">**참고**  IIS를 사용 하 여 .ICO 및 OSD 파일을 게시 하는 경우 OSD = TXT에 대 한 MIME 형식을 구성 해야 합니다. 그렇지 않으면 IIS는 .ICO 및 OSD 파일을 클라이언트에 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="2f6a3-116">IIS를 사용 하 여 패키지 (SFT 파일)를 게시 하는 경우 SFT = Binary에 대 한 MIME 형식을 구성 해야 합니다. 그렇지 않으면 IIS가 클라이언트에 SFT 파일을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f6a3-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="2f6a3-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2f6a3-117">Related topics</span></span>


[<span data-ttu-id="2f6a3-118">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="2f6a3-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="2f6a3-119">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="2f6a3-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="2f6a3-120">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="2f6a3-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="2f6a3-121">Application Virtualization Streaming Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="2f6a3-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="2f6a3-122">파일 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="2f6a3-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





