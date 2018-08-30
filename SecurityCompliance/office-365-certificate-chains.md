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
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533381"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="56413-106">Office 365 인증서 체인</span><span class="sxs-lookup"><span data-stu-id="56413-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="56413-p102">Office 365 기술을 활용 하는 다른 인증서 공급자의 수입니다. 다음은 고객이 Office 365에 액세스할 때 발생할 수 있는 알려진된 Office 365 루트 인증서의 전체 목록에 대 한 설명입니다. 직접 인프라에 설치 해야할 수 인증서는 정보를 [Office 365 용 타사 SSL 인증서에 대 한 계획을](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce)참조 합니다. 다음 인증서 정보는 Office 365의 모든 전세계 및 국가 클라우드 인스턴스에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56413-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="56413-111">**인증서 유형**</span><span class="sxs-lookup"><span data-stu-id="56413-111">**Certificate type**</span></span>|<span data-ttu-id="56413-112">**여.p7b 다운로드**</span><span class="sxs-lookup"><span data-stu-id="56413-112">**P7b download**</span></span>|<span data-ttu-id="56413-113">**CRL 끝점**</span><span class="sxs-lookup"><span data-stu-id="56413-113">**CRL Endpoints**</span></span>|<span data-ttu-id="56413-114">**OCSP 끝점**</span><span class="sxs-lookup"><span data-stu-id="56413-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="56413-115">**AIA 끝점**</span><span class="sxs-lookup"><span data-stu-id="56413-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="56413-116">공개적으로 신뢰할 수 있는 루트 인증서</span><span class="sxs-lookup"><span data-stu-id="56413-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="56413-117">Office 365 루트 인증서 번들 (여.p7b)</span><span class="sxs-lookup"><span data-stu-id="56413-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="56413-118">crl.globalsign.net</span><span class="sxs-lookup"><span data-stu-id="56413-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="56413-119">www.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="56413-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="56413-120">해당 없음</span><span class="sxs-lookup"><span data-stu-id="56413-120">N/A</span></span>  <br/> |<span data-ttu-id="56413-121">해당 없음</span><span class="sxs-lookup"><span data-stu-id="56413-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="56413-122">공개적으로 신뢰할 수 있는 중간 인증서</span><span class="sxs-lookup"><span data-stu-id="56413-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="56413-123">Office 365 중간 인증서 번들 (여.p7b)</span><span class="sxs-lookup"><span data-stu-id="56413-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="56413-124">cdp1.public trust.com</span><span class="sxs-lookup"><span data-stu-id="56413-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="56413-125">crl.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="56413-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="56413-126">crl.entrust.net</span><span class="sxs-lookup"><span data-stu-id="56413-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="56413-127">crl.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="56413-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="56413-128">crl.globalsign.net</span><span class="sxs-lookup"><span data-stu-id="56413-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="56413-129">crl.identrust.com</span><span class="sxs-lookup"><span data-stu-id="56413-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="56413-130">crl.thawte.com</span><span class="sxs-lookup"><span data-stu-id="56413-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="56413-131">crl3.digicert.com</span><span class="sxs-lookup"><span data-stu-id="56413-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="56413-132">crl4.digicert.com</span><span class="sxs-lookup"><span data-stu-id="56413-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="56413-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="56413-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="56413-134">www.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="56413-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="56413-135">isrg.trustid.ocsp.identrust.com</span><span class="sxs-lookup"><span data-stu-id="56413-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="56413-136">ocsp.digicert.com</span><span class="sxs-lookup"><span data-stu-id="56413-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="56413-137">ocsp.entrust.net</span><span class="sxs-lookup"><span data-stu-id="56413-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="56413-138">ocsp.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="56413-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="56413-139">ocsp.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="56413-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="56413-140">ocsp.startssl.com</span><span class="sxs-lookup"><span data-stu-id="56413-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="56413-141">ocsp.thawte.com</span><span class="sxs-lookup"><span data-stu-id="56413-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="56413-142">ocsp2.globalsign.com</span><span class="sxs-lookup"><span data-stu-id="56413-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="56413-143">ocspcnnicroot.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="56413-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="56413-144">루트-c3-c a 2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="56413-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="56413-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="56413-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="56413-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="56413-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="56413-147">aia.startssl.com</span><span class="sxs-lookup"><span data-stu-id="56413-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="56413-148">apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="56413-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="56413-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="56413-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="56413-150">www.cnnic.cn</span><span class="sxs-lookup"><span data-stu-id="56413-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="56413-151">루트 및 인증서 공급자에 대 한 추가 세부 정보를 보려면 아래 중간 섹션을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="56413-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="56413-152">Office 365 루트 인증서 세부 정보</span><span class="sxs-lookup"><span data-stu-id="56413-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="56413-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="56413-153"></span></span>

 <span data-ttu-id="56413-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="56413-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="56413-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="56413-155">|:-----|</span></span>
|<span data-ttu-id="56413-156">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="56413-157">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-157">**Serial Number**</span></span>|
|<span data-ttu-id="56413-158">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-158"></span></span>|
|<span data-ttu-id="56413-159">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-159">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-160">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-160"></span></span>|
|<span data-ttu-id="56413-161">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-162">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-162"></span></span>|
|<span data-ttu-id="56413-163">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-164">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-164"></span></span>|
|<span data-ttu-id="56413-165">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-165">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-166">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-166"></span></span>|
|<span data-ttu-id="56413-167">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-168">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-168"></span></span>|
|<span data-ttu-id="56413-169">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-170">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-170"></span></span>|
|<span data-ttu-id="56413-171">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-172">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-172"></span></span>|
|<span data-ttu-id="56413-173">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-174">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-174"></span></span>|
   
 <span data-ttu-id="56413-175">**CNNIC 루트**</span><span class="sxs-lookup"><span data-stu-id="56413-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-176">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-176">**Subject**</span></span>|
|<span data-ttu-id="56413-177">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-177"></span></span>|
|<span data-ttu-id="56413-178">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-178">**Serial Number**</span></span>|
|<span data-ttu-id="56413-179">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-179"></span></span>|
|<span data-ttu-id="56413-180">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-180">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-181">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-181"></span></span>|
|<span data-ttu-id="56413-182">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-183">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-183"></span></span>|
|<span data-ttu-id="56413-184">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-185">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-185"></span></span>|
|<span data-ttu-id="56413-186">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-186">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-187">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-187"></span></span>|
|<span data-ttu-id="56413-188">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-189">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-189"></span></span>|
|<span data-ttu-id="56413-190">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-191">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-191"></span></span>|
|<span data-ttu-id="56413-192">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-193">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-193"></span></span>|
|<span data-ttu-id="56413-194">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-195">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-195"></span></span>|
|<span data-ttu-id="56413-196">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-197">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-197"></span></span>|
   
 <span data-ttu-id="56413-198">**DigiCert 전역 루트 CA**</span><span class="sxs-lookup"><span data-stu-id="56413-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-199">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-199">**Subject**</span></span>|
