---
title: 전자 소프트웨어 배포 시스템을 통해 MED-V 작업 영역을 배포하는 방법
description: 전자 소프트웨어 배포 시스템을 통해 MED-V 작업 영역을 배포하는 방법
author: dansimp
ms.assetid: b5134c35-e1de-470c-93f8-ead6218d9dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56d21b0c2f010f63c04056d9fadd7763531bd9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812993"
---
# 전자 소프트웨어 배포 시스템을 통해 MED-V 작업 영역을 배포하는 방법


전자 소프트웨어 배포 시스템은 속도가 느리거나 빠른 네트워크 연결을 통해 다양 한 컴퓨터로 소프트웨어를 효율적으로 이동 하도록 설계 되었습니다. 다음 섹션에서는 소프트웨어 배포 시스템을 사용 하 여 엔터프라이즈 전체에 MED-V 작업 영역을 배포 하는 데 도움이 되는 정보와 지침을 제공 합니다.

**참고**  
사용 하는 소프트웨어 배포 솔루션에 따라 특정 솔루션의 요구 사항에 대해 잘 알고 있어야 합니다. System Center Configuration Manager 2007 R2 이상 버전을 사용 하는 경우 Microsoft 기술 라이브러리 ()의 [Configuration Manager 문서 라이브러리](https://go.microsoft.com/fwlink/?LinkId=66999) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=66999) .



**중요**  
System Center Configuration Manager 2007 SP2를 사용 하 고 있으며 MED-V 작업 영역이 **NAT** 모드에서 작동 하도록 구성 된 경우 가상 컴퓨터는 인터넷 기반 클라이언트로 분류 되며 콘텐츠를 다운로드할 가장 가까운 배포 지점을 찾을 수 없습니다.

MED-V에서 관리 되는 [vm에 대 한 기능을 개선 하는 핫픽스](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) med-v에서 관리 하 고 **NAT** 모드에서 작동 하도록 구성 된 가상 컴퓨터에는 새 기능을 추가 합니다.) 새로운 기능을 통해 가상 머신은 가장 가까운 배포 지점에 액세스할 수 있습니다. 따라서 관리자는 동일한 방식으로 가상 컴퓨터와 호스트 컴퓨터를 관리할 수 있습니다. 이 핫픽스는 사이트 서버, 그리고 클라이언트에 먼저 설치 해야 합니다.

업데이트를 공개적으로 사용할 수 있습니다. 그러나 Microsoft 서비스에 대 한 계약을 수락 하 라는 메시지가 표시 될 수 있습니다. 후속 웹 페이지의 메시지에 따라이 핫픽스를 검색 합니다.



배치 파일을 사용 하 여 MED-V 구성 요소를 함께 배포할 수도 있지만, 이렇게 하려면 Windows 가상 PC를 설치한 후 다시 시작 해야 합니다. 이 요구 사항을 무시 하기 위해 모든 구성 요소를 설치한 후 단일 다시 시작을 지정할 수 있습니다. MED-V 작업 영역 설치가 RUNKEY에 항목을 배치 하기 때문에 단일 다시 시작 또한 MED-V가 자동으로 시작 됩니다.

**소프트웨어 배포 시스템을 사용 하 여 MED-V 작업 영역을 배포 하려면**

1.  전자 소프트웨어 배포 시스템의 컴퓨터 및 사용자 그룹을 컴퓨터/사용자의 대상 집합으로 정의 합니다.

2.  배포 해야 하는 각 Microsoft 설치 파일에 대 한 패키지를 만듭니다. 다음은 필수 파일 및 설치 해야 하는 순서입니다.

    1.  **Windows 가상 PC** – 아직 설치 되지 않은 경우 (컴퓨터를 다시 시작 해야 함). 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    2.  **Windows 가상 PC 추가 및 업데이트** -아직 설치 되지 않은 경우 자세한 내용은 [설치 필수 구성 요소 구성을](configure-installation-prerequisites.md)참조 하세요.

    3.  **Med-v 호스트 에이전트 설치 파일** – 호스트 에이전트 (Med-v-v _HostAgent \ _Setup 설치 파일)를 설치 합니다. 자세한 내용은 [Med-v 호스트 에이전트를 수동으로 설치 하는 방법을](how-to-manually-install-the-med-v-host-agent.md)참조 하세요.

        **Warning**  
        MED-V 호스트 에이전트를 설치 하기 전에 Internet Explorer를 닫은 경우 나중에 URL 리디렉션으로 충돌이 발생할 수 있습니다. 배포 중에 컴퓨터 다시 시작을 지정 하 여이 작업을 수행할 수도 있습니다.



    4.  Med-v 작업 **영역 설치 관리자, VHD, 설치 실행 파일** – **Med-v 작업 영역 포장기**에서 생성 됩니다. 자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.

        **중요**  
        압축 된 가상 하드 디스크 파일 (.sdv) 및 설치 실행 프로그램 (setup.exe)이 MED-V 작업 영역 설치 관리자와 같은 폴더에 있어야 합니다. 그런 다음 setup.exe를 실행 하 여 MED-V 작업 영역 설치 관리자를 설치 합니다.



~~~
    **Tip**  
    Because problems can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



