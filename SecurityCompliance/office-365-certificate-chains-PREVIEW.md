---
title: Office 365 인증서 체인
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 기술을 활용 하는 다른 인증서 공급자의 수입니다. 다음은 고객이 Office 365에 액세스할 때 발생할 수 있는 알려진된 Office 365 루트 인증서의 전체 목록에 대 한 설명입니다. 인증서에 대 한 정보 직접 인프라에 설치 Office 365 용 타사 SSL 인증서에 대 한 계획을 참조 하십시오 해야할 수 있습니다. 다음 인증서 정보는 Office 365의 모든 전세계 및 국가 클라우드 인스턴스에 적용 됩니다.
ms.openlocfilehash: 1dcc2dc38bb8e3239a3be3983791b0c60917dc5e
ms.sourcegitcommit: 13f40ff7c1799152bf45af2d8110f4f3235b770a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "25549765"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="87487-106">Office 365 인증서 체인</span><span class="sxs-lookup"><span data-stu-id="87487-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="87487-p102">Office 365 기술을 활용 하는 다른 인증서 공급자의 수입니다. 다음은 고객이 Office 365에 액세스할 때 발생할 수 있는 알려진된 Office 365 루트 인증서의 전체 목록에 대 한 설명입니다. 직접 인프라에 설치 해야할 수 인증서는 정보를 [Office 365 용 타사 SSL 인증서에 대 한 계획을](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce)참조 합니다. 다음 인증서 정보는 Office 365의 모든 전세계 및 국가 클라우드 인스턴스에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87487-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="87487-111">**인증서 유형**</span><span class="sxs-lookup"><span data-stu-id="87487-111">**Certificate type**</span></span>|<span data-ttu-id="87487-112">**여.p7b 다운로드**</span><span class="sxs-lookup"><span data-stu-id="87487-112">**P7b download**</span></span>|<span data-ttu-id="87487-113">**CRL 끝점**</span><span class="sxs-lookup"><span data-stu-id="87487-113">**CRL Endpoints**</span></span>|<span data-ttu-id="87487-114">**OCSP 끝점**</span><span class="sxs-lookup"><span data-stu-id="87487-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="87487-115">**AIA 끝점**</span><span class="sxs-lookup"><span data-stu-id="87487-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="87487-116">공개적으로 신뢰할 수 있는 루트 인증서</span><span class="sxs-lookup"><span data-stu-id="87487-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="87487-117">Office 365 루트 인증서 번들 (여.p7b)</span><span class="sxs-lookup"><span data-stu-id="87487-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="87487-118">crl.globalsign.net</span><span class="sxs-lookup"><span data-stu-id="87487-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="87487-119">www.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="87487-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="87487-120">해당 없음</span><span class="sxs-lookup"><span data-stu-id="87487-120">N/A</span></span>  <br/> |<span data-ttu-id="87487-121">해당 없음</span><span class="sxs-lookup"><span data-stu-id="87487-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="87487-122">공개적으로 신뢰할 수 있는 중간 인증서</span><span class="sxs-lookup"><span data-stu-id="87487-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="87487-123">Office 365 중간 인증서 번들 (여.p7b)</span><span class="sxs-lookup"><span data-stu-id="87487-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="87487-124">cdp1.public trust.com</span><span class="sxs-lookup"><span data-stu-id="87487-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="87487-125">crl.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="87487-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="87487-126">crl.entrust.net</span><span class="sxs-lookup"><span data-stu-id="87487-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="87487-127">crl.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="87487-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="87487-128">crl.globalsign.net</span><span class="sxs-lookup"><span data-stu-id="87487-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="87487-129">crl.identrust.com</span><span class="sxs-lookup"><span data-stu-id="87487-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="87487-130">crl.thawte.com</span><span class="sxs-lookup"><span data-stu-id="87487-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="87487-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="87487-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="87487-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="87487-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="87487-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="87487-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="87487-134">www.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="87487-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="87487-135">isrg.trustid.ocsp.identrust.com</span><span class="sxs-lookup"><span data-stu-id="87487-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="87487-136">ocsp.digicert.com</span><span class="sxs-lookup"><span data-stu-id="87487-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="87487-137">ocsp.entrust.net</span><span class="sxs-lookup"><span data-stu-id="87487-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="87487-138">ocsp.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="87487-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="87487-139">ocsp.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="87487-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="87487-140">ocsp.startssl.com</span><span class="sxs-lookup"><span data-stu-id="87487-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="87487-141">ocsp.thawte.com</span><span class="sxs-lookup"><span data-stu-id="87487-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="87487-142">ocsp2.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="87487-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="87487-143">ocspcnnicroot.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="87487-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="87487-144">루트-c3-c a 2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="87487-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="87487-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="87487-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="87487-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="87487-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="87487-147">aia.startssl.com</span><span class="sxs-lookup"><span data-stu-id="87487-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="87487-148">apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="87487-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="87487-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="87487-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="87487-150">www.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="87487-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="87487-151">루트 및 인증서 공급자에 대 한 추가 세부 정보를 보려면 아래 중간 섹션을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87487-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="87487-152">Office 365 루트 인증서 세부 정보</span><span class="sxs-lookup"><span data-stu-id="87487-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="87487-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="87487-153"></span></span>

 <span data-ttu-id="87487-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="87487-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="87487-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="87487-155">|:-----|</span></span>
|<span data-ttu-id="87487-156">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="87487-157">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-157">**Serial Number**</span></span>|
|<span data-ttu-id="87487-158">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-158"></span></span>|
|<span data-ttu-id="87487-159">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-159">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-160">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-160"></span></span>|
|<span data-ttu-id="87487-161">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-162">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-162"></span></span>|
|<span data-ttu-id="87487-163">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-164">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-164"></span></span>|
|<span data-ttu-id="87487-165">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-165">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-166">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-166"></span></span>|
|<span data-ttu-id="87487-167">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-168">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-168"></span></span>|
|<span data-ttu-id="87487-169">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-170">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-170"></span></span>|
|<span data-ttu-id="87487-171">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-172">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-172"></span></span>|
|<span data-ttu-id="87487-173">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-174">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-174"></span></span>|
   
 <span data-ttu-id="87487-175">**CNNIC 루트**</span><span class="sxs-lookup"><span data-stu-id="87487-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-176">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-176">**Subject**</span></span>|
