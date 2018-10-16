---
title: Office 365 인증서 체인
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 기술을 활용 하는 다른 인증서 공급자의 수입니다. 다음은 고객이 Office 365에 액세스할 때 발생할 수 있는 알려진된 Office 365 루트 인증서의 전체 목록에 대 한 설명입니다. 인증서에 대 한 정보 직접 인프라에 설치 Office 365 용 타사 SSL 인증서에 대 한 계획을 참조 하십시오 해야할 수 있습니다. 다음 인증서 정보는 Office 365의 모든 전세계 및 국가 클라우드 인스턴스에 적용 됩니다.
ms.openlocfilehash: 97e00833e57f8f6b7352650b0efdef51ddba77fa
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575362"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="5558b-106">Office 365 인증서 체인</span><span class="sxs-lookup"><span data-stu-id="5558b-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="5558b-p102">Office 365 기술을 활용 하는 다른 인증서 공급자의 수입니다. 다음은 고객이 Office 365에 액세스할 때 발생할 수 있는 알려진된 Office 365 루트 인증서의 전체 목록에 대 한 설명입니다. 직접 인프라에 설치 해야할 수 인증서는 정보를 [Office 365 용 타사 SSL 인증서에 대 한 계획을](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce)참조 합니다. 다음 인증서 정보는 Office 365의 모든 전세계 및 국가 클라우드 인스턴스에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5558b-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="5558b-111">**인증서 유형**</span><span class="sxs-lookup"><span data-stu-id="5558b-111">**Certificate type**</span></span>|<span data-ttu-id="5558b-112">**여.p7b 다운로드**</span><span class="sxs-lookup"><span data-stu-id="5558b-112">**P7b download**</span></span>|<span data-ttu-id="5558b-113">**CRL 끝점**</span><span class="sxs-lookup"><span data-stu-id="5558b-113">**CRL Endpoints**</span></span>|<span data-ttu-id="5558b-114">**OCSP 끝점**</span><span class="sxs-lookup"><span data-stu-id="5558b-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="5558b-115">**AIA 끝점**</span><span class="sxs-lookup"><span data-stu-id="5558b-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="5558b-116">공개적으로 신뢰할 수 있는 루트 인증서</span><span class="sxs-lookup"><span data-stu-id="5558b-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="5558b-117">Office 365 루트 인증서 번들 (여.p7b)</span><span class="sxs-lookup"><span data-stu-id="5558b-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="5558b-118">crl.globalsign.net</span><span class="sxs-lookup"><span data-stu-id="5558b-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="5558b-119">www.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="5558b-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="5558b-120">해당 없음</span><span class="sxs-lookup"><span data-stu-id="5558b-120">N/A</span></span>  <br/> |<span data-ttu-id="5558b-121">해당 없음</span><span class="sxs-lookup"><span data-stu-id="5558b-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="5558b-122">공개적으로 신뢰할 수 있는 중간 인증서</span><span class="sxs-lookup"><span data-stu-id="5558b-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="5558b-123">Office 365 중간 인증서 번들 (여.p7b)</span><span class="sxs-lookup"><span data-stu-id="5558b-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="5558b-124">cdp1.public trust.com</span><span class="sxs-lookup"><span data-stu-id="5558b-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="5558b-125">crl.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="5558b-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="5558b-126">crl.entrust.net</span><span class="sxs-lookup"><span data-stu-id="5558b-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="5558b-127">crl.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="5558b-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="5558b-128">crl.globalsign.net</span><span class="sxs-lookup"><span data-stu-id="5558b-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="5558b-129">crl.identrust.com</span><span class="sxs-lookup"><span data-stu-id="5558b-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="5558b-130">crl.thawte.com</span><span class="sxs-lookup"><span data-stu-id="5558b-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="5558b-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="5558b-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="5558b-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="5558b-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="5558b-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="5558b-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="5558b-134">www.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="5558b-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="5558b-135">isrg.trustid.ocsp.identrust.com</span><span class="sxs-lookup"><span data-stu-id="5558b-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="5558b-136">ocsp.digicert.com</span><span class="sxs-lookup"><span data-stu-id="5558b-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="5558b-137">ocsp.entrust.net</span><span class="sxs-lookup"><span data-stu-id="5558b-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="5558b-138">ocsp.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="5558b-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="5558b-139">ocsp.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="5558b-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="5558b-140">ocsp.startssl.com</span><span class="sxs-lookup"><span data-stu-id="5558b-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="5558b-141">ocsp.thawte.com</span><span class="sxs-lookup"><span data-stu-id="5558b-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="5558b-142">ocsp2.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="5558b-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="5558b-143">ocspcnnicroot.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="5558b-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="5558b-144">루트-c3-c a 2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="5558b-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="5558b-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="5558b-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="5558b-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="5558b-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="5558b-147">aia.startssl.com</span><span class="sxs-lookup"><span data-stu-id="5558b-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="5558b-148">apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="5558b-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="5558b-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="5558b-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="5558b-150">www.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="5558b-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="5558b-151">루트 및 인증서 공급자에 대 한 추가 세부 정보를 보려면 아래 중간 섹션을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5558b-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="5558b-152">Office 365 루트 인증서 세부 정보</span><span class="sxs-lookup"><span data-stu-id="5558b-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="5558b-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="5558b-153"></span></span>

 <span data-ttu-id="5558b-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="5558b-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="5558b-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="5558b-155">|:-----|</span></span>
|<span data-ttu-id="5558b-156">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="5558b-157">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-157">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-158">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-158"></span></span>|
|<span data-ttu-id="5558b-159">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-159">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-160">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-160"></span></span>|
|<span data-ttu-id="5558b-161">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-162">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-162"></span></span>|
|<span data-ttu-id="5558b-163">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-164">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-164"></span></span>|
|<span data-ttu-id="5558b-165">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-165">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-166">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-166"></span></span>|
|<span data-ttu-id="5558b-167">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-168">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-168"></span></span>|
|<span data-ttu-id="5558b-169">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-170">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-170"></span></span>|
|<span data-ttu-id="5558b-171">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-172">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-172"></span></span>|
|<span data-ttu-id="5558b-173">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-174">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-174"></span></span>|
   
 <span data-ttu-id="5558b-175">**CNNIC 루트**</span><span class="sxs-lookup"><span data-stu-id="5558b-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-176">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-176">**Subject**</span></span>|
|<span data-ttu-id="5558b-177">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-177"></span></span>|
|<span data-ttu-id="5558b-178">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-178">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-179">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-179"></span></span>|
|<span data-ttu-id="5558b-180">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-180">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-181">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-181"></span></span>|
|<span data-ttu-id="5558b-182">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-183">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-183"></span></span>|
|<span data-ttu-id="5558b-184">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-185">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-185"></span></span>|
|<span data-ttu-id="5558b-186">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-186">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-187">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-187"></span></span>|
|<span data-ttu-id="5558b-188">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-189">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-189"></span></span>|
|<span data-ttu-id="5558b-190">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-191">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-191"></span></span>|
|<span data-ttu-id="5558b-192">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-193">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-193"></span></span>|
|<span data-ttu-id="5558b-194">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-195">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-195"></span></span>|
|<span data-ttu-id="5558b-196">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-197">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-197"></span></span>|
   
 <span data-ttu-id="5558b-198">**DigiCert 전역 루트 CA**</span><span class="sxs-lookup"><span data-stu-id="5558b-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-199">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-199">**Subject**</span></span>|
