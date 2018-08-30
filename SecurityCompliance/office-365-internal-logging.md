---
title: Office 365 엔지니어링을 위한 office 365 내부 로깅
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/18/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Office 365 엔지니어링에 대 한 내부 어떻게 로깅에 대 한 설명을 팀 작동 합니다.
ms.openlocfilehash: 1a613584b6b815524435acb20db7a8022d95e3bc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533206"
---
# <a name="internal-logging-for-office-365-engineering"></a><span data-ttu-id="d632c-103">Office 365 엔지니어링에 대한 내부 로깅</span><span class="sxs-lookup"><span data-stu-id="d632c-103">Internal Logging for Office 365 Engineering</span></span>
<span data-ttu-id="d632c-p101">이벤트와 고객을 위해 사용할 수 있는 로그 데이터 외에도 Office 365 엔지니어에 게 사용할 수 있는 내부 로그 데이터 수집 시스템도 됩니다. 다양 한 유형의 로그 데이터는 컴퓨팅 Cosmos 라는 서비스 지정 하 고 내부 큰 데이터를 Office 365 서버에서 업로드 됩니다. 각 서비스 팀 집계 및 분석을 위해 Cosmos 데이터베이스에는 해당 서버에서 감사 로그를 업로드합니다. 이 데이터 전송에 구체적으로 승인 된 포트 및 프로토콜 Office 데이터 로더 (ODL) 라는 독점 자동화 도구를 사용 하 여 FIPS 140-2-유효성을 검사 TLS 연결을 통해 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d632c-p101">In addition to the events and log data available for customers, there is also an internal log data collection system that is available to Office 365 engineers. Many different types of log data are uploaded from Office 365 servers to an internal, big data computing service called Cosmos. Each service team uploads audit logs from their respective servers into the Cosmos database for aggregation and analysis. This data transfer occurs over a FIPS 140-2-validated TLS connection on specifically approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span>

<span data-ttu-id="d632c-p102">서비스 팀에 중앙화 된 리포지토리로 Cosmos를 사용 하 여 응용 프로그램 사용, 시스템 및 운영 성능 측정 하 고 비정상적인 및 문제 또는 보안 문제를 나타낼 수 있는 패턴을 찾고 대 한 분석을 수행 합니다. 각 서비스 팀에 Cosmos, 분석를 검색 하는 기능에 따라 포함 된 로그 종종의 기준선을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d632c-p102">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues. Each service team uploads a baseline of logs into Cosmos, depending on what they are looking to analyze, that often include:</span></span>
- <span data-ttu-id="d632c-110">이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="d632c-110">Event logs</span></span>
- <span data-ttu-id="d632c-111">AppLocker 로그</span><span class="sxs-lookup"><span data-stu-id="d632c-111">AppLocker logs</span></span>
- <span data-ttu-id="d632c-112">성능 데이터</span><span class="sxs-lookup"><span data-stu-id="d632c-112">Performance data</span></span>
- <span data-ttu-id="d632c-113">System Center 데이터</span><span class="sxs-lookup"><span data-stu-id="d632c-113">System Center data</span></span>
- <span data-ttu-id="d632c-114">통화 정보 기록</span><span class="sxs-lookup"><span data-stu-id="d632c-114">Call detail records</span></span>
- <span data-ttu-id="d632c-115">체감 품질 데이터</span><span class="sxs-lookup"><span data-stu-id="d632c-115">Quality of experience data</span></span>
- <span data-ttu-id="d632c-116">IIS 웹 서버 로그</span><span class="sxs-lookup"><span data-stu-id="d632c-116">IIS Web Server logs</span></span>
- <span data-ttu-id="d632c-117">SQL Server 로그</span><span class="sxs-lookup"><span data-stu-id="d632c-117">SQL Server logs</span></span>
- <span data-ttu-id="d632c-118">Syslog 데이터</span><span class="sxs-lookup"><span data-stu-id="d632c-118">Syslog data</span></span>
- <span data-ttu-id="d632c-119">보안 감사 로그</span><span class="sxs-lookup"><span data-stu-id="d632c-119">Security audit logs</span></span>

