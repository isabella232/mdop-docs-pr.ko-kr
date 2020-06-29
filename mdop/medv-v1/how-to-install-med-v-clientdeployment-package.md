---
title: MED-V 클라이언트를 설치하는 방법
description: MED-V 클라이언트를 설치하는 방법
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827193"
---
# <span data-ttu-id="75926-103">MED-V 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="75926-103">How to Install MED-V Client</span></span>


<span data-ttu-id="75926-104">배포 패키지 기반 시나리오에서 MED-V 클라이언트 설치는 배포 패키지에 포함 되어 패키지에서 직접 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75926-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="75926-105">중요</span><span class="sxs-lookup"><span data-stu-id="75926-105">Important</span></span>**  
<span data-ttu-id="75926-106">이미지를 포함 하지 않는 배포 패키지를 사용 하는 경우 배포 패키지를 설치 하기 전에 이미지를 웹에 업로드 하거나 미리 스테이지 폴더로 푸시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="75926-107">배포 패키지를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="75926-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="75926-108">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-108">Do one of the following:</span></span>

    -   <span data-ttu-id="75926-109">웹에서 MED-V 패키지를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="75926-110">배포 USB 또는 DVD를 호스트 드라이브에 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="75926-111">MED-V가 자동으로 실행 되지 않는 경우 MED-VAutoInstaller.exe를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="75926-112">이미 설치 된 구성 요소와 현재 설치 되 고 있는 항목을 나열 하는 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75926-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="75926-113">참고</span><span class="sxs-lookup"><span data-stu-id="75926-113">Note</span></span>**  
    <span data-ttu-id="75926-114">지원 되지 않는 Microsoft 가상 PC 버전이 호스트 컴퓨터에 있는 경우 기존 버전을 제거 하 고 설치 관리자를 다시 실행 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75926-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="75926-115">필요한 경우 컴퓨터를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="75926-116">설치가 완료 되 면 MED-V가 시작 되 고 설치가 완료 되었음을 알리는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75926-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="75926-117">다음 사용자 이름 및 암호를 사용 하 여 MED-V에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="75926-118">도메인 이름 및 사용자 이름 뒤에 MED-V와 함께 작업할 수 있는 도메인 사용자의 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="75926-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="75926-119">예: "domain \ _name \\user\ _name", "password"</span><span class="sxs-lookup"><span data-stu-id="75926-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="75926-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="75926-120">Related topics</span></span>


[<span data-ttu-id="75926-121">배포 패키지를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="75926-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="75926-122">서버에 MED-V 이미지를 업로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="75926-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="75926-123">클라이언트 설치 명령줄 참조</span><span class="sxs-lookup"><span data-stu-id="75926-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)