|<span data-ttu-id="5558b-200">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-200"></span></span>|
|<span data-ttu-id="5558b-201">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-201">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-202">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-202"></span></span>|
|<span data-ttu-id="5558b-203">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-203">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-204">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-204"></span></span>|
|<span data-ttu-id="5558b-205">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-206">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-206"></span></span>|
|<span data-ttu-id="5558b-207">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-208">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-208"></span></span>|
|<span data-ttu-id="5558b-209">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-209">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-210">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-210"></span></span>|
|<span data-ttu-id="5558b-211">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-212">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-212"></span></span>|
|<span data-ttu-id="5558b-213">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-214">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-214"></span></span>|
|<span data-ttu-id="5558b-215">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-216">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-216"></span></span>|
|<span data-ttu-id="5558b-217">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-218">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-218"></span></span>|
|<span data-ttu-id="5558b-219">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-220">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-220"></span></span>|
   
 <span data-ttu-id="5558b-221">**DigiCert 높은 보증 EV 루트 CA**</span><span class="sxs-lookup"><span data-stu-id="5558b-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-222">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-222">**Subject**</span></span>|
|<span data-ttu-id="5558b-223">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-223"></span></span>|
|<span data-ttu-id="5558b-224">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-224">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-225">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-225"></span></span>|
|<span data-ttu-id="5558b-226">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-226">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-227">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-227"></span></span>|
|<span data-ttu-id="5558b-228">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-229">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-229"></span></span>|
|<span data-ttu-id="5558b-230">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-231">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-231"></span></span>|
|<span data-ttu-id="5558b-232">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-232">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-233">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-233"></span></span>|
|<span data-ttu-id="5558b-234">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-235">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-235"></span></span>|
|<span data-ttu-id="5558b-236">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-237">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-237"></span></span>|
|<span data-ttu-id="5558b-238">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-239">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-239"></span></span>|
|<span data-ttu-id="5558b-240">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-241">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-241"></span></span>|
|<span data-ttu-id="5558b-242">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-243">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-243"></span></span>|
   
 <span data-ttu-id="5558b-244">**D-신뢰 루트 클래스 3 CA 2 2009**</span><span class="sxs-lookup"><span data-stu-id="5558b-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-245">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-245">**Subject**</span></span>|
|<span data-ttu-id="5558b-246">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-246"></span></span>|
|<span data-ttu-id="5558b-247">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-247">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-248">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-248"></span></span>|
|<span data-ttu-id="5558b-249">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-249">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-250">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-250"></span></span>|
|<span data-ttu-id="5558b-251">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-252">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-252"></span></span>|
|<span data-ttu-id="5558b-253">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-254">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-254"></span></span>|
|<span data-ttu-id="5558b-255">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-255">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-256">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-256"></span></span>|
|<span data-ttu-id="5558b-257">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-258">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-258"></span></span>|
|<span data-ttu-id="5558b-259">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-260">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-260"></span></span>|
|<span data-ttu-id="5558b-261">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-262">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-262"></span></span>|
|<span data-ttu-id="5558b-263">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-264">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-264"></span></span>|
|<span data-ttu-id="5558b-265">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-265">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-266">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-266"></span></span>|
   
 <span data-ttu-id="5558b-267">**D-신뢰 루트 클래스 3 CA 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="5558b-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-268">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-268">**Subject**</span></span>|
|<span data-ttu-id="5558b-269">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-269"></span></span>|
|<span data-ttu-id="5558b-270">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-270">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-271">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-271"></span></span>|
|<span data-ttu-id="5558b-272">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-272">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-273">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-273"></span></span>|
|<span data-ttu-id="5558b-274">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-275">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-275"></span></span>|
|<span data-ttu-id="5558b-276">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-277">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-277"></span></span>|
|<span data-ttu-id="5558b-278">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-278">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-279">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-279"></span></span>|
|<span data-ttu-id="5558b-280">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-281">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-281"></span></span>|
|<span data-ttu-id="5558b-282">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-283">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-283"></span></span>|
|<span data-ttu-id="5558b-284">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-285">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-285"></span></span>|
|<span data-ttu-id="5558b-286">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-287">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-287"></span></span>|
|<span data-ttu-id="5558b-288">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-288">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-289">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-289"></span></span>|
   
 <span data-ttu-id="5558b-290">**DST 루트 CA X3**</span><span class="sxs-lookup"><span data-stu-id="5558b-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-291">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-291">**Subject**</span></span>|
|<span data-ttu-id="5558b-292">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-292"></span></span>|
|<span data-ttu-id="5558b-293">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-293">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-294">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-294"></span></span>|
|<span data-ttu-id="5558b-295">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-295">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-296">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-296"></span></span>|
|<span data-ttu-id="5558b-297">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-298">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-298"></span></span>|
|<span data-ttu-id="5558b-299">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-300">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-300"></span></span>|
|<span data-ttu-id="5558b-301">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-301">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-302">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-302"></span></span>|
|<span data-ttu-id="5558b-303">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-304">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-304"></span></span>|
|<span data-ttu-id="5558b-305">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-306">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-306"></span></span>|
|<span data-ttu-id="5558b-307">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-308">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-308"></span></span>|
|<span data-ttu-id="5558b-309">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-310">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-310"></span></span>|
   
 <span data-ttu-id="5558b-311">**루트 인증 기관-G2 맡길**</span><span class="sxs-lookup"><span data-stu-id="5558b-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-312">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-312">**Subject**</span></span>|
|<span data-ttu-id="5558b-313">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-313"></span></span>|
|<span data-ttu-id="5558b-314">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-314">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-315">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-315"></span></span>|
|<span data-ttu-id="5558b-316">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-316">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-317">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-317"></span></span>|
|<span data-ttu-id="5558b-318">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-319">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-319"></span></span>|
|<span data-ttu-id="5558b-320">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-321">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-321"></span></span>|
|<span data-ttu-id="5558b-322">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-322">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-323">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-323"></span></span>|
|<span data-ttu-id="5558b-324">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-325">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-325"></span></span>|
|<span data-ttu-id="5558b-326">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-327">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-327"></span></span>|
|<span data-ttu-id="5558b-328">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-329">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-329"></span></span>|
|<span data-ttu-id="5558b-330">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-331">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-331"></span></span>|
   
 <span data-ttu-id="5558b-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="5558b-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-333">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-333">**Subject**</span></span>|
|<span data-ttu-id="5558b-334">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-334"></span></span>|
|<span data-ttu-id="5558b-335">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-335">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-336">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-336"></span></span>|
|<span data-ttu-id="5558b-337">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-337">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-338">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-338"></span></span>|
|<span data-ttu-id="5558b-339">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-340">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-340"></span></span>|
|<span data-ttu-id="5558b-341">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-342">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-342"></span></span>|
|<span data-ttu-id="5558b-343">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-343">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-344">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-344"></span></span>|
|<span data-ttu-id="5558b-345">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-346">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-346"></span></span>|
|<span data-ttu-id="5558b-347">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-348">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-348"></span></span>|
|<span data-ttu-id="5558b-349">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-350">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-350"></span></span>|
|<span data-ttu-id="5558b-351">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-352">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-352"></span></span>|
   
 <span data-ttu-id="5558b-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="5558b-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-354">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-354">**Subject**</span></span>|
