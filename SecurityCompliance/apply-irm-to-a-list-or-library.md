---
title: 목록 또는 라이브러리에 정보 권한 관리 (IRM) 적용
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 3bdb5c4e-94fc-4741-b02f-4e7cc3c54aa1
description: 정보 권한 관리 (IRM)를 사용 하 여 손쉽게 제어 하 고 목록 또는 라이브러리에서 다운로드 되는 파일 보호를 수 있습니다.
ms.openlocfilehash: 5a48abf13841716d4dba34311d69ca2e6a5ea422
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533428"
---
# <a name="apply-information-rights-management-irm-to-a-list-or-library"></a><span data-ttu-id="47134-103">목록 또는 라이브러리에 정보 권한 관리 (IRM) 적용</span><span class="sxs-lookup"><span data-stu-id="47134-103">Apply Information Rights Management (IRM) to a list or library</span></span>

<span data-ttu-id="47134-104">정보 권한 관리 (IRM)를 사용 하 여 손쉽게 제어 하 고 목록 또는 라이브러리에서 다운로드 되는 파일 보호를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-104">You can use Information Rights Management (IRM) to help control and protect files that are downloaded from lists or libraries.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="47134-105">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="47134-105">Before you begin</span></span>

- <span data-ttu-id="47134-p101">Azure 정보 보호 및 온-프레미스 해당, Active Directory Rights Management Services (AD RMS)에서 Azure 권한 관리 서비스 (Azure RMS) 사이트에 대 한 정보 권한 관리를 지원 합니다. 별도 또는 추가 설치 없음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p101">The Azure Rights Management service (Azure RMS) from Azure Information Protection, and the on-premises equivalent, Active Directory Rights Management Services (AD RMS), support Information Rights Management for sites. No separate or additional installations are required.</span></span>
    
- <span data-ttu-id="47134-108">목록 또는 라이브러리에 IRM을 적용 하기 전에 먼저 사이트에 대 한 관리자가 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-108">Before you apply IRM to a list or library it must first be enabled by an administrator for your site.</span></span>
    
- <span data-ttu-id="47134-109">목록 또는 라이브러리에 IRM을 적용할 해당 목록이 나 라이브러리에 대 한 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-109">To apply IRM to a list or library, you must have administrator permissions for that list or library.</span></span>
    
- <span data-ttu-id="47134-p102">SharePoint Online을 사용 하는 경우에 사용자가 더 큰 IRM으로 보호 된 파일을 다운로드할 때 제한 시간에 발생할 수 있습니다. 이 경우 Office 프로그램을 사용 하 여 IRM 보호 기능을 적용 하 고 IRM을 사용 하지 않는 SharePoint 라이브러리에 큰 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p102">If you are using SharePoint Online, your users might experience timeouts when downloading larger IRM-protected files. If this happens, then apply IRM protection by using your Office programs, and store larger files in a SharePoint library that does not use IRM.</span></span>
    
> [!NOTE]
> <span data-ttu-id="47134-112">SharePoint Server 2013을 사용 하는 경우 서버 관리자가 조직에서 사용자가 IRM을 사용 하 여 보호 하려는 모든 파일 형식에 대 한 모든 프런트엔드 웹 서버에 보호기를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-112">If you're using SharePoint Server 2013, a server administrator must install protectors on all front-end Web servers for every file type that the people in your organization want to protect by using IRM.</span></span> 
  
## <a name="apply-irm-to-a-list-or-library"></a><span data-ttu-id="47134-113">목록 또는 라이브러리에 IRM을 적용</span><span class="sxs-lookup"><span data-stu-id="47134-113">Apply IRM to a list or library</span></span>
<span data-ttu-id="47134-114"><a name="__toc256598179"> </a></span><span class="sxs-lookup"><span data-stu-id="47134-114"></span></span>

![정보 권한 관리 설정](media/1b708102-9c90-42b0-b255-ef0e72d0be88.png)
  
1. <span data-ttu-id="47134-116">IRM을 구성 하려면 목록 또는 라이브러리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-116">Go to the list or library for which you want to configure IRM.</span></span>
    
