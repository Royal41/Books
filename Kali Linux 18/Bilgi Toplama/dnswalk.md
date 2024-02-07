## dnswalk --nedir?

#dnswalk - araci ile zone transferleri gosteren basit bir aracdir.Kullanimi  "dnswalk domain.com." kimidir   domain `in sonuna "." (nokte) qoyulmalidir.

Dnswalk bir DNS hata ayıklayıcıdır. Belirli etki alanların bölge transferlerini gerçekleştirir ve veritabanını, hem iç tutarlılık hem de doğruluk bakımından çeşitli yollarla kontrol eder.




                                                                             
┌──(kali㉿kali)-[~]
└─$ dnswalk google.com.
Checking google.com.
Getting zone transfer of google.com. from ns1.google.com...failed
FAIL: Zone transfer of google.com. from ns1.google.com failed: corrupt packet
Getting zone transfer of google.com. from ns4.google.com...failed
FAIL: Zone transfer of google.com. from ns4.google.com failed: corrupt packet
Getting zone transfer of google.com. from ns3.google.com...failed
FAIL: Zone transfer of google.com. from ns3.google.com failed: corrupt packet
Getting zone transfer of google.com. from ns2.google.com...failed
FAIL: Zone transfer of google.com. from ns2.google.com failed: corrupt packet
BAD: All zone transfer attempts of google.com. failed!
4 failures, 0 warnings, 1 errors.
