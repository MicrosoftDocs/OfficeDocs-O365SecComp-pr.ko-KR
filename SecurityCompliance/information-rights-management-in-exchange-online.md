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
search.appverid:
- MET150
ms.assetid: 2c956776-0016-4be6-b4cd-133a237f4a9e
description: 전자 메일을 통해 재무 데이터, 법적 계약, 기밀 제품 정보, 매출 보고서 및 매출 예상, 환자 건강 정보 또는 고객 및 직원 정보와 같은 중요한 정보를 교환하는 경우가 많습니다. 따라서 사서함이 잠재적으로 중요한 정보를 대량 포함하는 리포지토리가 될 뿐 아니라 정보 유출이 조직에 심각한 위협이 될 수 있습니다.
ms.openlocfilehash: 5036fe359215de1c2674d7efabbb283c78418a19
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002575"
---
# <a name="information-rights-management-in-exchange-online"></a><span data-ttu-id="e5b12-104">Exchange Online의 정보 권한 관리</span><span class="sxs-lookup"><span data-stu-id="e5b12-104">Information Rights Management in Exchange Online</span></span>

<span data-ttu-id="e5b12-p102">전자 메일을 통해 재무 데이터, 법적 계약, 기밀 제품 정보, 매출 보고서 및 매출 예상, 환자 건강 정보 또는 고객 및 직원 정보와 같은 중요한 정보를 교환하는 경우가 많습니다. 따라서 사서함이 잠재적으로 중요한 정보를 대량 포함하는 리포지토리가 될 뿐 아니라 정보 유출이 조직에 심각한 위협이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p102">People often use email to exchange sensitive information, such as financial data, legal contracts, confidential product information, sales reports and projections, patient health information, or customer and employee information. As a result, mailboxes can become repositories for large amounts of potentially sensitive information and information leakage can become a serious threat to your organization.</span></span>
  
<span data-ttu-id="e5b12-p103">정보 유출을 방지 하려면 Exchange Online 포함 전자 메일 메시지와 첨부 파일의 온라인 및 오프 라인 보호 기능을 제공 하는 정보 권한 관리 (IRM) 기능입니다. Microsoft Outlook 또는 웹에서 Outlook의 사용자가 IRM 보호를 적용할 수 및 전송 보호 규칙 또는 Outlook 보호 규칙을 사용 하 여 관리자가 적용할 수 있습니다. IRM 및 수에 액세스, 전달, 인쇄 또는 전자 메일 내에서 중요 한 데이터를 복사 하는 사용자가 컨트롤 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p103">To help prevent information leakage, Exchange Online includes Information Rights Management (IRM) functionality that provides online and offline protection of email messages and attachments. IRM protection can be applied by users in Microsoft Outlook or Outlook on the web, and it can be applied by administrators using transport protection rules or Outlook protection rules. IRM helps you and your users control who can access, forward, print, or copy sensitive data within an email.</span></span>
  
## <a name="changes-to-how-irm-works-with-office-365-message-encryption-ome-and-azure-active-directory"></a><span data-ttu-id="e5b12-110">Office 365 메시지 암호화 (OME) 및 Azure Active Directory와의 IRM 작동 방식 변경</span><span class="sxs-lookup"><span data-stu-id="e5b12-110">Changes to how IRM works with Office 365 Message Encryption (OME) and Azure Active Directory</span></span>

<span data-ttu-id="e5b12-p104">9 월 2017을 설정 하면 새로운 Office 365 메시지 암호화 기능을 조직에 대 한, 기준도 설정한 IRM Azure 권한 관리 (Azure RMS)에 사용 하기 위한 합니다. 하면 더이상 Azure RMS와 IRM 별도로 설정 합니다. 대신, OME 및 권한 관리 함께 원활 하 게 작동 합니다. 새로운 기능에 대 한 자세한 내용은 [Office 365 메시지 암호화 FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e)를 참조 하십시오. 조직 내에서 새 OME 기능을 사용 하 여 시작 준비가 된 것을 하는 경우 참조 [Azure 정보 보호 위쪽에 구축 된 새로운 Office 365 메시지 암호화 기능을 설정](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)합니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p104">As of September 2017, when you set up the new Office 365 Message Encryption capabilities for your organization, you also set up IRM for use with Azure Rights Management (Azure RMS). You no longer set up IRM with Azure RMS separately. Instead, OME and rights management work seamlessly together. For more details about the new capabilities, see [Office 365 Message Encryption FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e). If you're ready to get started using the new OME capabilities within your organization, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e).</span></span>
  
## <a name="how-irm-works-with-exchange-online-and-active-directory-rights-management-services"></a><span data-ttu-id="e5b12-116">Exchange Online 및 Active Directory 권한 관리 서비스의 IRM 작동 방식</span><span class="sxs-lookup"><span data-stu-id="e5b12-116">How IRM works with Exchange Online and Active Directory Rights Management Services</span></span>

<span data-ttu-id="e5b12-p105">Exchange Online IRM 온-프레미스 Active Directory Rights Management Services (AD RMS), Windows Server 2008에서 이동 하 고 나중에 정보 보호 기술을 사용합니다. IRM 보호 전자 메일 메시지에 AD RMS 권한 정책 템플릿을 적용 하 여 전자 메일에 적용 됩니다. 권한 보호 온라인 및 오프 라인에서 내부 및 조직의 방화벽 외부에서 발생 하는 메시지 자체에 첨부 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p105">Exchange Online IRM uses on-premises Active Directory Rights Management Services (AD RMS), an information protection technology in Windows Server 2008 and later. IRM protection is applied to email by applying an AD RMS rights policy template to an email message. Rights are attached to the message itself so that protection occurs online and offline and inside and outside of your organization's firewall.</span></span>
  
