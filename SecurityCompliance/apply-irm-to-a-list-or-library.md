---
title: 목록 또는 라이브러리에 IRM (정보 권한 관리) 적용
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
ms.collection:
- M365-security-compliance
description: IRM (정보 권한 관리)을 사용 하 여 목록 또는 라이브러리에서 다운로드 한 파일을 제어 하 고 보호 하는 데 도움을 받을 수 있습니다.
ms.openlocfilehash: ae07136cf128f167695f667cc8a149492287f498
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220418"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a><span data-ttu-id="37ce7-103">목록 또는 라이브러리에 IRM (정보 권한 관리) 적용</span><span class="sxs-lookup"><span data-stu-id="37ce7-103">Apply Information Rights Management (IRM) to a list or library</span></span>

<span data-ttu-id="37ce7-104">IRM (정보 권한 관리)을 사용 하 여 목록 또는 라이브러리에서 다운로드 한 파일을 제어 하 고 보호 하는 데 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-104">You can use Information Rights Management (IRM) to help control and protect files that are downloaded from lists or libraries.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="37ce7-105">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="37ce7-105">Before you begin</span></span>

- <span data-ttu-id="37ce7-p101">azure information Protection에서 azure rms (권한 관리 서비스) 및 온-프레미스에 해당 하는 AD rms (Active Directory rights management Services)는 사이트에 대 한 정보 권한 관리를 지원 합니다. 별도의 설치 또는 추가 설치가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p101">The Azure Rights Management service (Azure RMS) from Azure Information Protection, and the on-premises equivalent, Active Directory Rights Management Services (AD RMS), support Information Rights Management for sites. No separate or additional installations are required.</span></span>
    
- <span data-ttu-id="37ce7-108">목록이 나 라이브러리에 IRM을 적용 하기 전에 먼저 사이트 관리자가이를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-108">Before you apply IRM to a list or library it must first be enabled by an administrator for your site.</span></span>
    
- <span data-ttu-id="37ce7-109">목록이 나 라이브러리에 IRM을 적용 하려면 해당 목록 또는 라이브러리에 대 한 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-109">To apply IRM to a list or library, you must have administrator permissions for that list or library.</span></span>
    
- <span data-ttu-id="37ce7-p102">SharePoint Online을 사용 하는 경우 더 큰 IRM으로 보호 된 파일을 다운로드할 때 시간 초과가 발생할 수 있습니다. 이 경우 Office 프로그램을 사용 하 여 irm 보호를 적용 하 고 더 큰 파일을 irm을 사용 하지 않는 SharePoint 라이브러리에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p102">If you are using SharePoint Online, your users might experience timeouts when downloading larger IRM-protected files. If this happens, then apply IRM protection by using your Office programs, and store larger files in a SharePoint library that does not use IRM.</span></span>
    
> [!NOTE]
> <span data-ttu-id="37ce7-112">SharePoint server 2013을 사용 하는 경우 서버 관리자는 IRM을 사용 하 여 조직의 사용자가 보호할 모든 파일 형식에 대해 모든 프런트 엔드 웹 서버에 보호기를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-112">If you're using SharePoint Server 2013, a server administrator must install protectors on all front-end Web servers for every file type that the people in your organization want to protect by using IRM.</span></span> 
  
## <a name="apply-irm-to-a-list-or-library"></a><span data-ttu-id="37ce7-113">목록 또는 라이브러리에 IRM 적용</span><span class="sxs-lookup"><span data-stu-id="37ce7-113">Apply IRM to a list or library</span></span>
<span data-ttu-id="37ce7-114"><a name="__toc256598179"> </a></span><span class="sxs-lookup"><span data-stu-id="37ce7-114"></span></span>

