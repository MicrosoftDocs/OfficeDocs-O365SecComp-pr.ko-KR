---
title: DLP 정책 만들기, 테스트 및 조정
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'DLP 정책을 사용 하 여 시작 하는 것이 가장 편리 하 고 가장 일반적인 방법은 Office 365에 포함 된 서식 파일 중 하나를 사용 하는 것입니다. '
ms.openlocfilehash: 1d4697811a5d8dd426fed80d3d60bcd2fbea6335
ms.sourcegitcommit: 42c7ad69f95fc4d2de13293b39cc44931b9f82e6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/14/2018
ms.locfileid: "26522790"
---
# <a name="create-test-and-tune-a-dlp-policy"></a><span data-ttu-id="b3fbc-103">DLP 정책 만들기, 테스트 및 조정</span><span class="sxs-lookup"><span data-stu-id="b3fbc-103">Create, test, and tune a DLP policy</span></span>

<span data-ttu-id="b3fbc-104">**보안 주체 작성자**</span><span class="sxs-lookup"><span data-stu-id="b3fbc-104">**Principal author**</span></span> </br>
<span data-ttu-id="b3fbc-105">Paul Cunningham, Microsoft MVP</span><span class="sxs-lookup"><span data-stu-id="b3fbc-105">Paul Cunningham, Microsoft MVP</span></span> </br>
[<span data-ttu-id="b3fbc-106">실제적인 365</span><span class="sxs-lookup"><span data-stu-id="b3fbc-106">Practical 365</span></span>](https://practical365.com/) </br>
[<span data-ttu-id="b3fbc-107">@Practical365</span><span class="sxs-lookup"><span data-stu-id="b3fbc-107">@Practical365</span></span>](https://twitter.com/practical365)</br>
__________________________________________________

<span data-ttu-id="b3fbc-p101">데이터 손실 방지는 원치 않는 당사자에 게 중요 한 정보의 의도적인 또는 실수로 노출 되지 않도록 하 여 조직의 도움이 되는 Office 365의 규정 준수 기능입니다. DLP에 Exchange Server와 Exchange Online에서 해당 루트가 하며 SharePoint Online 및 비즈니스용 OneDrive에 적용할 수 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p101">Data loss prevention is a compliance feature of Office 365 that is designed to help your organization prevent the intentional or accidental exposure of sensitive information to unwanted parties. DLP has its roots in Exchange Server and Exchange Online, and is also applicable in SharePoint Online and OneDrive for Business.</span></span>

<span data-ttu-id="b3fbc-p102">DLP 신용 카드 번호와 같은 중요 한 정보 및 개인 식별 정보 (pii 개인)에 대 한 자세한 내용은 전자 메일 메시지 및 파일의 내용을 검토 하는 콘텐츠 분석 엔진을 사용 합니다. 중요 한 정보 일반적으로 전자 메일을 전송 하거나 서는 안 전자 메일 메시지 또는 파일을 암호화와 같은 추가 단계를 수행 하지 않고 문서에 포함 합니다. DLP를 사용 하 여 중요 한 정보를 검색 하 고 다음과 같이 조치를 취할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p102">DLP uses a content analysis engine to examine the contents of email messages and files, looking for sensitive information such as credit card numbers and personally identifiable information (PII). Sensitive information should typically not be sent in email, or included in documents, without taking additional steps such as encrypting the email message or files. Using DLP you can detect sensitive information, and take action such as:</span></span>

- <span data-ttu-id="b3fbc-113">감사 목적에 대 한 이벤트를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-113">Log the event for auditing purposes</span></span>
- <span data-ttu-id="b3fbc-114">최종 사용자에 게 전자 메일을 보내는 또는 파일 공유는 경고를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-114">Display a warning to the end user who is sending the email or sharing the file</span></span>
- <span data-ttu-id="b3fbc-115">전자 메일 또는 파일 공유에서 수행할 적극적으로 차단</span><span class="sxs-lookup"><span data-stu-id="b3fbc-115">Actively block the email or file sharing from taking place</span></span>

<span data-ttu-id="b3fbc-p103">경우에 따라 고객 보호 해야 하는 데이터의 형식을 갖도록 자신을 고려해 보지 않았다고 때문에 DLP를 해제 합니다. 의료 기록 또는 금융 정보 등의 중요 한 데이터를만 있는지 온라인 저장소를 실행 하는 회사 또는 의료 산업에 대 한 것으로 가정 합니다. 하지만 실현 하지 자신이 하는 경우에 모든 비즈니스를 정기적으로 중요 한 정보를 처리할 수 있습니다. 직원 이름의 스프레드시트 및 생일의 시작 날짜는 고객 이름 및 신용 카드 세부 정보를 스프레드시트로 중요 한입니다. 및 이러한 유형의 정보는 직원의 일상적인 작업에 대 한 시스템에서 CSV 파일 내보내기의 경우 nothing 생각 하 고 다른 사람에 게 전자 메일 보내기 자동 이동으로 예상 보다 더 많이 주위에 배치할 경향이 있습니다. 또한 배울 수 있습니다 얼마나 자주 직원 같은 결과가 발생을 고려 하지 않고 신용 카드 또는 금융 세부 정보를 포함 하는 전자 메일을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p103">Sometimes customers dismiss DLP because they don't consider themselves to have the type of data that needs protecting. The assumption is that sensitive data, such as medical records or financial information, only exists for industries like health care or for companies that run online stores. But any business can handle sensitive information on a regular basis, even if they don't realize it. A spreadsheet of employee names and dates of birth is just as sensitive as a spreadsheet of customer names and credit card details. And this type of information tends to float around more than you might expect, as employees quietly go about their day to day tasks, thinking nothing of export a CSV file from a system and emailing it to someone. You might also be surprised how often employees send emails containing credit card or banking details without considering the consequences.</span></span>

## <a name="how-sensitive-information-is-detected-by-dlp"></a><span data-ttu-id="b3fbc-122">DLP 중요 한 정보를 검색 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b3fbc-122">How sensitive information is detected by DLP</span></span>

<span data-ttu-id="b3fbc-p104">중요 한 정보는 함께 근접 한 위치와 같은 다른 표시기로의 특정 키워드에 대 한 일치 패턴 정규식 (RegEx) 패턴 일치 하 여 식별 됩니다. 이 예는 신용 카드 번호입니다. VISA 신용 카드 번호는 16 자리 합니다. 그러나 이러한 자릿수 쓸 수-1111-이며-따라서, 예: 다양 한 방식에서 1111 1111 1111 1111 또는 1111111111111111 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p104">Sensitive information is identified by regular expression (RegEx) pattern matching, in combination with with other indicators such as the proximity of certain keywords to the matching patterns. An example of this is credit card numbers. A VISA credit card number has 16 digits. However, those digits can be written in different ways, such as 1111-1111-1111-1111, 1111 1111 1111 1111, or 1111111111111111.</span></span>

<span data-ttu-id="b3fbc-p105">임의의 16 자리 문자열은 반드시 신용 카드 번호 하지, 도움말 데스크 시스템 또는 하드웨어의 일련 번호가에서 티켓 번호를 일 수 있습니다. 신용 카드 번호와 치명적이 지 16 자리 문자열의 차이점을 구별 하는 계산은 번호에서 다양 한 신용 카드 브랜드에서 알려진된 패턴을 일치 하는지 확인 하려면 수행된 (체크섬) 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p105">Any 16 digit string is not necessarily a credit card number, it could be a ticket number from a help desk system, or a serial number of a piece of hardware. To tell the difference between a credit card number and a harmless 16-digit string, a calculation is performed (checksum) to confirm that the numbers match a known pattern from the various credit card brands.</span></span>

<span data-ttu-id="b3fbc-129">또한 신용 카드 만료 날짜를 있을 수 있는 날짜 값을 "VISA" 또는 "AMEX" 근접 한 위치와 같은 키워드의 근접 데이터 신용 카드 번호 인지 여부에 대 한 결정을 내리는 데도 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-129">Furthermore, the proximity of keywords such as “VISA” or “AMEX”, along with the proximity to date values that might be the credit card expiry date, is also considered to make a decision about whether the data is a credit card number or not.</span></span>

<span data-ttu-id="b3fbc-130">즉, DLP는 전자 메일에서 이러한 두 텍스트 간의 차이 인식할 수 있을 만큼 스마트 일반적으로:</span><span class="sxs-lookup"><span data-stu-id="b3fbc-130">In other words, DLP is usually smart enough to recognize the difference between these two texts in an email:</span></span>

- <span data-ttu-id="b3fbc-p106">"하면 주문할 수 나에 게 새 랩톱. 내 VISA 번호 1111-1111-1111-1111, 만료 11/22 사용할 수 있으며 있을 때 예상된 배달 날짜를 보내 합니다. "</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p106">“Can you order me a new laptop. Use my VISA number 1111-1111-1111-1111, expiry 11/22, and send me the estimated delivery date when you have it.”</span></span>
- <span data-ttu-id="b3fbc-p107">"내 랩톱 일련번호 2222 2222-2222 2222 이며 11/2010에서 구입 합니다. 방식으로 내 출장 visa 승인 되 아직 "?</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p107">“My laptop serial number is 2222-2222-2222-2222 and it was purchased on 11/2010. By the way, is my travel visa approved yet?”</span></span>

<span data-ttu-id="b3fbc-135">책갈피가 지정 된 변경 하지 않으려면 좋은 참조는 각 정보 유형에 검색 하는 방법에 대해 설명 하는이 [중요 한 정보 형식에 대 한 항목](what-the-sensitive-information-types-look-for.md) 입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-135">A good reference to keep bookmarked is this [topic on sensitive information types](what-the-sensitive-information-types-look-for.md) that explains how each information type is detected.</span></span>

## <a name="where-to-start-with-data-loss-prevention"></a><span data-ttu-id="b3fbc-136">데이터 손실 방지로 시작 하는 위치</span><span class="sxs-lookup"><span data-stu-id="b3fbc-136">Where to start with data loss prevention</span></span>

<span data-ttu-id="b3fbc-p108">데이터 유출의 위험 완전히 확실 하지 않으면 때 여기서 DLP 구현 된 시작할지 정확 하 게 수행 되려면 어렵습니다. 놓기만 DLP 정책 설정 하기 전에 해당 효율성 및 정확도 측정 수 있도록 "테스트 모드"에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p108">When the risks of data leakage aren't entirely obvious, it's difficult to work out where exactly you should start with implementing DLP. Fortunately, DLP policies can be run in “test mode”, allowing you to gauge their effectiveness and accuracy before you turn them on.</span></span>

<span data-ttu-id="b3fbc-p109">Exchange 관리 센터를 통해 Exchange Online에 대 한 DLP 정책을 관리할 수 있습니다. 하지만 이것은 무엇 I를 사용 하 여이 문서의 데모에 대 한 보안 및 규정 준수 센터를 통해 모든 작업에 대 한 DLP 정책을 구성할 수 있습니다. 보안 및 규정 준수 센터에서 **데이터 손실 방지**아래에서 DLP 정책을 찾을 수 > **정책**입니다. 시작 하려면 **정책 만들기** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p109">DLP policies for Exchange Online can be managed through the Exchange admin center. But you can configure DLP policies for all workloads through the Security & Compliance Center, so that's what I'll use for demonstrations in this article. In the Security & Compliance Center you'll find the DLP policies under **Data loss prevention** > **Policy**. Click on **Create a policy** to start.</span></span>

<span data-ttu-id="b3fbc-p110">Office 365 [DLP 정책 템플릿](what-the-dlp-policy-templates-include.md) DLP 정책 만들기를 사용할 수 있는 범위를 제공 합니다. 호주 비즈니스는 자신이 가정해 보겠습니다. 재무, 의료 및 상태 및 정보 공개의 일반 범주로 구분 하는 오스트레일리아와 관련 된 필드만 표시 하려면 정책 서식 파일을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p110">Office 365 provides a range of [DLP policy templates](what-the-dlp-policy-templates-include.md) you can use to create DLP policies. Let's say that you're an Australian business. You can filter the policy templates to display only those that are relevant to Australia, which fall into the general categories of Financial, Medical and Health, and Privacy.</span></span>

![국가 또는 지역을 선택 하는 옵션](media/DLP-create-test-tune-choose-country.png)

<span data-ttu-id="b3fbc-147">이 데모에 대 한 정보 유형의 호주 세금 파일 번호 (TFN) 및 운전 면허 번호를 포함 하는 오스트레일리아 개인 식별 정보 pii (개인) 데이터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-147">For this demonstration I'll choose Australian Personally Identifiable Information (PII) Data, which includes the information types of Australian Tax File Number (TFN) and Driver's License Number.</span></span>

![정책 서식 파일을 선택 하는 옵션](media/DLP-create-test-tune-choose-policy-template.png)

<span data-ttu-id="b3fbc-p111">새 DLP 정책 이름을 지정 합니다. 기본 이름을 DLP 정책 템플릿을 일치시킬지 하지만 동일한 서식 파일에서 여러 정책을 만들 수 있으므로, 자신만의 자세히 설명 하는 이름을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p111">Give your new DLP policy a name. The default name will match the DLP policy template, but you should choose a more descriptive name of your own, because multiple policies can be created from the same template.</span></span>

![사용자의 정책 이름을 지정 하는 옵션](media/DLP-create-test-tune-name-policy.png)

<span data-ttu-id="b3fbc-p112">정책에 적용 되는 위치를 선택 합니다. DLP 정책을 Exchange Online, SharePoint Online 및 비즈니스용 OneDrive를 적용할 수 있습니다. 모든 위치에 적용할 구성 된이 정책을 유지 하도록 하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p112">Choose the locations that the policy will apply to. DLP policies can apply to Exchange Online, SharePoint Online, and OneDrive for Business. I am going to leave this policy configured to apply to all locations.</span></span>

![모든 위치를 선택 하는 옵션](media/DLP-create-test-tune-choose-locations.png)

<span data-ttu-id="b3fbc-p113">방금 첫번째 **정책 설정** 단계에서 지금에 대 한 기본값을 적용 합니다. 사용자 지정 DLP 정책에서 수행할 수 있는 작업의 많은 이지만 경우 기본값은 미세 장소를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p113">At the first **Policy Settings** step just accept the defaults for now. There is quite a lot of customization you can do in DLP policies, but the defaults are a fine place to start.</span></span>

![보호 하기 위해 콘텐츠 형식의 사용자 지정 하는 옵션](media/DLP-create-test-tune-default-customization-settings.png)

<span data-ttu-id="b3fbc-p114">**다음** 을 클릭 한 후 더 많은 사용자 지정 옵션을 포함 한 추가 **정책 설정** 페이지와 함께 표시 됩니다. 방금 테스트 하는 정책에 대 한 방법은 조정이 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p114">After clicking **Next** you'll be presented with an additional **Policy Settings** page with more customization options. For a policy that you are just testing, here's where you can start to make some adjustments.</span></span>

- <span data-ttu-id="b3fbc-p115">이제는만 있는 것을 테스트 하 고 사용자에 게 아직 아무것도 표시 하지 않으려는 경우에 적절 한 단계에 대 한 정책 팁을 해제 했을 때 I. 정책 팁 DLP 정책 위반을 대 한 정보는 사용자에 게 경고를 표시 합니다. 예: Outlook 사용자 연결 했을 때 이러한 파일 신용 카드 번호를 포함 하는 경고가 표시 및 거부를 전자 메일 포함 될 합니다. 정책 팁의 목적은 발생 하기 전에 비준수 동작을 중지 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p115">I've turned off policy tips for now, which is a reasonable step to take if you're just testing things out and don't want to display anything to users yet. Policy tips display warnings to users that they're about to violate a DLP policy. For example, an Outlook user will see a warning that the file they've attached contains credit card numbers and will cause their email to be rejected. The goal of policy tips is to stop the non-compliant behaviour before it happens.</span></span>
- <span data-ttu-id="b3fbc-165">이 정책을 모든 공유 하지 방금 대량 데이터의 공유 오스트레일리아 PII 데이터를 검색 하에 1, 10에서 인스턴스의 수를 감소 했을 때 I 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-165">I've also decreased the number of instances from 10 to 1, so that this policy will detect any sharing of Australian PII data, not just bulk sharing of the data.</span></span>
- <span data-ttu-id="b3fbc-166">문제 보고서 전자 메일에 다른 받는 사람을 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-166">I've also added another recipient to the incident report email.</span></span>

![추가 정책 설정](media/DLP-create-test-tune-more-policy-settings.png)

<span data-ttu-id="b3fbc-p116">마지막으로, 처음 테스트 모드에서 실행 하도록이 정책을 구성 했습니다. 여기 테스트 모드에 있는 동안 정책 팁을 사용 하지 않도록 설정 하는 옵션은 또한 알 수 있습니다. 이 정책에서 사용 하도록 설정 하는 정책 팁 되었지만를 표시 하거나 표시 되지 않도록의 테스트를 진행 하는 동안 여부를 결정 하는 융통성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p116">Finally, I've configured this policy to run in test mode initially. Notice there's also an option here to disable policy tips while in test mode. This gives you the flexibility to have policy tips enabled in the policy, but then decide whether to show or suppress them during your testing.</span></span>

![정책을 먼저 테스트 하는 옵션](media/DLP-create-test-tune-test-mode.png)

<span data-ttu-id="b3fbc-172">최종 검토 화면에서 정책 만들기를 종료 하려면 **만들기** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-172">On the final review screen click **Create** to finish creating the policy.</span></span>

## <a name="test-a-dlp-policy"></a><span data-ttu-id="b3fbc-173">DLP 정책 테스트</span><span class="sxs-lookup"><span data-stu-id="b3fbc-173">Test a DLP policy</span></span>

<span data-ttu-id="b3fbc-p117">새 DLP 정책에 따라 1 시간 약 이내에 적용 되기 시작 합니다. 배치 하 고 일반 사용자 작업에 의해 트리거되도록 기다립니다 또는 사용자가 직접 트리거하 시킬 수 있습니다. 이전 I이 [중요 한 정보 형식에 대 한 항목](what-the-sensitive-information-types-look-for.md)을 DLP 일치 하는 결과 트리거하는 방법에 대 한 정보를 제공 하는에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p117">Your new DLP policy will begin to take effect within about 1 hour. You can sit and wait for it to be triggered by normal user activity, or you can try to trigger it yourself. Earlier I linked to this [topic on sensitive information types](what-the-sensitive-information-types-look-for.md), which provides you with information about how to trigger DLP matches.</span></span>

<span data-ttu-id="b3fbc-p118">한 예로이 문서에 대해 만든 I DLP 정책에는 호주 세금 파일 번호 (TFN)을 검색 합니다. 설명서에 따라 다음 조건에 일치 하는 삼고 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p118">As an example, the DLP policy I created for this article will detect Australian tax file numbers (TFN). According to the documentation, the match is based on the following criteria.</span></span>

![호주 세금 파일 번호에 대 한 설명서](media/DLP-create-test-tune-Australia-Tax-File-Number-doc.png)
 
<span data-ttu-id="b3fbc-p119">대신 뭉툭한 방식으로 TFN 감지를 설명 하기 위해 단어 "세금 파일 번호"가 있는 전자 메일 및 가까운 위치에 9 숫자 문자열은 항해를 통해 문제 없이 합니다. DLP 정책 이벤트가 트리거되지 않습니다 이유는 9 자리 문자열 유효한 TFN 이며 뿐아니라 치명적이 지 문자열로 숫자를 나타내는 체크섬을 통과 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p119">To demonstrate TFN detection in a rather blunt manner, an email with the words “Tax file number” and a 9 digit string in close proximity will sail through without any issues. The reason it does not trigger the DLP policy is that the 9-digit string must pass the checksum that indicates it is a valid TFN and not just a harmless string of numbers.</span></span>

![체크섬을 통과 하지 않는 호주 세금 파일 번호](media/DLP-create-test-tune-email-test1.png)

<span data-ttu-id="b3fbc-p120">비교에서 단어 "세금 파일 번호"가 있는 전자 메일 및 체크섬을 전달 하는 유효한 TFN 정책을 트리거합니다. 여기 레코드에 대 한 사용 하 고 TFN 찍은 생성 하는 웹사이트에서 유효 하지만 정품 아님 TFNs 합니다. [유효 하지만 위조 신용 카드 번호](http://www.fakecreditcardgenerator.net/)를 생성 하는 유사한 사이트 있습니다. 이러한 사이트는 위조와 숫자를 유효 하지 하 고 체크섬을 전달 하지 않습니다 (따라서 정책을 트리거하지 않습니다)를 사용 하는 DLP 정책을 테스트할 때 가장 일반적인 실수 중 하나 때문에 매우 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p120">In comparison, an email with the words “Tax file number” and a valid TFN that passes the checksum will trigger the policy. For the record here, the TFN I'm using was taken from a website that generates valid, but not genuine, TFNs. There are similar sites that generate [valid but fake credit card numbers](http://www.fakecreditcardgenerator.net/). Such sites are very useful because one of the most common mistakes when testing a DLP policy is using a fake number that's not valid and won't pass the checksum (and therefore won't trigger the policy).</span></span>

![체크섬을 전달 하는 호주 세금 파일 번호](media/DLP-create-test-tune-email-test2.png)

<span data-ttu-id="b3fbc-188">문제 보고서 전자 메일 검색 된 중요 한 정보 유형, 얼마나 많은 인스턴스 검색 된 및이 검색의 신뢰도 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-188">The incident report email includes the type of sensitive information that was detected, how many instances were detected, and the confidence level of the detection.</span></span>

![세금 파일 번호를 표시 하는 문제 보고서 감지](media/DLP-create-test-tune-email-incident-report.png)

<span data-ttu-id="b3fbc-p121">DLP 정책에 따라 테스트 모드에서 나가기 문제 보고서 전자 메일을 분석 하는 경우에 DLP 정책 및 얼마나 효과적인 지는 것이 적용 되는의 정확성에 대 한 이해할 수 있도록 시작할 수 있습니다. 문제 보고서 외에도 테 넌 트 간에 정책 일치 항목의 집계 보기를 확인 하려면 [DLP 보고서를 사용 하 여](view-the-dlp-reports.md) 을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p121">If you leave your DLP policy in test mode and analyze the incident report emails, you can start to get a feel for the accuracy of the DLP policy and how effective it will be when it is enforced. In addition to the incident reports, you can [use the DLP reports](view-the-dlp-reports.md) to see an aggregated view of policy matches across your tenant.</span></span>

## <a name="tune-a-dlp-policy"></a><span data-ttu-id="b3fbc-192">DLP 정책 조정</span><span class="sxs-lookup"><span data-stu-id="b3fbc-192">Tune a DLP policy</span></span>

<span data-ttu-id="b3fbc-p122">정책 적중을 분석할 때 정책이 작동 하는 방식에 따라 일부 조정 하는 것이 좋습니다. 간단한 예로 전자 메일에 하나의 TFN (것 생각 하 고 여전히, 아니지만 데모를 위해와 보겠습니다) 문제, 수 없지만 둘 이상의 인스턴스는 문제를 결정할 수 있습니다. 여러 인스턴스 외부 회계 서비스 같은 외부 업체에 HR 데이터베이스에서 CSV 내보내기 이메일을 보내 직원 등 위험한 시나리오 될 수 있습니다. 임이 확실 무언가 감지 하 여 차단 것이 좋은 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p122">As you analyze your policy hits you might want to make some adjustments to how the policies behave. As a simple example, you might determine that one TFN in email is not a problem (I think it still is, but let's go with it for the sake of demonstration), but two or more instances is a problem. Multiple instances could be a risky scenario such as an employee emailing a CSV export from the HR database to an external party, for example an external accounting service. Definitely something you would prefer to detect and block.</span></span>

<span data-ttu-id="b3fbc-197">보안 및 규정 준수 센터의 동작을 조정 하려면 기존 정책을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-197">In the Security & Compliance Center you can edit an existing policy to adjust the behaviour.</span></span>

![정책 편집 하려면 옵션](media/DLP-create-test-tune-edit-policy.png)
 
<span data-ttu-id="b3fbc-199">특정 작업에만 또는 특정 사이트 및 계정 정책을 적용 되도록 위치 설정을 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-199">You can adjust the location settings so that the policy is applied only to specific workloads, or to specific sites and accounts.</span></span>

![특정 위치를 선택 하는 옵션](media/DLP-create-test-tune-edit-locations.png)

<span data-ttu-id="b3fbc-201">정책 설정을 조정 하 고 필요에 맞게 규칙을 편집할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-201">You can also adjust the policy settings and edit the rules to better suit your needs.</span></span>

![규칙을 편집 하는 옵션](media/DLP-create-test-tune-edit-rule.png)

<span data-ttu-id="b3fbc-203">DLP 정책 내에서 규칙을 편집 하는 경우 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-203">When editing a rule within a DLP policy you can change:</span></span>

- <span data-ttu-id="b3fbc-204">유형 및 규칙을 트리거하는 중요 한 데이터의 인스턴스 수를 포함 하는 조건.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-204">The conditions, including the type and number of instances of sensitive data that will trigger the rule.</span></span>
- <span data-ttu-id="b3fbc-205">작업 수행 되는 내용에 대 한 액세스를 제한 하는 등입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-205">The actions that are taken, such as restricting access to the content.</span></span>
- <span data-ttu-id="b3fbc-206">사용자 알림-은 자신의 전자 메일 클라이언트 또는 웹 브라우저에서 사용자에 게 표시 되는 정책 팁입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-206">User notifications, which are policy tips that are displayed to the user in their email client or web browser.</span></span>
- <span data-ttu-id="b3fbc-207">사용자가 자신의 전자 메일 또는 파일 공유를 계속 진행 하도록 선택할 수 있는지 여부를 결정 하는 사용자 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-207">User overrides, which determines whether users can choose to proceed with their email or file sharing anyway.</span></span>
- <span data-ttu-id="b3fbc-208">문제 보고서를 관리자에 게 알려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-208">Incident reports, to notify administrators.</span></span>

![규칙의 부분을 편집 하는 옵션](media/DLP-create-test-tune-editing-options.png)

<span data-ttu-id="b3fbc-p123">이 데모에서는 사용자 알림 (적절 한 사용자를 위한 교육 없이 이렇게 주의 해야) 정책에 추가 했을 때 I 및 사용자가 업무상의 이유에 또는 가양성으로 플래그를 지정 하 여 정책을 재정의 하도록 허용 합니다. Note 조직의 정책에 대 한 추가 정보를 포함 하거나 질문이 있는 경우 지원 서비스에 문의 하는 사용자의 메시지를 표시 하려는 경우 전자 메일 및 정책 팁 텍스트도 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p123">For this demonstration I've added user notifications to the policy (be careful of doing this without adequate user awareness training), and allowed users to override the policy with a business justification or by flagging it as a false positive. Note that you can also customize the email and policy tip text if you want to include any additional information about your organization's policies, or prompt users to contact support if they have questions.</span></span>

![사용자 알림 및 재정의 대 한 옵션](media/DLP-create-test-tune-user-notifications.png)

<span data-ttu-id="b3fbc-p124">높은 볼륨 및 낮은 볼륨의 처리에 대 한 두 규칙을 포함 하는 정책, 원하는 작업에 모두 편집 해야 합니다. 이 경우 해당 특성에 따라 다르게 처리 하는 기회입니다. 예, 낮은 볼륨 위반에 대 한 재정의 허용 하지만 높은 볼륨 위반에 대 한 재정의 허용 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p124">The policy contains two rules for handling of high volume and low volume, so be sure to edit both with the actions that you want. This is an opportunity to treat cases differently depending on their characteristics. For example, you might allow overrides for low volume violations, but not allow overrides for high volume violations.</span></span>

![높은 볼륨 및 낮은 볼륨에 대 한 규칙에 대 한 규칙을 하나](media/DLP-create-test-tune-two-rules.png)

<span data-ttu-id="b3fbc-217">또한 실제로 차단 또는 정책 위반에 있는 콘텐츠에 액세스를 제한 하려는 경우 그렇게 규칙에 대 한 동작을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-217">Also, if you want to actually block or restrict access to content that is in violation of policy, you need to configure an action on the rule to do so.</span></span>

![콘텐츠에 대 한 액세스를 제한 하는 옵션](media/DLP-create-test-tune-restrict-access-action.png)

<span data-ttu-id="b3fbc-p125">정책 설정에 이러한 변경 내용을 저장 후도 반환 하는 정책에 대 한 기본 설정 페이지로 고 정책을 테스트 모드에 있는 동안 사용자에 게 정책 팁을 표시 하는 옵션을 사용 하도록 설정 해야 합니다. 이것이 최종 사용자에 게 DLP 정책의 소개 하 고 사용자를 위한 교육, 너무 많은 경우 가양성 생산성이 영향을 줄 위험 없이 수행 하는 효과적인 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p125">After saving those changes to the policy settings, I also need to return to the main settings page for the policy and enable the option to show policy tips to users while the policy is in test mode. This is an effective way to introduce DLP policies to your end users, and do user awareness training, without risking too many false positives that impact their productivity.</span></span>

![테스트 모드에서 정책 팁을 표시 하려면 옵션](media/DLP-create-test-tune-show-policy-tips.png)

<span data-ttu-id="b3fbc-p126">서버 쪽 (또는 클라우드 쪽 원할 경우)에서 변경 될 수 있습니다 하지 즉시 적용, 다양 한 처리 간격으로 인해 합니다. 사용자에 게 새 정책 팁을 표시 하는 DLP 정책 변경, 걸 하는 경우 사용자는 즉시 적용 24 시간 마다 정책 변경 내용을 확인 하는 자신의 Outlook 클라이언트에서 변경 된 내용을 나타나지 않을 수 없습니다. 테스트에 대해 속도 작업 하려는 경우에 [PolicyNudges 키에서 마지막 다운로드 타임 스탬프를](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451)지우려면이 레지스트리 수정 프로그램을 사용할 수 있습니다. Outlook 최신 정책 정보 다시 시작 하 고 전자 메일 메시지를 작성을 시작 하면 다음 번에 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p126">On the server side (or cloud side if you prefer), the change may not take effect immediately, due to various processing intervals. If you're making a DLP policy change that will display new policy tips to a user, the user may not see the changes take effect immediately in their Outlook client, which checks for policy changes every 24 hours. If you want to speed things up for testing, you can use this registry fix to [clear the last download time stamp from the PolicyNudges key](https://support.microsoft.com/en-au/help/2823261/changes-to-a-data-loss-prevention-policy-don-t-take-effect-in-outlook?__hstc=18650278.46377037dc0a82baa8a30f0ef07a7b2f.1538687978676.1538693509953.1540315763430.3&__hssc=18650278.1.1540315763430&__hsfp=3446956451). Outlook will download the latest policy information the next time you restart it and begin composing an email message.</span></span>

<span data-ttu-id="b3fbc-226">사용 하도록 설정 하는 정책 팁을 설치한 경우 발생 하는 경우 가양성을 보고할 수로 사용자 Outlook에서 팁을 참조 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-226">If you have policy tips enabled, the user will begin to see the tips in Outlook, and can report false positives to you when they occur.</span></span>

![정책 팁 가양성 보고 하는 옵션](media/DLP-create-test-tune-policy-tip-in-outlook.png)

## <a name="investigate-false-positives"></a><span data-ttu-id="b3fbc-228">가양성 조사</span><span class="sxs-lookup"><span data-stu-id="b3fbc-228">Investigate false positives</span></span>

<span data-ttu-id="b3fbc-p127">DLP 정책 템플릿께 바로 완벽 하지 않습니다. 찾을 수 있으므로 방식을 DLP 배포에 쉽게 하는 것이 중요 이유는 환경에서 발생 일부 가양성 적절 하 게 테스트 하 고 정책에 조정 하는 시간을 라인 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p127">DLP policy templates are not perfect straight out of the box. It's likely that you'll find some false positives occurring in your environment, which is why it's so important to ease your way into a DLP deployment, taking the time to adequately test and tune your policies.</span></span>

<span data-ttu-id="b3fbc-p128">가양성의 예는 다음과 같습니다. 이 전자 메일은 매우 치명적이 지입니다. 사용자를 다른 사람에 게 자신의 휴대폰 번호를 제공 하 이며 자신의 전자 메일 서명을 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p128">Here's an example of a false positive. This email is quite harmless. The user is providing their mobile phone number to someone, and including their email signature.</span></span>

![잘못 된 양의 정보를 표시 하는 전자 메일](media/DLP-create-test-tune-false-positive-email.png)
 
<span data-ttu-id="b3fbc-235">경고 전자 메일 중요 한 정보를 포함 하는 정책 팁 사용자에 게 표시 하지만 특히, 호주 운전 면허 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-235">But the user sees a policy tip warning them that the email contains sensitive information, specifically, an Australian driver's license number.</span></span>

![정책 팁의 가양성 보고 하는 옵션](media/DLP-create-test-tune-policy-tip-closeup.png)

<span data-ttu-id="b3fbc-p129">사용자는 가양성을 보고할 수 및 관리자가 발생 한 이유를 찾을 수 있습니다. 문제 보고서 전자 메일에서 전자 메일 가양성으로 플래그가 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p129">The user can report the false positive, and the administrator can look into why it has occurred. In the incident report email, the email is flagged as a false positive.</span></span>

![문제 보고서 보여주는 가양성](media/DLP-create-test-tune-false-positive-incident-report.png)

<span data-ttu-id="b3fbc-p130">이 드라이버의 라이선스 대/소문자에 깊이를 좋은 예입니다. 이 가양성이 발생 한 이유는 "오스트레일리아 드라이버 라이센스" 유형 (하나라도 10 자리 문자열의 일부인), 9 자리 문자열을 통해 트리거될 "시드니 nsw" 키워드를 300 자 근접 내 (하지 대/소문자 구분)입니다. 따라서 시드니에 있는 것으로 수행 되는 사용자 때문에 전화 번호 및 전자 메일 서명 하 여 트리거되는 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p130">This driver's license case is a good example to dig into. The reason this false positive has occurred is that the “Australian Driver's License” type will be triggered by any 9-digit string (even one that is part of a 10-digit string), within 300 characters proximity to the keywords “sydney nsw” (not case sensitive). So it's triggered by the phone number and email signature, only because the user happens to be in Sydney.</span></span>

<span data-ttu-id="b3fbc-p131">특히, "시드니, NSW" 쉼표가 있는지 확인, DLP 정책 발생 하지 않습니다. I 잘 이유에 쉼표를 사용 하면 여기에 차이 및 이유 다른 도시 및 오스트레일리아에서 상태 호주 운전 라이선스 정보 종류에 대 한 키워드에 포함 되지 않습니다 되지만 이동 하는 다음과 같은 모릅니다. 따라서 수는 어떤 것에 대 한? 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p131">Interestingly, if “Sydney, NSW” has a comma, the DLP policy is not triggered. I have no idea why a comma makes any difference here, nor why other cities and states in Australia aren't included in the keywords for the Australian driver's license information type, but there you go. So, what can we do about it? There's a couple of options.</span></span>

<span data-ttu-id="b3fbc-p132">한 가지 방법은 호주 운전 라이선스 정보 유형을 정책에서 제거 합니다. DLP 정책 서식 파일의 일부 이므로 여기에는 우리는 반드시 사용 하지 않아도 사용할 수 있지만 합니다. 세금 파일 번호와 하지 드라이버의 라이선스에만 관심이 하는 경우만 제거할 수 있습니다. 예, 정책의 낮은 볼륨 규칙에서 제거 수 있지만 여러 드라이버 라이선스 목록이 여전히 인식 되도록 높은 볼륨 규칙에 둡니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p132">One option is to remove the Australian driver's license information type from the policy. It's in there because it's part of the DLP policy template, but we're not forced to use it. If you're only interested in Tax File Numbers and not driver's licenses, you can just remove it. For example, you can remove it from the low volume rule in the policy, but leave it in the high volume rule so that lists of multiple drivers licenses are still detected.</span></span>

![규칙에서 중요 한 정보 형식을 삭제 하려면 옵션](media/DLP-create-test-tune-delete-low-volume-rule.png)
 
<span data-ttu-id="b3fbc-252">인스턴스를 여러개 있는 경우에 드라이버의 라이선스 낮은 볼륨 됨 되도록 단순히 인스턴스 수가 증가 하는 방법도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-252">Another option is to simply increase the instance count, so that a low volume of driver's licenses is only detected when there are multiple instances.</span></span>

![인스턴스 수를 편집 하려면 옵션](media/DLP-create-test-tune-edit-instance-count.png)

<span data-ttu-id="b3fbc-p133">인스턴스 수를 변경 하는 것 외에도 일치 하는 정확도 (또는 신뢰도)을 조정할 수 있습니다. 중요 한 정보 유형의 패턴은 여러, 프로그램 규칙과 일치 하는 특정 패턴만 있도록 하면 규칙에 일치 하는 정확도 조정할 수 있습니다. 예를 가양성을 줄이려면 설정할 수 있습니다 규칙의 일치 하는 정확도 가장 높은 신뢰도가 패턴만 일치 하도록 합니다. 신뢰도 계산 하는 방법을 이해 까다로운 (및이 게시물의 범위를 벗어납니다), 이지만 [신뢰 수준을 조정 규칙을 사용 하는 방법](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy)에 대 한 적절 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p133">In addition to changing the instance count, you can also adjust the match accuracy (or confidence level). If your sensitive information type has multiple patterns, you can adjust the match accuracy in your rule, so that your rule matches only specific patterns. For example, to help reduce false positives, you can set the match accuracy of your rule so that it matches only the pattern with the highest confidence level. Understanding how confidence level is calculated is a bit tricky (and beyond the scope of this post), but here's a good explanation of [how to use confidence level to tune your rules](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#match-accuracy).</span></span>

<span data-ttu-id="b3fbc-p134">가져올 좀더 자세한도 하는 경우 마지막으로, 모든 중요 한 정보 유형 사용자 지정할 수 있습니다, 고급 따로 등의 키워드 대 한 [호주 운전 라이선스](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number), 위에 트리거한 가양성을 제거 하려면 목록에서 "시드니 NSW"를 제거할 수 있습니다. XML 및 PowerShell을 사용 하 여이 작업을 수행 하는 방법을 알아보려면 [기본 제공 중요 한 정보 유형 사용자 지정](customize-a-built-in-sensitive-information-type.md)에서이 항목을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p134">Finally, if you want to get even a bit more advanced, you can customize any sensitive information type -- for example, you can remove "Sydney NSW" from the list of keywords for [Australian Driver's License](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for#australia-drivers-license-number), to eliminate the false positive triggered above. To learn how to do this by using XML and PowerShell, see this topic on [customizing a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

## <a name="turn-off-a-dlp-policy"></a><span data-ttu-id="b3fbc-260">DLP 정책 끄기</span><span class="sxs-lookup"><span data-stu-id="b3fbc-260">Turn off a DLP policy</span></span>

<span data-ttu-id="b3fbc-261">때 했으면 DLP 정책은 정확 하 게 하 고 효과적으로 중요 한 정보 유형 및 최종 사용자에 게 전체에서 되 고 정책을 사용 하 여 처리 하기 위해 준비가 하 여 검색을 다음 수의 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-261">When you're happy that your DLP policy is accurately and effectively detecting sensitive information types, and that your end users are ready to deal with the policies being in place, then you can enable the policy.</span></span>

![정책 설정 하는 옵션](media/DLP-create-test-tune-turn-on-policy.png)
 
<span data-ttu-id="b3fbc-263">정책 됩니다 [하 고 Office 365 보안 및 규정 준수 센터 PowerShell 연결](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) 을 적용 하 고는 DistributionStatus를 참조 [하면 DlpCompliancePolicy cmdlet](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) 을 실행 하는 경우 참조을 기다리는 중 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-263">If you're waiting to see when the policy will take effect, [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps) and run the [Get-DlpCompliancePolicy cmdlet](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/get-dlpcompliancepolicy?view=exchange-ps) to see the DistributionStatus.</span></span>

![Powershell에서 cmdlet을 실행합니다.](media/DLP-create-test-tune-PowerShell.png)

<span data-ttu-id="b3fbc-p135">DLP 정책을 켜서 후 일부 최종 테스트 하도록 자신만의 예상된 정책 작업 수행 하는지를 실행 해야 합니다. 신용 카드 데이터 등의 작업을 테스트 하려는 경우 온라인으로 웹사이트 샘플 신용 카드를 생성 하는 방법에 대 한 정보 또는 기타 개인 정보 전달 체크섬을 트리거 (영문) 정책에 있는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p135">After turning on the DLP policy, you should run some final tests of your own to make sure that the expected policy actions are occurring. If you're trying to test things like credit card data, there are websites online with information on how to generate sample credit card or other personal information that will pass checksums and trigger your policies.</span></span>

<span data-ttu-id="b3fbc-267">사용자 재정의 허용 하는 정책을 정책 팁의 일부로 사용자에 게 해당 옵션을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-267">Policies that allow user overrides will present that option to the user as part of the policy tip.</span></span>

![사용자 재정의 허용 하는 정책 팁](media/DLP-create-test-tune-override-option.png)

<span data-ttu-id="b3fbc-269">콘텐츠를 제한 하는 정책 정책 팁의 일부로 사용자에 게 경고를 표시 하 고 전자 메일을 보내는에서 금지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-269">Policies that restrict content will present the warning to the user as part of the policy tip, and prevent them from sending the email.</span></span>

![정책 팁을 콘텐츠 제한 됩니다.](media/DLP-create-test-tune-restrict-warning.png)

## <a name="summary"></a><span data-ttu-id="b3fbc-271">요약</span><span class="sxs-lookup"><span data-stu-id="b3fbc-271">Summary</span></span>

<span data-ttu-id="b3fbc-p136">데이터 손실 방지 정책은 모든 유형의 조직에 유용 합니다. 일부 DLP 정책을 테스트는 정책 팁, 최종 사용자 재정 및 문제 보고서 등의 작업을 많이 제어로 인해 낮은 위험 수준의 연습 합니다. 조직에서 이미 발생 하는 어떤 유형의 위반으로 인해를 참조 하는 일부 DLP 정책을 자동으로 테스트할 수 있습니다 하 고 다음 크 정책의 경우 false 양의 비율이 낮은, 허용 되는 항목과 허용 되지에 사용자를 교육 하 고 다음에 DLP 정책에는 조직입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fbc-p136">Data loss prevention policies are useful for organizations of all types. Testing some DLP policies is a low risk exercise due to the control you have over things like policy tips, end user overrides, and incident reports. You can quietly test some DLP policies to see what type of violations are already occurring in your organization, and then craft policies with low false positive rates, educate your users on what is allowed and not allowed, and then roll out your DLP policies to the organization.</span></span>
