---
title: "Azure Information protection의 보호 기능을 사용 하 여 기존 Office 365 테 넌 트에" krowley 만든이 "를 적용 합니다. 만든이: laurawi: it 전문 ms. 날짜 우선 순위: 일반 검색. appverid:
- MET150 assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d. 컬렉션:
    - M365-security-준수 설명: "7 월 2018에 시작 하 여 정보를 보호 하는 초기 단계를 지원 하기 위해 모든 azure information protection 적합 한 테 넌 트에는 기본적으로 azure information protection의 보호 기능이 설정 됩니다. Azure Information protection의 보호 기능은 이전에는 Office 365에서 권한 관리 또는 Azure RMS로 알려져 있었습니다. 조직에 Office E3 서비스 계획 또는 서비스 계획이 더 높은 경우에는 이러한 기능을 롤아웃할 때 Azure 정보 보호를 통해 정보를 보호 하기 시작할 수 있습니다. "
---

# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Azure Information protection의 보호 기능을 통해 기존 Office 365 테 넌 트에 배포

정보를 보호 하는 초기 단계를 지원 하기 위해 7 월 2018 일부터 모든 azure information protection 적합 한 테 넌 트에는 기본적으로 azure information protection의 보호 기능이 설정 됩니다. Azure Information protection의 보호 기능은 이전에는 Office 365에서 권한 관리 또는 Azure RMS로 알려져 있었습니다. 조직에 Office E3 서비스 계획 또는 서비스 계획이 더 높은 경우에는 이러한 기능을 롤아웃할 때 Azure information Protection을 통해 정보를 보호 하기 시작할 수 있게 됩니다.
  
## <a name="changes-beginning-july-1-2018"></a>2018 년 7 월 1 일부터 변경

2018 년 7 월 1 일부 터 시작 하는 Microsoft는 다음 구독 계획 중 하나가 있는 모든 Office 365 테 넌 트에 대해 Azure Information protection의 보호 기능을 사용 하도록 설정 합니다.
  
- office 365 메시지 암호화는 office 365 E3 및 e5, Microsoft E3 및 e5, office 365 A1, A3, A5 및 office 365 G3 및 G5의 일부로 제공 됩니다. Azure Information protection에서 제공 하는 새로운 보호 기능을 수신 하기 위해 추가 라이선스가 필요 하지는 않습니다. 
    
- 또한 다음 계획에 Azure Information Protection 계획 1을 추가 하 여 exchange online 계획 1, exchange online 계획 2, office 365 F1, office 365 business Essentials, office 365 business Premium 등의 새로운 Office 365 메시지 암호화 기능을 받을 수 있습니다. Office 365 Enterprise E1.
    
- Office 365 메시지 암호화에서 각 사용자 benefiting 기능을 사용 하도록 허가 받아야 합니다.
    
