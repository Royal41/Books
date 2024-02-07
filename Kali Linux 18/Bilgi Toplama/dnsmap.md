## dnsmap -  nedir?


DNSMAP--bu komanda SUBDOMAİN axtariş etmək üçün istifade edilir.

misal üçün "dnsmap google.com" kimi axtariş etdikde --108 domain, 129  İP adres tapildi.Subdomainlerin İp adresinin gostermekdedir."Wordlist" şeklinde arama yapmak istersek ise "-w "  parametresinden istifade ede bilerik.


usage: dnsmap <target-domain> [options]
options:
-w <wordlist-file>
-r <regular-results-file>
-c <csv-results-file>
-d <delay-millisecs>
-i <ips-to-ignore> (useful if you're obtaining false positives)
Kod:
e.g.:
dnsmap target-domain.foo
dnsmap target-domain.foo -w yourwordlist.txt -r /tmp/domainbf_results.txt
dnsmap target-fomain.foo -r /tmp/ -d 3000
dnsmap target-fomain.foo -r ./domainbf_results.txt