|<span data-ttu-id="56413-200">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-200"></span></span>|
|<span data-ttu-id="56413-201">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-201">**Serial Number**</span></span>|
|<span data-ttu-id="56413-202">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-202"></span></span>|
|<span data-ttu-id="56413-203">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-203">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-204">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-204"></span></span>|
|<span data-ttu-id="56413-205">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-206">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-206"></span></span>|
|<span data-ttu-id="56413-207">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-208">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-208"></span></span>|
|<span data-ttu-id="56413-209">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-209">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-210">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-210"></span></span>|
|<span data-ttu-id="56413-211">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-212">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-212"></span></span>|
|<span data-ttu-id="56413-213">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-214">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-214"></span></span>|
|<span data-ttu-id="56413-215">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-216">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-216"></span></span>|
|<span data-ttu-id="56413-217">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-218">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-218"></span></span>|
|<span data-ttu-id="56413-219">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-220">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-220"></span></span>|
   
 <span data-ttu-id="56413-221">**DigiCert 높은 보증 EV 루트 CA**</span><span class="sxs-lookup"><span data-stu-id="56413-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-222">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-222">**Subject**</span></span>|
|<span data-ttu-id="56413-223">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-223"></span></span>|
|<span data-ttu-id="56413-224">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-224">**Serial Number**</span></span>|
|<span data-ttu-id="56413-225">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-225"></span></span>|
|<span data-ttu-id="56413-226">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-226">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-227">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-227"></span></span>|
|<span data-ttu-id="56413-228">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-229">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-229"></span></span>|
|<span data-ttu-id="56413-230">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-231">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-231"></span></span>|
|<span data-ttu-id="56413-232">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-232">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-233">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-233"></span></span>|
|<span data-ttu-id="56413-234">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-235">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-235"></span></span>|
|<span data-ttu-id="56413-236">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-237">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-237"></span></span>|
|<span data-ttu-id="56413-238">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-239">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-239"></span></span>|
|<span data-ttu-id="56413-240">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-241">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-241"></span></span>|
|<span data-ttu-id="56413-242">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-243">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-243"></span></span>|
   
 <span data-ttu-id="56413-244">**D-신뢰 루트 클래스 3 CA 2 2009**</span><span class="sxs-lookup"><span data-stu-id="56413-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-245">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-245">**Subject**</span></span>|
|<span data-ttu-id="56413-246">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-246"></span></span>|
|<span data-ttu-id="56413-247">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-247">**Serial Number**</span></span>|
|<span data-ttu-id="56413-248">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-248"></span></span>|
|<span data-ttu-id="56413-249">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-249">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-250">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-250"></span></span>|
|<span data-ttu-id="56413-251">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-252">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-252"></span></span>|
|<span data-ttu-id="56413-253">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-254">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-254"></span></span>|
|<span data-ttu-id="56413-255">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-255">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-256">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-256"></span></span>|
|<span data-ttu-id="56413-257">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-258">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-258"></span></span>|
|<span data-ttu-id="56413-259">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-260">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-260"></span></span>|
|<span data-ttu-id="56413-261">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-262">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-262"></span></span>|
|<span data-ttu-id="56413-263">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-264">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-264"></span></span>|
|<span data-ttu-id="56413-265">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-265">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-266">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-266"></span></span>|
   
 <span data-ttu-id="56413-267">**D-신뢰 루트 클래스 3 CA 2 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="56413-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-268">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-268">**Subject**</span></span>|
|<span data-ttu-id="56413-269">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-269"></span></span>|
|<span data-ttu-id="56413-270">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-270">**Serial Number**</span></span>|
|<span data-ttu-id="56413-271">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-271"></span></span>|
|<span data-ttu-id="56413-272">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-272">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-273">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-273"></span></span>|
|<span data-ttu-id="56413-274">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-275">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-275"></span></span>|
|<span data-ttu-id="56413-276">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-277">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-277"></span></span>|
|<span data-ttu-id="56413-278">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-278">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-279">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-279"></span></span>|
|<span data-ttu-id="56413-280">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-281">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-281"></span></span>|
|<span data-ttu-id="56413-282">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-283">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-283"></span></span>|
|<span data-ttu-id="56413-284">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-285">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-285"></span></span>|
|<span data-ttu-id="56413-286">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-287">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-287"></span></span>|
|<span data-ttu-id="56413-288">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-288">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-289">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-289"></span></span>|
   
 <span data-ttu-id="56413-290">**DST 루트 CA X3**</span><span class="sxs-lookup"><span data-stu-id="56413-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-291">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-291">**Subject**</span></span>|
|<span data-ttu-id="56413-292">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-292"></span></span>|
|<span data-ttu-id="56413-293">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-293">**Serial Number**</span></span>|
|<span data-ttu-id="56413-294">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-294"></span></span>|
|<span data-ttu-id="56413-295">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-295">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-296">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-296"></span></span>|
|<span data-ttu-id="56413-297">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-298">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-298"></span></span>|
|<span data-ttu-id="56413-299">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-300">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-300"></span></span>|
|<span data-ttu-id="56413-301">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-301">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-302">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-302"></span></span>|
|<span data-ttu-id="56413-303">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-304">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-304"></span></span>|
|<span data-ttu-id="56413-305">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-306">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-306"></span></span>|
|<span data-ttu-id="56413-307">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-308">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-308"></span></span>|
|<span data-ttu-id="56413-309">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-310">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-310"></span></span>|
   
 <span data-ttu-id="56413-311">**루트 인증 기관-G2 맡길**</span><span class="sxs-lookup"><span data-stu-id="56413-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-312">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-312">**Subject**</span></span>|
|<span data-ttu-id="56413-313">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-313"></span></span>|
|<span data-ttu-id="56413-314">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-314">**Serial Number**</span></span>|
|<span data-ttu-id="56413-315">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-315"></span></span>|
|<span data-ttu-id="56413-316">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-316">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-317">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-317"></span></span>|
|<span data-ttu-id="56413-318">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-319">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-319"></span></span>|
|<span data-ttu-id="56413-320">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-321">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-321"></span></span>|
|<span data-ttu-id="56413-322">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-322">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-323">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-323"></span></span>|
|<span data-ttu-id="56413-324">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-325">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-325"></span></span>|
|<span data-ttu-id="56413-326">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-327">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-327"></span></span>|
|<span data-ttu-id="56413-328">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-329">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-329"></span></span>|
|<span data-ttu-id="56413-330">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-331">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-331"></span></span>|
   
 <span data-ttu-id="56413-332">**Entrust.net Certification Authority (2048)**</span><span class="sxs-lookup"><span data-stu-id="56413-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-333">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-333">**Subject**</span></span>|