|<span data-ttu-id="5558b-355">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-355"></span></span>|
|<span data-ttu-id="5558b-356">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-356">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-357">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-357"></span></span>|
|<span data-ttu-id="5558b-358">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-358">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-359">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-359"></span></span>|
|<span data-ttu-id="5558b-360">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-361">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-361"></span></span>|
|<span data-ttu-id="5558b-362">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-363">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-363"></span></span>|
|<span data-ttu-id="5558b-364">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-364">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-365">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-365"></span></span>|
|<span data-ttu-id="5558b-366">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-367">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-367"></span></span>|
|<span data-ttu-id="5558b-368">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-369">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-369"></span></span>|
|<span data-ttu-id="5558b-370">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-371">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-371"></span></span>|
|<span data-ttu-id="5558b-372">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-373">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-373"></span></span>|
|<span data-ttu-id="5558b-374">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-375">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-375"></span></span>|
|<span data-ttu-id="5558b-376">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-376">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-377">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-377"></span></span>|
   
 <span data-ttu-id="5558b-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="5558b-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-379">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-379">**Subject**</span></span>|
|<span data-ttu-id="5558b-380">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-380"></span></span>|
|<span data-ttu-id="5558b-381">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-381">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-382">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-382"></span></span>|
|<span data-ttu-id="5558b-383">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-383">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-384">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-384"></span></span>|
|<span data-ttu-id="5558b-385">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-386">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-386"></span></span>|
|<span data-ttu-id="5558b-387">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-388">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-388"></span></span>|
|<span data-ttu-id="5558b-389">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-389">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-390">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-390"></span></span>|
|<span data-ttu-id="5558b-391">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-392">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-392"></span></span>|
|<span data-ttu-id="5558b-393">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-394">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-394"></span></span>|
|<span data-ttu-id="5558b-395">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-396">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-396"></span></span>|
|<span data-ttu-id="5558b-397">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-398">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-398"></span></span>|
   
 <span data-ttu-id="5558b-399">**thawte 기본 루트 CA-G3**</span><span class="sxs-lookup"><span data-stu-id="5558b-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-400">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-400">**Subject**</span></span>|
|<span data-ttu-id="5558b-401">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-401"></span></span>|
|<span data-ttu-id="5558b-402">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-402">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-403">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-403"></span></span>|
|<span data-ttu-id="5558b-404">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-404">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-405">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-405"></span></span>|
|<span data-ttu-id="5558b-406">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-407">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-407"></span></span>|
|<span data-ttu-id="5558b-408">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-409">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-409"></span></span>|
|<span data-ttu-id="5558b-410">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-410">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-411">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-411"></span></span>|
|<span data-ttu-id="5558b-412">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-413">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-413"></span></span>|
|<span data-ttu-id="5558b-414">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-415">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-415"></span></span>|
|<span data-ttu-id="5558b-416">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-417">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-417"></span></span>|
|<span data-ttu-id="5558b-418">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-419">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-419"></span></span>|
   
 <span data-ttu-id="5558b-420">**VeriSign 클래스 3 기본 공용 인증 기관-g 5**</span><span class="sxs-lookup"><span data-stu-id="5558b-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-421">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-421">**Subject**</span></span>|
|<span data-ttu-id="5558b-422">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-422"></span></span>|
|<span data-ttu-id="5558b-423">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-423">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-424">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-424"></span></span>|
|<span data-ttu-id="5558b-425">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-425">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-426">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-426"></span></span>|
|<span data-ttu-id="5558b-427">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-428">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-428"></span></span>|
|<span data-ttu-id="5558b-429">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-430">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-430"></span></span>|
|<span data-ttu-id="5558b-431">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-431">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-432">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-432"></span></span>|
|<span data-ttu-id="5558b-433">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-434">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-434"></span></span>|
|<span data-ttu-id="5558b-435">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-436">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-436"></span></span>|
|<span data-ttu-id="5558b-437">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-438">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-438"></span></span>|
|<span data-ttu-id="5558b-439">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-440">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="5558b-441">Office 365 중간 인증서 세부 정보</span><span class="sxs-lookup"><span data-stu-id="5558b-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="5558b-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="5558b-442"></span></span>

 <span data-ttu-id="5558b-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="5558b-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-444">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-444">**Subject**</span></span>|
|<span data-ttu-id="5558b-445">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-445"></span></span>|
|<span data-ttu-id="5558b-446">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-446">**Issuer**</span></span>|
|<span data-ttu-id="5558b-447">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-447"></span></span>|
|<span data-ttu-id="5558b-448">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-448">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-449">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-449"></span></span>|
|<span data-ttu-id="5558b-450">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-450">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-451">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-451"></span></span>|
|<span data-ttu-id="5558b-452">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-453">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-453"></span></span>|
|<span data-ttu-id="5558b-454">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-455">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-455"></span></span>|
|<span data-ttu-id="5558b-456">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-456">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-457">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-457"></span></span>|
|<span data-ttu-id="5558b-458">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-459">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-459"></span></span>|
|<span data-ttu-id="5558b-460">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-461">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-461"></span></span>|
|<span data-ttu-id="5558b-462">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-463">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-463"></span></span>|
|<span data-ttu-id="5558b-464">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-465">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-465"></span></span>|
|<span data-ttu-id="5558b-466">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-467">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-467"></span></span>|
|<span data-ttu-id="5558b-468">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-468">**AIA URLs**</span></span>|
|<span data-ttu-id="5558b-469">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-469"></span></span>|
|<span data-ttu-id="5558b-470">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-470">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-471">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-471"></span></span>|
|<span data-ttu-id="5558b-472">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-473">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-473"></span></span>|
   
 <span data-ttu-id="5558b-474">**D-신뢰 SSL 클래스 3 CA 1 2009**</span><span class="sxs-lookup"><span data-stu-id="5558b-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-475">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-475">**Subject**</span></span>|
|<span data-ttu-id="5558b-476">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-476"></span></span>|
|<span data-ttu-id="5558b-477">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-477">**Issuer**</span></span>|
|<span data-ttu-id="5558b-478">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-478"></span></span>|
|<span data-ttu-id="5558b-479">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="5558b-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="5558b-480">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-480"></span></span>|
|<span data-ttu-id="5558b-481">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-481">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-482">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-482"></span></span>|
|<span data-ttu-id="5558b-483">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-483">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-484">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-484"></span></span>|
|<span data-ttu-id="5558b-485">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-486">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-486"></span></span>|
|<span data-ttu-id="5558b-487">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-488">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-488"></span></span>|
|<span data-ttu-id="5558b-489">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-489">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-490">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-490"></span></span>|
|<span data-ttu-id="5558b-491">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-492">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-492"></span></span>|
|<span data-ttu-id="5558b-493">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-494">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-494"></span></span>|
|<span data-ttu-id="5558b-495">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-496">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-496"></span></span>|
|<span data-ttu-id="5558b-497">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-498">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-498"></span></span>|
|<span data-ttu-id="5558b-499">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-500">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-500"></span></span>|
|<span data-ttu-id="5558b-501">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-501">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-502">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-502"></span></span>|
|<span data-ttu-id="5558b-503">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-504">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-504"></span></span>|
   
 <span data-ttu-id="5558b-505">**D-신뢰 SSL 클래스 3 CA 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="5558b-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-506">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-506">**Subject**</span></span>|