|<span data-ttu-id="87487-177">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-177"></span></span>|
|<span data-ttu-id="87487-178">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-178">**Serial Number**</span></span>|
|<span data-ttu-id="87487-179">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-179"></span></span>|
|<span data-ttu-id="87487-180">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-180">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-181">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-181"></span></span>|
|<span data-ttu-id="87487-182">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-183">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-183"></span></span>|
|<span data-ttu-id="87487-184">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-185">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-185"></span></span>|
|<span data-ttu-id="87487-186">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-186">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-187">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-187"></span></span>|
|<span data-ttu-id="87487-188">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-189">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-189"></span></span>|
|<span data-ttu-id="87487-190">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-191">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-191"></span></span>|
|<span data-ttu-id="87487-192">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-193">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-193"></span></span>|
|<span data-ttu-id="87487-194">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-195">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-195"></span></span>|
|<span data-ttu-id="87487-196">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-197">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-197"></span></span>|
   
 <span data-ttu-id="87487-198">**DigiCert 전역 루트 CA**</span><span class="sxs-lookup"><span data-stu-id="87487-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-199">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-199">**Subject**</span></span>|
|<span data-ttu-id="87487-200">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-200"></span></span>|
|<span data-ttu-id="87487-201">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-201">**Serial Number**</span></span>|
|<span data-ttu-id="87487-202">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-202"></span></span>|
|<span data-ttu-id="87487-203">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-203">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-204">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-204"></span></span>|
|<span data-ttu-id="87487-205">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-206">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-206"></span></span>|
|<span data-ttu-id="87487-207">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-208">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-208"></span></span>|
|<span data-ttu-id="87487-209">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-209">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-210">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-210"></span></span>|
|<span data-ttu-id="87487-211">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-212">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-212"></span></span>|
|<span data-ttu-id="87487-213">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-214">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-214"></span></span>|
|<span data-ttu-id="87487-215">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-216">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-216"></span></span>|
|<span data-ttu-id="87487-217">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-218">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-218"></span></span>|
|<span data-ttu-id="87487-219">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-220">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-220"></span></span>|
   
 <span data-ttu-id="87487-221">**DigiCert 높은 보증 EV 루트 CA**</span><span class="sxs-lookup"><span data-stu-id="87487-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-222">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-222">**Subject**</span></span>|
|<span data-ttu-id="87487-223">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-223"></span></span>|
|<span data-ttu-id="87487-224">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-224">**Serial Number**</span></span>|
|<span data-ttu-id="87487-225">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-225"></span></span>|
|<span data-ttu-id="87487-226">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-226">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-227">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-227"></span></span>|
|<span data-ttu-id="87487-228">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-229">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-229"></span></span>|
|<span data-ttu-id="87487-230">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-231">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-231"></span></span>|
|<span data-ttu-id="87487-232">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-232">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-233">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-233"></span></span>|
|<span data-ttu-id="87487-234">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-235">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-235"></span></span>|
|<span data-ttu-id="87487-236">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-237">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-237"></span></span>|
|<span data-ttu-id="87487-238">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-239">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-239"></span></span>|
|<span data-ttu-id="87487-240">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-241">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-241"></span></span>|
|<span data-ttu-id="87487-242">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-243">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-243"></span></span>|
   
 <span data-ttu-id="87487-244">**D-신뢰 루트 클래스 3 CA 2 2009**</span><span class="sxs-lookup"><span data-stu-id="87487-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-245">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-245">**Subject**</span></span>|
|<span data-ttu-id="87487-246">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-246"></span></span>|
|<span data-ttu-id="87487-247">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-247">**Serial Number**</span></span>|
|<span data-ttu-id="87487-248">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-248"></span></span>|
|<span data-ttu-id="87487-249">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-249">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-250">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-250"></span></span>|
|<span data-ttu-id="87487-251">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-252">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-252"></span></span>|
|<span data-ttu-id="87487-253">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-254">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-254"></span></span>|
|<span data-ttu-id="87487-255">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-255">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-256">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-256"></span></span>|
|<span data-ttu-id="87487-257">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-258">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-258"></span></span>|
|<span data-ttu-id="87487-259">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-260">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-260"></span></span>|
|<span data-ttu-id="87487-261">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-262">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-262"></span></span>|
|<span data-ttu-id="87487-263">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-264">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-264"></span></span>|
|<span data-ttu-id="87487-265">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-265">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-266">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-266"></span></span>|
   
 <span data-ttu-id="87487-267">**D-신뢰 루트 클래스 3 CA 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="87487-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-268">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-268">**Subject**</span></span>|
|<span data-ttu-id="87487-269">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-269"></span></span>|
|<span data-ttu-id="87487-270">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-270">**Serial Number**</span></span>|
|<span data-ttu-id="87487-271">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-271"></span></span>|
|<span data-ttu-id="87487-272">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-272">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-273">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-273"></span></span>|
|<span data-ttu-id="87487-274">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-275">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-275"></span></span>|
|<span data-ttu-id="87487-276">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-277">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-277"></span></span>|
|<span data-ttu-id="87487-278">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-278">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-279">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-279"></span></span>|
|<span data-ttu-id="87487-280">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-281">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-281"></span></span>|
|<span data-ttu-id="87487-282">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-283">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-283"></span></span>|
|<span data-ttu-id="87487-284">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-285">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-285"></span></span>|
|<span data-ttu-id="87487-286">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-287">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-287"></span></span>|
|<span data-ttu-id="87487-288">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-288">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-289">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-289"></span></span>|
   
 <span data-ttu-id="87487-290">**DST 루트 CA X3**</span><span class="sxs-lookup"><span data-stu-id="87487-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-291">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-291">**Subject**</span></span>|
|<span data-ttu-id="87487-292">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-292"></span></span>|
|<span data-ttu-id="87487-293">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-293">**Serial Number**</span></span>|
|<span data-ttu-id="87487-294">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-294"></span></span>|
|<span data-ttu-id="87487-295">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-295">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-296">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-296"></span></span>|
|<span data-ttu-id="87487-297">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-298">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-298"></span></span>|
|<span data-ttu-id="87487-299">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-300">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-300"></span></span>|
|<span data-ttu-id="87487-301">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-301">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-302">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-302"></span></span>|
|<span data-ttu-id="87487-303">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-304">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-304"></span></span>|
|<span data-ttu-id="87487-305">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-306">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-306"></span></span>|
|<span data-ttu-id="87487-307">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-308">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-308"></span></span>|
|<span data-ttu-id="87487-309">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-310">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-310"></span></span>|
   
 <span data-ttu-id="87487-311">**루트 인증 기관-G2 맡길**</span><span class="sxs-lookup"><span data-stu-id="87487-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-312">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-312">**Subject**</span></span>|
|<span data-ttu-id="87487-313">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-313"></span></span>|
|<span data-ttu-id="87487-314">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-314">**Serial Number**</span></span>|
|<span data-ttu-id="87487-315">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-315"></span></span>|
|<span data-ttu-id="87487-316">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-316">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-317">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-317"></span></span>|
|<span data-ttu-id="87487-318">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-319">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-319"></span></span>|
|<span data-ttu-id="87487-320">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-321">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-321"></span></span>|
|<span data-ttu-id="87487-322">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-322">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-323">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-323"></span></span>|
|<span data-ttu-id="87487-324">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-325">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-325"></span></span>|
|<span data-ttu-id="87487-326">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-327">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-327"></span></span>|
|<span data-ttu-id="87487-328">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-329">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-329"></span></span>|
|<span data-ttu-id="87487-330">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-331">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-331"></span></span>|
   
 <span data-ttu-id="87487-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="87487-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-333">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-333">**Subject**</span></span>|
