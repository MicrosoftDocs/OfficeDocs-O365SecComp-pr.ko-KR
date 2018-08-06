---
title: S/MIME용으로 Office 365에 사용자 인증서 동기화
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: S/MIME로 보호된 메시지를 보내려면 적절한 인증서를 설정해야 합니다. Exchange Online을 통해 암호화된 메시지를 보내기 위해 보낸 사람의 전자 메일 프로그램은 받는 사람의 공용 인증서를 사용하여 메시지를 암호화합니다. 이 공용 X.509 인증서를 Office 365에 게시해야 합니다.
ms.openlocfilehash: aa94dfa6702a25b3fc6b8b883daceddf31d2f66a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026195"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a>S/MIME용으로 Office 365에 사용자 인증서 동기화

S/MIME로 보호된 메시지를 보내려면 적절한 인증서를 설정해야 합니다. Exchange Online을 통해 암호화된 메시지를 보내기 위해 보낸 사람의 전자 메일 프로그램은 받는 사람의 공용 인증서를 사용하여 메시지를 암호화합니다. 이 공용 X.509 인증서를 Office 365에 게시해야 합니다.
  
## <a name="to-sync-certificates-that-support-smime"></a>S/MIME을 지원하는 인증서를 동기화하려면

인증서를 발급하고 로컬 Active Directory 도메인 서비스에 게시하여 S/MIME 설정을 시작합니다. Exchange 2013에서 인증서를 관리하는 방법에 대한 자세한 내용은 [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx)을 참조하세요.
  
인증서를 게시 한 후 Office 365를 온-프레미스 Exchange 환경에서 사용자 데이터를 동기화 하도록 Azure Active Directory 동기화 도구를 사용 합니다. 이 프로세스에 대 한 자세한 내용은 참조 하십시오. [DirSync: 디렉터리 동기화 도구 버전 릴리스 기록](https://go.microsoft.com/fwlink/p/?LinkId=392587)합니다.
  
이 도구는 S/MIME에 사용할 수 있도록 다른 디렉터리 데이터를 동기화하는 동시에 데이터를 사용하여 메시지를 서명 및 암호화할 수 있도록 각 사용자 개체에 대해  `userCertificate` 및  `userSMIMECertificate` 특성도 동기화합니다. 
  
## <a name="more-information"></a>추가 정보

[S/MIME 메시지 서명 및 암호화에 대 한](s-mime-for-message-signing-and-encryption.md)
  
[Azure Active Directory 동기화 도구](https://go.microsoft.com/fwlink/p/?LinkId=392587)
  

