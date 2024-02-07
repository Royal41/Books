## dnsdict6 -- nedir?

# bu komanda Subdomain leri axtarisi ucundur.Dnsdic6 aracı hedef sitenin domain,subdomain,mx kayıtlarını gibi bilgilerini bulmamıza yarar.


-------

Hedef sitenin sub-domainlerini bulmak için

dnsdict6 siteismi.com => yazılır...

İşimize yarıyacak parametreler

-d parametresi:
Bu parametre mx kayıtları vb. kayıtların bilgilerini Ipv4 VE Ipv6 adreslerine göre gösterilmesini sağlar.
Ipv4 için -d4, Ipv6 için -d6 parametresi kullanılır her ikisi içinde -d46 parametresi kullanılır.

Wordlistin Ayarlanabilmesi İçin Kullanılabilecek Parametreler
Dnsdic6da taramalar yaparken wordlist kullanılır normal bir wordlistin değeri 796dır ama biz buna değişik büyük-küçük değerlerde verebiliriz.

-s => Bunun değeri 50dir, Wordliste 50 değerini verir arama yaparken...
-m => Bunun değeri 796dır, Wordliste değer vermeseniz bile bu değere göre tarama yapar.
-l => Bunun değeri 1416dır, Wordliste 1416 değerini verir ve ona göre arama veya tarama yapar.
-x => Bununda değeri 3211dir...

Şimdi örnek olarak bunlarla ilgili bir kaç komut vereyim:

dnsdict6 -d4 -s Cyber-warrior.org => Bu komutta Cyber-warrior.org sitesini 50 arama değerinde, Ipv4 adresine göre tarar.
dnsdict6 -d6 -m Cyber-warrior.org => Bu komutta Cyber-warrior.org sitesini normal(-m(medium)) 796 arama değerinde, Ipv6 adresine göre arar veya tarar hangisini diyecekseniz size kalmış.
dnsdict6 -d46 -x Cyber-warrior.org => Bu komutta Cyber-warrior.org sitesini 3211 arama değerinde, Ipv4 ve Ipv6 adreslerine göre arar veya tarar.
