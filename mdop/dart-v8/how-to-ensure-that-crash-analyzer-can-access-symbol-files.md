---
title: 크래시 분석기가 기호 파일에 액세스할 수 있도록 하는 방법
description: 크래시 분석기가 기호 파일에 액세스할 수 있도록 하는 방법
author: dansimp
ms.assetid: 99839013-1cd8-44d1-8484-0e15261c5a4b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 944198b95528a548acbe1229f9f3aad4c224af29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821228"
---
# <span data-ttu-id="70d1e-103">크래시 분석기가 기호 파일에 액세스할 수 있도록 하는 방법</span><span class="sxs-lookup"><span data-stu-id="70d1e-103">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>


<span data-ttu-id="70d1e-104">일반적으로 디버깅 정보는 프로그램과는 별도의 기호 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-104">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="70d1e-105">응답을 중지 한 응용 프로그램을 디버깅할 때는 기호 정보에 대 한 액세스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-105">You must have access to the symbol information when you debug an application that has stopped responding.</span></span>

<span data-ttu-id="70d1e-106">심볼 파일은 **충돌 분석기**를 실행할 때 자동으로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-106">Symbol files are automatically downloaded when you run **Crash Analyzer**.</span></span> <span data-ttu-id="70d1e-107">컴퓨터에 인터넷 연결이 없거나 네트워크에 설치 되어 있는 컴퓨터에서 HTTP 프록시 서버에 액세스 해야 하는 경우 기호 파일을 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-107">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

**<span data-ttu-id="70d1e-108">충돌 분석기가 기호 파일에 액세스할 수 있도록 하려면</span><span class="sxs-lookup"><span data-stu-id="70d1e-108">To ensure that Crash Analyzer can access symbol files</span></span>**

1.  **<span data-ttu-id="70d1e-109">덤프 파일을 다른 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-109">Copy the dump file to another computer.</span></span>** <span data-ttu-id="70d1e-110">인터넷 연결이 부족 하 여 기호를 다운로드할 수 없는 경우에는 메모리 덤프 파일을 인터넷에 연결 되어 있는 컴퓨터로 복사 하 고 해당 컴퓨터에서 독립 실행형 **충돌 분석기 마법사** 를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-110">If the symbols cannot be downloaded because of a lack of an Internet connection, copy the memory dump file to a computer that does have an Internet connection and run the stand-alone **Crash Analyzer Wizard** on that computer.</span></span>

2.  **<span data-ttu-id="70d1e-111">다른 컴퓨터에서 기호 파일에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-111">Access the symbol files from another computer.</span></span>** <span data-ttu-id="70d1e-112">인터넷 연결이 부족 하 여 기호를 다운로드할 수 없는 경우 인터넷에 연결 되어 있지 않은 컴퓨터에서 기호를 다운로드 한 다음 인터넷에 연결 되어 있지 않은 컴퓨터에 복사 하거나 네트워크 드라이브를 로컬 네트워크에서 기호를 사용할 수 있는 위치에 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-112">If the symbols cannot be downloaded because of a lack of an Internet connection, you can download the symbols from a computer that does have an Internet connection and then copy them to the computer that does not have an Internet connection, or you can map a network drive to a location where the symbols are available on the local network.</span></span> <span data-ttu-id="70d1e-113">Windows 복구 환경 (WindowsRE)에서 **충돌 분석기** 를 실행 하는 경우 Microsoft 진단 및 복구 도구 모음 (DaRT) 8.0 복구 이미지에 기호 파일을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-113">If you run the **Crash Analyzer** in a Windows Recovery Environment (WindowsRE), you can include the symbol files on the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

