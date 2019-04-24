---
title: Office 365에서 데이터 보존, 삭제 및 폐기
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 데이터 보존, 삭제 및 폐기와 관련 된 Microsoft의 Office 365 정책에 대 한 개요입니다.
ms.openlocfilehash: fcae11f10278f1357a68ea3f9a1178da97322775
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262840"
---
# <a name="data-retention-deletion-and-destruction-in-office-365"></a>Office 365에서 데이터 보존, 삭제 및 폐기

Microsoft에는 삭제 후 고객 데이터가 보존 되는 기간을 지정 하는 Office 365에 대 한 데이터 처리 표준 정책이 있습니다. 일반적으로 다음과 같은 두 가지 시나리오에서 고객 데이터를 삭제할 수 있습니다.

- **활성 삭제** -테 넌 트에서 활성 구독이 있고, 사용자가 데이터를 삭제 하거나, 관리자가 사용자가 제공한 데이터를 삭제 합니다.
- **수동 삭제** -테 넌 트 구독이 종료 됩니다.

## <a name="data-retention"></a>데이터 보존

다음 표에서는 이러한 각 삭제 시나리오에 대해 데이터 범주 및 분류별의 최대 데이터 보존 기간을 보여 줍니다.

| 데이터 범주 | 데이터 분류 | 설명 | 예 | 보존 기간 |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| 고객 데이터 | 고객 콘텐츠| 관리자 및 사용자가 직접 제공 하거나 만든 콘텐츠 <br><br> 여기에는 Office 365의 서비스를 사용할 때 Microsoft 데이터 센터에 만들어지고 저장 된 모든 텍스트, 사운드, 비디오, 이미지 파일 및 소프트웨어가 포함 됩니다. | 사용자가 데이터를 작성할 수 있도록 하는 가장 일반적으로 사용 되는 Office 365 응용 프로그램의 예에는 Word, Excel, PowerPoint, Outlook, OneNote 등이 있습니다. <br><br> 고객 콘텐츠에는 고객 소유/제공 비밀 (암호, 인증서, 암호화 키, 저장소 키)도 포함 됩니다. | **활성 삭제 시나리오:** 최대 30 일 <br><br> **수동 삭제 시나리오:** 최대 180 일 |
| 고객 데이터 | 최종 사용자 식별이 가능한 정보 (EUII) | Microsoft 서비스의 사용자를 식별 하는 데 사용할 수 있는 데이터입니다. EUII에는 고객 콘텐츠가 포함 되지 않음 | 사용자 이름 또는 표시 이름 (DOMAIN\UserName) <br><br> 사용자 계정 이름 (name @ domain) <br><br>  사용자 관련 IP 주소 | **활성 삭제 시나리오:** 최대 180 일 (테 넌 트 관리자 작업에만 해당) <br><br> **수동 삭제 시나리오:** 최대 180 일 |
| 개인 데이터 <br> (데이터는 고객 데이터에 포함 되지 않음) | 최종 사용자 익명 id (eupi) | microsoft 서비스 사용자에 게 연결 되는 식별자입니다. eupi가 매핑 테이블과 같은 다른 정보와 함께 사용 되는 경우 최종 사용자를 식별 합니다. <br><br> 사용자가 업로드 하거나 만든 정보를 eupi에 포함 하지 않음 | 사용자 guid, PUIDs 또는 sid <br><br> 세션 id | **활성 삭제 시나리오:** 최대 30 일 <br><br> **수동 삭제 시나리오:** 최대 180 일 |

## <a name="subscription-retention"></a>구독 보존

활성 구독의 용어 중에는 구독자가 Office 365에 저장 된 고객 데이터에 액세스 하거나, 압축을 풀거나, 삭제할 수 있습니다. 유료 구독이 종료 되거나 종료 되 면 Microsoft는 Office 365에 저장 된 고객 데이터를 90 일 동안 제한 된 기능 계정으로 유지 하 여 구독자가 데이터를 추출할 수 있도록 합니다. 90 일의 보존 기간이 끝나면 Microsoft는 계정을 사용 하지 않도록 설정 하 고 고객 데이터를 삭제 합니다. Office 365에 대 한 구독 만료 또는 종료 후부터 180 일 이내에 Microsoft는 계정을 사용 하지 않도록 설정 하 고 모든 고객 데이터를 계정에서 삭제 합니다. 데이터의 최대 보존 기간이 경과 되 면 데이터를 상업적으로 복구할 수 없게 됩니다.

무료 평가판의 경우 계정이 대부분의 국가 및 지역에서 30 일 동안 유예 상태로 전환 됩니다. 이 유예 기간 동안 Office 365을 구입 하는 옵션이 있습니다. Office 365을 구입 하지 않기로 결정 한 경우 평가판을 취소 하거나 유예 기간이 만료 되도록 하 고 평가판 계정 정보 및 데이터를 삭제할 수 있습니다.

## <a name="expedited-deletion"></a>긴급 삭제
구독 기간이 진행 되는 동안 구독자는 Microsoft 지원에 연락 하 고 긴급 구독 프로 비전 해제를 요청할 수 있습니다. 이 프로세스에서는 관리자가 Microsoft에서 제공 하는 잠금 코드를 입력 하 고 나 서 비활성 사서함에 보관 되거나 저장 되는 Exchange online의 데이터를 비롯 한 모든 사용자 데이터가 3 일 후에 삭제 됩니다. 촉진 프로 비전 해제에 대 한 자세한 내용은 [Cancel Office 365](https://support.office.com/article/Cancel-Office-365-for-business-b1bc0bef-4608-4601-813a-cdd9f746709a)를 참조 하세요.

## <a name="related-links"></a>관련 링크
- [데이터 폐기](office-365-data-destruction.md)
- [Office 365의 불변성](office-365-data-immutability.md)
- [Exchange Online 데이터 삭제](office-365-exchange-online-data-deletion.md)
- [SharePoint Online 데이터 삭제](office-365-sharepoint-online-data-deletion.md)
- [비즈니스용 Skype 데이터 삭제](office-365-skype-data-deletion.md)