|<span data-ttu-id="5558b-507">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-507"></span></span>|
|<span data-ttu-id="5558b-508">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-508">**Issuer**</span></span>|
|<span data-ttu-id="5558b-509">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-509"></span></span>|
|<span data-ttu-id="5558b-510">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="5558b-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="5558b-511">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-511"></span></span>|
|<span data-ttu-id="5558b-512">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-512">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-513">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-513"></span></span>|
|<span data-ttu-id="5558b-514">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-514">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-515">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-515"></span></span>|
|<span data-ttu-id="5558b-516">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-517">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-517"></span></span>|
|<span data-ttu-id="5558b-518">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-519">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-519"></span></span>|
|<span data-ttu-id="5558b-520">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-520">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-521">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-521"></span></span>|
|<span data-ttu-id="5558b-522">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-523">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-523"></span></span>|
|<span data-ttu-id="5558b-524">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-525">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-525"></span></span>|
|<span data-ttu-id="5558b-526">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-527">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-527"></span></span>|
|<span data-ttu-id="5558b-528">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-529">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-529"></span></span>|
|<span data-ttu-id="5558b-530">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-531">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-531"></span></span>|
|<span data-ttu-id="5558b-532">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-532">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-533">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-533"></span></span>|
|<span data-ttu-id="5558b-534">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-535">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-535"></span></span>|
   
 <span data-ttu-id="5558b-536">**DigiCert 클라우드 서비스 CA-1**</span><span class="sxs-lookup"><span data-stu-id="5558b-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-537">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-537">**Subject**</span></span>|
|<span data-ttu-id="5558b-538">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-538"></span></span>|
|<span data-ttu-id="5558b-539">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-539">**Issuer**</span></span>|
|<span data-ttu-id="5558b-540">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-540"></span></span>|
|<span data-ttu-id="5558b-541">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-541">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-542">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-542"></span></span>|
|<span data-ttu-id="5558b-543">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-543">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-544">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-544"></span></span>|
|<span data-ttu-id="5558b-545">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-546">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-546"></span></span>|
|<span data-ttu-id="5558b-547">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-548">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-548"></span></span>|
|<span data-ttu-id="5558b-549">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-549">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-550">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-550"></span></span>|
|<span data-ttu-id="5558b-551">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-552">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-552"></span></span>|
|<span data-ttu-id="5558b-553">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-554">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-554"></span></span>|
|<span data-ttu-id="5558b-555">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-556">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-556"></span></span>|
|<span data-ttu-id="5558b-557">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-558">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-558"></span></span>|
|<span data-ttu-id="5558b-559">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-560">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-560"></span></span>|
|<span data-ttu-id="5558b-561">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-561">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-562">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-562"></span></span>|
|<span data-ttu-id="5558b-563">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-564">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-564"></span></span>|
   
 <span data-ttu-id="5558b-565">**DigiCert SHA2 높은 보증 서버 CA**</span><span class="sxs-lookup"><span data-stu-id="5558b-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-566">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-566">**Subject**</span></span>|
|<span data-ttu-id="5558b-567">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-567"></span></span>|
|<span data-ttu-id="5558b-568">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-568">**Issuer**</span></span>|
|<span data-ttu-id="5558b-569">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-569"></span></span>|
|<span data-ttu-id="5558b-570">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-570">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-571">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-571"></span></span>|
|<span data-ttu-id="5558b-572">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-572">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-573">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-573"></span></span>|
|<span data-ttu-id="5558b-574">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-575">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-575"></span></span>|
|<span data-ttu-id="5558b-576">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-577">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-577"></span></span>|
|<span data-ttu-id="5558b-578">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-578">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-579">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-579"></span></span>|
|<span data-ttu-id="5558b-580">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-581">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-581"></span></span>|
|<span data-ttu-id="5558b-582">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-583">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-583"></span></span>|
|<span data-ttu-id="5558b-584">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-585">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-585"></span></span>|
|<span data-ttu-id="5558b-586">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-587">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-587"></span></span>|
|<span data-ttu-id="5558b-588">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-589">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-589"></span></span>|
|<span data-ttu-id="5558b-590">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-590">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-591">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-591"></span></span>|
|<span data-ttu-id="5558b-592">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-593">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-593"></span></span>|
   
 <span data-ttu-id="5558b-594">**DigiCert SHA2 안전한 서버 CA**</span><span class="sxs-lookup"><span data-stu-id="5558b-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-595">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-595">**Subject**</span></span>|
|<span data-ttu-id="5558b-596">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-596"></span></span>|
|<span data-ttu-id="5558b-597">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-597">**Issuer**</span></span>|
|<span data-ttu-id="5558b-598">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-598"></span></span>|
|<span data-ttu-id="5558b-599">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-599">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-600">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-600"></span></span>|
|<span data-ttu-id="5558b-601">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-601">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-602">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-602"></span></span>|
|<span data-ttu-id="5558b-603">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-604">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-604"></span></span>|
|<span data-ttu-id="5558b-605">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-606">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-606"></span></span>|
|<span data-ttu-id="5558b-607">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-607">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-608">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-608"></span></span>|
|<span data-ttu-id="5558b-609">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-610">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-610"></span></span>|
|<span data-ttu-id="5558b-611">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-612">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-612"></span></span>|
|<span data-ttu-id="5558b-613">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-614">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-614"></span></span>|
|<span data-ttu-id="5558b-615">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-616">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-616"></span></span>|
|<span data-ttu-id="5558b-617">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-618">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-618"></span></span>|
|<span data-ttu-id="5558b-619">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-619">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-620">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-620"></span></span>|
|<span data-ttu-id="5558b-621">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-622">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-622"></span></span>|
   
 <span data-ttu-id="5558b-623">**인증 기관-L1C 맡길**</span><span class="sxs-lookup"><span data-stu-id="5558b-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-624">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-624">**Subject**</span></span>|
|<span data-ttu-id="5558b-625">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-625"></span></span>|
|<span data-ttu-id="5558b-626">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-626">**Issuer**</span></span>|
|<span data-ttu-id="5558b-627">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-627"></span></span>|
|<span data-ttu-id="5558b-628">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-628">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-629">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-629"></span></span>|
|<span data-ttu-id="5558b-630">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-630">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-631">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-631"></span></span>|
|<span data-ttu-id="5558b-632">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-633">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-633"></span></span>|
|<span data-ttu-id="5558b-634">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-635">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-635"></span></span>|
|<span data-ttu-id="5558b-636">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-636">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-637">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-637"></span></span>|
|<span data-ttu-id="5558b-638">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-639">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-639"></span></span>|
|<span data-ttu-id="5558b-640">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-641">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-641"></span></span>|
|<span data-ttu-id="5558b-642">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-643">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-643"></span></span>|
|<span data-ttu-id="5558b-644">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-645">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-645"></span></span>|
|<span data-ttu-id="5558b-646">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-647">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-647"></span></span>|
|<span data-ttu-id="5558b-648">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-648">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-649">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-649"></span></span>|
|<span data-ttu-id="5558b-650">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-651">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-651"></span></span>|
   
 <span data-ttu-id="5558b-652">**인증 기관-L1K 맡길**</span><span class="sxs-lookup"><span data-stu-id="5558b-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-653">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-653">**Subject**</span></span>|
