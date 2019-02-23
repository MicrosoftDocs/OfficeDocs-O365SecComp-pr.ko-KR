---
title: 온-프레미스 AD RMS 서버를 사용 하도록 IRM 구성
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/13/2017
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3ecde857-4b7c-451d-b4aa-9eeffc8a8c61
ms.collection:
- M365-security-compliance
description: 이 항목에서는 AD RMS 서버를 사용하도록 IRM을 구성하는 방법을 보여줍니다.
ms.openlocfilehash: 19d353dc8aa0e02b564616aacdde31c0fffa0483
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215259"
---
# <a name="configure-irm-to-use-an-on-premises-ad-rms-server"></a><span data-ttu-id="f77f3-103">온-프레미스 AD RMS 서버를 사용하도록 IRM 구성</span><span class="sxs-lookup"><span data-stu-id="f77f3-103">Configure IRM to use an on-premises AD RMS server</span></span>
  
<span data-ttu-id="f77f3-p101">온-프레미스 배포와 함께 사용 하는 경우 Exchange Online의 IRM (정보 권한 관리)은 Windows Server 2008 이상에서 정보 보호 기술인 AD RMS (Active Directory Rights management Services)를 사용 합니다. IRM 보호는 전자 메일 메시지에 AD RMS 권한 정책 템플릿을 적용 하 여 전자 메일에 적용 됩니다. 권한은 메시지 자체에 첨부 되므로 보호가 온라인 및 오프 라인 상태이 고 조직의 방화벽 내부 및 외부에서 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p101">For use with on-premises deployments, Information Rights Management (IRM) in Exchange Online uses Active Directory Rights Management Services (AD RMS), an information protection technology in Windows Server 2008 and later. IRM protection is applied to email by applying an AD RMS rights policy template to an email message. Rights are attached to the message itself so that protection occurs online and offline and inside and outside of your organization's firewall.</span></span>
  
