##DNSENUM---DNS Enumeration, Perl ile yazılmış hedef sistem hakkında bilgi toplamaya yarayan bir araçtır. Server adı, alt alan adı, mail adresi gibi önemli bilgilere ulaşmamızı sağlar  


dnsenum aracı, ağda belirli bir hedef alan adının altyapısını keşfetmek ve güvenlik açıklarını tespit etmek için sıklıkla güvenlik testlerinde kullanılır. Aşağıdaki gibi çeşitli DNS kayıtlarını sorgulayabilir ve analiz edebilir:

-NS (Name Server): Alan adını yönlendiren DNS sunucularının kayıtları.
-MX (Mail Exchange): E-posta sunucularının kayıtları.
-A (Address): Belirli bir alan adının IPv4 adresi.
-AAAA (IPv6 Address): Belirli bir alan adının IPv6 adresi.
-CNAME (Canonical Name): Bir alan adının başka bir alan adına yönlendirilmesi.
-TXT (Text): Metin bilgileri ve SPF kayıtları gibi.
-PTR (Pointer): Bir IP adresinin alan adı.



#GENEL SEÇENEKLER:
–dnsserver <server> >Bu DNS sunucusunu A, NS ve MX sorguları için kullanın.
–enum > Kısayol seçeneği – eşittir 5 -s 15 -w.
-h, –help > Bu yardım mesajını yazdır.
–noreverse > Geriye doğru arama işlemlerini atla.
–nocolor > ANSIColor çıkışını devre dışı bırak.
–private > domain_ips.txt dosyasının sonunda özel ips’leri gösterin ve kaydedin.
–subfile <dosya> > Bu dosyaya tüm geçerli alt alanları yaz.
-t, –timeout <değer> > tcp ve udp zaman aşımı değerlerini saniye cinsinden (varsayılan: 10 sn).
–threads > <value> Farklı sorgular gerçekleştirecek iş parçacıklarının sayısı.
-v, –verbose > Ayrıntılı ol: tüm ilerlemeyi ve tüm hata iletilerini göster.

#GOOGLE HAZIRLAMA SEÇENEKLERİ:
-p, –pages <değer> Adları sıyırırken işlenecek google arama sayfalarının sayısını, varsayılan 5 sayfadır, -s anahtarı belirtilmelidir.
-s, –scrap <değer> Google’dan sıyrılacak maksimum alt alan sayısı (varsayılan 15).

#BRÜT KUVVET SEÇENEKLERİ:
-f, –file <dosya> kaba kuvvet uygulamak için bu dosyadaki alt alanları oku.
-u, –update <a | g | r | z>
-F anahtarıyla belirtilen dosyayı geçerli alt alan adlarıyla güncelleyin.
a (tümü) Tüm sonuçları kullanarak güncelleme.
g Yalnızca google kazıma sonuçlarını kullanarak güncelleme.
r Yalnızca ters arama sonuçları kullanarak güncelleme.
z Yalnızca zonetransfer sonuçlarını kullanarak güncelleme.
-r, –recursion Alt etki alanlarında özyineleme, kaba bir NS kaydı olan tüm keşfedilen alt etki alanlarını zorlar.

#WHOIS NETRANGE SEÇENEKLERİ:
-d, –delay <değer> Whois sorguları arasında beklenecek maksimum saniye değeri, değer rasgele tanımlanır, varsayılan: 3s.
-w, –whois Whois sorgularını c sınıfı ağ aralıklarıyla gerçekleştirin.
** Uyarı **: Bu, çok büyük ağlar oluşturabilir ve geriye doğru arama yapmak çok zaman alır.
TERS BAKIŞ SEÇENEKLERİ:
-e, –exclude <regexp>

Regexp ifadesiyle eşleşen PTR kayıtlarını geçersiz ana bilgisayar adlarında yararlı olan geriye doğru arama sonuçlarından hariç tutun.

#ÇIKIŞ SEÇENEKLERİ:
-o –output <dosya> XML biçiminde çıktı. MagicTree’de içe aktarılabilir (www.gremwell.com)