|<span data-ttu-id="5558b-654">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-654"></span></span>|
|<span data-ttu-id="5558b-655">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-655">**Issuer**</span></span>|
|<span data-ttu-id="5558b-656">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-656"></span></span>|
|<span data-ttu-id="5558b-657">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-657">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-658">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-658"></span></span>|
|<span data-ttu-id="5558b-659">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-659">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-660">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-660"></span></span>|
|<span data-ttu-id="5558b-661">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-662">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-662"></span></span>|
|<span data-ttu-id="5558b-663">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-664">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-664"></span></span>|
|<span data-ttu-id="5558b-665">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-665">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-666">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-666"></span></span>|
|<span data-ttu-id="5558b-667">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-668">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-668"></span></span>|
|<span data-ttu-id="5558b-669">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-670">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-670"></span></span>|
|<span data-ttu-id="5558b-671">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-672">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-672"></span></span>|
|<span data-ttu-id="5558b-673">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-674">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-674"></span></span>|
|<span data-ttu-id="5558b-675">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-676">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-676"></span></span>|
|<span data-ttu-id="5558b-677">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-677">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-678">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-678"></span></span>|
|<span data-ttu-id="5558b-679">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-680">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-680"></span></span>|
   
 <span data-ttu-id="5558b-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="5558b-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-682">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-682">**Subject**</span></span>|
|<span data-ttu-id="5558b-683">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-683"></span></span>|
|<span data-ttu-id="5558b-684">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-684">**Issuer**</span></span>|
|<span data-ttu-id="5558b-685">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-685"></span></span>|
|<span data-ttu-id="5558b-686">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-686">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-687">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-687"></span></span>|
|<span data-ttu-id="5558b-688">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-688">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-689">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-689"></span></span>|
|<span data-ttu-id="5558b-690">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-691">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-691"></span></span>|
|<span data-ttu-id="5558b-692">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-693">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-693"></span></span>|
|<span data-ttu-id="5558b-694">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-694">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-695">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-695"></span></span>|
|<span data-ttu-id="5558b-696">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-697">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-697"></span></span>|
|<span data-ttu-id="5558b-698">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-699">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-699"></span></span>|
|<span data-ttu-id="5558b-700">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-701">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-701"></span></span>|
|<span data-ttu-id="5558b-702">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-703">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-703"></span></span>|
|<span data-ttu-id="5558b-704">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-705">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-705"></span></span>|
|<span data-ttu-id="5558b-706">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-706">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-707">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-707"></span></span>|
|<span data-ttu-id="5558b-708">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-709">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-709"></span></span>|
   
 <span data-ttu-id="5558b-710">**GlobalSign 유효성 검사 CA-SHA256-g 2를 확장 합니다.**</span><span class="sxs-lookup"><span data-stu-id="5558b-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-711">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-711">**Subject**</span></span>|
|<span data-ttu-id="5558b-712">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-712"></span></span>|
|<span data-ttu-id="5558b-713">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-713">**Issuer**</span></span>|
|<span data-ttu-id="5558b-714">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-714"></span></span>|
|<span data-ttu-id="5558b-715">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-715">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-716">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-716"></span></span>|
|<span data-ttu-id="5558b-717">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-717">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-718">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-718"></span></span>|
|<span data-ttu-id="5558b-719">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-720">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-720"></span></span>|
|<span data-ttu-id="5558b-721">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-722">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-722"></span></span>|
|<span data-ttu-id="5558b-723">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-723">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-724">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-724"></span></span>|
|<span data-ttu-id="5558b-725">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-726">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-726"></span></span>|
|<span data-ttu-id="5558b-727">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-728">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-728"></span></span>|
|<span data-ttu-id="5558b-729">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-730">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-730"></span></span>|
|<span data-ttu-id="5558b-731">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-732">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-732"></span></span>|
|<span data-ttu-id="5558b-733">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-734">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-734"></span></span>|
|<span data-ttu-id="5558b-735">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-735">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-736">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-736"></span></span>|
|<span data-ttu-id="5558b-737">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-738">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-738"></span></span>|
   
 <span data-ttu-id="5558b-739">**GlobalSign 유효성 검사-SHA256-CA G3 확장**</span><span class="sxs-lookup"><span data-stu-id="5558b-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-740">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-740">**Subject**</span></span>|
|<span data-ttu-id="5558b-741">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-741"></span></span>|
|<span data-ttu-id="5558b-742">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-742">**Issuer**</span></span>|
|<span data-ttu-id="5558b-743">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-743"></span></span>|
|<span data-ttu-id="5558b-744">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-744">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-745">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-745"></span></span>|
|<span data-ttu-id="5558b-746">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-746">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-747">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-747"></span></span>|
|<span data-ttu-id="5558b-748">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-749">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-749"></span></span>|
|<span data-ttu-id="5558b-750">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-751">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-751"></span></span>|
|<span data-ttu-id="5558b-752">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-752">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-753">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-753"></span></span>|
|<span data-ttu-id="5558b-754">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-755">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-755"></span></span>|
|<span data-ttu-id="5558b-756">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-757">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-757"></span></span>|
|<span data-ttu-id="5558b-758">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-759">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-759"></span></span>|
|<span data-ttu-id="5558b-760">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-761">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-761"></span></span>|
|<span data-ttu-id="5558b-762">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-763">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-763"></span></span>|
|<span data-ttu-id="5558b-764">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-764">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-765">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-765"></span></span>|
|<span data-ttu-id="5558b-766">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-767">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-767"></span></span>|
   
 <span data-ttu-id="5558b-768">**GlobalSign 조직 유효성 검사 CA-SHA256-g 2**</span><span class="sxs-lookup"><span data-stu-id="5558b-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-769">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-769">**Subject**</span></span>|
|<span data-ttu-id="5558b-770">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-770"></span></span>|
|<span data-ttu-id="5558b-771">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-771">**Issuer**</span></span>|
|<span data-ttu-id="5558b-772">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-772"></span></span>|
|<span data-ttu-id="5558b-773">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-773">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-774">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-774"></span></span>|
|<span data-ttu-id="5558b-775">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-775">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-776">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-776"></span></span>|
|<span data-ttu-id="5558b-777">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-778">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-778"></span></span>|
|<span data-ttu-id="5558b-779">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-780">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-780"></span></span>|
|<span data-ttu-id="5558b-781">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-781">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-782">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-782"></span></span>|
|<span data-ttu-id="5558b-783">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-784">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-784"></span></span>|
|<span data-ttu-id="5558b-785">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-786">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-786"></span></span>|
|<span data-ttu-id="5558b-787">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-788">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-788"></span></span>|
|<span data-ttu-id="5558b-789">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-790">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-790"></span></span>|
|<span data-ttu-id="5558b-791">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-792">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-792"></span></span>|
|<span data-ttu-id="5558b-793">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-793">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-794">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-794"></span></span>|
|<span data-ttu-id="5558b-795">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-796">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-796"></span></span>|
   
 <span data-ttu-id="5558b-797">**GlobalSign 조직 유효성 검사 CA-SHA256-g 2**</span><span class="sxs-lookup"><span data-stu-id="5558b-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-798">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-798">**Subject**</span></span>|
