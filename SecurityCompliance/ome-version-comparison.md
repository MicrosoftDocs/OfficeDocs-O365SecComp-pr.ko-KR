---
title: Office 365 메시지 암호화 버전 비교
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: 두 작업을 계속 함께 하는 방법에 따라 다양 한 버전의 Office 365 메시지 암호화도 함께 제공 되는 기능에 차이점을 설명 하는데 도움이 됩니다.
ms.openlocfilehash: a418d840c7e0eb50ae076bf2b03164bef9488058
ms.sourcegitcommit: 88f3982217c29b558e3f9e838bcb425da395dd5e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/02/2019
ms.locfileid: "29708545"
---
# <a name="compare-versions-of-ome"></a>OME의 버전을 비교

이 문서에는 레거시 Office 365 메시지 암호화 새 OME 기능을 비교합니다. 새 기능은 합병 및 OME와 정보 권한 관리 (IRM)의 최신 버전입니다. Office 365 조직에는 다음 두가지 수 공존 하는 방법을 다루는 표시 됩니다.

||
|:-----|
|이 문서는 Office 365 메시지 암호화에 대 한 문서를 더 큰 시리즈의 일부입니다. 이 문서는 관리자 및 ITPros 위한 것입니다. 방금 경우 보내거나 암호화 된 메시지를 받는 방법에 대 한 정보에 대 한 자세한 내용은 [Office 365 메시지 암호화 OME ()](ome.md) 의 문서 목록을 참조 하 고 요구 사항에 가장 적합 한 문서를 찾습니다. |
||

## <a name="side-by-side-comparison-of-features-and-capabilities"></a>특징 및 기능에 대해-나란히 비교

|                                   |오래 된 기능       |                   |새로운 기능              |
|-----------------------------------|-------------------|-------------------|--------------------------|
|**기능**                     | **레거시 OME**    | **IRM**           | **새 OME 기능** |
|*암호화 된 메일 보내기*        |Exchange 메일 흐름 규칙을 통해|최종 사용자가 Outlook 데스크톱 또는; 웹에서 Outlook을 시작 합니다. Exchange를 통해 메일 흐름 규칙 또는|최종 사용자가 Outlook 데스크톱, Outlook for Mac, 또는; 웹에서 Outlook을 시작 합니다. Exchange 전송 규칙 및 Office 365 데이터 손실 방지 (DLP)를 통해|
|*권한 관리 서식 파일*       |   해당 없음      |착신 전환 옵션을 사용자 지정 서식 파일|착신 전환 옵션, 암호화 전용 옵션 및 사용자 지정 서식 파일을 수행 합니다.|
|*받는 사람 유형*                   |내부 및 외부의 받는 사람|내부 받는 사람         |내부 및 외부의 받는 사람|
|*내부 받는 사람에 대 한 환경*|받는 사람에 게 자신이 다운로드 하 고 웹 브라우저 또는 모바일 응용 프로그램에서 열 수 있는 HTML 메시지로 수신|Outlook 클라이언트에서 네이티브 인라인 환경|Office 365 받는 사람에 대 한 기본 인라인 경험 합니다. 다른 모든 받는 사람 (다운로드 또는 app 필요 없음) OME 포털에서 메시지를 읽을 수 있습니다.|
|*외부의 받는 사람에 대 한 환경*|받는 사람에 게 자신이 다운로드 하 고 웹 브라우저 또는 모바일 응용 프로그램에서 열 수 있는 HTML 메시지로 수신|해당 없음|Office 365 받는 사람에 대 한 기본 인라인 경험 합니다. 다른 모든 받는 사람 (다운로드 또는 app 필요 없음) OME 포털에서 메시지를 읽을 수 있습니다.|
|*첨부 파일 사용 권한*           |첨부 파일에 대 한 제한 없음|첨부 파일 보호|첨부 파일 전달 하지 않음 옵션 및 사용자 지정 서식 파일에 대 한 보호 됩니다. 관리자는 암호화 전용 옵션에 대 한 첨부 파일 또는 하지 보호 되는지 여부를 선택할 수 있습니다.|
|*가져올 사용자 고유의 키 (BYOK) 지원*|없음                |없음               |BYOK 지원          |
||

