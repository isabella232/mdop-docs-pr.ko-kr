---
title: 사용자 권한을 구성하는 방법
description: 사용자 권한을 구성하는 방법
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817733"
---
# <span data-ttu-id="4a170-103">사용자 권한을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="4a170-103">How to Configure User Permissions</span></span>


<span data-ttu-id="4a170-104">**권한** 레지스트리 키 (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions) 아래의 키 값을 편집 하 여 관리 권한이 없는 사용자에 대 한 일부 작업을 사용 하도록 설정 하거나 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a170-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="4a170-105">이 키는 관리자 권한이 있는 사용자가 이러한 키 값을 편집할 수 있기 때문에 특별 한 보안을 제공 하는 것이 아니라 사용자가 실수를 하지 않도록 하는 데 주로 사용 되는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4a170-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="4a170-106">다음 절차에서는 키 값을 변경 하는 방법의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a170-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="4a170-107">App-v (Application Virtualization) 클라이언트 레지스트리 키 및 값에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=121528> 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a170-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="4a170-108">사용자 권한을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="4a170-108">To change user permissions</span></span>**

1.  <span data-ttu-id="4a170-109">사용자가 오프 라인 모드에서 클라이언트를 실행 하도록 선택할 수 있도록 하려면 다음 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a170-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="4a170-110">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="4a170-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="4a170-111">사용자가 사용자 인터페이스를 통해 모든 응용 프로그램을 볼 수 있도록 하려면 다음 키 값을 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a170-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="4a170-112">값을 0으로 설정 하면 사용자가 사용할 수 있는 응용 프로그램만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a170-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="4a170-113">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="4a170-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="4a170-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4a170-114">Related topics</span></span>


[<span data-ttu-id="4a170-115">명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="4a170-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="4a170-116">Application Virtualization Client의 사용자 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="4a170-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





