---
title: 기존 Office 365 테 넌 트에 롤아웃 Azure 정보 보호의 보호 기능
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d
description: 7 월 2018 모든 Azure 정보 보호 가능한 테 넌 트를 시작 하 여 정보를 보호 하는 초기 단계를 위해 됩니다가 Azure 정보 보호의 보호 기능 기본적으로 설정 합니다. Azure 정보 보호의 보호 기능으로 권한 관리 또는 Azure RMS Office 365에서 이전의 했습니다. 조직에는 Office E3 서비스 계획 또는 더 높은 서비스 계획 하는 경우 이러한 기능 모색 때 Azure 정보 보호 기능을 통해 정보를 보호 머리 시작을 받을 수 있게 합니다.
ms.openlocfilehash: be0200da3032dccbcf54e67f3bdfbac800b65526
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533228"
---
# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>기존 Office 365 테 넌 트에 롤아웃 Azure 정보 보호의 보호 기능

7 월 2018 모든 Azure 정보 보호 가능한 테 넌 트를 시작 하 여 정보를 보호 하는 초기 단계를 위해 됩니다가 Azure 정보 보호의 보호 기능 기본적으로 설정 합니다. Azure 정보 보호의 보호 기능으로 권한 관리 또는 Azure RMS Office 365에서 이전의 했습니다. 조직에는 Office E3 서비스 계획 또는 더 높은 서비스 계획 하는 경우 이러한 기능 모색 때 Azure 정보 보호 기능을 통해 정보를 보호 머리 시작을 받을 수 있게 합니다.
  
## <a name="changes-beginning-july-1-2018"></a>2018 년 7 월 1을 시작 하는 변경 내용

Microsoft은 2018 년 7 월 1, 시작 다음의 구독 계획 중 하나를 가진 모든 Office 365 테 넌 트에 대 한 Azure 정보 보호에서 보호 기능을 활성화 됩니다.
  
- Office 365 메시지 암호화는 Office 365 E3 및 e 5, Microsoft E3 및 e 5, Office 365 A1, a 3 및 A5, 및 Office 365 G3 / g 5의 일부분으로 제공 됩니다. Azure 정보 보호 구동 되는 새 보호 기능을 수신 하기 위한 추가 라이선스를 필요 하지 않습니다. 
    
- 다음에 Azure 정보 보호 계획 1 새로운 Office 365 메시지 암호화 기능을 수신 하도록 계획을 추가할 수도 있습니다: Exchange Online 계획 1 "," Exchange Online 계획 2 "," Office 365 F1 "," Office 365 비즈니스 Essentials "," Office 365 프리미엄, 또는 Office 365 Enterprise E1 합니다.
    
- Office 365 메시지 암호화에서 이점의 각 사용자 기능에 의해 표시할 사용이 허가 되도록 해야 합니다.
    
