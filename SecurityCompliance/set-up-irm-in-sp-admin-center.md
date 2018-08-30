---
title: SharePoint 관리 센터에서 정보 권한 관리 (IRM)를 설정
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: SharePoint Online IRM을 통해 Microsoft Azure Active Directory 서비스 RMS (권한 관리)를 사용 하 여 SharePoint 목록 및 문서 라이브러리를 보호 하는 방법에 알아봅니다.
ms.openlocfilehash: dea8c71ce67207b3c40a1f934f90e63740f70f29
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533500"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a><span data-ttu-id="06db7-103">SharePoint 관리 센터에서 정보 권한 관리 (IRM)를 설정</span><span class="sxs-lookup"><span data-stu-id="06db7-103">Set up Information Rights Management (IRM) in SharePoint admin center</span></span>

<span data-ttu-id="06db7-p101">SharePoint Online에서 IRM 보호 목록 및 라이브러리 수준에서 파일에 적용 됩니다. 조직에서 IRM 보호를 사용할 수 있으려면 먼저 권한 관리를 설정 해야 합니다. IRM은 Azure 정보 보호를 암호화 하 여 사용 현황 제한 할당에서 Azure 권한 관리 서비스에 의존 합니다. 일부 Office 365 계획 Azure 권한 관리에만 포함 합니다. 자세한 내용을 보려면 [어떻게 Office 응용 프로그램 및 서비스 Azure 권한 관리를 지 원하는](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support)읽습니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-p101">Within SharePoint Online, IRM protection is applied to files at the list and library level. Before your organization can use IRM protection, you must first set up Rights Management. IRM relies on the Azure Rights Management service from Azure Information Protection to encrypt and assign usage restrictions. Some Office 365 plans include Azure Rights Management, but not all. To learn more, read [How Office applications and services support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support).</span></span>
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a><span data-ttu-id="06db7-109">SharePoint 관리 센터를 사용 하 여 IRM 서비스 설정</span><span class="sxs-lookup"><span data-stu-id="06db7-109">Turn on IRM service using SharePoint admin center</span></span>

