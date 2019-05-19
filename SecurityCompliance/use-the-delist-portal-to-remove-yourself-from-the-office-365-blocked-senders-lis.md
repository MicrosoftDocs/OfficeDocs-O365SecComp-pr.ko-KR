---
title: 목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 4/18/2016
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: 해당 전자 메일 주소가 Office 365에 포함되는 받는 사람에게 전자 메일을 보내려고 할 때 오류 메시지가 발생하나요? 오류 메시지가 표시되지 않아야 한다고 생각될 경우 목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인을 제거할 수 있습니다.
ms.openlocfilehash: 7ad7ac050829f2014d2c16dd39ad67fb2e91a1ec
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157850"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a><span data-ttu-id="3cf13-104">목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인 제거</span><span class="sxs-lookup"><span data-stu-id="3cf13-104">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>

<span data-ttu-id="3cf13-p102">해당 전자 메일 주소가 Office 365에 포함되는 받는 사람에게 전자 메일을 보내려고 할 때 오류 메시지가 발생하나요? 오류 메시지가 표시되지 않아야 한다고 생각될 경우 목록 해제 포털을 사용하여 Office 365 수신 거부 목록에서 본인을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-p102">Are you getting an error message when you try to send an email to a recipient whose email address is in Office 365? If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the Office 365 blocked senders list.</span></span>
  
## <a name="what-is-the-office-365-blocked-senders-list"></a><span data-ttu-id="3cf13-107">Office 365 수신 거부 목록은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="3cf13-107">What is the Office 365 blocked senders list?</span></span>

<span data-ttu-id="3cf13-p103">Microsoft는 수신 거부 목록을 사용하여 스팸, 스푸핑 및 피싱 공격으로부터 고객을 보호합니다. 메일 서버의 IP 주소, 즉 메일 서버가 인터넷에서 자신을 식별하는 데 사용하는 주소는 다양한 이유 중 하나로 Office 365의 잠재적 위협으로 태그가 지정되었습니다. Office 365에서 이 목록에 IP 주소를 추가하면 Microsoft 데이터 센터를 통한 해당 IP 주소와 고객의 간의 추가 통신이 금지됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-p103">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks. Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Office 365 for one of a variety of reasons. When Office 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>
  
<span data-ttu-id="3cf13-111">다음과 같은 오류가 포함된 메일 메시지에 대한 응답이 수신되면 이 목록에 본인이 추가된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-111">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>
  
> <span data-ttu-id="3cf13-112">550 5.7.606-649 액세스 거부, 금지 된 보낸 IP [_ip 주소_]; 이 목록에서 제거를 요청 하려면을 https://sender.office.com/ 방문 하 여 지침을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="3cf13-112">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit https://sender.office.com/ and follow the directions.</span></span> <span data-ttu-id="3cf13-113">자세한 내용은 [Office 365의 전자 메일 배달 못 함 보고서](http://go.microsoft.com/fwlink/?LinkID=526653)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cf13-113">For more information please see [Email non-delivery reports in Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span></span>
  
<span data-ttu-id="3cf13-114">여기서  _IP address_는 메일 서버가 실행되는 컴퓨터의 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-114">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span> 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="3cf13-115">Office 365 목록 해제 포털을 사용하여 수신 거부 목록에서 본인을 제거하려면</span><span class="sxs-lookup"><span data-stu-id="3cf13-115">To use the Office 365 delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="3cf13-116">웹 브라우저에서 [https://sender.office.com](https://sender.office.com)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-116">In a web browser, go to [https://sender.office.com](https://sender.office.com).</span></span>
    
2. <span data-ttu-id="3cf13-p105">페이지의 지시를 따릅니다. 오류 메시지가 전송된 전자 메일 주소와 오류 메시지에 지정된 IP 주소를 사용하고 있는지 확인합니다. 방문할 때마다 하나의 전자 메일 주소 및 하나의 IP 주소만 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-p105">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>
    
3. <span data-ttu-id="3cf13-120">**전송**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-120">Click **Submit**.</span></span>
    
    <span data-ttu-id="3cf13-121">포털에서는 사용자가 제공한 전자 메일 주소로 전자 메일을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-121">The portal sends an email to the email address that you supply.</span></span> <span data-ttu-id="3cf13-122">전자 메일은 다음과 같이 표시 됩니다. ![목록 해제 포털을 통해 요청을 제출할 때 받는 전자 메일의 스크린샷](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="3cf13-122">The email will look something like the following: ![Screenshot of email received when you submit a request through the delist portal](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>
  
4. <span data-ttu-id="3cf13-123">목록 해제 포털을 사용하여 사용자에게 전송된 전자 메일의 확인 링크를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-123">Click the confirmation link in the email sent to you by the delisting portal.</span></span>
    
    <span data-ttu-id="3cf13-124">그러면 목록 해제 포털로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-124">This brings you back to the delist portal.</span></span>
    
5. <span data-ttu-id="3cf13-125">목록 해제 포털에서 **IP 목록 해제**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-125">In the delist portal, click **Delist IP**.</span></span>
    
    <span data-ttu-id="3cf13-p107">수신 거부 목록에서 IP 주소가 제거되면 해당 IP 주소에서 보낸 전자 메일 메시지가 Office 365를 사용하는 받는 사람에게 배달됩니다. 따라서 해당 IP 주소에서 보낸 전자 메일에 부적절하거나 악의적인 내용이 없는지 확인해야 합니다. 이러한 내용이 있으면 해당 IP 주소가 다시 차단될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-p107">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Office 365. So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="3cf13-128">제한이 제거 되려면 최대 1 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cf13-128">It may take up to 1 hour before restrictions are removed.</span></span>