|<span data-ttu-id="56413-334">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-334"></span></span>|
|<span data-ttu-id="56413-335">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-335">**Serial Number**</span></span>|
|<span data-ttu-id="56413-336">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-336"></span></span>|
|<span data-ttu-id="56413-337">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-337">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-338">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-338"></span></span>|
|<span data-ttu-id="56413-339">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-340">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-340"></span></span>|
|<span data-ttu-id="56413-341">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-342">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-342"></span></span>|
|<span data-ttu-id="56413-343">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-343">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-344">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-344"></span></span>|
|<span data-ttu-id="56413-345">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-346">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-346"></span></span>|
|<span data-ttu-id="56413-347">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-348">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-348"></span></span>|
|<span data-ttu-id="56413-349">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-350">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-350"></span></span>|
|<span data-ttu-id="56413-351">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-352">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-352"></span></span>|
   
 <span data-ttu-id="56413-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="56413-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-354">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-354">**Subject**</span></span>|
|<span data-ttu-id="56413-355">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-355"></span></span>|
|<span data-ttu-id="56413-356">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-356">**Serial Number**</span></span>|
|<span data-ttu-id="56413-357">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-357"></span></span>|
|<span data-ttu-id="56413-358">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-358">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-359">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-359"></span></span>|
|<span data-ttu-id="56413-360">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-361">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-361"></span></span>|
|<span data-ttu-id="56413-362">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-363">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-363"></span></span>|
|<span data-ttu-id="56413-364">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-364">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-365">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-365"></span></span>|
|<span data-ttu-id="56413-366">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-367">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-367"></span></span>|
|<span data-ttu-id="56413-368">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-369">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-369"></span></span>|
|<span data-ttu-id="56413-370">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-371">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-371"></span></span>|
|<span data-ttu-id="56413-372">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-373">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-373"></span></span>|
|<span data-ttu-id="56413-374">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-375">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-375"></span></span>|
|<span data-ttu-id="56413-376">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-376">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-377">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-377"></span></span>|
   
 <span data-ttu-id="56413-378">**GlobalSign Root CA**</span><span class="sxs-lookup"><span data-stu-id="56413-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-379">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-379">**Subject**</span></span>|
|<span data-ttu-id="56413-380">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-380"></span></span>|
|<span data-ttu-id="56413-381">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-381">**Serial Number**</span></span>|
|<span data-ttu-id="56413-382">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-382"></span></span>|
|<span data-ttu-id="56413-383">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-383">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-384">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-384"></span></span>|
|<span data-ttu-id="56413-385">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-386">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-386"></span></span>|
|<span data-ttu-id="56413-387">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-388">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-388"></span></span>|
|<span data-ttu-id="56413-389">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-389">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-390">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-390"></span></span>|
|<span data-ttu-id="56413-391">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-392">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-392"></span></span>|
|<span data-ttu-id="56413-393">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-394">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-394"></span></span>|
|<span data-ttu-id="56413-395">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-396">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-396"></span></span>|
|<span data-ttu-id="56413-397">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-398">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-398"></span></span>|
   
 <span data-ttu-id="56413-399">**thawte 기본 루트 CA-G3**</span><span class="sxs-lookup"><span data-stu-id="56413-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-400">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-400">**Subject**</span></span>|
|<span data-ttu-id="56413-401">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-401"></span></span>|
|<span data-ttu-id="56413-402">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-402">**Serial Number**</span></span>|
|<span data-ttu-id="56413-403">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-403"></span></span>|
|<span data-ttu-id="56413-404">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-404">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-405">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-405"></span></span>|
|<span data-ttu-id="56413-406">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-407">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-407"></span></span>|
|<span data-ttu-id="56413-408">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-409">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-409"></span></span>|
|<span data-ttu-id="56413-410">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-410">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-411">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-411"></span></span>|
|<span data-ttu-id="56413-412">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-413">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-413"></span></span>|
|<span data-ttu-id="56413-414">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-415">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-415"></span></span>|
|<span data-ttu-id="56413-416">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-417">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-417"></span></span>|
|<span data-ttu-id="56413-418">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-419">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-419"></span></span>|
   
 <span data-ttu-id="56413-420">**VeriSign 클래스 3 기본 공용 인증 기관-g 5**</span><span class="sxs-lookup"><span data-stu-id="56413-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-421">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-421">**Subject**</span></span>|
|<span data-ttu-id="56413-422">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-422"></span></span>|
|<span data-ttu-id="56413-423">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-423">**Serial Number**</span></span>|
|<span data-ttu-id="56413-424">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-424"></span></span>|
|<span data-ttu-id="56413-425">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-425">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-426">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-426"></span></span>|
|<span data-ttu-id="56413-427">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-428">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-428"></span></span>|
|<span data-ttu-id="56413-429">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-430">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-430"></span></span>|
|<span data-ttu-id="56413-431">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-431">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-432">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-432"></span></span>|
|<span data-ttu-id="56413-433">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-434">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-434"></span></span>|
|<span data-ttu-id="56413-435">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-436">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-436"></span></span>|
|<span data-ttu-id="56413-437">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-438">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-438"></span></span>|
|<span data-ttu-id="56413-439">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-440">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="56413-441">Office 365 중간 인증서 세부 정보</span><span class="sxs-lookup"><span data-stu-id="56413-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="56413-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="56413-442"></span></span>

 <span data-ttu-id="56413-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="56413-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-444">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-444">**Subject**</span></span>|
|<span data-ttu-id="56413-445">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-445"></span></span>|
|<span data-ttu-id="56413-446">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-446">**Issuer**</span></span>|
|<span data-ttu-id="56413-447">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-447"></span></span>|
|<span data-ttu-id="56413-448">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-448">**Serial Number**</span></span>|
|<span data-ttu-id="56413-449">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-449"></span></span>|
|<span data-ttu-id="56413-450">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-450">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-451">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-451"></span></span>|
|<span data-ttu-id="56413-452">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-453">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-453"></span></span>|
|<span data-ttu-id="56413-454">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-455">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-455"></span></span>|
|<span data-ttu-id="56413-456">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-456">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-457">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-457"></span></span>|
|<span data-ttu-id="56413-458">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-459">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-459"></span></span>|
|<span data-ttu-id="56413-460">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-461">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-461"></span></span>|
|<span data-ttu-id="56413-462">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-463">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-463"></span></span>|
|<span data-ttu-id="56413-464">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-465">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-465"></span></span>|
|<span data-ttu-id="56413-466">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-467">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-467"></span></span>|
|<span data-ttu-id="56413-468">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="56413-468">**AIA URLs**</span></span>|
|<span data-ttu-id="56413-469">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-469"></span></span>|
|<span data-ttu-id="56413-470">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-470">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-471">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-471"></span></span>|
|<span data-ttu-id="56413-472">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-473">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-473"></span></span>|
   
 <span data-ttu-id="56413-474">**D-신뢰 SSL 클래스 3 CA 1 2009**</span><span class="sxs-lookup"><span data-stu-id="56413-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-475">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-475">**Subject**</span></span>|
