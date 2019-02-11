---
title: Office 365 메시지 암호화 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Office 365에서 새 메시지 보호 기능이 작동 하는 방법에 대 한 질문이 있습니까? 여기에 대 한 답변을 확인 합니다.
ms.openlocfilehash: e35495106b44ccb566f4da743264def8c7d4f96f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696272"
---
# <a name="office-365-message-encryption-faq"></a><span data-ttu-id="ac1cf-104">Office 365 메시지 암호화 FAQ</span><span class="sxs-lookup"><span data-stu-id="ac1cf-104">Office 365 Message Encryption FAQ</span></span>

<span data-ttu-id="ac1cf-p102">Office 365에서 새 메시지 보호 기능이 작동 하는 방법에 대 한 질문이 있습니까? 여기에 대 한 답변을 확인 합니다. 또한 살펴보려면 [질문과 대답 (영문) Azure 정보 보호의 데이터 보호 기능에 대 한](https://docs.microsoft.com/information-protection/get-started/faqs-rms) 데이터 보호 서비스, Azure 권한 관리에 대 한 질문에 대 한 대답 Azure 정보 보호에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p102">Have a question about how the new message protection capabilities in Office 365 work? Check for an answer here. Also, take a look at [Frequently asked questions about data protection in Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/faqs-rms) for answers to questions about the data protection service, Azure Rights Management, in Azure Information Protection.</span></span>

||
|:-----|
|<span data-ttu-id="ac1cf-p103">이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 ITPros 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||
  
## <a name="what-is-office-365-message-encryption-ome"></a><span data-ttu-id="ac1cf-111">Office 365 메시지 암호화 (OME) 이란?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-111">What is Office 365 Message Encryption (OME)?</span></span>

<span data-ttu-id="ac1cf-p104">OME 전자 메일 암호화 및 권한 관리 기능을 결합합니다. 권한 관리 기능은 Azure 정보 보호에서 전원을 공급 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p104">OME combines email encryption and rights management capabilities. Rights management capabilities are powered by Azure Information Protection.</span></span>
  
## <a name="who-can-use-ome"></a><span data-ttu-id="ac1cf-114">OME를 사용할 수 있는 사람?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-114">Who can use OME?</span></span>

<span data-ttu-id="ac1cf-115">다음과 같은 조건에서는 OME에 대 한 새로운 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-115">You can use the new capabilities for OME under the following conditions:</span></span>
  
- <span data-ttu-id="ac1cf-116">Office 365의 Exchange Online에 대 한 OME 또는 IRM을 설정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-116">If you have never set up OME or IRM for Exchange Online in Office 365.</span></span>
    
- <span data-ttu-id="ac1cf-117">OME 및 IRM을 설정한 경우에 Azure 정보 보호에서 Azure 권한 관리 서비스를 사용 하는 경우 다음이 단계를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-117">If you have set up OME and IRM, you can use these steps if you are using the Azure Rights Management service from Azure Information Protection.</span></span>
    
- <span data-ttu-id="ac1cf-p105">Exchange Online Active Directory Rights Management 서비스 (AD RMS)를 사용할 경우 즉시 이러한 새 기능을 활성화할 수 없습니다. 대신, 해야 [Azure 정보 보호 AD RMS를](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) 마이그레이션하려면 먼저. 마이그레이션을 완료 한 경우에 OME를 성공적으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p105">If you are using Exchange Online with Active Directory Rights Management service (AD RMS), you can't enable these new capabilities right away. Instead, you need to [migrate AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) first. When you've finished the migration, you can successfully set up OME.</span></span> 
    
    <span data-ttu-id="ac1cf-121">계속 사용 하려는 경우 온-프레미스 AD RMS Exchange Online과 Azure 정보 보호로 마이그레이션하는 대신, 됩니다 이러한 새 기능을 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-121">If you choose to continue to use on-premises AD RMS with Exchange Online instead of migrating to Azure Information Protection, you will not be able to use these new capabilities.</span></span>
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a><span data-ttu-id="ac1cf-122">새 OME 기능을 사용 하 여 어떤 구독을 필요 합니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-122">What subscriptions do I need to use the new OME capabilities?</span></span>

<span data-ttu-id="ac1cf-123">새 OME 기능을 사용 하려면 필요한 다음 계획 중 하나:</span><span class="sxs-lookup"><span data-stu-id="ac1cf-123">To use the new OME capabilities, you need one of the following plans:</span></span>
  
- <span data-ttu-id="ac1cf-p106">Office 365 메시지 암호화는 Office 365 E3 및 e 5, Microsoft E3 및 e 5, Office 365 A1, a 3 및 A5, 및 Office 365 G3 / g 5의 일부분으로 제공 됩니다. 고객은 Azure 정보 보호 구동 되는 새 보호 기능을 수신 하기 위한 추가 라이선스를 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p106">Office 365 Message Encryption is offered as part of Office 365 E3 and E5, Microsoft E3 and E5, Office 365 A1, A3, and A5, and Office 365 G3 and G5. Customers do not need additional licenses to receive the new protection capabilities powered by Azure Information Protection.</span></span> 
    
- <span data-ttu-id="ac1cf-126">다음에 Azure 정보 보호 계획 1 새로운 Office 365 메시지 암호화 기능을 수신 하도록 계획을 추가할 수도 있습니다: Exchange Online 계획 1 "," Exchange Online 계획 2 "," Office 365 F1 "," Office 365 비즈니스 Essentials "," Office 365 프리미엄, 또는 Office 365 Enterprise E1 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-126">You can also add Azure Information Protection Plan 1 to the following plans to receive the new Office 365 Message Encryption capabilities: Exchange Online Plan 1, Exchange Online Plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium, or Office 365 Enterprise E1.</span></span>
    
- <span data-ttu-id="ac1cf-127">Office 365 메시지 암호화에서 이점의 각 사용자 기능에 의해 표시할 사용이 허가 되도록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-127">Each user benefiting from Office 365 Message Encryption needs to be licensed to be covered by the feature.</span></span>
    
- <span data-ttu-id="ac1cf-128">전체 목록은 Office 365 메시지 암호화에 대 한 [Exchange Online 서비스 설명](https://technet.microsoft.com/library/exchange-online-service-description.aspx) 을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-128">For the full list see the [Exchange Online service descriptions](https://technet.microsoft.com/library/exchange-online-service-description.aspx) for Office 365 Message Encryption.</span></span> 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a><span data-ttu-id="ac1cf-129">사용할 수 있는 Exchange Online으로 Azure 정보 보호에 직접 키 (BYOK)를 가져올?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-129">Can I use Exchange Online with bring your own key (BYOK) in Azure Information Protection?</span></span>

<span data-ttu-id="ac1cf-p107">예! OME를 설정 하기 전에 BYOK를 설정 하는 단계를 완료 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p107">Yes! Microsoft recommends that you complete the steps to set up BYOK before you set up OME.</span></span>
  
<span data-ttu-id="ac1cf-132">BYOK 하는 방법에 대 한 자세한 내용은 [계획 및 구현 하 여 Azure 정보 보호 테 넌 트 키를](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-132">For more information about BYOK, see [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).</span></span>
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a><span data-ttu-id="ac1cf-133">OME 및 Azure 정보 보호와 BYOK 변경 하려면 Microsoft의 접근 방식 subpoenas 예: 제 3 자 데이터 요청에?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-133">Do OME and BYOK with Azure Information Protection change Microsoft's approach to third-party data requests such as subpoenas?</span></span>

<span data-ttu-id="ac1cf-p108">아니요. OME 및 옵션을 제공 하 고 컨트롤 Azure 정보 보호에서 BYOK, 호출을 직접 암호화 키를 된 법률 적용 subpoenas에 응답 하도록 설계 되지 않았습니다. Azure 정보 보호에 대 한 BYOK와 OME 준수 중심 고객을 위해 설계 되었습니다. Microsoft는 매우 심각 하 게 고객 데이터에 대 한 타사 요청을 수행합니다. 클라우드 서비스 공급자로 항상 담당 고객 데이터의 개인정보 보호 합니다. 이벤트는 이벤트에 모두를 소환장 적용 됩니까, 제 3 자 정보를 가져올 고객에 게 착신 전환 하려고 항상 했습니다. (Brad Smith의 블로그 (영문)를 참조 하십시오: [정부 스누핑의 고객 데이터를 보호](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). 주기적으로 접수 요청의 자세한 정보를 게시 합니다. 타사 데이터 요청에 대 한 자세한 내용은 Microsoft 보안 센터에서 [정부 및 고객 데이터에 액세스 하는 법률 적용 요청에 응답](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) 을 참조 하십시오. 또한, "공개 고객에서에서 데이터의" [온라인 서비스 약관 (OST)를](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p108">No. OME and the option to provide and control your own encryption keys, called BYOK, from Azure Information Protection were not designed to respond to law enforcement subpoenas. OME, with BYOK for Azure Information Protection, was designed for compliance-focused customers. Microsoft takes third-party requests for customer data very seriously. As a cloud service provider, we always advocate for the privacy of customer data. In the event we get a subpoena, we always attempt to redirect the third party to the customer to obtain the information. (Please read Brad Smith's blog: [Protecting customer data from government snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). We periodically publish detailed information of the request we receive. For more information regarding third-party data requests, see [Responding to government and law enforcement requests to access customer data](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) on the Microsoft Trust Center. Also, see "Disclosure of Customer Data" in the [Online Services Terms (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).</span></span>
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a><span data-ttu-id="ac1cf-144">이 기능은 기존 Office 365 메시지 암호화 (OME) 및 정보 권한 관리 (IRM) 기능 관련이 있습니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-144">How is this feature related to legacy Office 365 Message Encryption (OME) and Information Rights Management (IRM) features?</span></span>

<span data-ttu-id="ac1cf-p109">기존 IRM 및 레거시 OME 솔루션의 발전은 Office 365 메시지 암호화에 대 한 새 기능을. 다음 표에서 자세한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p109">The new capabilities for Office 365 Message Encryption are an evolution of the existing IRM and legacy OME solutions. The following table provides more details.</span></span>
  
<span data-ttu-id="ac1cf-147">**레거시 OME, IRM, 및 새 OME 기능 비교**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-147">**Comparison of legacy OME, IRM, and new OME capabilities**</span></span>

|<span data-ttu-id="ac1cf-148">**기능**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-148">**Capability**</span></span>|<span data-ttu-id="ac1cf-149">**이전 버전의 OME**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-149">**Previous versions of OME**</span></span>|<span data-ttu-id="ac1cf-150">**IRM**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-150">**IRM**</span></span>|<span data-ttu-id="ac1cf-151">**새 OME 기능**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-151">**New OME capabilities**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ac1cf-152">**암호화 된 전자 메일 보내기**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-152">**Sending an encrypted email**</span></span>|<span data-ttu-id="ac1cf-153">Exchange 메일 흐름 규칙을 통해만</span><span class="sxs-lookup"><span data-stu-id="ac1cf-153">Only through Exchange mail flow rules</span></span>|<span data-ttu-id="ac1cf-154">PC, Outlook for Mac, 또는; 웹에서 Outlook에 대 한 Outlook에서 시작 하는 최종 사용자 Exchange를 통해 메일 흐름 규칙 또는</span><span class="sxs-lookup"><span data-stu-id="ac1cf-154">End-user initiated from Outlook for PC, Outlook for Mac, or Outlook on the web; or through Exchange mail flow rules</span></span>|<span data-ttu-id="ac1cf-155">PC, Outlook for Mac, 또는; 웹에서 Outlook에 대 한 Outlook에서 시작 하는 최종 사용자 메일 흐름 규칙을 통해 또는</span><span class="sxs-lookup"><span data-stu-id="ac1cf-155">End-user initiated from Outlook for PC, Outlook for Mac, or Outlook on the web; or through mail flow rules</span></span>|
|<span data-ttu-id="ac1cf-156">**권한 관리**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-156">**Rights management**</span></span>|-|<span data-ttu-id="ac1cf-157">착신 전환 옵션을 사용자 지정 서식 파일</span><span class="sxs-lookup"><span data-stu-id="ac1cf-157">Do Not Forward option and custom templates</span></span>|<span data-ttu-id="ac1cf-158">착신 전환 옵션, 암호화 전용 옵션, 기본 및 사용자 지정 서식 파일을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-158">Do Not Forward option, encrypt-only option, default and custom templates</span></span>|
|<span data-ttu-id="ac1cf-159">**지원 되는 받는 사람 유형**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-159">**Supported recipient type**</span></span>|<span data-ttu-id="ac1cf-160">외부 받는 사람</span><span class="sxs-lookup"><span data-stu-id="ac1cf-160">External recipients only</span></span>|<span data-ttu-id="ac1cf-161">내부 받는 사람</span><span class="sxs-lookup"><span data-stu-id="ac1cf-161">Internal recipients only</span></span>|<span data-ttu-id="ac1cf-162">내부 및 외부의 받는 사람</span><span class="sxs-lookup"><span data-stu-id="ac1cf-162">Internal and external recipients</span></span>|
|<span data-ttu-id="ac1cf-163">**받는 사람에 대 한 환경**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-163">**Experience for recipient**</span></span>|<span data-ttu-id="ac1cf-164">외부 받는 사람에 게는 자신이 다운로드 하 고 브라우저에서 열 또는 모바일 응용 프로그램을 다운로드 하는 HTML 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-164">External recipients received an HTML message that they downloaded and opened in a browser or downloaded mobile app.</span></span>|<span data-ttu-id="ac1cf-165">내부 받는 사람에 게 PC에 대 한 Outlook, Outlook for Mac, 및 웹에 있는 Outlook에서 암호화 된 전자 메일을 수신 하는 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-165">Internal recipients only received encrypted email in Outlook for PC, Outlook for Mac, and Outlook on the web.</span></span>|<span data-ttu-id="ac1cf-p110">내부 및 외부 받는 사람에 게 iOS, 또는 모든 Office 365 또는 같은 Office 365 조직에는 여부에 관계 없이 웹 포털을 통해 PC에 대 한 Outlook, Outlook for Mac, 웹에 있는 Outlook, Android, Outlook 및 Outlook에서 전자 메일을 수신 조직입니다. OME 포털에는 별도 다운로드 없음 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p110">Internal and external recipients receive email in Outlook for PC, Outlook for Mac, Outlook on the web, Outlook for Android, and Outlook for iOS, or through a web portal, regardless of whether or not they are in the same Office 365 organization or in any Office 365 organization. The OME portal requires no separate download.</span></span>|
|<span data-ttu-id="ac1cf-168">**사용자 고유의 키 지원 가져오기**</span><span class="sxs-lookup"><span data-stu-id="ac1cf-168">**Bring Your Own Key support**</span></span>|<span data-ttu-id="ac1cf-169">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="ac1cf-169">Not available</span></span>|<span data-ttu-id="ac1cf-170">사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="ac1cf-170">Not available</span></span>| <span data-ttu-id="ac1cf-171">BYOK 지원</span><span class="sxs-lookup"><span data-stu-id="ac1cf-171">BYOK supported</span></span>|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a><span data-ttu-id="ac1cf-172">내 조직에 대 한 새 OME 기능을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ac1cf-172">How do I enable the new OME capabilities for my organization?</span></span>

<span data-ttu-id="ac1cf-173">[새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-173">See [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md).</span></span>
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a><span data-ttu-id="ac1cf-174">이전 버전의 OME 되지 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-174">Will the previous version of OME be deprecated?</span></span>

<span data-ttu-id="ac1cf-p111">이전 버전의 OME 사용할 수 있습니다, 지금은 하지 사용 되지 않습니다. 그러나 매우 문서의 내용도 새롭고 향상 된 OME 솔루션을 사용 하는 조직입니다. OME 아직 배포 하지 않은 고객은 OME의 이전 버전의 새로운 배포를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p111">You can still use the previous version of OME, it will not be deprecated at this time. However, we highly encourage organizations to use the new and improved OME solution. Customers that have not already deployed OME cannot set up a new deployment of the previous version of OME.</span></span>
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a><span data-ttu-id="ac1cf-178">내 조직 Active Directory 권한 관리를 사용 하 여,이 기능은 사용할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-178">My organization uses Active Directory Rights Management, can I use this functionality?</span></span>

<span data-ttu-id="ac1cf-p112">아니요. Exchange Online Active Directory Rights Management 서비스 (AD RMS)를 사용할 경우 즉시 이러한 새 기능을 활성화할 수 없습니다. 대신, 해야 [Azure 정보 보호 AD RMS를](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) 마이그레이션하려면 먼저.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p112">No. If you are using Exchange Online with Active Directory Rights Management service (AD RMS), you can't enable these new capabilities right away. Instead, you need to [migrate AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) first.</span></span> 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a><span data-ttu-id="ac1cf-p113">내 조직에 Exchange 하이브리드 배포 합니다. 이 기능을 사용할 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p113">My organization has an Exchange Hybrid deployment. Can I use this feature?</span></span>

<span data-ttu-id="ac1cf-p114">온-프레미스 사용자는 Exchange Online 메일 흐름 규칙을 사용 하 여 암호화 된 메일을 보낼 수 있습니다. 이 작업을 수행 하기 위해 Exchange Online을 통해 전자 메일을 라우팅할 해야 합니다. 자세한 내용은 참조 [제 2 부: 메일을 Office 365로 전자 메일 서버에서 전송 구성](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365)합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p114">On-premises users can send encrypted mail using Exchange Online mail flow rules. In order to do this, you need to route email through Exchange Online. For more information, see [Part 2: Configure mail to flow from your email server to Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365).</span></span>
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a><span data-ttu-id="ac1cf-p115">OME 암호화 된 메시지를 작성 하기 위해 사용 하 여 어떤 전자 메일 클라이언트를 필요 합니까? 보호 된 메시지를 보내는 어떤 응용 프로그램은 지원 합니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p115">What email client do I need to use in order to create an OME encrypted message? What applications are supported for sending protected messages?</span></span>

<span data-ttu-id="ac1cf-189">웹에 있는 Outlook 및 Outlook 2016 및 PC 및 Mac, Outlook 2013에서 보호 된 메시지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-189">You can create protected messages from Outlook 2016, and Outlook 2013 for PC and Mac, and from Outlook on the web.</span></span>
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a><span data-ttu-id="ac1cf-190">어떤 전자 메일 클라이언트를 읽고 보호 된 전자 메일에 회신 지원 됩니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-190">What email clients are supported to read and reply to protected emails?</span></span>

<span data-ttu-id="ac1cf-p116">읽을 수 있으며 Office 365 사용자의 경우 (Android 및 iOS) PC 및 Mac (2013 및 2016), 웹, Outlook 및 Outlook 모바일 Outlook에서 응답할 수 있습니다. 조직에서 허용 하는 경우에 iOS 기본 메일 클라이언트를 사용할 수 있습니다. Office 365가 아닌 사용자 인 경우 읽기 및 웹 브라우저를 통해 웹에서 암호화 된 메시지를 회신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p116">You can read and respond from Outlook for PC and Mac (2013 and 2016), Outlook on the web, and Outlook mobile (Android and iOS) if you are an Office 365 user. You can also use the iOS native mail client if your organization allows it. If you are a non-Office 365 user, you can read and reply to encrypted messages on the web through your web browser.</span></span>
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a><span data-ttu-id="ac1cf-p117">보호 된 전자 메일의 첨부 파일로 파일 유형은 지원 됩니까? 첨부 파일에 전자 메일을 보호와 관련 된 보호 정책을 상속 수행?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p117">What file types are supported as attachments in protected emails? Do attachments inherit the protection policies associated with protected emails?</span></span>

<span data-ttu-id="ac1cf-196">보호 정책은 파일 형식에서 언급 한 [여기](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types)에 적용 되는 않지만 모든 파일 형식을 제한 된 메일에 첨부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-196">You can attach any file type to a protected mail, however protection policies are applied only on the file formats mentioned [here](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types).</span></span> 
  
<span data-ttu-id="ac1cf-p118">예: Word, Excel 또는 PowerPoint 파일을 파일 형식 지원 되는 경우 파일은 항상 받는 사람이 첨부 파일 다운로드 한 후에 보호 됩니다. 예, 첨부 파일은 전달 하지 않음에 의해 보호 하 고 원래 받는 사람을 다운로드 하 여 새 받는 사람에 게 첨부 파일을 전달 하는 경우 새 받는 사람 보호 된 파일을 열 수 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p118">If a file format is supported, such as a Word, Excel, or PowerPoint file, the file is always protected, even after the attachment has been downloaded by the recipient. For example, if an attachment is protected by Do Not Forward, and the original recipient downloads and forwards the attachment to a new recipient, the new recipient will not be able to open the protected file.</span></span>
  
## <a name="are-pdf-file-attachments-supported"></a><span data-ttu-id="ac1cf-199">PDF 파일 첨부 파일이 지원 됩니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-199">Are PDF file attachments supported?</span></span>

<span data-ttu-id="ac1cf-p119">보호 된 메시지를 PDF 파일을 첨부 하는 경우 메시지 자체를 보호할 수 있습니다 있지만 추가 보호 없이 받는 것 받은 후 PDF 파일에 적용 됩니다. 즉, 다른 이름으로 저장 하는 받는 사람 수, 앞으로, 복사 및 PDF 파일을 인쇄 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p119">If you attach a PDF file to a protected message, the message itself will be protected, but no additional protection will be applied to the PDF file after the recipient has received it. This means that the recipient can Save As, Forward, Copy, and Print the PDF file.</span></span>
  
## <a name="are-onedrive-for-business-attachments-supported"></a><span data-ttu-id="ac1cf-202">지원 되는 비즈니스 첨부 파일을 위한 OneDrive 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-202">Are OneDrive for Business attachments supported?</span></span>

<span data-ttu-id="ac1cf-p120">아직 아니에요. OneDrive 비즈니스 첨부 파일에 대 한 지원 되지 않으며 최종 사용자에 게 비즈니스 첨부 파일에 대 한 클라우드 OneDrive 포함 된 메일을 암호화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p120">Not yet. OneDrive for Business attachments are not supported and end-users can't encrypt a mail that contains a cloud OneDrive for Business attachment.</span></span>
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a><span data-ttu-id="ac1cf-205">I 자동으로 메시지를 암호화할 수 정책을 설정 하 여?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-205">Can I automatically encrypt messages by setting up policies?</span></span>

<span data-ttu-id="ac1cf-p121">예입니다. 사용 하 여 메일 흐름 규칙 Exchange Online을 자동으로 특정 조건에 따라 메시지를 암호화 합니다. 예, 받는 사람에 기반 하는 정책을 만들 수 있습니다 ID, 받는 사람 도메인 또는 본문 또는 메시지의 제목에 콘텐츠에 합니다. 참조 [Office 365에서 전자 메일 메시지를 암호화 하는 메일 흐름 규칙을 정의 합니다.](define-mail-flow-rules-to-encrypt-email.md)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p121">Yes. Use mail flow rules in Exchange Online to automatically encrypt a message based on certain conditions. For example, you can create policies that are based on recipient ID, recipient domain, or on the content in the body or subject of the message. See [Define mail flow rules to encrypt email messages in Office 365.](define-mail-flow-rules-to-encrypt-email.md)</span></span>
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a><span data-ttu-id="ac1cf-210">I 자동으로 메시지를 암호화할 수 정책에서 데이터 손실 방지 (DLP) 보안을 통해을 설정 하 여 &amp; 준수 센터?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-210">Can I automatically encrypt messages by setting up policies in Data Loss Prevention (DLP) through the Security &amp; Compliance Center?</span></span>

<span data-ttu-id="ac1cf-p122">예! Exchange Online에서 또는 보안에서 DLP를 사용 하 여 메일 흐름 규칙을 설정할 수 &amp; 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p122">Yes! You can set up mail flow rules in Exchange Online or by using DLP in the Security &amp; Compliance Center.</span></span>
  
## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a><span data-ttu-id="ac1cf-213">공유 사서함에 전송 된 암호화 된 메시지를 열 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-213">Can I open encrypted messages sent to a Shared Mailbox?</span></span>

<span data-ttu-id="ac1cf-214">공유 사서함에 대 한 현재 암호화 된 메시지를 사용 하는 것이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-214">Currently encrypted messages are not supported for a Shared Mailbox.</span></span>

## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a><span data-ttu-id="ac1cf-215">사용자 지정 하는 암호화 된 메시지 브랜딩 내 회사와?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-215">Can I customize encrypted messages with my company branding?</span></span>

<span data-ttu-id="ac1cf-p123">예! 전자 메일 메시지와 OME 포털을 사용자 지정에 대 한 자세한 내용은 참조 하십시오. 조직의 브랜드를 암호화 된 메시지에 추가 합니다. 참조 [조직의 브랜드 암호화 된 메시지에 추가할.](add-your-organization-brand-to-encrypted-messages.md)</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p123">Yes! For information on customizing email messages and the OME portal, see Add your organization's brand to your encrypted messages. See [Add your organization's brand to your encrypted messages.](add-your-organization-brand-to-encrypted-messages.md)</span></span>
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a><span data-ttu-id="ac1cf-219">모든 보고 기능 또는 암호화 된 전자 메일에 대 한 통찰력 있는?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-219">Are there any reporting capabilities or insights for encrypted emails?</span></span>

<span data-ttu-id="ac1cf-220">이 시간이 더 길지만 출시 예정에 있지.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-220">Not at this time but coming soon.</span></span>
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a><span data-ttu-id="ac1cf-221">메시지 암호화를 사용 하 여 eDiscovery 등의 규정 준수 기능와 수 있습니까?</span><span class="sxs-lookup"><span data-stu-id="ac1cf-221">Can I use message encryption with compliance features such as eDiscovery?</span></span>

<span data-ttu-id="ac1cf-p124">예입니다. 모든 암호화 된 전자 메일 메시지는 Office 365 규정 준수 기능 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac1cf-p124">Yes. All encrypted email messages are discoverable by Office 365 compliance features.</span></span>
  

