---
title: 도메인 가입 및 도메인에 가입되지 않은 클라이언트
description: 도메인 가입 및 도메인에 가입되지 않은 클라이언트
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821633"
---
# 도메인 가입 및 도메인에 가입되지 않은 클라이언트


클라이언트가 도메인에 가입 되어 있는지 아니면 도메인이 연결 되지 않은 경우에 관계 없이 App-v 데스크톱 클라이언트를 구성 하 여 네트워크에 대 한 연결을 허용 하도록 할 수 있습니다.

## 도메인에 가입 된 클라이언트


도메인에 가입 되어 있지만 내부 네트워크 외부의 클라이언트는 VPN 연결을 사용 하 여 App-v 인프라와 통신할 수 있습니다. 사용자에 게 내부 네트워크를 유지 하지만 App-v 인프라에서 통신할 수 있는 능력을 제공 하려는 경우 환경에는 거의 설정이 필요 합니다. 사용자가 이미 도메인에 속해 있기 때문에 클라이언트에서 캐시 된 자격 증명을 지원 하는지 확인 하기만 하면 됩니다. 이는 기본 구성 이며,이 설정에 대 한 변경 내용은 그룹 정책에서 수행할 수 있습니다.

App-v 보안 모범 사례 가이드에 언급 된 대로 사용자는 인증을 위해 사용자 티켓을 App-v 인프라에 보내려고 시도 합니다. 티켓이 만료 된 경우에는 컴퓨터에서 NTLM 및 캐시 된 자격 증명을 사용 하 여 되돌립니다. 로밍을 허용 하려면 관리자가 내부적으로 액세스 되는 게시 서버를 이름 외부에서 사용할 수 있는지 확인 하 여 이름이 올바르게 확인 되도록 해야 합니다.

## 비도메인 가입 클라이언트


도메인에 가입 되어 있지 않지만 app-v 인프라에서 통신 해야 하는 클라이언트는 App-v 인프라에 대 한 인증이 성공적으로 수행 되도록 구성 되어야 합니다. App-v 데스크톱 클라이언트는 게시 새로 고침 프로세스에 대 한 메시지를 허용 하지 않으므로 해당 자격 증명을 App-v 관리 서버에 표시 하도록 클라이언트를 구성 해야 합니다.

비도메인 가입 클라이언트에서 새로 고침을 게시 하도록 구성 된 게시 서버는 클라이언트가 액세스 하는 외부 이름이 게시 서버의 인증서에 대 한 일반 이름 또는 SAN (주체 대체 이름)으로 구성 되어야 합니다.

## 관련 항목


[Windows Vista에 적합 한 자격 증명을 할당 하는 방법](how-to-assign--the-proper-credentials-for-windows-vista.md)

[Windows XP에 적합 한 자격 증명을 할당 하는 방법](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