2. <span data-ttu-id="47134-p103">리본 메뉴에서 **라이브러리** 탭을 클릭 하 고 **라이브러리 설정**을 클릭 합니다. (목록에서 작업 하는 경우 **목록** 탭을 클릭 한 다음 **목록 설정**을 클릭).</span><span class="sxs-lookup"><span data-stu-id="47134-p103">On the ribbon, click the **Library** tab, and then click **Library Settings**. (If you are working in a list, click the **List** tab, and then click **List Settings**).</span></span>
    
    ![리본 메뉴에서 SharePoint 라이브러리 설정 단추](media/cdf718fa-d792-40fc-8026-00c3b80b9e05.png)
  
3. <span data-ttu-id="47134-p104">**사용 권한 및 관리**에서 **정보 권한 관리**를 클릭 합니다. 정보 권한 관리 링크가 나타나지 않으면 사이트에 대 한 IRM 사용 되지 될 수 있습니다. 사이트에 대 한 IRM을 사용 하도록 설정 하는 서버 관리자에 게 문의 합니다. 그림 라이브러리에 대 한 정보 권한 관리 링크가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p104">Under **Permissions and Management**, click **Information Rights Management**. If the Information Rights Management link does not appear, IRM might not be enabled for your site. Contact your server administrator to see if it is possible to enable IRM for your site. The Information Rights Management link does not appear for picture libraries.</span></span>
    
4. <span data-ttu-id="47134-124">**정보 권한 관리 설정** 페이지에서이 목록 또는 라이브러리에서 다운로드 되는 문서에 제한 된 사용 권한을 적용 하려면 **다운로드 시이 라이브러리에서 문서에 대 한 사용 권한을 제한** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-124">On the **Information Rights Management Settings** page, select the **Restrict permission to documents in this library on download** check box to apply restricted permission to documents that are downloaded from this list or library.</span></span> 
    
5. <span data-ttu-id="47134-p105">**만들기 권한 정책 제목** 상자에이 정책을 다른 정책과 구별 하기 위해 나중에 사용할 수 있는 정책에 대 한 설명 이름을 입력 합니다. 예, 입력할 수 **회사 기밀** 기밀 회사 문서가 포함 될 라이브러리 또는 목록으로 제한 된 사용 권한을 적용 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="47134-p105">In the **Create a permission policy title** box, type a descriptive name for the policy that you can use later to differentiate this policy from other policies. For example, you can type **Company Confidential** if you are applying restricted permission to a list or library that will contain company documents that are confidential.</span></span> 
    
6. <span data-ttu-id="47134-p106">**추가 권한 정책 설명** 상자에이 목록 또는이 목록 또는 라이브러리의 문서를 처리 하는 방법을 설명 하는 라이브러리를 사용 하는 사람에 게 표시 되는 설명을 입력 합니다. 예, 입력할 수 있습니다 **다른 직원과이 문서의 내용을 논의** 내부 직원에 게 이러한 문서에 있는 정보에 대 한 액세스를 제한 하려는 경우.</span><span class="sxs-lookup"><span data-stu-id="47134-p106">In the **Add a permission policy description** box, type a description that will appear to people who use this list or library that explains how they should handle the documents in this list or library. For example, you can type **Discuss the contents of this document only with other employees** if you want to restrict access to the information in these documents to internal employees.</span></span> 
    
7. <span data-ttu-id="47134-129">제한 사항을 추가이 목록 또는 라이브러리에서 문서에 적용할 **표시 옵션**을 클릭 하 고 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-129">To apply additional restrictions to the documents in this list or library, click **Show Options**, and do any of the following:</span></span>
    
