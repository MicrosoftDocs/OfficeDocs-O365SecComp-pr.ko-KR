---
title: Office 365 보안 사고 대응
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/27/2018
audience: ITPro
ms.topic: overview
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: 이 솔루션은 가장 일반적인 사이버 보안 공격이 Office 365에서 어떤 방식으로 표시 될 수 있는지와이에 대처 하는 방법을 알려줍니다.
ms.openlocfilehash: 900022d97c974bdf84d3077c1127e715c06fa5de
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157680"
---
# <a name="office-365-security-incident-response"></a><span data-ttu-id="84f03-103">Office 365 보안 사고 대응</span><span class="sxs-lookup"><span data-stu-id="84f03-103">Office 365 Security Incident Response</span></span>

 <span data-ttu-id="84f03-104">**요약:** 이 솔루션은 Office 365에서 가장 일반적인 사이버 보안 공격에 대 한 지표, 지정 된 공격을 확실 하 게 확인 하는 방법 및 응답 하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-104">**Summary:** This solution tells you what the indicators are for the most common cyber-security attacks in Office 365, how to positively confirm any given attack, and how to respond to it.</span></span>
  
## <a name="overview"></a><span data-ttu-id="84f03-105">개요</span><span class="sxs-lookup"><span data-stu-id="84f03-105">Overview</span></span>
<span data-ttu-id="84f03-106">모든 사이버 공격이 thwarted 수 있는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-106">Not all cyber attacks can be thwarted.</span></span> <span data-ttu-id="84f03-107">공격자가 방어 전략의 새로운 약점을 지속적으로 찾고 있거나 이전 버전을 이용 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-107">Attackers are constantly looking for new weaknesses in your defensive strategy or they are exploiting old ones.</span></span> <span data-ttu-id="84f03-108">공격을 인식 하는 방법을 알면 보다 신속 하 게 응답 하 여 보안 인시던트 기간을 단축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-108">Knowing how to recognize an attack allows you to respond to it faster, which shortens the duration of the security incident.</span></span>

<span data-ttu-id="84f03-109">이 문서 시리즈는 Office 365에서 특정 유형의 공격을 이해 하 고이를 처리할 수 있는 단계를 제공 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-109">This series of article helps you understand what a particular type of attack might look like in Office 365 and gives you steps you can take to respond.</span></span> <span data-ttu-id="84f03-110">다음은 이해를 위한 빠른 입력 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-110">They are quick entry points to understanding:</span></span>
 
- <span data-ttu-id="84f03-111">공격과 공격 방식 및 작동 방식</span><span class="sxs-lookup"><span data-stu-id="84f03-111">What the attack is and how it works.</span></span>
- <span data-ttu-id="84f03-112">찾을 대상 및 해당 항목을 찾는 방법에 대 한 손상 표시기 (IOC)입니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-112">What signs, called indicators of compromise (IOC), to look for and how to look for them.</span></span>
- <span data-ttu-id="84f03-113">공격을 적극적으로 확인 하는 방법</span><span class="sxs-lookup"><span data-stu-id="84f03-113">How to positively confirm the attack.</span></span>
- <span data-ttu-id="84f03-114">나중에 공격을 중단 하 고 조직을 보다 효율적으로 보호 하기 위해 수행 해야 하는 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-114">Steps to take to cut off the attack and better protect your organization in the future.</span></span>
- <span data-ttu-id="84f03-115">각 공격 유형에 대 한 자세한 정보로 연결 되는 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-115">Links to in-depth information on each attack type.</span></span>

<span data-ttu-id="84f03-116">시간이 지남에 따라 추가 되는 문서를 매달 다시 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="84f03-116">Check back here monthly as more articles will be added over time.</span></span>

## <a name="detect-and-remediate-articles"></a><span data-ttu-id="84f03-117">문서 검색 및 수정</span><span class="sxs-lookup"><span data-stu-id="84f03-117">Detect and remediate articles</span></span>

- [<span data-ttu-id="84f03-118">Office 365에서 불법 동의 권한 부여 검색 및 교정</span><span class="sxs-lookup"><span data-stu-id="84f03-118">Detect and Remediate Illicit Consent Grants in Office 365</span></span>](detect-and-remediate-illicit-consent-grants.md)
- [<span data-ttu-id="84f03-119">Office 365에서 Outlook 규칙 및 사용자 지정 양식 주입 공격 감지 및 재구성</span><span class="sxs-lookup"><span data-stu-id="84f03-119">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)
 
## <a name="incident-response-articles"></a><span data-ttu-id="84f03-120">인시던트 대응 문서</span><span class="sxs-lookup"><span data-stu-id="84f03-120">Incident response articles</span></span>

- [<span data-ttu-id="84f03-121">Office 365에서 손상된 이메일 계정에 응답</span><span class="sxs-lookup"><span data-stu-id="84f03-121">Responding to a Compromised Email Account in Office 365</span></span>](responding-to-a-compromised-email-account.md)

## <a name="secure-office-365-like-a-cybersecurity-pro"></a><span data-ttu-id="84f03-122">사이버 보안 전문가와 같은 Office 365 보안</span><span class="sxs-lookup"><span data-stu-id="84f03-122">Secure Office 365 like a cybersecurity pro</span></span>
<span data-ttu-id="84f03-123">Office 365 구독에는 데이터 및 사용자를 보호하는 데 사용할 수있는 강력한 보안 기능이 함께 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-123">Your Office 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.</span></span>  <span data-ttu-id="84f03-124">[Office 365 보안 로드맵: 최초 30일, 90일 및 그 이후의 최우선 순위](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352)를 사용하여 Microsoft에서 권장하는 Office 365 테넌트 보안을 구현합니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-124">Use the [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) to implement Microsoft recommended best practices for securing your Office 365 tenant.</span></span>
- <span data-ttu-id="84f03-125">처음 30일 이내에 수행 할 작업</span><span class="sxs-lookup"><span data-stu-id="84f03-125">Tasks to accomplish in the first 30 days.</span></span>  <span data-ttu-id="84f03-126">이러한 작업들은 즉각적인 영향을 미치며 사용자에게 영향을 미치지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-126">These have immediate affect and are low-impact to your users.</span></span>
- <span data-ttu-id="84f03-127">90일 이내에 수행해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="84f03-127">Tasks to accomplish in 90 days.</span></span> <span data-ttu-id="84f03-128">이를 통해 계획 하 고 구현 하는 데 다소 시간이 걸리고 보안 환경을 크게 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-128">These take a bit more time to plan and implement but greatly improve your security posture</span></span>
- <span data-ttu-id="84f03-129">90일 초과</span><span class="sxs-lookup"><span data-stu-id="84f03-129">Beyond 90 days.</span></span> <span data-ttu-id="84f03-130">이러한 향상된 기능은 처음 90일간의 작업에서 구축됩니다.</span><span class="sxs-lookup"><span data-stu-id="84f03-130">These enhancements build in your first 90 days work.</span></span>






