# Introduction

Hagezi's Lists are converted to MiHomo mrs format. All lists are rebuilt and deployed from their original sources every day.

If you like the project and you can benefit from it, leave a :star: (top right) and become a [stargazer](https://github.com/MiHomoer/MiHomo-Hagezi/stargazers)! Thanks for your support!

# Usage

Add appropriate changes to your yaml file. You can choose one from HageziUltimate, HageziProPlus, or HageziPro.

```
dns:
  enable: true
  nameserver-policy:
    'rule-set:HageziProPlus': 'rcode://success'

rule-providers:
  HageziProPlus:
    type: http
    format: mrs
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/MiHomoer/MiHomo-Hagezi@release/HageziProPlus.mrs"
    path: ./HageziProPlus.mrs
    interval: 86400

rules:
  - RULE-SET,HageziProPlus,REJECT,no-resolve
```

By using Sniffer, you may also block requests from apps that connect directly to third-party resolvers.

```
sniffer:
  enable: true
  force-dns-mapping: true
  parse-pure-ip: true
  override-destination: true
  sniff:
    HTTP:
      ports:
        - 80
        - 8080-8880
      override-destination: true
    TLS:
      ports:
        - 443
        - 8443
      override-destination: true
    QUIC:
      ports:
        - 443
        - 8443
      override-destination: true
```

# License

This project, except for upstream sources, is licensed under the GNU GPLv3 License - see the [LICENSE](LICENSE) file for details.

All rights are reserved for All upstream sources used in this project according to their respective licenses. Please refer to [Sources](#sources) section for more details.

# Disclaimer

This repository is not affiliated, associated, authorized, endorsed by, or in any way officially connected to any of the aforementioned resources, websites, services, or any entity which this may concern, in any way.  
The data in this repository is gathered from publicly available resources and is provided as-is, intended for informational purposes only with no guarantee of accuracy, liability or availability and We are not responsible for any harm or damage that may arise from using the data in this repository. Please do your research before using any data from this repository.

# Sources

[@hagezi/dns-blocklists](https://github.com/hagezi/dns-blocklists)
