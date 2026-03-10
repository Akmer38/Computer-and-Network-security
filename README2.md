<div align="center">

# 🛡️ Computer and Network Security  
## 📡 Router Configuration Assignment

Cisco Router CLI configuration and basic networking tasks.

</div>

---

# 📑 Table of Contents

- [Assignment Overview](#assignment-overview)
- [Router Naming](#router-naming)
- [Security Configuration](#security-configuration)
- [Interface Configuration](#interface-configuration)
- [Static Routing](#static-routing)
- [Configuration Backup](#configuration-backup)
- [Router Management](#router-management)
- [Connectivity Test](#connectivity-test)

---

# 📘 Assignment Overview

Bu ödevde iki adet Cisco router kullanılarak aşağıdaki işlemler gerçekleştirilmiştir:

- Router isimlendirme
- Şifre yapılandırması
- Interface IP ayarları
- Statik yönlendirme
- TFTP ile konfigürasyon yedekleme
- Hostname tablosu kullanımı
- Router yeniden başlatma ve test

---

# 🖥 Network Topology

      10.0.0.0 /30
  +-------------------+
  |                   |

[ GAD ] ----------- [ BHM ]
| |
| |
| 192.168.55.0 /26


---

# 🏷 Router Naming

| Router | Hostname |
|------|------|
| Router 1 | **GAD** |
| Router 2 | **BHM** |

### Configuration

```bash
Router(config)# hostname GAD
Router(config)# hostname BHM
🔐 Security Configuration

Her iki router için enable şifresi ayarlanmıştır.

Configuration	Value
Enable Password	ktun2025
Password Encryption	Enabled
Commands
Router(config)# enable secret ktun2025
Router(config)# service password-encryption
🌐 Interface Configuration
GAD Router
Interface	IP Address	Subnet
FastEthernet 0/1	10.0.0.1	/30
GAD(config)# interface fastEthernet 0/1
GAD(config-if)# ip address 10.0.0.1 255.255.255.252
GAD(config-if)# no shutdown
BHM Router
Interface	IP Address	Subnet
FastEthernet 0/1	10.0.0.2	/30
FastEthernet 0/0	192.168.55.1	/26
BHM(config)# interface fastEthernet 0/1
BHM(config-if)# ip address 10.0.0.2 255.255.255.252
BHM(config-if)# no shutdown
BHM(config)# interface fastEthernet 0/0
BHM(config-if)# ip address 192.168.55.1 255.255.255.192
BHM(config-if)# no shutdown
📡 Host Table Configuration

GAD router üzerinde BHM router için hostname tablosuna kayıt eklenmiştir.

GAD(config)# ip host BHM 10.0.0.2

Bu sayede routerlar IP yerine hostname kullanarak iletişim kurabilir.

🔀 Static Routing

GAD router üzerinde aşağıdaki statik rota eklenmiştir:

Destination Network : 192.168.55.0
Subnet Mask        : 255.255.255.192
Next Hop           : 10.0.0.2
Command
GAD(config)# ip route 192.168.55.0 255.255.255.192 10.0.0.2
💾 Configuration Backup

GAD router konfigürasyonu TFTP sunucusuna yedeklenmiştir.

Backup file name:

GAD-backup
Command
GAD# copy running-config tftp
🔄 Configuration Restore

BHM router konfigürasyonu TFTP sunucusundan alınarak güncellenmiştir.

BHM# copy tftp running-config
⚙ Router Name Correction

Konfigürasyon kopyalandıktan sonra router ismi GAD olarak değişmiştir.

Tekrar BHM olarak ayarlanmıştır.

Router(config)# hostname BHM
📡 Connectivity Test

GAD routerından BHM routerına hostname kullanılarak ping gönderilmiştir.

GAD# ping BHM

⚠ İlk ping sonucunun 4/5 olması normaldir.

Bunun sebebi:

ARP tablosunun ilk ping sırasında oluşturulmasıdır.

🔁 Router Restart

BHM router yeniden başlatılmıştır.

BHM# reload

Router yeniden başladıktan sonra tekrar ping testi yapılmıştır.

GAD# ping BHM
<div align="center">

📡 Computer and Network Security
Cisco Router Configuration Lab

</div> ```