|<span data-ttu-id="56413-476">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-476"></span></span>|
|<span data-ttu-id="56413-477">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-477">**Issuer**</span></span>|
|<span data-ttu-id="56413-478">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-478"></span></span>|
|<span data-ttu-id="56413-479">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="56413-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="56413-480">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-480"></span></span>|
|<span data-ttu-id="56413-481">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-481">**Serial Number**</span></span>|
|<span data-ttu-id="56413-482">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-482"></span></span>|
|<span data-ttu-id="56413-483">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-483">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-484">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-484"></span></span>|
|<span data-ttu-id="56413-485">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-486">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-486"></span></span>|
|<span data-ttu-id="56413-487">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-488">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-488"></span></span>|
|<span data-ttu-id="56413-489">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-489">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-490">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-490"></span></span>|
|<span data-ttu-id="56413-491">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-492">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-492"></span></span>|
|<span data-ttu-id="56413-493">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-494">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-494"></span></span>|
|<span data-ttu-id="56413-495">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-496">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-496"></span></span>|
|<span data-ttu-id="56413-497">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-498">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-498"></span></span>|
|<span data-ttu-id="56413-499">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-500">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-500"></span></span>|
|<span data-ttu-id="56413-501">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-501">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-502">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-502"></span></span>|
|<span data-ttu-id="56413-503">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-504">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-504"></span></span>|
   
 <span data-ttu-id="56413-505">**D-신뢰 SSL 클래스 3 CA 1 EV 2009**</span><span class="sxs-lookup"><span data-stu-id="56413-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-506">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-506">**Subject**</span></span>|
|<span data-ttu-id="56413-507">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-507"></span></span>|
|<span data-ttu-id="56413-508">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-508">**Issuer**</span></span>|
|<span data-ttu-id="56413-509">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-509"></span></span>|
|<span data-ttu-id="56413-510">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="56413-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="56413-511">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-511"></span></span>|
|<span data-ttu-id="56413-512">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-512">**Serial Number**</span></span>|
|<span data-ttu-id="56413-513">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-513"></span></span>|
|<span data-ttu-id="56413-514">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-514">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-515">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-515"></span></span>|
|<span data-ttu-id="56413-516">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-517">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-517"></span></span>|
|<span data-ttu-id="56413-518">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-519">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-519"></span></span>|
|<span data-ttu-id="56413-520">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-520">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-521">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-521"></span></span>|
|<span data-ttu-id="56413-522">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-523">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-523"></span></span>|
|<span data-ttu-id="56413-524">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-525">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-525"></span></span>|
|<span data-ttu-id="56413-526">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-527">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-527"></span></span>|
|<span data-ttu-id="56413-528">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-529">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-529"></span></span>|
|<span data-ttu-id="56413-530">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-531">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-531"></span></span>|
|<span data-ttu-id="56413-532">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-532">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-533">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-533"></span></span>|
|<span data-ttu-id="56413-534">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-535">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-535"></span></span>|
   
 <span data-ttu-id="56413-536">**DigiCert 클라우드 서비스 CA-1**</span><span class="sxs-lookup"><span data-stu-id="56413-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-537">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-537">**Subject**</span></span>|
|<span data-ttu-id="56413-538">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-538"></span></span>|
|<span data-ttu-id="56413-539">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-539">**Issuer**</span></span>|
|<span data-ttu-id="56413-540">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-540"></span></span>|
|<span data-ttu-id="56413-541">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-541">**Serial Number**</span></span>|
|<span data-ttu-id="56413-542">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-542"></span></span>|
|<span data-ttu-id="56413-543">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-543">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-544">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-544"></span></span>|
|<span data-ttu-id="56413-545">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-546">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-546"></span></span>|
|<span data-ttu-id="56413-547">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-548">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-548"></span></span>|
|<span data-ttu-id="56413-549">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-549">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-550">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-550"></span></span>|
|<span data-ttu-id="56413-551">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-552">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-552"></span></span>|
|<span data-ttu-id="56413-553">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-554">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-554"></span></span>|
|<span data-ttu-id="56413-555">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-556">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-556"></span></span>|
|<span data-ttu-id="56413-557">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-558">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-558"></span></span>|
|<span data-ttu-id="56413-559">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-560">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-560"></span></span>|
|<span data-ttu-id="56413-561">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-561">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-562">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-562"></span></span>|
|<span data-ttu-id="56413-563">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-564">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-564"></span></span>|
   
 <span data-ttu-id="56413-565">**DigiCert SHA2 높은 보증 서버 CA**</span><span class="sxs-lookup"><span data-stu-id="56413-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-566">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-566">**Subject**</span></span>|
|<span data-ttu-id="56413-567">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-567"></span></span>|
|<span data-ttu-id="56413-568">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-568">**Issuer**</span></span>|
|<span data-ttu-id="56413-569">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-569"></span></span>|
|<span data-ttu-id="56413-570">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-570">**Serial Number**</span></span>|
|<span data-ttu-id="56413-571">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-571"></span></span>|
|<span data-ttu-id="56413-572">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-572">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-573">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-573"></span></span>|
|<span data-ttu-id="56413-574">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-575">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-575"></span></span>|
|<span data-ttu-id="56413-576">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-577">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-577"></span></span>|
|<span data-ttu-id="56413-578">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-578">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-579">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-579"></span></span>|
|<span data-ttu-id="56413-580">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-581">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-581"></span></span>|
|<span data-ttu-id="56413-582">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-583">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-583"></span></span>|
|<span data-ttu-id="56413-584">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-585">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-585"></span></span>|
|<span data-ttu-id="56413-586">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-587">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-587"></span></span>|
|<span data-ttu-id="56413-588">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-589">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-589"></span></span>|
|<span data-ttu-id="56413-590">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-590">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-591">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-591"></span></span>|
|<span data-ttu-id="56413-592">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-593">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-593"></span></span>|
   
 <span data-ttu-id="56413-594">**DigiCert SHA2 안전한 서버 CA**</span><span class="sxs-lookup"><span data-stu-id="56413-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-595">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-595">**Subject**</span></span>|
|<span data-ttu-id="56413-596">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-596"></span></span>|
|<span data-ttu-id="56413-597">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-597">**Issuer**</span></span>|
|<span data-ttu-id="56413-598">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-598"></span></span>|
|<span data-ttu-id="56413-599">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-599">**Serial Number**</span></span>|
|<span data-ttu-id="56413-600">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-600"></span></span>|
|<span data-ttu-id="56413-601">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-601">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-602">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-602"></span></span>|
|<span data-ttu-id="56413-603">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-604">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-604"></span></span>|
|<span data-ttu-id="56413-605">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-606">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-606"></span></span>|
|<span data-ttu-id="56413-607">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-607">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-608">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-608"></span></span>|
|<span data-ttu-id="56413-609">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-610">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-610"></span></span>|
|<span data-ttu-id="56413-611">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-612">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-612"></span></span>|
|<span data-ttu-id="56413-613">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-614">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-614"></span></span>|
|<span data-ttu-id="56413-615">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-616">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-616"></span></span>|
|<span data-ttu-id="56413-617">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-618">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-618"></span></span>|
|<span data-ttu-id="56413-619">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-619">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-620">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-620"></span></span>|
|<span data-ttu-id="56413-621">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-622">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-622"></span></span>|
   
 <span data-ttu-id="56413-623">**인증 기관-L1C 맡길**</span><span class="sxs-lookup"><span data-stu-id="56413-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-624">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-624">**Subject**</span></span>|
