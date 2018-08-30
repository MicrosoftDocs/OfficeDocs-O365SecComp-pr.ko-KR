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
# <a name="office-365-certificate-chains"></a>Office 365 인증서 체인

Office 365 기술을 활용 하는 다른 인증서 공급자의 수입니다. 다음은 고객이 Office 365에 액세스할 때 발생할 수 있는 알려진된 Office 365 루트 인증서의 전체 목록에 대 한 설명입니다. 직접 인프라에 설치 해야할 수 인증서는 정보를 [Office 365 용 타사 SSL 인증서에 대 한 계획을](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce)참조 합니다. 다음 인증서 정보는 Office 365의 모든 전세계 및 국가 클라우드 인스턴스에 적용 됩니다.
  

|**인증서 유형**|**여.p7b 다운로드**|**CRL 끝점**|**OCSP 끝점**|**AIA 끝점**|
|:-----|:-----|:-----|:-----|:-----|
|[공개적으로 신뢰할 수 있는 루트 인증서](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[Office 365 루트 인증서 번들 (여.p7b)](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |crl.globalsign.net  <br/> www.d-trust.net  <br/> |해당 없음  <br/> |해당 없음  <br/> |
|[공개적으로 신뢰할 수 있는 중간 인증서](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[Office 365 중간 인증서 번들 (여.p7b)](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |cdp1.public trust.com  <br/> crl.cnnic.cn  <br/> crl.entrust.net  <br/> crl.globalsign.com  <br/> crl.globalsign.net  <br/> crl.identrust.com  <br/> crl.thawte.com  <br/> crl3.digicert.com  <br/> crl4.digicert.com  <br/> s1.symcb.com  <br/> www.d-trust.net  <br/> |isrg.trustid.ocsp.identrust.com  <br/> ocsp.digicert.com  <br/> ocsp.entrust.net  <br/> ocsp.globalsign.com  <br/> ocsp.omniroot.com  <br/> ocsp.startssl.com  <br/> ocsp.thawte.com  <br/> ocsp2.globalsign.com  <br/> ocspcnnicroot.cnnic.cn  <br/> 루트-c3-c a 2-2009.ocsp.d-trust.net  <br/> root-c3-ca2-ev-2009.ocsp.d-trust.net  <br/> s2.symcb.com  <br/> |aia.startssl.com  <br/> apps.identrust.com  <br/> cacert.omniroot.com  <br/> www.cnnic.cn  <br/> |
   
루트 및 인증서 공급자에 대 한 추가 세부 정보를 보려면 아래 중간 섹션을 확장 합니다.
  
## <a name="office-365-root-certificate-details"></a>Office 365 루트 인증서 세부 정보
<a name="RootCerts"> </a>

 **Baltimore CyberTrust Root**
  
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **CNNIC 루트**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **DigiCert 전역 루트 CA**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **DigiCert 높은 보증 EV 루트 CA**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **D-신뢰 루트 클래스 3 CA 2 2009**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
   
 **D-신뢰 루트 클래스 3 CA 2 EV 2009**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
   
 **DST 루트 CA X3**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **루트 인증 기관-G2 맡길**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **Entrust.net Certification Authority (2048)**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **GlobalSign**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
   
 **GlobalSign Root CA**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **thawte 기본 루트 CA-G3**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
 **VeriSign 클래스 3 기본 공용 인증 기관-g 5**
  
||
|:-----|
|**제목**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
   
## <a name="office-365-intermediate-certificate-details"></a>Office 365 중간 인증서 세부 정보
<a name="IntermediateCerts"> </a>

 **CNNIC SHA256 SSL**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**AIA Url**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **D-신뢰 SSL 클래스 3 CA 1 2009**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**주체 대체 이름**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **D-신뢰 SSL 클래스 3 CA 1 EV 2009**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**주체 대체 이름**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **DigiCert 클라우드 서비스 CA-1**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **DigiCert SHA2 높은 보증 서버 CA**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **DigiCert SHA2 안전한 서버 CA**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **인증 기관-L1C 맡길**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **인증 기관-L1K 맡길**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **GlobalSign**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **GlobalSign 유효성 검사 CA-SHA256-g 2를 확장 합니다.**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **GlobalSign 유효성 검사-SHA256-CA G3 확장**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **GlobalSign 조직 유효성 검사 CA-SHA256-g 2**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **GlobalSign 조직 유효성 검사 CA-SHA256-g 2**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **이제 기관 X3 암호화**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**AIA Url**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Microsoft IT SSL SHA2**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
   
 **Microsoft IT SSL SHA2**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Microsoft IT TLS CA 1**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Microsoft IT TLS CA 2**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Microsoft IT TLS CA 4**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Microsoft IT TLS CA 5**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Symantec 클래스 3 EV SSL CA-G3**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**주체 대체 이름**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Symantec 클래스 3 안전한 서버 CA-G4**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**주체 대체 이름**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **thawte SHA256 SSL CA**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**주체 대체 이름**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
 **Verizon Akamai SureServer CA g 14-SHA2**
  
||
|:-----|
|**제목**|
|:-----|
|**Issuer**|
|:-----|
|**일련번호**|
|:-----|
|**공개 키 길이**|
|:-----|
|**서명 알고리즘**|
|:-----|
|**유효 하지 전에**|
|:-----|
|**유효 하지 후**|
|:-----|
|**주체 키 식별자**|
|:-----|
|**인증 기관 키 식별자**|
|:-----|
|**지문 (s h A-1)**|
|:-----|
|**지문 (s h A-256)**|
|:-----|
|**Pin (s h A-256)**|
|:-----|
|**AIA Url**|
|:-----|
|**CRL Url**|
|:-----|
|**OCSP Url**|
|:-----|
   
## <a name="additional-certificate-paths"></a>추가 인증서 경로
<a name="IntermediateCerts"> </a>

다음은 위에 포함 되지 않은 시간에 따른 위의 목록을 사용 하 여 병합 될 하 레거시 인증서를 포함 합니다.
  
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


