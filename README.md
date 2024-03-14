# Zabbix Expiration Template

While not strictly traditional monitoring, this template offers a practical solution. There are instances where monitoring certain elements, such as the expiration date of an API key, license, or password, proves challenging. Although setting up password expiration alerts can be useful, it's not always feasible.

To address this issue, you can utilize this template. Easily apply it to a host (or create a new one) and introduce a macro containing one or more items for which you desire expiration warnings.

Macro example:
| Macro | Value |
| ------ | ------ |
| {$EXPIRATION.CHECKS} | Some API Key:2024-04-14,Some Other API Key:2024-05-12,Some License:2024-03-10 |

Make sure to use the collons and comma's

All items will be discovered and will alert. Macro's used for alerting:
| Macro | Value |
| ------ | ------ |
| {$EXPIRE.DISASTER} | 0 |
| {$EXPIRE.HIGH} | 5 |
| {$EXPIRE.AVERAGE} | 10 |
| {$EXPIRE.WARN} | 30 |
| {$EXPIRE.INFO} | 60 |

Example of the problems displaying in Zabbix:
![Screenshot](https://raw.githubusercontent.com/Zablove/zabbix_expiration_template/screenshot/main/screenshot1.png)
