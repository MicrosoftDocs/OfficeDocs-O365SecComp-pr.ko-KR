---
title: Set up Information Rights Management (IRM) in SharePoint admin center
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: Sharepoint 목록 및 문서 라이브러리를 보호 하기 위해 Microsoft Azure Active Directory RMS (권한 관리 서비스)를 통해 SharePoint Online IRM을 사용 하는 방법을 알아봅니다.
ms.openlocfilehash: 16a76ecda37bd5480285dd70670843a88198bdb7
ms.sourcegitcommit: a97e7da9a1f870540f0bdcba7be5fb6f8bd12f74
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35756850"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a>Set up Information Rights Management (IRM) in SharePoint admin center

## <a name="introduction"></a>소개

SharePoint Online 내에서 IRM 보호는 목록 및 라이브러리 수준의 파일에 적용 됩니다. 조직에서 IRM 보호를 사용 하려면 먼저 권한 관리를 설정 해야 합니다. IRM은 azure Information Protection의 Azure 권한 관리 서비스에 의존 하 여 사용 제한을 암호화 및 할당 합니다. 일부 Office 365 계획에는 Azure 권한 관리 등이 포함 됩니다. 자세한 내용은 [Office 응용 프로그램 및 서비스에서 Azure 권한 관리를 지 원하는 방법을](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support)읽어 보세요.
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a>SharePoint 관리 센터를 사용 하 여 IRM 서비스 설정