|<span data-ttu-id="5558b-799">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-799"></span></span>|
|<span data-ttu-id="5558b-800">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-800">**Issuer**</span></span>|
|<span data-ttu-id="5558b-801">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-801"></span></span>|
|<span data-ttu-id="5558b-802">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-802">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-803">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-803"></span></span>|
|<span data-ttu-id="5558b-804">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-804">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-805">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-805"></span></span>|
|<span data-ttu-id="5558b-806">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-807">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-807"></span></span>|
|<span data-ttu-id="5558b-808">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-809">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-809"></span></span>|
|<span data-ttu-id="5558b-810">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-810">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-811">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-811"></span></span>|
|<span data-ttu-id="5558b-812">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-813">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-813"></span></span>|
|<span data-ttu-id="5558b-814">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-815">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-815"></span></span>|
|<span data-ttu-id="5558b-816">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-817">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-817"></span></span>|
|<span data-ttu-id="5558b-818">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-819">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-819"></span></span>|
|<span data-ttu-id="5558b-820">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-821">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-821"></span></span>|
|<span data-ttu-id="5558b-822">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-822">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-823">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-823"></span></span>|
|<span data-ttu-id="5558b-824">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-825">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-825"></span></span>|
   
 <span data-ttu-id="5558b-826">**이제 기관 X3 암호화**</span><span class="sxs-lookup"><span data-stu-id="5558b-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-827">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-827">**Subject**</span></span>|
|<span data-ttu-id="5558b-828">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-828"></span></span>|
|<span data-ttu-id="5558b-829">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-829">**Issuer**</span></span>|
|<span data-ttu-id="5558b-830">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-830"></span></span>|
|<span data-ttu-id="5558b-831">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-831">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-832">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-832"></span></span>|
|<span data-ttu-id="5558b-833">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-833">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-834">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-834"></span></span>|
|<span data-ttu-id="5558b-835">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-836">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-836"></span></span>|
|<span data-ttu-id="5558b-837">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-838">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-838"></span></span>|
|<span data-ttu-id="5558b-839">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-839">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-840">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-840"></span></span>|
|<span data-ttu-id="5558b-841">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-842">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-842"></span></span>|
|<span data-ttu-id="5558b-843">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-844">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-844"></span></span>|
|<span data-ttu-id="5558b-845">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-846">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-846"></span></span>|
|<span data-ttu-id="5558b-847">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-848">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-848"></span></span>|
|<span data-ttu-id="5558b-849">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-850">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-850"></span></span>|
|<span data-ttu-id="5558b-851">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-851">**AIA URLs**</span></span>|
|<span data-ttu-id="5558b-852">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-852"></span></span>|
|<span data-ttu-id="5558b-853">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-853">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-854">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-854"></span></span>|
|<span data-ttu-id="5558b-855">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-856">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-856"></span></span>|
   
 <span data-ttu-id="5558b-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="5558b-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-858">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-858">**Subject**</span></span>|
|<span data-ttu-id="5558b-859">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-859"></span></span>|
|<span data-ttu-id="5558b-860">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-860">**Issuer**</span></span>|
|<span data-ttu-id="5558b-861">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-861"></span></span>|
|<span data-ttu-id="5558b-862">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-862">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-863">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-863"></span></span>|
|<span data-ttu-id="5558b-864">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-864">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-865">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-865"></span></span>|
|<span data-ttu-id="5558b-866">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-867">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-867"></span></span>|
|<span data-ttu-id="5558b-868">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-869">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-869"></span></span>|
|<span data-ttu-id="5558b-870">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-870">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-871">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-871"></span></span>|
|<span data-ttu-id="5558b-872">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-873">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-873"></span></span>|
|<span data-ttu-id="5558b-874">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-875">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-875"></span></span>|
|<span data-ttu-id="5558b-876">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-877">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-877"></span></span>|
|<span data-ttu-id="5558b-878">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-879">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-879"></span></span>|
|<span data-ttu-id="5558b-880">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-881">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-881"></span></span>|
|<span data-ttu-id="5558b-882">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-882">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-883">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-883"></span></span>|
   
 <span data-ttu-id="5558b-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="5558b-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-885">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-885">**Subject**</span></span>|
|<span data-ttu-id="5558b-886">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-886"></span></span>|
|<span data-ttu-id="5558b-887">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-887">**Issuer**</span></span>|
|<span data-ttu-id="5558b-888">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-888"></span></span>|
|<span data-ttu-id="5558b-889">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-889">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-890">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-890"></span></span>|
|<span data-ttu-id="5558b-891">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-891">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-892">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-892"></span></span>|
|<span data-ttu-id="5558b-893">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-894">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-894"></span></span>|
|<span data-ttu-id="5558b-895">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-896">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-896"></span></span>|
|<span data-ttu-id="5558b-897">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-897">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-898">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-898"></span></span>|
|<span data-ttu-id="5558b-899">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-900">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-900"></span></span>|
|<span data-ttu-id="5558b-901">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-902">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-902"></span></span>|
|<span data-ttu-id="5558b-903">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-904">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-904"></span></span>|
|<span data-ttu-id="5558b-905">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-906">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-906"></span></span>|
|<span data-ttu-id="5558b-907">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-908">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-908"></span></span>|
|<span data-ttu-id="5558b-909">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-909">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-910">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-910"></span></span>|
|<span data-ttu-id="5558b-911">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-912">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-912"></span></span>|
   
 <span data-ttu-id="5558b-913">**Microsoft IT TLS CA 1**</span><span class="sxs-lookup"><span data-stu-id="5558b-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-914">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-914">**Subject**</span></span>|
|<span data-ttu-id="5558b-915">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-915"></span></span>|
|<span data-ttu-id="5558b-916">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-916">**Issuer**</span></span>|
|<span data-ttu-id="5558b-917">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-917"></span></span>|
|<span data-ttu-id="5558b-918">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-918">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-919">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-919"></span></span>|
|<span data-ttu-id="5558b-920">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-920">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-921">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-921"></span></span>|
|<span data-ttu-id="5558b-922">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-923">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-923"></span></span>|
|<span data-ttu-id="5558b-924">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-925">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-925"></span></span>|
|<span data-ttu-id="5558b-926">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-926">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-927">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-927"></span></span>|
|<span data-ttu-id="5558b-928">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-929">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-929"></span></span>|
|<span data-ttu-id="5558b-930">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-931">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-931"></span></span>|
|<span data-ttu-id="5558b-932">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-933">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-933"></span></span>|
|<span data-ttu-id="5558b-934">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-935">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-935"></span></span>|
|<span data-ttu-id="5558b-936">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-937">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-937"></span></span>|
|<span data-ttu-id="5558b-938">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-938">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-939">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-939"></span></span>|
|<span data-ttu-id="5558b-940">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-941">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-941"></span></span>|
   
 <span data-ttu-id="5558b-942">**Microsoft IT TLS CA 2**</span><span class="sxs-lookup"><span data-stu-id="5558b-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-943">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-943">**Subject**</span></span>|
