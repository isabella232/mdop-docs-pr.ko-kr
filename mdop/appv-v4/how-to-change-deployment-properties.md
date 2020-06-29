---
title: 배포 속성을 변경하는 방법
description: 배포 속성을 변경하는 방법
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818063"
---
# <span data-ttu-id="79d63-103">배포 속성을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="79d63-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="79d63-104">다음 절차를 사용 하 여 응용 프로그램 가상화 서버 URL, 가상화 된 응용 프로그램에 필요한 운영 체제, 설치할 가상 응용 프로그램의 출력 옵션을 비롯 하 여 시퀀싱 하는 응용 프로그램에 대 한 **배포** 탭 정보를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="79d63-105">서버 URL을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="79d63-105">To change the server URL</span></span>**

1.  <span data-ttu-id="79d63-106">드롭다운 목록 상자에서 스트리밍 프로토콜을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="79d63-107">가상 응용 프로그램 서버 또는 서버 그룹의 부하 분산 장치의 호스트 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="79d63-108">실제 호스트 이름 또는 IP 주소를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="79d63-109">가상 응용 프로그램 서버 또는 부하 분산이 스트리밍된 응용 프로그램에 대 한 Application Virtualization 데스크톱 클라이언트 요청을 수신 대기 하는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="79d63-110">소프트웨어 패키지가 저장 되는 가상 응용 프로그램 서버의 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="79d63-111">응용 프로그램 운영 체제 요구 사항을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="79d63-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="79d63-112">필요한 운영 체제를 추가 하려면 **사용 가능한** 목록에서 해당 시스템을 선택 하 고 화살표 단추를 클릭 하 여 **선택한** 운영 체제 목록 컨트롤을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="79d63-113">운영 체제를 제거 하려면 **선택한** 목록 컨트롤에서 시스템을 선택 하 고 화살표 단추를 클릭 하 여 **사용 가능한** 운영 체제 목록 컨트롤을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="79d63-114">응용 프로그램 출력 옵션을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="79d63-114">To change the application output options</span></span>**

1.  <span data-ttu-id="79d63-115">**압축 알고리즘** 드롭다운 목록에서 응용 프로그램을 스트리밍할 때 사용할 압축 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="79d63-116">패키지 된 응용 프로그램의 보안 설명자를 배포할 때 적용 하려면 **보안 설명자 적용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="79d63-117">**차이점 파일 생성** 을 선택 하 여 이전 시퀀싱 된 버전의 응용 프로그램에 대 한 차이점 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="79d63-118">설치 프로그램 패키지를 만들려면 **Microsoft Windows Installer (MSI) 패키지 생성** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d63-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="79d63-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="79d63-119">Related topics</span></span>


[<span data-ttu-id="79d63-120">배포 탭 정보</span><span class="sxs-lookup"><span data-stu-id="79d63-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="79d63-121">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="79d63-121">Sequencer Console</span></span>](sequencer-console.md)

 

 