|<span data-ttu-id="87487-334">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-334"></span></span>|
|<span data-ttu-id="87487-335">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-335">**Serial Number**</span></span>|
|<span data-ttu-id="87487-336">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-336"></span></span>|
|<span data-ttu-id="87487-337">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-337">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-338">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-338"></span></span>|
|<span data-ttu-id="87487-339">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-340">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-340"></span></span>|
|<span data-ttu-id="87487-341">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-342">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-342"></span></span>|
|<span data-ttu-id="87487-343">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-343">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-344">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-344"></span></span>|
|<span data-ttu-id="87487-345">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-346">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-346"></span></span>|
|<span data-ttu-id="87487-347">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-348">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-348"></span></span>|
|<span data-ttu-id="87487-349">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-350">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-350"></span></span>|
|<span data-ttu-id="87487-351">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-352">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-352"></span></span>|
   
 <span data-ttu-id="87487-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="87487-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-354">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-354">**Subject**</span></span>|
|<span data-ttu-id="87487-355">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-355"></span></span>|
|<span data-ttu-id="87487-356">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-356">**Serial Number**</span></span>|
|<span data-ttu-id="87487-357">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-357"></span></span>|
|<span data-ttu-id="87487-358">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-358">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-359">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-359"></span></span>|
|<span data-ttu-id="87487-360">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-361">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-361"></span></span>|
|<span data-ttu-id="87487-362">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-363">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-363"></span></span>|
|<span data-ttu-id="87487-364">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-364">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-365">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-365"></span></span>|
|<span data-ttu-id="87487-366">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-367">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-367"></span></span>|
|<span data-ttu-id="87487-368">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-369">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-369"></span></span>|
|<span data-ttu-id="87487-370">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-371">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-371"></span></span>|
|<span data-ttu-id="87487-372">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-373">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-373"></span></span>|
|<span data-ttu-id="87487-374">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-375">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-375"></span></span>|
|<span data-ttu-id="87487-376">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-376">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-377">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-377"></span></span>|
   
 <span data-ttu-id="87487-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="87487-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-379">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-379">**Subject**</span></span>|
|<span data-ttu-id="87487-380">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-380"></span></span>|
|<span data-ttu-id="87487-381">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-381">**Serial Number**</span></span>|
|<span data-ttu-id="87487-382">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-382"></span></span>|
|<span data-ttu-id="87487-383">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-383">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-384">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-384"></span></span>|
|<span data-ttu-id="87487-385">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-386">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-386"></span></span>|
|<span data-ttu-id="87487-387">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-388">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-388"></span></span>|
|<span data-ttu-id="87487-389">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-389">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-390">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-390"></span></span>|
|<span data-ttu-id="87487-391">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-392">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-392"></span></span>|
|<span data-ttu-id="87487-393">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-394">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-394"></span></span>|
|<span data-ttu-id="87487-395">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-396">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-396"></span></span>|
|<span data-ttu-id="87487-397">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-398">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-398"></span></span>|
   
 <span data-ttu-id="87487-399">**thawte 기본 루트 CA-G3**</span><span class="sxs-lookup"><span data-stu-id="87487-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-400">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-400">**Subject**</span></span>|
|<span data-ttu-id="87487-401">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-401"></span></span>|
|<span data-ttu-id="87487-402">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-402">**Serial Number**</span></span>|
|<span data-ttu-id="87487-403">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-403"></span></span>|
|<span data-ttu-id="87487-404">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-404">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-405">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-405"></span></span>|
|<span data-ttu-id="87487-406">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-407">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-407"></span></span>|
|<span data-ttu-id="87487-408">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-409">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-409"></span></span>|
|<span data-ttu-id="87487-410">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-410">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-411">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-411"></span></span>|
|<span data-ttu-id="87487-412">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-413">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-413"></span></span>|
|<span data-ttu-id="87487-414">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-415">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-415"></span></span>|
|<span data-ttu-id="87487-416">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-417">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-417"></span></span>|
|<span data-ttu-id="87487-418">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-419">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-419"></span></span>|
   
 <span data-ttu-id="87487-420">**VeriSign 클래스 3 기본 공용 인증 기관-g 5**</span><span class="sxs-lookup"><span data-stu-id="87487-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-421">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-421">**Subject**</span></span>|
|<span data-ttu-id="87487-422">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-422"></span></span>|
|<span data-ttu-id="87487-423">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-423">**Serial Number**</span></span>|
|<span data-ttu-id="87487-424">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-424"></span></span>|
|<span data-ttu-id="87487-425">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-425">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-426">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-426"></span></span>|
|<span data-ttu-id="87487-427">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-428">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-428"></span></span>|
|<span data-ttu-id="87487-429">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-430">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-430"></span></span>|
|<span data-ttu-id="87487-431">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-431">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-432">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-432"></span></span>|
|<span data-ttu-id="87487-433">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-434">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-434"></span></span>|
|<span data-ttu-id="87487-435">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-436">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-436"></span></span>|
|<span data-ttu-id="87487-437">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-438">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-438"></span></span>|
|<span data-ttu-id="87487-439">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-440">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="87487-441">Office 365 중간 인증서 세부 정보</span><span class="sxs-lookup"><span data-stu-id="87487-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="87487-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="87487-442"></span></span>

 <span data-ttu-id="87487-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="87487-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-444">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-444">**Subject**</span></span>|
|<span data-ttu-id="87487-445">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-445"></span></span>|
|<span data-ttu-id="87487-446">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-446">**Issuer**</span></span>|
|<span data-ttu-id="87487-447">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-447"></span></span>|
|<span data-ttu-id="87487-448">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-448">**Serial Number**</span></span>|
|<span data-ttu-id="87487-449">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-449"></span></span>|
|<span data-ttu-id="87487-450">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-450">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-451">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-451"></span></span>|
|<span data-ttu-id="87487-452">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-453">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-453"></span></span>|
|<span data-ttu-id="87487-454">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-455">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-455"></span></span>|
|<span data-ttu-id="87487-456">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-456">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-457">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-457"></span></span>|
|<span data-ttu-id="87487-458">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-459">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-459"></span></span>|
|<span data-ttu-id="87487-460">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-461">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-461"></span></span>|
|<span data-ttu-id="87487-462">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-463">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-463"></span></span>|
|<span data-ttu-id="87487-464">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-465">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-465"></span></span>|
|<span data-ttu-id="87487-466">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-467">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-467"></span></span>|
|<span data-ttu-id="87487-468">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="87487-468">**AIA URLs**</span></span>|
|<span data-ttu-id="87487-469">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-469"></span></span>|
|<span data-ttu-id="87487-470">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-470">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-471">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-471"></span></span>|
|<span data-ttu-id="87487-472">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-473">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-473"></span></span>|
   
 <span data-ttu-id="87487-474">**D-신뢰 SSL 클래스 3 CA 1 2009**</span><span class="sxs-lookup"><span data-stu-id="87487-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-475">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-475">**Subject**</span></span>|