<span data-ttu-id="d632c-p103">Cosmos에 데이터를 업로드 하기 전에 ODL 응용 프로그램 스크러빙 서비스를 사용 하 여 테 넌 트 정보 및 최종 사용자 식별 정보 등의 고객 데이터를 포함 하는 모든 필드를 난독 처리 및 이러한 필드는 해시 값을 바꿉니다. Anonymized 및 해시 된 로그 다시 작성 되며 다음 Cosmos로 업로드 됩니다. 팀이 서비스는 상관, 경고 및 보고에 대 한 Cosmos에서 자신의 데이터에 대해 범위가 지정 된 쿼리를 실행 합니다. Cosmos에서 감사 로그 데이터 보존 기간 서비스 팀;에 의해 결정 됩니다. 보안 문제 조사를 지원 하 고 규정 보존 요구를 충족 하기 위해 대부분의 감사 로그 데이터는 90 일 동안 또는 그 이상 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d632c-p103">Prior to uploading data into Cosmos, the ODL application uses a scrubbing service to obfuscate any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value. The anonymized and hashed logs are rewritten and then uploaded into Cosmos. Service teams run scoped queries against their data in Cosmos for correlation, alerting, and reporting. The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="d632c-p104">Cosmos에 저장 된 데이터를 Office 365에 대 한 액세스 권한이 부여 된 직원에 게 제한 됩니다. Microsoft 감사 기능을 담당 하는 서비스 팀 구성원의 제한 된 하위 집합을 관리 감사 기능을 제한 합니다. 이러한 팀 구성원을 수정 하거나 Cosmos에서 데이터를 삭제 하는 기능을 사용 하지 않은 및 Cosmos에 대 한 로깅 메커니즘에 모든 변경 내용을 기록 되 고 감사를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d632c-p104">Access to Office 365 data stored in Cosmos is restricted to authorized personnel. Microsoft restricts the management of audit functionality to the limited subset of service team members that are responsible for audit functionality. These team members do not have the ability to modify or delete data from Cosmos, and all changes to logging mechanisms for Cosmos are recorded and audited.</span></span>

<span data-ttu-id="d632c-p105">특정 분석을 수행 하려면 특정 응용 프로그램의 권한을 부여 하 여 분석을 위해 해당 로그 데이터를 액세스 하는 각 서비스 팀입니다. 등 Office 365 보안 팀은 독점적인 이벤트 로그 파서를 통해 Cosmos에서 데이터를 사용 하 여 관계를 지정, 경고, 및 Office 365 프로덕션 환경에서 가능한 의심 스러운 활동에 대 한 조치 가능한 보고서를 생성 합니다. 이 데이터에서 보고서, 보안 문제를 해결 하 고 서비스의 전반적인 성능이 개선 하기 위해 사용 됩니다. 특정 알림 또는 보고서를 조사 해야 추가 하는 경우 서비스 담당자는 Office 365 서비스에 다시 데이터를 가져올 수를 요청할 수 있습니다. 특정 로그 이후 Cosmos에서 가져올에 암호화 및 서비스 직원 암호 해독 키에 액세스할 수 없는, 대상 로그 권한이 부여 된 서비스 직원에 게 범위가 지정 된 결과 반환 하는 암호 해독 서비스를 통해 프로그래밍 방식으로 전달 됩니다. 이 연습에서 발견 된 모든 취약점 보고 되 고 Microsoft의 표준 보안 사고 관리 채널을 사용 하 여 에스컬레이션 합니다.</span><span class="sxs-lookup"><span data-stu-id="d632c-p105">Each service team accesses its log data for analysis by authorizing certain applications to conduct specific analysis. For example, the Office 365 Security team uses data from Cosmos through a proprietary event log parser to correlate, alert, and generate actionable reports on possible suspicious activity in the Office 365 production environment. The reports from this data are used to correct vulnerabilities, and to improve the overall performance of the service. If a specific alert or report requires further investigation, service personnel can request that data be imported back into the Office 365 service. Since the specific log being imported from Cosmos is in encrypted and service personnel do not have access to decryption keys, the target log is programmatically passed through a decryption service that returns scoped results to the authorized service personnel. Any vulnerabilities found from this exercise are reported and escalated using Microsoft's standard security incident management channels.</span></span>
