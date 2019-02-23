---
title: office 365 엔지니어링을 위한 office 365 내부 로깅
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Office 365 엔지니어링 팀에 대 한 내부 로깅이 작동 하는 방식에 대 한 설명입니다.
ms.openlocfilehash: 68f8763b9a647de462f402e40a4c78749343dfd9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216498"
---
# <a name="internal-logging-for-office-365-engineering"></a><span data-ttu-id="752f8-103">Office 365 엔지니어링에 대한 내부 로깅</span><span class="sxs-lookup"><span data-stu-id="752f8-103">Internal Logging for Office 365 Engineering</span></span>
<span data-ttu-id="752f8-p101">고객에 게 제공 되는 이벤트 및 로그 데이터 외에 Office 365 엔지니어가 사용할 수 있는 내부 로그 데이터 수집 시스템도 있습니다. 다양 한 유형의 로그 데이터가 Office 365 서버에서 Cosmos 라는 내부, 대규모 데이터 컴퓨팅 서비스로 업로드 됩니다. 각 서비스 팀은 집계 및 분석을 위해 각 서버의 감사 로그를 Cosmos 데이터베이스에 업로드 합니다. 이 데이터 전송은 ODL (Office data Loader) 라는 전용 자동화 도구를 사용 하 여 특별히 승인 된 포트 및 프로토콜에 대해 FIPS 140-2 유효성 검사 TLS 연결을 통해 수행 됩니다. Office 365에서 감사 레코드를 수집 하 고 처리 하는 데 사용 되는 도구는 원래 감사 레코드 콘텐츠 또는 시간 순서에 대 한 영구 또는 되돌릴 수 없는 변경 작업을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="752f8-p101">In addition to the events and log data available for customers, there is also an internal log data collection system that is available to Office 365 engineers. Many different types of log data are uploaded from Office 365 servers to an internal, big data computing service called Cosmos. Each service team uploads audit logs from their respective servers into the Cosmos database for aggregation and analysis. This data transfer occurs over a FIPS 140-2-validated TLS connection on specifically approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL). The tools used in Office 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="752f8-p102">서비스 팀에서는 Cosmos을 중앙 리포지토리로 사용 하 여 응용 프로그램 사용 현황 분석을 수행 하 고, 시스템 및 운영 성과를 측정 하며, 문제 또는 보안 문제를 나타내는 abnormalities 및 패턴을 찾습니다. 각 서비스 팀은 분석 하려는 대상에 따라 다음을 포함 하는 Cosmos에 로그 초기 계획을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="752f8-p102">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues. Each service team uploads a baseline of logs into Cosmos, depending on what they are looking to analyze, that often include:</span></span>
- <span data-ttu-id="752f8-111">이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="752f8-111">Event logs</span></span>
- <span data-ttu-id="752f8-112">AppLocker 로그</span><span class="sxs-lookup"><span data-stu-id="752f8-112">AppLocker logs</span></span>
- <span data-ttu-id="752f8-113">성능 데이터</span><span class="sxs-lookup"><span data-stu-id="752f8-113">Performance data</span></span>
- <span data-ttu-id="752f8-114">System Center data</span><span class="sxs-lookup"><span data-stu-id="752f8-114">System Center data</span></span>
- <span data-ttu-id="752f8-115">통화 정보 기록</span><span class="sxs-lookup"><span data-stu-id="752f8-115">Call detail records</span></span>
- <span data-ttu-id="752f8-116">경력 데이터 품질</span><span class="sxs-lookup"><span data-stu-id="752f8-116">Quality of experience data</span></span>
- <span data-ttu-id="752f8-117">IIS 웹 서버 로그</span><span class="sxs-lookup"><span data-stu-id="752f8-117">IIS Web Server logs</span></span>
- <span data-ttu-id="752f8-118">SQL Server 로그</span><span class="sxs-lookup"><span data-stu-id="752f8-118">SQL Server logs</span></span>
- <span data-ttu-id="752f8-119">Syslog 데이터</span><span class="sxs-lookup"><span data-stu-id="752f8-119">Syslog data</span></span>
- <span data-ttu-id="752f8-120">보안 감사 로그</span><span class="sxs-lookup"><span data-stu-id="752f8-120">Security audit logs</span></span>