|<span data-ttu-id="87487-476">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-476"></span></span>|
|<span data-ttu-id="87487-477">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-477">**Issuer**</span></span>|
|<span data-ttu-id="87487-478">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-478"></span></span>|
|<span data-ttu-id="87487-479">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="87487-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="87487-480">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-480"></span></span>|
|<span data-ttu-id="87487-481">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-481">**Serial Number**</span></span>|
|<span data-ttu-id="87487-482">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-482"></span></span>|
|<span data-ttu-id="87487-483">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-483">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-484">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-484"></span></span>|
|<span data-ttu-id="87487-485">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-486">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-486"></span></span>|
|<span data-ttu-id="87487-487">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-488">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-488"></span></span>|
|<span data-ttu-id="87487-489">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-489">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-490">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-490"></span></span>|
|<span data-ttu-id="87487-491">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-492">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-492"></span></span>|
|<span data-ttu-id="87487-493">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-494">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-494"></span></span>|
|<span data-ttu-id="87487-495">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-496">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-496"></span></span>|
|<span data-ttu-id="87487-497">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-498">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-498"></span></span>|
|<span data-ttu-id="87487-499">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-500">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-500"></span></span>|
|<span data-ttu-id="87487-501">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-501">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-502">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-502"></span></span>|
|<span data-ttu-id="87487-503">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-504">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-504"></span></span>|
   
 <span data-ttu-id="87487-505">**D-신뢰 SSL 클래스 3 CA 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="87487-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-506">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-506">**Subject**</span></span>|
|<span data-ttu-id="87487-507">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-507"></span></span>|
|<span data-ttu-id="87487-508">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-508">**Issuer**</span></span>|
|<span data-ttu-id="87487-509">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-509"></span></span>|
|<span data-ttu-id="87487-510">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="87487-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="87487-511">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-511"></span></span>|
|<span data-ttu-id="87487-512">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-512">**Serial Number**</span></span>|
|<span data-ttu-id="87487-513">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-513"></span></span>|
|<span data-ttu-id="87487-514">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-514">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-515">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-515"></span></span>|
|<span data-ttu-id="87487-516">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-517">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-517"></span></span>|
|<span data-ttu-id="87487-518">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-519">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-519"></span></span>|
|<span data-ttu-id="87487-520">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-520">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-521">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-521"></span></span>|
|<span data-ttu-id="87487-522">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-523">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-523"></span></span>|
|<span data-ttu-id="87487-524">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-525">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-525"></span></span>|
|<span data-ttu-id="87487-526">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-527">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-527"></span></span>|
|<span data-ttu-id="87487-528">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-529">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-529"></span></span>|
|<span data-ttu-id="87487-530">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-531">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-531"></span></span>|
|<span data-ttu-id="87487-532">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-532">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-533">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-533"></span></span>|
|<span data-ttu-id="87487-534">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-535">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-535"></span></span>|
   
 <span data-ttu-id="87487-536">**DigiCert 클라우드 서비스 CA-1**</span><span class="sxs-lookup"><span data-stu-id="87487-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-537">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-537">**Subject**</span></span>|
|<span data-ttu-id="87487-538">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-538"></span></span>|
|<span data-ttu-id="87487-539">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-539">**Issuer**</span></span>|
|<span data-ttu-id="87487-540">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-540"></span></span>|
|<span data-ttu-id="87487-541">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-541">**Serial Number**</span></span>|
|<span data-ttu-id="87487-542">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-542"></span></span>|
|<span data-ttu-id="87487-543">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-543">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-544">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-544"></span></span>|
|<span data-ttu-id="87487-545">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-546">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-546"></span></span>|
|<span data-ttu-id="87487-547">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-548">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-548"></span></span>|
|<span data-ttu-id="87487-549">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-549">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-550">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-550"></span></span>|
|<span data-ttu-id="87487-551">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-552">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-552"></span></span>|
|<span data-ttu-id="87487-553">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-554">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-554"></span></span>|
|<span data-ttu-id="87487-555">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-556">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-556"></span></span>|
|<span data-ttu-id="87487-557">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-558">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-558"></span></span>|
|<span data-ttu-id="87487-559">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-560">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-560"></span></span>|
|<span data-ttu-id="87487-561">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-561">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-562">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-562"></span></span>|
|<span data-ttu-id="87487-563">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-564">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-564"></span></span>|
   
 <span data-ttu-id="87487-565">**DigiCert SHA2 높은 보증 서버 CA**</span><span class="sxs-lookup"><span data-stu-id="87487-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-566">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-566">**Subject**</span></span>|
|<span data-ttu-id="87487-567">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-567"></span></span>|
|<span data-ttu-id="87487-568">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-568">**Issuer**</span></span>|
|<span data-ttu-id="87487-569">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-569"></span></span>|
|<span data-ttu-id="87487-570">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-570">**Serial Number**</span></span>|
|<span data-ttu-id="87487-571">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-571"></span></span>|
|<span data-ttu-id="87487-572">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-572">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-573">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-573"></span></span>|
|<span data-ttu-id="87487-574">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-575">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-575"></span></span>|
|<span data-ttu-id="87487-576">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-577">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-577"></span></span>|
|<span data-ttu-id="87487-578">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-578">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-579">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-579"></span></span>|
|<span data-ttu-id="87487-580">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-581">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-581"></span></span>|
|<span data-ttu-id="87487-582">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-583">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-583"></span></span>|
|<span data-ttu-id="87487-584">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-585">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-585"></span></span>|
|<span data-ttu-id="87487-586">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-587">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-587"></span></span>|
|<span data-ttu-id="87487-588">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-589">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-589"></span></span>|
|<span data-ttu-id="87487-590">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-590">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-591">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-591"></span></span>|
|<span data-ttu-id="87487-592">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-593">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-593"></span></span>|
   
 <span data-ttu-id="87487-594">**DigiCert SHA2 안전한 서버 CA**</span><span class="sxs-lookup"><span data-stu-id="87487-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-595">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-595">**Subject**</span></span>|