|<span data-ttu-id="47134-130">**이 작업을 수행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="47134-130">**To do this:**</span></span>|<span data-ttu-id="47134-131">**이 작업을 수행 합니다.**</span><span class="sxs-lookup"><span data-stu-id="47134-131">**Do this:**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47134-132">이 목록 또는 라이브러리에서 문서를 인쇄 하는 사용자를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-132">Allow people to print documents from this list or library</span></span>  <br/> |<span data-ttu-id="47134-133">**인쇄 허용 뷰어** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-133">Select the **Allow viewers to print** check box.</span></span>  <br/> |
|<span data-ttu-id="47134-134">허용 된 최소 문서에 포함 된 코드 또는 매크로 실행 하는 항목 보기 권한을 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="47134-134">Allow people with at least the View Items permission to run embedded code or macros on a document.</span></span>  <br/> |<span data-ttu-id="47134-135">**스크립트 및 화면 판독기 다운로드 된 문서에 대해 함수를 실행 하는 뷰어 허용** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-135">Select the **Allow viewers to run script and screen reader to function on downloaded documents** check box.</span></span>  <br/> <span data-ttu-id="47134-136">이 옵션을 선택 하는 경우 사용자가 문서의 콘텐츠를 추출 하는 코드를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-136">If you select this option, users could run code to extract the contents of a document.</span></span>           |
|<span data-ttu-id="47134-137">사용자 지정 된 간격 자격 증명을 확인 하는 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-137">Require that people verify their credentials at specific intervals.</span></span>  <br/> <span data-ttu-id="47134-p107">지정된 된 시간 동안에는 콘텐츠에 액세스를 제한 하려는 경우이 옵션을 선택 합니다. 이 옵션을 선택 하는 경우 지정된 된 수 일 및 사용자의 자격 증명을 확인 하 고 새 복사본을 다운로드 하는 서버로 반환 하려면 필요 합니다 후 콘텐츠에 액세스할 수 있는 사용자의 발급 라이선스 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p107">Select this option if you want to restrict access to content to a specified period of time. If you select this option, people's issuance licenses to access the content will expire after the specified number of days, and people will be required to return to the server to verify their credentials and download a new copy.</span></span>  <br/> |<span data-ttu-id="47134-140">선택 된 **사용자가이 간격을 사용 하 여 자격 증명을 확인 해야 합니다 (일)** 확인란을 선택한 다음 문서를 볼 수를 구하려는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-140">Select the **Users must verify their credentials using this interval (days)** check box, and then specify the number of days for which you want the document to be viewable.</span></span>  <br/> |
| <span data-ttu-id="47134-141">사용자를이 목록 또는 라이브러리에 IRM을 지원 하지 않는 문서를 업로드할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-141">Prevent people from uploading documents that do not support IRM to this list or library.</span></span>  <br/>  <span data-ttu-id="47134-142">이 옵션을 선택 하는 경우 사용자는 다음과 같은 파일 형식 중 하나를 업로드할 수 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-142">If you select this option, people will not be able to upload any of the following file types:</span></span>  <br/>  <span data-ttu-id="47134-143">모든 프런트엔드 웹 서버에 설치 하는 해당 IRM 보호 장치가 없는 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="47134-143">File types that do not have corresponding IRM protectors installed on all of the front-end Web servers.</span></span>  <br/>  <span data-ttu-id="47134-144">SharePoint Server 2010를 해독할 수 없습니다는 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="47134-144">File types that SharePoint Server 2010 cannot decrypt.</span></span>  <br/>  <span data-ttu-id="47134-145">다른 프로그램에서 IRM으로 보호 되는 파일 형식</span><span class="sxs-lookup"><span data-stu-id="47134-145">File types that are IRM protected in another program</span></span>  <br/> |<span data-ttu-id="47134-146">**사용자가 IRM을 지원 하지 않는 문서를 업로드할 수 없도록 함** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-146">Select the **Do not allow users to upload documents that do not support IRM** check box.</span></span>  <br/> |
|<span data-ttu-id="47134-147">이 목록 또는 라이브러리에서 특정 날짜에 제한 된 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-147">Remove restricted permissions from this list or library on a specific date.</span></span>  <br/> |<span data-ttu-id="47134-148">**라이브러리에 대 한 액세스를 제한 중지** 확인란을 선택 하 고 원하는 날짜를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-148">Select the **Stop restricting access to the library at** check box, and then select the date that you want.</span></span>  <br/> |
|<span data-ttu-id="47134-149">문서를 여는데 라이선스 프로그램에 대 한 제어 간격 자격 증명에 캐시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47134-149">Control the interval that credentials are cached for the program that is licensed to open the document.</span></span>  <br/> |<span data-ttu-id="47134-150">**그룹 보호 및 자격 증명 간격을 설정**, theinterval 일 수에 자격 증명을 캐시에 대 한 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-150">In the **Set group protection and credentials interval**, enter theinterval for caching credentials in number of days.</span></span>  <br/> |
|<span data-ttu-id="47134-151">사용자가 동일한 그룹의 멤버와 공유할 수 있도록 그룹 보호를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-151">Allow group protection so that users can share with members of the same group.</span></span>  <br/> |<span data-ttu-id="47134-152">**허용 그룹 보호**선택 하 고 공유 하는 것에 대 한 그룹의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-152">Select **Allow group protection**, and enter the group's name for sharing.</span></span>  <br/> |
   
