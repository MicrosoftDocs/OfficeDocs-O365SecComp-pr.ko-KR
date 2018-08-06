---
title: Exchange Online의 정보 권한 관리
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/13/2017
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2c956776-0016-4be6-b4cd-133a237f4a9e
description: 전자 메일을 통해 재무 데이터, 법적 계약, 기밀 제품 정보, 매출 보고서 및 매출 예상, 환자 건강 정보 또는 고객 및 직원 정보와 같은 중요한 정보를 교환하는 경우가 많습니다. 따라서 사서함이 잠재적으로 중요한 정보를 대량 포함하는 리포지토리가 될 뿐 아니라 정보 유출이 조직에 심각한 위협이 될 수 있습니다.
ms.openlocfilehash: de3bc22075a4a0f5e81fddece4c7ff3a54b22382
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027235"
---
# <a name="information-rights-management-in-exchange-online"></a>Exchange Online의 정보 권한 관리

전자 메일을 통해 재무 데이터, 법적 계약, 기밀 제품 정보, 매출 보고서 및 매출 예상, 환자 건강 정보 또는 고객 및 직원 정보와 같은 중요한 정보를 교환하는 경우가 많습니다. 따라서 사서함이 잠재적으로 중요한 정보를 대량 포함하는 리포지토리가 될 뿐 아니라 정보 유출이 조직에 심각한 위협이 될 수 있습니다.
  
정보 유출을 방지 하려면 Exchange Online 포함 전자 메일 메시지와 첨부 파일의 온라인 및 오프 라인 보호 기능을 제공 하는 정보 권한 관리 (IRM) 기능입니다. Microsoft Outlook 또는 웹에서 Outlook의 사용자가 IRM 보호를 적용할 수 및 전송 보호 규칙 또는 Outlook 보호 규칙을 사용 하 여 관리자가 적용할 수 있습니다. IRM 및 수에 액세스, 전달, 인쇄 또는 전자 메일 내에서 중요 한 데이터를 복사 하는 사용자가 컨트롤 도움이 됩니다.
  
## <a name="changes-to-how-irm-works-with-office-365-message-encryption-ome-and-azure-active-directory"></a>Office 365 메시지 암호화 (OME) 및 Azure Active Directory와의 IRM 작동 방식 변경

9 월 2017을 설정 하면 새로운 Office 365 메시지 암호화 기능을 조직에 대 한, 기준도 설정한 IRM Azure 권한 관리 (Azure RMS)에 사용 하기 위한 합니다. 하면 더이상 Azure RMS와 IRM 별도로 설정 합니다. 대신, OME 및 권한 관리 함께 원활 하 게 작동 합니다. 새로운 기능에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e)를 참조 하십시오. 조직 내에서 새 OME 기능을 사용 하 여 시작 준비가 된 것을 하는 경우 참조 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)합니다.
  
## <a name="how-irm-works-with-exchange-online-and-active-directory-rights-management-services"></a>Exchange Online 및 Active Directory 권한 관리 서비스의 IRM 작동 방식

Exchange Online IRM 온-프레미스 Active Directory Rights Management Services (AD RMS), Windows Server 2008에서 이동 하 고 나중에 정보 보호 기술을 사용합니다. IRM 보호 전자 메일 메시지에 AD RMS 권한 정책 템플릿을 적용 하 여 전자 메일에 적용 됩니다. 권한 보호 온라인 및 오프 라인에서 내부 및 조직의 방화벽 외부에서 발생 하는 메시지 자체에 첨부 됩니다.
  
사용자는 받는 사람에 게 메시지에 대 한 사용 권한을 제어 하는 전자 메일 메시지에 서식 파일을 적용할 수 있습니다. 메시지에는 AD RMS 권한 정책을 적용 하 여 착신 전환, 메시지에서 정보를 추출, 메시지를 저장 하거나 메시지를 인쇄 하는 등의 작업을 제어할 수 있습니다.
  
Windows Server 2008 이상을 실행 하는 AD RMS 서버를 사용 하 여 IRM을 구성할 수 있습니다. 클라우드 기반 조직에 대 한 AD RMS 권한 정책 서식 파일을 관리 하려면 AD RMS 서버를 사용할 수 있습니다. Outlook는 또한 사용자가 메시지를 보낼 때에 IRM 보호를 적용할 수 있도록 AD RMS 서버에 사용 합니다. 자세한 내용은 참조 [온-프레미스를 사용 하 여 IRM 구성 AD RMS 서버](configure-irm-to-use-an-on-premises-ad-rms-server.md)합니다. 
  
IRM을 사용하도록 설정한 후에는 다음과 같이 메시지에 IRM 보호를 적용할 수 있습니다.
  
- **사용자 Outlook 및 웹에서 Outlook을 사용 하 여 서식 파일을 수동으로 적용할 수 있습니다.** 사용자 **사용 권한 설정** 목록에서 서식 파일을 선택 하 여 전자 메일 메시지에 AD RMS 권한 정책 서식 파일을 적용할 수 있습니다. 사용자는 IRM으로 보호 된 메시지를 보낼 때 지원 되는 형식을 사용 하는 모든 첨부 파일 메시지와 동일한 IRM 보호를 받을 수도 있습니다. Word, Excel 및 PowerPoint으로.xps 파일 및 연결 된 전자 메일 메시지와 연결 된 파일에 IRM 보호 적용 됩니다. 
    
- **관리자 전송 보호 규칙을 사용 하 여 Outlook과 웹에서 Outlook에 IRM 보호를 자동으로 적용할 수 있습니다.** IRM 보호 메시지를 전송 보호 규칙을 만들 수 있습니다. 규칙 조건에 맞는 메시지에 AD RMS 권한 정책 템플릿을 적용 하려면 전송 보호 규칙 동작을 구성 합니다. IRM을 사용 하도록 설정한 후 조직의 AD RMS 권한 정책 템플릿 **적용 권한 보호 된 메시지를**호출 하는 전송 보호 규칙 작업을 사용 하 여 사용할 수는 있습니다.
    
- **관리자 Outlook 보호 규칙을 만들 수 있습니다.** Outlook 보호 규칙은 메시지를를 보낸 사용자는 보낸 사람의 부서를 포함 하는 메시지 조건에 따라 Outlook 2010 (하지 웹에 있는 Outlook)의 메시지에 IRM 보호를 자동으로 적용 하 고 내부 또는 외부 받는 사람에 게 표시 되는 인지 대화 조직입니다. 자세한 내용은 [Outlook 보호 규칙 만들기](http://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx)를 참조 합니다.
    