|<span data-ttu-id="87487-596">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-596"></span></span>|
|<span data-ttu-id="87487-597">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-597">**Issuer**</span></span>|
|<span data-ttu-id="87487-598">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-598"></span></span>|
|<span data-ttu-id="87487-599">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-599">**Serial Number**</span></span>|
|<span data-ttu-id="87487-600">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-600"></span></span>|
|<span data-ttu-id="87487-601">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-601">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-602">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-602"></span></span>|
|<span data-ttu-id="87487-603">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-604">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-604"></span></span>|
|<span data-ttu-id="87487-605">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-606">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-606"></span></span>|
|<span data-ttu-id="87487-607">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-607">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-608">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-608"></span></span>|
|<span data-ttu-id="87487-609">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-610">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-610"></span></span>|
|<span data-ttu-id="87487-611">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-612">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-612"></span></span>|
|<span data-ttu-id="87487-613">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-614">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-614"></span></span>|
|<span data-ttu-id="87487-615">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-616">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-616"></span></span>|
|<span data-ttu-id="87487-617">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-618">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-618"></span></span>|
|<span data-ttu-id="87487-619">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-619">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-620">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-620"></span></span>|
|<span data-ttu-id="87487-621">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-622">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-622"></span></span>|
   
 <span data-ttu-id="87487-623">**인증 기관-L1C 맡길**</span><span class="sxs-lookup"><span data-stu-id="87487-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-624">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-624">**Subject**</span></span>|
|<span data-ttu-id="87487-625">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-625"></span></span>|
|<span data-ttu-id="87487-626">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-626">**Issuer**</span></span>|
|<span data-ttu-id="87487-627">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-627"></span></span>|
|<span data-ttu-id="87487-628">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-628">**Serial Number**</span></span>|
|<span data-ttu-id="87487-629">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-629"></span></span>|
|<span data-ttu-id="87487-630">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-630">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-631">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-631"></span></span>|
|<span data-ttu-id="87487-632">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-633">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-633"></span></span>|
|<span data-ttu-id="87487-634">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-635">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-635"></span></span>|
|<span data-ttu-id="87487-636">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-636">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-637">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-637"></span></span>|
|<span data-ttu-id="87487-638">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-639">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-639"></span></span>|
|<span data-ttu-id="87487-640">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-641">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-641"></span></span>|
|<span data-ttu-id="87487-642">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-643">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-643"></span></span>|
|<span data-ttu-id="87487-644">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-645">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-645"></span></span>|
|<span data-ttu-id="87487-646">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-647">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-647"></span></span>|
|<span data-ttu-id="87487-648">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-648">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-649">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-649"></span></span>|
|<span data-ttu-id="87487-650">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-651">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-651"></span></span>|
   
 <span data-ttu-id="87487-652">**인증 기관-L1K 맡길**</span><span class="sxs-lookup"><span data-stu-id="87487-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-653">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-653">**Subject**</span></span>|
|<span data-ttu-id="87487-654">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-654"></span></span>|
|<span data-ttu-id="87487-655">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-655">**Issuer**</span></span>|
|<span data-ttu-id="87487-656">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-656"></span></span>|
|<span data-ttu-id="87487-657">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-657">**Serial Number**</span></span>|
|<span data-ttu-id="87487-658">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-658"></span></span>|
|<span data-ttu-id="87487-659">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-659">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-660">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-660"></span></span>|
|<span data-ttu-id="87487-661">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-662">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-662"></span></span>|
|<span data-ttu-id="87487-663">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-664">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-664"></span></span>|
|<span data-ttu-id="87487-665">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-665">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-666">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-666"></span></span>|
|<span data-ttu-id="87487-667">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-668">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-668"></span></span>|
|<span data-ttu-id="87487-669">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-670">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-670"></span></span>|
|<span data-ttu-id="87487-671">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-672">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-672"></span></span>|
|<span data-ttu-id="87487-673">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-674">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-674"></span></span>|
|<span data-ttu-id="87487-675">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-676">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-676"></span></span>|
|<span data-ttu-id="87487-677">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-677">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-678">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-678"></span></span>|
|<span data-ttu-id="87487-679">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-680">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-680"></span></span>|
   
 <span data-ttu-id="87487-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="87487-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-682">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-682">**Subject**</span></span>|
|<span data-ttu-id="87487-683">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-683"></span></span>|
|<span data-ttu-id="87487-684">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-684">**Issuer**</span></span>|
|<span data-ttu-id="87487-685">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-685"></span></span>|
|<span data-ttu-id="87487-686">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-686">**Serial Number**</span></span>|
|<span data-ttu-id="87487-687">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-687"></span></span>|
|<span data-ttu-id="87487-688">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-688">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-689">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-689"></span></span>|
|<span data-ttu-id="87487-690">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-691">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-691"></span></span>|
|<span data-ttu-id="87487-692">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-693">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-693"></span></span>|
|<span data-ttu-id="87487-694">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-694">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-695">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-695"></span></span>|
|<span data-ttu-id="87487-696">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-697">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-697"></span></span>|
|<span data-ttu-id="87487-698">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-699">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-699"></span></span>|
|<span data-ttu-id="87487-700">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-701">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-701"></span></span>|
|<span data-ttu-id="87487-702">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-703">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-703"></span></span>|
|<span data-ttu-id="87487-704">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-705">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-705"></span></span>|
|<span data-ttu-id="87487-706">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-706">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-707">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-707"></span></span>|
|<span data-ttu-id="87487-708">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-709">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-709"></span></span>|
   
 <span data-ttu-id="87487-710">**GlobalSign 유효성 검사 CA-SHA256-g 2를 확장 합니다.**</span><span class="sxs-lookup"><span data-stu-id="87487-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-711">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-711">**Subject**</span></span>|
|<span data-ttu-id="87487-712">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-712"></span></span>|
|<span data-ttu-id="87487-713">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-713">**Issuer**</span></span>|
|<span data-ttu-id="87487-714">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-714"></span></span>|
|<span data-ttu-id="87487-715">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-715">**Serial Number**</span></span>|
|<span data-ttu-id="87487-716">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-716"></span></span>|
|<span data-ttu-id="87487-717">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-717">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-718">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-718"></span></span>|
|<span data-ttu-id="87487-719">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-720">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-720"></span></span>|
|<span data-ttu-id="87487-721">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-722">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-722"></span></span>|
|<span data-ttu-id="87487-723">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-723">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-724">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-724"></span></span>|
|<span data-ttu-id="87487-725">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-726">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-726"></span></span>|
|<span data-ttu-id="87487-727">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-728">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-728"></span></span>|
|<span data-ttu-id="87487-729">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-730">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-730"></span></span>|
|<span data-ttu-id="87487-731">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-732">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-732"></span></span>|
|<span data-ttu-id="87487-733">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-734">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-734"></span></span>|
|<span data-ttu-id="87487-735">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-735">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-736">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-736"></span></span>|
|<span data-ttu-id="87487-737">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-738">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-738"></span></span>|
   
 <span data-ttu-id="87487-739">**GlobalSign 유효성 검사-SHA256-CA G3 확장**</span><span class="sxs-lookup"><span data-stu-id="87487-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-740">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-740">**Subject**</span></span>|
