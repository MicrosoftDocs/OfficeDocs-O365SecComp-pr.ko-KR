---
title: 문서 지문
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: exchange-online
localization_priority: Normal
ms.assetid: 1e0c579c-26e0-462a-a1b0-d7506dfe05fa
description: 정보 근로자 들이 조직에서 다양 한 종류의 일반적인 하루 동안 중요 한 정보를 처리 합니다. 문서 지 문은 보다 쉽게 조직 전체에서 사용 되는 표준 양식을 식별 하 여이 정보를 보호할 수 있습니다. 이 항목에서는 문서 지문과 PowerShell을 사용 하 여 하나를 만드는 방법을 개념을 설명 합니다.
ms.openlocfilehash: d73b769e7a014f2642a0fcd66cc6a500c68c46c3
ms.sourcegitcommit: 4be502d1fc6cbaef4c72d599758d51efe3a173c9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23867504"
---
# <a name="document-fingerprinting"></a><span data-ttu-id="51c7e-105">문서 지문</span><span class="sxs-lookup"><span data-stu-id="51c7e-105">Document Fingerprinting</span></span>

<span data-ttu-id="51c7e-p102">정보 근로자 들이 조직에서 다양 한 종류의 일반적인 하루 동안 중요 한 정보를 처리 합니다. 보안에서 &amp; 준수 센터, 문서 지문 보다 쉽게 조직 전체에서 사용 되는 표준 양식을 식별 하 여이 정보를 보호할 수 있습니다. 이 항목에서는 문서 지문과 PowerShell을 사용 하 여 하나를 만드는 방법을 개념을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p102">Information workers in your organization handle many kinds of sensitive information during a typical day. In the Security &amp; Compliance Center, Document Fingerprinting makes it easier for you to protect this information by identifying standard forms that are used throughout your organization. This topic describes the concepts behind Document Fingerprinting and how to create one by using PowerShell.</span></span>
  
## <a name="basic-scenario-for-document-fingerprinting"></a><span data-ttu-id="51c7e-109">문서 지문 관련 기본 시나리오</span><span class="sxs-lookup"><span data-stu-id="51c7e-109">Basic scenario for Document Fingerprinting</span></span>

<span data-ttu-id="51c7e-p103">문서 지 문은 표준 양식이 DLP 정책 규칙에 사용할 수 있는 중요 한 정보 유형으로 변환 하는 데이터 손실 방지 (DLP) 기능을입니다. 예, 빈 특허 서식 파일에 기초한 문서 지문을 만들 수 있으며 다음 감지 하는 DLP 정책 및 중요 한 콘텐츠가 포함 된 모든 보내는 특허 서식 파일에서 데이터를 입력할 블록을 만듭니다. 필요에 따라 중요 한 정보를 보낼 수 있습니다를 보낸 사람이 받는 사람 정규화는 특허를 받을 수 있는지 확인 해야 보낸사람 알리도록 [정책 팁](use-notifications-and-policy-tips.md) 을 설정할 수 있습니다. 조직에서 사용 되는 모든 텍스트 기반 폼이이 프로세스가 작동 합니다. 업로드할 수 있는 양식의 추가 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p103">Document Fingerprinting is a Data Loss Prevention (DLP) feature that converts a standard form into a sensitive information type, which you can use in the rules of your DLP policies. For example, you can create a document fingerprint based on a blank patent template and then create a DLP policy that detects and blocks all outgoing patent templates with sensitive content filled in. Optionally, you can set up [policy tips](use-notifications-and-policy-tips.md) to notify senders that they might be sending sensitive information, and the sender should verify that the recipients are qualified to receive the patents. This process works with any text-based forms used in your organization. Additional examples of forms that you can upload include:</span></span> 
  
- <span data-ttu-id="51c7e-115">정부 양식</span><span class="sxs-lookup"><span data-stu-id="51c7e-115">Government forms</span></span>
    
- <span data-ttu-id="51c7e-116">HIPAA(Health Insurance Portability and Accountability Act) 준수 양식</span><span class="sxs-lookup"><span data-stu-id="51c7e-116">Health Insurance Portability and Accountability Act (HIPAA) compliance forms</span></span>
    
