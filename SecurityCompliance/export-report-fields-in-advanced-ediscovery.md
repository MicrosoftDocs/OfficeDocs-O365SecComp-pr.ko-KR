---
title: Office 365 Advanced eDiscovery 보고서 필드 내보내기
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 840a5aff-ecd0-4e56-ad22-fe99bc143687
description: 고급 ediscovery 내보내기 보고서에 포함 되는 모든 필드에 설명 합니다.
ms.openlocfilehash: a578523098248bcfa16ea8ba97d756d97ba060fa
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533185"
---
# <a name="export-report-fields-in-office-365-advanced-ediscovery"></a>Office 365 Advanced eDiscovery 보고서 필드 내보내기

> [!NOTE]
> 고급 eDiscovery 조직에 대 한 고급 준수 추가 기능 또는 e 5 구독은 Office 365 E3 필요합니다. 해당 요금제에 가입한 상태 고급 eDiscovery 시도 하려는 하지 경우에 [Office 365 Enterprise e 5의 평가판 등록](https://go.microsoft.com/fwlink/p/?LinkID=698279)할 수 있습니다. 
  
이 항목의 표준 및 모든 서식 파일에 대 한 고급 eDiscovery 내보내기 보고서 필드에 설명 합니다.
  
## <a name="export-report-fields"></a>내보내기 보고서 필드

다음 표에서 각 내보내기 서식 파일에 대 한 필드를 나열합니다.
  
|**내보내기 필드 이름입니다.**|**그룹**|**설명**|**지원 되는 표준 서식 파일**|**지원 되는 모든 서식 파일**|
|:-----|:-----|:-----|:-----|:-----|
|가지고  <br/> |일반  <br/> |행 번호입니다.  <br/> |예  <br/> |예  <br/> |
|File_ID  <br/> |일반  <br/> |파일 id입니다.  <br/> |예  <br/> |예  <br/> |
|File_class  <br/> |처리   <br/> |파일 클래스입니다.  <br/> |예  <br/> |예  <br/> |
|Family_ID  <br/> |처리   <br/> |(일반적으로 전자 메일 인스턴스와 해당 첨부 파일이) 파일을 그룹화 하는데 사용 되는 숫자 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|For_review  <br/> |처리   <br/> |필드는 검토를 위해 내보내기에 포함 됨을 표시 하는 플래그입니다.  <br/> |예  <br/> |예  <br/> |
|Native_file_name  <br/> |처리   <br/> |폴더를 참조 하는 확장명 없이 기본 파일 이름입니다.  <br/> |예  <br/> |예  <br/> |
|Custodians  <br/> |일반  <br/> |파일의 더불어 합니다.  <br/> |예  <br/> |예  <br/> |
|Set_ID  <br/> |분석  <br/> |"ND 설정" 또는 "집합으로 전자 메일 을" id입니다.  <br/> |예  <br/> |예  <br/> |
|Inclusive_type  <br/> |전자 메일  <br/> |다음 값에 따라 파일 까지의 인지 여부를 나타내는: 0-하지 (포함) 1-(포함), 2-3-포괄 복사본 빼기 (포함).  <br/> |예  <br/> |예  <br/> |
|Marked_as_pivot  <br/> |거의 중복 되는 값  <br/> |파일을 피벗 인지 여부를 나타냅니다.  <br/> |예  <br/> |예  <br/> |
|Similarity_percent  <br/> |거의 중복 되는 값  <br/> |피벗 기준으로 다음과 비슷한의 백분율입니다.  <br/> |예  <br/> |예  <br/> |
|Duplicate_subset  <br/> |거의 중복 되는 값  <br/> |중복 된 하위 집합의 고유 식별자입니다. 파일에 텍스트 정확 하 게 중복 되는 값이 있는지 여부를 나타냅니다.  <br/> |예  <br/> |예  <br/> |
|날짜  <br/> |일반  <br/> |파일의 날짜 (파일 형식-전자 메일에 따라 달라 집니다: 보낸 날짜, 문서: 수정한 날짜).  <br/> |예  <br/> |예  <br/> |
|Dominant_theme  <br/> |분석  <br/> |파일의 기본 테마입니다.  <br/> |예  <br/> |예  <br/> |
|Themes_list  <br/> |테마  <br/> |테마 이름의 목록입니다.  <br/> |예  <br/> |예  <br/> |
|ND_set  <br/> |EquiSet  <br/> |Nearduplicate 집합의 고유 숫자 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|Email_set  <br/> |전자 메일  <br/> |전자 메일의 고유한 숫자 식별자를 설정합니다.  <br/> |예  <br/> |예  <br/> |
|Email_thread  <br/> |전자 메일  <br/> |설명 내 전자 메일에서 전자 메일의 위치를 루트에서 모든 노드 Id의 Consists 마침표로 구분 하 여 현재 전자 메일을 설정 합니다.  <br/> |예  <br/> |예  <br/> |
|Email_subject  <br/> |전자 메일  <br/> |전자 메일의 제목입니다.  <br/> |예  <br/> |예  <br/> |
|Email_date_sent  <br/> |전자 메일  <br/> |전자 메일 전송 된 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Email_participants  <br/> |전자 메일  <br/> |누락 된 링크를 포함 하 여 전자 메일 스레드의 모든 참가자의 전자 메일 주소입니다.  <br/> |예  <br/> |예  <br/> |
|Email_participant_domains  <br/> |전자 메일  <br/> |누락 된 링크에 대 한 포함 하 여 전자 메일 스레드에서 모든 참가자의 도메인입니다.  <br/> |예  <br/> |예  <br/> |
|Email_sender  <br/> |전자 메일  <br/> |전자 메일 보낸사람 이름 및/또는 주소입니다.  <br/> |예  <br/> |예  <br/> |
|Email_sender_domain  <br/> |전자 메일  <br/> |보낸 사람의 도메인으로 전자 메일을 합니다.  <br/> |예  <br/> |예  <br/> |
|Email_to  <br/> |전자 메일  <br/> |전자 메일의 받는 사람에 게 있습니다.  <br/> |예  <br/> |예  <br/> |
|Email_cc  <br/> |전자 메일  <br/> |전자 메일의 받는 사람을 참조 합니다.  <br/> |예  <br/> |예  <br/> |
|Email_bcc  <br/> |전자 메일  <br/> |전자 메일의 숨은 참조 받는 사람입니다.  <br/> |예  <br/> |예  <br/> |
|Email_recipient_domains  <br/> |전자 메일  <br/> |받는 사람에 게 전자 메일 도메인 (받는, 받는 사람, 참조 및 숨은 참조)을 선택 합니다.  <br/> |예  <br/> |예  <br/> |
|Email_date_received  <br/> |전자 메일  <br/> |전자 메일을 받은 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Email_action  <br/> |전자 메일  <br/> |값: 전자 메일 제목에 따라: "앞 으로" (에 대 한 "펌웨어:"), "회신" (에 대 한 "RE:") 또는 "다른" (다른 제목 텍스트).  <br/> |예  <br/> |예  <br/> |
|Meeting_Start_Date/시간  <br/> ||날짜 및 모임 항목을 시작 하는 시간입니다.  <br/> |예  <br/> |예  <br/> |
|Meeting_End_Date/시간  <br/> ||날짜 및 모임 항목을 종료 된 시간입니다.  <br/> |예  <br/> |예  <br/> |
|File_relevance_score  <br/> |관련성  <br/> |관련성 점수 (0-100). 당 미화 합니다.  <br/> |예  <br/> |예  <br/> |
|Family_relevance_score  <br/> |관련성  <br/> |최대 제품군 관련성 점수 (0-100). 당 미화 합니다.  <br/> |예  <br/> |예  <br/> |
|Relevance_tag  <br/> |관련성  <br/> |파일을 관련성에 태그가 지정 된 수동으로 하는 경우 파일의 태그 지정 합니다. 당 미화 합니다.  <br/> |예  <br/> |예  <br/> |
|Relevance_load_group  <br/> |관련성  <br/> |문제 당 field로 지정된 된 파일의 관련성 부하 그룹  <br/> |예  <br/> |예  <br/> |
|Normalized_relevance_score  <br/> |관련성  <br/> |정규화 된 관련성 점수 (0-100)이 고, 문제 및 부하 간에와 비슷합니다.  <br/> |예  <br/> |예  <br/> |
|Marked_as_seed  <br/> |관련성  <br/> |문제/범주 관련성 당에서 시드 파일로 수로 설정 된 경우 파일의 태그 지정 합니다.  <br/> |예  <br/> |예  <br/> |
|Marked_as_pre 태그가 지정 된  <br/> |관련성  <br/> |문제/범주의 관련성 당 미리 태그가 지정 된로 설정 되었을 경우 파일의 태그 지정 합니다.  <br/> |예  <br/> |예  <br/> |
|Relevance_status_description  <br/> |관련성  <br/> |관련성 상태에 대 한 설명입니다.  <br/> |예  <br/> |예  <br/> |
|설명  <br/> |일반  <br/> |다음은 사용자가 입력 한 설명입니다.  <br/> |예  <br/> |예  <br/> |
|Export_input_path  <br/> |처리   <br/> |경로 입력된 하는 내보내기입니다.  <br/> |예  <br/> |예  <br/> |
|Pivot_ID  <br/> |거의 중복 되는 값  <br/> |파일의 피벗 ID입니다.  <br/> |예  <br/> |예  <br/> |
|Family_size  <br/> |처리   <br/> |제품군에 있는 파일의 수입니다.  <br/> |예  <br/> |예  <br/> |
|Native_type  <br/> |처리   <br/> |기본 파일 형식입니다. 예, 스프레드시트 또는 프레젠테이션 합니다.  <br/> |예  <br/> |예  <br/> |
|Native_MD5  <br/> |처리   <br/> |기본 파일의 MD5 해시 값입니다.  <br/> |예  <br/> |예  <br/> |
|Native_size  <br/> |처리   <br/> |기본 파일 크기입니다.  <br/> |예  <br/> |예  <br/> |
|Native_extension  <br/> |처리   <br/> |기본 파일 확장명입니다.  <br/> |예  <br/> |예  <br/> |
|Doc_date_modified  <br/> |문서 속성  <br/> |파일의 메타 데이터에서 가져온 네이티브 파일 수정 된 날짜입니다.  <br/> |예  <br/> |예  <br/> |
|Doc_date_created  <br/> |문서 속성  <br/> |기본 파일을 만든 날짜, 파일의 메타 데이터에서 만든 합니다.  <br/> |예  <br/> |예  <br/> |
|Doc_modified_by  <br/> |문서 속성  <br/> |파일의 메타 데이터에서 수행 하는 기본 파일을 수정한 사용자입니다.  <br/> |예  <br/> |예  <br/> |
|O365_date_modified  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 날짜 네이티브 파일 수정 되었습니다.  <br/> |예  <br/> |예  <br/> |
|O365_date_created  <br/> |문서 속성  <br/> |네이티브 파일을 만든 날짜, SharePoint 또는 Exchange 필드에서 가져옵니다.  <br/> |예  <br/> |예  <br/> |
|O365_modified_by  <br/> |문서 속성  <br/> |마지막으로 수정한 사용자 네이티브 파일을 SharePoint 또는 Exchange 필드에서 가져옵니다.  <br/> |예  <br/> |예  <br/> |
|Compound_path  <br/> |처리   <br/> |복합 소스를 포함 하 여 기본 파일 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Input_path  <br/> |처리   <br/> |입력된 파일의 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Input_date_modified  <br/> |처리   <br/> |날짜 입력 파일을 마지막으로 수정한 합니다.  <br/> |예  <br/> |예  <br/> |
|ND_ET_sort_excl_attach  <br/> |분석  <br/> |연결 된 전자 메일을 설정 하 고 검토를 위해 nd 등을 설정 합니다. 명의 ' 접두사 ND 집합 및 'E'를 전자 메일 ssets에 추가 됨에 따라 추가 됩니다.  <br/> |예  <br/> |예  <br/> |
|ND_ET_sort_incl_attach  <br/> |분석  <br/> |연결 된 전자 메일을 설정 하 고 검토를 위해 설정 ND는 ' ND 집합 및 'E'에 접두사 추가 됨에 따라 추가를 전자 메일 설정 합니다. 또한 각 전자 메일 프로그램 Email_set 내에서 적절 한 해당 첨부 파일이 옵니다.  <br/> |예  <br/> |예  <br/> |
|Deduped_custodians  <br/> |일반  <br/> |취소 duped 파일의 custodians  <br/> |예  <br/> |예  <br/> |
|Deduped_file_IDs  <br/> |일반  <br/> |취소 duped 파일의 Id  <br/> |예  <br/> |예  <br/> |
|Deduped_paths  <br/> |일반  <br/> |취소 duped 파일의 경로  <br/> |예  <br/> |예  <br/> |
|File_key  <br/> |일반  <br/> |나중에 사용할 수에 대 한 내부 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|Export_native_path  <br/> |처리   <br/> |내보내기 패키지에서 네이티브 파일의 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Extracted_text_path  <br/> |처리   <br/> |추출 된 파일의 경로입니다.  <br/> |예  <br/> |예  <br/> |
|Process_batch  <br/> |처리   <br/> |일괄 가져오기에 대 한 일괄 처리 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|Process_status_ID  <br/> |처리   <br/> |프로세스 단계 상태를 나타내는 하는 식별자입니다.  <br/> |예  <br/> |예  <br/> |
|Process_status_description  <br/> |처리   <br/> |처리 단계 상태 설명: 성공 또는 오류 설명 합니다.  <br/> |예  <br/> |예  <br/> |
|Export_status_ID  <br/> |처리   <br/> |내보내기 상태의 ID입니다.  <br/> |예  <br/> |예  <br/> |
|Export_status_description  <br/> |처리   <br/> |내보내기 상태의 설명 성공 또는 오류 설명 합니다.  <br/> |예  <br/> |예  <br/> |
|Read_percent  <br/> |관련성  <br/> |읽기 % (0-100)입니다. 당 미화 합니다.  <br/> |예  <br/> |예  <br/> |
|Doc_author  <br/> |문서 속성  <br/> |문서 속성: 만든이입니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_comments  <br/> |문서 속성  <br/> |문서 속성: 설명 합니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_keywords  <br/> |문서 속성  <br/> |문서 속성: 키워드입니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_last_saved_by  <br/> |문서 속성  <br/> |문서 속성: 마지막으로 저장 합니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_revision  <br/> |문서 속성  <br/> |문서 속성: 수정 버전 번호입니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_subject  <br/> |문서 속성  <br/> |문서 속성: 제목입니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_template  <br/> |문서 속성  <br/> |문서 속성: 서식 파일입니다.  <br/> |아니요  <br/> |예  <br/> |
|Doc_title  <br/> |문서 속성  <br/> |문서 속성: 제목입니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_has_attachment  <br/> |전자 메일  <br/> |전자 메일에 하나 이상의 첨부 하는 경우를 나타냅니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_importance  <br/> |전자 메일  <br/> |전자 메일 중요도 속성입니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_level  <br/> |전자 메일  <br/> |전자 메일 스레드 내에서 전자 메일의 수준을 나타냅니다. 첨부 파일을 첨부 된 전자 메일의 값입니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_recipients  <br/> |전자 메일  <br/> |받는 사람에 게 전자 메일 이름 및/또는 (받는, 받는 사람, 참조 및 숨은 참조) 주소 하십시오.  <br/> |아니요  <br/> |예  <br/> |
|Email_security  <br/> |전자 메일  <br/> |전자 메일 보안 속성입니다.  <br/> |아니요  <br/> |예  <br/> |
|Email_sensitivity  <br/> |전자 메일  <br/> |전자 메일 sensitivity 속성입니다.  <br/> |아니요  <br/> |예  <br/> |
|Export_batch  <br/> |처리   <br/> |파일의 마지막 내보내기 일괄 처리 이름입니다.  <br/> |아니요  <br/> |예  <br/> |
|Export_session  <br/> |처리   <br/> |파일의 마지막 내보내기 세션 Id를 포함 하 여 날짜입니다.  <br/> |아니요  <br/> |예  <br/> |
|Extracted_text_length  <br/> |처리   <br/> |추출 된 텍스트 파일의 문자 길이입니다.  <br/> |아니요  <br/> |예  <br/> |
|Family_duplicate_set  <br/> |처리   <br/> |다른 사용자의 텍스트 정확 하 게 중복 되는 제품군에 대 한 숫자 식별자 (각각-: 정확히 중복 되는 제품군의 모든 구성원).  <br/> |아니요  <br/> |예  <br/> |
|Has_Text  <br/> |처리   <br/> |파일에는 텍스트 인지 여부를 나타내는: 0-없음; 1-예입니다.  <br/> |아니요  <br/> |예  <br/> |
|Input_file_ID  <br/> |처리   <br/> |파일을 추출 하는 입력 파일의 ID입니다.  <br/> |아니요  <br/> |예  <br/> |
|Native_SHA_256  <br/> |처리   <br/> |기본 파일의 s h A-256 해시 값입니다.  <br/> |아니요  <br/> |예  <br/> |
|O365_authors  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 네이티브 파일을 수정 하는 사용자입니다.  <br/> |아니요  <br/> |예  <br/> |
|O365_created_by  <br/> |문서 속성  <br/> |SharePoint 또는 Exchange 필드에서 가져온 네이티브 파일을 만든 사용자입니다.  <br/> |아니요  <br/> |예  <br/> |
|Parent_node  <br/> |전자 메일  <br/> |전자 메일 스레드의 노드를 누락 된 링크 하지 않은 가장 가까운 부모 노드 관련이 있습니다.  <br/> |아니요  <br/> |예  <br/> |
|Set_order_inclusives_first  <br/> |전자 메일  <br/> |전자 메일 및 첨부 파일: 시간순 카운터 (Inclusives 첫번째). 문서: 피벗 다음과 비슷한 점수를 내림차순으로 처음 하 고 나머지 되 합니다.  <br/> |아니요  <br/> |예  <br/> |
|Tagged_By  <br/> |관련성  <br/> |관련성에 파일을 태그가 지정 된 특정 문제에 대 한 사용자입니다.  <br/> |아니요  <br/> |예  <br/> |
|Word_count  <br/> |분석  <br/> |다음은 문서에 있는 단어의 수입니다.  <br/> |아니요  <br/> |예  <br/> |
|||||||||||
||||||
||||||
   
## <a name="related-topics"></a>관련 항목

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[고급 eDiscovery 사용 하 여 사례 데이터 내보내기 (영문)](export-case-data-in-advanced-ediscovery.md)
  
[결과 내보내기 (영문)](export-results-in-advanced-ediscovery.md)
  
[일괄 처리 기록 보기 및 이전 결과 내보내기](view-batch-history-and-export-past-results.md)
  