<span data-ttu-id="752f8-p103">Cosmos에 데이터를 업로드 하기 전에 ODL 응용 프로그램은 스크러빙 서비스를 사용 하 여 테 넌 트 정보, 최종 사용자 식별 정보 등의 고객 데이터가 포함 된 모든 필드를 해시 값으로 바꿉니다. 익명 및 해시 된 로그가 다시 작성 된 다음 Cosmos에 업로드 됩니다. 서비스 팀은 상관 관계, 경고 및 보고를 위해 Cosmos에서 데이터에 대해 범위 지정 쿼리를 실행 합니다. Cosmos의 감사 로그 데이터 보존 기간은 서비스 팀에 따라 결정 됩니다. 대부분의 감사 로그 데이터는 보안 인시던트 조사를 지원 하 고 규정 보존 요구 사항을 충족 하기 위해 90 일 이상 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="752f8-p103">Prior to uploading data into Cosmos, the ODL application uses a scrubbing service to obfuscate any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value. The anonymized and hashed logs are rewritten and then uploaded into Cosmos. Service teams run scoped queries against their data in Cosmos for correlation, alerting, and reporting. The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="752f8-p104">Cosmos에 저장 된 Office 365 데이터에 대 한 액세스 권한이 권한 있는 담당자 에게만 제한 됩니다. Microsoft는 감사 기능을 담당 하는 서비스 팀 구성원의 제한 된 하위 집합으로 감사 기능을 관리할 수 있도록 제한 합니다. 이러한 팀 구성원은 Cosmos에서 데이터를 수정 하거나 삭제할 수 없으며 Cosmos에 대 한 로깅 메커니즘에 대 한 모든 변경 내용이 기록 및 감사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="752f8-p104">Access to Office 365 data stored in Cosmos is restricted to authorized personnel. Microsoft restricts the management of audit functionality to the limited subset of service team members that are responsible for audit functionality. These team members do not have the ability to modify or delete data from Cosmos, and all changes to logging mechanisms for Cosmos are recorded and audited.</span></span>

<span data-ttu-id="752f8-p105">각 서비스 팀은 특정 분석을 수행 하도록 특정 응용 프로그램에 부여 하 여 분석을 위해 로그 데이터에 액세스 합니다. 예를 들어 office 365 보안 팀은 Cosmos의 데이터를 독점 이벤트 로그 파서를 통해 사용 하 여 Office 365 프로덕션 환경에서 의심 스러운 작업을 수행할 수 있는 보고서에 대 한 문제를 해결 하 고 생성 합니다. 이 데이터의 보고서는 취약성을 수정 하 고 서비스의 전반적인 성능을 향상 시키는 데 사용 됩니다. 특정 경고나 보고서에 대해 자세히 조사 해야 하는 경우 서비스 담당자는 데이터를 다시 Office 365 서비스로 가져오도록 요청할 수 있습니다. Cosmos에서 가져오는 특정 로그는 암호화 되 고 서비스 직원에 게 암호 해독 키에 대 한 액세스 권한이 없기 때문에, 대상 로그는 인증 된 서비스 담당자에 게 범위가 지정 된 결과를 반환 하는 암호 해독 서비스를 통해 프로그래밍 방식으로 전달 됩니다. 이 연습에서 발견 된 모든 취약성은 Microsoft의 표준 보안 인시던트 관리 채널을 사용 하 여 보고 되 고 제기 됩니다.</span><span class="sxs-lookup"><span data-stu-id="752f8-p105">Each service team accesses its log data for analysis by authorizing certain applications to conduct specific analysis. For example, the Office 365 Security team uses data from Cosmos through a proprietary event log parser to correlate, alert, and generate actionable reports on possible suspicious activity in the Office 365 production environment. The reports from this data are used to correct vulnerabilities, and to improve the overall performance of the service. If a specific alert or report requires further investigation, service personnel can request that data be imported back into the Office 365 service. Since the specific log being imported from Cosmos is in encrypted and service personnel do not have access to decryption keys, the target log is programmatically passed through a decryption service that returns scoped results to the authorized service personnel. Any vulnerabilities found from this exercise are reported and escalated using Microsoft's standard security incident management channels.</span></span>