|<span data-ttu-id="87487-741">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-741"></span></span>|
|<span data-ttu-id="87487-742">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-742">**Issuer**</span></span>|
|<span data-ttu-id="87487-743">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-743"></span></span>|
|<span data-ttu-id="87487-744">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-744">**Serial Number**</span></span>|
|<span data-ttu-id="87487-745">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-745"></span></span>|
|<span data-ttu-id="87487-746">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-746">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-747">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-747"></span></span>|
|<span data-ttu-id="87487-748">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-749">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-749"></span></span>|
|<span data-ttu-id="87487-750">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-751">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-751"></span></span>|
|<span data-ttu-id="87487-752">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-752">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-753">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-753"></span></span>|
|<span data-ttu-id="87487-754">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-755">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-755"></span></span>|
|<span data-ttu-id="87487-756">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-757">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-757"></span></span>|
|<span data-ttu-id="87487-758">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-759">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-759"></span></span>|
|<span data-ttu-id="87487-760">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-761">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-761"></span></span>|
|<span data-ttu-id="87487-762">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-763">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-763"></span></span>|
|<span data-ttu-id="87487-764">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-764">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-765">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-765"></span></span>|
|<span data-ttu-id="87487-766">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-767">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-767"></span></span>|
   
 <span data-ttu-id="87487-768">**GlobalSign 조직 유효성 검사 CA-SHA256-g 2**</span><span class="sxs-lookup"><span data-stu-id="87487-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-769">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-769">**Subject**</span></span>|
|<span data-ttu-id="87487-770">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-770"></span></span>|
|<span data-ttu-id="87487-771">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-771">**Issuer**</span></span>|
|<span data-ttu-id="87487-772">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-772"></span></span>|
|<span data-ttu-id="87487-773">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-773">**Serial Number**</span></span>|
|<span data-ttu-id="87487-774">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-774"></span></span>|
|<span data-ttu-id="87487-775">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-775">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-776">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-776"></span></span>|
|<span data-ttu-id="87487-777">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-778">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-778"></span></span>|
|<span data-ttu-id="87487-779">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-780">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-780"></span></span>|
|<span data-ttu-id="87487-781">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-781">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-782">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-782"></span></span>|
|<span data-ttu-id="87487-783">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-784">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-784"></span></span>|
|<span data-ttu-id="87487-785">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-786">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-786"></span></span>|
|<span data-ttu-id="87487-787">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-788">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-788"></span></span>|
|<span data-ttu-id="87487-789">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-790">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-790"></span></span>|
|<span data-ttu-id="87487-791">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-792">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-792"></span></span>|
|<span data-ttu-id="87487-793">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-793">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-794">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-794"></span></span>|
|<span data-ttu-id="87487-795">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-796">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-796"></span></span>|
   
 <span data-ttu-id="87487-797">**GlobalSign 조직 유효성 검사 CA-SHA256-g 2**</span><span class="sxs-lookup"><span data-stu-id="87487-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-798">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-798">**Subject**</span></span>|
|<span data-ttu-id="87487-799">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-799"></span></span>|
|<span data-ttu-id="87487-800">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-800">**Issuer**</span></span>|
|<span data-ttu-id="87487-801">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-801"></span></span>|
|<span data-ttu-id="87487-802">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-802">**Serial Number**</span></span>|
|<span data-ttu-id="87487-803">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-803"></span></span>|
|<span data-ttu-id="87487-804">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-804">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-805">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-805"></span></span>|
|<span data-ttu-id="87487-806">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-807">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-807"></span></span>|
|<span data-ttu-id="87487-808">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-809">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-809"></span></span>|
|<span data-ttu-id="87487-810">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-810">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-811">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-811"></span></span>|
|<span data-ttu-id="87487-812">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-813">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-813"></span></span>|
|<span data-ttu-id="87487-814">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-815">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-815"></span></span>|
|<span data-ttu-id="87487-816">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-817">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-817"></span></span>|
|<span data-ttu-id="87487-818">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-819">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-819"></span></span>|
|<span data-ttu-id="87487-820">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-821">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-821"></span></span>|
|<span data-ttu-id="87487-822">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-822">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-823">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-823"></span></span>|
|<span data-ttu-id="87487-824">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-825">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-825"></span></span>|
   
 <span data-ttu-id="87487-826">**이제 기관 X3 암호화**</span><span class="sxs-lookup"><span data-stu-id="87487-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-827">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-827">**Subject**</span></span>|
|<span data-ttu-id="87487-828">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-828"></span></span>|
|<span data-ttu-id="87487-829">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-829">**Issuer**</span></span>|
|<span data-ttu-id="87487-830">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-830"></span></span>|
|<span data-ttu-id="87487-831">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-831">**Serial Number**</span></span>|
|<span data-ttu-id="87487-832">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-832"></span></span>|
|<span data-ttu-id="87487-833">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-833">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-834">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-834"></span></span>|
|<span data-ttu-id="87487-835">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-836">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-836"></span></span>|
|<span data-ttu-id="87487-837">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-838">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-838"></span></span>|
|<span data-ttu-id="87487-839">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-839">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-840">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-840"></span></span>|
|<span data-ttu-id="87487-841">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-842">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-842"></span></span>|
|<span data-ttu-id="87487-843">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-844">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-844"></span></span>|
|<span data-ttu-id="87487-845">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-846">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-846"></span></span>|
|<span data-ttu-id="87487-847">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-848">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-848"></span></span>|
|<span data-ttu-id="87487-849">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-850">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-850"></span></span>|
|<span data-ttu-id="87487-851">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="87487-851">**AIA URLs**</span></span>|
|<span data-ttu-id="87487-852">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-852"></span></span>|
|<span data-ttu-id="87487-853">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-853">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-854">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-854"></span></span>|
|<span data-ttu-id="87487-855">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-856">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-856"></span></span>|
   
 <span data-ttu-id="87487-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="87487-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-858">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-858">**Subject**</span></span>|
|<span data-ttu-id="87487-859">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-859"></span></span>|
|<span data-ttu-id="87487-860">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-860">**Issuer**</span></span>|
|<span data-ttu-id="87487-861">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-861"></span></span>|
|<span data-ttu-id="87487-862">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-862">**Serial Number**</span></span>|
|<span data-ttu-id="87487-863">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-863"></span></span>|
|<span data-ttu-id="87487-864">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-864">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-865">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-865"></span></span>|
|<span data-ttu-id="87487-866">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-867">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-867"></span></span>|
|<span data-ttu-id="87487-868">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-869">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-869"></span></span>|
|<span data-ttu-id="87487-870">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-870">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-871">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-871"></span></span>|
|<span data-ttu-id="87487-872">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-873">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-873"></span></span>|
|<span data-ttu-id="87487-874">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-875">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-875"></span></span>|
|<span data-ttu-id="87487-876">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-877">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-877"></span></span>|
|<span data-ttu-id="87487-878">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-879">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-879"></span></span>|
|<span data-ttu-id="87487-880">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-881">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-881"></span></span>|
|<span data-ttu-id="87487-882">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-882">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-883">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-883"></span></span>|
   
 <span data-ttu-id="87487-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="87487-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-885">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-885">**Subject**</span></span>|
