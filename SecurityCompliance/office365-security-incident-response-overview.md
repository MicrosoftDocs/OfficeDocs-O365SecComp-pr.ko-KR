---
title: Office 365 보안 사고 대응
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/27/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: 이 솔루션은 가장 일반적인 사이버 보안 공격이 Office 365에서 어떤 방식으로 표시 될 수 있는지와이에 대처 하는 방법을 알려줍니다.
ms.openlocfilehash: ac0a61e31f50846547517d721456a5229a7fb64c
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223287"
---
# <a name="office-365-security-incident-response"></a><span data-ttu-id="ed68a-103">Office 365 보안 사고 대응</span><span class="sxs-lookup"><span data-stu-id="ed68a-103">Office 365 Security Incident Response</span></span>

 <span data-ttu-id="ed68a-104">**요약:** 이 솔루션은 Office 365에서 가장 일반적인 사이버 보안 공격에 대 한 지표, 지정 된 공격을 확실 하 게 확인 하는 방법 및 응답 하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-104">**Summary:** This solution tells you what the indicators are for the most common cyber-security attacks in Office 365, how to positively confirm any given attack, and how to respond to it.</span></span>
  
## <a name="overview"></a><span data-ttu-id="ed68a-105">개요</span><span class="sxs-lookup"><span data-stu-id="ed68a-105">Overview</span></span>
<span data-ttu-id="ed68a-p101">모든 사이버 공격이 thwarted 수 있는 것은 아닙니다. 공격자가 방어 전략의 새로운 약점을 지속적으로 찾고 있거나 이전 버전을 이용 하 고 있습니다. 공격을 인식 하는 방법을 알면 보다 신속 하 게 응답 하 여 보안 인시던트 기간을 단축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-p101">Not all cyber attacks can be thwarted. Attackers are constantly looking for new weaknesses in your defensive strategy or they are exploiting old ones. Knowing how to recognize an attack allows you to respond to it faster, which shortens the duration of the security incident.</span></span>

<span data-ttu-id="ed68a-p102">이 문서 시리즈는 Office 365에서 특정 유형의 공격을 이해 하 고이를 처리할 수 있는 단계를 제공 하는 데 도움이 됩니다. 다음은 이해를 위한 빠른 입력 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-p102">This series of article helps you understand what a particular type of attack might look like in Office 365 and gives you steps you can take to respond. They are quick entry points to understanding:</span></span>
 
- <span data-ttu-id="ed68a-111">공격과 공격 방식 및 작동 방식</span><span class="sxs-lookup"><span data-stu-id="ed68a-111">What the attack is and how it works.</span></span>
- <span data-ttu-id="ed68a-112">찾을 대상 및 해당 항목을 찾는 방법에 대 한 손상 표시기 (IOC)입니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-112">What signs, called indicators of compromise (IOC), to look for and how to look for them.</span></span>
- <span data-ttu-id="ed68a-113">공격을 적극적으로 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ed68a-113">How to positively confirm the attack.</span></span>
- <span data-ttu-id="ed68a-114">나중에 공격을 중단 하 고 조직을 보다 효율적으로 보호 하기 위해 수행 해야 하는 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-114">Steps to take to cut off the attack and better protect your organization in the future.</span></span>
- <span data-ttu-id="ed68a-115">각 공격 유형에 대 한 자세한 정보로 연결 되는 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-115">Links to in-depth information on each attack type.</span></span>

<span data-ttu-id="ed68a-116">시간이 지남에 따라 추가 되는 문서를 매달 다시 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="ed68a-116">Check back here monthly as more articles will be added over time.</span></span>

## <a name="detect-and-remediate-articles"></a><span data-ttu-id="ed68a-117">문서 검색 및 수정</span><span class="sxs-lookup"><span data-stu-id="ed68a-117">Detect and remediate articles</span></span>

- [<span data-ttu-id="ed68a-118">Office 365에서 불법 동의 권한 부여 검색 및 교정</span><span class="sxs-lookup"><span data-stu-id="ed68a-118">Detect and Remediate Illicit Consent Grants in Office 365</span></span>](detect-and-remediate-illicit-consent-grants.md)
- [<span data-ttu-id="ed68a-119">Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성</span><span class="sxs-lookup"><span data-stu-id="ed68a-119">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)
 
## <a name="incident-response-articles"></a><span data-ttu-id="ed68a-120">인시던트 대응 문서</span><span class="sxs-lookup"><span data-stu-id="ed68a-120">Incident response articles</span></span>

- [<span data-ttu-id="ed68a-121">Office 365에서 손상된 이메일 계정에 응답</span><span class="sxs-lookup"><span data-stu-id="ed68a-121">Responding to a Compromised Email Account in Office 365</span></span>](responding-to-a-compromised-email-account.md)

## <a name="secure-office-365-like-a-cybersecurity-pro"></a><span data-ttu-id="ed68a-122">cybersecurity pro와 같은 Office 365 보호</span><span class="sxs-lookup"><span data-stu-id="ed68a-122">Secure Office 365 like a cybersecurity pro</span></span>
<span data-ttu-id="ed68a-p103">Office 365 구독에는 데이터와 사용자를 보호 하는 데 사용할 수 있는 강력한 보안 기능 집합이 포함 되어 있습니다.  office 365 보안 로드맵: office 365 테 넌 트를 보호 하기 위한 Microsoft 권장 모범 사례를 구현 하는 데 [처음 30 일, 90 일 및 그 이상에 대 한 주요 우선 순위](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-p103">Your Office 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.  Use the [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) to implement Microsoft recommended best practices for securing your Office 365 tenant.</span></span>
- <span data-ttu-id="ed68a-p104">처음 30 일 이내에 수행 해야 하는 작업입니다.  이러한 설정은 즉시 영향을 미치며 사용자에 게 미치는 영향이 낮습니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-p104">Tasks to accomplish in the first 30 days.  These have immediate affect and are low-impact to your users.</span></span>
- <span data-ttu-id="ed68a-p105">90 일 이내에 수행할 작업입니다. 이를 통해 계획 하 고 구현 하는 데 다소 시간이 걸리고 보안 환경을 크게 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-p105">Tasks to accomplish in 90 days. These take a bit more time to plan and implement but greatly improve your security posture</span></span>
- <span data-ttu-id="ed68a-p106">90 일을 초과 합니다. 처음 90 일의 향상 된 기능 빌드는 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed68a-p106">Beyond 90 days. These enhancements build in your first 90 days work.</span></span>






