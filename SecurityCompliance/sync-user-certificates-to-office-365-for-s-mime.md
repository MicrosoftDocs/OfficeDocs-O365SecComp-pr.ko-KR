---
title: S/MIME용으로 Office 365에 사용자 인증서 동기화
ms.author: chrisda
author: chrisda
manager: Serdars
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: S/MIME로 보호된 메시지를 보내려면 적절한 인증서를 설정해야 합니다. Exchange Online을 통해 암호화된 메시지를 보내기 위해 보낸 사람의 전자 메일 프로그램은 받는 사람의 공용 인증서를 사용하여 메시지를 암호화합니다. 이 공용 X.509 인증서를 Office 365에 게시해야 합니다.
ms.openlocfilehash: 35de3ba34be48a8553c7034f646576e4fca8b870
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295001"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a>S/MIME용으로 Office 365에 사용자 인증서 동기화

모든 사용자가 Exchange Online에서 S/MIME으로 보호 된 메시지를 보낼 수 있으려면 해당 인증서를 설정 해야 합니다. Exchange Online을 통해 암호화 된 메시지를 보내기 위해 보낸 사람의 전자 메일 앱은 받는 사람의 공용 인증서를 사용 하 여 메시지를 암호화 합니다. 이 공용 x.509 인증서를 Office 365에 게시 해야 합니다.

## <a name="to-sync-certificates-that-support-smime"></a>S/MIME을 지원하는 인증서를 동기화하려면

인증서를 발급 하 고 로컬 Active Directory 도메인 서비스에 게시 하 여 S/MIME 설정을 시작 합니다. Exchange Server에서 인증서를 관리 하는 방법에 대 한 자세한 내용은 [디지털 인증서 및 SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx)을 참조 하십시오.

인증서를 게시 한 후에는 Azure Active Directory 동기화 도구를 사용 하 여 온-프레미스 Exchange 환경의 사용자 데이터를 Office 365와 동기화 합니다. 이 프로세스에 대 한 자세한 내용은 [DirSync: 디렉터리 동기화 도구 버전 릴리스 기록을](https://go.microsoft.com/fwlink/p/?LinkId=392587)참조 하세요.

S/MIME을 위해 다른 디렉터리 데이터를 동기화 하는 것과 함께,이 도구는 각 사용자 개체에 대 한 **userCertificate** 및 **userSMIMECertificate** 특성을 동기화 하 여 데이터를 사용 하 여 메시지를 서명 하 고 암호화 하는 데 사용할 수 있습니다.

## <a name="more-information"></a>추가 정보

[메시지 서명 및 암호화를 위한 S/MIME](s-mime-for-message-signing-and-encryption.md)

[Azure Active Directory 동기화 도구](https://go.microsoft.com/fwlink/p/?LinkId=392587)
