---
title: AD RMS를 사용하여 Exchange Online 메일 암호화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/13/2017
audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2c956776-0016-4be6-b4cd-133a237f4a9e
description: 필요한 경우 조직 요구 사항을 충족 하기 위해 온-프레미스 AD RMS (Active Directory Rights Management Service)를 사용 하도록 Exchange Online IRM을 구성할 수 있습니다. 이는 일반적인 것이 아닙니다. AD RMS를 사용 해야 하는 요구 사항이 없는 경우에는 Office 메시지 암호화를 대신 사용 합니다.
ms.openlocfilehash: f5611ca7efeae0ab60ef90ebf4f8a225ea1332e7
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154270"
---
# <a name="exchange-online-mail-encryption-with-ad-rms"></a>AD RMS를 사용하여 Exchange Online 메일 암호화

Exchange Online에는 정보 유출을 방지하기 위해 전자 메일 메시지와 첨부 파일을 온라인과 오프라인에서 보호하는 IRM(정보 권한 관리) 기능이 포함되어 있습니다. 필요한 경우 조직 요구 사항을 충족 하기 위해 온-프레미스 AD RMS (Active Directory Rights Management Service)를 사용 하도록 Exchange Online IRM을 구성할 수 있습니다. 이는 일반적인 것이 아닙니다. AD RMS를 사용 해야 하는 요구 사항이 없는 경우에는 [Office 365 메시지 암호화](ome.md) 를 대신 사용 합니다. 

IRM 보호는 Microsoft Outlook 또는 웹용 Outlook 사용자가 적용할 수 있으며, 전송 보호 규칙 또는 Outlook 보호 규칙을 사용 하 여 관리자가 적용할 수 있습니다. IRM을 통해 고객과 고객의 사용자는 전자 메일 내의 중요한 데이터를 액세스, 전달, 인쇄 또는 복사할 수 있는 사람을 제어할 수 있습니다.
  
## <a name="changes-to-how-irm-works-with-office-365-message-encryption-ome-and-azure-active-directory"></a>IRM이 Office 365 메시지 암호화 (OME) 및 Azure Active Directory에서 작동 하는 방식에 대 한 변경 사항

9 월 2017 일, 조직에 대 한 새 Office 365 메시지 암호화 기능을 설정할 때 azure RMS (Azure 권한 관리)와 함께 사용할 수 있도록 IRM을 설정 합니다. 더 이상 Azure RMS를 사용 하 여 IRM을 별도로 설정 하지는 않습니다. 대신 OME 및 권한 관리가 함께 원활 하 게 작동 합니다. 새 기능에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e)를 참조 하세요. 조직 내에서 새 OME 기능을 사용할 준비가 [되 면 Set Up Office 365 Message Encryption capabilities for The Azure Information Protection](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)를 참조 하세요.
  
## <a name="how-irm-works-with-exchange-online-and-active-directory-rights-management-services"></a>Exchange Online 및 Active Directory 권한 관리 서비스에서 IRM이 작동 하는 방식

Exchange Online IRM은 Windows Server 2008 이상에서 정보 보호 기술인 온-프레미스 AD RMS (Active Directory Rights Management Services)를 사용 합니다. AD RMS 권한 정책 템플릿을 전자 메일 메시지에 적용하여 전자 메일에 IRM 보호를 적용합니다. 권한은 메시지 자체에 첨부 되므로 보호가 온라인 및 오프 라인 상태이 고 조직의 방화벽 내부 및 외부에서 보호 됩니다.
  
사용자는 전자 메일 메시지에 템플릿을 적용 하 여 받는 사람이 메시지에 대해 갖는 사용 권한을 제어할 수 있습니다. 즉, 메시지에 AD RMS 권한 정책을 적용하여 전달, 메시지에서 정보 추출, 메시지 저장 또는 메시지 인쇄 등의 작업을 제어할 수 있습니다.
  
Windows Server 2008 이상 버전을 실행 하는 AD RMS 서버를 사용 하도록 IRM을 구성할 수 있습니다. 이 AD RMS 서버를 사용하여 클라우드 기반 조직에 대한 AD RMS 권한 정책 템플릿을 관리합니다. 또한 Outlook에서는 AD RMS 서버를 사용하여 사용자가 자신이 보낸 메시지에 IRM 보호를 적용할 수 있도록 합니다. 자세한 내용은 [온-프레미스 AD RMS 서버를 사용 하도록 IRM 구성을](configure-irm-to-use-an-on-premises-ad-rms-server.md)참조 하십시오. 
  
IRM을 사용하도록 설정한 후에는 다음과 같이 메시지에 IRM 보호를 적용할 수 있습니다.
  
- **사용자는 수동으로 Outlook 및 웹용 Outlook을 사용 하 여 서식 파일을 적용할 수 있습니다.** 사용자는 **사용 권한 설정** 목록에서 AD RMS 권한 정책 템플릿을 선택하여 전자 메일 메시지에 적용할 수 있습니다. 사용자가 IRM으로 보호된 메시지를 보내는 경우 지원되는 형식을 사용하는 첨부된 파일에도 메시지와 같은 IRM 보호가 적용됩니다. IRM 보호는 .xps 파일 및 첨부된 전자 메일 메시지는 물론 Word, Excel 및 PowerPoint와 연결된 파일에도 적용됩니다. 
    
- **관리자는 전송 보호 규칙을 사용 하 여 Outlook 및 웹용 Outlook에 모두 IRM 보호를 자동으로 적용할 수 있습니다.** IRM 보호 메시지에 대한 전송 보호 규칙을 만들 수 있습니다. 규칙 조건에 맞는 메시지에 AD RMS 권한 정책 템플릿을 적용하도록 전송 보호 규칙 동작을 구성합니다. IRM을 사용하도록 설정하고 나면 조직의 AD RMS 권한 정책 템플릿을 **다음을 포함하는 메시지에 권한 보호 적용**이라는 전송 보호 규칙 동작과 함께 사용할 수 있게 됩니다.
    
- **관리자가 Outlook 보호 규칙을 만들 수 있습니다.** Outlook 보호 규칙은 보낸 사람의 부서, 메시지를 보낸 사람 및 받는 사람이 외부에 있는지 여부를 포함 하는 메시지 조건을 기준으로 Outlook 2010 (웹에서 Outlook이 아님)의 메시지에 IRM 보호를 자동으로 적용 합니다. 조직. 자세한 내용은 [Create an Outlook Protection Rule](http://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx)를 참조하십시오.
    

