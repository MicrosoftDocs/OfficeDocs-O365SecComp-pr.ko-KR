---
title: 위임된 관리 FAQ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: 이 항목에서는 다른 테넌트(회사)에 대한 EOP(Exchange Online Protection)를 관리하는 능력을 비롯하여 위임 받은 Office 365 관리 작업을 수행하려는 Microsoft 파트너 및 리셀러를 위한 질문과 답변이 제공됩니다.
ms.openlocfilehash: b6096e835f90a0d5f22a39a5df76e52f1a25a79d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027495"
---
# <a name="delegated-administration-faq"></a>위임된 관리 FAQ

이 항목에서는 다른 테넌트(회사)에 대한 EOP(Exchange Online Protection)를 관리하는 능력을 비롯하여 위임 받은 Office 365 관리 작업을 수행하려는 Microsoft 파트너 및 리셀러를 위한 질문과 답변이 제공됩니다.
  
 **Q. 저는 재판매인이고 고객의 테넌트를 관리해야 합니다. 이 작업은 어떻게 수행해야 합니까?**
  
A. Microsoft 파트너이거나 재판매인일 경우 그리고 Microsoft 관리자가 되기 위해 등록한 경우 사용 권한을 요청하여 Office 365 관리 센터에서 테넌트를 관리할 수 있습니다. 이를 위임된 관리하고 하며, 이를 통해 조직의 관리자처럼 Office 365 테넌트(EOP 설정 포함)를 관리할 수 있습니다. 위임된 관리를 수행하는 단계는 다음과 같습니다.
  
1. [Microsoft Office 365 관리자](https://aka.ms/cloudbenefits)로 등록합니다.
    
2. Office 365 위임된 관리에 등록합니다. 고객의 계정을 관리할 수 있으려면 위임된 관리자로서 승인을 받아야 합니다. 승인을 받으려면 먼저 [위임된 관리를 위한 제안을 고객에게 보냅니다](https://go.microsoft.com/fwlink/?LinkId=396829). 나중에 고객에게 위임된 관리를 제안할 수도 있습니다. 
    
3. [위임된 관리 추가 또는 삭제](https://go.microsoft.com/fwlink/?LinkId=396831)에 설명된 단계에 따라 위임된 관리 계정을 만듭니다.
    
Office 365 위임된 관리 설정 방법에 대한 자세한 내용은 [파트너: 비즈니스 창출 및 Office 365 파트너 계정 관리](https://go.microsoft.com/fwlink/?LinkId=301485) 를 참조하세요. 
  
 **Q. 저는 재판매인이 아니라 고객입니다. 하위 테넌트를 위해 위임된 관리를 설정하려면 어떻게 합니까?**
  
A. 위임된 관리는 현재 재판매인 및 파트너만 사용할 수 있습니다. 그렇지만 하위 테넌트(회사)에 정책을 적용하는 데 도움이 되는 샘플 Windows PowerShell 스크립트를 제공해 드립니다. 자세한 내용은 [여러 테넌트에 EOP 설정을 적용하기 위한 샘플 스크립트](sample-script-for-applying-eop-settings-to-multiple-tenants.md)를 참조하세요.
  
 **Q. 하위 테넌트 관리자가 정책을 수정하지 못하게 하려면 어떻게 합니까?**
  
A. Office 365는 현재 이 기능을 지원하지 않습니다.
  
 **Q. 모든 하위 테넌트의 보고를 통합하려면 어떻게 합니까?**
  
A. 관리하는 회사의 보고 기능 통합을 현재 Office 365 관리 센터에서는 사용할 수 없습니다. 그렇지만 원격 Windows PowerShell 또는 [보고 웹 서비스](https://go.microsoft.com/fwlink/?LinkId=279926)를 통해서는 이 작업을 수행할 수 있습니다. 
  

