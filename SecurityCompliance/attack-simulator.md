---
title: Office 365의 공격 시뮬레이터
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/05/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: Office 365 전역 관리자는 공격 시뮬레이터를 사용 하 여 조직에서 현실적인 공격 시나리오를 실행할 수 있습니다. 이를 통해 실질적인 공격이 비즈니스에 방문 하기 전에 취약 한 사용자를 식별 하 고 찾을 수 있습니다.
ms.openlocfilehash: e372fe3c4cc10c4f96836db394fbccd2f180145a
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693667"
---
# <a name="attack-simulator-in-office-365"></a>Office 365의 공격 시뮬레이터

**요약** office 365 전역 관리자이 고 조직에 [office 365 위협 조사 및 응답 기능이](office-365-ti.md)있으면 공격 시뮬레이터를 사용 하 여 조직에서 현실적인 공격 시나리오를 실행할 수 있습니다. 이를 통해 실질적인 공격이 아래 줄에 영향을 주는 이전에 취약 한 사용자를 식별 하 고 찾을 수 있습니다. 자세한 내용은이 문서를 참조 하세요.

> [!IMPORTANT]
> office 365 advanced threat protection 및 위협 조사 및 응답 (이전의 위협 인텔리전스)은 이제 추가 위협 방지 기능을 사용 하 여 Office 365 Advanced Threat protection 계획 2에 포함 되어 있습니다. 자세한 내용은 [office 365 advanced threat protection 요금제 및 가격](https://products.office.com/exchange/advance-threat-protection) 및 [office 365 advanced threat protection 서비스 설명을](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)참조 하세요.
  
## <a name="the-attacks"></a>공격

현재 다음과 같은 세 가지 유형의 공격 시뮬레이션이 제공 됩니다.
  
- [표시 이름 스피어-피싱 공격](attack-simulator.md#spearphish)
    
- [암호 분무 공격](attack-simulator.md#passwordspray)
    
- [무작위 암호 공격](attack-simulator.md#bruteforce)
    
공격이 정상적으로 시작 되려면 시뮬레이트된 공격을 실행 하는 데 사용 하는 계정에 multi-factor authentication을 사용 합니다. 또한 Office 365 전역 관리자 여야 합니다.
  
> [!NOTE]
> 조건부 액세스에 대 한 지원이 곧 제공 될 예정입니다. 
  
공격 시뮬레이터에 액세스 &amp; 하려면 보안 및 준수 센터에서 **위협 관리** \> **공격 시뮬레이터**를 선택 합니다.
  
## <a name="before-you-begin"></a>시작 하기 전에

사용자와 조직이 공격 시뮬레이터에 대해 다음 요구 사항을 충족 하는지 확인 합니다.
      
- **조직의 전자 메일이 Exchange Online에서 호스트 됩니다**. 온-프레미스 전자 메일 서버에는 Attack 시뮬레이터를 사용할 수 없습니다.
    
- **사용자는 Office 365 전역 관리자 여야 합니다.**
    
- **최소 Office 365 전역 관리자 계정에 대해 MFA ( [multi-factor authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide) )가 설정 됩니다**. 가장 이상적으로는 조직의 모든 사용자에 대해 MFA를 설정 하는 것이 좋습니다.
 
- **조직에 [Office 365 Advanced Threat Protection 계획 2](office-365-ti.md)가 있으며**, 보안 &amp; 및 준수 센터에서 공격 시뮬레이터가 표시 됩니다 ( **위협 관리** \> **공격 시뮬레이터**로 이동).<br/>![위협 관리-공격 시뮬레이터](media/ThreatMgmt-AttackSimulator.png)

    
## <a name="display-name-spear-phishing-attack"></a>표시 이름 스피어-피싱 공격

피싱은 사회 공학적 스타일 공격으로 classed 다양 한 공격 집합에 대 한 일반 용어입니다. 이 공격은 특정 개인 또는 조직 그룹을 목표로 하는 스피어 피싱에 중점을 두었습니다. 일반적으로 일부 정찰 자가 수행 하는 사용자 지정 된 공격과 받는 사람에 게 신뢰를 생성 하는 표시 이름 (예: 조직의 임원 으로부터 온 것 처럼 보이는 전자 메일 메시지)을 사용 합니다.
  
이 공격은 표시 이름과 원본 주소를 변경 하 여 메시지를 보낸 사람을 조작할 수 있는 방법을 중점적으로 설명 합니다. 스피어-피싱 공격이 성공 하면 cybercriminals에서 사용자 자격 증명에 액세스할 수 있습니다.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>스피어 피싱 공격을 시뮬레이션 하려면

![전자 메일 본문 작성](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
**전자 메일 본문** 필드 자체에서 서식 있는 html 편집기를 직접 만들거나 HTML 원본으로 작업할 수 있습니다.
  
1. [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **위협 관리** \> **공격 시뮬레이터**를 선택 합니다.
    
2. 공격에 대 한 의미 있는 캠페인 이름을 지정 하거나 서식 파일을 선택 합니다. <br/>![피싱 시작 페이지](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. 대상 받는 사람을 지정 합니다. 조직의 개인 또는 그룹이 될 수 있습니다. 공격이 성공 하려면 각 대상이 지정 된 받는 사람에 게 Exchange Online 사서함이 있어야 합니다. <br/>![받는 사람 선택](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. 피싱 메일 세부 정보를 구성 합니다. <br/>![전자 메일 세부 정보 구성](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/>HTML 서식 지정은 캠페인 요구 사항에 따라 복잡할 수도 있고 기본 형식이 될 수 있습니다. 전자 메일 형식이 HTML 인 것 처럼 이미지와 텍스트를 삽입 하 여 believability을 향상 시킬 수 있습니다. 수신 되는 전자 메일 클라이언트에서 받은 메시지의 모양을 제어할 수 있습니다.
    
5. **보낸 사람 (이름)** 필드에 대 한 텍스트를 지정 합니다. 받는 전자 메일 클라이언트의 **표시 이름** 에이 필드를 표시 합니다. 
    
6. 텍스트 또는 **보낸 사람** 필드를 지정 합니다. 받는 전자 메일 클라이언트에 있는 보낸 사람의 전자 메일 주소로 표시 되는 필드입니다. <br/>조직 내에서 기존 전자 메일 네임 스페이스를 입력할 수 있습니다 (이 작업을 수행 하면 전자 메일 주소가 받는 클라이언트에서 실제로 확인 되 고, 매우 높은 신뢰 모델이 촉진 됨), 외부 전자 메일 주소를 입력할 수 있습니다. 지정한 전자 메일 주소가 실제로 존재 하는 것은 아니지만, 유효한 SMTP 주소 형식 (예: user @ domainname. 확장명)을 사용 해야 합니다. 
  
7. 드롭다운 선택기를 사용 하 여 공격에 포함 될 콘텐츠 유형을 반영 하는 피싱 로그인 서버 URL을 선택 합니다. 문서 배달, 기술, 급여 등의 다양 한 테마가 지정 된 url을 선택할 수 있습니다. 이 URL은 대상 사용자가 클릭 하 라는 메시지가 표시 되는 경우 효과적입니다.
    
8. 사용자 지정 랜딩 페이지 URL을 지정 합니다. 이 방법을 사용 하면 사용자가 공격이 완료 되 면 지정한 URL로 리디렉션됩니다. 예를 들어 내부 인식 교육이 있는 경우 여기에서 지정할 수 있습니다.
    
9. **제목** 필드에 대 한 텍스트를 지정 합니다. 받는 전자 메일 클라이언트에서 **주체 이름** 으로 표시 되는 필드입니다. 
    
10. 대상이 받게 될 **전자 메일 본문** 을 구성 합니다. <br/>`${username}`전자 메일 본문에 대상 이름을 삽입 합니다. <br/>`${loginserverurl}`대상 사용자가 클릭 하도록 할 URL을 삽입 합니다. 
    
11. **다음을** 선택 하 고 **마침을** 클릭 하 여 공격을 시작 합니다. 스피어 피싱 전자 메일 메시지는 대상 받는 사람의 사서함으로 배달 됩니다. 
    
## <a name="password-spray-attack"></a>암호 분무 공격

조직에 대 한 암호 분무 공격은 잘못 된 행위자가 테 넌 트에서 유효한 사용자 목록을 성공적으로 가져온 후에 사용 됩니다. 잘못 된 행위자가 사용자 들이 사용 하는 일반적인 암호를 알고 있습니다. 이 공격은 많이 사용 되는 공격으로, 실행 하는 데 비용이 적게 드는 공격이 며 무작위 접근 방식 보다 감지 하기가 더 어렵습니다.
  
이 공격은 대규모 대상 기반 사용자에 대해 공통 암호를 지정할 수 있도록 하는 데 중점을 둔 것입니다.
  
### <a name="to-simulate-a-password-spray-attack"></a>암호 분무 공격을 시뮬레이션 하려면

1. [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **위협 관리** \> **공격 시뮬레이터**를 선택 합니다.
    
2. 공격에 대해 의미 있는 캠페인 이름을 지정 합니다.
    
3. 대상 받는 사람을 지정 합니다. 조직의 개인 또는 그룹이 될 수 있습니다. 공격이 성공 하려면 대상 받는 사람에 게 Exchange Online 사서함이 있어야 합니다.
    
4. 공격에 사용할 암호를 지정 합니다. 예를 들어 사용자가 시도할 수 있는 공통적이 고 관련 `Fall2017`암호는 한 가지입니다. 다른 것은 `Spring2018`또는 `Password1`입니다.
    
5. **마침을** 선택 하 여 공격을 시작 합니다. 
    
## <a name="brute-force-password-attack"></a>무작위 암호 공격

조직에 대 한 무작위 암호 공격은 잘못 된 행위자가 테 넌 트에서 주요 사용자 목록을 성공적으로 가져온 후에 일반적으로 사용 됩니다. 이 공격은 단일 사용자 계정에 대 한 암호 집합 시도에 집중 합니다.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>무작위 암호 공격을 시뮬레이트하기 위해

1. [보안 &amp; 및 준수 센터](https://protection.office.com)에서 **위협 관리** \> **공격 시뮬레이터**를 선택 합니다.
    
2. 공격에 대해 의미 있는 캠페인 이름을 지정 합니다.
    
3. 대상 받는 사람을 지정 합니다. 공격이 성공 하려면 대상 받는 사람에 게 Exchange Online 사서함이 있어야 합니다.
    
4. 공격에 사용할 암호 집합을 지정 합니다. 이렇게 하려면 암호 목록에 텍스트 (.txt) 파일을 사용할 수 있습니다. 텍스트 파일의 크기는 10mb를 넘을 수 없습니다. 한 줄에 하나씩 암호를 사용 하 고 목록의 마지막 암호 다음에 하드 리턴을 포함 해야 합니다.
    
5. **마침을** 선택 하 여 공격을 시작 합니다. 
    
## <a name="new-features-in-attack-simulator"></a>Attack 시뮬레이터의 새로운 기능

새 기능이 공격 시뮬레이터에 추가 됩니다. 다음과 같은 다양한 알고리즘과 방법이 있습니다.

- **고급 보고 기능** 공격 시뮬레이션 전자 메일 메시지를 여는 가장 빠른 시간 (또는 가장 느림)과 같은 데이터와 메시지에서 링크를 클릭 하는 가장 빠른 시간 (또는 가장 느림)이 표시 될 수 있습니다.

- **전자 메일 서식 파일 편집기**입니다. 이후 공격 시뮬레이션에 사용할 수 있는 재사용 가능한 사용자 지정 전자 메일 템플릿을 만들 수 있습니다.

[Microsoft 365 로드맵을](https://www.microsoft.com/microsoft-365/roadmap) 방문 하 여 개발 중인 작업, 진행 중인 작업 및 이미 실행 된 작업을 확인 합니다.

## <a name="see-also"></a>참고 항목

[Office 365 Advanced Threat Protection 서비스 Desription](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)

[Office 365 Advanced Threat Protection](office-365-atp.md)



