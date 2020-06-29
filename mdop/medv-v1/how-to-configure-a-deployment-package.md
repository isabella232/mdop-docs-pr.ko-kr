---
title: 배포 패키지를 구성하는 방법
description: 배포 패키지를 구성하는 방법
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825948"
---
# <span data-ttu-id="aed42-103">배포 패키지를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="aed42-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="aed42-104">패키징 마법사는 로컬 컴퓨터에 폴더를 만들고 필요한 모든 설치 파일을 단일 폴더로 전송 하 여 패키지를 만드는 과정을 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="aed42-105">그런 다음 폴더의 콘텐츠를 배포를 위해 여러 이동식 미디어 드라이브로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="aed42-106">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-106">Note</span></span>**  
<span data-ttu-id="aed42-107">단일 패키지는 x86 및 x64 시스템 모두에 대 한 설치 파일을 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="aed42-108">배포 패키지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="aed42-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="aed42-109">배포 패키지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="aed42-109">To create a deployment package</span></span>**

1. <span data-ttu-id="aed42-110">하나 이상의 로컬 압축 이미지를 만들었는지 **이미지** 모듈에서 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="aed42-111">**도구** 메뉴에서 **패키징 마법사**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="aed42-112">**패키징 마법사** 시작 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="aed42-113">**작업 영역 이미지** 페이지에서 패키지에 이미지 **포함 확인란을** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="aed42-114">**이미지** 필드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="aed42-115">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-115">Note</span></span>**  
   <span data-ttu-id="aed42-116">MED-V 패키지에는 이미지가 필요 하지 않습니다. 이미지 없이 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="aed42-117">이러한 경우 이미지를 서버에 업로드 하 여 나중에 네트워크를 통해 클라이언트에 다운로드 하거나 이미지 프리 스테이지 폴더로 푸시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="aed42-118">**이미지** 목록을 클릭 하 여 사용 가능한 모든 이미지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="aed42-119">패키지에 복사할 이미지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="aed42-120">**새로 고침** 을 클릭 하 여 사용 가능한 이미지 목록을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="aed42-121">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-121">Click **Next**.</span></span>

7. <span data-ttu-id="aed42-122">**Med-v 설치 설정** 페이지에서 다음 중 하나를 수행 하 여 med-v 설치 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="aed42-123">**Med-v 설치 파일** 필드에 설치 파일이 있는 디렉터리의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="aed42-124">설치 파일이 있는 디렉터리를 찾아보려면 **...** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="aed42-125">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-125">Note</span></span>**  
   <span data-ttu-id="aed42-126">이 필드는 필수 이며, 마법사가 올바른 파일 이름 없이 계속 진행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="aed42-127">**서버 주소** 필드에 서버 이름 또는 IP 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="aed42-128">**서버 포트** 필드에 서버 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="aed42-129">서버에 연결 하기 위해 https 연결이 필요한 경우 **https를 사용 하 여 서버에 액세스** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="aed42-130">다음 중 하나를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-130">Do one of the following:</span></span>

    -   <span data-ttu-id="aed42-131">**기본 설치 설정을**클릭 하 고 **다음** 을 클릭 하 여 계속 진행 하 고 기본 설정을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="aed42-132">**사용자 지정 설치 설정을**클릭 하 고 **다음** 을 클릭 하 여 설치 설정을 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="aed42-133">**Med-v 설치 사용자 지정 설정** 페이지의 **설치 폴더** 필드에 med-v 파일이 설치 될 호스트 컴퓨터의 폴더 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="aed42-134">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-134">Note</span></span>**  
            <span data-ttu-id="aed42-135">상수 대신 경로에 변수를 사용 하는 것이 좋으며,이는 컴퓨터 마다 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="aed42-136">예를 들어 *c:\\MED-V*대신 *%ProgramFiles%\\MED-V* 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="aed42-137">**추가 설치** 페이지에서 **가상화 소프트웨어 설치 포함** 확인란을 선택 하 여 패키지에 가상 PC 설치를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="aed42-138">**설치 파일** 필드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="aed42-139">가상화 소프트웨어 설치 파일의 전체 경로를 입력 하거나 **...** 를 클릭 하 여 디렉터리를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="aed42-140">가상 PC 업데이트 설치를 패키지에 포함 하려면 **가상 PC QFE 설치 포함** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="aed42-141">**설치 파일** 필드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="aed42-142">가상 PC 업데이트 설치 파일의 전체 경로를 입력 하거나 **...** 를 클릭 하 여 디렉터리를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="aed42-143">Microsoft .net framework 2.0 설치를 패키지에 포함 하려면 **microsoft .Net framework 설치 포함 2.0** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="aed42-144">**설치 파일** 필드를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="aed42-145">Microsoft .NET Framework 2.0 설치 파일의 전체 경로를 입력 하거나 **...** 를 클릭 하 여 디렉터리를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="aed42-146">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-146">Click **Next**.</span></span>

16. <span data-ttu-id="aed42-147">**마무리** 페이지에서 다음 중 하나를 실행 하 여 패키지를 저장할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="aed42-148">**패키지 대상** 필드에 패키지를 저장할 디렉터리의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="aed42-149">설치 파일을 저장 해야 하는 디렉터리를 찾아보려면 **...** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="aed42-150">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-150">Note</span></span>**  
    <span data-ttu-id="aed42-151">패키지를 빌드하면 실제 패키지 크기 보다 많은 공간이 소모 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="aed42-152">따라서 하드 드라이브에 패키지를 작성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="aed42-153">패키지를 만든 후에는 USB에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="aed42-154">**패키지 이름** 필드에 패키지의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="aed42-155">**마침을** 클릭 하 여 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="aed42-156">패키지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-156">The package is created.</span></span> <span data-ttu-id="aed42-157">이 작업은 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-157">This might take several minutes.</span></span>

    <span data-ttu-id="aed42-158">패키지를 만든 후에는 성공적으로 완료 되었음을 알리는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="aed42-159">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-159">Note</span></span>**  
<span data-ttu-id="aed42-160">이동식 미디어에 직접 모든 파일을 저장 한 경우 폴더 자체를 제외 하 고 폴더의 내용만 복사 하 여 이동식 미디어에 복사할 수 있도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="aed42-161">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-161">Note</span></span>**  
<span data-ttu-id="aed42-162">이동식 미디어는 패키지 내용이 이동식 미디어의 메모리 중 최대 3/4을 소모 하도록 충분히 커야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="aed42-163">참고</span><span class="sxs-lookup"><span data-stu-id="aed42-163">Note</span></span>**  
<span data-ttu-id="aed42-164">패키지를 만들 때 빌드가 완료 되 면 실제 패키지 크기의 크기를 두 배로 설정 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed42-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="aed42-165">관련 항목</span><span class="sxs-lookup"><span data-stu-id="aed42-165">Related topics</span></span>


[<span data-ttu-id="aed42-166">MED-V 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="aed42-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