|<span data-ttu-id="56413-625">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-625"></span></span>|
|<span data-ttu-id="56413-626">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-626">**Issuer**</span></span>|
|<span data-ttu-id="56413-627">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-627"></span></span>|
|<span data-ttu-id="56413-628">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-628">**Serial Number**</span></span>|
|<span data-ttu-id="56413-629">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-629"></span></span>|
|<span data-ttu-id="56413-630">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-630">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-631">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-631"></span></span>|
|<span data-ttu-id="56413-632">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-633">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-633"></span></span>|
|<span data-ttu-id="56413-634">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-635">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-635"></span></span>|
|<span data-ttu-id="56413-636">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-636">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-637">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-637"></span></span>|
|<span data-ttu-id="56413-638">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-639">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-639"></span></span>|
|<span data-ttu-id="56413-640">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-641">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-641"></span></span>|
|<span data-ttu-id="56413-642">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-643">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-643"></span></span>|
|<span data-ttu-id="56413-644">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-645">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-645"></span></span>|
|<span data-ttu-id="56413-646">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-647">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-647"></span></span>|
|<span data-ttu-id="56413-648">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-648">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-649">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-649"></span></span>|
|<span data-ttu-id="56413-650">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-651">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-651"></span></span>|
   
 <span data-ttu-id="56413-652">**인증 기관-L1K 맡길**</span><span class="sxs-lookup"><span data-stu-id="56413-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-653">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-653">**Subject**</span></span>|
|<span data-ttu-id="56413-654">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-654"></span></span>|
|<span data-ttu-id="56413-655">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-655">**Issuer**</span></span>|
|<span data-ttu-id="56413-656">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-656"></span></span>|
|<span data-ttu-id="56413-657">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-657">**Serial Number**</span></span>|
|<span data-ttu-id="56413-658">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-658"></span></span>|
|<span data-ttu-id="56413-659">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-659">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-660">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-660"></span></span>|
|<span data-ttu-id="56413-661">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-662">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-662"></span></span>|
|<span data-ttu-id="56413-663">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-664">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-664"></span></span>|
|<span data-ttu-id="56413-665">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-665">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-666">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-666"></span></span>|
|<span data-ttu-id="56413-667">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-668">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-668"></span></span>|
|<span data-ttu-id="56413-669">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-670">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-670"></span></span>|
|<span data-ttu-id="56413-671">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-672">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-672"></span></span>|
|<span data-ttu-id="56413-673">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-674">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-674"></span></span>|
|<span data-ttu-id="56413-675">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-676">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-676"></span></span>|
|<span data-ttu-id="56413-677">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-677">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-678">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-678"></span></span>|
|<span data-ttu-id="56413-679">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-680">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-680"></span></span>|
   
 <span data-ttu-id="56413-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="56413-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-682">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-682">**Subject**</span></span>|
|<span data-ttu-id="56413-683">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-683"></span></span>|
|<span data-ttu-id="56413-684">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-684">**Issuer**</span></span>|
|<span data-ttu-id="56413-685">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-685"></span></span>|
|<span data-ttu-id="56413-686">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-686">**Serial Number**</span></span>|
|<span data-ttu-id="56413-687">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-687"></span></span>|
|<span data-ttu-id="56413-688">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-688">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-689">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-689"></span></span>|
|<span data-ttu-id="56413-690">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-691">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-691"></span></span>|
|<span data-ttu-id="56413-692">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-693">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-693"></span></span>|
|<span data-ttu-id="56413-694">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-694">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-695">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-695"></span></span>|
|<span data-ttu-id="56413-696">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-697">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-697"></span></span>|
|<span data-ttu-id="56413-698">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-699">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-699"></span></span>|
|<span data-ttu-id="56413-700">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-701">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-701"></span></span>|
|<span data-ttu-id="56413-702">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-703">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-703"></span></span>|
|<span data-ttu-id="56413-704">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-705">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-705"></span></span>|
|<span data-ttu-id="56413-706">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-706">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-707">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-707"></span></span>|
|<span data-ttu-id="56413-708">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-709">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-709"></span></span>|
   
 <span data-ttu-id="56413-710">**GlobalSign 유효성 검사 CA-SHA256-g 2를 확장 합니다.**</span><span class="sxs-lookup"><span data-stu-id="56413-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-711">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-711">**Subject**</span></span>|
|<span data-ttu-id="56413-712">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-712"></span></span>|
|<span data-ttu-id="56413-713">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-713">**Issuer**</span></span>|
|<span data-ttu-id="56413-714">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-714"></span></span>|
|<span data-ttu-id="56413-715">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-715">**Serial Number**</span></span>|
|<span data-ttu-id="56413-716">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-716"></span></span>|
|<span data-ttu-id="56413-717">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-717">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-718">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-718"></span></span>|
|<span data-ttu-id="56413-719">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-720">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-720"></span></span>|
|<span data-ttu-id="56413-721">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-722">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-722"></span></span>|
|<span data-ttu-id="56413-723">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-723">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-724">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-724"></span></span>|
|<span data-ttu-id="56413-725">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-726">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-726"></span></span>|
|<span data-ttu-id="56413-727">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-728">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-728"></span></span>|
|<span data-ttu-id="56413-729">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-730">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-730"></span></span>|
|<span data-ttu-id="56413-731">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-732">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-732"></span></span>|
|<span data-ttu-id="56413-733">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-734">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-734"></span></span>|
|<span data-ttu-id="56413-735">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-735">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-736">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-736"></span></span>|
|<span data-ttu-id="56413-737">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-738">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-738"></span></span>|
   
 <span data-ttu-id="56413-739">**GlobalSign 유효성 검사-SHA256-CA G3 확장**</span><span class="sxs-lookup"><span data-stu-id="56413-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-740">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-740">**Subject**</span></span>|