- <span data-ttu-id="51c7e-117">인사 부서의 직원 정보 양식</span><span class="sxs-lookup"><span data-stu-id="51c7e-117">Employee information forms for Human Resources departments</span></span>
    
- <span data-ttu-id="51c7e-118">조직용으로 특수 작성된 사용자 지정 양식</span><span class="sxs-lookup"><span data-stu-id="51c7e-118">Custom forms created specifically for your organization</span></span>
    
<span data-ttu-id="51c7e-p104">원칙적으로 이미 조직이 특정 폼을 사용 하 여 중요 한 정보를 전송 하 여 설정 된 비즈니스 연습 합니다. 문서 지문으로 변환 하 고 해당 정책을 설정 하려면 빈 폼을 업로드 한 후의 DLP 해당 지문과 일치 하는 아웃 바운드 메일의 모든 문서를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p104">Ideally, your organization already has an established business practice of using certain forms to transmit sensitive information. After you upload an empty form to be converted to a document fingerprint and set up a corresponding policy, the DLP detects any documents in outbound mail that match that fingerprint.</span></span>
  
## <a name="how-document-fingerprinting-works"></a><span data-ttu-id="51c7e-121">문서 지문의 작동 방식</span><span class="sxs-lookup"><span data-stu-id="51c7e-121">How Document Fingerprinting works</span></span>

<span data-ttu-id="51c7e-p105">했을 때 이미 개이면 문서 실제 지문 필요는 없지만 이름을 기능에 설명 하는 하는데 도움이 됩니다. 다른 사람의 지문 고유 패턴 있는 동일한 방식으로 문서 고유 word 패턴을 포함 합니다. 파일을 업로드 하면 DLP은 문서에서 고유한 단어 패턴을 식별, 해당 패턴을 기준으로 문서 지문을 만들고 해당 문서 지문을 사용 하 여 동일한 패턴을 포함 하는 아웃 바운드 문서를 검색 합니다. 폼을 업로드 하는 이유 이거나 서식 파일의 문서 지문 가장 효율적인 종류를 만듭니다. 양식을 작성 하는 모든 사람 단어의 동일한 원래 집합을 사용 하 여 다음 문서에가 자신의 고유한 단어를 추가 합니다. 아웃 바운드 문서 암호로 보호 된 도메인이 아니고 원본 양식의 모든 텍스트가 포함 된, 있기만 DLP 문서 문서 지문과 일치 하는 경우 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p105">You've probably already guessed that documents don't have actual fingerprints, but the name helps explain the feature. In the same way that a person's fingerprints have unique patterns, documents have unique word patterns. When you upload a file, DLP identifies the unique word pattern in the document, creates a document fingerprint based on that pattern, and uses that document fingerprint to detect outbound documents containing the same pattern. That's why uploading a form or template creates the most effective type of document fingerprint. Everyone who fills out a form uses the same original set of words and then adds his or her own words to the document. As long as the outbound document isn't password protected and contains all the text from the original form, DLP can determine if the document matches the document fingerprint.</span></span>
  
<span data-ttu-id="51c7e-128">다음 예에서는 특허 서식 파일을 기준으로 문서 지문을 만들 때 수행되는 작업을 설명하지만 원하는 모든 양식을 기준으로 문서 지문을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-128">The following example shows what happens if you create a document fingerprint based on a patent template, but you can use any form as a basis for creating a document fingerprint.</span></span>
  
<span data-ttu-id="51c7e-129">**특허 서식 파일의 문서 지문과 일치하는 특허 문서의 예**</span><span class="sxs-lookup"><span data-stu-id="51c7e-129">**Example of a patent document matching a document fingerprint of a patent template**</span></span>

![Document_Fingerprinting_diagram.png](media/Document_Fingerprinting_diagram.png)
  
