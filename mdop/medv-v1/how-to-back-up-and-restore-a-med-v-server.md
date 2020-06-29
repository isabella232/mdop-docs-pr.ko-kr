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
# <span data-ttu-id="972d4-103">MED-V 서버를 백업 및 복원하는 방법</span><span class="sxs-lookup"><span data-stu-id="972d4-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="972d4-104">서버에 있는 XML 파일을 백업 하 고 서버에 데이터가 손실 되는 경우 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="972d4-105">MED-V 서버를 백업 하려면</span><span class="sxs-lookup"><span data-stu-id="972d4-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="972d4-106">\* &lt; InstallDir &gt; \\Servers\\configurationserver\*에 있는 다음 파일을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="972d4-107">**참고**  구성이 기본값에서 변경 된 경우 파일이 다른 위치에 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="972d4-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="972d4-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="972d4-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="972d4-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="972d4-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="972d4-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="972d4-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="972d4-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="972d4-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="972d4-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="972d4-113">**참고**  또한 ServerSettings.xml 파일도 백업할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="972d4-114">그러나 특정 구성이 변경 된 경우 (예: 원본 서버에서 MED-V VM 디렉터리는 "*c:\\vms*"에 있으며 해당 디렉터리가 새 서버에 존재 하지 않는 경우) 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="972d4-115">MED-V 서버를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="972d4-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="972d4-116">새 MED-V 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="972d4-117">백업 파일을 다음 디렉터리에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="972d4-118">&lt;InstallDir &gt; \\Servers\\configurationserver</span><span class="sxs-lookup"><span data-stu-id="972d4-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="972d4-119">MED-V 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="972d4-119">Restart the MED-V service.</span></span>

 

 





