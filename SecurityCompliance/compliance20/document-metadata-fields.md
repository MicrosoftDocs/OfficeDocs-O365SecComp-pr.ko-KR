---
title: 고급 eDiscovery의 문서 메타 데이터 필드
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 33e2603aaeb4505768e76149b76dc18648250a52
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151940"
---
# <a name="document-metadata-fields-in-advanced-ediscovery"></a>고급 eDiscovery의 문서 메타 데이터 필드

다음 표에는 고급 eDiscovery의 사례에 있는 검토 집합의 문서에 대 한 메타 데이터 필드가 나와 있습니다. 이 테이블은 메타 데이터 필드의 이름, 검토 집합에서 쿼리를 실행할 때 필드를 검색할 수 있는지 여부, 검토 집합에서 선택한 문서의 파일 메타 데이터를 볼 때 필드가 있는지 여부 및 문서 a에서 필드를 포함할지 여부를 나타냅니다. 다시 내보냅니다.

| 필드 이름 | 검색 가능한 필드 이름 | 내보낸 필드 이름 | 표시 필드 이름 | 설명 |
| :- |  :- |  :- |  :- |  :- |
| 첨부 파일 콘텐츠 Id | AttachmentContentId |  | 첨부 파일 콘텐츠 Id | 항목의 첨부 파일 콘텐츠 Id입니다. |
| 첨부 파일 이름 | AttachmentNames | Attachment_Names | 첨부 파일 이름 | 첨부 파일 이름의 목록입니다. |
| 변호사 클라이언트 권한 점수 | AttorneyClientPrivilegeScore |  | 변호사 클라이언트 권한 점수 | 변호사-클라이언트 권한 모델 콘텐츠 점수입니다. |
| 만든 이 | 만든 이 | Doc_authors | 만든 이 | 문서 메타 데이터의 작성자 |
| 대상 | 대상 | Email_bcc | 대상 | 메시지 유형에 대 한 숨은 참조 필드입니다.  **DisplayName \<SMTPAddress>** 형식입니다. |
| 참조란 | 참조란 | Email_cc | 참조란 | 메시지 유형에 대 한 참조 필드입니다.  **DisplayName \<SMTPAddress>** 형식입니다. |
| 준수 레이블 | ComplianceLabels | Compliance_labels | 준수 레이블 | Office 365에 규정 준수 레이블이 적용 되었습니다. |
| 컴파운드 경로 | CompoundPath | Compound_path | 컴파운드 경로 | 항목의 원본을 설명 하는 사람이 읽을 수 있는 경로입니다. |
| 콘텐츠 | 콘텐츠 |  |  | 추출 된 항목의 텍스트입니다. |
| 대화 본문 | 대화 본문 |  | 대화 본문 | 항목의 대화 본문입니다. |
| 대화 항목 | 대화 항목 |  | 대화 항목 | 항목의 대화 주제입니다. |
| 대화 ID | ConversationId | Conversation_ID | 대화 ID | 메시지의 대화 Id입니다. |
| 대화 인덱스 |  | Conversation_index | 대화 인덱스 | 메시지의 대화 인덱스입니다. |
| 대화 Pdf 시간 | ConversationPdfTime |  | 대화 Pdf 시간 | PDF 버전의 대화를 만든 날짜입니다. |
| 대화 교정 진행 시간 | ConversationRedactionBurnTime |  | 대화 교정 진행 시간 | 채팅을 위해 PDF 버전의 대화를 만든 날짜입니다. |
| 문서를 만든 날짜 | CreatedTime | Doc_date_created | 문서를 만든 날짜 | 문서 메타 데이터에서 날짜를 만듭니다. |
| Custodian | Custodian | Custodian | Custodian | 항목이 연결 된 custodian의 이름입니다. |
| 날짜 | 날짜 | 날짜 | 날짜 | Date는 파일 형식에 따라 달라 지는 계산 필드입니다.<br />**전자 메일**: 보낸 날짜<br />**전자 메일 첨부 파일**: 마지막으로 수정한 날짜 (사용할 수 없는 경우 부모의 보낸 날짜)<br />**포함 된 문서**: 마지막으로 수정한 날짜 이며, 사용할 수 없는 경우 부모의 마지막으로 수정한 날짜입니다.<br />**SPO 문서 (최신 첨부 파일 포함)**: SharePoint 마지막으로 수정한 날짜 (사용할 수 없는 경우 문서 마지막으로 수정한 날짜)<br />**Office 이외의 문서**: 마지막으로 수정한 날짜<br />**모임**: 모임 시작 날짜<br />**음성 메일**: 보낸 날짜<br />**IM**: 보낸 날짜입니다. |
| 기타 경로 | Dedupedcompoundpath | Deduped_compound_path | 기타 경로 | 정확 하 게 중복 되는 문서의 복합형 경로 목록 (전자 메일: 콘텐츠 기반, 문서: 해시 기반) |
| 기타 custodians | DedupedCustodians | Deduped_custodians | 기타 custodians | 전자 메일에 따라 정확 하 게 중복 되는 문서의 custodians (즉, 콘텐츠 기반, 문서에 대 한 해시 기반)의 목록입니다. |
| 기타 파일 Id | DedupedFileIds | Deduped_file_IDs | 기타 파일 Id | 정확 하 게 중복 되는 문서의 파일 Id 목록 (전자 메일: 콘텐츠 기반, 문서: 해시 기반) |
| 문서 설명 | : Doccomments) | Doc_comments | 문서 설명 | 문서 메타 데이터의 설명입니다. |
| 문서 회사 |  | Doc_company | 문서 회사 | 문서 메타 데이터의 회사입니다. |
| DocIndex |  |  |  | 패밀리의 인덱스입니다. -1 또는 0은 루트가 루트 임을 의미 합니다. |
| 문서 키워드 |  | Doc_keywords | 문서 키워드 | 문서 메타 데이터의 키워드입니다. |
| 문서를 수정한 사람 |  | Doc_modified_by | 문서를 수정한 사람 | 문서 메타 데이터에서 마지막으로 수정한 날짜입니다. |
| 문서 개정판 |  | Doc_revision | 문서 개정판 | 문서 메타 데이터의 수정 버전입니다. |
| 문서 제목 |  | Doc_subject | 문서 제목 | 문서 메타 데이터의 제목입니다. |
| 문서 서식 파일 |  | Doc_template | 문서 서식 파일 | 문서 메타 데이터의 서식 파일입니다. |
| 주요 테마 | DominantTheme | Dominant_theme | 주요 테마 | 분석을 위해 계산 되는 기준 테마입니다. |
| 중복 된 하위 집합 |  | Duplicate_subset | 중복 된 하위 집합 | 정확 하 게 중복 되는 그룹 ID입니다. |
| EmailAction |  | Email_action |  | 없음, 회신 메시지의 제목 줄을 기준으로 전달 합니다. |
| 전자 메일 배달 확인 |  | Email_delivery_receipt | 전자 메일 배달 확인 | 배달 확인을 위해 인터넷 헤더에 제공 되는 전자 메일 주소입니다. |
| 얼마나 | EmailImportance | Email_importance | 얼마나 | 메시지의 중요도: **0**: 낮음; **1**: 보통; **2**: 높음 |
| EmailLevel |  | Email_level |  | 메시지가 속한 전자 메일 스레드 내의 메시지 수준을 나타냅니다. 첨부 파일은 부모 메시지의 값을 상속 합니다. |
| 전자 메일 메시지 Id |  | Email_message_ID | 전자 메일 메시지 Id | 메시지의 인터넷 메시지 Id입니다. |
| EmailReadReceipt |  | Email_read_receipt |  | 읽음 확인을 위해 인터넷 헤더에 제공 되는 전자 메일 주소입니다. |
| 전자 메일 보안 | EmailSecurity | Email_security | 전자 메일 보안 | 메시지 보안 설정: **0**: 없음; **1**: 서명 됨 **2**: 암호화 됨; **3**: 암호화 및 서명 됨 |
| 전자 메일 민감도 | EmailSensitivity | email_sensitivity | 전자 메일 민감도 | 민감도 설정: **0**: 없음; **1**: 개인; **2**: Private; **3**: CompanyConfidential. |
| 전자 메일 설정 | EmailSet | Email_set | 전자 메일 설정 | 같은 전자 메일 집합에 있는 모든 메시지의 그룹 ID입니다. |
| EmailThread |  | Email_thread |  | 전자 메일 집합 내의 메시지 위치입니다. 루트에서 현재 메시지, 즉 마침표로 구분 된 모든 노드 Id를 구성 합니다. |
| 추출 된 콘텐츠 형식 |  | Extracted_content_type | 추출 된 콘텐츠 형식 | 콘텐츠 형식을 mime 형식 형식으로 추출 합니다. 예를 들면 image/jpeg와 같이 사용할 때 |
| ExtractedTextLength |  | Extracted_text_length |  | 추출 된 텍스트의 문자 수입니다. |
| 가족 관련성 점수 케이스 1 |  | Family_relevance_score_case_issue_1 |  | 제품군 관련성 점수 1의 관련성을 구분 합니다. |
| FamilyDuplicateSet |  | Family_duplicate_set |  | 서로 완전히 중복 되는 패밀리에 대 한 숫자 식별자입니다 (콘텐츠 및 동일한 첨부 파일 모두 동일). |
| 가족 번호 | FamilyId | Family_ID | 가족 번호 | 가족 번호 모든 항목을 그룹화 합니다. 전자 메일의 경우 메시지 및 모든 첨부 파일을 포함 합니다. 문서의 경우 여기에는 문서 및 포함 된 항목이 포함 됩니다. |
| 패밀리 크기 |  | Family_size | 패밀리 크기 | 가족에 있는 문서 수입니다. |
| 파일 관련성 점수 케이스 1 |  | File_relevance_score_case_issue_1 |  | 파일 관련성 점수 사례 1과 관련성을 구분 합니다. |
| File 클래스 | FileClass | File_class | File 클래스 | SharePoint 및 OneDrive의 콘텐츠: **문서**; Exchange의 콘텐츠: **전자 메일**또는 **첨부 파일** |
| 파일 ID | 열려 | File_ID | 파일 ID | 문서 식별자가 사례 내에서 고유 합니다.|
| 파일 시스템 작성일 |  | File_system_date_created | 파일 시스템 작성일 | 파일 시스템에서 만든 날짜 (비 Office 365 데이터에만 적용 됨) |
| 파일 시스템 날짜 수정 됨 |  | File_system_date_modified | 파일 시스템 날짜 수정 됨 | 파일 시스템에서 수정한 날짜 (비 Office 365 데이터에만 적용 됨) |
| 파일 형식 | FileType |  | 파일 형식 | 파일 확장명을 기반으로 하는 항목의 파일 형식입니다. |
| 첨부 파일 있음 | HasAttachment | Email_has_attachment | 첨부 파일 있음 | 메시지에 첨부 파일이 있는지 여부를 나타냅니다. |
| 변호사 있음 | HasAttorney |  | 변호사 있음 | 하나 이상의 참가자가 변호사 목록에 있으면 True이 고, 그렇지 않으면 false입니다. 그렇지 않은 경우이 값은 False입니다. |
| HasText |  | Has_text |  | 항목에 텍스트가 있는지 여부를 나타내며, 가능한 값은 True 및 False입니다. |
| 변경할 수 없는 ID | ImmutableId | Immutable_ID | 변경할 수 없는 ID | Office 365에 저장 된 변경 불가능 한 Id입니다. |
| 포함 유형 | InclusiveType | Inclusive_type | 포함 유형 | 분석에 대해 계산 된 포괄 유형: **0** -포함 안 함 **1 개** (포함) **2 개** 포함 마이너스; **3** -포함 복사본 |
| 다음에 대 한 회신 Id |  | In_reply_to_ID | 다음에 대 한 회신 Id | 메시지의 Id에 대 한 회신에서 |
| 대표 | IsRepresentative | Is_representative | 대표 | 정확 하 게 일치 하는 모든 집합의 문서 하나는 담당자로 표시 됩니다. |
| Item 클래스 | ItemClass | Item_class | Item 클래스 | Exchange server에서 제공 하는 항목 클래스 예: **IPM. 참고 사항** |
| Last modified date | LastModifiedDate | Doc_date_modified | Last modified date | 문서 메타 데이터에서 마지막으로 수정한 날짜입니다. |
| 부하 ID | LoadId | Load_ID | 부하 ID | 항목이 검토 집합에 로드 된 부하 Id입니다. |
| 위치 | 위치 | 위치 | 위치 | 문서에서 원본으로 사용한 위치 유형을 나타내는 문자열입니다.<br />O365이 아닌 > 가져온 데이터<br />팀-> 팀<br />EXO-> Exchange<br />SPO-> SharePoint<br />비즈니스용 OneDrive-> OneDrive |
| 위치 이름 | Msrtcsip-locationname | Location_name | 위치 이름 | 항목의 원본을 식별 하는 문자열입니다.  Exchange의 경우 사서함의 SMTP 주소가 됩니다.  SharePoint 및 OneDrive의 경우 사이트 모음의 URL입니다. |
| 담당자로 표시 됨 | MarkAsRepresentative |  | 담당자로 표시 됨 | 정확히 중복 된 각 집합의 한 문서를 담당자로 표시 합니다. |
| 사전 태그가 지정 된 사례 문제 1로 표시 |  | Marked_as_pre_tagged_Case_issue_1 |  | 미리 태그가 지정 된 사례 문제점 1이 관련성에 따라 표시 됩니다. |
| 시드 사례 1로 표시 된 경우 |  | Marked_as_seed_Case_issue_1 |  | 시드 사례 1로 표시 된 경우와 관련성을 구분 합니다. |
| 모임 종료 날짜 | MeetingEndDate | Meeting_end_date | 모임 종료 날짜 | 모임의 모임 종료 날짜입니다. |
| 모임 시작 날짜 | MeetingStartDate | Meeting_start_date | 모임 시작 날짜 | 모임에 대 한 모임 시작 날짜입니다. |
| 메시지 종류 | MessageKind | Message_kind | 메시지 종류 | 검색할 메시지의 유형입니다.<br />사용 가능한 값: <br />연락처만 <br />docs <br />메일 주소 <br />externaldata <br />못한 <br />메시징을 <br />저널이 <br />모임의 <br />microsoftteams (Microsoft 팀의 채팅, 모임 및 통화에서 항목을 반환 합니다.) <br />notes <br />게시물 <br />rssfeeds <br />작업과 <br />음성 메일 |
| 네이티브 확장명 | NativeExtension | Native_extension | 네이티브 확장명 | 항목의 네이티브 확장명입니다. |
| 기본 파일 이름 | NativeFileName | Native_file_name | 기본 파일 이름 | 항목의 기본 파일 이름입니다. |
| NativeMD5 |  | Native_MD5 |  | 파일 스트림의 MD5 해시 |
| ND/ET Sort: 첨부 파일 제외 | NdEtSortExclAttach | ND_ET_sort_excl_attach | ND/ET Sort: 첨부 파일 제외 | 검토 시간을 효율적으로 정렬 하기 위해 전자 메일 설정 및 ND 집합을 연결 합니다. D는 ND 집합에 접두사로 추가 되 고 E는 전자 메일 집합에 추가 됩니다. |
| ND/ET Sort: 첨부 파일 포함 | NdEtSortInclAttach | ND_ET_sort_incl_attach | ND/ET Sort: 첨부 파일 포함 | 검토 시간을 효율적으로 정렬 하기 위해 전자 메일 설정 및 ND 집합을 연결 합니다. D는 ND 집합에 접두사로 추가 되 고 E는 전자 메일 집합에 추가 됩니다. 전자 메일 집합 내의 각 전자 메일에 해당 하는 첨부 파일이 나옵니다. |
| 정규화 된 관련성 점수 사례 1 |  | Normalized_relevance_score_case_issue_1 |  | 정규화 된 관련성 점수 사례 1과 관련성을 구분 합니다. |
| O365 제작자 |  | O365_authors | O365 제작자 | SharePoint에서 만든이입니다. |
| O365을 만든 사람 |  | O365_created_by | O365을 만든 사람 | SharePoint에서 만듭니다. |
| O365 작성일 |  | O365_date_created | O365 작성일 | SharePoint에서 만든 날짜입니다. |
| O365 날짜 수정 됨 |  | O365_date_modified | O365 날짜 수정 됨 | SharePoint에서 마지막으로 수정한 날짜입니다. |
| O365 수정한 사람 |  | O365_modified_by | O365 수정한 사람 | SharePoint에서 수정 됨 |
| 상위 ID | 아닌 parentid | Parent_ID | 상위 ID | 항목 부모의 Id입니다. |
| ParentNode |  | Parent_node |  | 전자 메일 스레드에서 가장 가까운 전자 메일 메시지입니다. |
| 상위 경로 | ParentPath | Parent_path | 상위 경로 | 항목의 직계 부모에 대 한 컴파운드 경로입니다. |
| 참가자 도메인 | ParticipantDomains | Email_participant_domains | 참가자 도메인 | 메시지 참가자의 모든 도메인 목록입니다. |
| 할당 | 할당 | Email_participants | 할당 | 메시지의 모든 참석자 목록 예: 보낸 사람, 받는 사람, 참조, 숨은 참조 |
| 피벗 ID | PivotId | Pivot_ID | 피벗 ID | 피벗의 ID입니다. |
| 잠재적으로 권한이 부여 된 | PotentiallyPrivileged | Potentially_privileged | 잠재적으로 권한이 부여 된 | True 이면 변호사 권한 검색 모델이 문서에 잠재적으로 권한이 부여 된 것으로 간주 합니다. |
| 처리 상태 | ProcessingStatus | Error_code | 처리 상태 | 항목을 검토 집합에 추가한 후의 처리 상태 |
| 사례 1 (읽기 비율) |  | Read_percent_Case_issue_1 |  | 사례 1의 관련성을 확인 합니다. |
| 백분위 수 | ReadPercentile 수 |  | 백분위 수 | 관련성에 따라 문서에 대 한 백분위 수를 읽습니다. |
| 받는 사람 수 |  | Recipient_count | 받는 사람 수 | 메시지의 받는 사람 수입니다. |
| 받는 사람 도메인 | RecipientDomains | Email_recipient_domains | 받는 사람 도메인 | 메시지를 받는 사람의 모든 도메인 목록입니다. |
| 받는 사람 | 받는 사람 | Email_recipients | 받는 사람 | 메시지의 모든 받는 사람, 참조, 숨은 참조에 대 한 목록입니다. |
| 관련성 로드 그룹 사례 문제 1 |  | Relevance_load_group_case_issue_1 |  | 관련성 로드 그룹 사례 문제점 1과 관련성을 구분 합니다. |
| 관련성 상태 설명 사례 문제점 1 |  | Relevance_status_description_Case_issue_1 |  | 관련성 상태 설명 사례 문제점 1이 관련성에 해당 합니다. |
| 관련성 태그 사례 이슈 1 |  | Relevance_tag_case_issue_1 |  | 관련성 태그 사례 이슈 관련성 1 |
| 관련성 설명 |  | Relevance_comment | 관련성 설명 | 관련성에 대 한 설명 필드입니다. |
| 관련성 점수 | RelevanceScore |  | 관련성 점수 | 관련성을 기준으로 문서의 관련성 점수입니다. |
| 관련성 태그 | RelevanceTag |  | 관련성 태그 | 관련성을 기준으로 문서의 관련성 점수입니다. |
| 대표 번호 | RepresentativeId |  | 대표 번호 | 정확히 중복 된 각 집합의 숫자 식별자입니다. |
| 보낸 사람 | 보낸 사람 | Email_sender | 보낸 사람 | 메시지 유형 (보낸 사람) 필드입니다.  **DisplayName \<SmtpAddress>** 형식입니다. |
| 보낸 사람/만든이 | SenderAuthor |  | 보낸 사람/만든이 | 항목의 보낸 사람 또는 만든이로 구성 된 계산 필드입니다. |
| 보낸 사람 도메인 | SenderDomain | Email_sender_domain | 보낸 사람 도메인 | 보낸 사람의 도메인입니다. |
| 전송할 | 전송할 | Email_date_sent | 전송할 | 메시지를 보낸 날짜입니다. |
| 순서 설정: 첫째 포함 | SetOrderInclusivesFirst | Set_order_inclusives_first | 순서 (오름차순)를 설정 합니다. | 정렬 필드-전자 메일 및 첨부 파일: 연대 시간순, 문서: 피벗 먼저 유사성 점수를 내림차순으로 사용 합니다. |
| SimilarityPercent |  | Similarity_percent |  | 유사 복제 설정의 피벗에 대 한 문서를 나타냅니다. |
| 기본 파일 크기 | 크기 | Native_size | 기본 파일 크기 | 네이티브 항목의 바이트 수입니다. |
| 제목 | 제목 | Email_subject | 제목 | 메시지의 제목입니다. |
| 제목/제목 | 호칭 제목 |  | 제목/제목 | 항목의 제목 또는 제목으로 구성 된 계산 필드입니다. |
| 사례 문제점 1 별 태그 지정 |  | Tagged_by_Case_issue_1 |  | 사례 문제점 1에 대 한이 문서를 태그가 지정 된 사용자는 관련성을 갖습니다. |
| 사이 | 사이 | 사이 | 사이 | 검토 집합에 적용 된 태그 |
| 테마 목록 | 기타 Eslist | Themes_list | 테마 목록 | 분석을 위해 계산 되는 테마 목록 |
| 제목 | 제목 | Doc_title | 제목 | 문서 메타 데이터의 제목입니다. |
| 받는 사람 | 받는 사람 | Email_to | 받는 사람 | 메시지 유형에 대 한 To 필드입니다.  형식은 **DisplayName\<SmtpAddress>** |
| 전자 메일 설정의 고유 | UniqueInEmailSet |  | 전자 메일 설정의 고유 | 전자 메일 집합에 첨부 파일이 중복 된 경우 False입니다. |
| 재구성 됨 | WasRemediated | Was_Remediated | 재구성 됨 | 항목이 재구성 된 경우 True이 고 그렇지 않으면 False입니다. |
| 단어 개수 | WordCount | Word_count | 단어 개수 | 항목의 단어 수입니다. |
||||||

  > [!NOTE]
  > Office 365에서 직접 검색할 때 검색 가능한 필드에 대 한 자세한 내용은 [키워드 쿼리 및 검색 조건을](https://docs.microsoft.com/en-us/office365/securitycompliance/keyword-queries-and-search-conditions) 참조 하 여 콘텐츠 검색