3. 패키지를 자동 모드로 실행 하도록 구성 합니다 (사용자 조작이 필요 없음).

   자동 모드로 실행 하면 Internet Explorer가 실행 중이면 닫을 것인지 묻는 메시지가 표시 되 고 MED-V 호스트 에이전트를 시작 하 라는 메시지가 표시 됩니다. 두 작업은 모두 컴퓨터를 다시 시작할 때 수행 됩니다.

   **참고**  
   Windows 가상 PC를 설치 하려면 컴퓨터를 다시 시작 해야 합니다. 다시 시작을 억제 하 고 MED-V에 설치 하는 데 필요한 필수 구성 요소를 무시 하는 경우 단일 설치 프로세스를 만들고 모든 구성 요소를 동시에 설치할 수 있습니다. 명령줄 인수를 사용 하 여이 작업을 수행할 수도 있습니다. 이러한 인수의 예는 [전자 소프트웨어 배포 시스템을 통해 Med-v 구성 요소를 배포 하는 방법을](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md#bkmk-batch)참조 하세요. 컴퓨터를 다시 시작 하면 MED-V가 자동으로 시작 됩니다.



4. Windows 가상 PC를 설치 하기 전에 MED-V와 해당 구성 요소를 설치 합니다. 이 항목의 뒷부분에 나오는 일괄 처리 파일 예제를 참조 하세요.

   **중요**  
   필수 VPC 구성 요소 보다 먼저 MED-V 구성 요소를 설치할 수 있도록 예제 배치 파일에 나와 있는 것 처럼 **무시 \ _PREREQUISITES** 옵션을 선택 합니다. 단일 다시 시작을 허용 하려면이 순서로 MED-V 구성 요소를 설치 합니다.



5. 설치에 필요한 기타 요구 사항과 대상 플랫폼, 빈 디스크 공간 등의 소프트웨어 배포 시스템을 식별 합니다.

6. 패키지를 컴퓨터/사용자의 대상 집합에 할당 합니다.

   컴퓨터가 실행 되 면 소프트웨어 배포 시스템 클라이언트에서 새 패키지를 사용할 수 있음을 인식 하 고 정의 및 요구 사항에 따라 패키지를 설치 하기 시작 합니다. 설치는 자동으로 연속적으로 실행 되어야 합니다. 모든 패키지가 설치 될 때까지 다시 시작 하지 않아도 되는 단일 프로세스로이 작업을 수행 하는 것이 좋습니다.

7. 설치가 완료 되 면 업데이트 된 컴퓨터를 다시 시작 합니다.

   소프트웨어 배포 시스템에 따라 컴퓨터를 다시 시작 하도록 예약 하거나, 최종 사용자가 일반 작업 중에 수동으로 컴퓨터를 다시 시작할 수 있습니다. 컴퓨터가 다시 시작 되 면 최종 사용자가 로그온 한 후에 MED-V가 자동으로 시작 됩니다. MED-V가 처음 시작 되 면 설치 프로그램이 처음으로 실행 됩니다.

처음 설치를 시작할 때 지정한 가상 하드 디스크의 크기와 시작 시 MED-V 작업 영역에 적용 된 정책의 수에 따라 완료 하는 데 몇 분 정도 걸릴 수 있습니다. 최종 사용자는 알림 영역에서 MED-V 아이콘을 시청 하 여 진행률을 추적할 수 있습니다. 처음 설정 하는 방법에 대 한 자세한 내용은 [med-v 2.0 배포 개요](med-v-20-deployment-overview.md)를 참조 하세요.

**배치 파일을 사용 하 여 MED-V 작업 영역을 설치 하려면**

1.  관리 자격 증명을 사용 하 여 명령 프롬프트에서 설치를 실행 합니다.

2.  각 구성 요소를 단일 디렉터리에 배포 합니다. 네트워크 공유에서 실행 하는 경우에는. a i a dv 파일의 압축을 푸는 데 시간이 더 걸립니다.

3.  가장 좋은 방법은 MED-V 호스트 에이전트 및 MED-V 작업 영역 패키지 파일을 설치한 후 Windows 가상 PC 및 Windows 가상 PC 핫픽스가 설치 되도록 지정 하는 것입니다. 즉, Windows Update는 다시 시작을 요구 하 여 설치 프로세스에 간섭이 발생 하지 않습니다.

4.  일괄 처리 파일이 완료 된 후 컴퓨터를 다시 시작 합니다.

다시 시작 하면 사용자에 게 처음 설정 하 고 MED-V의 구성을 완료 하 라는 메시지가 표시 됩니다.

다음 예제에서는 지정 된 인수를 사용 하 여 단일 프로세스로 64 비트 MED-V 구성 요소를 설치 하는 방법을 보여 줍니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">인수</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/norestart</p></td>
<td align="left"><p>Windows Virtual PC 및 Windows 가상 PC 업데이트 설치가 호스트 컴퓨터를 다시 시작 하지 않도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/quiet</p></td>
<td align="left"><p>사용자 조작 없이 자동 모드로 MED-V 구성 요소를 설치 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/qn</p></td>
<td align="left"><p>사용자 인터페이스 없이 MED-V 구성 요소를 설치 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IGNORE_PREREQUISITES</p></td>
<td align="left"><p>Windows 가상 PC를 확인 하지 않고 설치 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 설치의 일부로 Windows 가상 PC를 설치 하는 경우에만이 인수를 지정 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>OVERWRITEVHD</p></td>
<td align="left"><p>MED-V 작업 영역을 강제로 설치 하 고 생성 될 수 있는 모든 메시지를 방지 합니다.</p></td>
</tr>
</tbody>
</table>



## 예제


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## 관련 항목


[MED-V 2.0 배포 개요](med-v-20-deployment-overview.md)

[Windows 7 이미지에서 MED-V 작업 영역을 배포하는 방법](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)









