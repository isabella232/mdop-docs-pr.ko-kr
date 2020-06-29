---
title: 클러스터 모드용 MED-V 서버 구성
description: 클러스터 모드용 MED-V 서버 구성
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826718"
---
# <span data-ttu-id="217dc-103">클러스터 모드용 MED-V 서버 구성</span><span class="sxs-lookup"><span data-stu-id="217dc-103">Configuring MED-V Server for Cluster Mode</span></span>


<span data-ttu-id="217dc-104">클러스터 모드에서 MED-V 서버를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-104">You can configure the MED-V server in cluster mode.</span></span> <span data-ttu-id="217dc-105">클러스터 모드에서는 두 개의 서버가 사용 되 고 두 서버 모두에 대해 상호 종속으로 식별 된 모든 파일이 파일 시스템에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-105">In cluster mode, two servers are used and all files identified as mutual to both servers are placed on a file system.</span></span> <span data-ttu-id="217dc-106">서버는 파일을 로컬로 저장 하는 대신 파일 시스템에서 파일에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-106">The server accesses the files from the file system rather than storing the files locally.</span></span>

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**<span data-ttu-id="217dc-107">클러스터 모드에서 MED-V 서버를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="217dc-107">To configure the MED-V server in cluster mode</span></span>**

1.  <span data-ttu-id="217dc-108">서버 중 하나에 MED-V를 설치 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-108">Install and configure MED-V on one of the servers.</span></span>

2.  <span data-ttu-id="217dc-109">모든 서버에서 액세스할 수 있는 중앙 위치에서 공유 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-109">Create a shared network in a central location where all of the servers can access it.</span></span>

3.  <span data-ttu-id="217dc-110">\* &lt; InstallDir &gt; /Servers/ConfigurationServer\* 폴더의 콘텐츠를 공유 네트워크에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-110">Copy the contents of the *&lt;InstallDir&gt;/Servers/ConfigurationServer* folder to the shared network.</span></span>

4.  <span data-ttu-id="217dc-111">지정 된 모든 서버에 MED-V 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-111">Install MED-V server on all designated servers.</span></span>

5.  <span data-ttu-id="217dc-112">공유 네트워크에서 모든 MED-V 서버 시스템 계정에 대 한 모든 액세스 권한을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-112">On the shared network, assign full access to all MED-V server system accounts.</span></span>

6.  <span data-ttu-id="217dc-113">각 서버에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-113">On each server, do the following:</span></span>

    1.  <span data-ttu-id="217dc-114">\* &lt; InstallDir &gt; /Servers/ServerConfiguration.xml\* 파일에서 \* &lt; storepath &gt; \* 의 값을 공유 네트워크 경로로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-114">In the *&lt;InstallDir&gt;/Servers/ServerConfiguration.xml* file, set the value of *&lt;StorePath&gt;* to the shared network path.</span></span>

    2.  <span data-ttu-id="217dc-115">원본 서버에서 모든 MED-V 서버로 \* &lt; 명령이 있는 salldir &gt; /Servers/KeyPair.xml\* 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-115">Copy the *&lt;InstsallDir&gt;/Servers/KeyPair.xml* file from the original server to all MED-V servers.</span></span>

    3.  <span data-ttu-id="217dc-116">MED-V 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-116">Restart the MED-V service.</span></span>

<span data-ttu-id="217dc-117">**참고**  모든 서버에 동일한 로컬 설정 (예: 수신 포트, IIS 서버, 관리 권한, 보고서 데이터베이스 등)이 있는 경우 \* &lt; InstallDir &gt; /Servers/ServerSettings.xml\* 모든 서버 에서도 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="217dc-117">**Note** If all servers have the same local settings (such as listening ports, IIS server, management permissions, report database, and so on), the *&lt;InstallDir&gt;/Servers/ServerSettings.xml* can be shared by all servers as well.</span></span>

 

## <span data-ttu-id="217dc-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="217dc-118">Related topics</span></span>


[<span data-ttu-id="217dc-119">MED-V 인프라 계획 및 디자인</span><span class="sxs-lookup"><span data-stu-id="217dc-119">MED-V Infrastructure Planning and Design</span></span>](med-v-infrastructure-planning-and-design.md)

 

 