|<span data-ttu-id="56413-741">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-741"></span></span>|
|<span data-ttu-id="56413-742">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-742">**Issuer**</span></span>|
|<span data-ttu-id="56413-743">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-743"></span></span>|
|<span data-ttu-id="56413-744">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-744">**Serial Number**</span></span>|
|<span data-ttu-id="56413-745">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-745"></span></span>|
|<span data-ttu-id="56413-746">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-746">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-747">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-747"></span></span>|
|<span data-ttu-id="56413-748">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-749">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-749"></span></span>|
|<span data-ttu-id="56413-750">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-751">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-751"></span></span>|
|<span data-ttu-id="56413-752">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-752">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-753">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-753"></span></span>|
|<span data-ttu-id="56413-754">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-755">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-755"></span></span>|
|<span data-ttu-id="56413-756">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-757">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-757"></span></span>|
|<span data-ttu-id="56413-758">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-759">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-759"></span></span>|
|<span data-ttu-id="56413-760">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-761">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-761"></span></span>|
|<span data-ttu-id="56413-762">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-763">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-763"></span></span>|
|<span data-ttu-id="56413-764">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-764">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-765">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-765"></span></span>|
|<span data-ttu-id="56413-766">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-767">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-767"></span></span>|
   
 <span data-ttu-id="56413-768">**GlobalSign 조직 유효성 검사 CA-SHA256-g 2**</span><span class="sxs-lookup"><span data-stu-id="56413-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-769">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-769">**Subject**</span></span>|
|<span data-ttu-id="56413-770">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-770"></span></span>|
|<span data-ttu-id="56413-771">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-771">**Issuer**</span></span>|
|<span data-ttu-id="56413-772">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-772"></span></span>|
|<span data-ttu-id="56413-773">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-773">**Serial Number**</span></span>|
|<span data-ttu-id="56413-774">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-774"></span></span>|
|<span data-ttu-id="56413-775">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-775">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-776">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-776"></span></span>|
|<span data-ttu-id="56413-777">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-778">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-778"></span></span>|
|<span data-ttu-id="56413-779">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-780">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-780"></span></span>|
|<span data-ttu-id="56413-781">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-781">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-782">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-782"></span></span>|
|<span data-ttu-id="56413-783">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-784">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-784"></span></span>|
|<span data-ttu-id="56413-785">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-786">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-786"></span></span>|
|<span data-ttu-id="56413-787">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-788">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-788"></span></span>|
|<span data-ttu-id="56413-789">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-790">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-790"></span></span>|
|<span data-ttu-id="56413-791">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-792">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-792"></span></span>|
|<span data-ttu-id="56413-793">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-793">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-794">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-794"></span></span>|
|<span data-ttu-id="56413-795">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-796">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-796"></span></span>|
   
 <span data-ttu-id="56413-797">**GlobalSign 조직 유효성 검사 CA-SHA256-g 2**</span><span class="sxs-lookup"><span data-stu-id="56413-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-798">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-798">**Subject**</span></span>|
|<span data-ttu-id="56413-799">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-799"></span></span>|
|<span data-ttu-id="56413-800">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-800">**Issuer**</span></span>|
|<span data-ttu-id="56413-801">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-801"></span></span>|
|<span data-ttu-id="56413-802">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-802">**Serial Number**</span></span>|
|<span data-ttu-id="56413-803">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-803"></span></span>|
|<span data-ttu-id="56413-804">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-804">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-805">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-805"></span></span>|
|<span data-ttu-id="56413-806">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-807">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-807"></span></span>|
|<span data-ttu-id="56413-808">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-809">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-809"></span></span>|
|<span data-ttu-id="56413-810">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-810">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-811">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-811"></span></span>|
|<span data-ttu-id="56413-812">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-813">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-813"></span></span>|
|<span data-ttu-id="56413-814">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-815">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-815"></span></span>|
|<span data-ttu-id="56413-816">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-817">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-817"></span></span>|
|<span data-ttu-id="56413-818">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-819">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-819"></span></span>|
|<span data-ttu-id="56413-820">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-821">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-821"></span></span>|
|<span data-ttu-id="56413-822">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-822">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-823">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-823"></span></span>|
|<span data-ttu-id="56413-824">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-825">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-825"></span></span>|
   
 <span data-ttu-id="56413-826">**이제 기관 X3 암호화**</span><span class="sxs-lookup"><span data-stu-id="56413-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-827">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-827">**Subject**</span></span>|
|<span data-ttu-id="56413-828">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-828"></span></span>|
|<span data-ttu-id="56413-829">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-829">**Issuer**</span></span>|
|<span data-ttu-id="56413-830">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-830"></span></span>|
|<span data-ttu-id="56413-831">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-831">**Serial Number**</span></span>|
|<span data-ttu-id="56413-832">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-832"></span></span>|
|<span data-ttu-id="56413-833">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-833">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-834">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-834"></span></span>|
|<span data-ttu-id="56413-835">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-836">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-836"></span></span>|
|<span data-ttu-id="56413-837">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-838">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-838"></span></span>|
|<span data-ttu-id="56413-839">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-839">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-840">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-840"></span></span>|
|<span data-ttu-id="56413-841">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-842">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-842"></span></span>|
|<span data-ttu-id="56413-843">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-844">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-844"></span></span>|
|<span data-ttu-id="56413-845">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-846">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-846"></span></span>|
|<span data-ttu-id="56413-847">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-848">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-848"></span></span>|
|<span data-ttu-id="56413-849">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-850">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-850"></span></span>|
|<span data-ttu-id="56413-851">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="56413-851">**AIA URLs**</span></span>|
|<span data-ttu-id="56413-852">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-852"></span></span>|
|<span data-ttu-id="56413-853">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-853">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-854">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-854"></span></span>|
|<span data-ttu-id="56413-855">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-856">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-856"></span></span>|
   
 <span data-ttu-id="56413-857">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="56413-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-858">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-858">**Subject**</span></span>|
|<span data-ttu-id="56413-859">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-859"></span></span>|
|<span data-ttu-id="56413-860">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-860">**Issuer**</span></span>|
|<span data-ttu-id="56413-861">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-861"></span></span>|
|<span data-ttu-id="56413-862">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-862">**Serial Number**</span></span>|
|<span data-ttu-id="56413-863">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-863"></span></span>|
|<span data-ttu-id="56413-864">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-864">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-865">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-865"></span></span>|
|<span data-ttu-id="56413-866">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-867">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-867"></span></span>|
|<span data-ttu-id="56413-868">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-869">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-869"></span></span>|
|<span data-ttu-id="56413-870">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-870">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-871">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-871"></span></span>|
|<span data-ttu-id="56413-872">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-873">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-873"></span></span>|
|<span data-ttu-id="56413-874">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-875">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-875"></span></span>|
|<span data-ttu-id="56413-876">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-877">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-877"></span></span>|
|<span data-ttu-id="56413-878">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-879">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-879"></span></span>|
|<span data-ttu-id="56413-880">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-881">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-881"></span></span>|
|<span data-ttu-id="56413-882">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-882">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-883">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-883"></span></span>|
   
 <span data-ttu-id="56413-884">**Microsoft IT SSL SHA2**</span><span class="sxs-lookup"><span data-stu-id="56413-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-885">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-885">**Subject**</span></span>|