![정보 권한 관리 설정](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. <span data-ttu-id="37ce7-116">IRM을 구성할 목록 또는 라이브러리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-116">Go to the list or library for which you want to configure IRM.</span></span>
    
2. <span data-ttu-id="37ce7-p103">리본 메뉴에서 **라이브러리** 탭을 클릭 한 다음 **라이브러리 설정을**클릭 합니다. 목록에서 작업 하는 경우 **목록** 탭을 클릭 한 다음 **목록 설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p103">On the ribbon, click the **Library** tab, and then click **Library Settings**. (If you are working in a list, click the **List** tab, and then click **List Settings**).</span></span>
    
    ![리본의 SharePoint 라이브러리 설정 단추](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. <span data-ttu-id="37ce7-p104">**사용 권한 및 관리**에서 **정보 권한 관리**를 클릭 합니다. 정보 권한 관리 링크가 나타나지 않으면 사이트에 IRM을 사용 하도록 설정 하지 않은 것일 수 있습니다. 서버 관리자에 게 문의 하 여 사이트에 대해 IRM을 사용 하도록 설정 하는 것이 가능한 것인지 확인 합니다. 그림 라이브러리에 대해서는 정보 권한 관리 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p104">Under **Permissions and Management**, click **Information Rights Management**. If the Information Rights Management link does not appear, IRM might not be enabled for your site. Contact your server administrator to see if it is possible to enable IRM for your site. The Information Rights Management link does not appear for picture libraries.</span></span>
    
4. <span data-ttu-id="37ce7-124">**정보 권한 관리 설정** 페이지에서이 목록 또는 라이브러리에서 다운로드 한 문서에 제한 된 사용 권한을 적용 하려면 **다운로드 시이 라이브러리의 문서에 대 한 사용 권한 제한** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-124">On the **Information Rights Management Settings** page, select the **Restrict permission to documents in this library on download** check box to apply restricted permission to documents that are downloaded from this list or library.</span></span> 
    
5. <span data-ttu-id="37ce7-p105">**사용 권한 정책 제목 만들기** 상자에 나중에이 정책을 다른 정책과 구분 하는 데 사용할 수 있는 정책에 대 한 설명이 포함 된 이름을 입력 합니다. 예를 들어 회사 문서가 기밀 문서를 포함 하는 목록이 나 라이브러리에 제한 된 사용 권한을 적용 하는 경우 **회사 기밀** 을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p105">In the **Create a permission policy title** box, type a descriptive name for the policy that you can use later to differentiate this policy from other policies. For example, you can type **Company Confidential** if you are applying restricted permission to a list or library that will contain company documents that are confidential.</span></span> 
    
6. <span data-ttu-id="37ce7-p106">**권한 정책 설명 추가** 상자에이 목록 또는 라이브러리의 문서를 처리 하는 방법을 설명 하는이 목록이 나 라이브러리를 사용 하는 사용자에 게 표시 되는 설명을 입력 합니다. 예를 들어 내부 직원에 게 이러한 문서의 정보에 대 한 액세스를 제한 하려는 경우 **이 문서의 내용을 다른 직원과만 토론할** 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p106">In the **Add a permission policy description** box, type a description that will appear to people who use this list or library that explains how they should handle the documents in this list or library. For example, you can type **Discuss the contents of this document only with other employees** if you want to restrict access to the information in these documents to internal employees.</span></span> 
    
7. <span data-ttu-id="37ce7-129">이 목록 또는 라이브러리의 문서에 추가 제한을 적용 하려면 **옵션 표시**를 클릭 하 고 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-129">To apply additional restrictions to the documents in this list or library, click **Show Options**, and do any of the following:</span></span>
    
|<span data-ttu-id="37ce7-130">**이렇게 하려면 다음을 수행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="37ce7-130">**To do this:**</span></span>|<span data-ttu-id="37ce7-131">**다음을 수행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="37ce7-131">**Do this:**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37ce7-132">사용자가이 목록 또는 라이브러리에서 문서를 인쇄할 수 있도록 허용</span><span class="sxs-lookup"><span data-stu-id="37ce7-132">Allow people to print documents from this list or library</span></span>  <br/> |<span data-ttu-id="37ce7-133">**보는 사람에 게 인쇄 허용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-133">Select the **Allow viewers to print** check box.</span></span>  <br/> |
|<span data-ttu-id="37ce7-134">항목 보기 권한을 가진 사용자가 문서에 포함 된 코드 또는 매크로를 실행할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-134">Allow people with at least the View Items permission to run embedded code or macros on a document.</span></span>  <br/> |<span data-ttu-id="37ce7-135">**검토자가 다운로드 한 문서에 대해 작동 하도록 스크립트 및 화면 판독기를 실행 하도록 허용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-135">Select the **Allow viewers to run script and screen reader to function on downloaded documents** check box.</span></span>  <br/> <span data-ttu-id="37ce7-136">이 옵션을 선택 하면 사용자가 코드를 실행 하 여 문서 내용을 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-136">If you select this option, users could run code to extract the contents of a document.</span></span>           |
|<span data-ttu-id="37ce7-137">사용자가 특정 간격으로 자격 증명을 확인 하도록 요구 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-137">Require that people verify their credentials at specific intervals.</span></span>  <br/> <span data-ttu-id="37ce7-p107">특정 기간에만 콘텐츠에 대 한 액세스를 제한 하려면이 옵션을 선택 합니다. 이 옵션을 선택 하면 콘텐츠 액세스를 위한 사용자의 발급 라이선스가 지정 된 일 수 후에 만료 되며, 사용자는 자격 증명을 확인 하 고 새 복사본을 다운로드 하기 위해 서버로 돌아가야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p107">Select this option if you want to restrict access to content to a specified period of time. If you select this option, people's issuance licenses to access the content will expire after the specified number of days, and people will be required to return to the server to verify their credentials and download a new copy.</span></span>  <br/> |<span data-ttu-id="37ce7-140">**사용자가이 간격 (일)을 사용 하 여 자격 증명을 확인 해야 함** 확인란을 선택 하 고 문서를 볼 수 있는 기간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-140">Select the **Users must verify their credentials using this interval (days)** check box, and then specify the number of days for which you want the document to be viewable.</span></span>  <br/> |
| <span data-ttu-id="37ce7-141">사용자가 IRM을 지원 하지 않는 문서를이 목록 또는 라이브러리로 업로드 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-141">Prevent people from uploading documents that do not support IRM to this list or library.</span></span>  <br/>  <span data-ttu-id="37ce7-142">이 옵션을 선택 하면 사용자가 다음 파일 형식을 업로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-142">If you select this option, people will not be able to upload any of the following file types:</span></span>  <br/>  <span data-ttu-id="37ce7-143">모든 프런트 엔드 웹 서버에 해당 IRM 보호 장치가 설치 되어 있지 않은 파일 형식</span><span class="sxs-lookup"><span data-stu-id="37ce7-143">File types that do not have corresponding IRM protectors installed on all of the front-end Web servers.</span></span>  <br/>  <span data-ttu-id="37ce7-144">SharePoint Server 2010에서 암호를 해독할 수 없는 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-144">File types that SharePoint Server 2010 cannot decrypt.</span></span>  <br/>  <span data-ttu-id="37ce7-145">다른 프로그램에서 IRM으로 보호 되는 파일 형식</span><span class="sxs-lookup"><span data-stu-id="37ce7-145">File types that are IRM protected in another program</span></span>  <br/> |<span data-ttu-id="37ce7-146">**사용자가 IRM을 지원 하지 않는 문서를 업로드 하는 것을 허용** 하지 않음 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-146">Select the **Do not allow users to upload documents that do not support IRM** check box.</span></span>  <br/> |
|<span data-ttu-id="37ce7-147">특정 날짜에이 목록 또는 라이브러리에서 제한 된 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-147">Remove restricted permissions from this list or library on a specific date.</span></span>  <br/> |<span data-ttu-id="37ce7-148">**라이브러리에 대 한 액세스 제한 중지** 확인란을 선택 하 고 원하는 날짜를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-148">Select the **Stop restricting access to the library at** check box, and then select the date that you want.</span></span>  <br/> |
|<span data-ttu-id="37ce7-149">문서를 열 수 있는 라이선스가 있는 프로그램에 대 한 자격 증명이 캐시 되는 간격을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-149">Control the interval that credentials are cached for the program that is licensed to open the document.</span></span>  <br/> |<span data-ttu-id="37ce7-150">**그룹 보호 및 자격 증명 설정 간격**에서 자격 증명 캐시 간격 (일 수)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-150">In the **Set group protection and credentials interval**, enter theinterval for caching credentials in number of days.</span></span>  <br/> |
|<span data-ttu-id="37ce7-151">사용자가 같은 그룹의 구성원과 공유할 수 있도록 그룹 보호를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-151">Allow group protection so that users can share with members of the same group.</span></span>  <br/> |<span data-ttu-id="37ce7-152">**그룹 보호 허용**을 선택 하 고 그룹의 공유 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-152">Select **Allow group protection**, and enter the group's name for sharing.</span></span>  <br/> |
   
8. <span data-ttu-id="37ce7-153">원하는 옵션을 모두 선택 했으면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-153">After you finish selecting the options you want, click **OK**.</span></span>
  
## <a name="what-is-information-rights-management"></a><span data-ttu-id="37ce7-154">정보 권한 관리 란?</span><span class="sxs-lookup"><span data-stu-id="37ce7-154">What is Information Rights Management?</span></span>
<span data-ttu-id="37ce7-155"><a name="__toc256598175"> </a></span><span class="sxs-lookup"><span data-stu-id="37ce7-155"></span></span>

<span data-ttu-id="37ce7-p108">IRM (정보 권한 관리)을 사용 하면 사용자가 목록 또는 라이브러리에서 다운로드 한 파일에 대해 수행할 수 있는 작업을 제한할 수도 있습니다. IRM은 다운로드 한 파일을 암호화 하 고 이러한 파일의 암호를 해독할 수 있는 사용자 및 프로그램 집합을 제한 합니다. 또한 IRM은 파일을 읽을 수 있는 사용자의 권한을 제한 하 여 파일 복사본을 인쇄 하거나 복사본에서 텍스트를 복사 하는 등의 작업을 수행할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p108">Information Rights Management (IRM) enables you to limit the actions that users can take on files that have been downloaded from lists or libraries. IRM encrypts the downloaded files and limits the set of users and programs that are allowed to decrypt these files. IRM can also limit the rights of the users who are allowed to read files, so that they cannot take actions such as print copies of the files or copy text from them.</span></span>
  
<span data-ttu-id="37ce7-p109">목록이 나 라이브러리에서 IRM을 사용 하 여 중요 한 콘텐츠를 보급 하는 것을 제한할 수 있습니다. 예를 들어 문서 라이브러리를 만들어 선택한 마케팅 담당자와 함께 예정 된 제품에 대 한 정보를 공유 하는 경우 IRM을 사용 하 여 이러한 개인이이 콘텐츠를 회사의 다른 직원과 공유 하지 못하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p109">You can use IRM on lists or libraries to limit the dissemination of sensitive content. For example, if you are creating a document library to share information about upcoming products with selected marketing representatives, you can use IRM to prevent these individuals from sharing this content with other employees in the company.</span></span>
  
<span data-ttu-id="37ce7-p110">사이트에서 개별 파일이 아닌 전체 목록이 나 라이브러리에 IRM을 적용 합니다. 이를 통해 전체 문서 또는 파일 집합에 대 한 일관 된 수준의 보호를 보다 쉽게 보장할 수 있습니다. 따라서 조직은 기밀 또는 독점 정보의 사용 및 보급을 제어 하는 회사 정책을 적용 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p110">On a site, you apply IRM to an entire list or library, rather than to individual files. This makes it easier to ensure a consistent level of protection for an entire set of documents or files. IRM can thus help your organization to enforce corporate policies that govern the use and dissemination of confidential or proprietary information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37ce7-164">정보 권한 관리와 관련 된이 페이지의 정보는 Microsoft sharepoint server 2013 및 SharePoint server 2016 사용권 조항 계약에서 ' 정보 권한 관리 '를 참조 하는 모든 용어를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-164">The information on this page regarding Information Rights Management supersedes any terms that reference 'Information Rights Management' in any Microsoft SharePoint Server 2013 and SharePoint Server 2016 license term agreements.</span></span> 
  
### <a name="how-irm-can-help-protect-content"></a><span data-ttu-id="37ce7-165">IRM을 통해 콘텐츠를 보호 하는 방법</span><span class="sxs-lookup"><span data-stu-id="37ce7-165">How IRM can help protect content</span></span>
<span data-ttu-id="37ce7-166"><a name="__toc256598176"> </a></span><span class="sxs-lookup"><span data-stu-id="37ce7-166"></span></span>

<span data-ttu-id="37ce7-167">IRM을 사용 하면 제한 된 콘텐츠를 다음과 같은 방식으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-167">IRM helps to protect restricted content in the following ways:</span></span>
  
- <span data-ttu-id="37ce7-168">권한 있는 보기가 무단 사용을 위해 콘텐츠를 복사, 수정, 인쇄, 팩스 또는 복사 하 고 붙여 넣는 것을 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-168">Helps to prevent an authorized viewer from copying, modifying, printing, faxing, or copying and pasting the content for unauthorized use</span></span>
    
- <span data-ttu-id="37ce7-169">Microsoft Windows의 화면 인쇄 기능을 사용 하 여 권한 있는 사용자가 콘텐츠를 복사 하지 못하도록 방지 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-169">Helps to prevent an authorized viewer from copying the content by using the Print Screen feature in Microsoft Windows</span></span>
    
- <span data-ttu-id="37ce7-170">서버에서 다운로드 한 후에도 전자 메일로 콘텐츠를 전송 하는 경우 권한이 없는 사용자에 게 콘텐츠가 표시 되지 않도록 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-170">Helps to prevent an unauthorized viewer from viewing the content if it is sent in e-mail after it is downloaded from the server</span></span>
    
- <span data-ttu-id="37ce7-171">사용자가 자신의 자격 증명을 확인 하 고 콘텐츠를 다시 다운로드 해야 하는 지정 된 기간에 따라 콘텐츠에 대 한 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-171">Restricts access to content to a specified period of time, after which users must confirm their credentials and download the content again</span></span>
    
- <span data-ttu-id="37ce7-172">조직 내에서 콘텐츠의 사용 및 보급을 제어 하는 회사 정책을 적용 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-172">Helps to enforce corporate policies that govern the use and dissemination of content within your organization</span></span>
    
### <a name="how-irm-cannot-help-protect-content"></a><span data-ttu-id="37ce7-173">IRM을 통해 콘텐츠를 보호 하는 방법</span><span class="sxs-lookup"><span data-stu-id="37ce7-173">How IRM cannot help protect content</span></span>
<span data-ttu-id="37ce7-174"><a name="__toc256598177"> </a></span><span class="sxs-lookup"><span data-stu-id="37ce7-174"></span></span>

<span data-ttu-id="37ce7-175">IRM에서는 다음과 같은 제한 된 콘텐츠를 보호할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-175">IRM cannot protect restricted content from the following:</span></span>
  
- <span data-ttu-id="37ce7-176">트로이 목마, 키 입력로 거 및 특정 유형의 스파이웨어와 같은 악의적인 프로그램을 통한 지우기, 도난, 캡처 또는 전송</span><span class="sxs-lookup"><span data-stu-id="37ce7-176">Erasure, theft, capture, or transmission by malicious programs such as Trojan horses, keystroke loggers, and certain types of spyware</span></span>
    
- <span data-ttu-id="37ce7-177">컴퓨터 바이러스의 작업으로 인해 손실 또는 손상</span><span class="sxs-lookup"><span data-stu-id="37ce7-177">Loss or corruption because of the actions of computer viruses</span></span>
    
- <span data-ttu-id="37ce7-178">화면에 표시 된 콘텐츠를 수동으로 복사 하거나 다시 입력</span><span class="sxs-lookup"><span data-stu-id="37ce7-178">Manual copying or retyping of content from the display on a screen</span></span>
    
- <span data-ttu-id="37ce7-179">화면에 표시 되는 콘텐츠의 디지털 또는 영화 사진</span><span class="sxs-lookup"><span data-stu-id="37ce7-179">Digital or film photography of content that is displayed on a screen</span></span>
    
- <span data-ttu-id="37ce7-180">타사 화면 캡처 프로그램을 사용 하 여 복사</span><span class="sxs-lookup"><span data-stu-id="37ce7-180">Copying through the use of third-party screen-capture programs</span></span>
    
- <span data-ttu-id="37ce7-181">타사 화면 캡처 프로그램 또는 복사 하 여 붙여넣기 작업을 사용 하 여 콘텐츠 메타 데이터 (열 값) 복사</span><span class="sxs-lookup"><span data-stu-id="37ce7-181">Copying of content metadata (column values) through the use of third-party screen-capture programs or copy-and-paste action</span></span>
    
[<span data-ttu-id="37ce7-182">목록 또는 라이브러리에 정보 권한 관리 적용</span><span class="sxs-lookup"><span data-stu-id="37ce7-182">Apply Information Rights Management to a list or library</span></span>](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a><span data-ttu-id="37ce7-183">목록 및 라이브러리에 대 한 IRM 작동 방식</span><span class="sxs-lookup"><span data-stu-id="37ce7-183">How IRM works for lists and libraries</span></span>
<span data-ttu-id="37ce7-184"><a name="__toc256598178"> </a></span><span class="sxs-lookup"><span data-stu-id="37ce7-184"></span></span>

<span data-ttu-id="37ce7-p111">IRM 보호는 목록 또는 라이브러리 수준의 파일에 적용 됩니다. 라이브러리에 대해 IRM을 사용 하도록 설정 된 경우 권한 관리는 해당 라이브러리의 모든 파일에 적용 됩니다. 목록에 대해 IRM을 사용 하도록 설정 된 경우, 권한 관리는 실제 목록 항목이 아니라 목록 항목에 첨부 된 파일에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p111">IRM protection is applied to files at the list or library level. When IRM is enabled for a library, rights management applies to all of the files in that library. When IRM is enabled for a list, rights management applies only to files that are attached to list items, not the actual list items.</span></span>
  
<span data-ttu-id="37ce7-p112">사용자가 IRM 사용 목록 또는 라이브러리에서 파일을 다운로드 하는 경우 파일은 인증 된 사용자만 볼 수 있도록 암호화 됩니다. 각 권한 관리 파일에는 해당 파일을 보는 사용자에 게 제한을 적용 하는 발급 라이선스도 포함 되어 있습니다. 일반적인 제한 사항에는 파일 읽기 전용, 텍스트 복사 사용 안 함, 사용자가 로컬 복사본을 저장 하지 못하도록 방지, 사용자가 파일을 인쇄 하지 못하게 하는 등이 포함 됩니다. IRM 지원 파일 형식을 읽을 수 있는 클라이언트 프로그램은 권한 관리 파일 내에서 발급 라이선스를 사용 하 여 이러한 제한을 적용 합니다. 이는 권한 관리 파일이 서버에서 다운로드 된 후에도 해당 파일의 보호를 유지 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p112">When people download files in an IRM-enabled list or library, the files are encrypted so that only authorized people can view them. Each rights-managed file also contains an issuance license that imposes restrictions on the people who view the file. Typical restrictions include making a file read-only, disabling the copying of text, preventing people from saving a local copy, and preventing people from printing the file. Client programs that can read IRM-supported file types use the issuance license within the rights-managed file to enforce these restrictions. This is how a rights-managed file retains its protection even after it is downloaded from the server.</span></span>
  
<span data-ttu-id="37ce7-p113">목록이 나 라이브러리에서 다운로드 될 때 파일에 적용 되는 제한 유형은 해당 파일을 포함 하는 사이트에 대 한 개별 사용자의 권한을 기반으로 합니다. 다음 표에서는 사이트에 대 한 사용 권한이 IRM 사용 권한에 어떻게 대응 하는지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p113">The types of restrictions that are applied to a file when it is downloaded from a list or library are based on the individual user's permissions on the site that contains the file. The following table explains how the permissions on sites correspond to IRM permissions.</span></span>
  
|<span data-ttu-id="37ce7-195">**사용 권한**</span><span class="sxs-lookup"><span data-stu-id="37ce7-195">**Permissions**</span></span>|<span data-ttu-id="37ce7-196">**IRM 사용 권한**</span><span class="sxs-lookup"><span data-stu-id="37ce7-196">**IRM Permissions**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37ce7-197">사용 권한 관리, 웹 사이트 관리</span><span class="sxs-lookup"><span data-stu-id="37ce7-197">Manage Permissions, Manage Web Site</span></span>  <br/> |<span data-ttu-id="37ce7-198">**모든** 권한 (클라이언트 프로그램에서 정의 됨):이 권한을 사용 하면 일반적으로 권한 관리 콘텐츠의 사용 권한을 읽고, 편집 하 고, 복사 하 고, 저장 하 고, 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-198">**Full control** (as defined by the client program): This permission generally allows a user to read, edit, copy, save, and modify permissions of rights-managed content.</span></span>  <br/> |
|<span data-ttu-id="37ce7-199">항목 편집, 목록 관리, 페이지 추가 및 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="37ce7-199">Edit Items, Manage Lists, Add and Customize Pages</span></span>  <br/> |<span data-ttu-id="37ce7-200">**편집**, **복사**및 **저장**: 목록 또는 라이브러리에 대 한 정보 권한 관리 설정 페이지에서 사용자 **가 문서 인쇄 허용** 확인란이 선택 되어 있는 경우에만 파일을 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-200">**Edit**, **Copy**, and **Save**: A user can print a file only if the **Allow users to print documents** check box is selected on the Information Rights Management Settings page for the list or library.</span></span>  <br/> |
|<span data-ttu-id="37ce7-201">항목 보기</span><span class="sxs-lookup"><span data-stu-id="37ce7-201">View Items</span></span>  <br/> |<span data-ttu-id="37ce7-p114">**읽기**: 사용자가 문서를 읽을 수 있지만 콘텐츠를 복사 하거나 수정할 수 없습니다. 목록 또는 라이브러리에 대 한 정보 권한 관리 설정 페이지에서 사용자 **가 문서 인쇄 허용** 확인란이 선택 되어 있는 경우에만 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p114">**Read**: A user can read the document, but cannot copy or modify its content. A user can print only if the **Allow users to print documents** check box is selected on the Information Rights Management Settings page for the list or library.  </span></span><br/> |
|<span data-ttu-id="37ce7-204">기타</span><span class="sxs-lookup"><span data-stu-id="37ce7-204">Other</span></span>  <br/> |<span data-ttu-id="37ce7-205">다른 사용 권한은 IRM 사용 권한에 직접 대응 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-205">No other permissions correspond directly to IRM permissions.</span></span>  <br/> |
   
<span data-ttu-id="37ce7-p115">SharePoint Server 2013에서 목록 또는 라이브러리에 대해 IRM을 사용 하도록 설정 하면 모든 프런트 엔드 웹 서버에 보호 기능이 설치 된 목록 또는 라이브러리의 파일 형식만 보호할 수 있습니다. 보호 기능 이란 특정 파일 형식의 권한 관리 파일에 대 한 암호화 및 암호 해독을 제어 하는 프로그램입니다. SharePoint에는 다음 파일 형식에 대 한 보호기가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-p115">When you enable IRM for a list or library in SharePoint Server 2013, you can only protect file types in that list or library for which a protector is installed on all front-end Web servers. A protector is a program that controls the encryption and decryption of rights-managed files of a specific file format. SharePoint includes protectors for the following file types:</span></span>
  
- <span data-ttu-id="37ce7-209">Microsoft Office InfoPath 양식</span><span class="sxs-lookup"><span data-stu-id="37ce7-209">Microsoft Office InfoPath forms</span></span>
    
- <span data-ttu-id="37ce7-210">다음 Microsoft Office 프로그램에 대 한 97-2003 파일 형식: Word, Excel 및 PowerPoint</span><span class="sxs-lookup"><span data-stu-id="37ce7-210">The 97-2003 file formats for the following Microsoft Office programs: Word, Excel, and PowerPoint</span></span>
    
- <span data-ttu-id="37ce7-211">다음 Microsoft Office 프로그램의 office Open XML 형식: Word, Excel 및 PowerPoint</span><span class="sxs-lookup"><span data-stu-id="37ce7-211">The Office Open XML Formats for the following Microsoft Office programs: Word, Excel, and PowerPoint</span></span>
    
- <span data-ttu-id="37ce7-212">XPS (XML Paper Specification) 형식</span><span class="sxs-lookup"><span data-stu-id="37ce7-212">The XML Paper Specification (XPS) format</span></span>
    
<span data-ttu-id="37ce7-213">조직에서 위의 목록 외에 다른 파일 형식도 보호 하기 위해 IRM을 사용 하려는 경우에는 서버 관리자가 이러한 추가 파일 형식에 대해 보호기를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ce7-213">If your organization plans to use IRM to protect any other file types in addition to those listed above, your server administrator must install protectors for these additional file formats.</span></span>
  