8. <span data-ttu-id="47134-153">원하는 옵션을 선택 했으면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-153">After you finish selecting the options you want, click **OK**.</span></span>
  
## <a name="what-is-information-rights-management"></a><span data-ttu-id="47134-154">정보 권한 관리 이란?</span><span class="sxs-lookup"><span data-stu-id="47134-154">What is Information Rights Management?</span></span>
<span data-ttu-id="47134-155"><a name="__toc256598175"> </a></span><span class="sxs-lookup"><span data-stu-id="47134-155"></span></span>

<span data-ttu-id="47134-p108">정보 권한 관리 (IRM)를 사용 하면 사용자가 목록이 나 라이브러리에서 다운로드 파일에 대해 수행할 수 있는 작업을 제한할 수 있습니다. IRM은 다운로드 한 파일을 암호화 하 고 사용자와 이러한 파일 암호를 해독 하 허용 되는 프로그램의 집합을 제한 합니다. IRM에서 텍스트를 복사 하거나 파일의 복사본을 인쇄 하는 등의 작업을 수행할 수는 없습니다 있도록 파일을 읽을 수 있는 사용자의 권한을 제한할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p108">Information Rights Management (IRM) enables you to limit the actions that users can take on files that have been downloaded from lists or libraries. IRM encrypts the downloaded files and limits the set of users and programs that are allowed to decrypt these files. IRM can also limit the rights of the users who are allowed to read files, so that they cannot take actions such as print copies of the files or copy text from them.</span></span>
  
<span data-ttu-id="47134-p109">중요 한 콘텐츠를 배포 하지 못하도록 하려면 목록 또는 라이브러리에 IRM을 사용할 수 있습니다. 예, 선택한 마케팅 담당자와 예정 된 제품에 대 한 정보를 공유 하는 문서 라이브러리를 만드는 경우 이러한 개인 회사의 다른 직원과이 콘텐츠를 공유 하지 못하도록 하려면 IRM을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p109">You can use IRM on lists or libraries to limit the dissemination of sensitive content. For example, if you are creating a document library to share information about upcoming products with selected marketing representatives, you can use IRM to prevent these individuals from sharing this content with other employees in the company.</span></span>
  
<span data-ttu-id="47134-p110">사이트에서 개별 파일 대신 전체 목록 또는 라이브러리에 IRM 적용 합니다. 그러면 일관 된 문서 또는 파일의 전체 집합에 대 한 보호 수준을 확인 하려면 더 쉽습니다. IRM 사용과 기밀 또는 독점 정보의 배포를 제어 하는 회사 정책을 적용 하 여 조직의 도움말 따라서 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p110">On a site, you apply IRM to an entire list or library, rather than to individual files. This makes it easier to ensure a consistent level of protection for an entire set of documents or files. IRM can thus help your organization to enforce corporate policies that govern the use and dissemination of confidential or proprietary information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="47134-164">정보 권한 관리에 대 한이 페이지의 정보를 Microsoft SharePoint Server 2013 및 SharePoint Server 2016 라이선스 용어 계약에 ' 정보 권한 관리 '를 참조 하는 모든 용어를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-164">The information on this page regarding Information Rights Management supersedes any terms that reference 'Information Rights Management' in any Microsoft SharePoint Server 2013 and SharePoint Server 2016 license term agreements.</span></span> 
  
### <a name="how-irm-can-help-protect-content"></a><span data-ttu-id="47134-165">IRM 보호할 수 있는 방법을 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="47134-165">How IRM can help protect content</span></span>
<span data-ttu-id="47134-166"><a name="__toc256598176"> </a></span><span class="sxs-lookup"><span data-stu-id="47134-166"></span></span>

<span data-ttu-id="47134-167">IRM 다음과 같은 방법으로 제한 된 콘텐츠를 보호 하는데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47134-167">IRM helps to protect restricted content in the following ways:</span></span>
  