|<span data-ttu-id="87487-886">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-886"></span></span>|
|<span data-ttu-id="87487-887">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-887">**Issuer**</span></span>|
|<span data-ttu-id="87487-888">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-888"></span></span>|
|<span data-ttu-id="87487-889">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-889">**Serial Number**</span></span>|
|<span data-ttu-id="87487-890">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-890"></span></span>|
|<span data-ttu-id="87487-891">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-891">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-892">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-892"></span></span>|
|<span data-ttu-id="87487-893">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-894">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-894"></span></span>|
|<span data-ttu-id="87487-895">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-896">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-896"></span></span>|
|<span data-ttu-id="87487-897">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-897">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-898">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-898"></span></span>|
|<span data-ttu-id="87487-899">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-900">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-900"></span></span>|
|<span data-ttu-id="87487-901">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-902">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-902"></span></span>|
|<span data-ttu-id="87487-903">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-904">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-904"></span></span>|
|<span data-ttu-id="87487-905">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-906">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-906"></span></span>|
|<span data-ttu-id="87487-907">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-908">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-908"></span></span>|
|<span data-ttu-id="87487-909">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-909">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-910">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-910"></span></span>|
|<span data-ttu-id="87487-911">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-912">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-912"></span></span>|
   
 <span data-ttu-id="87487-913">**Microsoft IT TLS CA 1**</span><span class="sxs-lookup"><span data-stu-id="87487-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-914">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-914">**Subject**</span></span>|
|<span data-ttu-id="87487-915">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-915"></span></span>|
|<span data-ttu-id="87487-916">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-916">**Issuer**</span></span>|
|<span data-ttu-id="87487-917">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-917"></span></span>|
|<span data-ttu-id="87487-918">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-918">**Serial Number**</span></span>|
|<span data-ttu-id="87487-919">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-919"></span></span>|
|<span data-ttu-id="87487-920">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-920">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-921">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-921"></span></span>|
|<span data-ttu-id="87487-922">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-923">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-923"></span></span>|
|<span data-ttu-id="87487-924">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-925">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-925"></span></span>|
|<span data-ttu-id="87487-926">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-926">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-927">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-927"></span></span>|
|<span data-ttu-id="87487-928">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-929">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-929"></span></span>|
|<span data-ttu-id="87487-930">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-931">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-931"></span></span>|
|<span data-ttu-id="87487-932">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-933">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-933"></span></span>|
|<span data-ttu-id="87487-934">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-935">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-935"></span></span>|
|<span data-ttu-id="87487-936">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-937">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-937"></span></span>|
|<span data-ttu-id="87487-938">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-938">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-939">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-939"></span></span>|
|<span data-ttu-id="87487-940">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-941">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-941"></span></span>|
   
 <span data-ttu-id="87487-942">**Microsoft IT TLS CA 2**</span><span class="sxs-lookup"><span data-stu-id="87487-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-943">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-943">**Subject**</span></span>|
|<span data-ttu-id="87487-944">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-944"></span></span>|
|<span data-ttu-id="87487-945">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-945">**Issuer**</span></span>|
|<span data-ttu-id="87487-946">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-946"></span></span>|
|<span data-ttu-id="87487-947">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-947">**Serial Number**</span></span>|
|<span data-ttu-id="87487-948">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-948"></span></span>|
|<span data-ttu-id="87487-949">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-949">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-950">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-950"></span></span>|
|<span data-ttu-id="87487-951">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-952">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-952"></span></span>|
|<span data-ttu-id="87487-953">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-954">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-954"></span></span>|
|<span data-ttu-id="87487-955">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-955">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-956">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-956"></span></span>|
|<span data-ttu-id="87487-957">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-958">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-958"></span></span>|
|<span data-ttu-id="87487-959">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-960">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-960"></span></span>|
|<span data-ttu-id="87487-961">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-962">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-962"></span></span>|
|<span data-ttu-id="87487-963">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-964">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-964"></span></span>|
|<span data-ttu-id="87487-965">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-966">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-966"></span></span>|
|<span data-ttu-id="87487-967">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-967">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-968">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-968"></span></span>|
|<span data-ttu-id="87487-969">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-970">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-970"></span></span>|
   
 <span data-ttu-id="87487-971">**Microsoft IT TLS CA 4**</span><span class="sxs-lookup"><span data-stu-id="87487-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-972">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-972">**Subject**</span></span>|
|<span data-ttu-id="87487-973">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-973"></span></span>|
|<span data-ttu-id="87487-974">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-974">**Issuer**</span></span>|
|<span data-ttu-id="87487-975">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-975"></span></span>|
|<span data-ttu-id="87487-976">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-976">**Serial Number**</span></span>|
|<span data-ttu-id="87487-977">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-977"></span></span>|
|<span data-ttu-id="87487-978">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-978">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-979">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-979"></span></span>|
|<span data-ttu-id="87487-980">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-981">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-981"></span></span>|
|<span data-ttu-id="87487-982">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-983">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-983"></span></span>|
|<span data-ttu-id="87487-984">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-984">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-985">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-985"></span></span>|
|<span data-ttu-id="87487-986">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-987">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-987"></span></span>|
|<span data-ttu-id="87487-988">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-989">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-989"></span></span>|
|<span data-ttu-id="87487-990">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-991">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-991"></span></span>|
|<span data-ttu-id="87487-992">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-993">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-993"></span></span>|
|<span data-ttu-id="87487-994">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-995">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-995"></span></span>|
|<span data-ttu-id="87487-996">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-996">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-997">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-997"></span></span>|
|<span data-ttu-id="87487-998">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-999">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-999"></span></span>|
   
 <span data-ttu-id="87487-1000">**Microsoft IT TLS CA 5**</span><span class="sxs-lookup"><span data-stu-id="87487-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-1001">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-1001">**Subject**</span></span>|
|<span data-ttu-id="87487-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1002"></span></span>|
|<span data-ttu-id="87487-1003">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-1003">**Issuer**</span></span>|
|<span data-ttu-id="87487-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1004"></span></span>|
|<span data-ttu-id="87487-1005">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-1005">**Serial Number**</span></span>|
|<span data-ttu-id="87487-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1006"></span></span>|
|<span data-ttu-id="87487-1007">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1008"></span></span>|
|<span data-ttu-id="87487-1009">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1010"></span></span>|
|<span data-ttu-id="87487-1011">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1012"></span></span>|
|<span data-ttu-id="87487-1013">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1014"></span></span>|
|<span data-ttu-id="87487-1015">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1016"></span></span>|
|<span data-ttu-id="87487-1017">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1018"></span></span>|
|<span data-ttu-id="87487-1019">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1020"></span></span>|
|<span data-ttu-id="87487-1021">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1022"></span></span>|
|<span data-ttu-id="87487-1023">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1024"></span></span>|
|<span data-ttu-id="87487-1025">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1026"></span></span>|
|<span data-ttu-id="87487-1027">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1028"></span></span>|
   
 <span data-ttu-id="87487-1029">**Symantec 클래스 3 EV SSL CA-G3**</span><span class="sxs-lookup"><span data-stu-id="87487-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-1030">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-1030">**Subject**</span></span>|
