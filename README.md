# MiHomo-Hagezi
MiHomo Hagezi RuleSets

# :writing_hand: Introduction



# :computer: Usage

  nameserver-policy:
    'rule-set:HageziProPlus': 'rcode://success'

rule-providers:
  HageziProPlus:
    type: http
    format: mrs
    behavior: domain
    url: "https://fastly.jsdelivr.net/gh/MiHomoer/MiHomo-Hagezi@release/HageziProPlus.mrs"
    path: ./HageziProPlus.mrs
    interval: 86400

rules:
  - RULE-SET,HageziProPlus,REJECT,no-resolve

# :copyright: License

This project, except for upstream sources, is licensed under the GNU GPLv3 License - see the [LICENSE](LICENSE) file for details.

All rights are reserved for All upstream sources used in this project according to their respective licenses. Please refer to [Sources](#sources) section for more details.

# :package: Sources

# :warning: Disclaimer

This repository is not affiliated, associated, authorized, endorsed by, or in any way officially connected to any of the aforementioned resources, websites, services, or any entity which this may concern, in any way.  
The data in this repository is gathered from publicly available resources and is provided as-is, intended for informational purposes only with no guarantee of accuracy, liability or availability and We are not responsible for any harm or damage that may arise from using the data in this repository. Please do your research before using any data from this repository.

# :pray: Special Thanks