- <span data-ttu-id="47134-168">복사, 수정, 인쇄, 팩스, 또는 복사 및 붙여넣기 무단된으로 사용에 대 한 콘텐츠에서 권한이 부여 된 뷰어를 방지할 수</span><span class="sxs-lookup"><span data-stu-id="47134-168">Helps to prevent an authorized viewer from copying, modifying, printing, faxing, or copying and pasting the content for unauthorized use</span></span>
    
- <span data-ttu-id="47134-169">Microsoft Windows에서 Print Screen 기능을 사용 하 여 콘텐츠를 복사 하에서 권한이 부여 된 뷰어에 막을 수합니다</span><span class="sxs-lookup"><span data-stu-id="47134-169">Helps to prevent an authorized viewer from copying the content by using the Print Screen feature in Microsoft Windows</span></span>
    
- <span data-ttu-id="47134-170">권한이 없는 사용자는 서버에서 다운로드 한 후 전자 메일로 전송 하는 경우 콘텐츠를 볼 수 없도록 막을 수합니다</span><span class="sxs-lookup"><span data-stu-id="47134-170">Helps to prevent an unauthorized viewer from viewing the content if it is sent in e-mail after it is downloaded from the server</span></span>
    
- <span data-ttu-id="47134-171">콘텐츠에 되는 사용자가 자격 증명을 확인 하 고 해야 콘텐츠를 다시 다운로드 시간 지정된 된 기간에 대 한 액세스를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-171">Restricts access to content to a specified period of time, after which users must confirm their credentials and download the content again</span></span>
    
- <span data-ttu-id="47134-172">사용과 조직 내에서 콘텐츠 배포를 제어 하는 기업 정책을 적용 하는 데 도움이</span><span class="sxs-lookup"><span data-stu-id="47134-172">Helps to enforce corporate policies that govern the use and dissemination of content within your organization</span></span>
    
### <a name="how-irm-cannot-help-protect-content"></a><span data-ttu-id="47134-173">어떻게 IRM 보호할 수 없는 경우 콘텐츠</span><span class="sxs-lookup"><span data-stu-id="47134-173">How IRM cannot help protect content</span></span>
<span data-ttu-id="47134-174"><a name="__toc256598177"> </a></span><span class="sxs-lookup"><span data-stu-id="47134-174"></span></span>

<span data-ttu-id="47134-175">IRM 다음에서 제한 된 콘텐츠를 보호할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-175">IRM cannot protect restricted content from the following:</span></span>
  
- <span data-ttu-id="47134-176">지우지, 도난, 캡처, 또는 트로이 말, 키 입력으로 거 등 특정 유형의 스파이웨어 악성 프로그램으로 전송</span><span class="sxs-lookup"><span data-stu-id="47134-176">Erasure, theft, capture, or transmission by malicious programs such as Trojan horses, keystroke loggers, and certain types of spyware</span></span>
    
- <span data-ttu-id="47134-177">손실 또는 손상 컴퓨터 바이러스의 작업으로 인해</span><span class="sxs-lookup"><span data-stu-id="47134-177">Loss or corruption because of the actions of computer viruses</span></span>
    
- <span data-ttu-id="47134-178">수동으로 복사 하거나를 화면에 표시 된 콘텐츠를에서 다시 입력 하는</span><span class="sxs-lookup"><span data-stu-id="47134-178">Manual copying or retyping of content from the display on a screen</span></span>
    
- <span data-ttu-id="47134-179">디지털 콘텐츠를 화면에 표시 되는 사진 흐린 또는</span><span class="sxs-lookup"><span data-stu-id="47134-179">Digital or film photography of content that is displayed on a screen</span></span>
    
- <span data-ttu-id="47134-180">타사 화면 캡처 프로그램을 사용 하 여 복사</span><span class="sxs-lookup"><span data-stu-id="47134-180">Copying through the use of third-party screen-capture programs</span></span>
    
- <span data-ttu-id="47134-181">복사 하는 타사 화면 캡처 프로그램 또는 복사 하 여 붙여넣기 함수를 사용 하 여 콘텐츠 메타 데이터 (열 값)</span><span class="sxs-lookup"><span data-stu-id="47134-181">Copying of content metadata (column values) through the use of third-party screen-capture programs or copy-and-paste action</span></span>
    
