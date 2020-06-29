---
title: AGPM 서비스를 수신할 포트 수정
description: AGPM 서비스를 수신할 포트 수정
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820488"
---
# <span data-ttu-id="543e1-103">AGPM 서비스를 수신할 포트 수정</span><span class="sxs-lookup"><span data-stu-id="543e1-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="543e1-104">AGPM 서비스는 보관 및 프로덕션 환경의 Gpo (그룹 정책 개체)에 대 한 클라이언트 액세스를 관리 하는 보안 프록시 역할을 하는 Windows 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="543e1-105">기본적으로 AGPM 서비스는 포트 4600에서 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="543e1-106">각 아카이브의 용 AGPM (고급 그룹 정책 관리) 보관 인덱스 파일을 수정 하 여이 포트를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="543e1-107">**참고**  AGPM 서비스가 수신 대기 하는 포트를 수정 하기 전에, AGPM 보관 인덱스 파일 (gpostate.xml)을 백업 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="543e1-108">이 파일은 고급 그룹 정책 관리-서버를 설치 하는 동안 보관 경로로 입력 된 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="543e1-109">기본적으로이 파일의이 위치는 AGPM 서버의% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml입니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="543e1-110">보관 파일을 호스트 하는 컴퓨터를 모르는 경우 보관 경로를 수정 하는 절차에 따라 현재 보관 경로를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="543e1-111">자세한 내용은 [보관 경로 수정을](modify-the-archive-path.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="543e1-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="543e1-112">이 절차를 완료 하려면 AGPM 서버 (AGPM 서비스가 설치 되어 있는 컴퓨터)에 대 한 액세스 권한이 있는 사용자 계정이 고 보관 인덱스 파일을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="543e1-113">AGPM 서비스가 수신 대기 하는 포트를 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="543e1-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="543e1-114">보관 파일을 호스트 하는 컴퓨터에서 텍스트 편집기에 보관 인덱스 파일 (gpostate.xml)을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="543e1-115">파일에서 **agpm: port = "4600"** 를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="543e1-116">**4600** 를 AGPM 서비스가 수신 대기할 포트로 바꿉니다. 그런 다음 파일을 저장 하 고 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="543e1-117">AGPM 서버에서 AGPM 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="543e1-118">(자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service.md)를 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="543e1-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="543e1-119">각 그룹 정책 관리자에 대해 AGPM 서버 연결의 포트를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="543e1-120">(자세한 내용은 [AGPM 서버 연결 구성을](configure-the-agpm-server-connection.md)참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="543e1-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="543e1-121">각 보관 및 AGPM 서버에 대해 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="543e1-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="543e1-122">추가 참조</span><span class="sxs-lookup"><span data-stu-id="543e1-122">Additional references</span></span>

-   [<span data-ttu-id="543e1-123">AGPM 서비스 관리</span><span class="sxs-lookup"><span data-stu-id="543e1-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