|<span data-ttu-id="5558b-944">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-944"></span></span>|
|<span data-ttu-id="5558b-945">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-945">**Issuer**</span></span>|
|<span data-ttu-id="5558b-946">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-946"></span></span>|
|<span data-ttu-id="5558b-947">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-947">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-948">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-948"></span></span>|
|<span data-ttu-id="5558b-949">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-949">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-950">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-950"></span></span>|
|<span data-ttu-id="5558b-951">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-952">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-952"></span></span>|
|<span data-ttu-id="5558b-953">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-954">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-954"></span></span>|
|<span data-ttu-id="5558b-955">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-955">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-956">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-956"></span></span>|
|<span data-ttu-id="5558b-957">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-958">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-958"></span></span>|
|<span data-ttu-id="5558b-959">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-960">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-960"></span></span>|
|<span data-ttu-id="5558b-961">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-962">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-962"></span></span>|
|<span data-ttu-id="5558b-963">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-964">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-964"></span></span>|
|<span data-ttu-id="5558b-965">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-966">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-966"></span></span>|
|<span data-ttu-id="5558b-967">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-967">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-968">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-968"></span></span>|
|<span data-ttu-id="5558b-969">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-970">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-970"></span></span>|
   
 <span data-ttu-id="5558b-971">**Microsoft IT TLS CA 4**</span><span class="sxs-lookup"><span data-stu-id="5558b-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-972">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-972">**Subject**</span></span>|
|<span data-ttu-id="5558b-973">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-973"></span></span>|
|<span data-ttu-id="5558b-974">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-974">**Issuer**</span></span>|
|<span data-ttu-id="5558b-975">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-975"></span></span>|
|<span data-ttu-id="5558b-976">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-976">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-977">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-977"></span></span>|
|<span data-ttu-id="5558b-978">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-978">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-979">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-979"></span></span>|
|<span data-ttu-id="5558b-980">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-981">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-981"></span></span>|
|<span data-ttu-id="5558b-982">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-983">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-983"></span></span>|
|<span data-ttu-id="5558b-984">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-984">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-985">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-985"></span></span>|
|<span data-ttu-id="5558b-986">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-987">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-987"></span></span>|
|<span data-ttu-id="5558b-988">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-989">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-989"></span></span>|
|<span data-ttu-id="5558b-990">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-991">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-991"></span></span>|
|<span data-ttu-id="5558b-992">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-993">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-993"></span></span>|
|<span data-ttu-id="5558b-994">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-995">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-995"></span></span>|
|<span data-ttu-id="5558b-996">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-996">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-997">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-997"></span></span>|
|<span data-ttu-id="5558b-998">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-999">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-999"></span></span>|
   
 <span data-ttu-id="5558b-1000">**Microsoft IT TLS CA 5**</span><span class="sxs-lookup"><span data-stu-id="5558b-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-1001">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-1001">**Subject**</span></span>|
|<span data-ttu-id="5558b-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1002"></span></span>|
|<span data-ttu-id="5558b-1003">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-1003">**Issuer**</span></span>|
|<span data-ttu-id="5558b-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1004"></span></span>|
|<span data-ttu-id="5558b-1005">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-1005">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1006"></span></span>|
|<span data-ttu-id="5558b-1007">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1008"></span></span>|
|<span data-ttu-id="5558b-1009">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1010"></span></span>|
|<span data-ttu-id="5558b-1011">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1012"></span></span>|
|<span data-ttu-id="5558b-1013">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1014"></span></span>|
|<span data-ttu-id="5558b-1015">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1016"></span></span>|
|<span data-ttu-id="5558b-1017">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1018"></span></span>|
|<span data-ttu-id="5558b-1019">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1020"></span></span>|
|<span data-ttu-id="5558b-1021">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1022"></span></span>|
|<span data-ttu-id="5558b-1023">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1024"></span></span>|
|<span data-ttu-id="5558b-1025">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1026"></span></span>|
|<span data-ttu-id="5558b-1027">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1028"></span></span>|
   
 <span data-ttu-id="5558b-1029">**Symantec 클래스 3 EV SSL CA-G3**</span><span class="sxs-lookup"><span data-stu-id="5558b-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-1030">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-1030">**Subject**</span></span>|
|<span data-ttu-id="5558b-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1031"></span></span>|
|<span data-ttu-id="5558b-1032">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-1032">**Issuer**</span></span>|
|<span data-ttu-id="5558b-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1033"></span></span>|
|<span data-ttu-id="5558b-1034">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="5558b-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="5558b-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1035"></span></span>|
|<span data-ttu-id="5558b-1036">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-1036">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1037"></span></span>|
|<span data-ttu-id="5558b-1038">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1039"></span></span>|
|<span data-ttu-id="5558b-1040">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1041"></span></span>|
|<span data-ttu-id="5558b-1042">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1043"></span></span>|
|<span data-ttu-id="5558b-1044">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1045"></span></span>|
|<span data-ttu-id="5558b-1046">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1047"></span></span>|
|<span data-ttu-id="5558b-1048">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1049"></span></span>|
|<span data-ttu-id="5558b-1050">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1051"></span></span>|
|<span data-ttu-id="5558b-1052">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1053"></span></span>|
|<span data-ttu-id="5558b-1054">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1055"></span></span>|
|<span data-ttu-id="5558b-1056">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1057"></span></span>|
|<span data-ttu-id="5558b-1058">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1059"></span></span>|
   
 <span data-ttu-id="5558b-1060">**Symantec 클래스 3 안전한 서버 CA-G4**</span><span class="sxs-lookup"><span data-stu-id="5558b-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-1061">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-1061">**Subject**</span></span>|
|<span data-ttu-id="5558b-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1062"></span></span>|
|<span data-ttu-id="5558b-1063">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-1063">**Issuer**</span></span>|
|<span data-ttu-id="5558b-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1064"></span></span>|
|<span data-ttu-id="5558b-1065">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="5558b-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="5558b-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1066"></span></span>|
|<span data-ttu-id="5558b-1067">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-1067">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1068"></span></span>|
|<span data-ttu-id="5558b-1069">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1070"></span></span>|
|<span data-ttu-id="5558b-1071">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1072"></span></span>|
|<span data-ttu-id="5558b-1073">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1074"></span></span>|
|<span data-ttu-id="5558b-1075">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1076"></span></span>|
|<span data-ttu-id="5558b-1077">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1078"></span></span>|
|<span data-ttu-id="5558b-1079">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1080"></span></span>|
|<span data-ttu-id="5558b-1081">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1082"></span></span>|
|<span data-ttu-id="5558b-1083">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1084"></span></span>|
|<span data-ttu-id="5558b-1085">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1086"></span></span>|
|<span data-ttu-id="5558b-1087">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1088"></span></span>|
|<span data-ttu-id="5558b-1089">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1090"></span></span>|
   
 <span data-ttu-id="5558b-1091">**thawte SHA256 SSL CA**</span><span class="sxs-lookup"><span data-stu-id="5558b-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-1092">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-1092">**Subject**</span></span>|
