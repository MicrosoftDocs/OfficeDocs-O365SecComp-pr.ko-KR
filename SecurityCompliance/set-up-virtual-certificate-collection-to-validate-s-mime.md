---
title: S/MIME의 유효성을 검사 하기 위해 Exchange Online에서 가상 인증서 컬렉션 설정
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: 관리자는 Exchange Online에서 S/MIME 인증서의 유효성을 검사 하는 데 사용 되는 가상 인증서 컬렉션을 만드는 방법을 배울 수 있습니다.
ms.openlocfilehash: 15998bce1971952286d8dd4401a92f1e9e47c25d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260726"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a><span data-ttu-id="60899-103">S/MIME의 유효성을 검사 하기 위해 Exchange Online에서 가상 인증서 컬렉션 설정</span><span class="sxs-lookup"><span data-stu-id="60899-103">Set up virtual certificate collection in Exchange Online to validate S/MIME</span></span>

<span data-ttu-id="60899-104">관리자는 S/MIME 인증서의 유효성을 검사 하는 데 사용할 수 있는 가상 인증서 컬렉션을 Exchange Online에서 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="60899-104">As an admin, you will need to configure a virtual certificate collection in Exchange Online that will be used to validate S/MIME certificates.</span></span> <span data-ttu-id="60899-105">이 가상 인증서 컬렉션은 SST 파일 이름 확장명이 포함 된 인증서 저장소로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60899-105">This virtual certificate collection is set up as a certificate store with an SST filename extension.</span></span> <span data-ttu-id="60899-106">SST 파일에는 S/MIME 인증서 유효성을 검사할 때 사용되는 모든 루트 및 중간 인증서가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="60899-106">The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>

## <a name="create-and-save-an-sst"></a><span data-ttu-id="60899-107">SST 만들기 및 저장</span><span class="sxs-lookup"><span data-stu-id="60899-107">Create and save an SST</span></span>

<span data-ttu-id="60899-108">Windows PowerShell에서 SST cmdlet을 사용 하 여 신뢰할 수 있는 컴퓨터에서 인증서를 내보내고, \*\*\*\* _Type_ 값을 SST로 지정 하 여이 인증서 저장소 파일을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60899-108">You can create this SST certificate store file by exporting the certificates from a trusted machine using the **Export-Certificate** cmdlet in Windows PowerShell and specifying the _Type_ value as SST.</span></span> <span data-ttu-id="60899-109">자세한 내용은 [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="60899-109">For instructions, see [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span></span>

<span data-ttu-id="60899-110">SST 인증서 저장소 파일이 있으면 exchange online PowerShell에서 다음 구문을 사용 하 여 exchange online 가상 인증서 저장소에 SST 파일 콘텐츠를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="60899-110">Once you have the SST certificate store file, use the following syntax in Exchange Online PowerShell to save the SST file contents in the Exchange Online virtual certificate store.</span></span> <span data-ttu-id="60899-111">Exchange Online PowerShell에 연결하려면 [Exchange Online PowerShell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="60899-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

<span data-ttu-id="60899-112">이 예제에서는 SST 파일 C:\My documents\exported 인증서 저장소 SST를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60899-112">This example imports the SST file C:\My Documents\Exported Certificate Store.sst.</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

<span data-ttu-id="60899-113">구문 및 매개 변수에 대 한 자세한 내용은 [get-smimeconfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="60899-113">For detailed syntax and parameter information, see [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span></span>

## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="60899-114">인증서가 유효한지 확인</span><span class="sxs-lookup"><span data-stu-id="60899-114">Ensuring a certificate is valid</span></span>

<span data-ttu-id="60899-115">Exchange Online에서는 인증서 유효성 검사에 SST만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60899-115">In Exchange Online, only the SST is used for certificate validation.</span></span>

## <a name="more-information"></a><span data-ttu-id="60899-116">추가 정보</span><span class="sxs-lookup"><span data-stu-id="60899-116">More Information</span></span>

[<span data-ttu-id="60899-117">메시지 서명 및 암호화를 위한 S/MIME</span><span class="sxs-lookup"><span data-stu-id="60899-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="60899-118">get-smimeconfig</span><span class="sxs-lookup"><span data-stu-id="60899-118">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
