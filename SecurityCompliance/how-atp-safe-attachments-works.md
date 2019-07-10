---
title: Office 365 ATP 안전 첨부 파일의 작동 방식
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: 안전한 첨부 파일 기능은 전자 메일 첨부 파일을 클릭 하 여 확인할 시간을 제공 합니다. 안전한 첨부 파일을 사용 하 여 사용자가 전자 메일로 보내거나 받는 악의적인 파일 로부터 조직을 보호 합니다.
ms.openlocfilehash: f0f117388957a14e3765b963a0e390ffb8fd7943
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599174"
---
# <a name="how-ffice-365-atp-safe-attachments-works"></a>Ffice> 365 ATP에서 안전한 첨부 파일의 작동 방식

## <a name="how-it-works"></a>작업 방법

ATP 안전한 첨부 파일 기능은 조직의 사용자에 대해 전자 메일 첨부 파일을 확인 합니다. ATP 안전한 첨부 파일 정책이 적용 되 고 해당 정책에서 다루는 누군가가 Office 365의 전자 메일을 볼 때, 해당 전자 메일 첨부 파일을 확인 하 고 ATP 안전한 첨부 파일 정책에 따라 적절 한 조치를 취할 수 있습니다. 정책이 정의 된 방식에 따라 사용자가 악성 파일을 보낸 것을 알지 못하면 작업을 계속할 수 있습니다.
  
다음은 직장의 ATP 안전 첨부 파일에 대 한 두 가지 예입니다.
  
- **예 1: 전자 메일 첨부 파일** Lee에서 첨부 파일이 있는 전자 메일 메시지를 수신 한다고 가정 합니다. 해당 첨부 파일이 안전한 지 아니면 실제로 Lee의 사용자 자격 증명을 도용 하도록 설계 된 맬웨어가 있는지를 Lee는 것은 분명 하지 않습니다. Lee의 조직에서는 보안 관리자가 ATP 안전한 첨부 파일 정책을 며칠 전에 정의 했습니다. ATP 안전한 첨부 파일 기능을 사용 하 여 Lee가 수신 되기 전에 전자 메일 첨부 파일을 가상 환경에서 열고 테스트 합니다. 첨부 파일이 악성 인 것으로 확인 되 면 자동으로 제거 됩니다. 안전 하지 않은 첨부 파일은 Lee 클릭 하면 예상 대로 열립니다.

- **예 2: SharePoint Online의 파일** Jean에서 파일을 받아 SharePoint Online의 라이브러리에 업로드 했다고 가정 합니다. Jean는 파일에 대 한 링크를 나머지 팀과 공유 하 여 실제로 악성 프로그램 인지를 알지 못합니다. 다행 스럽게도 [SharePoint, OneDrive 및 Microsoft 팀](atp-for-spo-odb-and-teams.md) 은 악성 파일을 검색 하 고 차단 합니다. 며칠 후에 Chris가 문서를 엽니다. Chris가 파일을 볼 수는 있지만, chris의 컴퓨터와 악의 있는 파일을 보호 하는 공유를 열거나 공유할 수 없습니다.

ATP 안전한 첨부 파일 정책은 조직의 특정 사용자 또는 그룹이 나 전체 도메인에 적용할 수 있습니다. 또한 ATP 안전한 첨부 파일 정책은 실제 첨부 파일을 검색 하는 동안 자리 표시자 첨부 파일을 사용 하도록 구성할 수 있습니다. 자세한 내용은 **[Office 365에서 ATP 안전한 첨부 파일 정책 설정을](set-up-atp-safe-attachments-policies.md)** 참조 하십시오.

> [!NOTE]
> ATP 안전한 첨부 파일 검사는 Office 365 데이터가 있는 동일한 지역에서 발생 합니다. 데이터 센터 지역에 대 한 자세한 내용은 [어디에 있습니까?](https://products.office.com/where-is-your-data-located?geo=All) 를 참조 하세요. 

