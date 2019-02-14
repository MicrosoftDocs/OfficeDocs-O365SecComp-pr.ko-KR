---
title: Office 365의 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
description: Office 365에서 가장 강력한 암호화, 프로토콜 및 사용할 수 있는 기술을 사용 하 여 전송 하 고 나머지 부분에 콘텐츠 암호화 됩니다. Office 365의 암호화의 개요를 확인 합니다.
ms.openlocfilehash: 5f64d6e758818d410f54370adee549f565d4f042
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995109"
---
# <a name="encryption-in-office-365"></a>Office 365의 암호화

암호화는 파일 보호 및 정보 보호 전략의 중요 한 부분입니다. 이 문서는 Office 365의 모든 버전에 사용 되는 암호화 대략적를 읽고 Office 문서 암호 보호를 조직에 대 한 암호화 설정에서 암호화 작업에 대 한 도움말 보기입니다.
  
- 인증서 및 TLS와 같은 기술에 대 한 정보를 찾고 하는 경우 [Office 365의 암호화에 대 한 자세한 내용은 기술 참조 (영문)를](technical-reference-details-about-encryption.md)참조 하십시오.
    
- 구성 또는 조직에 대 한 암호화를 설정 하는 방법에 대 한 정보를 찾고 하는 경우 [Office 365 Enterprise의 암호화 설정](set-up-encryption.md)참조 하십시오.
    
## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>암호화 무엇 이며 Office 365에서 어떻게 작동 합니까?

높은 수준 암호화는 암호화 텍스트의 암호를 해독할 때까지 사용자 또는 컴퓨터에서 사용할 수 없는 암호화 텍스트에는 프로세스 (일반 텍스트 라고 함) 하 여 데이터를 인코딩입니다. 암호 해독에만 권한이 부여 된 사용자에 게 암호화 키가 필요 합니다. 암호화 소음이 권한이 부여 된 받는 사람에 게 전자 메일 메시지와 파일이 같은 콘텐츠를 해독할 수 있습니다.
  
단독으로 암호화 잘못 된 자동으로 시작에서 파일, 전자 메일 메시지, 일정 항목 등의 콘텐츠를 못하도록 막지 않습니다. 암호화는 조직에 대 한 더 큰 정보 보호 전략의 일부분입니다. 암호화를 사용 하 여만 받는 사람이 암호화 된 데이터를 사용할 수 있어야가을 수 있도록 할 수 있습니다.
  
원본 위치에 동시에 암호화의 여러 계층을 포함할 수 있습니다. 예, 전자 메일 메시지와 전자 메일 흐름 되는 통신 채널을 암호화할 수 있습니다. Office 365에서 여러 강력한 암호화 프로토콜 및 전송 계층 보안/Secure Sockets Layer (TLS/SSL), 인터넷 프로토콜 보안 (IPSec) 및 고급 암호화를 포함 하는 기술을 사용 하 여 전송 하 고 나머지 부분에서 데이터가 암호화 됩니다. 표준 (AES)입니다.
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>보관 된 데이터 및 데이터 전송에서에 대 한 암호화

 **보관 된 데이터의** 예로 SharePoint 라이브러리, Project Online 데이터, 비즈니스 모임, 전자 메일 메시지와 Office 365의 폴더에 저장 된 첨부 파일에 대 한 Skype에 업로드 된 문서를 업로드 된 파일 사서함 및 비즈니스용 OneDrive에 업로드 된 파일입니다. 
  
 **전송 되에서는 데이터의** 예로 배달 되지 진행 하는 메일 메시지 또는 온라인 모임에서 수행 되는 대화를 들 수 있습니다. Office 365는 데이터 전송 중에는 Office 365에 서버와 통신 하는 사용자의 장치 때마다 또는 Office 365 서버를 다른 서버와 통신 하는 경우. 
  
Office 365와 함께 여러 계층 및 데이터를 보호 하기 위해 협력 하는 암호화의 종류 가질 수 있습니다. 다음 표에서 추가 정보에 대 한 링크와 예가 포함 됩니다.
  