## <a name="advantages-of-using-the-new-ome-capabilities-over-legacy-ome"></a>레거시 OME을 통해 새 OME 기능을 사용할 때의 장점

새로운 기능 다음과 같은 이점을 제공합니다.

- 사용 하는 기능 암호화 전용 (보안 공동 작업 수)를 전달 하지 않음,으로 사용자 지정 제한 합니다.
- 보낸 사람은 Outlook 데스크톱, Outlook for Mac 및 웹 클라이언트에서 Outlook에서 수동으로 새 기능을 사용 하 여 암호화 된 메일을 보낼 수 있습니다.
- Office 365 받는 사람에 게 지원 되는 Outlook 클라이언트에서 인라인 경험을 사용 하 여 가져옵니다. 또는 관리자는 브랜딩된 환경을 Office 365 받는 사람에 게 표시 하도록 선택할 수 있습니다.
- Office 365 외부에서 Gmail, yahoo 및 Microsoft 계정과 같은 계정은 이러한 받는 사람에 대 한 더 나은 사용자 환경을 제공 하는 OME 포털과 페더레이션 사용자. 다른 모든 id 일회용 암호를를 사용 하 여 암호화 된 메시지에 액세스할 수 있습니다.
- 관리자는 브랜딩, 사용자 지정 하 고 여러 브랜딩 서식 파일을 만들 수 있습니다.
- 관리자는 새로운 기능을 사용 하 여 암호화 된 전자 메일을 해지할 수 있습니다.
- 보안을 통해 자세한 사용 현황 보고서를 제공 하는 새로운 기능 &amp; 준수 센터입니다.

## <a name="coexistence-of-legacy-ome-and-the-new-capabilities-in-the-same-tenant"></a>레거시 OME과 동일한 테 넌 트의 새로운 기능의 동시 사용

동일한 테 넌 트에 레거시 OME와 새 기능을 사용할 수 있습니다. 관리자로 서 이렇게 하면 사용자의 메일 흐름 규칙을 만들 때 사용 하 여 원하는 OME의 버전을 선택 하 여 합니다.

- OME의 레거시 버전을 지정 하려면 Exchange 메일 흐름 규칙 작업 "OME의 이전 버전을 적용 하는 경우"를 사용 합니다.
- 새로운 기능을 지정 하려면 Exchange 메일 흐름 규칙 작업 "적용 Office 365 메시지 암호화 및 권한 보호"를 사용 합니다.

사용자가 Outlook 데스크톱, Outlook for Mac 및 웹 클라이언트에서 Outlook에서 수동으로 새 기능을 사용 하 여 암호화 된 메일을 보낼 수도 있습니다.

## <a name="migrating-from-legacy-ome-to-the-new-capabilities"></a>레거시 OME에서 새로운 기능으로 마이그레이션

OME의 두 버전 모두 공존할 수 있는 경우에 좋습니다를 편집 하는 규칙 동작을 사용 하는 이전 메일 흐름 규칙 "OME의 이전 버전을 적용" 메일 흐름 규칙 작업 "적용 Office 365 메시지 암호화를 지정 하 여 새 기능을 사용 하려면 하 고 보호 권한 "합니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.

## <a name="getting-started-with-ome"></a>OME 시작 하기

일반적으로 새 OME 기능 Office 365 조직에 대해 자동으로 활성화 됩니다. 조직 내에서 새 OME 기능을 사용 하 여 시작 준비가 된 것을 하는 경우 [새로운 Office 365 메시지 암호화 기능을 설정](set-up-new-message-encryption-capabilities.md)참조 하십시오.

OME의 레거시 버전은 Azure 정보 보호 하도록 설정한 경우 Office 365 조직에 대해 자동으로 활성화 됩니다. 과거에는 레거시 OME Azure 정보 보호 설정 되지 않은 경우에 작동 합니다. 이 대/소문자 더이상 합니다.

Azure 정보 보호 하도록 설정한 경우에 레거시 OME를 사용 하 여를 시작 하려면 "OME의 이전 버전을 적용 하는 경우" 규칙 동작을 사용 하는 메일 흐름 규칙을 구성 하기만 하면 됩니다. 자세한 내용은 [Office 365에서 전자 메일 메시지를 암호화 메일 흐름 규칙 정의](define-mail-flow-rules-to-encrypt-email.md)참조 하십시오.