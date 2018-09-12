---
title: Office 365 피싱 방지 하기 위해 보낸사람 주소를 확인 하는 방법
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
description: '피싱을 방지 하려면 Office 365 및 Outlook.com 이제 필요에 대 한 RFC 준수에서: 주소입니다.'
ms.openlocfilehash: 8425d4ef7635c2beddcd7915daf73736432d4ca9
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955430"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="873c5-103">Office 365 피싱 방지 하기 위해 보낸사람 주소를 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="873c5-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="873c5-p101">Office 365와 Outlook.com 전자 메일 계정을 피싱 공격 수가 점점 많은 받습니다. From에 대 한 값이 있는 메시지를 보낼 피셔를 사용 하는 방법 중 하나는: [RFC 5322](https://tools.ietf.org/html/rfc5322)와 호환 되지 않은 주소입니다. From: 주소는 5322.From 주소를 라고도 합니다. Office 365 및 Outlook.com 필요 서비스에서 받은 메시지에 게는 RFC 규격를 포함 하도록이 유형의 피싱을 방지 하려면에서:이 문서에서 설명한 것 처럼 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p101">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks. One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322). The From: address is also called the 5322.From address. To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="873c5-p102">이 문서의 정보는 일반 형식의 전자 메일 주소를 기본적으로 이해 해야 합니다. 자세한 내용은 [RFC 5322](https://tools.ietf.org/html/rfc5322) (특히 3.2.3, 3.4, 및 섹션 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321) [RFC 3696](https://tools.ietf.org/html/rfc3696)을 참조 하십시오. 이 문서는 5322.From 주소에 대 한 정책 적용 하는 방법에 대 한 합니다. 이 문서는 5321.MailFrom 주소에 대 한 없습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p102">The information in this article requires you to have a basic understanding of the general format of email addresses. For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696). This article is about policy enforcement for the 5322.From address. This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="873c5-p103">그러나 중인 있으면 인터넷에서 계속 해 서 "합법적인" 전자 메일 메시지는 누락 된 있는 보내기 일부 레거시 전자 메일 서버에서 잘못 된 또는: 주소입니다. 정기적으로 이러한 레거시 시스템을 사용 하는 조직에서 전자 메일을 수신, 현대 보안 표준을 준수 하는 메일 서버를 업데이트 하려면 이러한 조직의 것을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p103">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address. If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="873c5-114">Microsoft는 2017 년 11 월 9에서이 문서에 설명 된 정책 적용 롤아웃 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="873c5-115">Office 365에서 유효한의 사용을 적용 하는 방법: 피싱 공격을 방지 하기 위해 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="873c5-p104">Office 365가 변경 From의 사용을 적용 하는 방식에 작업을 수행: 향상 하기 위해 받는 메시지에 주소 피싱 공격 으로부터 사용자를 보호 합니다. 이 문서의 내용</span><span class="sxs-lookup"><span data-stu-id="873c5-p104">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks. In this article:</span></span>
  
- [<span data-ttu-id="873c5-118">모든 메시지에서 유효한 포함 해야: 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="873c5-119">From의 형식: 표시 이름을 포함 하지 않으면 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-119">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="873c5-120">From의 형식: 주소 표시 이름을 포함 하는 경우</span><span class="sxs-lookup"><span data-stu-id="873c5-120">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="873c5-121">유효 하지 않은의 추가 예: 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-121">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="873c5-122">From을 위반 하지 않고 자동 회신 메시지를 사용자 지정 도메인을 표시 안함: 정책</span><span class="sxs-lookup"><span data-stu-id="873c5-122">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="873c5-123">Office 365에서 재정의: 적용 정책 처리</span><span class="sxs-lookup"><span data-stu-id="873c5-123">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="873c5-124">방지 하 고 Office 365의 cybercrimes 보호 하는 다른 방법</span><span class="sxs-lookup"><span data-stu-id="873c5-124">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="873c5-125">Terry Zink 블로그 읽기에 대 한 자세한 내용은 이러한 변경에 의해 영향을 받지 않습니다 다른 사용자 대신 보내기 "[수행의 의미는 전자 메일의 '보낸'를 언급할 때?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)"입니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-125">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="873c5-126">모든 메시지에서 유효한 포함 해야: 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-126">All messages must include a valid From: address</span></span>
<span data-ttu-id="873c5-127"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-127"></span></span>

<span data-ttu-id="873c5-p105">일부 자동화 된 메시지를 보낸을 포함 하지 않습니다: 전송 하는 경우를 처리 합니다. Office 365 또는 Outlook.com From 없이 메시지를 받을 때 이전에: 주소, 서비스에서 다음과 같은 기본 추가: 결과물 확인 하기 위해 메시지에 주소:</span><span class="sxs-lookup"><span data-stu-id="873c5-p105">Some automated messages don't include a From: address when they are sent. In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="873c5-p106">2017 년 11 월 9, 시작 Office 365가 될 롤아웃 변경 내용을 새 규칙을 적용 하는 해당 데이터 센터 및 메일 서버에 있는 From 없이 메시지: 주소는 Office 365 또는 Outlook.com에서 더이상 허용 됩니다. 대신 Office 365에서 받은 모든 메시지 이미 포함 되어 있어야에서 유효한: 주소입니다. 그렇지 않은 경우 Outlook.com 및 Office 365의 정크 메일 또는 지운 편지함 폴더에 메시지를 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p106">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com. Instead, all messages received by Office 365 must already contain a valid From: address. Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="873c5-133">구문 개요: From에 대 한 유효한 형식: Office 365에 대 한 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-133">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="873c5-134"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-134"></span></span>

<span data-ttu-id="873c5-p107">From 값에 대 한 형식: 주소 여러 Rfc 별 자세히 정의 됩니다. 주소 지정 하 고 유효한 지 여부에 간주할 수에 다음과 같은 여러 가지가 있습니다. 단순하게 유지 하는 다음과 같은 형식 및 정의 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p107">The format for the value of the From: address is defined in detail across several RFCs. There are many variations on addressing and what may be considered valid or invalid. To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="873c5-138">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-138">Where:</span></span>
  
- <span data-ttu-id="873c5-p108">(선택 사항)  *displayname* 은 전자 메일 주소의 소유자를 설명 하는 구문입니다. 예,이 기능이 필요할 수는 사서함의 이름 보다 보낸사람을 설명 하기 위해 보다 친숙 한 이름입니다. 표시 이름을 사용 하는 것은 선택 사항입니다. 그러나 표시 이름을 사용 하려는 하면 항상 묶어야 따옴표와 같이 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p108">(Optional)  *displayname*  is a phrase that describes the owner of the email address. For example, this might be a more user-friendly name to describe the sender than the name of the mailbox. Using a display name is optional. However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="873c5-143">(필수)  *emailaddress* 으로 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-143">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="873c5-144">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-144">Where:</span></span>
    
  - <span data-ttu-id="873c5-p109">(필수)  *로컬-* 부분은 주소와 연결 된 사서함을 식별 하는 문자열입니다. 이 도메인 내에서 고유 합니다. 자주, 사서함 소유자의 사용자 이름 또는 GUID를 값으로 사용 로컬 부분에 대 한 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p109">(Required)  *local-part*  is a string that identifies the mailbox associated with the address. This is unique within the domain. Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="873c5-148">(필수)  *도메인* 의 전자 메일 주소 중 로컬 부분으로 식별 된 사서함을 호스트 하는 메일 서버의 정규화 된 도메인 이름 (FQDN)은.</span><span class="sxs-lookup"><span data-stu-id="873c5-148">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="873c5-149">From의 형식: 표시 이름을 포함 하지 않으면 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-149">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="873c5-150"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-150"></span></span>

<span data-ttu-id="873c5-p110">A에서 올바르게 포맷: 주소는 표시 이름이 포함 되지 않은 단일 전자 메일 주소를 함께 또는 따로 꺾쇠 괄호를 포함 합니다. 공백으로 꺾쇠 괄호를 구분 하지 않는 것이 좋습니다. 또한 하지 뒤에 포함 아무것도 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p110">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets. Microsoft recommends that you do not separate the angle brackets with spaces. In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="873c5-154">다음 예는 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-154">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="873c5-155">다음 예제에서는 유효 하지만 꺾쇠 괄호와 전자 메일 주소 사이 공백이 포함 되어 있으므로 권장 되지:</span><span class="sxs-lookup"><span data-stu-id="873c5-155">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="873c5-156">다음 예제에서는 전자 메일 주소 다음 텍스트를 포함 하기 때문에 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-156">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="873c5-157">From의 형식: 주소 표시 이름을 포함 하는 경우</span><span class="sxs-lookup"><span data-stu-id="873c5-157">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="873c5-158"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-158"></span></span>

<span data-ttu-id="873c5-159">에 대 한에서: 표시 이름에 대 한 값이 포함 된 주소, 다음 규칙이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-159">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="873c5-p111">보낸사람 주소 표시 이름을 포함 하는 경우 표시 이름에 쉼표가 포함 표시 이름은 따옴표로 묶을 수 해야 합니다. 예를 들어:</span><span class="sxs-lookup"><span data-stu-id="873c5-p111">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks. For example:</span></span>
    
    <span data-ttu-id="873c5-162">다음 예제에서는 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-162">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="873c5-163">다음 예제에서는 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-163">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="873c5-164">해당 표시 이름에 쉼표를 포함 하는 경우 표시 이름을 따옴표로 하지 구분 RFC 5322에 따라 올바르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-164">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="873c5-165">최상의 방법으로 put 인용 부호에 관계 없이 표시 이름 주위 있는지 여부는 표시 이름 내에 쉼표를 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-165">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="873c5-166">표시 이름을 포함 하는 보낸사람 주소, 전자 메일 주소 꺾쇠 괄호 안에 묶을 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-166">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="873c5-167">최상의 방법으로 Microsoft 표시 이름 및 전자 메일 주소 사이 공백을 삽입 하는 강력 하 게 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-167">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="873c5-168">유효 하지 않은의 추가 예: 주소</span><span class="sxs-lookup"><span data-stu-id="873c5-168">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="873c5-169"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-169"></span></span>

- <span data-ttu-id="873c5-170">유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-170">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="873c5-p112">올바르지 않음. 전자 메일 주소는 꺾쇠 괄호와 묶지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p112">Invalid. The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="873c5-p113">유효 하지만 권장 하지는 않습니다. 표시 이름에 따옴표 않습니다. 표시 이름 주위에 따옴표를 항상 배치 것이 가장 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p113">Valid, but not recommended. The display name is not in quotes. As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="873c5-p114">올바르지 않음. 모든 작업은 사이 포함 된 따옴표, 표시 이름 뿐아니라:</span><span class="sxs-lookup"><span data-stu-id="873c5-p114">Invalid. Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="873c5-p115">올바르지 않음. 전자 메일 주소 주위 없는 꺾쇠 괄호 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p115">Invalid. There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="873c5-p116">올바르지 않음. 표시 이름 및 왼쪽된 꺾쇠 괄호 사이의 공간이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p116">Invalid. There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="873c5-p117">올바르지 않음. 표시 이름 주위 열린 닫는 인용 부호가 왼쪽된 꺾쇠 괄호 사이의 공간이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p117">Invalid. There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="873c5-184">From을 위반 하지 않고 자동 회신 메시지를 사용자 지정 도메인을 표시 안함: 정책</span><span class="sxs-lookup"><span data-stu-id="873c5-184">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="873c5-185"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-185"></span></span>

<span data-ttu-id="873c5-p118">새로 만들기와: 정책 적용 더 이상에서 사용할 수 없습니다: \< \> 자동 회신을 표시 하지 않으려면 합니다. 대신, 사용자 지정 도메인에 대 한 null MX 레코드를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p118">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies. Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="873c5-p119">메일 교환기 (MX) 레코드를 도메인에 대 한 메일을 받는 메일 서버를 식별 하는 DNS에 리소스 레코드를입니다. 자동 회신 (및 모든 회신) 응답 하는 서버가 메시지를 보낼 수 있는 게시 된 주소가 되지 않으므로 억제 원활 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p119">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain. Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="873c5-190">설정할 때 null MX 레코드를 사용자 지정 도메인에 대 한:</span><span class="sxs-lookup"><span data-stu-id="873c5-190">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="873c5-p120">도메인 선택에 맞지 않는 메시지를 보내며를 () 전자 메일을 받게 됩니다. 예: contoso.com에서 기본 도메인을 사용 하는 경우 noreply.contoso.com를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p120">Choose a domain from which to send messages that doesn't accept (receive) email. For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="873c5-p121">도메인에 대 한 null MX 레코드를 설정 합니다. Null MX 레코드는 단일 점을 사용 하 고 프로그램의 같이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p121">Set up the null MX record for your domain. A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="873c5-195">Null MX를 게시 하는 방법에 대 한 자세한 내용은 [RFC 7505](https://tools.ietf.org/html/rfc7505)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="873c5-195">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="873c5-196">Office 365에서 재정의: 적용 정책 처리</span><span class="sxs-lookup"><span data-stu-id="873c5-196">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="873c5-197"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-197"></span></span>

<span data-ttu-id="873c5-198">새 정책은 roll 완료 되 면 다음 방법 중 하나를 사용 하 여 Office 365에서 수신 되는 인바운드 메일에 대 한이 정책을 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-198">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="873c5-199">IP 허용 목록</span><span class="sxs-lookup"><span data-stu-id="873c5-199">IP allow lists</span></span>
    
- <span data-ttu-id="873c5-200">Exchange Online 메일 흐름 규칙</span><span class="sxs-lookup"><span data-stu-id="873c5-200">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="873c5-p122">From의 적용을 재정의 하는 것에 대 한 Microsoft 권장: 정책입니다. 이 정책을 재정의 스팸에 대 한 노출, 피싱, 및 기타 cybercrimes 조직의 위험을 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p122">Microsoft strongly recommends against overriding the enforcement of the From: policy. Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="873c5-p123">Office 365에서 보내는 아웃 바운드 메일에 대 한이 정책을 재정의할 수 없습니다. 또한 Outlook.com 지원 통한 경우에 어떤 종류의 재정의 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-p123">You cannot override this policy for outbound mail you send in Office 365. In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="873c5-205">방지 하 고 Office 365의 cybercrimes 보호 하는 다른 방법</span><span class="sxs-lookup"><span data-stu-id="873c5-205">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="873c5-206"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="873c5-206"></span></span>

<span data-ttu-id="873c5-207">피싱 같은 cybercrimes에 대 한 조직을 강화할 수는 방법에 대 한 자세한 내용은 스팸, 데이터 침해 및 기타 위협 요소는 [Office 365에 대 한 보안 모범 사례](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="873c5-207">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="873c5-208">관련 항목</span><span class="sxs-lookup"><span data-stu-id="873c5-208">Related Topics</span></span>

[<span data-ttu-id="873c5-209">후방 분산 메시지 및 EOP</span><span class="sxs-lookup"><span data-stu-id="873c5-209">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