<span data-ttu-id="51c7e-p106">특허 서식 파일에는 필드가 빈 "특허 제목," "발명가" 및 "설명" 각각의 해당 필드에 대 한 설명-word 패턴입니다. 원래 특허 서식 파일을 업로드 하면 일반 텍스트 및 지원 되는 파일 형식 중 하나에 됩니다. DLP 변환 작은 유니코드 XML에 해당 하는 문서 지문에이 단어 패턴 파일을 나타내는 원래 텍스트와 비교 하 여 고유한 해시 값을 포함 하는 Active Directory에서 데이터 분류 파일로 저장 됩니다. (보안 조치로 원래 문서 자체는 서비스에 저장 되지 않습니다; 해시 값만 저장 됩니다 및 해시 값에서 원본 문서를 다시 구성할 수는 없습니다.) 특허 지문 DLP 정책을 사용 하 여 연결할 수 있는 중요 한 정보 유형 됩니다. DLP 정책과 비교 하 여를 연결한 후에 DLP 특허 지문과 일치 하는 문서가 포함 된 모든 아웃 바운드 전자 메일을 감지 하 고 조직의 정책에 따라 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p106">The patent template contains the blank fields "Patent title," "Inventors," and "Description" and descriptions for each of those fields—that's the word pattern. When you upload the original patent template, it's in one of the supported file types and in plain text. DLP converts this word pattern into a document fingerprint, which is a small Unicode XML file containing a unique hash value representing the original text, and the fingerprint is saved as a data classification in Active Directory. (As a security measure, the original document itself isn't stored on the service; only the hash value is stored, and the original document can't be reconstructed from the hash value.) The patent fingerprint then becomes a sensitive information type that you can associate with a DLP policy. After you associate the fingerprint with a DLP policy, DLP detects any outbound emails containing documents that match the patent fingerprint and deals with them according to your organization's policy.</span></span> 

<span data-ttu-id="51c7e-p107">예, 다음 특허를 포함 하는 보내는 메시지를 보내지 못하도록 정규 직원 수 없도록 하는 DLP 정책을 설정 하는 것이 좋습니다. DLP 특허를 검색 하 고 해당 전자 메일을 차단 하는 특허 지문을 사용 합니다. 또는 다음을 통해 필요한 비즈니스 되었기 때문에 관련 된 특허권 다른 조직에 보낼 수 있도록 법률 부서 수 있도록 하는 것이 좋습니다. 특정 부서에 DLP 정책에서 해당 부서에 대 한 예외를 만들어 중요 한 정보를 보낼 수 있도록 허용할 수 또는 업무상의 이유에 된 정책 팁을 재정의 하려면 하도록 허용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p107">For example, you might want to set up a DLP policy that prevents regular employees from sending outgoing messages containing patents. DLP will use the patent fingerprint to detect patents and block those emails. Alternatively, you might want to let your legal department to be able to send patents to other organizations because it has a business need for doing so. You can allow specific departments to send sensitive information by creating exceptions for those departments in your DLP policy, or you can allow them to override a policy tip with a business justification.</span></span>
  
### <a name="supported-file-types"></a><span data-ttu-id="51c7e-140">지원되는 파일 형식</span><span class="sxs-lookup"><span data-stu-id="51c7e-140">Supported file types</span></span>

<span data-ttu-id="51c7e-p108">문서 지 문은 전송 규칙에서 지원 되는 동일한 파일 형식을 지원 합니다. 지원 되는 파일 형식 목록에 대 한 [메일 흐름 규칙에 대 한 콘텐츠 검사를 위해 지원 되는 파일 형식](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)참조 하십시오. 파일 형식에 대 한 빠른 메모: 전송 규칙 및 지원 하지 않습니다 문서 지문.dotx 파일 형식을 Word에서 서식 파일 이기 때문에 사용자 혼란의 원인이 될 수 있습니다. 단어 "서식 파일"이 고 다른 문서 지문 항목에 표시 되 면 표준 양식 서식 파일 형식으로 설정 하는 문서를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p108">Document Fingerprinting supports the same file types that are supported in transport rules. For a list of supported file types, see [Supported file types for mail flow rule content inspection](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection). One quick note about file types: neither transport rules nor Document Fingerprinting supports the .dotx file type, which can be confusing because that's a template file in Word. When you see the word "template" in this and other Document Fingerprinting topics, it refers to a document that you have established as a standard form, not the template file type.</span></span>
  
