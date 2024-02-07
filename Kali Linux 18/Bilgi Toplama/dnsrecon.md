## dnsrecon nedir?

# Dnsrecon  dns araclari icerisinde en kullanisli olanlari arasinda yer alir.Bircok basit parametresi sayesinde islemleri  kolayca hallede biliriz. Bu araclar sayesinde SUBDOMAIN,ip adresleri 
gibi bircik bilgiyi edinebiliriz.

misal ucun:
"-d" ile domain`imizi belirittik. "-t" parametresi "type" manasina gelir.Yani hangi tarama novunu istifade edeceyimizi qeyd edirik.
Parametreden sonra "goo" yaziriq. Bu google vasitest ile verilen domain'a aid subdomainleri cixarir.

"tld" komandi--aladi ve alanadi aid ip adreslerini tarayabiliriz.


DNSRecon, aşağıdakileri gerçekleştirme olanağı sağlar:

• Bölge Transferleri için tüm NS kayıtlarının kontrolü
• Belirli bir Alan Adı için Genel DNS Kayıtlarını Listelemek (MX, SOA, NS, A, AAAA, SPF ve TXT)
• Ortak SRV Kayıt Listeleme işlemini gerçekleştirme. Üst Düzey Alan (TLD) Genişletme
• Joker Kart Çözümü Kontrolü
• Belirli etki alanı ve sözcük listesi için alt alan ve sunucu bilgisayar A ve AAAA kayıtları üzerinde
deneme-yanılma (brute-force) işlemi
• Belli bir IP Aralığı veya CIDR için PTR Kayıt araması gerçekleştirme• Kontrol edilmek üzere bir metin dosyası içinde bulunan sunucu bilgisayar kayıtları listesindeki
A, AAAA ve CNAME Kayıtları için DNS Sunucusunda Önbelleğe Alınmış kayıtların kontrolü
• Google’ı kullanarak Yerel Ağ Listeleme Sunucu Bilgisayarları ve Alt Alanlarındaki Ortak mDNS kayıtlarını listeleme.


misal olaraq:

┌──(kali㉿kali)-[~]
└─$ dnsrecon -d yandex.com
[*] std: Performing General Enumeration against: yandex.com...
[!] Wildcard resolution is enabled on this domain
[!] It is resolving to any.yandex.ru
[!] It is resolving to 213.180.204.242
[!] All queries will resolve to this list of addresses!!
[-] DNSSEC is not configured for yandex.com
[*]      SOA ns1.yandex.ru 213.180.193.1
[*]      SOA ns1.yandex.ru 2a02:6b8::1
[*]      NS ns2.yandex.net 93.158.134.1
[*]      Bind Version for 93.158.134.1 "Yandex"
[*]      NS ns2.yandex.net 2a02:6b8:0:1::1
[*]      NS ns1.yandex.net 213.180.193.1
[*]      Bind Version for 213.180.193.1 "Yandex"
[*]      NS ns1.yandex.net 2a02:6b8::1
[*]      MX mx.yandex.ru 77.88.21.249
[*]      MX mx.yandex.ru 2a02:6b8::311
[*]      A yandex.com 5.255.255.80
[*]      A yandex.com 77.88.55.80
[*]      A yandex.com 77.88.55.77
[*]      A yandex.com 5.255.255.88
[*]      AAAA yandex.com 2a02:6b8:a::a
[*]      TXT yandex.com _globalsign-domain-verification=yDcBmFPlp3bbms9ozC4F_TFMjpx_6FGwMYHLU5iMM_
[*]      TXT yandex.com google-site-verification=FVk3gum7zZLdkqi96ypScROFMew0wMetq1Gpu4rkzPI
[*]      TXT yandex.com v=spf1 redirect=_spf.yandex.ru
[*]      TXT yandex.com 5849d1f0fc8a9e73d82dfed9f2c33931
[*]      TXT yandex.com facebook-domain-verification=gy3xj2e9mxu0vtcdgqcznoaxoaiv63
[*]      TXT yandex.com facebook-domain-verification=625igbkehyfptcek6nh1hz7q4s3h4a
[*]      TXT yandex.com _globalsign-domain-verification=5sDCV_WyeQA0MbiQ08EA7XQInb69bIINmwk_kLWfbR
[*]      TXT yandex.com _globalsign-domain-verification=miGQwresT1atzJyTrdpRtWq69tXhd_6bgMdCRotJZd
[*]      TXT yandex.com _globalsign-domain-verification=9PNcUbwBZ9H47gDTJoRVTT1rrVGj2IZsaFFL4dEVA7
[*]      TXT yandex.com _globalsign-domain-verification=zJjMlP1B6Q7ytzSIa3SU664oS9Q2g9rx7BXcFhbVxD
[*]      TXT _dmarc.yandex.com v=DMARC1; p=none; fo=1; rua=mailto:dmarc_agg@auth.returnpath.net,mailto:dmarc-rua@yandex.ru; ruf=mailto:dmarc_afrf@auth.returnpath.net
[*] Enumerating SRV Records
[+]      SRV _xmpp-server._tcp.yandex.com xmpp.yandex.ru 213.180.204.242 5269
[+]      SRV _xmpp-server._tcp.yandex.com xmpp.yandex.ru 2a02:6b8::242 5269
[+]      SRV _xmpp-client._tcp.yandex.com xmpp.yandex.ru 213.180.204.242 5222
[+]      SRV _xmpp-client._tcp.yandex.com xmpp.yandex.ru 2a02:6b8::242 5222
[+]      SRV _imaps._tcp.yandex.com imap.yandex.ru 77.88.21.125 993
[+]      SRV _imaps._tcp.yandex.com imap.yandex.ru 2a02:6b8::125 993
[+]      SRV _submission._tcp.yandex.com smtp.yandex.ru 77.88.21.158 587
[+]      SRV _submission._tcp.yandex.com smtp.yandex.ru 2a02:6b8::19d 587
[+] 8 Records Found



