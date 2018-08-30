---
title: Office 365 비디오에서 office 365 테 넌 트 격리
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: '요약: Office 365 비디오에서 테 넌 트 격리의 설명 합니다.'
ms.openlocfilehash: 9476047d56161ec2589fdf743d7ee837ea558865
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22533762"
---
# <a name="tenant-isolation-in-office-365-video"></a><span data-ttu-id="8a6f9-103">Office 365 비디오에서 테넌트 격리</span><span class="sxs-lookup"><span data-stu-id="8a6f9-103">Tenant Isolation in Office 365 Video</span></span>

> [!NOTE]
> <span data-ttu-id="8a6f9-p101">Office 365 비디오 Microsoft Stream으로 대체 됩니다. 인텔리전스 비디오 공동 작업을 추가 하 고 현재 Office 365 비디오 고객을 위한 전환 계획에 대 한 설명 하는 새 엔터프라이즈 비디오 서비스에 대 한 자세한 내용은, [에서 Office 365 비디오 스트림에 Migrate](https://docs.microsoft.com/stream/)를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p101">Office 365 Video will be replaced by Microsoft Stream. To learn more about the new enterprise video service that adds intelligence to video collaboration and learn about the transition plans for current Office 365 Video customers, see [Migrate to Stream from Office 365 Video](https://docs.microsoft.com/stream/).</span></span>

## <a name="introduction"></a><span data-ttu-id="8a6f9-106">소개</span><span class="sxs-lookup"><span data-stu-id="8a6f9-106">Introduction</span></span>
<span data-ttu-id="8a6f9-p102">Azure 저장소는 Office 365 비디오 및 영향을 비롯 한 여러 Office 365 서비스에 대 한 데이터를 저장 하는데 사용 됩니다. Azure 저장소는 구조화 되지 않은 데이터를 저장 하는데 사용 되는 높은 확장 가능성, REST 기반 클라우드 개체 저장소는 Blob 저장소를 포함 합니다. Azure 저장소를 사용 하 여 간단한 액세스 제어 모델입니다. Azure 각 구독에는 하나 이상의 저장소 계정을 만들 수 있습니다. 각 저장소 계정에는 해당 저장소 계정에서 모든 데이터에 대 한 액세스를 제어 하는데 사용 되는 단일 비밀 키를 있습니다. 이 메서드는 여기서 저장소가 응용 프로그램과 연결 하 고 해당 응용 프로그램 관련된 데이터;에 대해 모든 권한을 가집니다 하는 일반적인 시나리오를 지원합니다 Azure 저장소에 저장 함으로써 콘텐츠를 라 예입니다. 영향에 대 한 모든 고객 콘텐츠 공유 Azure 저장소 계정에 저장 됩니다. 각 사용자의 콘텐츠 Azure 저장소에서 blob의 별도 디렉터리 트리에 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p102">Azure Storage is used to store data for multiple Office 365 services, including Office 365 Video and Sway. Azure Storage includes Blob storage, which is a highly-scalable, REST-based, cloud object store that is used for storing unstructured data. Azure Storage uses a simple access control model; each Azure subscription can create one or more Storage Accounts. Each Storage Account has a single secret key that is used to control access to all data in that Storage Account. This supports the typical scenario where storage is associated with applications and those applications have full control over their associated data; for example, Sway storing content in Azure Storage. All customer content for Sway is stored in shared Azure storage accounts. Each user's content is in a separate directory tree of blobs in Azure storage.</span></span>

<span data-ttu-id="8a6f9-p103">고객 환경 (예: Azure 포털, SMAPI, 등)에 대 한 액세스를 관리 하는 시스템에서 Microsoft 운영 Azure 응용 프로그램 내에서 격리 됩니다. 이 논리적으로 고객 응용 프로그램 및 저장소 계층에서 고객 액세스 인프라에 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p103">The systems managing access to customer environments (e.g., the Azure Portal, SMAPI, etc.) are isolated within an Azure application operated by Microsoft. This logically separates the customer access infrastructure from the customer applications and storage layer.</span></span>

## <a name="tenant-isolation-in-office-365-video"></a><span data-ttu-id="8a6f9-116">Office 365 비디오에서 테넌트 격리</span><span class="sxs-lookup"><span data-stu-id="8a6f9-116">Tenant Isolation in Office 365 Video</span></span>
<span data-ttu-id="8a6f9-p104">[Office 365 비디오](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6) 은 게시, 공유 및 비디오 콘텐츠를 검색에 대 한 조직에 매우 안전 하 고, 조직 차원의 대상을 제공 하는 기업 포털입니다. Office 365 비디오에서는 각 테 넌 트의 비디오에 보관 되 격리 되 고 암호화 된 모든 위치 및만 사용할 수 액세스 및 조직의 비디오에 대 한 사용 권한을 가진 인증 된 사용자에 게 있습니다. Office 365 비디오 기술 조합을 사용 하 여이 수행 하기 위해.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p104">[Office 365 Video](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6) is an enterprise portal that provides organizations with a highly secure, organization-wide destination for posting, sharing, and discovering video content. In Office 365 Video, each tenant's videos are kept isolated and encrypted in all locations, and are only available to authenticated users that have access and permissions to the organization's videos. Office 365 Video uses a combination of technologies to accomplish this:</span></span>
- <span data-ttu-id="8a6f9-p105">SharePoint Online 비디오 파일 및 메타 데이터 (예: 비디오 제목, 설명)을 저장 하기 위해 사용 됩니다. 보안 및 규정 준수 계층 (인증 포함), 제공 및 기능을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p105">SharePoint Online is used for storing the video file and metadata (video title, description, etc.). It also provides the security and compliance layer (including authentication), and search features.</span></span>
- <span data-ttu-id="8a6f9-122">Azure 미디어 서비스 변환을, 환경에 적합 한 스트리밍, 안전 하 게 전달 (AES 암호화 사용) 및 축소판 그림 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-122">Azure Media Services provides transcoding, adaptive streaming, secure delivery (using AES encryption), and thumbnail features.</span></span>

<span data-ttu-id="8a6f9-p106">[Azure 미디어 서비스](https://azure.microsoft.com/services/media-services/) 는 플랫폼-로-a-서비스 클라우드에서 끝-미디어 워크플로 사용 하도록 설정 하는 것에 대 한 제공 합니다. 플랫폼 업로드, 인코딩, (PlayReady), 적용 된 암호화 및 전세계 Azure 데이터 센터를 통해 미디어 전송을 위한 REST API를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p106">[Azure Media Services](https://azure.microsoft.com/services/media-services/) is a platform-as-a-service offering for enabling end-to-end media workflows in the cloud. The platform provides a REST API for uploading, encoding, encrypting (with PlayReady), and delivery of media through Azure datacenters around the world.</span></span>

<span data-ttu-id="8a6f9-p107">Office 365 비디오에 대 한 모든 업로드 HTTPS를 통해 발생 합니다. 비디오 파일을 업로드 하는 경우 SharePoint Online에 저장 된 하 고 파일의 복사본을 Azure 미디어 서비스에는 암호화 된 채널을 통해 전송 됩니다. Azure 미디어 서비스 라우팅해야 환경 (예: 모바일, 대역폭이 낮은 고대역폭 등)를 보기 위해 최적화 된 여러 형식으로 비디오입니다. 원본 파일을 업로드 하는 동안 취득 함께 이러한 파일은 Azure Blob 저장소에 저장 됩니다. 재생을 위한 공통 암호화 m p e G 패키징 알고리즘 (또는 이전 PlayReady 버전) 당 AES 128를 사용 하 여 암호화 된 파일과 Azure Blob 저장소에 저장 되 고 전에 AES 256 저장소 암호화를 사용 하 여 암호화 합니다. (Azure 미디어 서비스 클라이언트 SDK를 사용 하 여 고객을 제어할 수 있는 암호화가 사용 됩니다. 예, 고객을 적용할 수 Azure 미디어 서비스 저장소 암호화 (AES 256) 높은 값 미디어 자산 Azure Blob 저장소를 업로드 하기 전에.)</span><span class="sxs-lookup"><span data-stu-id="8a6f9-p107">All uploads for Office 365 Video occur via HTTPS. When a video file is uploaded, it is stored in SharePoint Online, and a copy of the file is sent via an encrypted channel to Azure Media Services. Azure Media Services transcodes the video into multiple formats that are optimized for viewing experience (e.g., mobile, low-bandwidth, high-bandwidth, etc.). These files, along with the original file acquired during upload, are stored in Azure Blob storage. The files are encrypted using AES 128 per the MPEG Common Encryption packaging algorithm (or an earlier PlayReady version) for playback, and encrypted using AES 256 storage encryption before being stored in Azure Blob storage. (Using the Azure Media Services Client SDK, customers can control which encryption is used. For example, a customer could apply Azure Media Services storage encryption (AES 256) to a high-value media asset before uploading it Azure Blob storage.)</span></span>

<span data-ttu-id="8a6f9-132">Azure 미디어 서비스는 또한 암호화 된 채널을 통해 SharePoint online 축소판 그림 메타 데이터와 함께 전송 하는 비디오에 대 한 축소판 그림을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6f9-132">Azure Media Services also generates a thumbnail for the video, which it transmits along with thumbnail metadata to SharePoint Online via an encrypted channel.</span></span>