|<span data-ttu-id="56413-886">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-886"></span></span>|
|<span data-ttu-id="56413-887">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-887">**Issuer**</span></span>|
|<span data-ttu-id="56413-888">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-888"></span></span>|
|<span data-ttu-id="56413-889">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-889">**Serial Number**</span></span>|
|<span data-ttu-id="56413-890">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-890"></span></span>|
|<span data-ttu-id="56413-891">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-891">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-892">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-892"></span></span>|
|<span data-ttu-id="56413-893">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-894">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-894"></span></span>|
|<span data-ttu-id="56413-895">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-896">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-896"></span></span>|
|<span data-ttu-id="56413-897">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-897">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-898">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-898"></span></span>|
|<span data-ttu-id="56413-899">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-900">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-900"></span></span>|
|<span data-ttu-id="56413-901">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-902">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-902"></span></span>|
|<span data-ttu-id="56413-903">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-904">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-904"></span></span>|
|<span data-ttu-id="56413-905">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-906">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-906"></span></span>|
|<span data-ttu-id="56413-907">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-908">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-908"></span></span>|
|<span data-ttu-id="56413-909">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-909">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-910">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-910"></span></span>|
|<span data-ttu-id="56413-911">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-912">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-912"></span></span>|
   
 <span data-ttu-id="56413-913">**Microsoft IT TLS CA 1**</span><span class="sxs-lookup"><span data-stu-id="56413-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-914">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-914">**Subject**</span></span>|
|<span data-ttu-id="56413-915">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-915"></span></span>|
|<span data-ttu-id="56413-916">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-916">**Issuer**</span></span>|
|<span data-ttu-id="56413-917">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-917"></span></span>|
|<span data-ttu-id="56413-918">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-918">**Serial Number**</span></span>|
|<span data-ttu-id="56413-919">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-919"></span></span>|
|<span data-ttu-id="56413-920">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-920">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-921">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-921"></span></span>|
|<span data-ttu-id="56413-922">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-923">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-923"></span></span>|
|<span data-ttu-id="56413-924">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-925">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-925"></span></span>|
|<span data-ttu-id="56413-926">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-926">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-927">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-927"></span></span>|
|<span data-ttu-id="56413-928">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-929">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-929"></span></span>|
|<span data-ttu-id="56413-930">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-931">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-931"></span></span>|
|<span data-ttu-id="56413-932">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-933">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-933"></span></span>|
|<span data-ttu-id="56413-934">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-935">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-935"></span></span>|
|<span data-ttu-id="56413-936">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-937">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-937"></span></span>|
|<span data-ttu-id="56413-938">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-938">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-939">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-939"></span></span>|
|<span data-ttu-id="56413-940">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-941">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-941"></span></span>|
   
 <span data-ttu-id="56413-942">**Microsoft IT TLS CA 2**</span><span class="sxs-lookup"><span data-stu-id="56413-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-943">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-943">**Subject**</span></span>|
|<span data-ttu-id="56413-944">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-944"></span></span>|
|<span data-ttu-id="56413-945">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-945">**Issuer**</span></span>|
|<span data-ttu-id="56413-946">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-946"></span></span>|
|<span data-ttu-id="56413-947">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-947">**Serial Number**</span></span>|
|<span data-ttu-id="56413-948">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-948"></span></span>|
|<span data-ttu-id="56413-949">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-949">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-950">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-950"></span></span>|
|<span data-ttu-id="56413-951">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-952">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-952"></span></span>|
|<span data-ttu-id="56413-953">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-954">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-954"></span></span>|
|<span data-ttu-id="56413-955">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-955">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-956">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-956"></span></span>|
|<span data-ttu-id="56413-957">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-958">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-958"></span></span>|
|<span data-ttu-id="56413-959">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-960">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-960"></span></span>|
|<span data-ttu-id="56413-961">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-962">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-962"></span></span>|
|<span data-ttu-id="56413-963">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-964">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-964"></span></span>|
|<span data-ttu-id="56413-965">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-966">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-966"></span></span>|
|<span data-ttu-id="56413-967">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-967">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-968">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-968"></span></span>|
|<span data-ttu-id="56413-969">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-970">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-970"></span></span>|
   
 <span data-ttu-id="56413-971">**Microsoft IT TLS CA 4**</span><span class="sxs-lookup"><span data-stu-id="56413-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-972">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-972">**Subject**</span></span>|
|<span data-ttu-id="56413-973">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-973"></span></span>|
|<span data-ttu-id="56413-974">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-974">**Issuer**</span></span>|
|<span data-ttu-id="56413-975">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-975"></span></span>|
|<span data-ttu-id="56413-976">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-976">**Serial Number**</span></span>|
|<span data-ttu-id="56413-977">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-977"></span></span>|
|<span data-ttu-id="56413-978">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-978">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-979">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-979"></span></span>|
|<span data-ttu-id="56413-980">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-981">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-981"></span></span>|
|<span data-ttu-id="56413-982">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-983">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-983"></span></span>|
|<span data-ttu-id="56413-984">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-984">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-985">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-985"></span></span>|
|<span data-ttu-id="56413-986">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-987">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-987"></span></span>|
|<span data-ttu-id="56413-988">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-989">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-989"></span></span>|
|<span data-ttu-id="56413-990">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-991">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-991"></span></span>|
|<span data-ttu-id="56413-992">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-993">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-993"></span></span>|
|<span data-ttu-id="56413-994">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-995">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-995"></span></span>|
|<span data-ttu-id="56413-996">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-996">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-997">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-997"></span></span>|
|<span data-ttu-id="56413-998">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-999">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-999"></span></span>|
   
 <span data-ttu-id="56413-1000">**Microsoft IT TLS CA 5**</span><span class="sxs-lookup"><span data-stu-id="56413-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-1001">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-1001">**Subject**</span></span>|
|<span data-ttu-id="56413-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1002"></span></span>|
|<span data-ttu-id="56413-1003">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-1003">**Issuer**</span></span>|
|<span data-ttu-id="56413-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1004"></span></span>|
|<span data-ttu-id="56413-1005">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-1005">**Serial Number**</span></span>|
|<span data-ttu-id="56413-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1006"></span></span>|
|<span data-ttu-id="56413-1007">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1008"></span></span>|
|<span data-ttu-id="56413-1009">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1010"></span></span>|
|<span data-ttu-id="56413-1011">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1012"></span></span>|
|<span data-ttu-id="56413-1013">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1014"></span></span>|
|<span data-ttu-id="56413-1015">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1016"></span></span>|
|<span data-ttu-id="56413-1017">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1018"></span></span>|
|<span data-ttu-id="56413-1019">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1020"></span></span>|
|<span data-ttu-id="56413-1021">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1022"></span></span>|
|<span data-ttu-id="56413-1023">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1024"></span></span>|
|<span data-ttu-id="56413-1025">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1026"></span></span>|
|<span data-ttu-id="56413-1027">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1028"></span></span>|
   
 <span data-ttu-id="56413-1029">**Symantec 클래스 3 EV SSL CA-G3**</span><span class="sxs-lookup"><span data-stu-id="56413-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-1030">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-1030">**Subject**</span></span>|
