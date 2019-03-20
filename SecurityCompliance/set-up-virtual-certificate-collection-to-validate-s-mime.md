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
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693557"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a>S/MIME의 유효성을 검사 하기 위해 Exchange Online에서 가상 인증서 컬렉션 설정

관리자는 S/MIME 인증서의 유효성을 검사 하는 데 사용할 수 있는 가상 인증서 컬렉션을 Exchange Online에서 구성 해야 합니다. 이 가상 인증서 컬렉션은 SST 파일 이름 확장명이 포함 된 인증서 저장소로 설정 됩니다. SST 파일에는 S/MIME 인증서 유효성을 검사할 때 사용되는 모든 루트 및 중간 인증서가 포함됩니다.

## <a name="create-and-save-an-sst"></a>SST 만들기 및 저장

Windows PowerShell에서 SST cmdlet을 사용 하 여 신뢰할 수 있는 컴퓨터에서 인증서를 내보내고, **** _Type_ 값을 SST로 지정 하 여이 인증서 저장소 파일을 만들 수도 있습니다. 자세한 내용은 [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate)를 참조 하십시오.

SST 인증서 저장소 파일이 있으면 exchange online PowerShell에서 다음 구문을 사용 하 여 exchange online 가상 인증서 저장소에 SST 파일 콘텐츠를 저장 합니다. exchange online powershell에 연결 하려면 [exchange online powershell에 연결](https://go.microsoft.com/fwlink/p/?linkid=396554)을 참조 하세요.

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

이 예제에서는 SST 파일 C:\My documents\exported 인증서 저장소 SST를 가져옵니다.

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

구문 및 매개 변수에 대 한 자세한 내용은 [get-smimeconfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig)를 참조 하십시오.

## <a name="ensuring-a-certificate-is-valid"></a>인증서가 유효한지 확인

Exchange Online에서는 인증서 유효성 검사에 SST만 사용 됩니다.

## <a name="more-information"></a>추가 정보

[메시지 서명 및 암호화를 위한 S/MIME](s-mime-for-message-signing-and-encryption.md)

[get-smimeconfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