[<span data-ttu-id="47134-182">목록 또는 라이브러리에 정보 권한 관리 적용</span><span class="sxs-lookup"><span data-stu-id="47134-182">Apply Information Rights Management to a list or library</span></span>](https://support.office.com/article/6714cfe3-ef39-43b0-bb65-a887726bb63c)
  
## <a name="how-irm-works-for-lists-and-libraries"></a><span data-ttu-id="47134-183">목록 및 라이브러리에 대 한 IRM 작동 방식</span><span class="sxs-lookup"><span data-stu-id="47134-183">How IRM works for lists and libraries</span></span>
<span data-ttu-id="47134-184"><a name="__toc256598178"> </a></span><span class="sxs-lookup"><span data-stu-id="47134-184"></span></span>

<span data-ttu-id="47134-p111">IRM 보호 목록 또는 라이브러리 수준에서 파일에 적용 됩니다. 라이브러리에 대 한 IRM 사용 하는 경우 권한 관리에는 해당 라이브러리에 파일을 모두에 적용 됩니다. 목록에 대 한 IRM 사용 하는 경우 권한 관리 실제 목록 항목이 아닌 목록 항목에 연결 된 파일에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p111">IRM protection is applied to files at the list or library level. When IRM is enabled for a library, rights management applies to all of the files in that library. When IRM is enabled for a list, rights management applies only to files that are attached to list items, not the actual list items.</span></span>
  
<span data-ttu-id="47134-p112">사용자는 IRM 사용이 가능한 목록 또는 라이브러리의 파일을 다운로드 하는 경우 권한이 부여 된 사용자만 볼 수 있도록 파일 암호화 됩니다. 권한이 관리 되는 각 파일에는 파일을 보는 사용자에 대 한 제한 사항을 적용 하는 한 발급 라이선스를 들어 있습니다. 일반적인 제한 사항으로 파일을 읽기 전용, 로컬 복사본을 저장 하 고 사용자 파일 인쇄 하지 못하도록 방지에서 사용자를 방지 하 여 텍스트를 복사 하는 사용 하지 않도록 설정 합니다. IRM 지원 되는 파일 형식에서 읽을 수 있는 클라이언트 프로그램 권한 관리 파일 내에서 발급 라이선스를 사용 하 여 이러한 제한 사항을 적용 합니다. 서버에서 다운로드 한 후에 권한 관리 파일의 보호를 유지 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p112">When people download files in an IRM-enabled list or library, the files are encrypted so that only authorized people can view them. Each rights-managed file also contains an issuance license that imposes restrictions on the people who view the file. Typical restrictions include making a file read-only, disabling the copying of text, preventing people from saving a local copy, and preventing people from printing the file. Client programs that can read IRM-supported file types use the issuance license within the rights-managed file to enforce these restrictions. This is how a rights-managed file retains its protection even after it is downloaded from the server.</span></span>
  
<span data-ttu-id="47134-p113">목록 또는 라이브러리에서 다운로드 될 때 파일에 적용 되는 제한 사항 유형의 파일을 포함 하는 사이트에 대 한 개별 사용자의 권한을 기반으로 합니다. 다음 표에서 사이트에 대 한 권한을 IRM 사용 권한에 해당 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p113">The types of restrictions that are applied to a file when it is downloaded from a list or library are based on the individual user's permissions on the site that contains the file. The following table explains how the permissions on sites correspond to IRM permissions.</span></span>
  
|<span data-ttu-id="47134-195">**사용 권한**</span><span class="sxs-lookup"><span data-stu-id="47134-195">**Permissions**</span></span>|<span data-ttu-id="47134-196">**IRM 사용 권한**</span><span class="sxs-lookup"><span data-stu-id="47134-196">**IRM Permissions**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47134-197">웹사이트, 사용 권한 관리</span><span class="sxs-lookup"><span data-stu-id="47134-197">Manage Permissions, Manage Web Site</span></span>  <br/> |<span data-ttu-id="47134-198">**모든 권한** (정의된대로 클라이언트 프로그램에 의해):이 권한은 일반적으로 읽기, 편집, 복사, 저장 및 권한 관리 콘텐츠에 대 한 사용 권한을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-198">**Full control** (as defined by the client program): This permission generally allows a user to read, edit, copy, save, and modify permissions of rights-managed content.</span></span>  <br/> |
|<span data-ttu-id="47134-199">항목 편집, 목록 관리, 추가 하 고 페이지를 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="47134-199">Edit Items, Manage Lists, Add and Customize Pages</span></span>  <br/> |<span data-ttu-id="47134-200">**편집**, **복사**및 **저장**: 목록 또는 라이브러리에 대 한 정보 권한 관리 설정 페이지에서 **사용자가 문서를 인쇄 하도록 허용** 확인란이 선택 하는 경우에 사용자가 파일을 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-200">**Edit**, **Copy**, and **Save**: A user can print a file only if the **Allow users to print documents** check box is selected on the Information Rights Management Settings page for the list or library.</span></span>  <br/> |
|<span data-ttu-id="47134-201">항목 보기</span><span class="sxs-lookup"><span data-stu-id="47134-201">View Items</span></span>  <br/> |<span data-ttu-id="47134-p114">**읽기**: 사용자는 문서를 읽을 수 있지만 복사 수는 없습니다 또는 해당 콘텐츠를 수정 합니다. 사용자는 목록 또는 라이브러리에 대 한 정보 권한 관리 설정 페이지에서 **사용자가 문서를 인쇄 하도록 허용** 확인란이 선택 하는 경우에 인쇄할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p114">**Read**: A user can read the document, but cannot copy or modify its content. A user can print only if the **Allow users to print documents** check box is selected on the Information Rights Management Settings page for the list or library.  </span></span><br/> |
|<span data-ttu-id="47134-204">기타</span><span class="sxs-lookup"><span data-stu-id="47134-204">Other</span></span>  <br/> |<span data-ttu-id="47134-205">다른 사용 권한은 IRM 사용 권한 직접 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="47134-205">No other permissions correspond directly to IRM permissions.</span></span>  <br/> |
   
<span data-ttu-id="47134-p115">목록 또는 라이브러리의 SharePoint Server 2013에 대 한 IRM을 사용 하도록 설정 하는 경우에 해당 목록이 나 보호기를 모든 프런트엔드 웹 서버에 설치 되는 라이브러리의 파일 형식을 보호할 수 있습니다. 보호 기능에는 암호화 및 암호 해독의 특정 파일 형식의 파일 권한 관리를 제어 하는 프로그램입니다. SharePoint에는 다음과 같은 파일 형식에 대 한 보호기 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47134-p115">When you enable IRM for a list or library in SharePoint Server 2013, you can only protect file types in that list or library for which a protector is installed on all front-end Web servers. A protector is a program that controls the encryption and decryption of rights-managed files of a specific file format. SharePoint includes protectors for the following file types:</span></span>
  
- <span data-ttu-id="47134-209">Microsoft Office InfoPath 양식</span><span class="sxs-lookup"><span data-stu-id="47134-209">Microsoft Office InfoPath forms</span></span>
    
- <span data-ttu-id="47134-210">다음 Microsoft Office 프로그램에 대 한 97-2003 파일 형식: Word, Excel 및 PowerPoint</span><span class="sxs-lookup"><span data-stu-id="47134-210">The 97-2003 file formats for the following Microsoft Office programs: Word, Excel, and PowerPoint</span></span>
    
- <span data-ttu-id="47134-211">Office Open XML 파일 형식은 다음 Microsoft Office 프로그램에 대 한: Word, Excel 및 PowerPoint</span><span class="sxs-lookup"><span data-stu-id="47134-211">The Office Open XML Formats for the following Microsoft Office programs: Word, Excel, and PowerPoint</span></span>
    
- <span data-ttu-id="47134-212">XML Paper Specification (XPS) 형식</span><span class="sxs-lookup"><span data-stu-id="47134-212">The XML Paper Specification (XPS) format</span></span>
    
<span data-ttu-id="47134-213">위에 나열 된 외에도 다른 파일 형식을 보호 하기 위해 IRM을 사용 하 여 조직에서 계획, 서버 관리자가 이러한 추가 파일 형식에 대 한 보호기를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="47134-213">If your organization plans to use IRM to protect any other file types in addition to those listed above, your server administrator must install protectors for these additional file formats.</span></span>
  