3.  **<span data-ttu-id="70d1e-114">HTTP 프록시 서버를 통해 기호 파일에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-114">Access symbol files through an HTTP proxy server.</span></span>** <span data-ttu-id="70d1e-115">HTTP 프록시 서버에 액세스 해야 하기 때문에 기호를 다운로드할 수 없는 경우 다음 단계를 사용 하 여 HTTP 프록시 서버에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-115">If the symbols cannot be downloaded because an HTTP proxy server must be accessed, use the following steps to access an HTTP proxy server.</span></span> <span data-ttu-id="70d1e-116">DaRT 8.0의 **충돌 분석기 마법사** 에는 레이블 프록시 서버로 표시 된 **기호 파일 위치 지정** 대화 페이지에서 사용할 수 있는 설정이 있습니다 **(선택 사항으로 "server: port" 형식 사용)**.</span><span class="sxs-lookup"><span data-stu-id="70d1e-116">In DaRT 8.0, the **Crash Analyzer Wizard** has a setting available on the **Specify Symbol Files Location** dialog page, marked with the label **Proxy server (optional, using the format "server:port")**.</span></span> <span data-ttu-id="70d1e-117">이 입력란을 사용 하 여 프록시 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-117">You can use this text box to specify a proxy server.</span></span> <span data-ttu-id="70d1e-118">호스트 이름이 DNS 이름 또는 IP 주소이 고 포트는 \*\* &lt; &gt; &lt; &gt; \*\* &lt; **hostname** &gt; &lt; **port** &gt; TCP 포트 번호 (일반적으로 80) 인 형식 호스트 이름: 포트에 프록시 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-118">Enter the proxy address in the form **&lt;hostname&gt;:&lt;port&gt;**, where the &lt;**hostname**&gt; is a DNS name or IP address, and the &lt;**port**&gt; is a TCP port number, usually 80.</span></span> <span data-ttu-id="70d1e-119">**충돌 분석기** 는 두 가지 모드를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-119">There are two modes in which the **Crash Analyzer** can be run.</span></span> <span data-ttu-id="70d1e-120">다음은 이러한 각 모드에서 프록시 설정을 사용 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-120">Following is how you use the proxy setting in each of these modes:</span></span>

    -   <span data-ttu-id="70d1e-121">**온라인 모드:** 이 모드에서 프록시 서버 필드를 비워 두면 마법사는 제어판의 인터넷 옵션에서 프록시 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-121">**Online mode:** In this mode, if the proxy server field is left blank, the wizard uses the proxy settings from Internet Options in Control Panel.</span></span> <span data-ttu-id="70d1e-122">제공 된 텍스트 상자에 프록시 주소를 입력 하면 해당 주소가 사용 되 고 인터넷 옵션의 설정이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-122">If you enter a proxy address in the text box which is provided, that address will be used, and it will override the setting in the Internet Options.</span></span>

    -   <span data-ttu-id="70d1e-123">Windows 복구 환경 (WindowsRE): **진단 및 복구 도구 집합** 창에서 **충돌 분석기** 를 실행 하는 경우 기본 프록시 주소가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-123">Windows Recovery Environment (WindowsRE): When you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window, there is no default proxy address.</span></span> <span data-ttu-id="70d1e-124">컴퓨터가 인터넷에 직접 연결 된 경우 프록시 주소는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-124">If the computer is directly connected to the Internet, a proxy address is not required.</span></span> <span data-ttu-id="70d1e-125">따라서 마법사 설정에서이 필드를 비워 둘 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-125">Therefore, you can leave this field blank in the wizard setting.</span></span> <span data-ttu-id="70d1e-126">컴퓨터가 인터넷에 직접 연결 되어 있지 않고 프록시 서버가 있는 네트워크 환경에 있는 경우 마법사에서 프록시 필드를 설정 하 여 기호 저장소에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-126">If the computer is not directly connected to the Internet, and it is in a network environment that has a proxy server, you must set the proxy field in the wizard to access the symbol store.</span></span> <span data-ttu-id="70d1e-127">프록시 주소는 네트워크 관리자 로부터 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-127">The proxy address can be obtained from the network administrator.</span></span> <span data-ttu-id="70d1e-128">프록시 서버 설정은 공용 기호 저장소가 인터넷에 연결 된 경우에만 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-128">Setting the proxy server is important only when the public symbol store is connected to the Internet.</span></span> <span data-ttu-id="70d1e-129">이미 DaRT 복구 이미지에 기호가 있거나 해당 기호를 로컬로 사용할 수 있는 경우 프록시 서버 설정이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70d1e-129">If the symbols are already on the DaRT recovery image, or if they are available locally, setting the proxy server is not required.</span></span>

## <span data-ttu-id="70d1e-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="70d1e-130">Related topics</span></span>


[<span data-ttu-id="70d1e-131">크래시 분석기를 사용하여 시스템 오류 진단</span><span class="sxs-lookup"><span data-stu-id="70d1e-131">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[<span data-ttu-id="70d1e-132">DaRT 8.0 작업</span><span class="sxs-lookup"><span data-stu-id="70d1e-132">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