- 전체 목록은 Office 365 메시지 암호화에 대 한 [Exchange Online 서비스 설명을](https://technet.microsoft.com/library/exchange-online-service-description.aspx) 참조 하세요. 
    
테 넌 트 관리자는 Office 365 관리자 포털에서 보호 상태를 확인할 수 있습니다. 
  
![Office 365의 권한 관리가 활성화 되었음을 보여 주는 스크린샷](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>변경 되는 이유는 무엇 인가요?

Office 365 메시지 암호화는 Azure Information protection의 보호 기능을 활용 합니다. Office 365 메시지 암호화에 대 한 최신 개선 사항 및 Microsoft 365의 정보 보호에 대 한 폭넓은 투자를 통해 조직에서 최대한 간편 하 게 보호 기능을 설정 하 고 사용할 수 있습니다. 설정 하기가 어려웠습니다. 기본적으로 Azure Information protection의 보호 기능을 설정 하 여 중요 한 데이터를 빠르게 보호할 수 있습니다.
  
## <a name="does-this-impact-me"></a>나에 게 영향을 줍니까?

office 365 조직에서 적격 office 365 라이선스를 구매한 경우이 변경으로 인해 테 넌 트가 영향을 받게 됩니다.
  
 **중요!** 온-프레미스 환경에서 AD RMS (Active Directory Rights Management Services)를 사용 하는 경우에는이 변경 내용을 즉시 옵트아웃 하거나 Azure Information Protection으로 마이그레이션해야 하 여 다음 30 일 이내에이 변경 내용을 롤아웃 해야 합니다. 옵트아웃 하는 방법에 대 한 자세한 내용은이 문서 뒷부분에 나오는 "AD RMS를 사용 하 여 out?를 선택 하는 방법"을 참조 하십시오. 마이그레이션하려는 경우 [AD RMS에서 Azure Information Protection으로 마이그레이션을 참조 하세요.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>AD RMS (Active Directory Rights Management Services)와 함께 Azure Information Protection을 사용할 수 있나요?

아니요. 이 배포 시나리오는 지원 되지 않습니다. 추가 옵트아웃 단계를 수행 하지 않고 일부 컴퓨터가 Azure 권한 관리 서비스를 자동으로 시작 하 고 AD RMS 클러스터에 연결할 수도 있습니다. 이 시나리오는 지원 되지 않으며 결과를 신뢰할 수 없으므로 다음 30 일 이내에 이러한 변경 내용을 취소 하는 것이 중요 하므로 이러한 새로운 기능을 롤아웃하기는 것이 좋습니다. 옵트아웃 하는 방법에 대 한 자세한 내용은이 문서 뒷부분에 나오는 "AD RMS를 사용 하 여 out?를 선택 하는 방법"을 참조 하십시오. 마이그레이션하려는 경우 [AD RMS에서 Azure Information Protection으로 마이그레이션을 참조 하세요.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>AD RMS를 사용 하 고 있는지 여부를 어떻게 알 수 있나요?

다음 지침에 따라 ad rms [(Active Directory rights management Services)를 배포 하는 경우 Azure 권한 관리에 대 한 환경을 준비 하는](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) 방법을 참조 하세요. 
  
1. 선택 사항 이지만 대부분의 AD rms 배포는 도메인 컴퓨터에서 ad rms 클러스터를 검색할 수 있도록 SCP (서비스 연결 지점)를 Active Directory에 게시 합니다. 
  
ADSI 편집을 사용 하 여 Active Directory에 게시 된 SCP가 있는지 확인: cn = Configuration [server name], cn = Services, cn = rightsmanagementservices, CN = SCP
    
2. SCP를 사용 하지 않는 경우 AD RMS 클러스터에 연결 하는 windows 컴퓨터는 windows 레지스트리를 사용 하 여 클라이언트 쪽 서비스 검색 또는 라이선스 리디렉션을 위해 구성 해야 함: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation 또는 HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
이러한 레지스트리 구성에 대 한 자세한 내용은 [Windows 레지스트리를 사용 하 여 클라이언트 쪽 서비스 검색 설정](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) 및 [라이선스 서버 트래픽 리디렉션을](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic)참조 하십시오.
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>AD RMS를 사용 하는 경우 어떻게 하면이를 옵트아웃 합니까?

예정 된 변경 내용을 취소 하려면 다음 단계를 완료 합니다.
  
1. Office 365 조직에서 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 하는 경우 Windows PowerShell 세션을 시작 하 고 Exchange Online에 연결 합니다. 자세한 내용은 [Exchange Online PowerShell에 연결을](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)참조 하십시오.
    
2. 다음 구문을 사용 하 여 irmconfiguration cmdlet을 실행 합니다.
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>이 변경 사항을 적용 한 후에는 무엇을 기대할 것인가?

이 기능이 사용 하도록 설정 된 경우에는 [Microsoft Ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) 에서 발표 된 새로운 버전의 Office 365 메시지 암호화를 사용 하 고 Azure 정보의 암호화 및 보호 기능을 활용할 수 있습니다. 보호용. 
  
![웹용 Outlook에서 OME protected 메시지를 표시 하는 스크린샷](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
새로운 향상 된 기능에 대 한 자세한 내용은 [Office 365 메시지 암호화](ome.md)를 참조 하세요.
  

