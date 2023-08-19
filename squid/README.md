# Upload squid log

## 1. Manual

### 1.1 Create modplura and version number

    echo "ModPlura-squid" > /etc/modplura

    echo "0.0.1" >> /etc/modplura

### 1.2 cat /etc/modplura

    ModPlura-squid
    0.0.1

## 2. Error

### 2.1 Problem

    FATAL : Cannot open '/var/log/plura/weblog.log' for writing.

### 2.2 How to solve

    touch /var/log/plura/weblog.log
    chmod -R 766 /var/log/plura/weblog.log
    chcon -t squid_log_t /var/log/plura/weblog.log
