# OpenClash AdBlock
Ini adalah adblock untuk openclash, source list diambil dari `oisd.nl`. Source list diupdate setiap hari secara otomatis oleh bot github.

| PACK NAME | DESCRIPTION | SOURCES |
|---------|:-------:|:-----:|
OISD Big | Blocks Ads, (Mobile) App Ads, Phishing, Malvertising, Malware, Spyware, Ransomware, CryptoJacking, Scam, ... Telemetry/Analytics/Tracking (Where not needed for proper functionality) | https://big.oisd.nl/domainswild |
OISD Small | Mainly focusses on blocking ads | https://small.oisd.nl/domainswild |
OISD NSFW | Blocks porn/shock/adult sites | https://nsfw.oisd.nl/domainswild
adaway | Blocklist suitable for android / iOS, it focuses on blocking mobile ad providers. | https://adaway.org/hosts.txt |
ABPindo | It focuses on blocking Indonesian & Malaysian ads | https://github.com/ABPindo/indonesianadblockrules |

Untuk menggunakan, edit `config.yaml` pada `/etc/openclash/config/config.yaml` seperti ini:
```
rule-providers:
  oisd_big:
    type: http
    behavior: classical
    path: "./rule_provider/oisd_big.yaml"
    url: https://raw.githubusercontent.com/hillz2/openclash_adblock/main/oisd_big.yaml
    interval: 28800 # Update rules every 8 hours
    
rules:
# AdBlock
- RULE-SET,oisd_big,REJECT
```

Setelah di test dengan situs [Adblock Test](https://d3ward.github.io/toolz/adblock.html) hasilnya:

![2022-06-08-213555-1920x986-scrot.png](https://i.ibb.co/HVxLfYz/2024-01-13-185840-1920x973-scrot.png)

Hasil di situs adblock test bisa berbeda beda karena source list diupdate setiap hari.