|<span data-ttu-id="87487-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1031"></span></span>|
|<span data-ttu-id="87487-1032">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-1032">**Issuer**</span></span>|
|<span data-ttu-id="87487-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1033"></span></span>|
|<span data-ttu-id="87487-1034">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="87487-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="87487-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1035"></span></span>|
|<span data-ttu-id="87487-1036">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-1036">**Serial Number**</span></span>|
|<span data-ttu-id="87487-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1037"></span></span>|
|<span data-ttu-id="87487-1038">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1039"></span></span>|
|<span data-ttu-id="87487-1040">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1041"></span></span>|
|<span data-ttu-id="87487-1042">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1043"></span></span>|
|<span data-ttu-id="87487-1044">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1045"></span></span>|
|<span data-ttu-id="87487-1046">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1047"></span></span>|
|<span data-ttu-id="87487-1048">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1049"></span></span>|
|<span data-ttu-id="87487-1050">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1051"></span></span>|
|<span data-ttu-id="87487-1052">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1053"></span></span>|
|<span data-ttu-id="87487-1054">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1055"></span></span>|
|<span data-ttu-id="87487-1056">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1057"></span></span>|
|<span data-ttu-id="87487-1058">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1059"></span></span>|
   
 <span data-ttu-id="87487-1060">**Symantec 클래스 3 안전한 서버 CA-G4**</span><span class="sxs-lookup"><span data-stu-id="87487-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-1061">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-1061">**Subject**</span></span>|
|<span data-ttu-id="87487-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1062"></span></span>|
|<span data-ttu-id="87487-1063">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-1063">**Issuer**</span></span>|
|<span data-ttu-id="87487-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1064"></span></span>|
|<span data-ttu-id="87487-1065">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="87487-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="87487-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1066"></span></span>|
|<span data-ttu-id="87487-1067">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-1067">**Serial Number**</span></span>|
|<span data-ttu-id="87487-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1068"></span></span>|
|<span data-ttu-id="87487-1069">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1070"></span></span>|
|<span data-ttu-id="87487-1071">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1072"></span></span>|
|<span data-ttu-id="87487-1073">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1074"></span></span>|
|<span data-ttu-id="87487-1075">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1076"></span></span>|
|<span data-ttu-id="87487-1077">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1078"></span></span>|
|<span data-ttu-id="87487-1079">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1080"></span></span>|
|<span data-ttu-id="87487-1081">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1082"></span></span>|
|<span data-ttu-id="87487-1083">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1084"></span></span>|
|<span data-ttu-id="87487-1085">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1086"></span></span>|
|<span data-ttu-id="87487-1087">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1088"></span></span>|
|<span data-ttu-id="87487-1089">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1090"></span></span>|
   
 <span data-ttu-id="87487-1091">**thawte SHA256 SSL CA**</span><span class="sxs-lookup"><span data-stu-id="87487-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-1092">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-1092">**Subject**</span></span>|
|<span data-ttu-id="87487-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1093"></span></span>|
|<span data-ttu-id="87487-1094">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-1094">**Issuer**</span></span>|
|<span data-ttu-id="87487-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1095"></span></span>|
|<span data-ttu-id="87487-1096">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="87487-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="87487-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1097"></span></span>|
|<span data-ttu-id="87487-1098">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-1098">**Serial Number**</span></span>|
|<span data-ttu-id="87487-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1099"></span></span>|
|<span data-ttu-id="87487-1100">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1101"></span></span>|
|<span data-ttu-id="87487-1102">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1103"></span></span>|
|<span data-ttu-id="87487-1104">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1105"></span></span>|
|<span data-ttu-id="87487-1106">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1107"></span></span>|
|<span data-ttu-id="87487-1108">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1109"></span></span>|
|<span data-ttu-id="87487-1110">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1111"></span></span>|
|<span data-ttu-id="87487-1112">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1113"></span></span>|
|<span data-ttu-id="87487-1114">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1115"></span></span>|
|<span data-ttu-id="87487-1116">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1117"></span></span>|
|<span data-ttu-id="87487-1118">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1119"></span></span>|
|<span data-ttu-id="87487-1120">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1121"></span></span>|
   
 <span data-ttu-id="87487-1122">**Verizon Akamai SureServer CA g 14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="87487-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="87487-1123">**제목**</span><span class="sxs-lookup"><span data-stu-id="87487-1123">**Subject**</span></span>|
|<span data-ttu-id="87487-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1124"></span></span>|
|<span data-ttu-id="87487-1125">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="87487-1125">**Issuer**</span></span>|
|<span data-ttu-id="87487-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1126"></span></span>|
|<span data-ttu-id="87487-1127">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="87487-1127">**Serial Number**</span></span>|
|<span data-ttu-id="87487-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1128"></span></span>|
|<span data-ttu-id="87487-1129">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="87487-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="87487-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1130"></span></span>|
|<span data-ttu-id="87487-1131">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="87487-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="87487-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1132"></span></span>|
|<span data-ttu-id="87487-1133">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="87487-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="87487-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1134"></span></span>|
|<span data-ttu-id="87487-1135">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="87487-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="87487-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1136"></span></span>|
|<span data-ttu-id="87487-1137">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="87487-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1138"></span></span>|
|<span data-ttu-id="87487-1139">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="87487-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="87487-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1140"></span></span>|
|<span data-ttu-id="87487-1141">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="87487-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="87487-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1142"></span></span>|
|<span data-ttu-id="87487-1143">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1144"></span></span>|
|<span data-ttu-id="87487-1145">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="87487-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="87487-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1146"></span></span>|
|<span data-ttu-id="87487-1147">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="87487-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1148"></span></span>|
|<span data-ttu-id="87487-1149">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="87487-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1150"></span></span>|
|<span data-ttu-id="87487-1151">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="87487-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="87487-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="87487-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="87487-1153">추가 인증서 경로</span><span class="sxs-lookup"><span data-stu-id="87487-1153">Additional certificate paths</span></span>
<span data-ttu-id="87487-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="87487-1154"></span></span>

<span data-ttu-id="87487-1155">다음은 위에 포함 되지 않은 시간에 따른 위의 목록을 사용 하 여 병합 될 하 레거시 인증서를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="87487-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