<span data-ttu-id="06db7-p102">조직에는 IRM으로 보호 하는 SharePoint 목록 및 라이브러리 수, 전에 먼저 조직에 대 한 권한 관리 서비스를 활성화 해야 합니다. 자세한 방법을 [Azure 권한 관리 활성화](https://docs.microsoft.com/information-protection/deploy-use/activate-service)를 참조 하십시오. 권한 관리 서비스를 사용 하도록 설정 하려면 Office 365 전역 관리자 권한이 있는 작업이 나 교육용 계정을 사용 해야 합니다. 그렇지 않은 경우, SharePoint Online을 사용한 IRM 기능을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-p102">Before your organization can IRM-protect SharePoint lists and libraries, you must first activate the Rights Management service for your organization. To learn how see [Activating Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/activate-service). You must use a work or school account that has Office 365 global administrator privileges to enable the Rights Management service. Otherwise, you won't be able to use IRM features with SharePoint Online.</span></span>
  
<span data-ttu-id="06db7-114">권한 관리 서비스를 활성화 한 후 SharePoint 관리 센터에 로그인 IRM를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-114">After activating the Rights Management service, sign in to the SharePoint admin center to turn on IRM.</span></span>
  
1. <span data-ttu-id="06db7-115">전역 관리자 또는 SharePoint 관리자 Office 365에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-115">Sign in to Office 365 as a global admin or SharePoint admin.</span></span>
    
2. <span data-ttu-id="06db7-p103">왼쪽 위의 ![Office 365에서 앱 시작 관리자 아이콘](media/e5aee650-c566-4100-aaad-4cc2355d909f.png)을 선택하고 **관리자**를 선택해 Office 365 관리 센터를 엽니다. (관리자 타일이 표시 되지 않으면 조직에서 Office 365 관리자 권한이 없는 상태입니다.)</span><span class="sxs-lookup"><span data-stu-id="06db7-p103">Select the app launcher icon ![The app launcher icon in Office 365](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) in the upper-left and choose **Admin** to open the Office 365 admin center. (If you don't see the Admin tile, you don't have Office 365 administrator permissions in your organization.)</span></span> 
    
3. <span data-ttu-id="06db7-118">왼쪽된 창에서 **관리 센터** 를 선택 \> **SharePoint**합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-118">In the left pane, choose **Admin centers** \> **SharePoint**.</span></span>
    
4. <span data-ttu-id="06db7-119">왼쪽된 창에서 **설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-119">In the left pane, choose **settings**.</span></span>
    
5. <span data-ttu-id="06db7-p104">**정보 권한 관리 (IRM)** 섹션에서 **구성에 지정 된 IRM 서비스를 사용 하 여**를 선택한 다음 **IRM 설정을 새로 고칠**를 선택 합니다. IRM 설정을 새로 고치면, 조직의 사용자가 SharePoint 목록 및 문서 라이브러리에 IRM을 사용 하 여 시작할 수 있습니다. 그러나 이렇게 하는 옵션을 최대 걸릴 수 있습니다 1 시간에 라이브러리 설정 및 목록 설정에 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-p104">In the **Information Rights Management (IRM)** section, choose **Use the IRM service specified in your configuration**, and then choose **Refresh IRM Settings**. After you refresh IRM settings, people in your organization can begin using IRM in their SharePoint lists and document libraries. However, the options to do so may take up to an hour to appear in Library Settings and List Settings.</span></span>
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a><span data-ttu-id="06db7-123">IRM 사용 SharePoint 문서 라이브러리 및 목록</span><span class="sxs-lookup"><span data-stu-id="06db7-123">IRM-enable SharePoint document libraries and lists</span></span>
<span data-ttu-id="06db7-124"><a name="__toc220831191"> </a></span><span class="sxs-lookup"><span data-stu-id="06db7-124"></span></span>

<span data-ttu-id="06db7-p105">IRM 설정을 새로 고친 후 사이트 소유자가 SharePoint 목록 IRM으로 보호 수 및 문서 라이브러리입니다. 자세한 내용은 [목록이 나 라이브러리에 정보 권한 관리 적용](apply-irm-to-a-list-or-library.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06db7-p105">After refreshing IRM settings, site owners can IRM-protect their SharePoint lists and document libraries. For more information, see [Apply Information Rights Management to a list or library](apply-irm-to-a-list-or-library.md).</span></span>
  
<span data-ttu-id="06db7-p106">목록 또는 라이브러리에 IRM을 사용 하는 사이트 소유자 때 해당 목록이 나 라이브러리의 모든 지원 되는 파일 형식을 보호할 수 있습니다. 라이브러리에 대 한 IRM 사용 하는 경우 권한 관리에는 해당 라이브러리에 파일을 모두에 적용 됩니다. 목록에 대 한 IRM을 사용 하도록 설정 하는 경우에 권한 관리 실제 목록 항목이 아닌 목록 항목에 연결 된 파일에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-p106">When site owners enable IRM for a list or library, they can protect any supported file types in that list or library. When IRM is enabled for a library, rights management applies to all of the files in that library. When you enable IRM for a list, rights management applies only to files that are attached to list items, not the actual list items.</span></span>
  
<span data-ttu-id="06db7-p107">사용자는 IRM 사용이 가능한 목록 또는 라이브러리의 파일을 다운로드 하는 경우 권한이 부여 된 사용자만 볼 수 있도록 파일 암호화 됩니다. 권한이 관리 되는 각 파일에는 파일을 보는 사용자에 대 한 제한 사항을 적용 하는 한 발급 라이선스를 들어 있습니다. 일반적인 제한 사항으로 파일을 읽기 전용, 로컬 복사본을 저장 하 고 사용자 파일 인쇄 하지 못하도록 방지에서 사용자를 방지 하 여 텍스트를 복사 하는 사용 하지 않도록 설정 합니다. IRM 지원 되는 파일 형식에서 읽을 수 있는 클라이언트 프로그램 권한 관리 파일 내에서 발급 라이선스를 사용 하 여 이러한 제한 사항을 적용 합니다. 다운로드 된 후에 권한 관리 파일의 보호를 유지 하는 방법입니다. 목록 또는 라이브러리에 IRM을 사용 하려면 [목록 또는 라이브러리에 정보 권한 관리 적용](apply-irm-to-a-list-or-library.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06db7-p107">When people download files in an IRM-enabled list or library, the files are encrypted so that only authorized people can view them. Each rights-managed file also contains an issuance license that imposes restrictions on the people who view the file. Typical restrictions include making a file read-only, disabling the copying of text, preventing people from saving a local copy, and preventing people from printing the file. Client programs that can read IRM-supported file types use the issuance license within the rights-managed file to enforce these restrictions. This is how a rights-managed file retains its protection even after it is downloaded. To enable IRM on a list or library, see [Apply Information Rights Management to a list or library](apply-irm-to-a-list-or-library.md).</span></span>
  
<span data-ttu-id="06db7-p108">만들기 또는 Office Online을 사용 하는 IRM 사용이 가능한 라이브러리에서 문서를 편집할 수는 없습니다. 대신 한번에 한 명의 대화 상대를 다운로드 하 고 IRM으로 암호화 된 파일을 편집할 수 있습니다. 체크인 및 체크아웃 *공동 작성* , 관리 또는 여러 사용자 간에 제작에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-p108">You cannot create or edit documents in an IRM-enabled library using Office Online. Instead, one person at a time can download and edit IRM-encrypted files. Use check-in and check-out to manage  *co-authoring*  , or authoring across multiple users.</span></span> 
  
<span data-ttu-id="06db7-p109">IRM으로 보호 된 라이브러리에서 PDF 파일을 다운로드 하는 경우 Office 365 보호 된 PDF 파일을 만듭니다. 파일의 확장명 변경 되지 않습니다 있지만 파일은 보호 합니다. 이 파일을 보려면 Azure 정보 보호 뷰어를 전체 Azure 정보 보호 클라이언트에서 수행 해야 또는 보호 된 PDF 파일의 보기를 지 원하는 다른 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-p109">When you download a PDF file from an IRM-protected library, Office 365 creates a protected PDF file. The file's extension won't change, but the file is protected. To view this file you'll need the Azure Information Protection viewer, the full Azure Information Protection client, or another application that supports viewing protected PDF files.</span></span> 
  
<span data-ttu-id="06db7-142">SharePoint Online에서는 다음 파일 형식의 암호화를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06db7-142">SharePoint Online supports encryption of the following file types:</span></span>
  
- <span data-ttu-id="06db7-143">PDF</span><span class="sxs-lookup"><span data-stu-id="06db7-143">PDF</span></span>
    
- <span data-ttu-id="06db7-144">다음 Microsoft Office 프로그램에 대 한 97-2003 파일 형식: Word, Excel 및 PowerPoint</span><span class="sxs-lookup"><span data-stu-id="06db7-144">The 97-2003 file formats for the following Microsoft Office programs: Word, Excel, and PowerPoint</span></span>
    
- <span data-ttu-id="06db7-145">다음 Microsoft Office 프로그램에 대 한 Office Open XML 형식: Word, Excel 및 PowerPoint</span><span class="sxs-lookup"><span data-stu-id="06db7-145">The Office Open XML formats for the following Microsoft Office programs: Word, Excel, and PowerPoint</span></span>
    
- <span data-ttu-id="06db7-146">XML Paper Specification (XPS) 형식</span><span class="sxs-lookup"><span data-stu-id="06db7-146">The XML Paper Specification (XPS) format</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="06db7-147">다음 단계</span><span class="sxs-lookup"><span data-stu-id="06db7-147">Next steps</span></span>
<span data-ttu-id="06db7-148"><a name="__toc220831191"> </a></span><span class="sxs-lookup"><span data-stu-id="06db7-148"></span></span>

<span data-ttu-id="06db7-p110">SharePoint Online에 대 한 IRM 사용 했으면, 목록 및 라이브러리에 권한 관리 적용을 시작할 수 있습니다. 내용은 [목록이 나 라이브러리에 정보 권한 관리 적용](apply-irm-to-a-list-or-library.md)을 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06db7-p110">Once you've enabled IRM for SharePoint Online, you can start applying rights management to lists and libraries. For information, see [Apply Information Rights Management to a list or library](apply-irm-to-a-list-or-library.md).</span></span>
  
<span data-ttu-id="06db7-p111">Windows 용 새 OneDrive 동기화 클라이언트는 이제 동기화 (영문) IRM으로 보호 된 SharePoint 문서 라이브러리와 OneDrive 위치 (으로 라이브러리에 대 한 IRM 설정을 문서 액세스 권한이 만료 되도록 설정 되지 않습니다)을 지원 합니다. 자세한 내용은 또는 새 동기화 클라이언트 배포를 시작 하려면 [Windows에 대 한 새 OneDrive 동기화 클라이언트 배포](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668)를 참조 하십시오.</span><span class="sxs-lookup"><span data-stu-id="06db7-p111">The new OneDrive sync client for Windows now supports synchronizing IRM-protected SharePoint document libraries and OneDrive locations (as long as the IRM setting for the library isn't set to expire document access rights). For more information, or to get started deploying the new sync client, see [Deploy the new OneDrive sync client for Windows](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668).</span></span>
  
[<span data-ttu-id="06db7-153">페이지의 위쪽</span><span class="sxs-lookup"><span data-stu-id="06db7-153">Top of Page</span></span>](set-up-irm-in-sp-admin-center.md#__top)
  