- 전체 목록은 Office 365 메시지 암호화에 대 한 [Exchange Online 서비스 설명](https://technet.microsoft.com/library/exchange-online-service-description.aspx) 을 참조 합니다. 
    
테 넌 트 관리자는 Office 365 관리자 포털의 보호 상태를 확인할 수 있습니다. 
  
![Office 365에서 해당 권한 관리를 보여주는 스크린샷이 활성화 됩니다.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>이 변경 하는 이유는?

Office 365 메시지 암호화 Azure 정보 보호의 보호 기능을 활용합니다. Office 365 메시지 암호화의 최근 개선 사항 및 Microsoft 365의 정보 보호 기능을 사용해 광범위 한 투자의 핵심, 우리는 보다 쉽게 사용 하 여 과거에 암호화로 사용해 보호 기능을 사용 하는 조직에 대 한 기술 설정 하기 어려운 되었을 수 있습니다. 기본적으로 Azure 정보 보호의 보호 기능을 설정 하 여 시작할 수 있는 신속 하 게 중요 한 데이터를 보호 합니다.
  
## <a name="does-this-impact-me"></a>이 영향을 줄 있나요?

Office 365 조직에 사용할 수 있는 Office 365 라이선스를 구입 하 고, 테 넌 트는 이러한 변경에 의해 영향을 합니다.
  
 **중요!** 온-프레미스 환경에서 Active Directory Rights Management Services (AD RMS)를 사용 하는 경우 옵트아웃할이 변경이 내용 즉시 하거나 앞으로 30 일 내에서이 변경을 모색 전에 Azure 정보 보호를 마이그레이션해야 합니다. 옵트아웃,이 문서 뒷부분의 "AD RMS 사용, out? 수신 동의 어떻게"를 참조 하는 방법에 대 한 정보입니다. 마이그레이션하는 것을 선호 하는 경우 참조 [Azure 정보 보호 AD RMS에서 마이그레이션.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Azure 정보 보호를 사용 하 여 Active Directory 권한 관리 서비스 (AD RMS)와 함께 수 있습니까?

아니요. 이것은 지원 되는 배포 시나리오가 아닙니다. 추가 옵트아웃 단계를 수행 하지 않고 일부 컴퓨터 Azure 권한 관리 서비스를 사용 하 여 자동으로 시작 하 고도 AD RMS 클러스터에 연결 될 수 있습니다. 이 시나리오 지원 되지 않습니다 있으며 신뢰할 수 없는 결과 수 있으므로 이러한 새로운 기능은 모색 하기 전에 다음 30 일 내에서이 변경을 나올 때까지 옵트아웃 중요 합니다. 옵트아웃,이 문서 뒷부분의 "AD RMS 사용, out? 수신 동의 어떻게"를 참조 하는 방법에 대 한 정보입니다. 마이그레이션하는 것을 선호 하는 경우 참조 [Azure 정보 보호 AD RMS에서 마이그레이션.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>AD RMS를 사용 하 고 하는 경우 어떻게 알 수 있습니까?

[Active Directory Rights Management Services (AD RMS)도 있는 경우 Azure 권한 관리를 위한 환경을 준비 하는 중](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) 에서 이러한 지침을 사용 하 여 AD RMS를 배포한 경우 확인 하려면: 
  
1. 선택 사항이 며 있지만 대부분의 AD RMS 배포 도메인 컴퓨터 AD RMS 클러스터를 검색할 수 있도록 Active Directory에 서비스 연결 지점 (SCP)를 게시 합니다. 
  
ADSI 편집을 사용 하 여 Active Directory에 게시 한 SCP 해야 하는지 여부를 확인 하려면: CN = Configuration [서버 이름], CN = Services, CN RightsManagementServices, CN = SCP =
    
2. AD RMS 클러스터에 연결 하는 Windows 컴퓨터를 Windows 레지스트리를 사용 하 여 클라이언트쪽 서비스 검색 또는 라이선스 리디렉션을 구성 해야 SCP를 사용 하지 않는 경우: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation 또는 HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
이러한 레지스트리 구성에 대 한 자세한 내용은 [Windows 레지스트리를 사용 하 여 활성화 클라이언트쪽 서비스 검색](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) 및 [리디렉션 서버 트래픽 라이선스](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic)를 참조 하십시오.
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>AD RMS 어떻게 수행 합니까 옵트아웃할 사용 합니까?

예정 된 변경, 거부 하려면 다음이 단계를 완료 합니다.
  
1. Office 365 조직에 대 한 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 하는 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Connect to Exchange Online PowerShell를](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)참조 하십시오.
    
2. 다음 구문을 사용 하 여 Set-irmconfiguration cmdlet을 실행 합니다.
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>무엇을 수 후이 변경 되었음을 나타내는 것으로 예상 합니까?

활성화 되 면이 되어 있음 하지 않은 경우, 새 버전의 [Microsoft Ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) 에서 발표 된 Azure 정보의 암호화 및 보호 기능을 활용 하는 Office 365 메시지 암호화를 사용 하 여 시작할 수 있습니다. 보호 합니다. 
  
![OME을 보여주는 스크린샷 보호 웹에 있는 Outlook에서 메시지를 받습니다.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
새 향상 된 기능에 대 한 자세한 내용은 [Office 365 메시지 암호화](ome.md)를 참조 하십시오.
  