|<span data-ttu-id="5558b-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1093"></span></span>|
|<span data-ttu-id="5558b-1094">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-1094">**Issuer**</span></span>|
|<span data-ttu-id="5558b-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1095"></span></span>|
|<span data-ttu-id="5558b-1096">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="5558b-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="5558b-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1097"></span></span>|
|<span data-ttu-id="5558b-1098">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-1098">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1099"></span></span>|
|<span data-ttu-id="5558b-1100">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1101"></span></span>|
|<span data-ttu-id="5558b-1102">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1103"></span></span>|
|<span data-ttu-id="5558b-1104">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1105"></span></span>|
|<span data-ttu-id="5558b-1106">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1107"></span></span>|
|<span data-ttu-id="5558b-1108">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1109"></span></span>|
|<span data-ttu-id="5558b-1110">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1111"></span></span>|
|<span data-ttu-id="5558b-1112">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1113"></span></span>|
|<span data-ttu-id="5558b-1114">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1115"></span></span>|
|<span data-ttu-id="5558b-1116">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1117"></span></span>|
|<span data-ttu-id="5558b-1118">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1119"></span></span>|
|<span data-ttu-id="5558b-1120">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1121"></span></span>|
   
 <span data-ttu-id="5558b-1122">**Verizon Akamai SureServer CA g 14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="5558b-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="5558b-1123">**제목**</span><span class="sxs-lookup"><span data-stu-id="5558b-1123">**Subject**</span></span>|
|<span data-ttu-id="5558b-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1124"></span></span>|
|<span data-ttu-id="5558b-1125">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="5558b-1125">**Issuer**</span></span>|
|<span data-ttu-id="5558b-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1126"></span></span>|
|<span data-ttu-id="5558b-1127">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="5558b-1127">**Serial Number**</span></span>|
|<span data-ttu-id="5558b-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1128"></span></span>|
|<span data-ttu-id="5558b-1129">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="5558b-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="5558b-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1130"></span></span>|
|<span data-ttu-id="5558b-1131">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="5558b-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="5558b-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1132"></span></span>|
|<span data-ttu-id="5558b-1133">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="5558b-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="5558b-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1134"></span></span>|
|<span data-ttu-id="5558b-1135">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="5558b-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="5558b-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1136"></span></span>|
|<span data-ttu-id="5558b-1137">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1138"></span></span>|
|<span data-ttu-id="5558b-1139">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="5558b-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="5558b-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1140"></span></span>|
|<span data-ttu-id="5558b-1141">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="5558b-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1142"></span></span>|
|<span data-ttu-id="5558b-1143">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1144"></span></span>|
|<span data-ttu-id="5558b-1145">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="5558b-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="5558b-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1146"></span></span>|
|<span data-ttu-id="5558b-1147">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="5558b-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1148"></span></span>|
|<span data-ttu-id="5558b-1149">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="5558b-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1150"></span></span>|
|<span data-ttu-id="5558b-1151">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="5558b-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="5558b-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="5558b-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="5558b-1153">추가 인증서 경로</span><span class="sxs-lookup"><span data-stu-id="5558b-1153">Additional certificate paths</span></span>
<span data-ttu-id="5558b-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="5558b-1154"></span></span>

<span data-ttu-id="5558b-1155">다음은 위에 포함 되지 않은 시간에 따른 위의 목록을 사용 하 여 병합 될 하 레거시 인증서를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="5558b-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
```
evsecure-aia.verisign.com
sa.symcb.com
sd.symcb.com
*.omniroot.com
*.verisign.com
*.symcb.com
*.symcd.com
*.verisign.net
*.geotrust.com
*.entrust.net
*.public-trust.com
EVIntl-ocsp.verisign.com
EVSecure-ocsp.verisign.com
isrg.trustid.ocsp.identrust.com
ocsp.digicert.com
ocsp.entrust.net
ocsp.globalsign.com/ExtendedSSLSHA256CACross
ocsp.globalsign.com/rootr1
ocsp.globalsign.com/rootr2
ocsp2.globalsign.com/rootr3
ocsp.int-x3.letsencrypt.org/
ocsp.msocsp.com
ocsp.omniroot.com/baltimoreroot
ocsp2.globalsign.com/gsextendvalsha2g3r3
ocsp2.globalsign.com/gsorganizationvalsha2g2
ocsp2.globalsign.com/gsorganizationvalsha2g3
ocsp2.globalsign.com/rootr3
ocspx.digicert.com
s2.symcb.com
sr.symcd.com
su.symcd.com
vassg142.ocsp.omniroot.com
cdp1.public-trust.com/CRL/Omniroot2025.crl
crl.entrust.net/2048ca.crl
crl.entrust.net/g2ca.crl
crl.entrust.net/level1k.crl
crl.entrust.net/rootca1.crl
crl.globalsign.com/gs/gsextendvalsha2g3r3.crl
crl.globalsign.com/gs/gsorganizationvalsha2g2.crl
crl.globalsign.com/gsorganizationvalsha2g3.crl
crl.globalsign.com/root.crl
crl.globalsign.net/root-r2.crl
crl.globalsign.com/root-r3.crl
crl.globalsign.net/root.crl
crl.identrust.com/DSTROOTCAX3CRL.crl
crl.microsoft.com/pki/mscorp/crl/msitwww1.crl
crl.microsoft.com/pki/mscorp/crl/msitwww2.crl
crl3.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl3.digicert.com/DigiCertGlobalRootCA.crl
crl3.digicert.com/sha2-ev-server-g1.crl
crl3.digicert.com/sha2-ha-server-g5.crl
crl3.digicert.com/ssca-sha2-g5.crl
crl4.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl4.digicert.com/DigiCertGlobalRootCA.crl
crl4.digicert.com/DigiCertHighAssuranceEVRootCA.crl
crl4.digicert.com/sha2-ev-server-g1.crl
crl4.digicert.com/sha2-ha-server-g5.crl
crl4.digicert.com/ssca-sha2-g5.crl
EVIntl-crl.verisign.com/EVIntl2006.crl
EVSecure-crl.verisign.com/pca3-g5.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww1.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww2.crl
s1.symcb.com/pca3-g5.crl
sr.symcb.com/sr.crl
su.symcb.com/su.crl
vassg142.crl.omniroot.com/vassg142.crl
aia.entrust.net/l1k-chain256.cer
apps.identrust.com/roots/dstrootcax3.p7c
https://cacert.a.omniroot.com/vassg142.crt
https://cacert.a.omniroot.com/vassg142.der
https://cacert.omniroot.com/baltimoreroot.crt
https://cacert.omniroot.com/baltimoreroot.der
cacerts.digicert.com/DigiCertCloudServicesCA-1.crt
cacerts.digicert.com/DigiCertSHA2ExtendedValidationServerCA.crt
cacerts.digicert.com/DigiCertSHA2HighAssuranceServerCA.crt
cacerts.digicert.com/DigiCertSHA2SecureServerCA.crt
cert.int-x3.letsencrypt.org/
EVIntl-aia.verisign.com/EVIntl2006.cer
secure.globalsign.com/cacert/gsextendvalsha2g2r2.crt
secure.globalsign.com/cacert/gsextendvalsha2g3r3.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g2r1.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g3.crt
sr.symcb.com/sr.crt
su.symcb.com/su.crt
https://www.digicert.com/CACerts/DigiCertGlobalRootCA.crt
https://www.digicert.com/CACerts/DigiCertHighAssuranceEVRootCA.crt
www.microsoft.com/pki/mscorp/msitwww1.crt
www.microsoft.com/pki/mscorp/msitwww2.crt

```


