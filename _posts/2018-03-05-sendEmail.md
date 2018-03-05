---
layout: post
title: SendEmail exchange
---

- Нстройка SendEmail + Star tls + Самоподписанный сертификат сервера

1. Установим SendEmail и доп модули
 ```bash
sudo apt install  sendemail libio-socket-ssl-perl libnet-ssleay-perl
```
2. Создать папку для сертификатов
 ```bash
sudo mkdir/usr/share/ca-certificates/vi
```
3. Открыть редактором новый файл с ключем .PKS
 ```bash
sudo vim /usr/share/ca-certificates/vi/ca-vi.crt
```
4. Добавить Ключ

```
-----BEGIN CERTIFICATE-----
MIIDbjCCAlagAwIBAgIQJKZ0oHkPC4JJLhIcBRao4DANBgkqhkiG9w0BAQsFADA/
MRMwEQYKCZImiZPyLGQBGRYDY29tMRUwEwYKCZImiZPyLGQBGRYFdml0cGMxETAP
BgNVBAMTCFZJLUNBLTAwMB4XDTExMTAwMzExMjExMFoXDTMxMTAwMzExMzEwOVow
PzETMBEGCgmSJomT8ixkARkWA2NvbTEVMBMGCgmSJomT8ixkARkWBXZpdHBjMREw
DwYDVQQDEwhWSS1DQS0wMDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEB
AL9uluSsLay4cBk7BZM/RNyXyNxuteococMTUQq9Mr1I5wVUw/wJlf1H9/OibfS2
NASqBBMxnl3r5kjAO/Hzs5CU9Id1xTf3Au712VCoYMoXbj+y0ZjwtJT4TpUet4K2
XbP/H//3qznywzk7pE+Y1HWQnOiE9ovC28VIIDnf2QbW52Q78i2R+QTVESYAGQ1t
bXIKYDyDu/g6MnGkBMoIE2TORcWdPoFuPMAeJyb98Cd51z/KA+F4CX5kOImXy6oE
wW4xMM/1ezZtbJqbrWPESjVC3GU0fiY9q0WsOaBXhMiNvVu7x45bTJjd/AWho/5V
Af3k1mthnz1RVzp4G4Mv2+0CAwEAAaNmMGQwEwYJKwYBBAGCNxQCBAYeBABDAEEw
CwYDVR0PBAQDAgGGMA8GA1UdEwEB/wQFMAMBAf8wHQYDVR0OBBYEFOOmUZSzVrCn
LT47AqSmt6I7inzrMBAGCSsGAQQBgjcVAQQDAgEAMA0GCSqGSIb3DQEBCwUAA4IB
AQAioeXe8DtY8ZxTLl6IjwX4/Hc0mE+N3vfiEuYYff8NgCLi3zC9/BUDu7/YPXkT
hOMnV1eXRKlYS5g4qisCUi5BHCOcVEWh6YmVO9bIQmHcdVgEzJniO/epYEtDRzbb
bKcrlcnl2wKpL8x9B5FU+8M6RLaQPEjJA9Qg897ip6HhQea3rVeg6F1A5GwkwQM9
PMun1eSdJnFvPDttF1OsPFAlaOqdLbC65DLVP9N2uVirijjYs1sE6yACbd1kY0zd
/vMPTS8kN6zJguapEl6BW2JBuSUKEAHKz9k8LR5JX7ithkwQ1y7c8MDUPgbGN3W5
p2q+Lq1KDIPfVRFz2N3LjIq2
-----END CERTIFICATE-----
```
5. Обновить и добавить новые сертификаты
```bash
sudo dpkg-reconfigure ca-certificates
```
6. Отправить тестовое письмо
```bash

#!/bin/sh
USER=""
PASSWORD=""

sendEmail -vvv \
 -o tls=yes \
 -f myemail@exemple.com \
 -t toemail@gmail.com \
 -s smtp.exemple.com:587 \
 -xu $USER \
 -xp $PASSWORD \
 -u "Привет Мир" \
 -m "Я отправил сообщение:  How are you? I'm testing sendEmail from the command line."

```


