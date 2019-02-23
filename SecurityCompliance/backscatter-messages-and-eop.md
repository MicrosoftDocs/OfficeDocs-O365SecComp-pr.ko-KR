---
제목: "EOP, krowley 만든이: laurawi: it 전문. 항목: 문서 ms. 서비스: O365-seccomp ms. 사용자 지정: TN2DMC localization_priority: 정상 검색. appverid:)입니다.
- MET150 assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4. 컬렉션:
    - M365-보안 준수 설명: "발송 된 메시지는 메일 서버가 보낸 자동 바운스 메시지로, 일반적으로 들어오는 스팸의 결과로 전송 됩니다. 후방 분산 DNSBL은 후방 산란 메시지를 보내는 IP 주소의 목록입니다. 스팸 발송자 목록이 아니며 후방 분산 DNSBL에서 서버를 제거해 서는 안 됩니다. "
---

# <a name="backscatter-messages-and-eop"></a>후방 분산 메시지 및 EOP

backscatter 메시지는 일반적으로 수신 스팸의 결과로 메일 서버에서 전송 되는 자동 바운스 메시지입니다. EOP (Exchange Online Protection)는 스팸 필터링 서비스 이므로, 존재 하지 않는 받는 사람에 게 전송 되는 전자 메일 메시지와 다른 의심 스러운 대상에 게는 서비스가 거부 됩니다. 이 경우 EOP는 NDR (배달 못 함 보고서) 메시지를 생성 하 고 다시 "sender"로 배달 합니다. 스팸 메일 발송자는 메시지에서 위조 되거나 잘못 된 "보낸 사람" 주소를 자주 사용 하기 때문에 NDR이 전송 되는 발신자 주소는 후방 산란 메시지를 표시할 수 있습니다. 이 경우 EOP 네트워크와 연결 된 보내는 서버가 후방 분산 DNS 차단 목록 (DNSBL)에 나열 될 수 있습니다. 후방 분산 DNSBL은 후방 산란 메시지를 보내는 IP 주소의 목록입니다. 스팸 발송자 목록이 아니며 후방 분산 DNSBL에서 서버를 제거 하려고 하지 않습니다. 
  
> [!TIP]
> 후방 분산 웹 사이트의 지침에 따르면 들어오는 모든 메일에 대해 거부 모드를 사용하는 것은 해당 서비스의 권장 구성 또는 사용 방식이 아닙니다. 대신 안전 모드에서 사용해야 합니다. 올바른 후방 분산 구성을 구현하는 방법에 대한 자세한 내용은 [Backscatterer.org 웹 사이트](http://www.backscatterer.org/?target=usage)를 참조하세요. 
  
## <a name="for-more-information"></a>자세한 내용

[Backscatterer.org IP 목록](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
[고급 스팸 필터링 옵션](advanced-spam-filtering-asf-options.md) 의 "NDR 백 분산" 항목을 참조 하세요.
  