#### <a name="limitations-of-document-fingerprinting"></a><span data-ttu-id="51c7e-145">문서 지문의 제한</span><span class="sxs-lookup"><span data-stu-id="51c7e-145">Limitations of document fingerprinting</span></span>

<span data-ttu-id="51c7e-146">문서 지 문은 다음과 같은 경우에 중요 한 정보를 검색 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-146">Document Fingerprinting won't detect sensitive information in the following cases:</span></span>
  
- <span data-ttu-id="51c7e-147">암호로 보호된 파일</span><span class="sxs-lookup"><span data-stu-id="51c7e-147">Password protected files</span></span>
    
- <span data-ttu-id="51c7e-148">이미지만 포함된 파일</span><span class="sxs-lookup"><span data-stu-id="51c7e-148">Files that contain only images</span></span>
    
- <span data-ttu-id="51c7e-149">문서 지문을 만드는 데 사용된 원본 양식의 모든 텍스트가 포함되지 않는 문서</span><span class="sxs-lookup"><span data-stu-id="51c7e-149">Documents that don't contain all the text from the original form used to create the document fingerprint</span></span>
    
## <a name="use-powershell-to-create-a-classification-rule-package-based-on-document-fingerprinting"></a><span data-ttu-id="51c7e-150">PowerShell을 사용 하 여 문서 지문을 기반으로 분류 규칙 패키지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="51c7e-150">Use PowerShell to create a classification rule package based on document fingerprinting</span></span>

