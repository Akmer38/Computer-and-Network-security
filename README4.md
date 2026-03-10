<div align="center">

# 🌐 Computer and Network Security  
## RIP v2 Routing Configuration Lab

📡 Cisco Router Dynamic Routing Configuration using **RIP Version 2**

</div>

---

# 📑 Table of Contents

- [Lab Overview](#lab-overview)
- [Network Topology](#network-topology)
- [Interface Configuration](#interface-configuration)
- [RIP v2 Configuration](#rip-v2-configuration)
- [Traceroute Tests](#traceroute-tests)
- [Results](#results)

---

# 📘 Lab Overview

Bu lab çalışmasında aşağıdaki işlemler gerçekleştirilmiştir:

- Router interface IP yapılandırması
- Router arayüzlerinin aktif edilmesi
- **RIP Version 2 dinamik yönlendirme protokolü kurulumu**
- PC'ler arasında **traceroute testi**
- Paketlerin izlediği yolun analiz edilmesi

Kullanılan cihazlar:

| Device | Type |
|------|------|
| R6 | Router |
| R7 | Router |
| R8 | Router |
| PC1 | End Device |
| PC2 | End Device |
| PC3 | End Device |

---

# 🖥 Network Topology

    PC1
     |
    R6
   /  \
  /    \
R7 ---- R8
|        |

PC2 PC3


Bu topology üzerinde routerlar **RIP v2 protokolü ile routing bilgisi paylaşır.**

---

# 🌐 Interface Configuration

Router arayüzlerine uygun **IP adresleri ve subnet maskları** atanmıştır.

### Örnek Konfigürasyon

```bash
Router(config)# interface fastEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown

📌 Her router için aşağıdaki işlemler yapılmıştır:

Interface seçildi

IP adresi verildi

Subnet mask ayarlandı

Interface aktif edildi (no shutdown)

🔀 RIP v2 Configuration

Tüm routerlarda RIP Version 2 yapılandırılmıştır.

RIP Özellikleri
Feature	Description
Routing Type	Distance Vector
Protocol	RIP Version 2
Metric	Hop Count
Maximum Hop	15
RIP v2 Konfigürasyonu
Router(config)# router rip
Router(config-router)# version 2
Router(config-router)# network 192.168.1.0
Router(config-router)# no auto-summary

📌 Bu ayar ile routerlar:

ağ bilgilerini paylaşır

routing tablolarını otomatik günceller

📡 Traceroute Tests

Ağ bağlantısını test etmek için traceroute komutu kullanılmıştır.

Traceroute sayesinde paketlerin ağda hangi routerlardan geçtiği görülebilir.

🖥 Test 1
PC1 → PC2
PC1> tracert PC2

📷 Screenshot

(Traceroute sonucu ekran görüntüsü buraya eklenecek)
🖥 Test 2
PC1 → PC3
PC1> tracert PC3

📷 Screenshot

(Traceroute sonucu ekran görüntüsü buraya eklenecek)
📊 Results

Traceroute testleri sonucunda paketlerin aşağıdaki routerlar üzerinden geçtiği gözlemlenmiştir.

PC1 → PC2
PC1 → R6 → R7 → PC2
PC1 → PC3
PC1 → R6 → R8 → PC3

Bu sonuçlar RIP v2'nin routing bilgilerini doğru şekilde dağıttığını göstermektedir.

📌 Conclusion

Bu lab çalışmasında:

✔ Router interface yapılandırması yapılmıştır
✔ RIP v2 dinamik yönlendirme kurulmuştur
✔ PC'ler arasında bağlantı doğrulanmıştır
✔ Traceroute ile paket yolları analiz edilmiştir

<div align="center">

⭐ Computer and Network Security Lab
Dynamic Routing with RIP v2

</div> ```
