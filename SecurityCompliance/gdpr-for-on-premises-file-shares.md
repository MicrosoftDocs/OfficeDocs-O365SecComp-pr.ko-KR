---
title: 온-프레미스 파일 공유 GDPR
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: 온-프레미스 Windows Server 파일 공유에서 GDPR 요구 사항을 해결하는 방법을 알아보세요.
ms.openlocfilehash: 14af73a2ff2a162f2f3e621c2efeb5d9050c069a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255226"
---
# <a name="gdpr-for-on-premises-windows-server-file-shares"></a><span data-ttu-id="1ee96-103">온-프레미스 Windows Server 파일 공유</span><span class="sxs-lookup"><span data-stu-id="1ee96-103">GDPR for on-premises Windows Server file shares</span></span>

<span data-ttu-id="1ee96-104">파일 공유에 권장되는 기본 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-104">The basic recommended approach for file shares is:</span></span>

-   <span data-ttu-id="1ee96-105">Azure Information Protection을 사용하여 중요한 데이터를 레이블 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-105">Use Azure Information Protection to label sensitive data.</span></span>

-   <span data-ttu-id="1ee96-106">Azure Information Protection 스캐너를 사용하여 데이터를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-106">Use Azure Information Protection scanner to find data.</span></span>

<span data-ttu-id="1ee96-107">파일 공유에 권장되는 방식에는 이러한 단계가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-107">The recommended approach for files shares includes these steps:</span></span>

1.  <span data-ttu-id="1ee96-108">**Azure Information Protection 스캐너를 설치하고 구성합니다.**</span><span class="sxs-lookup"><span data-stu-id="1ee96-108">**Install and configure Azure Information Protection scanner.**</span></span>

    -   <span data-ttu-id="1ee96-109">사용할 중요한 데이터 형식을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-109">Decide which sensitive data types to use.</span></span>

    -   <span data-ttu-id="1ee96-110">사용할 로컬 폴더 및 네트워크 공유를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-110">Specify local folders and network shares to use.</span></span>

2.  <span data-ttu-id="1ee96-111">**검색 주기를 완료합니다.**</span><span class="sxs-lookup"><span data-stu-id="1ee96-111">**Complete a discovery cycle.**</span></span>

    -   <span data-ttu-id="1ee96-112">검색 모드에서 스캐너를 실행하고 검색 결과의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-112">Run the scanner in discovery mode and validate the findings.</span></span>

    -   <span data-ttu-id="1ee96-113">필요에 따라 조건 및 중요한 정보 유형을 최적화합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-113">If needed, optimize the conditions and sensitive information types.</span></span>

    -   <span data-ttu-id="1ee96-114">레이블 자동 적용의 예상된 영향을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-114">Assess the expected impact of automatically applying labels.</span></span>

3.  <span data-ttu-id="1ee96-115">**Azure Information Protection 스캐너를 실행하여 적격 문서에 레이블을 적용합니다**.</span><span class="sxs-lookup"><span data-stu-id="1ee96-115">**Run the Azure Information Protection scanner to apply labels to qualifying documents**.</span></span>

4.  <span data-ttu-id="1ee96-116">**보호하려면:**</span><span class="sxs-lookup"><span data-stu-id="1ee96-116">**For protection:**</span></span>

    -   <span data-ttu-id="1ee96-117">Exchange 데이터 손실 방지 규칙을 구성하여 원하는 레이블로 문서를 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-117">Configure Exchange data loss prevention rules to protect documents with the desired label.</span></span>

    -   <span data-ttu-id="1ee96-118">권한을 사용하여 파일에 액세스할 수 있는 사람을 제한해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-118">Be sure to use permissions to limit who can access files.</span></span>

5.  <span data-ttu-id="1ee96-119">**모니터링하려면 Windows Server 로그를 SIEM 도구와 통합합니다.**</span><span class="sxs-lookup"><span data-stu-id="1ee96-119">**For monitoring, integrate Windows Server logs with a SIEM tool.**</span></span>

    -   <span data-ttu-id="1ee96-p101">데이터 주체 요청을 위한 개인 데이터를 찾으려면 Azure Information Protection 스캐너를 사용합니다. SharePoint Server 검색을 구성하여 파일 공유를 크롤링할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-p101">To find personal data for data subject requests, use Azure Information Protection scanner. You can also configure SharePoint Server search to crawl file shares.</span></span>

<span data-ttu-id="1ee96-122">Azure Information Protection 스캐너를 사용하여 개인 데이터를 찾고 레이블 지정하는 방법에 대한 자세한 내용은 [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>)에서 Microsoft GDPR 데이터 검색 도구 키트를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1ee96-122">For more information on using Azure Information Protection scanner to find and label personal data, see the Microsoft GDPR Data Discovery Toolkit at [http://aka.ms/gdprpartners](<http://aka.ms/gdprpartners>).</span></span>

<span data-ttu-id="1ee96-p102">조건을 위한 스캐너 구성 및 Office 365 DLP(데이터 손실 방지) 중요한 정보 유형의 사용에 대한 자세한 내용은 [Azure Information Protection의 자동 및 권장 분류를 위한 조건을 구성하는 방법](https://docs.microsoft.com/ko-KR/information-protection/deploy-use/configure-policy-classification)을 참조하세요. 새 Office 365 중요한 정보 유형은 스캐너에서 즉시 사용할 수 없으며 사용자 지정 중요한 정보 유형은 스캐너에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee96-p102">For information on configuring the scanner for conditions and using the Office 365 data loss prevention (DLP) sensitive information types, see [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/ko-KR/information-protection/deploy-use/configure-policy-classification). Note that new Office 365 sensitive information types will not be immediately available to use with the scanner and custom sensitive information types cannot be used with the scanner.</span></span>