<span data-ttu-id="f77f3-p102">이 항목에서는 AD RMS 서버를 사용 하도록 IRM을 구성 하는 방법을 보여 줍니다. azure Active Directory 및 azure 권한 관리에서 office 365 메시지 암호화에 대 한 새로운 기능을 사용 하는 방법에 대 한 자세한 내용은 [office 365 메시지 암호화 FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p102">This topic shows you how to configure IRM to use an AD RMS server. For information about using the new capabilities for Office 365 Message Encryption with Azure Active Directory and Azure Rights Management, see the [Office 365 Message Encryption FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).</span></span>
  
<span data-ttu-id="f77f3-109">Exchange Online의 IRM에 대한 자세한 내용은 [Exchange Online의 정보 권한 관리](information-rights-management-in-exchange-online.md)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-109">To learn more about IRM in Exchange Online, see [Information Rights Management in Exchange Online](information-rights-management-in-exchange-online.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f77f3-110">시작하기 전에 알아야 할 내용</span><span class="sxs-lookup"><span data-stu-id="f77f3-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="f77f3-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f77f3-111"></span></span>

- <span data-ttu-id="f77f3-112">이 작업의 예상 완료 시간: 30분</span><span class="sxs-lookup"><span data-stu-id="f77f3-112">Estimated time to complete this task: 30 minutes</span></span>
    
- <span data-ttu-id="f77f3-p103">이러한 절차를 수행하려면 먼저 사용 권한을 할당받아야 합니다. 필요한 사용 권한을 확인하려면 다음을 참조하세요. [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx)의 "정보 권한 관리" 항목</span><span class="sxs-lookup"><span data-stu-id="f77f3-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Information Rights Management" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="f77f3-p104">AD RMS 서버에서 Windows Server 2008 이상이 실행되고 있어야 합니다. AD RMS 배포 방법에 대한 자세한 내용은 [AD RMS 클러스터 설치](https://go.microsoft.com/fwlink/?LinkId=210873)를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p104">The AD RMS server must be running Windows Server 2008 or later. For details about how to deploy AD RMS, see [Installing an AD RMS Cluster](https://go.microsoft.com/fwlink/?LinkId=210873).</span></span>
    
- <span data-ttu-id="f77f3-117">Windows PowerShell을 설치 및 구성하고 서비스에 연결하는 방법에 대한 자세한 내용은 [원격 PowerShell을 사용하여 Exchange Online에 연결](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-117">For details about how to install and configure Windows PowerShell and connect to the service, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="f77f3-118">이 항목의 절차에 적용할 수 있는 바로 가기 키에 대한 자세한 내용은 **Keyboard shortcuts in Exchange 2013**을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f77f3-118">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="f77f3-p105">문제가 있습니까? Exchange 포럼에서 도움을 요청하세요. 포럼 주소는 다음과 같습니다.[Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), 또는 [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351)</span><span class="sxs-lookup"><span data-stu-id="f77f3-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="how-do-you-do-this"></a><span data-ttu-id="f77f3-122">어떻게 해야 합니까?</span><span class="sxs-lookup"><span data-stu-id="f77f3-122">How do you do this?</span></span>
<span data-ttu-id="f77f3-123"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="f77f3-123"></span></span>

### <a name="step-1-use-the-ad-rms-console-to-export-a-trusted-publishing-domain-tpd-from-an-ad-rms-server"></a><span data-ttu-id="f77f3-124">1단계: AD RMS 콘솔을 사용하여 AD RMS 서버에서 TPD(트러스트된 게시 도메인)를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-124">Step 1: Use the AD RMS console to export a trusted publishing domain (TPD) from an AD RMS server</span></span>

<span data-ttu-id="f77f3-p106">첫 번째 단계는 온-프레미스 AD RMS 서버의 TPD(트러스트된 게시 도메인)를 XML 파일로 내보내는 것입니다. TPD에는 RMS 기능을 사용하는 데 필요한 다음과 같은 설정이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p106">The first step is to export a trusted publishing domain (TPD) from the on-premises AD RMS server to an XML file. The TPD contains the following settings needed to use RMS features:</span></span> 
  
- <span data-ttu-id="f77f3-127">인증서 및 라이선스 서명 및 암호화에 사용되는 SLC(서버 사용 허가자 인증서)</span><span class="sxs-lookup"><span data-stu-id="f77f3-127">The server licensor certificate (SLC) used for signing and encrypting certificates and licenses</span></span>
    
- <span data-ttu-id="f77f3-128">라이선스 및 게시에 사용되는 URL</span><span class="sxs-lookup"><span data-stu-id="f77f3-128">The URLs used for licensing and publishing</span></span>
    
- <span data-ttu-id="f77f3-129">해당 TPD에 대한 특정 SLC로 만들어진 AD RMS 권한 정책 템플릿</span><span class="sxs-lookup"><span data-stu-id="f77f3-129">The AD RMS rights policy templates that were created with the specific SLC for that TPD</span></span>
    
<span data-ttu-id="f77f3-130">TPD를 가져오면 해당 TPD가 Exchange Online에 저장되고 보호됩니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-130">When you import the TPD, it's stored and protected in Exchange Online.</span></span>
  
1. <span data-ttu-id="f77f3-131">Active Directory Rights Management Services 콘솔을 연 다음 AD RMS 클러스터를 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-131">Open the Active Directory Rights Management Services console, and then expand the AD RMS cluster.</span></span>
    
2. <span data-ttu-id="f77f3-132">콘솔 트리에서 **트러스트 정책**을 확장한 다음 **트러스트된 게시 도메인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-132">In the console tree, expand **Trust Policies**, and then click **Trusted Publishing Domains**.</span></span>
    
3. <span data-ttu-id="f77f3-133">결과 창에서 내보낼 도메인에 대한 인증서를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-133">In the results pane, select the certificate for the domain you want to export.</span></span>
    
4. <span data-ttu-id="f77f3-134">**작업** 창에서 **트러스트된 게시 도메인 내보내기**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-134">In the **Actions** pane, click **Export Trusted Publishing Domain**.</span></span>
    
5. <span data-ttu-id="f77f3-p107">**게시 도메인 파일** 상자에서 **다른 이름으로 저장**을 클릭하여 파일을 로컬 컴퓨터의 특정 위치에 저장합니다. 파일 이름을 입력하고  `.xml` 파일 이름 확장명을 지정했는지 확인한 다음 **저장**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p107">In the **Publishing domain file** box, click **Save As** to save the file to a specific location on the local computer. Type a file name, making sure to specify the  `.xml` file name extension, and then click **Save**.</span></span>
    
6. <span data-ttu-id="f77f3-p108">**암호** 및 **암호 확인** 상자에 트러스트된 게시 도메인 파일을 암호화하는 데 사용할 강력한 암호를 입력합니다. TPD를 클라우드 기반 전자 메일 조직으로 가져올 때 이 암호를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p108">In the **Password** and **Confirm Password** boxes, type a strong password that will be used to encrypt the trusted publishing domain file. You will have to specify this password when you import the TPD to your cloud-based email organization.</span></span> 
    
### <a name="step-2-use-the-exchange-management-shell-to-import-the-tpd-to-exchange-online"></a><span data-ttu-id="f77f3-139">2 단계: exchange 관리 셸을 사용 하 여 TPD를 exchange Online으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="f77f3-139">Step 2: Use the Exchange Management Shell to import the TPD to Exchange Online</span></span>

<span data-ttu-id="f77f3-p109">TPD를 XML 파일로 내보낸 후에는 Exchange Online으로 가져와야 합니다. TPD를 가져오면 조직의 AD RMS 템플릿도 가져오게 됩니다. 첫 번째 TPD를 가져오면 해당 TPD가 클라우드 기반 조직에 대한 기본 TPD가 됩니다. 다른 TPD를 가져오는 경우 **Default** 스위치를 사용하여 TPD를 사용자가 사용할 수 있는 기본 TPD로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p109">After the TPD is exported to an XML file, you have to import it to Exchange Online. When a TPD is imported, your organization's AD RMS templates are also imported. When the first TPD is imported, it becomes the default TPD for your cloud-based organization. If you import another TPD, you can use the **Default** switch to make it the default TPD that is available to users.</span></span> 
  
<span data-ttu-id="f77f3-144">TPD를 가져오려면 Windows PowerShell에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-144">To import the TPD, run the following command in Windows PowerShell:</span></span>
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path <path to exported TPD file> -ReadCount 0)) -Name "<name of TPD>" -ExtranetLicensingUrl <URL> -IntranetLicensingUrl <URL>
```

<span data-ttu-id="f77f3-p110">Active Directory Rights Management Services 콘솔에서  _ExtranetLicensingUrl_ 및  _IntranetLicensingUrl_ 매개 변수에 대한 값을 가져올 수 있습니다. 콘솔 트리에서 AD RMS 클러스터를 선택합니다. 라이선스 URL이 결과 창에 표시됩니다. 이러한 URL은 콘텐츠의 암호를 해제해야 하는 경우와 Exchange Online에서 사용할 TPD를 결정해야 하는 경우 전자 메일 클라이언트가 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p110">You can obtain the values for the  _ExtranetLicensingUrl_ and  _IntranetLicensingUrl_ parameters in the Active Directory Rights Management Services console. Select the AD RMS cluster in the console tree. The licensing URLs are displayed in the results pane. These URLs are used by email clients when content has to be decrypted and when Exchange Online needs to determine which TPD to use.</span></span> 
  
<span data-ttu-id="f77f3-p111">이 명령을 실행하면 암호를 입력하라는 메시지가 표시됩니다. AD RMS 서버에서 TPD를 내보낼 때 지정한 암호를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p111">When you run this command, you'll be prompted for a password. Enter the password that you specified when you exported the TPD from your AD RMS server.</span></span>
  
<span data-ttu-id="f77f3-p112">예를 들어 다음 명령은 AD RMS 서버에서 내보내고 관리자 계정의 바탕 화면에 저장한 XML 파일을 사용하여 이름이 Exported TPD라는 TPD를 가져옵니다. Name 매개 변수를 사용하여 TPD에 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p112">For example, the following command imports the TPD named Exported TPD using the XML file that you exported from your AD RMS server and saved to the desktop of the Administrator account. The Name parameter is used to specify a name to the TPD.</span></span>
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path C:\Users\Administrator\Desktop\ExportTPD.xml -ReadCount 0)) -Name "Exported TPD" -ExtranetLicensingUrl https://corp.contoso.com/_wmcs/licensing -IntranetLicensingUrl https://rmsserver/_wmcs/licensing
```

<span data-ttu-id="f77f3-153">구문과 매개 변수에 대한 자세한 내용은 [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-153">For detailed syntax and parameter information, see [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx).</span></span>
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="f77f3-154">이 단계의 작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="f77f3-154">How do you know this step worked?</span></span>

<span data-ttu-id="f77f3-p113">TPD를 가져왔는지 확인하려면 **Get-RMSTrustedPublishingDomain** cmdlet을 실행하여 Exchange Online 조직에서 TPD를 검색합니다. 자세한 내용은 [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx)의 예를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p113">To verify that you have successfully imported the TPD, run the **Get-RMSTrustedPublishingDomain** cmdlet to retrieve TPDs in your Exchange Online organization. For details, see the examples in [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx).</span></span>
  
### <a name="step-3-use-the-exchange-management-shell-to-distribute-an-ad-rms-rights-policy-template"></a><span data-ttu-id="f77f3-157">3 단계: Exchange 관리 셸을 사용 하 여 AD RMS 권한 정책 템플릿을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-157">Step 3: Use the Exchange Management Shell to distribute an AD RMS rights policy template</span></span>

<span data-ttu-id="f77f3-p114">TPD를 가져온 후에는 AD RMS 권한 정책 템플릿이 배포 되었는지 확인 해야 합니다. 배포 된 서식 파일은 웹 (이전의 outlook web App) 사용자에 게 표시 되므로 전자 메일 메시지에 서식 파일을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p114">After you import the TPD, you must make sure an AD RMS rights policy template is distributed. A distributed template is visible to Outlook on the web (formerly known as Outlook Web App) users, who can then apply the templates to an email message.</span></span>
  
<span data-ttu-id="f77f3-160">기본 TPD에 포함된 모든 템플릿 목록을 반환하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-160">To return a list of all templates contained in the default TPD, run the following command:</span></span>
  
```
Get-RMSTemplate -Type All | fl
```

<span data-ttu-id="f77f3-p115">_Type_ 매개 변수의 값이 인 `Archived`경우 해당 템플릿은 사용자에 게 표시 되지 않습니다. 웹에서 Outlook에서는 기본 TPD의 배포 된 템플릿만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p115">If the value of the  _Type_ parameter is  `Archived`, the template isn't visible to users. Only distributed templates in the default TPD are available in Outlook on the web.</span></span>
  
<span data-ttu-id="f77f3-163">템플릿을 배포하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-163">To distribute a template, run the following command:</span></span>
  
```
Set-RMSTemplate -Identity "<name of the template>" -Type Distributed
```

<span data-ttu-id="f77f3-164">예를 들어 다음 명령은 Company Confidential 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-164">For example, the following command imports the Company Confidential template.</span></span>
  
```
Set-RMSTemplate -Identity "Company Confidential" -Type Distributed
```

<span data-ttu-id="f77f3-165">구문과 매개 변수에 대한 자세한 내용은 [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) 및 [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-165">For detailed syntax and parameter information, see [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) and [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx).</span></span>
  
 <span data-ttu-id="f77f3-166">**전달하지 않음 템플릿**</span><span class="sxs-lookup"><span data-stu-id="f77f3-166">**The Do Not Forward template**</span></span>
  
<span data-ttu-id="f77f3-p116">온-프레미스 조직의 기본 TPD를 Exchange Online으로 가져올 때 **전달하지 않음**이라는 하나의 AD RMS 권한 정책 템플릿을 가져옵니다. 이 템플릿은 기본 TPD를 가져올 때 기본적으로 배포됩니다. **Set-RMSTemplate** cmdlet을 사용하여 **전달하지 않음** 템플릿을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p116">When you import the default TPD from your on-premises organization into Exchange Online, one AD RMS rights policy template named **Do Not Forward** is imported. By default, this template is distributed when you import the default TPD. You can't use the **Set-RMSTemplate** cmdlet to modify the **Do Not Forward** template.</span></span> 
  
<span data-ttu-id="f77f3-p117">**전달하지 않음** 템플릿이 메시지에 적용되면 메시지에 주소가 지정되어 있는 받는 사람만 메시지를 읽을 수 있습니다. 또한 받는 사람은 다음을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p117">When the **Do Not Forward** template is applied to a message, only the recipients addressed in the message can read the message. Additionally, recipients can't do the following:</span></span> 
  
- <span data-ttu-id="f77f3-172">다른 사람에게 메시지를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-172">Forward the message to another person.</span></span>
    
- <span data-ttu-id="f77f3-173">메시지의 내용을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-173">Copy content from the message.</span></span>
    
- <span data-ttu-id="f77f3-174">메시지를 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-174">Print the message.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="f77f3-175">**전달하지 않음** 템플릿을 사용하는 경우 메시지의 정보가 수동으로 정보를 기록하는 타사 화면 캡처 프로그램, 카메라 또는 사용자에게 복사되지 않도록 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-175">The **Do Not Forward** template can't prevent information in a message from being copied with third-party screen capture programs, cameras, or users manually transcribing the information</span></span> 
  
<span data-ttu-id="f77f3-p118">온-프레미스 조직의 AD RMS 서버에 AD RMS 권한 정책 템플릿을 추가로 만들어 IRM 보호 요구 사항을 충족할 수 있습니다. AD RMS 권한 정책 템플릿을 추가로 만들 경우 다시 온-프레미스 AD RMS 서버에서 TPD를 내보낸 후 클라우드 기반 전자 메일 조직에서 해당 TPD를 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p118">You can create additional AD RMS rights policy templates on the AD RMS server in your on-premises organization to meet your IRM protection requirements. If you create additional AD RMS rights policy templates, you have to export the TPD from the on-premises AD RMS server again and refresh the TPD in the cloud-based email organization.</span></span> 
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="f77f3-178">이 단계의 작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="f77f3-178">How do you know this step worked?</span></span>

<span data-ttu-id="f77f3-p119">AD RMS 권한 정책 템플릿이 배포되었는지 확인하려면 **Get-RMSTemplate** cmdlet을 사용하여 템플릿 속성을 확인합니다. 자세한 내용은 [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx)의 예를 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p119">To verify that you have successfully distributed and AD RMS rights policy template, run the **Get-RMSTemplate** cmdlet to check the template's properties. For details, see the examples in [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx).</span></span>
  
### <a name="step-4-use-the-exchange-management-shell-to-enable-irm"></a><span data-ttu-id="f77f3-181">4 단계: Exchange 관리 셸을 사용 하 여 IRM을 사용 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="f77f3-181">Step 4: Use the Exchange Management Shell to enable IRM</span></span>

<span data-ttu-id="f77f3-182">TPD를 가져오고 AD RMS 권한 정책 템플릿을 배포했으면 다음 명령을 실행하여 클라우드 기반 전자 메일 조직에 대해 IRM을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-182">After you import the TPD and distribute an AD RMS rights policy template, run the following command to enable IRM for your cloud-based email organization.</span></span>
  
```
Set-IRMConfiguration -InternalLicensingEnabled $true
```

<span data-ttu-id="f77f3-183">구문과 매개 변수에 대한 자세한 내용은 [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx)을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-183">For detailed syntax and parameter information, see [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx).</span></span>
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="f77f3-184">이 단계의 작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="f77f3-184">How do you know this step worked?</span></span>

<span data-ttu-id="f77f3-185">IRM을 사용하도록 설정했는지 확인하려면 [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) cmdlet을 실행하여 Exchange Online 조직의 IRM 구성을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-185">To verify that you have successfully enabled IRM, run the [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) cmdlet to check IRM configuration in the Exchange Online organization.</span></span> 
  
## <a name="how-do-you-know-this-task-worked"></a><span data-ttu-id="f77f3-186">이 작업의 작동 여부는 어떻게 확인합니까?</span><span class="sxs-lookup"><span data-stu-id="f77f3-186">How do you know this task worked?</span></span>
<span data-ttu-id="f77f3-187"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="f77f3-187"></span></span>

<span data-ttu-id="f77f3-188">TPD를 가져오고 IRM을 사용하도록 설정했는지 확인하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-188">To verify that you have successfully imported the TPD and enabled IRM, do the following:</span></span>
  
- <span data-ttu-id="f77f3-p120">**Test-IRMConfiguration** cmdlet을 사용하여 IRM 기능을 테스트합니다. 자세한 내용은 [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx)의 "예 1"을 참조하십시오.</span><span class="sxs-lookup"><span data-stu-id="f77f3-p120">Use the **Test-IRMConfiguration** cmdlet to test IRM functionality. For details, see "Example 1" in [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx).</span></span>
    
- <span data-ttu-id="f77f3-191">웹의 Outlook에서 새 메시지를 작성 하 고 확장 된 메뉴 ( ![기타 옵션 아이콘](media/ITPro-EAC-MoreOptionsIcon.gif))에서 **사용 권한 설정** 옵션을 선택 하 여 IRM을 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="f77f3-191">Compose a new message in Outlook on the web and IRM-protect it by selecting **Set permissions** option from the extended menu ( ![More Options Icon](media/ITPro-EAC-MoreOptionsIcon.gif)).</span></span>
    

