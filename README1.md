🛡️ Computer and Network Security
📡 Cisco Show Commands Guide

Bu doküman, Cisco Router ve Switch cihazlarında kullanılan temel show komutlarını açıklamak amacıyla hazırlanmıştır.

📌 Bu komutlar sayesinde:

cihaz yapılandırması incelenebilir

ağ bağlantıları kontrol edilebilir

sistem durumu analiz edilebilir

hata ve log kayıtları görüntülenebilir

📚 İçindekiler

🔧 Configuration Commands

🌐 Interface Commands

🖥️ System Commands

🔀 Network Commands

📊 Monitoring Commands

🔧 Configuration Commands
1️⃣ show running-config

📌 Cihazın aktif yapılandırmasını gösterir

Bu komut cihazın RAM üzerinde çalışan mevcut konfigürasyonunu görüntüler.

⚠️ Eğer yapılandırma kaydedilmezse cihaz yeniden başlatıldığında kaybolur.

💻 Komut
Router# show running-config
2️⃣ show startup-config

📌 Cihazın başlangıç yapılandırmasını gösterir

Bu komut NVRAM içinde kayıtlı olan konfigürasyonu görüntüler.

📌 Router yeniden başlatıldığında bu yapılandırma yüklenir.

💻 Komut
Router# show startup-config
🌐 Interface Commands
3️⃣ show ip interface brief

📌 Tüm arayüzlerin özet durumunu gösterir

Bu komut aşağıdaki bilgileri hızlıca görmemizi sağlar:

✔ IP adresi
✔ Interface durumu
✔ Protocol durumu

💻 Komut
Router# show ip interface brief
📊 Örnek Çıktı
Interface              IP-Address      OK? Method Status                Protocol
FastEthernet0/0       192.168.1.1     YES manual up                    up
FastEthernet0/1       unassigned      YES unset  administratively down down
4️⃣ show interfaces

📌 Interface hakkında detaylı bilgi verir

Bu komut şu bilgileri gösterir:

📦 paket sayısı
⚠ hata sayısı
📶 bant genişliği
📊 trafik istatistikleri

💻 Komut
Router# show interfaces FastEthernet0/0
🖥️ System Commands
5️⃣ show version

📌 Cihazın sistem bilgilerini gösterir

Gösterilen bilgiler:

🧠 işlemci
💾 bellek
📀 IOS versiyonu
⏱ uptime

💻 Komut
Router# show version
📊 Örnek Çıktı
Cisco IOS Software, Version 12.4
System uptime is 2 hours, 30 minutes
Processor board ID FTX1234A1BC
Configuration register is 0x2102
6️⃣ show clock

📌 Cihazın sistem saatini gösterir

💻 Komut
Router# show clock
7️⃣ show processes

📌 CPU ve çalışan süreçleri gösterir

Bu komut sayesinde:

⚙ çalışan işlemler
📊 CPU kullanımı

görüntülenebilir.

💻 Komut
Router# show processes
🔀 Network Commands
8️⃣ show ip route

📌 Router'ın yönlendirme tablosunu gösterir

Gösterdiği bilgiler:

🌐 ağ yolları
📍 next-hop adresleri
🔁 routing protokolleri

💻 Komut
Router# show ip route
9️⃣ show arp

📌 IP – MAC eşleştirme tablosunu gösterir

ARP tablosu cihazın hangi IP adresinin hangi MAC adresine ait olduğunu gösterir.

💻 Komut
Router# show arp
📊 Örnek Çıktı
Protocol  Address          Age (min)  Hardware Addr   Type   Interface
Internet  192.168.1.10     2          00:1A:2B:3C:4D:5E  ARPA   FastEthernet0/0
🔁 Switch Commands
🔟 show mac address-table

📌 Switch üzerindeki MAC adreslerini gösterir

Bu komut sayesinde:

📡 cihazların hangi porta bağlı olduğu
🔗 MAC adresleri

görülebilir.

💻 Komut
Switch# show mac address-table
1️⃣1️⃣ show vlan brief

📌 Switch üzerindeki VLAN yapılandırmasını gösterir

💻 Komut
Switch# show vlan brief
📊 Örnek Çıktı
VLAN Name                             Status    Ports
1    default                          active    Fa0/1, Fa0/2, Fa0/3
10   Sales                            active    Fa0/4, Fa0/5
20   IT                               active    Fa0/6, Fa0/7
📊 Monitoring Commands
1️⃣2️⃣ show logging

📌 Cihazın log kayıtlarını gösterir

Bu loglar:

⚠ hatalar
ℹ bilgilendirmeler
🚨 uyarılar

içerebilir.

Router# show logging
1️⃣3️⃣ show users

📌 Cihaza bağlı kullanıcıları gösterir

Router# show users
1️⃣4️⃣ show history

📌 Girilen komut geçmişini gösterir

Router# show history
1️⃣5️⃣ show flash

📌 Flash bellekteki dosyaları listeler

Router# show flash
📌 Summary

Bu dokümanda Cisco cihazlarında kullanılan en önemli show komutları açıklanmıştır.

Bu komutlar sayesinde:

✔ cihaz yapılandırması kontrol edilir
✔ ağ bağlantıları incelenir
✔ sistem durumu analiz edilir
✔ sorun giderme yapılır