<span data-ttu-id="e5b12-p106">사용자는 받는 사람에 게 메시지에 대 한 사용 권한을 제어 하는 전자 메일 메시지에 서식 파일을 적용할 수 있습니다. 메시지에는 AD RMS 권한 정책을 적용 하 여 착신 전환, 메시지에서 정보를 추출, 메시지를 저장 하거나 메시지를 인쇄 하는 등의 작업을 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p106">Users can apply a template to an email message to control the permissions that recipients have on a message. Actions, such as forwarding, extracting information from a message, saving a message or printing a message can be controlled by applying an AD RMS rights policy to the message.</span></span>
  
<span data-ttu-id="e5b12-p107">Windows Server 2008 이상을 실행 하는 AD RMS 서버를 사용 하 여 IRM을 구성할 수 있습니다. 클라우드 기반 조직에 대 한 AD RMS 권한 정책 서식 파일을 관리 하려면 AD RMS 서버를 사용할 수 있습니다. Outlook는 또한 사용자가 메시지를 보낼 때에 IRM 보호를 적용할 수 있도록 AD RMS 서버에 사용 합니다. 자세한 내용은 참조 [온-프레미스를 사용 하 여 IRM 구성 AD RMS 서버](configure-irm-to-use-an-on-premises-ad-rms-server.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p107">You can configure IRM to use an AD RMS server running Windows Server 2008 or later. You can use this AD RMS server to manage the AD RMS rights policy templates for your cloud-based organization. Outlook also relies on the AD RMS server to enable users to apply IRM protection to messages they send. For details, see [Configure IRM to use an on-premises AD RMS server](configure-irm-to-use-an-on-premises-ad-rms-server.md).</span></span> 
  
<span data-ttu-id="e5b12-126">IRM을 사용하도록 설정한 후에는 다음과 같이 메시지에 IRM 보호를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-126">After it's enabled, IRM protection can be applied to messages as follows:</span></span>
  
- <span data-ttu-id="e5b12-p108">**사용자 Outlook 및 웹에서 Outlook을 사용 하 여 서식 파일을 수동으로 적용할 수 있습니다.** 사용자 **사용 권한 설정** 목록에서 서식 파일을 선택 하 여 전자 메일 메시지에 AD RMS 권한 정책 서식 파일을 적용할 수 있습니다. 사용자는 IRM으로 보호 된 메시지를 보낼 때 지원 되는 형식을 사용 하는 모든 첨부 파일 메시지와 동일한 IRM 보호를 받을 수도 있습니다. Word, Excel 및 PowerPoint으로.xps 파일 및 연결 된 전자 메일 메시지와 연결 된 파일에 IRM 보호 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p108">**Users can manually apply a template using Outlook and Outlook on the web.** Users can apply an AD RMS rights policy template to an email message by selecting the template from the **Set permissions** list. When users send an IRM-protected message, any attached files that use a supported format also receive the same IRM protection as the message. IRM protection is applied to files associated with Word, Excel, and PowerPoint, as well as .xps files and attached email messages.</span></span> 
    
- <span data-ttu-id="e5b12-p109">**관리자 전송 보호 규칙을 사용 하 여 Outlook과 웹에서 Outlook에 IRM 보호를 자동으로 적용할 수 있습니다.** IRM 보호 메시지를 전송 보호 규칙을 만들 수 있습니다. 규칙 조건에 맞는 메시지에 AD RMS 권한 정책 템플릿을 적용 하려면 전송 보호 규칙 동작을 구성 합니다. IRM을 사용 하도록 설정한 후 조직의 AD RMS 권한 정책 템플릿 **적용 권한 보호 된 메시지를**호출 하는 전송 보호 규칙 작업을 사용 하 여 사용할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p109">**Administrators can use transport protection rules to apply IRM protection automatically to both Outlook and Outlook on the web.** You can create transport protection rules to IRM-protect messages. Configure the transport protection rule action to apply an AD RMS rights policy template to messages that meet the rule condition. After you enable IRM, your organization's AD RMS rights policy templates are available to use with the transport protection rule action called **Apply rights protection to the message with**.</span></span>
    
- <span data-ttu-id="e5b12-p110">**관리자 Outlook 보호 규칙을 만들 수 있습니다.** Outlook 보호 규칙은 메시지를를 보낸 사용자는 보낸 사람의 부서를 포함 하는 메시지 조건에 따라 Outlook 2010 (하지 웹에 있는 Outlook)의 메시지에 IRM 보호를 자동으로 적용 하 고 내부 또는 외부 받는 사람에 게 표시 되는 인지 대화 조직입니다. 자세한 내용은 [Outlook 보호 규칙 만들기](http://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5b12-p110">**Administrators can create Outlook protection rules.** Outlook protection rules automatically apply IRM-protection to messages in Outlook 2010 (not Outlook on the web) based on message conditions that include the sender's department, who the message is sent to, and whether recipients are inside or outside your organization. For details, see [Create an Outlook Protection Rule](http://technet.microsoft.com/library/da64750d-faaf-44de-ad8c-888eba7fbdbf.aspx).</span></span>
    

