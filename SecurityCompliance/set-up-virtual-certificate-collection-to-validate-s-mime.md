---
title: S/MIME 유효성을 검사 하려면 가상 인증서 컬렉션 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: 테 넌 트 관리자의 S/MIME 인증서의 유효성을 검사 하는데 사용 되는 가상 인증서 컬렉션을 구성 해야 합니다.
ms.openlocfilehash: 4b2d85181d95bb1f90d46412cca85c2356d98e10
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22028145"
---
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a><span data-ttu-id="cdff9-103">S/MIME 유효성을 검사 하려면 가상 인증서 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="cdff9-103">Set up virtual certificate collection to validate S/MIME</span></span>

<span data-ttu-id="cdff9-p101">테넌트 관리자는 S/MIME 인증서의 유효성을 검사하는 데 사용할 가상 인증서 컬렉션을 구성해야 합니다. 이 가상 인증서 컬렉션은 SST 파일 이름 확장명이 지정된 인증서 저장소 파일 형식으로 설정됩니다. SST 파일에는 S/MIME 인증서 유효성을 검사할 때 사용되는 모든 루트 및 중간 인증서가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdff9-p101">As a tenant administrator you will need to configure a virtual certificate collection that will be used to validate S/MIME certificates. This virtual certificate collection is set up as a certificate store file type with an SST filename extension. The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>
  
## <a name="create-and-save-an-sst"></a><span data-ttu-id="cdff9-107">SST 만들기 및 저장</span><span class="sxs-lookup"><span data-stu-id="cdff9-107">Create and save an SST</span></span>
<span data-ttu-id="cdff9-108"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="cdff9-108"></span></span>

<span data-ttu-id="cdff9-p102">이 절차를 수행 하려면 셸을만 사용할 수 있습니다. 온-프레미스 Exchange 조직에서 Exchange 관리 셸을 열려면 하는 방법을 알아보려면 **셸을 열**을 참조 하십시오. Exchange Online에 연결 하려면 Windows PowerShell을 사용 하는 방법을 알아보려면 [Exchange Online PowerShell 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="cdff9-p102">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
<span data-ttu-id="cdff9-p103">관리자는  `Export-Certificate` cmdlet을 사용하고 형식을 SST로 지정하여 신뢰할 수 있는 컴퓨터에서 인증서를 내보내는 방법으로 이 SST 파일을 만들 수 있습니다.  `Export-Certificate` cmdlet에 대한 자세한 내용은 [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx) 참조 항목을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cdff9-p103">As an administrator, you can create this SST file by exporting the certificates from a trusted machine using the  `Export-Certificate` cmdlet and specifying the type as SST. For more information the  `Export-Certificate` cmdlet, see the [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx) reference topic.</span></span> 
  
<span data-ttu-id="cdff9-p104">SST 파일을 만든 후  `Set-Smimeconfig` cmdlet에서  _-SMIMECertificateIssuingCA_ 매개 변수를 사용하여 가상 인증서 저장소에 해당 파일을 저장합니다. 예를 들면 다음과 같습니다.  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span><span class="sxs-lookup"><span data-stu-id="cdff9-p104">Once the SST file is generated, use the  `Set-Smimeconfig` cmdlet to save it in the virtual certificate store by using the  _-SMIMECertificateIssuingCA_ parameter. For example:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span></span>
  
## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="cdff9-116">인증서가 유효한지 확인</span><span class="sxs-lookup"><span data-stu-id="cdff9-116">Ensuring a certificate is valid</span></span>
<span data-ttu-id="cdff9-117"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="cdff9-117"></span></span>

<span data-ttu-id="cdff9-p105">Exchange 2013 SP1에서는 먼저 SST 파일을 확인한 다음 인증서 유효성을 검사합니다. 유효성 검사가 실패하면 로컬 컴퓨터 인증서 저장소를 확인하여 인증서 유효성을 검사합니다. 이 동작은 Exchange 2013 SP1에서 새롭게 제공되며 이전 버전의 Exchange와는 다릅니다. Exchange Online에서는 유효성 검사에 SST만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdff9-p105">Exchange 2013 SP1 first checks for the SST file and validates the certificate. If the validation fails, it will look at the local machine certificate store to validate the certificate. This behavior is new for Exchange 2013 SP1 and different from prior versions of Exchange. In Exchange Online only the SST will be used for validation.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="cdff9-122">추가 정보</span><span class="sxs-lookup"><span data-stu-id="cdff9-122">More Information</span></span>
<span data-ttu-id="cdff9-123"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="cdff9-123"></span></span>

[<span data-ttu-id="cdff9-124">S/MIME 메시지 서명 및 암호화에 대 한</span><span class="sxs-lookup"><span data-stu-id="cdff9-124">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="cdff9-125">Get-smimeconfig</span><span class="sxs-lookup"><span data-stu-id="cdff9-125">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  

