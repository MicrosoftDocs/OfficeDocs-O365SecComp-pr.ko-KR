---
title: Office 365에서 보낸 사람 주소의 유효성을 검사 하 여 피싱을 방지 하는 방법
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: '피싱 방지를 위해 Office 365 및 Outlook.com에는 이제 From: 주소에 대 한 RFC 준수가 필요 합니다.'
ms.openlocfilehash: e540e56a7a40d13a92719865fccefefa61de47c2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32253936"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="7e480-103">Office 365에서 보낸 사람 주소의 유효성을 검사 하 여 피싱을 방지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7e480-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="7e480-104">Office 365 및 Outlook.com 전자 메일 계정에는 많은 수의 피싱 공격이 수신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-104">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks.</span></span> <span data-ttu-id="7e480-105">phishers을 사용 하는 한 가지 방법은 [RFC 5322](https://tools.ietf.org/html/rfc5322)을 준수 하지 않는 보낸 사람: 주소에 대 한 값이 포함 된 메시지를 보내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-105">One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322).</span></span> <span data-ttu-id="7e480-106">보낸 사람: 주소는 5322.from 주소의 주소 라고도 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-106">The From: address is also called the 5322.From address.</span></span> <span data-ttu-id="7e480-107">이러한 유형의 피싱를 방지 하기 위해 Office 365 및 Outlook.com에서는이 문서에 설명 된 대로 서비스에서 받은 메시지에 RFC 호환 From: address를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-107">To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7e480-108">이 문서의 정보를 사용 하려면 전자 메일 주소의 일반적인 형식을 기본적으로 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-108">The information in this article requires you to have a basic understanding of the general format of email addresses.</span></span> <span data-ttu-id="7e480-109">자세한 내용은 [rfc 5322](https://tools.ietf.org/html/rfc5322) (특히 3.2.3, 3.4 및 3.4.1), [rfc 5321](https://tools.ietf.org/html/rfc5321)및 [rfc 3696](https://tools.ietf.org/html/rfc3696)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7e480-109">For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696).</span></span> <span data-ttu-id="7e480-110">이 문서에서는 5322.from 주소의 주소에 대 한 정책 적용 정보를 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-110">This article is about policy enforcement for the 5322.From address.</span></span> <span data-ttu-id="7e480-111">이 문서는 5321 보낸 사람 주소에는 해당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-111">This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="7e480-112">아쉽게도 인터넷에는 여전히 일부 레거시 전자 메일 서버가 있는데,이는 주소가 누락 되었거나 형식이 잘못 된 "합법적인" 전자 메일 메시지를 계속 전송 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-112">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address.</span></span> <span data-ttu-id="7e480-113">이러한 레거시 시스템을 사용 하는 조직에서 정기적으로 전자 메일을 수신 하는 경우 해당 조직이 최신 보안 표준을 준수 하도록 메일 서버를 업데이트 하도록 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-113">If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="7e480-114">Microsoft는 2017 년 11 월 9 일에이 문서에서 설명 하는 정책의 적용을 롤아웃 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="7e480-115">Office 365에서 유효한 보낸 사람 주소 사용을 적용 하 여 피싱 공격을 방지 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7e480-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="7e480-116">Office 365은 피싱 공격 으로부터 사용자를 보호 하기 위해 받은 메시지에 보낸 사람: 주소를 사용 하도록 강제 적용 하는 방식을 변경 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-116">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks.</span></span> <span data-ttu-id="7e480-117">이 문서의 내용</span><span class="sxs-lookup"><span data-stu-id="7e480-117">In this article:</span></span>
  
- [<span data-ttu-id="7e480-118">모든 메시지에는 다음의 유효한 보낸 사람: 주소가 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="7e480-119">보낸 사람: 주소에 표시 이름을 포함 하지 않는 경우의 형식</span><span class="sxs-lookup"><span data-stu-id="7e480-119">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="7e480-120">보낸 사람: 주소에 표시 이름을 포함 하는 경우의 형식</span><span class="sxs-lookup"><span data-stu-id="7e480-120">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="7e480-121">유효한 및 잘못 된 보낸 사람에 대 한 추가 예: 주소</span><span class="sxs-lookup"><span data-stu-id="7e480-121">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="7e480-122">의 출처를 끊지 않고 사용자 지정 도메인에 대 한 자동 회신을 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-122">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="7e480-123">Office 365 From: address 강요 policy 재정의</span><span class="sxs-lookup"><span data-stu-id="7e480-123">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="7e480-124">Office 365에서 cybercrimes을 방지 하 고 보호 하는 기타 방법</span><span class="sxs-lookup"><span data-stu-id="7e480-124">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="7e480-125">다른 사용자 대신 보내기는이 변경 내용에 영향을 주지 않습니다. 자세한 내용은 Terry zink의 블로그 "[전자 메일의 ' 보낸 사람 '을 참조 하는 경우 무슨 의미 입니까?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)"를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-125">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="7e480-126">모든 메시지에는 다음의 유효한 보낸 사람: 주소가 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-126">All messages must include a valid From: address</span></span>
<span data-ttu-id="7e480-127"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-127"></span></span>

<span data-ttu-id="7e480-128">일부 자동화 된 메시지는 보낸 경우에 보낸 사람: 주소를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-128">Some automated messages don't include a From: address when they are sent.</span></span> <span data-ttu-id="7e480-129">이전의 경우 Office 365 또는 Outlook.com가 보낸 사람: 주소를 제외 하 고 메시지를 받은 경우 서비스는 다음과 같은 기본값을 메시지에 주소에 추가 하 여 it를 인도품으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-129">In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="7e480-130">2017 년 11 월 9 일부터 office 365은 데이터 센터 및 메일 서버에 대 한 변경 내용을 롤아웃하기 때문에 보낸 사람: 주소 없이 메시지가 office 365 또는 Outlook.com에서 더 이상 수락 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-130">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com.</span></span> <span data-ttu-id="7e480-131">대신, Office 365에서 수신 되는 모든 메시지에는 올바른 보낸 사람: 주소가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-131">Instead, all messages received by Office 365 must already contain a valid From: address.</span></span> <span data-ttu-id="7e480-132">그렇지 않으면 메시지가 Outlook.com 및 Office 365의 정크 메일 또는 지운 편지함 폴더에 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-132">Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="7e480-133">구문 개요: From: address for Office 365의 유효한 형식</span><span class="sxs-lookup"><span data-stu-id="7e480-133">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="7e480-134"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-134"></span></span>

<span data-ttu-id="7e480-135">From: 주소 값의 형식은 여러 rfc에서 세부 정보로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-135">The format for the value of the From: address is defined in detail across several RFCs.</span></span> <span data-ttu-id="7e480-136">주소 지정에는 많은 변화가 있으며 유효한 지 또는 잘못 된 것으로 간주 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-136">There are many variations on addressing and what may be considered valid or invalid.</span></span> <span data-ttu-id="7e480-137">이를 단순하게 유지 하기 위해 다음 형식과 정의를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-137">To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="7e480-138">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-138">Where:</span></span>
  
- <span data-ttu-id="7e480-139">반드시  *displayname* 은 전자 메일 주소의 소유자를 설명 하는 구입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-139">(Optional)  *displayname*  is a phrase that describes the owner of the email address.</span></span> <span data-ttu-id="7e480-140">예를 들어 사서함 이름 보다 사용자에 게 친숙 한 이름을 사용 하 여 보낸 사람을 설명할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-140">For example, this might be a more user-friendly name to describe the sender than the name of the mailbox.</span></span> <span data-ttu-id="7e480-141">표시 이름을 사용 하는 것은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-141">Using a display name is optional.</span></span> <span data-ttu-id="7e480-142">그러나 표시 이름을 사용 하도록 선택 하는 경우에는 다음과 같이 항상 따옴표로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-142">However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="7e480-143">않아도  *emailaddress* 는 다음으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-143">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="7e480-144">여기서 각 부분이 나타내는 의미는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-144">Where:</span></span>
    
  - <span data-ttu-id="7e480-145">않아도  *로컬 부분-* 주소와 연결 된 사서함을 식별 하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-145">(Required)  *local-part*  is a string that identifies the mailbox associated with the address.</span></span> <span data-ttu-id="7e480-146">이는 도메인 내에서 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-146">This is unique within the domain.</span></span> <span data-ttu-id="7e480-147">일반적으로 사서함 소유자의 사용자 이름 또는 GUID는 로컬 부분에 대 한 값으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-147">Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="7e480-148">않아도  *domain* 은 전자 메일 주소의 로컬 부분으로 식별 되는 사서함을 호스트 하는 메일 서버의 FQDN (정규화 된 도메인 이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-148">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="7e480-149">보낸 사람: 주소에 표시 이름을 포함 하지 않는 경우의 형식</span><span class="sxs-lookup"><span data-stu-id="7e480-149">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="7e480-150"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-150"></span></span>

<span data-ttu-id="7e480-151">표시 이름이 포함 되지 않은 적절 한 형식의 주소에는 단일 전자 메일 주소만 포함 되거나 꺾쇠 괄호를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-151">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets.</span></span> <span data-ttu-id="7e480-152">꺾쇠 괄호와 공백을 구분 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-152">Microsoft recommends that you do not separate the angle brackets with spaces.</span></span> <span data-ttu-id="7e480-153">또한 전자 메일 주소 다음에는 아무런 내용도 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="7e480-153">In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="7e480-154">다음 예제를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-154">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="7e480-155">다음은 유효 하지만 꺾쇠 괄호와 전자 메일 주소 사이에 공백이 포함 되므로 권장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-155">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="7e480-156">다음 예는 전자 메일 주소 다음에 텍스트가 포함 되어 있기 때문에 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-156">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="7e480-157">보낸 사람: 주소에 표시 이름을 포함 하는 경우의 형식</span><span class="sxs-lookup"><span data-stu-id="7e480-157">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="7e480-158"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-158"></span></span>

<span data-ttu-id="7e480-159">보낸 사람: 표시 이름에 대 한 값을 포함 하는 주소에는 다음 규칙이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-159">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="7e480-160">보낸 사람 주소에 표시 이름이 포함 되어 있고 표시 이름에 쉼표가 포함 되어 있으면 표시 이름을 따옴표 안에 넣어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-160">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks.</span></span> <span data-ttu-id="7e480-161">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-161">For example:</span></span>
    
    <span data-ttu-id="7e480-162">다음 예를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-162">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="7e480-163">다음 예는 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-163">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="7e480-164">RFC 5322에 따라 표시 이름이 쉼표를 포함 하는 경우 표시 이름을 따옴표로 묶지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-164">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="7e480-165">표시 이름에 쉼표가 있는지 여부에 관계 없이 표시 이름 앞뒤에 따옴표를 입력 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-165">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="7e480-166">보낸 사람 주소에 표시 이름이 포함 된 경우 전자 메일 주소를 꺾쇠 괄호 안에 넣어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-166">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="7e480-167">최상의 방법으로 표시 이름과 전자 메일 주소 사이에 공백을 삽입 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-167">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="7e480-168">유효한 및 잘못 된 보낸 사람에 대 한 추가 예: 주소</span><span class="sxs-lookup"><span data-stu-id="7e480-168">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="7e480-169"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-169"></span></span>

- <span data-ttu-id="7e480-170">잘못</span><span class="sxs-lookup"><span data-stu-id="7e480-170">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="7e480-171">올바르지 않음.</span><span class="sxs-lookup"><span data-stu-id="7e480-171">Invalid.</span></span> <span data-ttu-id="7e480-172">전자 메일 주소를 꺽쇠 괄호로 묶지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-172">The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="7e480-173">유효 하지만 권장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-173">Valid, but not recommended.</span></span> <span data-ttu-id="7e480-174">표시 이름이 따옴표가 아닌 경우</span><span class="sxs-lookup"><span data-stu-id="7e480-174">The display name is not in quotes.</span></span> <span data-ttu-id="7e480-175">가장 좋은 방법은 항상 표시 이름을 따옴표 앞에 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-175">As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="7e480-176">올바르지 않음.</span><span class="sxs-lookup"><span data-stu-id="7e480-176">Invalid.</span></span> <span data-ttu-id="7e480-177">표시 이름만이 아니라 인용 부호로 묶여 있는 항목은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-177">Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="7e480-178">올바르지 않음.</span><span class="sxs-lookup"><span data-stu-id="7e480-178">Invalid.</span></span> <span data-ttu-id="7e480-179">전자 메일 주소 주변에는 꺽쇠 괄호가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-179">There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="7e480-180">올바르지 않음.</span><span class="sxs-lookup"><span data-stu-id="7e480-180">Invalid.</span></span> <span data-ttu-id="7e480-181">표시 이름과 왼쪽 꺽쇠 괄호 사이에는 공백이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-181">There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="7e480-182">올바르지 않음.</span><span class="sxs-lookup"><span data-stu-id="7e480-182">Invalid.</span></span> <span data-ttu-id="7e480-183">표시 이름과 왼쪽 꺽쇠 괄호 사이에는 닫는 따옴표 사이에 공백이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-183">There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="7e480-184">의 출처를 끊지 않고 사용자 지정 도메인에 대 한 자동 회신을 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-184">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="7e480-185"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-185"></span></span>

<span data-ttu-id="7e480-186">새로운 from: 정책 적용을 사용 하 여 다음 \< \> 위치에서 더 이상 자동 회신을 사용 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-186">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies.</span></span> <span data-ttu-id="7e480-187">대신 사용자 지정 도메인에 대해 null MX 레코드를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-187">Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="7e480-188">MX (메일 교환기) 레코드는 도메인에 대 한 메일을 수신 하는 메일 서버를 식별 하는 DNS의 리소스 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-188">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain.</span></span> <span data-ttu-id="7e480-189">응답 서버가 메시지를 보낼 수 있는 게시 된 주소가 없기 때문에 자동 회신 (및 모든 응답)은 자연스럽 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-189">Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="7e480-190">사용자 지정 도메인에 대해 null MX 레코드를 설정 하는 경우 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-190">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="7e480-191">전자 메일을 수락 (수신) 하지 않는 메시지를 보낼 도메인을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-191">Choose a domain from which to send messages that doesn't accept (receive) email.</span></span> <span data-ttu-id="7e480-192">예를 들어 주 도메인이 contoso.com 인 경우 noreply.contoso.com을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-192">For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="7e480-193">도메인에 대해 null MX 레코드를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-193">Set up the null MX record for your domain.</span></span> <span data-ttu-id="7e480-194">null MX 레코드는 다음과 같은 단일 점으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-194">A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="7e480-195">null MX를 게시 하는 방법에 대 한 자세한 내용은 [RFC 7505](https://tools.ietf.org/html/rfc7505)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="7e480-195">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="7e480-196">Office 365 From: address 강요 policy 재정의</span><span class="sxs-lookup"><span data-stu-id="7e480-196">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="7e480-197"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-197"></span></span>

<span data-ttu-id="7e480-198">새 정책을 완료 한 후에는 다음 방법 중 하나를 사용 하 여 Office 365에서 받은 인바운드 메일용으로이 정책만 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-198">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="7e480-199">IP 허용 목록</span><span class="sxs-lookup"><span data-stu-id="7e480-199">IP allow lists</span></span>
    
- <span data-ttu-id="7e480-200">Exchange Online 메일 흐름 규칙</span><span class="sxs-lookup"><span data-stu-id="7e480-200">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="7e480-201">에서의 적용을 무시 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-201">Microsoft strongly recommends against overriding the enforcement of the From: policy.</span></span> <span data-ttu-id="7e480-202">이 정책을 재정의 하면 스팸, 피싱 및 기타 cybercrimes에 대 한 조직의 노출 위험을 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-202">Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="7e480-203">Office 365에서 보내는 아웃 바운드 메일에 대해서는이 정책을 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-203">You cannot override this policy for outbound mail you send in Office 365.</span></span> <span data-ttu-id="7e480-204">또한 Outlook.com에서는 지원을 통해 모든 종류의 재정의를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e480-204">In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="7e480-205">Office 365에서 cybercrimes을 방지 하 고 보호 하는 기타 방법</span><span class="sxs-lookup"><span data-stu-id="7e480-205">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="7e480-206"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="7e480-206"></span></span>

<span data-ttu-id="7e480-207">피싱, spamming, 데이터 위반 및 기타 위협과 같은 cybercrimes 로부터 조직을 강화 하는 방법에 대 한 자세한 내용은 [Office 365의 보안 모범 사례](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e480-207">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="7e480-208">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7e480-208">Related Topics</span></span>

[<span data-ttu-id="7e480-209">후방 분산 메시지 및 EOP</span><span class="sxs-lookup"><span data-stu-id="7e480-209">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

