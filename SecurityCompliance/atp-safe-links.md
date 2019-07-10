---
title: Office 365 ATP 안전한 링크
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: 안전한 링크 기능은 Office 문서 및 전자 메일 메시지에서 하이퍼링크를 클릭 하 여 확인할 시간을 제공 합니다. 안전한 링크를 사용 하 여 피싱 및 기타 공격 으로부터 조직을 보호 합니다.
ms.openlocfilehash: 34d1ebbc5e0434de55f9e5f74a000bc8978e603e
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598544"
---
# <a name="office-365-atp-safe-links"></a>Office 365 ATP 안전한 링크

## <a name="overview-of-office-365-atp-safe-links"></a>Office 365 ATP 안전한 링크 개요

> [!IMPORTANT]
> 이 문서는 [Office 365 Advanced Threat Protection](office-365-atp.md)을 사용 하는 비즈니스 고객을 위한 것입니다. Outlook.com, Office 365 Home 또는 Office 365 Personal을 사용 하는 경우 Outlook의 안전한 링크에 대 한 정보를 찾으려면 [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2)를 참조 하세요.

Office 365 ATP 안전한 링크 ( [Advanced Threat Protection](office-365-atp.md)의 일부)는 [전자 메일 메시지](how-atp-safe-links-works.md#how-atp-safe-links-works-with-urls-in-email) 및 [Office 문서](how-atp-safe-links-works.md#how-atp-safe-links-works-with-urls-in-office-documents)에서 웹 주소 (url)를 클릭 하 여 확인 하는 시간을 제공 하 여 조직을 보호 하는 데 도움이 될 수 있습니다. 보호는 Office 365 보안 팀에서 설정 하는 [ATP 안전한 링크 정책을](set-up-atp-safe-links-policies.md) 통해 정의 됩니다.
  
ATP 안전한 링크 정책이 마련 되 면 Office 365 전역 관리자, 보안 관리자 및 보안 독자는 [Advanced Threat Protection에 대 한 보고서를 볼](view-reports-for-atp.md)수 있습니다. 이러한 보고서의 정보는 보안 팀이 조직을 보호 하거나 보안 인시던트를 연구 하기 위해 추가 단계를 수행 하는 데 도움이 될 수 있습니다.

[ATP에 새로운 기능을 추가](office-365-atp.md#new-features-in-office-365-atp)하면 Office 365 보안 팀에서 조직의 [ATP 안전한 링크 정책을](set-up-atp-safe-links-policies.md)추가 하거나 편집할 수 있습니다. 또한 새로 수정한 [경고 페이지](atp-safe-links-warning-pages.md) 와 Outlook의 기본 링크 렌더링 (예: Office 365 ProPlus 버전 1809에 도입 됨)과 같은 변경 내용과 개선 사항이 있을 수 있습니다.
         
## <a name="how-to-get-atp-safe-links-protection"></a>ATP 안전한 링크 보호를 가져오는 방법

**먼저 구독에 [Advanced Threat Protection](office-365-atp.md)이 포함 되어 있는지 확인**합니다. ATP는 [microsoft 365 enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), office 365 Enterprise E5, office 365 교육용 A5 등 구독에 포함 되어 있습니다. 조직에서 Office 365 ATP를 포함 하지 않는 Office 365 구독을 사용 하는 경우 ATP를 추가 기능으로 구매할 수 있습니다. 자세한 내용은 다음 리소스를 참조하십시오. 

- [Office 365 Advanced Threat Protection 계획 및 가격 책정](https://products.office.com/exchange/advance-threat-protection)

- [Office 365 Advanced Threat Protection 서비스 설명](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) 
  
**다음으로 ATP 안전한 링크 정책이 정의 되어 있는지 확인**합니다. ( [Office 365 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조) ATP Safe Links 기능은 다음과 같은 경우에 활성화 됩니다.
  
- ATP 안전한 링크 정책은 전자 메일 및 Office 문서용으로 설정 됩니다. ( [Office 365에서 ATP 안전한 링크 정책 설정](set-up-atp-safe-links-policies.md)참조)

- Office 365 클라이언트 앱은 최신 인증을 사용 하도록 구성 됩니다 (Office 문서에서 ATP 안전한 링크 보호를 위한 기능). ( [Office 2016의 최신 인증을](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)참조 하세요.) 
    
- 사용자가 회사 또는 학교 계정을 사용 하 여 Office 365에 로그인 했습니다. ( [Office 또는 office 365에 로그인을](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)참조 하세요.)
    
- 조직의 전자 메일은 Exchange Online Protection을 통해 전달 됩니다.  

**또한 필요한 사용 권한이 있는지 확인**합니다. ATP 정책을 정의 하거나 편집 하려면 적절 한 역할이 할당 되어 있어야 합니다. 다음 표에서는 몇 가지 예를 설명 합니다.

|역할  |할당 된 위치/방법  |
|---------|---------|
|Office 365 전역 관리자 |Office 365을 구매 하기 위해 등록 하는 사람은 기본적으로 전역 관리자입니다. 자세한 내용은 [Office 365 관리자 역할 정보](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) 를 참조 하세요.         |
|보안 관리자 |Azure Active Directory 관리 센터 ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online 조직 관리 |Exchange 관리 센터 ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>또는 <br>  PowerShell cmdlet ( [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)참조) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>ATP 안전한 링크 보호가 적절 한지 확인 하는 방법

전역 관리자 또는 보안 관리자로 서 [ATP 안전한 링크 정책을](set-up-atp-safe-links-policies.md) 정기적으로 검토 해야 합니다. ATP Safe 링크 정책은 보호 기능을 전자 메일 메시지의 하이퍼링크에 적용할지, 아니면 Office 문서의 Url에도 적용할 지를 결정 합니다.

ATP 안전한 링크 정책이 마련 되 면 조직의 보안 팀은 [Advanced Threat protection에 대 한 보고서](view-reports-for-atp.md)를 확인 하 여 조직에서 Atp 안전 링크 보호가 작동 하는 방식을 확인할 수 있습니다. 

## <a name="example-scenarios"></a>예제 시나리오
  
다음 표에서는 ATP 안전한 링크 보호가 발생할 수도 있고 그렇지 않을 수도 있는 경우의 몇 가지 예를 설명 합니다. 이러한 모든 경우에는 조직에 Office 365 Enterprise E5가 있다고 가정 합니다.
  
|**시나리오 예**|**이 경우 ATP 안전한 링크 보호가 적용 됩니까?**|
|:-----|:-----|
|Jean은 전자 메일 및 Office 문서의 Url을 포함 하는 ATP 안전한 링크 정책이 있는 그룹의 구성원입니다. Jean에서 다른 사용자가 보낸 PowerPoint 프레젠테이션을 열고 프레젠테이션에서 URL을 클릭 합니다.  <br/> |예. 지정 된 ATP Safe Links 정책은 Jean가 로그인 하 고 Windows, iOS 또는 Android 장치에서 Office 365 ProPlus를 사용 하 여 Jean 열리는 Jean의 그룹, Jean의 전자 메일 및 Word, Excel, PowerPoint 또는 Visio 문서에 적용 됩니다.  <br/> |
|Chris의 조직에서는 모든 글로벌 또는 보안 관리자가 ATP 안전한 링크 정책을 아직 정의 하지 않았습니다. Chris에 게 악성 웹 사이트에 대 한 URL을 포함 하는 전자 메일을 받습니다. 이 URL은 악성이 고 링크를 클릭 하는 것을 알 수 있습니다.  <br/> |아니요. 조직의 모든 사용자에 대 한 Url을 포함 하는 기본 정책은 보호를 적용 하기 위해 정의 해야 합니다.  <br/> |
|Pat 조직의 글로벌 또는 보안 관리자가 ATP 안전한 링크 정책을 아직 정의 하거나 편집 하지 않은 경우 Word 문서를 열고 파일의 URL을 클릭 합니다.  <br/> |아니요. 보호 기능을 적용 하려면 Office 문서를 포함 하는 정책을 정의 해야 합니다. [Office 365에서 ATP 안전한 링크 정책 설정를](set-up-atp-safe-links-policies.md)참조 하세요.  <br/> |
|Lee의 조직에는 차단 된 웹 사이트로 `http://tailspintoys.com` 나열 된 ATP 안전한 링크 정책이 있습니다. Lee는에 대 `http://tailspintoys.com/aboutus/trythispage`한 URL을 포함 하는 전자 메일 메시지를 받습니다. Lee에서 URL을 클릭 합니다.  <br/> |전체 사이트와 모든 하위 페이지가 차단 된 Url 목록에 포함 되어 있는지 여부에 따라 달라 집니다. [ATP 안전한 링크를 사용 하 여 차단 된 사용자 지정 url 목록 설정를](set-up-a-custom-blocked-urls-list-wtih-atp.md)참조 하세요.  <br/> |
|Jean의 동료는 전자 메일에 악성 URL이 포함 되어 있다는 사실을 모르고 Jean에 게 전자 메일을 보냅니다.  <br/> |이는 조직 내에서 전송 되는 전자 메일에 대해 ATP 안전한 링크 정책이 정의 되어 있는지 여부에 따라 달라 집니다. [Office 365에서 ATP 안전한 링크 정책 설정를](set-up-atp-safe-links-policies.md)참조 하세요.  <br/> |


  