<span data-ttu-id="51c7e-p109">문서 지문 보안에서 PowerShell을 사용 하 여만 만들 현재 수 &amp; 준수 센터입니다. 을 연결 하기 위해 [연결 하 고 Office 365 보안 및 규정 준수 센터 PowerShell를](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p109">Note that you can currently create a document fingerprint only by using PowerShell in the Security &amp; Compliance Center. To connect, see [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

<span data-ttu-id="51c7e-p110">DLP 분류 규칙 패키지를 사용 하 여 중요 한 콘텐츠를 검색 합니다. 문서 지문에 따라 분류 규칙 패키지를 만들려면 **새로 만들기 DlpFingerprint** 및 **새로운 DlpSensitiveInformationType** cmdlet을 사용 합니다. **새로 DlpFingerprint** 의 결과 외부 데이터 분류 규칙 저장 되지 않습니다, 때문에 항상 실행 **새로 DlpFingerprint** 하 고 **새로 만들기 DlpSensitiveInformationType** 또는 **집합 DlpSensitiveInformationType** 같은 PowerShell 세션입니다. 다음 예제에서는 C:\My Documents\Contoso Employee Template.docx 파일에 기반 하 여 새 문서 지문을 만듭니다. 동일한 PowerShell 세션에서 **새로 만들기 DlpSensitiveInformationType** cmdlet과 함께 사용할 수 있도록 새 지문을 변수로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p110">DLP uses classification rule packages to detect sensitive content. To create a classification rule package based on a document fingerprint, use the **New-DlpFingerprint** and **New-DlpSensitiveInformationType** cmdlets. Because the results of **New-DlpFingerprint** aren't stored outside the data classification rule, you always run **New-DlpFingerprint** and **New-DlpSensitiveInformationType** or **Set-DlpSensitiveInformationType** in the same PowerShell session. The following example creates a new document fingerprint based on the file C:\My Documents\Contoso Employee Template.docx. You store the new fingerprint as a variable so you can use it with the **New-DlpSensitiveInformationType** cmdlet in the same PowerShell session.</span></span> 
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Employee Template.docx" -Encoding byte -ReadCount 0
$Employee_Fingerprint = New-DlpFingerprint -FileData $Employee_Template -Description "Contoso Employee Template"
```

<span data-ttu-id="51c7e-158">C:\My Documents\Contoso Customer Information Form.docx 파일의 문서 지문을 사용하는 "Contoso Employee Confidential"이라는 새 데이터 분류 규칙을 만들어 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-158">Now, let's create a new data classification rule named "Contoso Employee Confidential" that uses the document fingerprint of the file C:\My Documents\Contoso Customer Information Form.docx.</span></span>
  
```
$Employee_Template = Get-Content "C:\My Documents\Contoso Customer Information Form.docx" -Encoding byte -ReadCount 0
$Customer_Fingerprint = New-DlpFingerprint -FileData $Customer_Form -Description "Contoso Customer Information Form"
New-DlpSensitiveInformationType -Name "Contoso Customer Confidential" -Fingerprints $Customer_Fingerprint -Description "Message contains Contoso customer information." 
```

<span data-ttu-id="51c7e-159">**Get DlpSensitiveInformationType** cmdlet을 사용 하 여 모든 DLP 데이터 분류 규칙 패키지를 찾을 수 이제 있습니다 하 고이 예제에서는 "Contoso Customer Confidential"의 일부인 데이터 분류 규칙 패키지 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-159">You can now use the **Get-DlpSensitiveInformationType** cmdlet to find all DLP data classification rule packages, and in this example, "Contoso Customer Confidential" is part of the data classification rule packages list.</span></span> 
  
<span data-ttu-id="51c7e-p111">마지막으로 "Contoso Customer Confidential" 데이터 분류 규칙 패키지 보안에서 DLP 정책에 추가 &amp; 준수 센터입니다. "ConfidentialPolicy" 라는 기존 DLP 정책 규칙을 추가 하는이 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p111">Finally, add the "Contoso Customer Confidential" data classification rule package to a DLP policy in the Security &amp; Compliance Center. This example adds a rule to an existing DLP policy named "ConfidentialPolicy".</span></span>

```
New-DlpComplianceRule -Name "ContosoConfidentialRule" -Policy "ConfidentialPolicy" -ContentContainsSensitiveInformation @{Name="Contoso Customer Confidential"} -BlockAccess $True
```

<span data-ttu-id="51c7e-p112">또한 다음 예제와 같이 데이터 분류 규칙 패키지 Exchange Online의 전송 규칙에 사용할 수 있습니다. 이 명령을 실행 하려면 먼저 [Exchange Online powershell 연결](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)을 해야 합니다. 또한 걸리는 보안에서 동기화 할 규칙 패키지에 대 한 시간에 주의 &amp; Exchange 관리 센터에 준수 센터입니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-p112">You can also use the data classification rule package in transport rules in Exchange Online, as shown in the following example. To run this command, you first need to [Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Also note that it takes time for the rule package to sync from the Security &amp; Compliance Center to the Exchange Admin Center.</span></span>
  
```
New-TransportRule -Name "Notify :External Recipient Contoso confidential" -NotifySender NotifyOnly -Mode Enforce -SentToScope NotInOrganization -MessageContainsDataClassification @{Name=" Contoso Customer Confidential"}

```

<span data-ttu-id="51c7e-165">이제 DLP Contoso Customer Form.docx 문서 지문과 일치 하는 문서를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="51c7e-165">DLP now detects documents that match the Contoso Customer Form.docx document fingerprint.</span></span>
  
<span data-ttu-id="51c7e-166">구문 및 매개 변수 정보를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="51c7e-166">For syntax and parameter information, see:</span></span>

- [<span data-ttu-id="51c7e-167">새 DlpFingerprint</span><span class="sxs-lookup"><span data-stu-id="51c7e-167">New-DlpFingerprint</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpFingerprint)
- [<span data-ttu-id="51c7e-168">새 DlpSensitiveInformationType</span><span class="sxs-lookup"><span data-stu-id="51c7e-168">New-DlpSensitiveInformationType</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/New-DlpSensitiveInformationType)
- [<span data-ttu-id="51c7e-169">DlpSensitiveInformationType 제거</span><span class="sxs-lookup"><span data-stu-id="51c7e-169">Remove-DlpSensitiveInformationType</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Remove-DlpSensitiveInformationType)
- [<span data-ttu-id="51c7e-170">집합 DlpSensitiveInformationType</span><span class="sxs-lookup"><span data-stu-id="51c7e-170">Set-DlpSensitiveInformationType</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpSensitiveInformationType)
- [<span data-ttu-id="51c7e-171">Get-DlpSensitiveInformationType</span><span class="sxs-lookup"><span data-stu-id="51c7e-171">Get-DlpSensitiveInformationType</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpSensitiveInformationType)