|**종류의 콘텐츠**|**암호화 기술**|**자세한 내용은 리소스**|
|:-----|:-----|:-----|
|장치에서 파일입니다. 이 폴더, 컴퓨터, 태블릿, 또는 전화에 저장 하는 Office 문서 또는 Microsoft 클라우드로 저장 되는 데이터에 저장 하는 전자 메일 메시지를 포함할 수 있습니다.  <br/> |Microsoft 데이터 센터의 BitLocker 합니다. BitLocker는 사용 하 여 Windows 컴퓨터 및 태블릿 등의 클라이언트 컴퓨터에도 수 있습니다.  <br/> Microsoft 데이터 센터의 분산된 키 관리자 (DKM)  <br/> Office 365에 대 한 고객 키  <br/> |[Windows IT 센터: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Microsoft 보안 센터: 암호화](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [시리즈를 제어 하는 클라우드 보안: 보관 된 데이터를 암호화](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Exchange Online이 전자 메일 암호를 보호하는 방법](exchange-online-secures-email-secrets.md) <br/> [고객 키를 사용하여 Office 365에서 데이터 제어](controlling-your-data-using-customer-key.md) <br/> |
|사용자 간에 전송 되는 파일입니다. 이 Office 문서 또는 사용자 간에 공유 하는 SharePoint 목록 항목에 포함할 수 있습니다.  <br/> |파일 전송에 대 한 TLS  <br/> |[비즈니스용 OneDrive 및 SharePoint Online에서의 데이터 암호화](data-encryption-in-odb-and-spo.md) <br/> [온라인 비즈니스에 대 한 Skype: 보안 및 보관](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|전자 메일을 받는 사람에 게 간에 전송 합니다. Exchange Online에서 호스트 하는 전자 메일 포함 됩니다.  <br/> |Azure 권한 관리, S/MIME 및 전송 중에서 전자 메일에 대 한 TLS를 사용 하 여 office 365 메시지 암호화  <br/> |[Office 365 메시지 암호화 (OME)](ome.md) <br/> [Office 365의 전자 메일 암호화](email-encryption.md) <br/> [Office 365의 전자 메일 연결 보안을 위해 Exchange Online에서 TLS를 사용하는 방법](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |
   
## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>경우에 어떻게 합니까 필요한 보다 세부적으로 제어 암호화 보안 및 규정 준수 요구 사항을 충족 합니까?

볼륨 암호화, 파일 암호화 및 Office 365에서 사서함 암호화 솔루션 Microsoft 관리 외에도 더 엄격한 보안 및 규정 준수 요구 사항을 충족 고객 관리 옵션을 사용할 수 있습니다. 이러한 솔루션 Office 365와 함께 Azure 권한 관리 (Azure RMS)를 사용 합니다.
  
자세한 내용은 다음 리소스를 참조 하십시오.
  
- [Azure 권한 관리 이란?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
    
- [Office 365 관리 센터에서 Azure 권한 관리 활성화](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)
    
- [Set up Information Rights Management (IRM) in SharePoint admin center](set-up-irm-in-sp-admin-center.md)
    
## <a name="how-do-i"></a>작업 방법

|**이 작업을 수행 하려면**|**이러한 리소스를 참조 하십시오.**|
|:-----|:-----|
|내 조직에 대 한 암호화 설정  <br/> |[Office 365 Enterprise의 암호화 설정](set-up-encryption.md) <br/> |
|인증서, 기술 및 Office 365에서 TLS 암호화 제품군에 대 한 세부 정보 보기  <br/> |[Office 365의 암호화에 대 한 기술 정보](technical-reference-details-about-encryption.md) <br/> |
|모바일 장치에서 암호화 된 메시지와 함께 작동 합니다.  <br/> |[Android 장치에서 암호화 된 메시지 보기](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [IPhone 또는 iPad에서 암호화 된 메시지 보기](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|암호 보호 기능을 사용 하 여 문서를 암호화  <br/><br/>  현재 암호 보호 Office Online에서 지원 되지 않습니다. 암호 보호를 위한 Word, Excel 및 PowerPoint의 데스크톱 버전을 사용 합니다.           |[문서, 통합 문서 또는 프레젠테이션에 추가 또는 제거 보호](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (한 **추가 보호** 섹션을 선택 하 고 **데이터베이스 암호를** 참조)  <br/> |
|문서에서 암호화를 제거 합니다.  <br/> |[문서, 통합 문서 또는 프레젠테이션에 추가 또는 제거 보호](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) ( **보호를 제거** 하는 섹션을 선택 하 고 **암호 암호화 제거** 를 참조)  <br/> |
   
## <a name="related-topics"></a>관련 항목

[Office 365 보안 및 정보 보호 기능에 대 한 계획](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[보안 및 비즈니스-관리자 도움말에 대 한 Office 365의 규정 준수 기능](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  

