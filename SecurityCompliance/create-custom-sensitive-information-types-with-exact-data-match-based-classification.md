---
title: 정확한 데이터 매치를 사용한 사용자 지정 중요한 정보 유형 만들기
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: 분류에 기반한 정확한 데이터 매치를 사용한 사용자 지정 중요한 정보 유형 만들기
ms.openlocfilehash: 3c2b7cbabc77328f7d907927008e93606d40eded
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478197"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification"></a><span data-ttu-id="4a28a-103">분류에 기반한 정확한 데이터 매치를 사용한 사용자 지정 중요한 정보 유형 만들기</span><span class="sxs-lookup"><span data-stu-id="4a28a-103">See Create a custom sensitive information type with Exact Data Match based classification (Preview).</span></span>

## <a name="overview"></a><span data-ttu-id="4a28a-104">개요</span><span class="sxs-lookup"><span data-stu-id="4a28a-104">Overview</span></span>

<span data-ttu-id="4a28a-105">
  [사용자 지정 중요한 정보 유형](https://docs.microsoft.com/ko-KR/office365/securitycompliance/custom-sensitive-info-types)을 사용하면 중요한 정보를 의도하지 않거나 부적절하게 공유하는 것을 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-105">[Custom sensitive information types](https://docs.microsoft.com/en-us/office365/securitycompliance/custom-sensitive-info-types) are used to help prevent inadvertent or inappropriate sharing of sensitive information.</span></span> <span data-ttu-id="4a28a-106">관리자로서 [보안 및 준수 센터](https://docs.microsoft.com/ko-KR/office365/securitycompliance/create-a-custom-sensitive-information-type) 또는 [PowerShell](https://docs.microsoft.com/ko-KR/office365/securitycompliance/create-a-custom-sensitive-information-type-in-scc-powershell)을 사용하여 패턴, 증명( *직원*, *배지*, *ID* 등의 키워드), 문자 근접도(특정 패턴에서 증명과 문자가 근접한 정도) 및 신뢰 수준을 기반으로 사용자 지정 정보 유형을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-106">As an administrator, you can use the [Security & Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/create-a-custom-sensitive-information-type) or [PowerShell](https://docs.microsoft.com/en-us/office365/securitycompliance/create-a-custom-sensitive-information-type-in-scc-powershell) to define a custom sensitive information type based on patterns, evidence (keywords such as *employee*, *badge*, *ID*, and so on), character proximity (how close evidence is to characters in a particular pattern), and confidence levels.</span></span> <span data-ttu-id="4a28a-107">이러한 사용자 지정 중요한 정보 유형은 대부분의 조직에 필요한 비즈니스 요구 사항을 충족합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-107">Such custom sensitive information types meet business needs for many organizations.</span></span>

<span data-ttu-id="4a28a-108">일반적인 패턴과만 일치하는 것이 아니라 정확한 데이터 값을 사용하는 사용자 지정 중요한 정보 유형의 경우에는 어떻게 할까요?</span><span class="sxs-lookup"><span data-stu-id="4a28a-108">But what if you wanted a custom sensitive information type that uses exact data values, instead of matching only with generic patterns?</span></span> <span data-ttu-id="4a28a-109">정확한 데이터 매치(EDM) 기반 분류를 사용하여 다음과 같이 설계된 사용자 지정 중요한 정보 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-109">With Exact Data Match (EDM)-based classification, you can create a custom sensitive information type that is designed to:</span></span>

- <span data-ttu-id="4a28a-110">동적이며 새로 고치기 가능</span><span class="sxs-lookup"><span data-stu-id="4a28a-110">be dynamic and refreshable;</span></span>
- <span data-ttu-id="4a28a-111">확장성 향상</span><span class="sxs-lookup"><span data-stu-id="4a28a-111">be more scalable;</span></span>
- <span data-ttu-id="4a28a-112">가양성 수 감소</span><span class="sxs-lookup"><span data-stu-id="4a28a-112">result in fewer false-positives;</span></span>
- <span data-ttu-id="4a28a-113">구조화된 중요한 데이터 사용</span><span class="sxs-lookup"><span data-stu-id="4a28a-113">work with structured sensitive data;</span></span>
- <span data-ttu-id="4a28a-114">중요한 정보를 더 안전하게 처리</span><span class="sxs-lookup"><span data-stu-id="4a28a-114">handle sensitive information more securely; and</span></span>
- <span data-ttu-id="4a28a-115">여러 Microsoft 클라우드 서비스와 사용 가능.</span><span class="sxs-lookup"><span data-stu-id="4a28a-115">be used with several Microsoft cloud services.</span></span>

![EDM 기반 분류](media/EDMClassification.png)

<span data-ttu-id="4a28a-117">EDM 기반 분류를 사용하면 중요한 정보 데이터베이스의 정확한 값을 참조하는 사용자 지정 중요한 정보 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-117">EDM-based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="4a28a-118">데이터베이스는 매일 또는 매주 새로 고칠 수 있으며 최대 1000만 개의 데이터 행을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-118">The database can be refreshed daily or weekly, and it can contain up to 10 million rows of data.</span></span> <span data-ttu-id="4a28a-119">직원, 환자 또는 고객이 계속 이동하고 기록이 변경됨에 따라 사용자 지정 중요한 정보 유형을 적절하고 최신인 상태로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-119">So as employees, patients, or clients come and go, and records change, your custom sensitive information types remain current and applicable.</span></span> <span data-ttu-id="4a28a-120">또한 EDM 기반 분류를 [데이터 손실 방지 정책(DLP)](https://docs.microsoft.com/ko-KR/office365/securitycompliance/data-loss-prevention-policies) 또는 [Microsoft Cloud App Security 파일 정책](https://docs.microsoft.com/cloud-app-security/data-protection-policies) 등의 정책과 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-120">And, you can use EDM-based classification with policies, such as [data loss prevention policies](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies) (DLP) or [Microsoft Cloud App Security file policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="4a28a-121">필수 라이선스 및 사용 권한</span><span class="sxs-lookup"><span data-stu-id="4a28a-121">Required licenses and permissions</span></span>

<span data-ttu-id="4a28a-122">이 문서에 설명된 작업을 수행하려면 전역 관리자, 준수 관리자 또는 Exchange Online 관리자여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-122">You must be a global admin, compliance administrator, or Exchange Online administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="4a28a-123">DLP 권한에 관한 자세한 내용은  [사용 권한](https://docs.microsoft.com/ko-KR/office365/securitycompliance/data-loss-prevention-policies#permissions)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a28a-123">To learn more about DLP permissions, see [Permissions](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies#permissions).</span></span>

<span data-ttu-id="4a28a-124">일반적으로 사용 가능하게 되면 EDM 기반 분류가 다음 구독에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-124">When generally available, EDM-based classification will be included in these subscriptions</span></span>

- <span data-ttu-id="4a28a-125">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="4a28a-125">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="4a28a-126">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="4a28a-126">Microsoft 365 E5</span></span>
- <span data-ttu-id="4a28a-127">Microsoft 365 정보 보호 및 규정 준수</span><span class="sxs-lookup"><span data-stu-id="4a28a-127">Microsoft 365 Information Protection and Compliance</span></span>
- <span data-ttu-id="4a28a-128">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="4a28a-128">Office 365 Advanced Compliance</span></span>

## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="4a28a-129">워크플로 한 눈에 보기</span><span class="sxs-lookup"><span data-stu-id="4a28a-129">The work flow at a glance</span></span>

|<span data-ttu-id="4a28a-130">단계</span><span class="sxs-lookup"><span data-stu-id="4a28a-130">Phase</span></span>  |<span data-ttu-id="4a28a-131">필요한 사항</span><span class="sxs-lookup"><span data-stu-id="4a28a-131">What's needed</span></span>  |
|---------|---------|
|[<span data-ttu-id="4a28a-132">1단계: EDM 기반 분류 설정</span><span class="sxs-lookup"><span data-stu-id="4a28a-132">Part 1: Set up EDM-based classification</span></span>](#part-1-set-up-edm-based-classification)<br/><br/><span data-ttu-id="4a28a-133">(필요한 대로 수행)</span><span class="sxs-lookup"><span data-stu-id="4a28a-133">(As needed)</span></span><br/><span data-ttu-id="4a28a-134">- [데이터베이스 스키마 편집](#editing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="4a28a-134">- [Edit the database schema](#editing-the-schema-for-edm-based-classification)</span></span> <br/><span data-ttu-id="4a28a-135">- [스키마 제거](#removing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="4a28a-135">- [Remove the schema](#removing-the-schema-for-edm-based-classification)</span></span> |<span data-ttu-id="4a28a-136">- 중요한 데이터에 대한 읽기 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="4a28a-136">- Read access to the sensitive data</span></span><br/><span data-ttu-id="4a28a-137">- .xml 형식의 데이터베이스 스키마(예제 제공)</span><span class="sxs-lookup"><span data-stu-id="4a28a-137">- Database schema in .xml format (example provided)</span></span><br/><span data-ttu-id="4a28a-138">- .xml 형식의 규칙 패키지(예제 제공)</span><span class="sxs-lookup"><span data-stu-id="4a28a-138">- Rule package in .xml format (example provided)</span></span><br/><span data-ttu-id="4a28a-139">- 보안 및 준수 센터에 대한 관리자 권한(Windows PowerShell 사용)</span><span class="sxs-lookup"><span data-stu-id="4a28a-139">- Admin permissions to the Security & Compliance Center (using PowerShell)</span></span> |
|[<span data-ttu-id="4a28a-140">2단계: 중요한 데이터 색인화 및 업로드</span><span class="sxs-lookup"><span data-stu-id="4a28a-140">Part 2: Index and upload the sensitive data</span></span>](#part-2-index-and-upload-the-sensitive-data)<br/><br/><span data-ttu-id="4a28a-141">(필요한 대로 수행)</span><span class="sxs-lookup"><span data-stu-id="4a28a-141">(As needed)</span></span><br/>[<span data-ttu-id="4a28a-142">데이터 새로 고침</span><span class="sxs-lookup"><span data-stu-id="4a28a-142">Refresh the data</span></span>](#refreshing-your-sensitive-information-database) |<span data-ttu-id="4a28a-143">- 사용자 지정 보안 그룹 및 사용자 계정</span><span class="sxs-lookup"><span data-stu-id="4a28a-143">- Custom security group and user account</span></span><br/><span data-ttu-id="4a28a-144">- EDM 업로드 에이전트가 있는 컴퓨터에 대한 로컬 관리자 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="4a28a-144">- Local admin access to machine with EDM Upload Agent</span></span><br/><span data-ttu-id="4a28a-145">- 중요한 데이터에 대한 읽기 액세스 권한</span><span class="sxs-lookup"><span data-stu-id="4a28a-145">- Read access to the sensitive data</span></span><br/><span data-ttu-id="4a28a-146">- 데이터를 새로 고치는 프로세스 및 일정</span><span class="sxs-lookup"><span data-stu-id="4a28a-146">- Process and schedule for refreshing the data</span></span>|
|[<span data-ttu-id="4a28a-147">3단계: Microsoft 클라우드 서비스로 EDM 기반 분류 사용</span><span class="sxs-lookup"><span data-stu-id="4a28a-147">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |<span data-ttu-id="4a28a-148">- DLP 포함 Office 365 구독</span><span class="sxs-lookup"><span data-stu-id="4a28a-148">- Office 365 subscription with DLP</span></span><br/><span data-ttu-id="4a28a-149">- EDM 기반 분류 기능 사용</span><span class="sxs-lookup"><span data-stu-id="4a28a-149">- EDM-based classification feature enabled</span></span> |

### <a name="part-1-set-up-edm-based-classification"></a><span data-ttu-id="4a28a-150">1단계: EDM 기반 분류 설정</span><span class="sxs-lookup"><span data-stu-id="4a28a-150">Part 1: Set up EDM-based classification</span></span>

<span data-ttu-id="4a28a-151">EDM 기반 분류를 설정하고 구성하려면 중요한 데이터를 .csv 형식으로 저장하고, 중요한 정보의 데이터베이스 스키마를 정의하며, 규칙 패키지를 만든 다음 스키마와 규칙 패키지를 업로드해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-151">Setting up and configuring EDM-based classification involves saving sensitive data in .csv format, defining a schema for your database of sensitive information, creating a rule package, and then uploading the schema and rule package.</span></span>

#### <a name="define-the-schema-for-your-database-of-sensitive-information"></a><span data-ttu-id="4a28a-152">중요한 정보 데이터베이스의 스키마 정의</span><span class="sxs-lookup"><span data-stu-id="4a28a-152">Define the schema for your database of sensitive information</span></span>

1. <span data-ttu-id="4a28a-153">사용하려는 중요한 정보를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-153">Identify the sensitive information you want to use.</span></span> <span data-ttu-id="4a28a-154">Microsoft Excel과 같은 앱에 데이터를 내보내고 .csv 형식으로 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-154">Export the data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="4a28a-155">데이터 파일에는 최대 다음을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-155">The data file can include a maximum of:</span></span>
      - <span data-ttu-id="4a28a-156">최대 1000만 개의 중요한 데이터 행</span><span class="sxs-lookup"><span data-stu-id="4a28a-156">Up to 10 million rows of sensitive data</span></span>
      - <span data-ttu-id="4a28a-157">데이터 원본당 최대 32개의 열(필드)</span><span class="sxs-lookup"><span data-stu-id="4a28a-157">Up to 32 columns (fields) per data source</span></span>
      - <span data-ttu-id="4a28a-158">검색 가능으로 표시된 최대 5개의 열(필드)</span><span class="sxs-lookup"><span data-stu-id="4a28a-158">Up to 5 columns (fields) marked as searchable</span></span>

2. <span data-ttu-id="4a28a-159">첫 번째 행에 EDM 기반 분류에 사용한 필드의 이름이 포함되도록 .csv 파일에 중요한 데이터를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-159">Structure the sensitive data in the .csv file such that the first row includes the names of the fields used for EDM-based classification.</span></span> <span data-ttu-id="4a28a-160">.csv 파일에는 "ssn", "birthdate", "firstname", "lastname" 등의 필드 이름이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-160">In your .csv file, you might have field names, such as "ssn", "birthdate", "firstname", "lastname", and so on.</span></span> <span data-ttu-id="4a28a-161">예를 들어 .csv 파일은 *PatientRecords.csv*라고 하며 해당 열에는 *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN* 등이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-161">As an example, our .csv file is called *PatientRecords.csv*, and its columns include *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN* and more.</span></span>

3. <span data-ttu-id="4a28a-162">중요한 정보 데이터의 스키마를 .xml 형식으로 정의합니다(아래 예제와 비슷).</span><span class="sxs-lookup"><span data-stu-id="4a28a-162">Define the schema for the database of sensitive information in .xml format (similar to our example below).</span></span> <span data-ttu-id="4a28a-163">이 스키마 파일의 이름을 edm.xml로 지정하고 데이터베이스의 각 열에 \<Field name="" searchable=""/\> 구문을 사용하는 줄이 있도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-163">Name this schema file edm.xml, and configure it such that for each column in the database, there is a line that uses the syntax \<Field name="" searchable=""/\>.</span></span>

      - <span data-ttu-id="4a28a-164"> *Field name* 값에 열 이름을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-164">Use column names for *Field name* values.</span></span>
      - <span data-ttu-id="4a28a-165">최대 5개의 필드까지 검색할 수 있게 하려는 필드에 *searchable="true"* 를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-165">Use *searchable="true"* for the fields that you want to be searchable up to a maximum of 5 fields.</span></span> <span data-ttu-id="4a28a-166">최소 하나의 필드를 검색 가능한 항목으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-166">You must designate a minimum of one field as searchable.</span></span>

<span data-ttu-id="4a28a-167">예를 들어 다음 .xml 파일에서는 5개의 *필드(PatientID*, *MRN*, *SSN*, *Phone* 및 *DOB*)가 검색 가능으로 지정된 환자 레코드 데이터베이스의 스키마를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-167">As an example, the following .xml file defines the schema for a patient records database, with five fields specified as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span>

<span data-ttu-id="4a28a-168">(여기에 있는 예제를 복사, 수정 및 사용할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-168">(You can copy, modify, and use our example.)</span></span>

 ```xml
<EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
      <DataStore name="PatientRecords" description="Schema for patient records" version="1">
            <Field name="PatientID" searchable="true" />
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</EdmSchema>
```

4. [<span data-ttu-id="4a28a-169">Office 365 보안 및 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="4a28a-169">Connect to Office 365 Security & Compliance Center PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)

5. <span data-ttu-id="4a28a-170">데이터베이스 스키마를 업로드 하려면 다음과 같은 cmdlet을 한 번에 하나씩 실행하십시오:</span><span class="sxs-lookup"><span data-stu-id="4a28a-170">To upload the database schema, run the following cmdlets, one at a time:</span></span>

```powershell
$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

<span data-ttu-id="4a28a-171">다음과 같이 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-171">You will be prompted to confirm, as follows:</span></span>

> <span data-ttu-id="4a28a-172">확인</span><span class="sxs-lookup"><span data-stu-id="4a28a-172">Confirm</span></span>
>
> <span data-ttu-id="4a28a-173">이 작업을 수행하시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="4a28a-173">ConfirmAre you sure you want to perform this action?</span></span>
>
> <span data-ttu-id="4a28a-174">'patientrecords' 데이터 저장소의 새로운 EDM 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-174">New EDM Schema for the data store 'patientrecords' will be imported.</span></span>
>
> <span data-ttu-id="4a28a-175">\[Y\] 예 \[A\] 모두 예 \[N\] 아니요 \[L\] 모두 아니요 \[?\] 도움말(기본값: "Y"):</span><span class="sxs-lookup"><span data-stu-id="4a28a-175">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="4a28a-176">5단계에서 확인하지 않고 변경 사항을 적용하려면 New-DlpEdmSchema -FileData $edmSchemaXml 대신 해당 cmdlet을 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-176">If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: New-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="4a28a-177">EDMSchema를 추가 사항으로 업데이트하는 데 10~60분이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-177">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="4a28a-178">추가 사항을 사용하는 단계를 실행하기 전에 업데이트를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-178">The update must complete before you execute steps that use the additions.</span></span>

<span data-ttu-id="4a28a-179">중요한 정보 데이터베이스에 대한 스키마가 정의되었으므로 다음 단계는 규칙 패키지를 설정하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-179">Now that the schema for your database of sensitive information is defined, the next step is to set up a rule package.</span></span> <span data-ttu-id="4a28a-180"> [규칙 패키지 설정하기](#set-up-a-rule-package) 섹션으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-180">Proceed to the section [Set up a rule package](#set-up-a-rule-package).</span></span>

#### <a name="editing-the-schema-for-edm-based-classification"></a><span data-ttu-id="4a28a-181">EDM 기반 분류에 대한 스키마 편집</span><span class="sxs-lookup"><span data-stu-id="4a28a-181">Editing the schema for EDM-based classification</span></span>

<span data-ttu-id="4a28a-182">EDM 기반 분류에 사용되는 필드를 변경하는 것과 같이 edm.xml 파일을 변경하려면 다음 단계를 수행하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-182">If you want to make changes to your edm.xml file, such as changing which fields are used for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="4a28a-183">edm.xml 파일을 편집하십시오.(해당 문서의 [스키마 정의](#define-the-schema-for-your-database-of-sensitive-information) 섹션에서 다루는 파일입니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-183">Edit your edm.xml file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).</span></span>

2. [<span data-ttu-id="4a28a-184">Office 365 보안 및 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="4a28a-184">Connect to Office 365 Security & Compliance Center PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)

3. <span data-ttu-id="4a28a-185">데이터베이스 스키마를 업데이트하려면 다음과 같은 cmdlet을 한 번에 하나씩 실행하십시오:</span><span class="sxs-lookup"><span data-stu-id="4a28a-185">To update your database schema, run the following cmdlets, one at a time:</span></span>

```powershell
$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

<span data-ttu-id="4a28a-186">다음과 같이 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-186">You will be prompted to confirm, as follows:</span></span>

> <span data-ttu-id="4a28a-187">확인</span><span class="sxs-lookup"><span data-stu-id="4a28a-187">Confirm</span></span>
>
> <span data-ttu-id="4a28a-188">이 작업을 수행하시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="4a28a-188">ConfirmAre you sure you want to perform this action?</span></span>
>
> <span data-ttu-id="4a28a-189">'patientrecords' 데이터 저장소의 새로운 EDM 스키마를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-189">EDM Schema for the data store 'patientrecords' will be updated.</span></span>
>
> <span data-ttu-id="4a28a-190">\[Y\] 예 \[A\] 모두 예 \[N\] 아니요 \[L\] 모두 아니요 \[?\] 도움말(기본값: "Y"):</span><span class="sxs-lookup"><span data-stu-id="4a28a-190">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="4a28a-191">3단계에서 확인하지 않고 변경 사항을 적용하려면 Set-DlpEdmSchema -FileData $edmSchemaXml 대신 해당 cmdlet을 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-191">If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: Set-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="4a28a-192">EDMSchema를 추가 사항으로 업데이트하는 데 10~60분이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-192">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="4a28a-193">추가 사항을 사용하는 단계를 실행하기 전에 업데이트를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-193">The update must complete before you execute steps that use the additions.</span></span>

## <a name="removing-the-schema-for-edm-based-classification"></a><span data-ttu-id="4a28a-194">EDM 기반 분류에 대한 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="4a28a-194">Removing the schema for EDM-based classification</span></span>

<span data-ttu-id="4a28a-195">(필요한 경우) EDM 기반 분류에 사용 중인 스키마를 제거하려면 다음 단계를 따르십시오:</span><span class="sxs-lookup"><span data-stu-id="4a28a-195">(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:</span></span>

1. [<span data-ttu-id="4a28a-196">Office 365 보안 및 준수 센터 PowerShell에 연결</span><span class="sxs-lookup"><span data-stu-id="4a28a-196">Connect to Office 365 Security & Compliance Center PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)

2. <span data-ttu-id="4a28a-197">다음의 PowerShell cmdlet을 실행하여 "patientrecords"의 데이터 저장소 이름을 제거하고자 하는 것으로 대체하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-197">Run the following PowerShell cmdlets, substituting the data store name of "patientrecords" with the one you want to remove:</span></span>

```powershell
Remove-DlpEdmSchema -Identity patientrecords
```

<span data-ttu-id="4a28a-198">다음과 같이 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-198">You will be prompted to confirm, as follows:</span></span>

> <span data-ttu-id="4a28a-199">확인</span><span class="sxs-lookup"><span data-stu-id="4a28a-199">Confirm</span></span>
>
> <span data-ttu-id="4a28a-200">이 작업을 수행하시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="4a28a-200">ConfirmAre you sure you want to perform this action?</span></span>
>
> <span data-ttu-id="4a28a-201">'patientrecords' 데이터 저장소의 EDM 스키마를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-201">EDM Schema for the data store 'patientrecords' will be removed.</span></span>
>
> <span data-ttu-id="4a28a-202">\[Y\] 예 \[A\] 모두 예 \[N\] 아니요 \[L\] 모두 아니요 \[?\] 도움말(기본값: "Y"):</span><span class="sxs-lookup"><span data-stu-id="4a28a-202">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
>  <span data-ttu-id="4a28a-203">2단계에서 확인하지 않고 변경 사항을 적용하려면 Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false 대신 해당 cmdlet을 사용하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-203">If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span></span>

### <a name="set-up-a-rule-package"></a><span data-ttu-id="4a28a-204">규칙 패키지 설정</span><span class="sxs-lookup"><span data-stu-id="4a28a-204">Set up a rule package</span></span>

1. <span data-ttu-id="4a28a-205">다음 예제와 같이 in .xml 형식(유니코드 인코딩 사용)에 규칙 패키지를 생성하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-205">Create a rule package in .xml format (with Unicode encoding), similar to the following example.</span></span> <span data-ttu-id="4a28a-206">(여기에 있는 예제를 복사, 수정 및 사용할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-206">(You can copy, modify, and use our example.)</span></span>

<span data-ttu-id="4a28a-207">규칙 패키지를 설정하는 경우 .csv 파일과 edm.xml 파일을 정확하게 참조하도록 하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-207">When you set up your rule package, make sure to correctly reference your .csv file and edm.xml file.</span></span> <span data-ttu-id="4a28a-208">(여기에 있는 예제를 복사, 수정 및 사용할 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-208">You can copy, modify, and use our example.</span></span> <span data-ttu-id="4a28a-209">이 샘플 xml에서 EDM 중요 유형을 만들려면 다음 필드를 사용자 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-209">In this sample xml the following fields needs to be customized to create your EDM sensitive type:</span></span>

- <span data-ttu-id="4a28a-210">
  \*\*RulePack ID & ExactMatch ID*\*: [New-GUID](https://docs.microsoft.com/ko-KR/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6)를  사용하여 GUID를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-210">**RulePack id & ExactMatch id**: Use [New-GUID](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) to generate a GUID.</span></span>

- <span data-ttu-id="4a28a-211">**Datastore**: 이 필드는 사용할 EDM 조회 데이터 저장소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-211">**Datastore**: This field specifies EDM lookup data store to be used.</span></span> <span data-ttu-id="4a28a-212">구성된 EDM 스키마의 데이터 원본 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-212">You provide a data source name of a configured EDM Schema.</span></span>

- <span data-ttu-id="4a28a-213">**idMatch**: 이 필드는 EDM의 기본 요소를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-213">**idMatch**: This field points to the primary element for EDM.</span></span>
  - <span data-ttu-id="4a28a-214">Matches: 정확한 조회에 사용할 필드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-214">Matches: Specifies the field to be used in exact lookup.</span></span> <span data-ttu-id="4a28a-215">데이터 저장소의 EDM 스키마에서 검색 가능한 필드 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-215">You provide a searchable field name in EDM Schema for the DataStore.</span></span>
  - <span data-ttu-id="4a28a-216">Classification: 이 필드는 EDM 조회를 트리거하는 중요한 유형 일치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-216">Classification: This field specifies the sensitive type match that triggers EDM lookup.</span></span> <span data-ttu-id="4a28a-217">기존의 기본 제공 분류 또는 사용자 지정 분류의 이름 또는 GUID를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-217">You can provide Name or GUID of an existing built-in or custom classification.</span></span>

- <span data-ttu-id="4a28a-218">**Match:** 이 필드는 idMatch의 근접성에서 찾은 추가 증명을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-218">**Match:** This field points to additional evidence found in proximity of idMatch.</span></span>
  - <span data-ttu-id="4a28a-219">Matches: 데이터 저장소의 EDM 스키마에 필드 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-219">Matches: You provide any field name in EDM Schema for DataStore.</span></span>
- <span data-ttu-id="4a28a-220">**리소스:** 이 섹션에서는 여러 로캘에서 중요한 유형의 이름과 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-220">**Resource:** This section specifies the name and description for sensitive type in multiple locales.</span></span>
  - <span data-ttu-id="4a28a-221">idRef: ExactMatch ID의 GUID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-221">idRef: You provide GUID for ExactMatch id.</span></span>
  - <span data-ttu-id="4a28a-222">Name & des 스키마 설명 편집: 필요에 따라 사용자 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-222">Name & des Editing the schema criptions: customize as required.</span></span>

```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care EDM Rulepack</Name>
        <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
```

1. <span data-ttu-id="4a28a-223">다음의 PowerShell cmdlet을 한 번에 하나씩 실행하여 규칙 패키지를 업로드하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-223">Upload the rule package by running the following PowerShell cmdlets, one at a time:</span></span>

```powershell
$rulepack=Get-Content .\\rulepack.xml -Encoding Byte -ReadCount 0
New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack
```

<span data-ttu-id="4a28a-224">이 시점에서 EDM 기반 분류를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-224">At this point, you have set up EDM-based classification.</span></span> <span data-ttu-id="4a28a-225">다음 단계로는 중요한 데이터를 색인화하고 색인화된 데이터를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-225">The next step is to index the sensitive data, and then upload the indexed data.</span></span>

<span data-ttu-id="4a28a-226">PatientRecords 스키마가 검색 가능한 것으로 5개의 필드를 정의한 이전 절차에서 *PatientID*, *MRN*, *SSN*, *Phone* 및 *DOB*를 불러오십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-226">Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span> <span data-ttu-id="4a28a-227">예제 규칙 패키지에는 해당 필드가 포함되어 있으며 검색 가능한 필드당 하나의 *ExactMatch* 항목과 함께 데이터베이스 스키마 파일(edm.xml)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-227">Our example rule package includes those fields and references the database schema file (edm.xml), with one *ExactMatch* items per searchable field.</span></span> <span data-ttu-id="4a28a-228">다음의 ExactMatch 항목을 고려하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-228">Consider the following ExactMatch item:</span></span>

```xml
<ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
```

<span data-ttu-id="4a28a-229">해당 예제에서 다음과 같은 사항을 참고하십시오.</span><span class="sxs-lookup"><span data-stu-id="4a28a-229">In this example, note the following:</span></span>

- <span data-ttu-id="4a28a-230">데이터 저장소 이름은 이전에 생성한 .csv 파일( **데이터 저장소 = "PatientRecords"**)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-230">The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.</span></span>

- <span data-ttu-id="4a28a-231">idmatch 값은 데이터베이스 스키마 파일( **idMatch matches = "SSN"**)에 나열된 검색 가능한 필드를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-231">The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.</span></span>

- <span data-ttu-id="4a28a-232">분류 값이 기존 또는 사용자 지정 중요한 정보 유형( **분류 = "미국 SSN(사회 보장 번호)"**)을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-232">The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**.</span></span> <span data-ttu-id="4a28a-233">(이 경우 미국 주민 등록 번호의 기존의 중요한 정보 유형을 사용합니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-233">(In this case, we use the existing sensitive information type of U.S. Social Security Number.)</span></span>

> [!NOTE]
> <span data-ttu-id="4a28a-234">EDMSchema를 추가 사항으로 업데이트하는 데 10~60분이 소요될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-234">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="4a28a-235">추가 사항을 사용하는 단계를 실행하기 전에 업데이트를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-235">The update must complete before you execute steps that use the additions.</span></span>

### <a name="part-2-index-and-upload-the-sensitive-data"></a><span data-ttu-id="4a28a-236">2단계: 중요한 데이터 색인화 및 업로드</span><span class="sxs-lookup"><span data-stu-id="4a28a-236">Part 2: Index and upload the sensitive data</span></span>

<span data-ttu-id="4a28a-237">이 단계에서는 사용자 지정 보안 그룹 및 사용자 계정을 설정하고 EDM 업로드 에이전트 도구를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-237">During this phase, you set up a custom security group and user account, and set up the EDM Upload Agent tool.</span></span> <span data-ttu-id="4a28a-238">그런 다음 이 도구를 사용하여 중요한 데이터를 색인화하고 색인화된 데이터를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-238">Then, you use the tool to index the sensitive data, and upload the indexed data.</span></span>

#### <a name="set-up-the-security-group-and-user-account"></a><span data-ttu-id="4a28a-239">보안 그룹 및 사용자 계정 설정</span><span class="sxs-lookup"><span data-stu-id="4a28a-239">Set up the security group and user account</span></span>

1. <span data-ttu-id="4a28a-240">전역 관리자로서 관리 센터([https://admin.microsoft.com](https://admin.microsoft.com/))로 이동하여 EDM\_DataUploaders라는 [보안 그룹 만들기](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide)를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-240">As a global administrator, go to the admin center ([https://admin.microsoft.com](https://admin.microsoft.com/)) and [create a security group](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) called EDM\_DataUploaders.</span></span>

2. <span data-ttu-id="4a28a-241">한 명 이상의 사용자를 *EDM\_DataUploaders* 보안 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-241">Add one or more users to the *EDM\_DataUploaders* security group.</span></span> <span data-ttu-id="4a28a-242">(이러한 사용자가 중요한 정보 데이터베이스를 관리합니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-242">(These users will manage the database of sensitive information.)</span></span>

3. <span data-ttu-id="4a28a-243">중요한 데이터를 관리하는 각 사용자가 EDM 업로드 에이전트에 사용되는 컴퓨터에서 로컬 관리자인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-243">Make sure each user who is managing the sensitive data is a local admin on the machine used for the EDM Upload Agent.</span></span>

#### <a name="set-up-the-edm-upload-agent"></a><span data-ttu-id="4a28a-244">EDM 업로드 에이전트 설정</span><span class="sxs-lookup"><span data-stu-id="4a28a-244">Set up the EDM Upload Agent</span></span>

>[!NOTE]
> <span data-ttu-id="4a28a-245">이 절차를 시작하기 전에 *EDM\_DataUploaders* 보안 그룹의 구성원이며 컴퓨터의 로컬 관리자인지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-245">Before you begin this procedure, make sure that you are a member of the *EDM\_DataUploaders* security group and a local admin on your machine.</span></span>

1. <span data-ttu-id="4a28a-246">[EDM 업로드 에이전트](https://go.microsoft.com/fwlink/?linkid=2088639)를 다운로드하고 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-246">Download and install the [EDM Upload Agent](https://go.microsoft.com/fwlink/?linkid=2088639).</span></span> <span data-ttu-id="4a28a-247">기본적으로 설치 위치는 C:\\Program Files\\Microsoft\\EdmUploadAgent여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-247">By default, the installation location should be C:\\Program Files\\Microsoft\\EdmUploadAgent.</span></span>

2. <span data-ttu-id="4a28a-248">EDM 업로드 에이전트에 권한을 부여하려면 Windows 명령 프롬프트를 열고(관리자로) 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-248">To authorize the EDM Upload Agent, open Windows Command Prompt (as an administrator), and then run the following command:</span></span>

    `EdmUploadAgent.exe /Authorize`

3. <span data-ttu-id="4a28a-249">Office 365의 회사 또는 학교 계정을 사용하여 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-249">Sign in to Office 365 for business with your work or school account.</span></span>

<span data-ttu-id="4a28a-250">다음 단계로는 EDM 업로드 에이전트를 사용하여 중요한 데이터를 색인화하고 색인화된 데이터를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-250">The next step is to use the EDM Upload Agent to index the sensitive data, and then upload the indexed data.</span></span>

#### <a name="index-and-upload-the-sensitive-data"></a><span data-ttu-id="4a28a-251">중요한 데이터 색인화 및 업로드</span><span class="sxs-lookup"><span data-stu-id="4a28a-251">Index and upload the sensitive data</span></span>

<span data-ttu-id="4a28a-252">중요한 데이터 파일(여기에서 예제는 *PatientRecords.csv*임)을 컴퓨터의 로컬 드라이브에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-252">Save the sensitive data file (recall our example is *PatientRecords.csv*) to the local drive on the machine.</span></span> <span data-ttu-id="4a28a-253">(예제 *PatientRecords.csv* 파일을 C:\\Edm\\Data에 저장했습니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-253">(We saved our example *PatientRecords.csv* file to C:\\Edm\\Data.)</span></span>

<span data-ttu-id="4a28a-254">중요한 데이터를 색인화하고 업로드하려면 Windows 명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-254">To index and upload the sensitive data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadData /DataStoreName \<DataStoreName\> /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="4a28a-255">예제: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span><span class="sxs-lookup"><span data-stu-id="4a28a-255">Example: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span></span>

<span data-ttu-id="4a28a-256">격리된 환경에서 중요한 데이터의 인덱스를 분리하고 실행하려면 인덱스를 각각 실행하고 단계를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-256">To separate and execute index of sensitive data in an isolated environment, execute index and upload steps separately.</span></span>

<span data-ttu-id="4a28a-257">중요한 데이터를 색인화하려면 Windows 명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-257">To index the sensitive data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /CreateHash /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="4a28a-258">예제: **EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span><span class="sxs-lookup"><span data-stu-id="4a28a-258">Example: **EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span></span>

<span data-ttu-id="4a28a-259">색인화된 데이터를 업로드하려면 Windows 명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-259">To upload the indexed data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadHash /DataStoreName \<DataStoreName\> /HashFile \<HashedSourceFilePath\>`

<span data-ttu-id="4a28a-260">예제: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span><span class="sxs-lookup"><span data-stu-id="4a28a-260">Example: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span></span>

<span data-ttu-id="4a28a-261">중요한 데이터가 업로드되었는지 확인하려면 Windows 명령 프롬프트에서 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-261">To verify your sensitive data has been uploaded, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /GetDataStore`

<span data-ttu-id="4a28a-262">데이터 저장소 목록 및 마지막 업데이트 날짜를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-262">You'll see a list of data stores and when they were last updated.</span></span>

<span data-ttu-id="4a28a-263">계속하여 [중요한 정보 데이터베이스 새로 고침](#refreshing-your-sensitive-information-database)의 프로세스 및 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-263">Proceed to set up your process and schedule for [Refreshing your sensitive information database](#refreshing-your-sensitive-information-database).</span></span>

<span data-ttu-id="4a28a-264">이제 Microsoft 클라우드 서비스로 EDM 기반 분류를 사용할 준비가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-264">At this point, you are ready to use EDM-based classification with your Microsoft cloud services.</span></span> <span data-ttu-id="4a28a-265">예를 들어 [EDM 기반 분류를 사용하여 DLP 정책을 설정](#to-create-a-dlp-policy-with-edm)할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-265">For example, you can [set up a DLP policy using EDM-based classification](#to-create-a-dlp-policy-with-edm).</span></span>

#### <a name="refreshing-your-sensitive-information-database"></a><span data-ttu-id="4a28a-266">중요한 정보 데이터베이스 새로 고침</span><span class="sxs-lookup"><span data-stu-id="4a28a-266">Refreshing your sensitive information database</span></span>

<span data-ttu-id="4a28a-267">중요한 정보 데이터베이스를 매일 또는 매주 새로 고칠 수 있으며, EDM 업로드 도구를 사용하여 중요한 데이터를 다시 색인화한 다음 색인화된 데이터를 다시 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-267">You can refresh your sensitive information database daily or weekly, and the EDM Upload Tool can reindex the sensitive data and then reupload the indexed data.</span></span>

1. <span data-ttu-id="4a28a-268">중요한 정보 데이터베이스를 새로 고치는 빈도(매일 또는 매주)와 프로세스를 판별합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-268">Determine your process and frequency (daily or weekly) for refreshing the database of sensitive information.</span></span>

2. <span data-ttu-id="4a28a-269">Microsoft Excel과 같은 앱에 중요한 데이터를 다시 내보내고 .csv 형식으로 파일을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-269">Re-export the sensitive data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="4a28a-270"> [중요한 데이터 색인화 및 업로드](#index-and-upload-the-sensitive-data)에 설명된 단계를 수행할 때 사용한 파일 이름과 위치를 동일하게 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-270">Keep the same file name and location you used when you followed the steps described in [Index and upload the sensitive data](#index-and-upload-the-sensitive-data).</span></span>

> [!NOTE]
> <span data-ttu-id="4a28a-271">.csv 파일의 구조(필드 이름)를 변경하지 않은 경우 데이터를 새로 고칠 때 데이터베이스 스키마 파일을 변경하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-271">If there are no changes to the structure (field names) of the .csv file, you won't need to make any changes to your database schema file when you refresh the data.</span></span> <span data-ttu-id="4a28a-272">하지만 변경해야 하는 경우 데이터베이스 스키마와 규칙 패키지를 적절하게 편집해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-272">But if you must make changes, make sure to edit the database schema and your rule package accordingly.</span></span>

3. <span data-ttu-id="4a28a-273"> [작업 스케줄러](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page)를 사용하여 [중요한 데이터 색인화 및 업로드](#index-and-upload-the-sensitive-data) 절차의 2단계와 3단계를 자동화합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-273">Use [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) to automate steps 2 and 3 in the [Index and upload the sensitive data](#index-and-upload-the-sensitive-data) procedure.</span></span> <span data-ttu-id="4a28a-274">다음과 같은 여러 방법을 사용하여 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-274">You can schedule tasks using several methods:</span></span>

| <span data-ttu-id="4a28a-275">**방법**</span><span class="sxs-lookup"><span data-stu-id="4a28a-275">**Method**</span></span>             | <span data-ttu-id="4a28a-276">**수행할 작업**</span><span class="sxs-lookup"><span data-stu-id="4a28a-276">**What to do if rule processing fails**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="4a28a-277">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a28a-277">Windows PowerShell</span></span>     | <span data-ttu-id="4a28a-278"> [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) 문서와 이 문서에 있는 [예제 PowerShell 스크립트](#example-powershell-script-for-task-scheduler)를  참고하세요.</span><span class="sxs-lookup"><span data-stu-id="4a28a-278">See the [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) documentation and the [example PowerShell script](#example-powershell-script-for-task-scheduler) in this article</span></span> |
| <span data-ttu-id="4a28a-279">작업 스케줄러 API</span><span class="sxs-lookup"><span data-stu-id="4a28a-279">Task Scheduler API</span></span>     | <span data-ttu-id="4a28a-280"> [작업 스케줄러](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a28a-280">See the [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) documentation</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="4a28a-281">Windows 사용자 인터페이스</span><span class="sxs-lookup"><span data-stu-id="4a28a-281">Windows user interface</span></span> | <span data-ttu-id="4a28a-282">Windows에서 **시작**을 클릭하고 작업 스케줄러를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-282">In Windows, click **Start**, and type Task Scheduler.</span></span> <span data-ttu-id="4a28a-283">그런 다음 결과 목록에서 **작업 스케줄러**를 마우스 오른쪽 단추로 클릭하고 **관리자로 실행**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-283">Then, in the list of results, right-click **Task Scheduler**, and choose **Run as administrator**.</span></span>                                                                                                                                                                                                                                                                           |

#### <a name="example-powershell-script-for-task-scheduler"></a><span data-ttu-id="4a28a-284">작업 스케줄러의 예제 Windows PowerShell 스크립트</span><span class="sxs-lookup"><span data-stu-id="4a28a-284">Example PowerShell script for Task Scheduler</span></span>

<span data-ttu-id="4a28a-285">이 섹션에서는 데이터를 색인화하고 색인화된 데이터를 업로드하는 작업을 예약하는 데 사용할 수 있는 예제 Windows PowerShell 스크립트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-285">This section includes an example PowerShell script you can use to schedule your tasks for indexing data and uploading the indexed data:</span></span>

##### <a name="to-schedule-index-and-upload-in-a-combined-step"></a><span data-ttu-id="4a28a-286">인덱스를 예약하고 결합된 단계에 업로드하려면</span><span class="sxs-lookup"><span data-stu-id="4a28a-286">To schedule index and upload in a combined step</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$uploadDataArgs = '/UploadData /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ‘ /HashLocation’ + $hashLocation
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadDataArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

#### <a name="to-schedule-index-and-upload-as-separate-steps"></a><span data-ttu-id="4a28a-287">인덱스를 예약하고 별도의 단계로 업로드하려면</span><span class="sxs-lookup"><span data-stu-id="4a28a-287">To schedule index and upload as separate steps</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
$hashFile = "$fileLocation\\$dataStoreName$edmext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash' + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

### <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a><span data-ttu-id="4a28a-288">3단계: Microsoft 클라우드 서비스로 EDM 기반 분류 사용</span><span class="sxs-lookup"><span data-stu-id="4a28a-288">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>

<span data-ttu-id="4a28a-289">Exchange Online용 Office 365 DLP(전자 메일), Business용 OneDrive(파일), Microsoft Teams(대화) 및 Microsoft Cloud App Security DLP 정책은 EDM 중요 정보 유형을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-289">Office 365 DLP for Exchange Online (email), OneDrive for Business (files), Microsoft Teams (conversations) and Microsoft Cloud App Security DLP policies will support EDM sensitive information types.</span></span>

<span data-ttu-id="4a28a-290">다음 시나리오에 대한 EDM 중요 정보 유형은 현재 개발 중이지만 아직 사용할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-290">EDM sensitive information types for following scenarios are currently in development, but not yet available:</span></span>

- <span data-ttu-id="4a28a-291">SharePoint용 Office 365 DLP(파일)</span><span class="sxs-lookup"><span data-stu-id="4a28a-291">Office 365 DLP for SharePoint (files)</span></span>
- <span data-ttu-id="4a28a-292">민감도 레이블과 보존 레이블의 자동 분류</span><span class="sxs-lookup"><span data-stu-id="4a28a-292">Auto-classification of sensitivity labels and retention labels</span></span>

#### <a name="to-create-a-dlp-policy-with-edm"></a><span data-ttu-id="4a28a-293">EDM으로 DLP 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="4a28a-293">To create a DLP policy with EDM</span></span>

1. <span data-ttu-id="4a28a-294">보안 및 준수 센터로 이동([https://protection.office.com](https://protection.office.com/))합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-294">Go to the Security & Compliance Center</span></span>

2. <span data-ttu-id="4a28a-295"> **데이터 손실 방지** \> **정책**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-295">Choose **Data loss prevention** \> **Policy**.</span></span>

3. <span data-ttu-id="4a28a-296"> **정책 만들기** \> **사용자 지정** \> **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-296">Choose **Create a policy** \> **Custom** \> **Next**.</span></span>

4. <span data-ttu-id="4a28a-297"> **정책 이름 지정** 탭에 이름과 설명을 지정하고 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-297">On the **Name your policy** tab, specify a name and description, and then choose **Next**.</span></span>

5. <span data-ttu-id="4a28a-298"> **위치 선택** 탭에서 **특정 위치 선택 허용**을 선택하고 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-298">On the **Choose locations** tab, select **Let me choose specific locations**, and then choose **Next**.</span></span>

6. <span data-ttu-id="4a28a-299"> **상태** 열에서 **Exchange 전자 메일, OneDrive 계정, Teams 채팅 및 채널 메시지** 를 선택하고  **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-299">In the **Status** column, select **Exchange email, OneDrive accounts, Teams chat and channel message** , and then choose **Next**.</span></span> <span data-ttu-id="4a28a-300">(참고: EDM은 현재 SharePoint 사이트에서 지원되지 않으며 DLP 정책은 EDM용 Sharepoint에서 파일을 검색하지 않습니다.)</span><span class="sxs-lookup"><span data-stu-id="4a28a-300">(Note: EDM is currently not supported in SharePoint sites and DLP policy will not detect files in Sharepoint for EDM)</span></span>

7. <span data-ttu-id="4a28a-301"> **정책 설정** 탭에서 **고급 설정 사용**을 선택하고 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-301">On the **Policy settings** tab, choose **Use advanced settings**, and then choose **Next**.</span></span>

8. <span data-ttu-id="4a28a-302"> **+ 새 규칙**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-302">Choose **+ New rule**.</span></span>

9. <span data-ttu-id="4a28a-303"> **이름** 섹션에서 규칙의 이름과 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-303">In the **Name** section, specify a name and description for the rule.</span></span>

10. <span data-ttu-id="4a28a-304"> **조건** 섹션의 **+ 조건 추가** 목록에서 **콘텐츠에 중요한 유형 포함**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-304">In the **Conditions** section, in the **+ Add a condition** list, choose **Content contains sensitive type**.</span></span><br/><span data-ttu-id="4a28a-305">![콘텐츠에 중요한 정보 유형이 포함됨](media/edm-dlp-newrule-conditions.png)</span><span class="sxs-lookup"><span data-stu-id="4a28a-305">![Content contains sensitive info types](media/edm-dlp-newrule-conditions.png)</span></span><br/>

11. <span data-ttu-id="4a28a-306">규칙 패키지를 설치할 때 만든 중요한 정보 유형을 검색한 다음  **+ 추가**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-306">Search for the sensitive information type you created when you set up your rule package, and then choose **+ Add**.</span></span>  
    <span data-ttu-id="4a28a-307">그런 다음 **완료**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-307">Then choose **Done**.</span></span>

12. <span data-ttu-id="4a28a-308"> **사용자 알림**, **사용자 재정의**, **인시던트 보고서** 등의 규칙에 관한 옵션 선택을 완료한 다음 **저장**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-308">Finish selecting options for your rule, such as **User notifications**, **User overrides**, **Incident reports**, and so on, and then choose **Save**.</span></span>

13. <span data-ttu-id="4a28a-309"> **정책 설정** 탭에서 규칙을 검토하고 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-309">On the **Policy settings** tab, review your rules, and then choose **Next**.</span></span>

14. <span data-ttu-id="4a28a-310">정책을 바로 설정할지, 테스트할지, 아니면 설정 해제한 상태로 유지할지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-310">Specify whether to turn on the policy right away, test it out, or keep it turned off.</span></span> <span data-ttu-id="4a28a-311">그런 후 **다음**을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-311">Then choose **Next**.</span></span>

15. <span data-ttu-id="4a28a-312"> **설정 검토** 탭에서 정책을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-312">On the **Review your settings** tab, review your policy.</span></span> <span data-ttu-id="4a28a-313">필요한 대로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-313">Make any needed modifications.</span></span> <span data-ttu-id="4a28a-314">준비가 되면 **만들기**를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-314">When you're ready, choose **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="4a28a-315">새로운 DLP 정책이 데이터 센터에 적용되는 데 1시간 정도 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-315">Allow approximately one hour for your new DLP policy to work its way through your data center.</span></span>

## <a name="related-articles"></a><span data-ttu-id="4a28a-316">관련 문서</span><span class="sxs-lookup"><span data-stu-id="4a28a-316">Related articles</span></span>

<span data-ttu-id="4a28a-317">
  [기본 제공 중요 정보 유형 및 해당 유형이 찾는 항목](https://docs.microsoft.com/ko-KR/office365/securitycompliance/what-the-sensitive-information-types-look-for)</span><span class="sxs-lookup"><span data-stu-id="4a28a-317">[Built-in sensitive information types and what they look for](https://docs.microsoft.com/en-us/office365/securitycompliance/what-the-sensitive-information-types-look-for)</span></span>

<span data-ttu-id="4a28a-318">
  [사용자 지정 중요한 정보 유형](https://docs.microsoft.com/ko-KR/office365/securitycompliance/custom-sensitive-info-types)</span><span class="sxs-lookup"><span data-stu-id="4a28a-318">[Custom sensitive information types](https://docs.microsoft.com/en-us/office365/securitycompliance/custom-sensitive-info-types)</span></span>

<span data-ttu-id="4a28a-319">
  [DLP 정책 개요](https://docs.microsoft.com/ko-KR/office365/securitycompliance/data-loss-prevention-policies)</span><span class="sxs-lookup"><span data-stu-id="4a28a-319">[Overview of DLP policies](https://docs.microsoft.com/en-us/office365/securitycompliance/data-loss-prevention-policies)</span></span>

[<span data-ttu-id="4a28a-320">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="4a28a-320">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)

<span data-ttu-id="4a28a-321">
  [New-DlpEdmSchema](https://docs.microsoft.com/ko-KR/powershell/module/exchange/policy-and-compliance-dlp/new-dlpedmschema?view=exchange-ps)</span><span class="sxs-lookup"><span data-stu-id="4a28a-321">[New-DlpEdmSchema](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-dlp/new-dlpedmschema?view=exchange-ps)</span></span>

## <a name="feedback"></a><span data-ttu-id="4a28a-322">피드백</span><span class="sxs-lookup"><span data-stu-id="4a28a-322">Feedback</span></span>
<span data-ttu-id="4a28a-323">GitHub 피드백을 사용할 수 있지만, 공개 사이트에서만 문제를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a28a-323">GitHub feedback is enabled, but adding issues is only available on the public site.</span></span>
