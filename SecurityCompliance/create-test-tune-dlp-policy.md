---
title: DLP 정책 만들기, 테스트 및 조정
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'DLP 정책을 시작 하는 가장 쉽고 일반적인 방법은 Office 365에 포함 된 서식 파일 중 하나를 사용 하는 것입니다. '
ms.openlocfilehash: 14582a6507d271bc569aeb0c5456a662962d20a9
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223747"
---
# <a name="create-test-and-tune-a-dlp-policy"></a><span data-ttu-id="fca1a-103">DLP 정책 만들기, 테스트 및 조정</span><span class="sxs-lookup"><span data-stu-id="fca1a-103">Create, test, and tune a DLP policy</span></span>

<span data-ttu-id="fca1a-104">**주도자 작성자**</span><span class="sxs-lookup"><span data-stu-id="fca1a-104">**Principal author**</span></span> <br/>
<span data-ttu-id="fca1a-105">Paul Cunningham (Microsoft MVP)</span><span class="sxs-lookup"><span data-stu-id="fca1a-105">Paul Cunningham, Microsoft MVP</span></span> <br/>
[<span data-ttu-id="fca1a-106">실질적인 365</span><span class="sxs-lookup"><span data-stu-id="fca1a-106">Practical 365</span></span>](https://practical365.com/) <br/>
[<span data-ttu-id="fca1a-107">@Practical365</span><span class="sxs-lookup"><span data-stu-id="fca1a-107">@Practical365</span></span>](https://twitter.com/practical365)<br/>
__________________________________________________

<span data-ttu-id="fca1a-p101">데이터 손실 방지는 조직에서 원치 않는 사용자에 게 중요 한 정보를 고의적으로 또는 실수로 노출 하지 못하게 하는 데 도움이 되도록 설계 된 Office 365의 규정 준수 기능입니다. DLP는 exchange Server 및 exchange Online의 루트를 포함 하며 SharePoint online 및 비즈니스용 OneDrive 에서도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p101">Data loss prevention is a compliance feature of Office 365 that is designed to help your organization prevent the intentional or accidental exposure of sensitive information to unwanted parties. DLP has its roots in Exchange Server and Exchange Online, and is also applicable in SharePoint Online and OneDrive for Business.</span></span>

<span data-ttu-id="fca1a-p102">DLP는 콘텐츠 분석 엔진을 사용 하 여 전자 메일 메시지 및 파일의 내용을 검토 하 고 신용 카드 번호 및 PII (개인 식별 정보)와 같은 중요 한 정보를 검색 합니다. 중요 한 정보는 전자 메일 메시지를 암호화 하는 등의 추가 단계를 수행 하지 않고 전자 메일로 보내거나 문서에 포함 되지 않아야 합니다. DLP를 사용 하 여 중요 한 정보를 검색 하 고 다음과 같은 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p102">DLP uses a content analysis engine to examine the contents of email messages and files, looking for sensitive information such as credit card numbers and personally identifiable information (PII). Sensitive information should typically not be sent in email, or included in documents, without taking additional steps such as encrypting the email message or files. Using DLP you can detect sensitive information, and take action such as:</span></span>

- <span data-ttu-id="fca1a-113">감사 목적으로 이벤트 기록</span><span class="sxs-lookup"><span data-stu-id="fca1a-113">Log the event for auditing purposes</span></span>
- <span data-ttu-id="fca1a-114">전자 메일을 보내거나 파일을 공유 하는 최종 사용자에 게 경고를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-114">Display a warning to the end user who is sending the email or sharing the file</span></span>
- <span data-ttu-id="fca1a-115">전자 메일 또는 파일 공유가 수행 되는 것을 적극적으로 차단</span><span class="sxs-lookup"><span data-stu-id="fca1a-115">Actively block the email or file sharing from taking place</span></span>

<span data-ttu-id="fca1a-p103">때로는 사용자가 보호 해야 하는 데이터의 형식을 고려 하지 않으므로 DLP를 해제 하는 경우가 있습니다. 의료 기록 또는 금융 정보와 같은 중요 한 데이터는 산업 의료 같은 업종 또는 온라인 상점을 실행 하는 회사에만 존재 하는 것으로 가정 합니다. 그러나 모든 업무상 중요 한 정보를 인식 하지 못하는 경우에도 정기적으로 처리할 수 있습니다. 직원 이름 및 생년월일의 스프레드시트는 고객 이름 및 신용 카드의 정보에 대 한 스프레드시트와 마찬가지로 중요 한 것입니다. 또한 직원 들이 시스템에서 CSV 파일을 내보낸 후 다른 사람에 게 전자 메일을 보내는 것을 생각 하기 때문에이 정보 유형은 예상 보다 더 많은 시간을 들을 수 있습니다. 직원 들이 결과를 고려 하지 않고 신용 카드 또는 은행 정보를 포함 하는 전자 메일을 보내는 방법에 대해서도 생각해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p103">Sometimes customers dismiss DLP because they don't consider themselves to have the type of data that needs protecting. The assumption is that sensitive data, such as medical records or financial information, only exists for industries like health care or for companies that run online stores. But any business can handle sensitive information on a regular basis, even if they don't realize it. A spreadsheet of employee names and dates of birth is just as sensitive as a spreadsheet of customer names and credit card details. And this type of information tends to float around more than you might expect, as employees quietly go about their day to day tasks, thinking nothing of export a CSV file from a system and emailing it to someone. You might also be surprised how often employees send emails containing credit card or banking details without considering the consequences.</span></span>

## <a name="how-sensitive-information-is-detected-by-dlp"></a><span data-ttu-id="fca1a-122">DLP에서 중요 한 정보를 검색 하는 방법</span><span class="sxs-lookup"><span data-stu-id="fca1a-122">How sensitive information is detected by DLP</span></span>

<span data-ttu-id="fca1a-p104">중요 한 정보는 정규식 (RegEx) 패턴 일치로 식별 되며 특정 키워드를 일치 패턴에 근접 하 게 하는 등의 다른 표시기와 함께 사용 합니다. 이 예에서는 신용 카드 번호를 예로 들 수 있습니다. 신용 카드 번호는 16 자리입니다. 그러나 이러한 숫자는 1111-1111-1111-1111, 1111 1111 1111 1111 또는 1111111111111111과 같은 다양 한 방식으로 작성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p104">Sensitive information is identified by regular expression (RegEx) pattern matching, in combination with with other indicators such as the proximity of certain keywords to the matching patterns. An example of this is credit card numbers. A VISA credit card number has 16 digits. However, those digits can be written in different ways, such as 1111-1111-1111-1111, 1111 1111 1111 1111, or 1111111111111111.</span></span>

<span data-ttu-id="fca1a-p105">16 자리 문자열은 항상 신용 카드 번호가 아니며 지원 센터 시스템의 티켓 번호나 하드웨어의 일련 번호가 될 수 있습니다. 신용 카드 번호와 무해 한 16 자리 문자열을 구별 하기 위해 숫자가 다양 한 신용 카드 상표에서 알려진 패턴과 일치 하는 것을 확인 하는 계산 (체크섬)이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p105">Any 16 digit string is not necessarily a credit card number, it could be a ticket number from a help desk system, or a serial number of a piece of hardware. To tell the difference between a credit card number and a harmless 16-digit string, a calculation is performed (checksum) to confirm that the numbers match a known pattern from the various credit card brands.</span></span>

<span data-ttu-id="fca1a-129">또한 "로" 또는 "amex"와 같은 키워드와 같이 신용 카드 만료 날짜가 될 수 있는 날짜 값에 대 한 근접성과 함께 데이터가 신용 카드 번호 인지 여부를 결정 하는 것도 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-129">Furthermore, the proximity of keywords such as “VISA” or “AMEX”, along with the proximity to date values that might be the credit card expiry date, is also considered to make a decision about whether the data is a credit card number or not.</span></span>

<span data-ttu-id="fca1a-130">즉, 일반적으로 DLP는 전자 메일에서 이러한 두 가지 텍스트 간의 차이를 인식할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-130">In other words, DLP is usually smart enough to recognize the difference between these two texts in an email:</span></span>

- <span data-ttu-id="fca1a-p106">"새 랩톱을 주문할 수 있습니다. 내에 번호 1111-1111-1111-1111, 만료 11/22을 사용 하 여 예상 배달 날짜를 사용자에 게 제공 합니다. "</span><span class="sxs-lookup"><span data-stu-id="fca1a-p106">“Can you order me a new laptop. Use my VISA number 1111-1111-1111-1111, expiry 11/22, and send me the estimated delivery date when you have it.”</span></span>
- <span data-ttu-id="fca1a-p107">"내 랩탑 일련 번호는 2222-2222-2222-2222이 고 11/2010에서 구매한 것입니다. 내 출장은 아직 승인 되었습니까? "</span><span class="sxs-lookup"><span data-stu-id="fca1a-p107">“My laptop serial number is 2222-2222-2222-2222 and it was purchased on 11/2010. By the way, is my travel visa approved yet?”</span></span>

<span data-ttu-id="fca1a-135">이 항목에서는 각 정보 유형이 검색 되는 방식을 설명 하는 [중요 한 정보 유형에 대해 책갈피로 설정](what-the-sensitive-information-types-look-for.md) 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-135">A good reference to keep bookmarked is this [topic on sensitive information types](what-the-sensitive-information-types-look-for.md) that explains how each information type is detected.</span></span>

## <a name="where-to-start-with-data-loss-prevention"></a><span data-ttu-id="fca1a-136">데이터 손실 방지를 사용 하 여 시작 하는 위치</span><span class="sxs-lookup"><span data-stu-id="fca1a-136">Where to start with data loss prevention</span></span>

<span data-ttu-id="fca1a-p108">데이터 누출의 위험이 완전히 확실 하지 않을 경우에는 DLP 구현으로 시작 해야 하는 위치를 정확히 파악 하기가 어렵습니다. 다행히 DLP 정책은 "테스트 모드"에서 실행 될 수 있으므로, 기능을 설정 하기 전에 효율성과 정확성을 평가할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p108">When the risks of data leakage aren't entirely obvious, it's difficult to work out where exactly you should start with implementing DLP. Fortunately, DLP policies can be run in “test mode”, allowing you to gauge their effectiveness and accuracy before you turn them on.</span></span>

<span data-ttu-id="fca1a-p109">exchange Online에 대 한 DLP 정책은 exchange 관리 센터를 통해 관리할 수 있습니다. 그러나 보안 & 준수 센터를 통해 모든 작업에 대해 DLP 정책을 구성할 수 있으므로이 문서에서 시연 하는 데 사용 하는 것이 좋습니다. Security & 준수 센터에서 **데이터 손실 방지** > **정책**에 따라 DLP 정책을 찾을 수 있습니다. 시작할 **정책 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p109">DLP policies for Exchange Online can be managed through the Exchange admin center. But you can configure DLP policies for all workloads through the Security & Compliance Center, so that's what I'll use for demonstrations in this article. In the Security & Compliance Center you'll find the DLP policies under **Data loss prevention** > **Policy**. Click on **Create a policy** to start.</span></span>

<span data-ttu-id="fca1a-p110">Office 365에서는 dlp 정책을 만드는 데 사용할 수 있는 다양 한 [dlp 정책 템플릿을](what-the-dlp-policy-templates-include.md) 제공 합니다. 사용자가 오스트레일리아 business 라고 가정해 보겠습니다. 금융, 의료 및 건강 및 개인 정보에 대 한 일반적인 범주에 해당 하는 오스트레일리아와 관련 된 항목만 표시 하도록 정책 서식 파일을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p110">Office 365 provides a range of [DLP policy templates](what-the-dlp-policy-templates-include.md) you can use to create DLP policies. Let's say that you're an Australian business. You can filter the policy templates to display only those that are relevant to Australia, which fall into the general categories of Financial, Medical and Health, and Privacy.</span></span>

![국가 또는 지역을 선택 하는 옵션](media/DLP-create-test-tune-choose-country.png)

<span data-ttu-id="fca1a-147">이 데모에서는 tfn (오스트레일리아 세금 파일 번호) 및 운전 면허 번호에 대 한 정보 유형을 포함 하는 호주 PII (개인 식별이 가능한 정보) 데이터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-147">For this demonstration I'll choose Australian Personally Identifiable Information (PII) Data, which includes the information types of Australian Tax File Number (TFN) and Driver's License Number.</span></span>

![정책 서식 파일을 선택 하는 옵션](media/DLP-create-test-tune-choose-policy-template.png)

<span data-ttu-id="fca1a-p111">새 DLP 정책에 이름을 지정 합니다. 기본 이름은 DLP 정책 템플릿과 일치 하지만, 같은 템플릿에서 여러 정책을 만들 수 있으므로 고유한 이름을 직접 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p111">Give your new DLP policy a name. The default name will match the DLP policy template, but you should choose a more descriptive name of your own, because multiple policies can be created from the same template.</span></span>

![정책 이름을 선택 하는 옵션](media/DLP-create-test-tune-name-policy.png)

<span data-ttu-id="fca1a-p112">정책이 적용 될 위치를 선택 합니다. DLP 정책은 Exchange online, SharePoint Online 및 비즈니스용 OneDrive에 적용 될 수 있습니다. 이 정책을 모든 위치에 적용 하도록 유지 하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p112">Choose the locations that the policy will apply to. DLP policies can apply to Exchange Online, SharePoint Online, and OneDrive for Business. I am going to leave this policy configured to apply to all locations.</span></span>

![모든 위치를 선택 하는 옵션](media/DLP-create-test-tune-choose-locations.png)

<span data-ttu-id="fca1a-p113">첫 번째 **정책 설정** 단계에서는 지금은 기본값을 그대로 사용 합니다. DLP 정책에서는 많은 사용자 지정 작업을 수행할 수 있지만 기본값은 매우 적절 한 시작 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p113">At the first **Policy Settings** step just accept the defaults for now. There is quite a lot of customization you can do in DLP policies, but the defaults are a fine place to start.</span></span>

![보호할 콘텐츠 형식을 사용자 지정 하는 옵션](media/DLP-create-test-tune-default-customization-settings.png)

<span data-ttu-id="fca1a-p114">**다음** 을 클릭 하면 더 많은 사용자 지정 옵션을 포함 하는 추가 **정책 설정** 페이지가 표시 됩니다. 테스트 중인 정책에 대해 몇 가지 조정 작업을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p114">After clicking **Next** you'll be presented with an additional **Policy Settings** page with more customization options. For a policy that you are just testing, here's where you can start to make some adjustments.</span></span>

- <span data-ttu-id="fca1a-p115">지금은 테스트를 수행 하 고 사용자에 게 어떤 것도 표시 하지 않으려는 경우에는 적절 한 단계에 해당 하는 정책 팁을 해제 했습니다. 정책 팁은 DLP 정책을 위반 하려고 한다는 것을 사용자에 게 경고를 표시 합니다. 예를 들어 Outlook 사용자에 게는 첨부 된 파일에 신용 카드 번호가 포함 되어 있으며 전자 메일이 거부 된다는 경고가 표시 됩니다. 정책 팁의 목표는 문제가 발생 하기 전에 비규격 동작을 중지 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p115">I've turned off policy tips for now, which is a reasonable step to take if you're just testing things out and don't want to display anything to users yet. Policy tips display warnings to users that they're about to violate a DLP policy. For example, an Outlook user will see a warning that the file they've attached contains credit card numbers and will cause their email to be rejected. The goal of policy tips is to stop the non-compliant behaviour before it happens.</span></span>
- <span data-ttu-id="fca1a-165">또한이 정책이 데이터를 대량으로 공유 하는 것이 아니라 오스트레일리아 PII 데이터의 공유를 검색할 수 있도록 10에서 1 사이의 인스턴스 수를 줄였습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-165">I've also decreased the number of instances from 10 to 1, so that this policy will detect any sharing of Australian PII data, not just bulk sharing of the data.</span></span>
- <span data-ttu-id="fca1a-166">또한 문제 보고서 전자 메일에 다른 받는 사람도 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-166">I've also added another recipient to the incident report email.</span></span>

![추가 정책 설정](media/DLP-create-test-tune-more-policy-settings.png)

<span data-ttu-id="fca1a-p116">마지막으로 테스트 모드에서 초기에 실행 되도록이 정책을 구성 했습니다. 또한 테스트 모드에서 정책 팁을 사용 하지 않도록 설정 하는 옵션도 있습니다. 이렇게 하면 정책에 정책 팁을 사용할 수 있는 유연성이 제공 되지만 테스트 중에 정책을 표시할지 아니면 표시할지를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p116">Finally, I've configured this policy to run in test mode initially. Notice there's also an option here to disable policy tips while in test mode. This gives you the flexibility to have policy tips enabled in the policy, but then decide whether to show or suppress them during your testing.</span></span>

![정책을 먼저 테스트 하기 위한 옵션](media/DLP-create-test-tune-test-mode.png)

<span data-ttu-id="fca1a-172">최종 검토 화면에서 **만들기** 를 클릭 하 여 정책 만들기를 마칩니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-172">On the final review screen click **Create** to finish creating the policy.</span></span>

## <a name="test-a-dlp-policy"></a><span data-ttu-id="fca1a-173">DLP 정책 테스트</span><span class="sxs-lookup"><span data-stu-id="fca1a-173">Test a DLP policy</span></span>

<span data-ttu-id="fca1a-p117">새 DLP 정책이 약 1 시간 내에 적용 됩니다. 이 작업을 수행 하 고 정상적인 사용자 활동에 의해 트리거될 때까지 기다리거나 직접 트리거하도록 할 수도 있습니다. 이전에는 DLP 일치를 트리거하는 방법에 대 한 정보를 제공 하는 [중요 한 정보 유형에 대](what-the-sensitive-information-types-look-for.md)한이 항목에 연결 했습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p117">Your new DLP policy will begin to take effect within about 1 hour. You can sit and wait for it to be triggered by normal user activity, or you can try to trigger it yourself. Earlier I linked to this [topic on sensitive information types](what-the-sensitive-information-types-look-for.md), which provides you with information about how to trigger DLP matches.</span></span>

<span data-ttu-id="fca1a-p118">예를 들어이 문서에 대해 만든 DLP 정책을 통해 tfn (오스트레일리아 세금 파일 번호)가 검색 됩니다. 설명서에 따르면 일치는 다음 조건을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p118">As an example, the DLP policy I created for this article will detect Australian tax file numbers (TFN). According to the documentation, the match is based on the following criteria.</span></span>

![오스트레일리아 세금 파일 번호에 대 한 설명서](media/DLP-create-test-tune-Australia-Tax-File-Number-doc.png)
 
<span data-ttu-id="fca1a-p119">tfn 검색을 대신 사용 하는 방법에 대 한 자세한 내용은 "세금 파일 번호" 라는 단어와 근접 한 근사 문자열을 포함 하는 전자 메일은 아무런 문제 없이 sail 됩니다. DLP 정책을 트리거하지 않는 이유는 9 자리 문자열이 유효한 tfn 인지 확인 하는 체크섬을 통과 해야 하 고, 무해 한 숫자 문자열 일 뿐 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p119">To demonstrate TFN detection in a rather blunt manner, an email with the words “Tax file number” and a 9 digit string in close proximity will sail through without any issues. The reason it does not trigger the DLP policy is that the 9-digit string must pass the checksum that indicates it is a valid TFN and not just a harmless string of numbers.</span></span>

![호주 세금 파일 번호 체크섬을 통과 하지 않음](media/DLP-create-test-tune-email-test1.png)

<span data-ttu-id="fca1a-p120">비교에서는 "세금 파일 번호" 라는 단어가 포함 된 전자 메일 및 체크섬을 통과 하는 유효한 tfn이 정책을 트리거합니다. 여기에서 사용 중인 tfn은 정품이 아닌 유효한 TFNs를 생성 하는 웹 사이트에서 가져온 것 이었습니다. [유효 하지만 가짜 신용 카드 번호](http://www.fakecreditcardgenerator.net/)를 생성 하는 비슷한 사이트가 있습니다. 이러한 사이트는 DLP 정책을 테스트할 때 가장 흔히 발생 하는 실수 중 하나는 유효 하지 않은 가짜 번호를 사용 하 고 체크섬을 전달 하지 않으므로 정책을 트리거하지 않으므로 매우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p120">In comparison, an email with the words “Tax file number” and a valid TFN that passes the checksum will trigger the policy. For the record here, the TFN I'm using was taken from a website that generates valid, but not genuine, TFNs. There are similar sites that generate [valid but fake credit card numbers](http://www.fakecreditcardgenerator.net/). Such sites are very useful because one of the most common mistakes when testing a DLP policy is using a fake number that's not valid and won't pass the checksum (and therefore won't trigger the policy).</span></span>

![오스트레일리아 세금 검사를 통과 한 파일 번호](media/DLP-create-test-tune-email-test2.png)

<span data-ttu-id="fca1a-188">문제 보고서 전자 메일에는 검색 된 중요 한 정보 유형, 검색 된 인스턴스 수 및 검색의 신뢰 수준이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-188">The incident report email includes the type of sensitive information that was detected, how many instances were detected, and the confidence level of the detection.</span></span>

![검색 된 세금 파일 번호를 보여 주는 문제 보고서](media/DLP-create-test-tune-email-incident-report.png)

<span data-ttu-id="fca1a-p121">dlp 정책을 테스트 모드에서 유지 하 고 문제 보고서 전자 메일을 분석 하는 경우 dlp 정책의 정확성과 적용 시기에 대 한 느낌을 얻기 시작할 수 있습니다. 문제 보고서 외에도 [DLP 보고서를 사용](view-the-dlp-reports.md) 하 여 테 넌 트 전체의 정책 일치 항목에 대 한 집계 된 보기를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p121">If you leave your DLP policy in test mode and analyze the incident report emails, you can start to get a feel for the accuracy of the DLP policy and how effective it will be when it is enforced. In addition to the incident reports, you can [use the DLP reports](view-the-dlp-reports.md) to see an aggregated view of policy matches across your tenant.</span></span>

## <a name="tune-a-dlp-policy"></a><span data-ttu-id="fca1a-192">DLP 정책 조정</span><span class="sxs-lookup"><span data-stu-id="fca1a-192">Tune a DLP policy</span></span>

<span data-ttu-id="fca1a-p122">정책 방문을 분석할 때 정책 작동 방식을 약간 조정 하는 것이 좋습니다. 간단한 예로, 전자 메일에서 하나의 tfn이 문제가 되지 않고 여전히 있는 것 처럼 생각 하지만이를 시연 하기 위해 계속 진행 하는 것은 좋지만 두 개 이상의 인스턴스가 문제가 되는 것을 확인할 수 있습니다. 예를 들어, 외부 계정 서비스와 같이 HR 데이터베이스에서 외부 사용자에 게 CSV 내보내기를 전자 메일로 보내는 직원과 같은 위험 시나리오가 여러 개 있을 수 있습니다. 원하는 것은 감지 하 고 차단 하려는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p122">As you analyze your policy hits you might want to make some adjustments to how the policies behave. As a simple example, you might determine that one TFN in email is not a problem (I think it still is, but let's go with it for the sake of demonstration), but two or more instances is a problem. Multiple instances could be a risky scenario such as an employee emailing a CSV export from the HR database to an external party, for example an external accounting service. Definitely something you would prefer to detect and block.</span></span>

<span data-ttu-id="fca1a-197">Security & 준수 센터에서 기존 정책을 편집 하 여 동작을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-197">In the Security & Compliance Center you can edit an existing policy to adjust the behaviour.</span></span>

![정책 편집 옵션](media/DLP-create-test-tune-edit-policy.png)
 
<span data-ttu-id="fca1a-199">특정 작업 또는 특정 사이트와 계정에만 정책이 적용 되도록 위치 설정을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-199">You can adjust the location settings so that the policy is applied only to specific workloads, or to specific sites and accounts.</span></span>

![특정 위치 선택 옵션](media/DLP-create-test-tune-edit-locations.png)

<span data-ttu-id="fca1a-201">또한 사용자의 요구에 맞게 정책 설정을 조정 하 고 규칙을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-201">You can also adjust the policy settings and edit the rules to better suit your needs.</span></span>

![규칙 편집 옵션](media/DLP-create-test-tune-edit-rule.png)

<span data-ttu-id="fca1a-203">DLP 정책 내에서 규칙을 편집할 때 다음을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-203">When editing a rule within a DLP policy you can change:</span></span>

- <span data-ttu-id="fca1a-204">규칙을 트리거할 중요 한 데이터의 인스턴스 유형 및 수를 포함 하는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-204">The conditions, including the type and number of instances of sensitive data that will trigger the rule.</span></span>
- <span data-ttu-id="fca1a-205">콘텐츠에 대 한 액세스 제한 등 수행 해야 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-205">The actions that are taken, such as restricting access to the content.</span></span>
- <span data-ttu-id="fca1a-206">사용자 알림-전자 메일 클라이언트나 웹 브라우저에서 사용자에 게 표시 되는 정책 팁입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-206">User notifications, which are policy tips that are displayed to the user in their email client or web browser.</span></span>
- <span data-ttu-id="fca1a-207">사용자는 전자 메일 또는 파일 공유를 계속 진행 하도록 선택할 수 있는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-207">User overrides, which determines whether users can choose to proceed with their email or file sharing anyway.</span></span>
- <span data-ttu-id="fca1a-208">관리자에 게 알리기 위한 문제 보고서</span><span class="sxs-lookup"><span data-stu-id="fca1a-208">Incident reports, to notify administrators.</span></span>

![규칙의 부분 편집 옵션](media/DLP-create-test-tune-editing-options.png)

<span data-ttu-id="fca1a-p123">이 데모에서는 정책에 사용자 알림을 추가 했으며 (적절 한 사용자 인식 교육 없이이 작업을 주의 해야 함), 사용자가 비즈니스 근거로 정책을 재정의 하거나이를 가양성으로 플래그를 지정할 수 있었습니다. 조직의 정책에 대 한 추가 정보를 포함 하거나 궁금한 사항이 있는 경우 사용자에 게 문의 하 라는 메시지를 표시 하려는 경우 전자 메일 및 정책 팁 텍스트를 사용자 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p123">For this demonstration I've added user notifications to the policy (be careful of doing this without adequate user awareness training), and allowed users to override the policy with a business justification or by flagging it as a false positive. Note that you can also customize the email and policy tip text if you want to include any additional information about your organization's policies, or prompt users to contact support if they have questions.</span></span>

![사용자 알림 및 재정의에 대 한 옵션](media/DLP-create-test-tune-user-notifications.png)

<span data-ttu-id="fca1a-p124">정책에는 고용량 및 low 볼륨 처리를 위한 두 가지 규칙이 포함 되어 있으므로 원하는 작업을 사용 하 여 모두 편집 해야 합니다. 이렇게 하면 사례를 특성에 따라 다르게 처리할 수 있습니다. 예를 들어 낮은 볼륨 위반에 대해서는 재정의를 허용 하지만 높은 볼륨 위반에 대해서는 재정의를 허용 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p124">The policy contains two rules for handling of high volume and low volume, so be sure to edit both with the actions that you want. This is an opportunity to treat cases differently depending on their characteristics. For example, you might allow overrides for low volume violations, but not allow overrides for high volume violations.</span></span>

![대용량 및 낮은 볼륨에 대 한 하나의 규칙에 대 한 규칙 하나](media/DLP-create-test-tune-two-rules.png)

<span data-ttu-id="fca1a-217">또한 정책을 위반 하는 콘텐츠에 대 한 액세스를 실제로 차단 하거나 제한 하려는 경우 규칙에 대 한 작업을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-217">Also, if you want to actually block or restrict access to content that is in violation of policy, you need to configure an action on the rule to do so.</span></span>

![콘텐츠에 대 한 액세스를 제한 하는 옵션](media/DLP-create-test-tune-restrict-access-action.png)

<span data-ttu-id="fca1a-p125">정책 설정에 해당 변경 내용을 저장 한 후에는 정책의 주 설정 페이지로 돌아가 정책이 테스트 모드에 있는 동안 사용자에 게 정책 팁을 표시 하는 옵션을 사용 해야 합니다. 이 방법은 최종 사용자에 게 DLP 정책을 도입 하 고, 생산성에 영향을 주는 가양성을 너무 많이 포함 하지 않고 사용자의 교육을 수행할 수 있는 효과적인 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p125">After saving those changes to the policy settings, I also need to return to the main settings page for the policy and enable the option to show policy tips to users while the policy is in test mode. This is an effective way to introduce DLP policies to your end users, and do user awareness training, without risking too many false positives that impact their productivity.</span></span>

![테스트 모드에서 정책 팁을 표시 하는 옵션](media/DLP-create-test-tune-show-policy-tips.png)

<span data-ttu-id="fca1a-p126">서버 쪽 (또는 클라우드 쪽)에서 변경 내용이 다양 한 처리 간격으로 인해 즉시 적용 되지 않을 수 있습니다. 사용자에 게 새 정책 팁을 표시 하는 DLP 정책 변경을 수행 하는 경우 사용자는 Outlook 클라이언트에서 즉시 적용 되며, 변경 내용이 24 시간 마다 정책 변경을 확인 하지 않을 수 있습니다. 테스트를 위해 속도를 향상 시키려면이 레지스트리 수정 프로그램을 사용 하 여 [PolicyNudges 키에서 마지막 다운로드 시간 스탬프를 지울](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451)수 있습니다. 다음에 Outlook을 다시 시작 하 고 전자 메일 메시지를 작성할 때 최신 정책 정보를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p126">On the server side (or cloud side if you prefer), the change may not take effect immediately, due to various processing intervals. If you're making a DLP policy change that will display new policy tips to a user, the user may not see the changes take effect immediately in their Outlook client, which checks for policy changes every 24 hours. If you want to speed things up for testing, you can use this registry fix to [clear the last download time stamp from the PolicyNudges key](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451). Outlook will download the latest policy information the next time you restart it and begin composing an email message.</span></span>

<span data-ttu-id="fca1a-226">정책 팁을 사용 하는 경우 사용자는 Outlook에서 팁을 표시 하기 시작 하 고, 발생 하는 경우 가양성을 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-226">If you have policy tips enabled, the user will begin to see the tips in Outlook, and can report false positives to you when they occur.</span></span>

![가양성을 보고 하는 옵션을 포함 하는 정책 설명](media/DLP-create-test-tune-policy-tip-in-outlook.png)

## <a name="investigate-false-positives"></a><span data-ttu-id="fca1a-228">가양성 조사</span><span class="sxs-lookup"><span data-stu-id="fca1a-228">Investigate false positives</span></span>

<span data-ttu-id="fca1a-p127">DLP 정책 템플릿은 상자에서 완벽 하 게 처리 되지 않습니다. 환경에서 가양성이 발생 하는 것은 매우 중요 하므로 DLP 배포를 간편 하 게 수행 하 여 정책을 적절 하 게 테스트 하 고 조정 하는 데 소요 되는 시간을 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p127">DLP policy templates are not perfect straight out of the box. It's likely that you'll find some false positives occurring in your environment, which is why it's so important to ease your way into a DLP deployment, taking the time to adequately test and tune your policies.</span></span>

<span data-ttu-id="fca1a-p128">다음은 가양성의 예입니다. 이 전자 메일은 매우 무해 합니다. 사용자는 자신의 전자 메일 서명을 비롯 하 여 다른 사람에 게 휴대폰 번호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p128">Here's an example of a false positive. This email is quite harmless. The user is providing their mobile phone number to someone, and including their email signature.</span></span>

![가양성 정보를 보여 주는 전자 메일](media/DLP-create-test-tune-false-positive-email.png)
 
<span data-ttu-id="fca1a-235">하지만 사용자는 전자 메일에 중요 한 정보, 특히 오스트레일리아 운전 면허 번호를 포함 하는 정책 팁 경고를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-235">But the user sees a policy tip warning them that the email contains sensitive information, specifically, an Australian driver's license number.</span></span>

![정책 팁에서 가양성을 보고 하는 옵션](media/DLP-create-test-tune-policy-tip-closeup.png)

<span data-ttu-id="fca1a-p129">사용자가 가양성을 보고할 수 있으며, 관리자는이를 통해 발생 한 이유를 확인할 수 있습니다. 문제 보고서 전자 메일에서 전자 메일은 가양성으로 플래그가 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p129">The user can report the false positive, and the administrator can look into why it has occurred. In the incident report email, the email is flagged as a false positive.</span></span>

![가양성을 보여 주는 문제 보고서](media/DLP-create-test-tune-false-positive-incident-report.png)

<span data-ttu-id="fca1a-p130">이 드라이버의 사용 사례는 자세히 알아볼 수 있는 좋은 예입니다. 이 가양성이 발생 한 이유는 "오스트레일리아 nsw" (대/소문자 구분 안 함)와 같은 300 문자 이내에 있는 9 자리 문자열 (10 자리 문자열의 일부인 경우에도 마찬가지)에 의해 "호주 운전 면허" 유형이 트리거되는 것입니다. 사용자가 시드니에 있는 경우에만 전화 번호 및 전자 메일 서명에 의해 트리거되는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p130">This driver's license case is a good example to dig into. The reason this false positive has occurred is that the “Australian Driver's License” type will be triggered by any 9-digit string (even one that is part of a 10-digit string), within 300 characters proximity to the keywords “sydney nsw” (not case sensitive). So it's triggered by the phone number and email signature, only because the user happens to be in Sydney.</span></span>

<span data-ttu-id="fca1a-p131">흥미롭게도 "시드니, NSW"에 쉼표가 있으면 DLP 정책이 트리거되지 않습니다. 쉼표가 여기에 있는 이유는 무엇 인가요, 아니면 호주의 다른 도시와 주는 오스트레일리아 운전 면허 정보 유형의 키워드에 포함 되지 않는 이유와, 이러한 경우에는 문제가 발생 합니다. 그렇다면 어떤 작업을 수행 해야 하나요? 몇 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p131">Interestingly, if “Sydney, NSW” has a comma, the DLP policy is not triggered. I have no idea why a comma makes any difference here, nor why other cities and states in Australia aren't included in the keywords for the Australian driver's license information type, but there you go. So, what can we do about it? There's a couple of options.</span></span>

<span data-ttu-id="fca1a-p132">한 가지 방법은 정책에서 오스트레일리아 운전 면허 정보 유형을 제거 하는 것입니다. 이 파일은 DLP 정책 템플릿의 일부 이기 때문에 여기에는 포함 되어 있지만 반드시 사용 해야 하는 것은 아닙니다. 세금 파일 번호에만 관심이 있는 경우 운전 면허증은 제거 하기만 하면 됩니다. 예를 들어 정책의 볼륨 부족 규칙에서 해당 파일을 제거할 수 있지만 여러 드라이버 라이선스 목록이 계속 해 서 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p132">One option is to remove the Australian driver's license information type from the policy. It's in there because it's part of the DLP policy template, but we're not forced to use it. If you're only interested in Tax File Numbers and not driver's licenses, you can just remove it. For example, you can remove it from the low volume rule in the policy, but leave it in the high volume rule so that lists of multiple drivers licenses are still detected.</span></span>

![규칙에서 중요 한 정보 유형을 삭제 하는 옵션](media/DLP-create-test-tune-delete-low-volume-rule.png)
 
<span data-ttu-id="fca1a-252">또 다른 옵션은 인스턴스 수를 늘려 단순히 여러 인스턴스가 있는 경우에만 드라이버의 라이선스 부족을 검색 하도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-252">Another option is to simply increase the instance count, so that a low volume of driver's licenses is only detected when there are multiple instances.</span></span>

![인스턴스 수 편집 옵션](media/DLP-create-test-tune-edit-instance-count.png)

<span data-ttu-id="fca1a-p133">인스턴스 수를 변경 하는 것 외에도 일치 정확도 (또는 신뢰 수준)를 조정할 수도 있습니다. 중요 한 정보 유형에 여러 패턴이 있는 경우 규칙이 특정 패턴만 일치 하도록 규칙에서 정확도를 조정할 수 있습니다. 예를 들어 가양성을 줄이기 위해 신뢰도 수준이 가장 높은 패턴과 일치 하도록 규칙의 정확도를 설정할 수 있습니다. 신뢰도 수준이 계산 되는 방식을 이해 하는 것이이 게시물의 범위를 벗어나 다소 복잡 하지만, [신뢰 수준을 사용 하 여 규칙을 조정 하는 방법](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy)에 대 한 자세한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p133">In addition to changing the instance count, you can also adjust the match accuracy (or confidence level). If your sensitive information type has multiple patterns, you can adjust the match accuracy in your rule, so that your rule matches only specific patterns. For example, to help reduce false positives, you can set the match accuracy of your rule so that it matches only the pattern with the highest confidence level. Understanding how confidence level is calculated is a bit tricky (and beyond the scope of this post), but here's a good explanation of [how to use confidence level to tune your rules](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy).</span></span>

<span data-ttu-id="fca1a-p134">마지막으로 좀 더 높은 수준의 고급을 가져오려면 중요 한 정보 유형을 사용자 지정 하면 됩니다. 예를 들어, [오스트레일리아 운전 면허](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number)의 키워드 목록에서 "시드니 NSW"를 제거 하 여 위에서 트리거된 가양성을 제거할 수 있습니다. XML 및 PowerShell을 사용 하 여이 작업을 수행 하는 방법에 대 한 자세한 내용은 [기본 제공 중요 한 정보 유형을 사용자 지정](customize-a-built-in-sensitive-information-type.md)하는 경우이 항목을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p134">Finally, if you want to get even a bit more advanced, you can customize any sensitive information type -- for example, you can remove "Sydney NSW" from the list of keywords for [Australian Driver's License](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number), to eliminate the false positive triggered above. To learn how to do this by using XML and PowerShell, see this topic on [customizing a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

## <a name="turn-off-a-dlp-policy"></a><span data-ttu-id="fca1a-260">DLP 정책 끄기</span><span class="sxs-lookup"><span data-stu-id="fca1a-260">Turn off a DLP policy</span></span>

<span data-ttu-id="fca1a-261">DLP 정책이 정확 하 고 효과적으로 중요 한 정보 유형을 검색 하 고 최종 사용자가 해당 정책에 따라 처리할 준비가 되 면이 정책을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-261">When you're happy that your DLP policy is accurately and effectively detecting sensitive information types, and that your end users are ready to deal with the policies being in place, then you can enable the policy.</span></span>

![정책을 설정 하는 옵션](media/DLP-create-test-tune-turn-on-policy.png)
 
<span data-ttu-id="fca1a-263">정책이 적용 될 시기를 확인 하려면 [Office 365 Security & 준수 센터 PowerShell에 연결](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) 하 고 [remove-dlpcompliancepolicy cmdlet](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) 을 실행 하 여 DistributionStatus를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="fca1a-263">If you're waiting to see when the policy will take effect, [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) and run the [Get-DlpCompliancePolicy cmdlet](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) to see the DistributionStatus.</span></span>

![PowerShell에서 cmdlet 실행](media/DLP-create-test-tune-PowerShell.png)

<span data-ttu-id="fca1a-p135">DLP 정책을 설정한 후에는 일부 최종 테스트를 실행 하 여 예상 되는 정책 작업이 진행 되 고 있는지 확인 해야 합니다. 신용 카드 데이터와 같은 항목을 테스트 하려는 경우 온라인 웹 사이트에 예제 신용 카드를 생성 하는 방법에 대 한 정보 및 검사를 통과 하 고 정책을 트리거하는 기타 개인 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p135">After turning on the DLP policy, you should run some final tests of your own to make sure that the expected policy actions are occurring. If you're trying to test things like credit card data, there are websites online with information on how to generate sample credit card or other personal information that will pass checksums and trigger your policies.</span></span>

<span data-ttu-id="fca1a-267">사용자 재정의를 허용 하는 정책은 정책 팁의 일부로 해당 옵션을 사용자에 게 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-267">Policies that allow user overrides will present that option to the user as part of the policy tip.</span></span>

![사용자 재정의를 허용 하는 정책 팁](media/DLP-create-test-tune-override-option.png)

<span data-ttu-id="fca1a-269">콘텐츠를 제한 하는 정책은 정책 팁의 일부로 사용자에 게 경고를 표시 하 고 전자 메일을 보내는 것을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1a-269">Policies that restrict content will present the warning to the user as part of the policy tip, and prevent them from sending the email.</span></span>

![콘텐츠가 제한 되는 정책 팁](media/DLP-create-test-tune-restrict-warning.png)

## <a name="summary"></a><span data-ttu-id="fca1a-271">요약</span><span class="sxs-lookup"><span data-stu-id="fca1a-271">Summary</span></span>

<span data-ttu-id="fca1a-p136">데이터 손실 방지 정책은 모든 유형의 조직에 유용 합니다. 일부 DLP 정책은 정책 팁, 최종 사용자 재정의 및 문제 보고서와 같은 제어 항목으로 인해 낮은 위험 수준으로 진행 됩니다. 일부 DLP 정책을 자동으로 테스트 하 여 조직에서 이미 발생 하 고 있는 위반 유형을 확인 한 다음, 허용 및 허용 되지 않는 작업을 사용자에 게 교육 한 후에는 다음에 대 한 dlp 정책을 롤아웃할 수 있습니다. 조직.</span><span class="sxs-lookup"><span data-stu-id="fca1a-p136">Data loss prevention policies are useful for organizations of all types. Testing some DLP policies is a low risk exercise due to the control you have over things like policy tips, end user overrides, and incident reports. You can quietly test some DLP policies to see what type of violations are already occurring in your organization, and then craft policies with low false positive rates, educate your users on what is allowed and not allowed, and then roll out your DLP policies to the organization.</span></span>
