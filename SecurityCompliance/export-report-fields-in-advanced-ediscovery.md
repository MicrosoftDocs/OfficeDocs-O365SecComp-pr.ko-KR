---
title: Office 365 Advanced eDiscovery 보고서 필드 내보내기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: 고급 eDiscovery에 대 한 내보내기 보고서에 포함 되는 모든 필드에 대해 설명 합니다.
ms.openlocfilehash: a910fa94a1361e48099ef5792ce93d5934fdccc5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216658"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 보고서 필드 내보내기

> [!NOTE]
> Advanced eDiscovery를 사용하려면 Office 365 E3의 고급 준수 추가 기능이나 조직을 위한 E5 구독이 필요합니다. 이 요금제가 없는 상태에서 Advanced eDiscovery를 사용하려는 경우에는 [Office 365 Enterprise E5 평가판을 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
이 항목에서는 표준 및 모든 서식 파일에 대 한 고급 eDiscovery 내보내기 보고서 필드에 대해 설명 합니다.
  
## <a name="export-report-fields"></a>보고서 필드 내보내기

다음 표에서는 각 내보내기 서식 파일에 대 한 필드를 보여 줍니다.
  
|**필드 이름 내보내기**|**그룹**|**설명**|**표준 서식 파일에서 사용 가능**|**모든 템플릿에서 사용 가능**|
|:-----|:-----|:-----|:-----|:-----|
|Row_number  <br/> |일반  <br/> |행 번호입니다.  <br/> |예  <br/> |예  <br/> |
|File_ID  <br/> |일반  <br/> |파일 ID입니다.  <br/> |예  <br/> |예  <br/> |
|File_class  <br/> |처리   <br/> |File 클래스  <br/> |예  <br/> |예  <br/> |
|Family_ID  <br/> |처리   <br/> |파일을 그룹화 하는 데 사용 되는 숫자 식별자입니다 (일반적으로 전자 메일 인스턴스 및 첨부 파일).  <br/> |예  <br/> |예  <br/> |
|For_review  <br/> |처리   <br/> |검토용으로 내보낼 때 필드가 포함 됨을 나타내는 플래그입니다.  <br/> |예  <br/> |예  <br/> |
|Native_file_name  <br/> |처리   <br/> |폴더 및 확장명을 참조 하지 않고 네이티브 파일 이름입니다.  <br/> |예  <br/> |예  <br/> |
|Custodians  <br/> |일반  <br/> |파일의 Custodian입니다.  <br/> |예  <br/> |예  <br/> |
|Set_ID  <br/> |분석  <br/> |"ND set" 또는 "전자 메일 집합" id  <br/> |예  <br/> |예  <br/> |
|Inclusive_type  <br/> |전자 메일  <br/> |0-포함 하지 않음, 1-포괄, 2 포함 마이너스, 3 포함 복사본 값에 따라 파일이 포함 되는지 여부를 나타냅니다.  <br/> |예  <br/> |예  <br/> |
|Marked_as_pivot  <br/> |중복에 근접  <br/> |파일이 피벗 인지 여부를 나타냅니다.  <br/> |예  <br/> |예  <br/> |
|Similarity_percent  <br/> |중복에 근접  <br/> |피벗에 대 한 유사성 비율입니다.  <br/> |예  <br/> |예  <br/> |
|Duplicate_subset  <br/> |중복에 근접  <br/> |중복 된 하위 집합의 고유 식별자입니다. 파일에 정확히 텍스트 중복이 있는지 여부를 나타냅니다.  <br/> |예  <br/> |예  <br/> |
|날짜  <br/> |일반  <br/> |파일 날짜 (파일 형식-전자 메일: 보낸 날짜; 문서: 수정한 날짜)에 따라 달라 집니다.  <br/> |예  <br/> |예  <br/> |
|Dominant_theme  <br/> |분석  <br/> |파일의 기본 테마입니다.  <br/> |예  <br/> |예  <br/> |
|Themes_list  <br/> |테마  <br/> |테마 이름 목록  <br/> |예  <br/> |예  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Nearduplicate 집합의 고유 숫자 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|Email_set  <br/> |전자 메일  <br/> |전자 메일 집합의 고유 숫자 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|Email_thread  <br/> |전자 메일  <br/> |전자 메일 집합 내의 전자 메일 위치는 루트에서 현재 전자 메일로의 모든 노드 id로 구성 되며 마침표로 구분 됩니다.  <br/> |예  <br/> |예  <br/> |
|Email_subject  <br/> |전자 메일  <br/> |전자 메일의 제목입니다.  <br/> |예  <br/> |예  <br/> |
|Email_date_sent  <br/> |전자 메일  <br/> |전자 메일이 전송 된 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Email_participants  <br/> |전자 메일  <br/> |누락 된 링크를 포함 하 여 전자 메일 스레드에 있는 모든 참가자의 전자 메일 주소입니다.  <br/> |예  <br/> |예  <br/> |
|Email_participant_domains  <br/> |전자 메일  <br/> |누락 된 링크를 포함 하 여 전자 메일 스레드에 있는 모든 참가자의 도메인입니다.  <br/> |예  <br/> |예  <br/> |
|Email_sender  <br/> |전자 메일  <br/> |전자 메일 보낸 사람 이름 및/또는 주소입니다.  <br/> |예  <br/> |예  <br/> |
|Email_sender_domain  <br/> |전자 메일  <br/> |전자 메일 보낸 사람의 도메인  <br/> |예  <br/> |예  <br/> |
|Email_to  <br/> |전자 메일  <br/> |전자 메일의 받는 사람입니다.  <br/> |예  <br/> |예  <br/> |
|Email_cc  <br/> |전자 메일  <br/> |전자 메일의 참조 받는 사람입니다.  <br/> |예  <br/> |예  <br/> |
|Email_bcc  <br/> |전자 메일  <br/> |전자 메일의 숨은 참조 받는 사람입니다.  <br/> |예  <br/> |예  <br/> |
|Email_recipient_domains  <br/> |전자 메일  <br/> |전자 메일 받는 사람, 참조 및 숨은 참조 도메인입니다.  <br/> |예  <br/> |예  <br/> |
|Email_date_received  <br/> |전자 메일  <br/> |전자 메일을 받은 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Email_action  <br/> |전자 메일  <br/> |값: 전자 메일 제목에 따라 "Forward" ("FW:"), "Reply" ("RE:") 또는 "other" (기타 제목 텍스트)로 이동 합니다.  <br/> |예  <br/> |예  <br/> |
|Meeting_Start_Date/Time  <br/> ||모임 항목이 시작 된 날짜 및 시간입니다.  <br/> |예  <br/> |예  <br/> |
|Meeting_End_Date/Time  <br/> ||모임 항목이 종료 된 날짜 및 시간입니다.  <br/> |예  <br/> |예  <br/> |
|File_relevance_score  <br/> |적합성  <br/> |관련성 점수 (0-100)입니다. 문제 당  <br/> |예  <br/> |예  <br/> |
|Family_relevance_score  <br/> |적합성  <br/> |최대 제품군 관련성 점수 (0-100) 문제 당  <br/> |예  <br/> |예  <br/> |
|Relevance_tag  <br/> |적합성  <br/> |파일에 태그를 지정 하 여 해당 파일을 수동으로 관련성이 있는 경우 문제 당  <br/> |예  <br/> |예  <br/> |
|Relevance_load_group  <br/> |적합성  <br/> |문제 당 필드를 포함 하 여 지정 된 파일의 관련성 로드 그룹  <br/> |예  <br/> |예  <br/> |
|Normalized_relevance_score  <br/> |적합성  <br/> |정규화 된 관련성 점수 (0-100)-문제와 부하 사이에 비교 합니다.  <br/> |예  <br/> |예  <br/> |
|Marked_as_seed  <br/> |적합성  <br/> |파일에 태그를 지정 하 여 문제/범주에 따라 관련성 있는 시드 파일로 설정 된 경우  <br/> |예  <br/> |예  <br/> |
|Marked_as_pre-태그가 지정 된  <br/> |적합성  <br/> |파일에 태그를 지정 하 여 문제/범주에 대 한 관련성을 사전에 설명한 것으로 설정 된 경우  <br/> |예  <br/> |예  <br/> |
|Relevance_status_description  <br/> |적합성  <br/> |관련성 상태에 대 한 설명입니다.  <br/> |예  <br/> |예  <br/> |
|설명  <br/> |일반  <br/> |사용자가 입력 한 메모입니다.  <br/> |예  <br/> |예  <br/> |
|Export_input_path  <br/> |처리   <br/> |내보내기 입력 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Pivot_ID  <br/> |중복에 근접  <br/> |파일의 피벗 ID입니다.  <br/> |예  <br/> |예  <br/> |
|Family_size  <br/> |처리   <br/> |패밀리에 있는 파일의 수입니다.  <br/> |예  <br/> |예  <br/> |
|Native_type  <br/> |처리   <br/> |네이티브 파일 형식입니다. 예를 들면 스프레드시트나 presentation입니다.  <br/> |예  <br/> |예  <br/> |
|Native_MD5  <br/> |처리   <br/> |네이티브 파일의 MD5 해시 값입니다.  <br/> |예  <br/> |예  <br/> |
|Native_size  <br/> |처리   <br/> |기본 파일 크기  <br/> |예  <br/> |예  <br/> |
|Native_extension  <br/> |처리   <br/> |네이티브 파일 확장명입니다.  <br/> |예  <br/> |예  <br/> |
|Doc_date_modified  <br/> |문서 속성  <br/> |파일의 메타 데이터에서 원시 파일을 수정한 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Doc_date_created  <br/> |문서 속성  <br/> |파일의 메타 데이터에서 가져온 원시 파일을 만든 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Doc_modified_by  <br/> |문서 속성  <br/> |파일의 메타 데이터로 가져온 기본 파일을 수정한 사용자입니다.  <br/> |예  <br/> |예  <br/> |
|O365_date_modified  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 원시 파일을 수정한 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|O365_date_created  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 원시 파일을 만든 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|O365_modified_by  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 기본 파일을 마지막으로 수정한 사용자입니다.  <br/> |예  <br/> |예  <br/> |
|Compound_path  <br/> |처리   <br/> |복합 원본을 포함 하는 네이티브 파일 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Input_path  <br/> |처리   <br/> |입력 파일의 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Input_date_modified  <br/> |처리   <br/> |입력 파일을 마지막으로 수정한 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|ND_ET_sort_excl_attach  <br/> |분석  <br/> |검토용 전자 메일 설정 및 ND 집합 연결 ' m '은 ND 집합에 접두사로 추가 되 고 ' E '는 전자 메일 ssets에 추가 됩니다.  <br/> |예  <br/> |예  <br/> |
|ND_ET_sort_incl_attach  <br/> |분석  <br/> |전자 메일 설정 및 검토용으로 설정 된 nd ' m '은 nd 집합에 접두사로 추가 되 고 ' E '는 전자 메일 집합에 추가 됩니다. 또한 Email_set 내의 각 전자 메일에 해당 하는 첨부 파일이 포함 됩니다.  <br/> |예  <br/> |예   <br/> |
|Deduped_custodians  <br/> |일반  <br/> |duped 파일의 Custodians  <br/> |예  <br/> |예   <br/> |
|Deduped_file_IDs  <br/> |일반  <br/> |duped 파일의 id  <br/> |예  <br/> |예   <br/> |
|Deduped_paths  <br/> |일반  <br/> |duped 파일의 경로  <br/> |예  <br/> |예   <br/> |
|File_key  <br/> |일반  <br/> |나중에 사용할 내부 식별자입니다.  <br/> |예  <br/> |예   <br/> |
|Export_native_path  <br/> |처리   <br/> |내보내기 패키지에 있는 네이티브 파일의 경로입니다.  <br/> |예  <br/> |예   <br/> |
|Extracted_text_path  <br/> |처리   <br/> |압축을 푼 파일의 경로입니다.  <br/> |예  <br/> |예   <br/> |
|Process_batch  <br/> |처리   <br/> |가져오기 일괄 처리에 대 한 배치 식별자입니다.  <br/> |예  <br/> |예   <br/> |
|Process_status_ID  <br/> |처리   <br/> |프로세스 단계 상태를 나타내는 식별자입니다.  <br/> |예  <br/> |예   <br/> |
|Process_status_description  <br/> |처리   <br/> |프로세스 단계 상태 설명: 성공 또는 오류 설명입니다.  <br/> |예  <br/> |예   <br/> |
|Export_status_ID  <br/> |처리   <br/> |내보내기 상태의 ID입니다.  <br/> |예  <br/> |예   <br/> |
|Export_status_description  <br/> |처리   <br/> |내보내기 상태에 대 한 설명입니다. 성공 또는 오류에 대 한 설명입니다.  <br/> |예  <br/> |예   <br/> |
|Read_percent  <br/> |적합성  <br/> |읽기% (0-100) 문제 당  <br/> |예  <br/> |예   <br/> |
|Doc_author  <br/> |문서 속성  <br/> |문서 속성: 만든이  <br/> |아니요  <br/> |예  <br/> |
|Doc_comments  <br/> |문서 속성  <br/> |문서 속성: 메모  <br/> |아니요  <br/> |예  <br/> |
|Doc_keywords  <br/> |문서 속성  <br/> |문서 속성: 키워드  <br/> |아니요  <br/> |예  <br/> |
|Doc_last_saved_by  <br/> |문서 속성  <br/> |문서 속성: 마지막으로 저장 한 사람  <br/> |아니요  <br/> |예  <br/> |
|Doc_revision  <br/> |문서 속성  <br/> |문서 속성: 수정 번호입니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_subject  <br/> |문서 속성  <br/> |문서 속성: 제목  <br/> |아니요  <br/> |예  <br/> |
|Doc_template  <br/> |문서 속성  <br/> |문서 속성: template  <br/> |아니요  <br/> |예  <br/> |
|Doc_title  <br/> |문서 속성  <br/> |문서 속성: 제목  <br/> |아니요  <br/> |예  <br/> |
|Email_has_attachment  <br/> |전자 메일  <br/> |전자 메일에 첨부 파일이 하나 이상 있는지를 나타냅니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_importance  <br/> |전자 메일  <br/> |전자 메일 중요도 속성  <br/> |아니요  <br/> |예  <br/> |
|Email_level  <br/> |전자 메일  <br/> |전자 메일 스레드 내에서 전자 메일의 수준을 나타냅니다. 첨부 파일의 경우 첨부 된 전자 메일의 값입니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_recipients  <br/> |전자 메일  <br/> |전자 메일 받는 사람 이름, 참조 및 숨은 참조  <br/> |아니요  <br/> |예  <br/> |
|Email_security  <br/> |전자 메일  <br/> |전자 메일 보안 속성  <br/> |아니요  <br/> |예  <br/> |
|Email_sensitivity  <br/> |전자 메일  <br/> |전자 메일 민감도 속성  <br/> |아니요  <br/> |예  <br/> |
|Export_batch  <br/> |처리   <br/> |파일의 마지막 내보내기 일괄 처리 이름입니다.  <br/> |아니요  <br/> |예  <br/> |
|Export_session  <br/> |처리   <br/> |파일의 마지막 내보내기 세션 Id (날짜 포함)입니다.  <br/> |아니요  <br/> |예  <br/> |
|Extracted_text_length  <br/> |처리   <br/> |추출 된 텍스트 파일의 문자 길이입니다.  <br/> |아니요  <br/> |예  <br/> |
|Family_duplicate_set  <br/> |처리   <br/> |서로 완전히 중복 되는 패밀리에 대 한 숫자 식별자입니다 (각각의 가족의 모든 구성원은 정확한 중복).  <br/> |아니요  <br/> |예  <br/> |
|Has_Text  <br/> |처리   <br/> |파일에 텍스트가 있는지 여부를 나타냅니다. 1-예.  <br/> |아니요  <br/> |예  <br/> |
|Input_file_ID  <br/> |처리   <br/> |파일을 추출한 입력 파일의 ID입니다.  <br/> |아니요  <br/> |예  <br/> |
|Native_SHA_256  <br/> |처리   <br/> |네이티브 파일의 SHA-256 해시 값입니다.  <br/> |아니요  <br/> |예  <br/> |
|O365_authors  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 기본 파일을 수정한 사용자입니다.  <br/> |아니요  <br/> |예  <br/> |
|O365_created_by  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 기본 파일을 만든 사용자입니다.  <br/> |아니요  <br/> |예  <br/> |
|Parent_node  <br/> |전자 메일  <br/> |전자 메일 스레드의 노드를 누락 된 링크가 아닌 가장 가까운 상위 노드에 연결 합니다.  <br/> |아니요  <br/> |예  <br/> |
|Set_order_inclusives_first  <br/> |전자 메일  <br/> |전자 메일 및 첨부 파일: 카운터가 시간순으로 정렬 됩니다 (먼저 Inclusives). 문서: 먼저 피벗 및 유사성 점수에 따라 정렬 합니다.  <br/> |아니요  <br/> |예  <br/> |
|Tagged_By  <br/> |적합성  <br/> |특정 문제와 관련 하 여 파일에 태그를 지정한 사용자입니다.  <br/> |아니요  <br/> |예  <br/> |
|Word_count  <br/> |분석  <br/> |문서의 단어 수입니다.  <br/> |아니요  <br/> |예  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>관련 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[고급 eDiscovery를 사용 하 여 사례 데이터 내보내기](export-case-data-in-advanced-ediscovery.md)
  
[결과 내보내기](export-results-in-advanced-ediscovery.md)
  
[일괄 처리 기록 보기 및 이전 결과 내보내기](view-batch-history-and-export-past-results.md)
  

