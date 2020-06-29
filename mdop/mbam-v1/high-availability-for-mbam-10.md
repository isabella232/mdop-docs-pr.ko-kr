---
title: MBAM 1.0에 대한 고가용성
description: MBAM 1.0에 대한 고가용성
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825363"
---
# <span data-ttu-id="f43af-103">MBAM 1.0에 대한 고가용성</span><span class="sxs-lookup"><span data-stu-id="f43af-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="f43af-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM)의 고가용성 설치를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="f43af-105">MBAM에 대 한 고가용성 시나리오</span><span class="sxs-lookup"><span data-stu-id="f43af-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="f43af-106">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 결함을 허용 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="f43af-107">서버를 사용할 수 없게 되 면 사용자는 부정적인 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="f43af-108">예를 들어 MBAM 에이전트를 MBAM 웹 서버에 연결할 수 없는 경우 사용자에 게 작업을 묻는 메시지가 표시 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="f43af-109">MBAM 설치를 계획 하는 경우 MBAM 서비스의 사용 가능성에 영향을 줄 수 있는 다음 관심사를 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="f43af-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="f43af-110">드라이브 암호화 및 복구 암호-복구 암호를 escrowed 수 없는 경우 클라이언트 컴퓨터에서 암호화가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="f43af-111">준수 상태 데이터 업로드 – 준수 상태 보고서 서비스를 호스팅하는 서버를 사용할 수 없는 경우 준수 데이터는 현재 상태로 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="f43af-112">지원 센터 복구 키 액세스-지원 센터에서 MBAM 데이터베이스 정보에 액세스할 수 없는 경우에는 사용자에 게 복구 키를 제공할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="f43af-113">보고서의 가용성 – 준수 및 감사 보고서를 호스팅하는 서버를 사용할 수 없는 경우 보고서를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="f43af-114">MBAM의 고가용성에 대 한 주요 관심사는 BitLocker 키 복구 가용성입니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="f43af-115">지원 센터에서 복구 키를 제공할 수 없는 경우 잠긴 사용자는 컴퓨터의 잠금을 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="f43af-116">이 문제를 방지 하려면 고가용성을 보장 하기 위해 중복 웹 서버 및 데이터베이스를 구현 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f43af-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="f43af-117">MBAM 확장성 및 고가용성에 대 한 자세한 내용은 [Mbam 확장성 백서](https://go.microsoft.com/fwlink/p/?LinkId=229025) ()를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="f43af-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="f43af-118">Microsoft SQL Server의 고가용성에 대 한 일반적인 지침은 [고가용성 (()을 참조](https://go.microsoft.com/fwlink/p/?LinkId=221504) 하세요 https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="f43af-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="f43af-119">웹 서버의 가용성 및 확장성에 대 한 일반적인 지침은 [가용성 및 확장성](https://go.microsoft.com/fwlink/p/?LinkId=221503) (()을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="f43af-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="f43af-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f43af-120">Related topics</span></span>


[<span data-ttu-id="f43af-121">MBAM 1.0 유지 관리</span><span class="sxs-lookup"><span data-stu-id="f43af-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 