조직에서 SharePoint 목록 및 라이브러리를 IRM으로 보호 하기 전에 먼저 조직에 대 한 권한 관리 서비스를 활성화 해야 합니다. 자세한 내용은 [Azure 권한 관리 활성화](https://docs.microsoft.com/information-protection/deploy-use/activate-service)를 참조 하세요. 권한 관리 서비스를 사용 하도록 설정 하려면 Office 365 전역 관리자 권한이 있는 회사 또는 학교 계정을 사용 해야 합니다. 그렇지 않으면 SharePoint Online에서 IRM 기능을 사용할 수 없게 됩니다.
  
권한 관리 서비스를 활성화 한 후 SharePoint 관리 센터에 로그인 하 여 IRM을 설정 합니다.
  
1. 전역 관리자 또는 SharePoint 관리자 Office 365에 로그인합니다.
    
2. 앱 시작 관리자 아이콘 ![을 선택 하 고 왼쪽 위의 office 365](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) 에서 앱 시작 관리자 아이콘을 선택한 다음 **관리자** 를 선택 하 여 office 365 관리 센터를 엽니다. (If you don't see the Admin tile, you don't have Office 365 administrator permissions in your organization.) 
    
3. 왼쪽 창에서 **관리 센터** \> **SharePoint**를 선택 합니다.
    
4. 왼쪽 창에서 **설정을**선택 하 고 **클래식 설정 페이지**를 선택 합니다.
    
5. **Irm (정보 권한 관리** ) 섹션에서 **구성에 지정 된 IRM 서비스 사용**을 선택 하 고 **IRM 설정 새로 고침**을 선택 합니다. IRM 설정을 새로 고치면 조직의 사용자가 SharePoint 목록 및 문서 라이브러리에서 IRM 사용을 시작할 수 있습니다. 그러나 라이브러리 설정 및 목록 설정에 표시 되는 데 최대 1 시간이 걸릴 수 있습니다.
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a>IRM 사용 SharePoint 문서 라이브러리 및 목록
<a name="__toc220831191"> </a>

IRM 설정을 새로 고치면 사이트 소유자가 SharePoint 목록 및 문서 라이브러리를 IRM으로 보호할 수 있습니다. 자세한 내용은 [목록 또는 라이브러리에 정보 권한 관리 적용](apply-irm-to-a-list-or-library.md)을 참조 하십시오.
  
사이트 소유자가 목록 또는 라이브러리에 대해 IRM을 사용 하도록 설정 하면 해당 목록이 나 라이브러리에서 지원 되는 파일 형식을 보호할 수 있습니다. 라이브러리에 대해 IRM을 사용 하도록 설정 된 경우 권한 관리는 해당 라이브러리의 모든 파일에 적용 됩니다. 목록에 대해 IRM을 사용 하도록 설정 하는 경우, 권한 관리는 실제 목록 항목이 아니라 목록 항목에 첨부 된 파일에만 적용 됩니다.
  
사용자가 IRM 사용 목록 또는 라이브러리에서 파일을 다운로드 하는 경우 파일은 인증 된 사용자만 볼 수 있도록 암호화 됩니다. 각 권한 관리 파일에는 해당 파일을 보는 사용자에 게 제한을 적용 하는 발급 라이선스도 포함 되어 있습니다. 일반적인 제한 사항에는 파일 읽기 전용, 텍스트 복사 사용 안 함, 사용자가 로컬 복사본을 저장 하지 못하도록 방지, 사용자가 파일을 인쇄 하지 못하게 하는 등이 포함 됩니다. IRM 지원 파일 형식을 읽을 수 있는 클라이언트 프로그램은 권한 관리 파일 내에서 발급 라이선스를 사용 하 여 이러한 제한을 적용 합니다. 이는 권한 관리 파일이 다운로드 된 후에도 해당 파일의 보호를 유지 하는 방법입니다. 목록 또는 라이브러리에 대해 IRM을 사용 하도록 설정 하려면 [목록 또는 라이브러리에 정보 권한 관리 적용](apply-irm-to-a-list-or-library.md)을 참조 하십시오.
  
Office Online을 사용 하 여 IRM 사용 라이브러리에서는 문서를 만들거나 편집할 수 없습니다. 대신 한 번에 한 명의 사용자가 IRM으로 암호화 된 파일을 다운로드 하 고 편집할 수 있습니다. 체크 인 및 체크 아웃을 사용 하 여 *공동 작성* 을 관리 하거나 여러 사용자에 대해 제작 합니다. 
  
IRM으로 보호 된 라이브러리에서 PDF 파일을 다운로드 하면 Office 365에서 보호 된 PDF 파일을 만듭니다. 파일 확장명은 변경 되지 않지만 파일은 보호 됩니다. 이 파일을 보려면 Azure Information Protection 뷰어, 전체 Azure Information Protection 클라이언트 또는 보호 된 PDF 파일 보기를 지 원하는 다른 응용 프로그램이 필요 합니다. 
  
SharePoint Online에서는 다음과 같은 파일 형식에 대 한 암호화를 지원 합니다.
  
- PDF
    
- 다음 Microsoft Office 프로그램에 대 한 97-2003 파일 형식: Word, Excel 및 PowerPoint
    
- 다음 Microsoft Office 프로그램의 Office Open XML 형식: Word, Excel 및 PowerPoint
    
- XPS (XML Paper Specification) 형식
    
## <a name="next-steps"></a>다음 단계
<a name="__toc220831191"> </a>

SharePoint Online에 대해 IRM을 사용 하도록 설정한 후에는 목록 및 라이브러리에 대 한 권한 관리 적용을 시작할 수 있습니다. 자세한 내용은 [목록 또는 라이브러리에 정보 권한 관리 적용](apply-irm-to-a-list-or-library.md)을 참조 하십시오.
  
이제 Windows 용 새 OneDrive 동기화 클라이언트는 IRM으로 보호 된 SharePoint 문서 라이브러리 및 OneDrive 위치 동기화를 지원 합니다 (라이브러리의 IRM 설정이 만료 문서 액세스 권한으로 설정 되어 있지 않은 경우). 자세한 내용을 보거나 새 동기화 클라이언트 배포를 시작 하려면 [Windows 용 새 OneDrive 동기화 클라이언트 배포](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668)를 참조 하세요.
  
[Top of page](#introduction)  