|<span data-ttu-id="56413-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1031"></span></span>|
|<span data-ttu-id="56413-1032">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-1032">**Issuer**</span></span>|
|<span data-ttu-id="56413-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1033"></span></span>|
|<span data-ttu-id="56413-1034">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="56413-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="56413-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1035"></span></span>|
|<span data-ttu-id="56413-1036">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-1036">**Serial Number**</span></span>|
|<span data-ttu-id="56413-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1037"></span></span>|
|<span data-ttu-id="56413-1038">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1039"></span></span>|
|<span data-ttu-id="56413-1040">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1041"></span></span>|
|<span data-ttu-id="56413-1042">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1043"></span></span>|
|<span data-ttu-id="56413-1044">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1045"></span></span>|
|<span data-ttu-id="56413-1046">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1047"></span></span>|
|<span data-ttu-id="56413-1048">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1049"></span></span>|
|<span data-ttu-id="56413-1050">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1051"></span></span>|
|<span data-ttu-id="56413-1052">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1053"></span></span>|
|<span data-ttu-id="56413-1054">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1055"></span></span>|
|<span data-ttu-id="56413-1056">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1057"></span></span>|
|<span data-ttu-id="56413-1058">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1059"></span></span>|
   
 <span data-ttu-id="56413-1060">**Symantec 클래스 3 안전한 서버 CA-G4**</span><span class="sxs-lookup"><span data-stu-id="56413-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-1061">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-1061">**Subject**</span></span>|
|<span data-ttu-id="56413-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1062"></span></span>|
|<span data-ttu-id="56413-1063">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-1063">**Issuer**</span></span>|
|<span data-ttu-id="56413-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1064"></span></span>|
|<span data-ttu-id="56413-1065">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="56413-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="56413-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1066"></span></span>|
|<span data-ttu-id="56413-1067">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-1067">**Serial Number**</span></span>|
|<span data-ttu-id="56413-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1068"></span></span>|
|<span data-ttu-id="56413-1069">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1070"></span></span>|
|<span data-ttu-id="56413-1071">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1072"></span></span>|
|<span data-ttu-id="56413-1073">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1074"></span></span>|
|<span data-ttu-id="56413-1075">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1076"></span></span>|
|<span data-ttu-id="56413-1077">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1078"></span></span>|
|<span data-ttu-id="56413-1079">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1080"></span></span>|
|<span data-ttu-id="56413-1081">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1082"></span></span>|
|<span data-ttu-id="56413-1083">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1084"></span></span>|
|<span data-ttu-id="56413-1085">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1086"></span></span>|
|<span data-ttu-id="56413-1087">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1088"></span></span>|
|<span data-ttu-id="56413-1089">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1090"></span></span>|
   
 <span data-ttu-id="56413-1091">**thawte SHA256 SSL CA**</span><span class="sxs-lookup"><span data-stu-id="56413-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-1092">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-1092">**Subject**</span></span>|
|<span data-ttu-id="56413-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1093"></span></span>|
|<span data-ttu-id="56413-1094">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-1094">**Issuer**</span></span>|
|<span data-ttu-id="56413-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1095"></span></span>|
|<span data-ttu-id="56413-1096">**주체 대체 이름**</span><span class="sxs-lookup"><span data-stu-id="56413-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="56413-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1097"></span></span>|
|<span data-ttu-id="56413-1098">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-1098">**Serial Number**</span></span>|
|<span data-ttu-id="56413-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1099"></span></span>|
|<span data-ttu-id="56413-1100">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1101"></span></span>|
|<span data-ttu-id="56413-1102">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1103"></span></span>|
|<span data-ttu-id="56413-1104">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1105"></span></span>|
|<span data-ttu-id="56413-1106">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1107"></span></span>|
|<span data-ttu-id="56413-1108">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1109"></span></span>|
|<span data-ttu-id="56413-1110">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1111"></span></span>|
|<span data-ttu-id="56413-1112">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1113"></span></span>|
|<span data-ttu-id="56413-1114">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1115"></span></span>|
|<span data-ttu-id="56413-1116">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1117"></span></span>|
|<span data-ttu-id="56413-1118">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1119"></span></span>|
|<span data-ttu-id="56413-1120">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1121"></span></span>|
   
 <span data-ttu-id="56413-1122">**Verizon Akamai SureServer CA g 14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="56413-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="56413-1123">**제목**</span><span class="sxs-lookup"><span data-stu-id="56413-1123">**Subject**</span></span>|
|<span data-ttu-id="56413-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1124"></span></span>|
|<span data-ttu-id="56413-1125">**Issuer**</span><span class="sxs-lookup"><span data-stu-id="56413-1125">**Issuer**</span></span>|
|<span data-ttu-id="56413-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1126"></span></span>|
|<span data-ttu-id="56413-1127">**일련번호**</span><span class="sxs-lookup"><span data-stu-id="56413-1127">**Serial Number**</span></span>|
|<span data-ttu-id="56413-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1128"></span></span>|
|<span data-ttu-id="56413-1129">**공개 키 길이**</span><span class="sxs-lookup"><span data-stu-id="56413-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="56413-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1130"></span></span>|
|<span data-ttu-id="56413-1131">**서명 알고리즘**</span><span class="sxs-lookup"><span data-stu-id="56413-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="56413-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1132"></span></span>|
|<span data-ttu-id="56413-1133">**유효 하지 전에**</span><span class="sxs-lookup"><span data-stu-id="56413-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="56413-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1134"></span></span>|
|<span data-ttu-id="56413-1135">**유효 하지 후**</span><span class="sxs-lookup"><span data-stu-id="56413-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="56413-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1136"></span></span>|
|<span data-ttu-id="56413-1137">**주체 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="56413-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1138"></span></span>|
|<span data-ttu-id="56413-1139">**인증 기관 키 식별자**</span><span class="sxs-lookup"><span data-stu-id="56413-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="56413-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1140"></span></span>|
|<span data-ttu-id="56413-1141">**지문 (s h A-1)**</span><span class="sxs-lookup"><span data-stu-id="56413-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="56413-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1142"></span></span>|
|<span data-ttu-id="56413-1143">**지문 (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1144"></span></span>|
|<span data-ttu-id="56413-1145">**Pin (s h A-256)**</span><span class="sxs-lookup"><span data-stu-id="56413-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="56413-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1146"></span></span>|
|<span data-ttu-id="56413-1147">**AIA Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="56413-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1148"></span></span>|
|<span data-ttu-id="56413-1149">**CRL Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="56413-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1150"></span></span>|
|<span data-ttu-id="56413-1151">**OCSP Url**</span><span class="sxs-lookup"><span data-stu-id="56413-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="56413-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="56413-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="56413-1153">추가 인증서 경로</span><span class="sxs-lookup"><span data-stu-id="56413-1153">Additional certificate paths</span></span>
<span data-ttu-id="56413-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="56413-1154"></span></span>

<span data-ttu-id="56413-1155">다음은 위에 포함 되지 않은 시간에 따른 위의 목록을 사용 하 여 병합 될 하 레거시 인증서를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="56413-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


