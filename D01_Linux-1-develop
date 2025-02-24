## Part 1. Operatsion sistemani o'rnatish
Birinchi VertualBox o'rnatdim. Keyin Ubuntu 20.04 Server LTS ni o'rnatib, chiqqan terminalga cat /etc/issue ni kiritdim. Natija quyidagicha: 
![Part 1](/src/images/image1_01.png)<br>

## Part 2. Foydalanuvchi yaratish tartibi
1. Terminalga sudo useradd -p user -s /bin/bash new=user -G adm kiritdim, ya'ni paroli user bo'lgan new=user nomli yangi foydalanuvchi yaratdim. Natija quyidagicha:
![Part 2_01](/src/images/image2_01.png)<br>

2. cat /etc/passwd komandasi bilan quyidagi natijaga erishamiz:
![Part 2_02](/src/images/image2_02.png)<br>

## Part 3. Opertsion tizim tarmog'ini sozlash
1. Mashina nomini ushbu komanda bilan sudo hostnamectl set-hostname user-1 "user-1" deb o'zgartirdim. Natija quyidagicha:
![Part 3_01](/src/images/image3_01.png)<br>

2. Vaqt zonasini yashash hududimga mos ravishda sozladim. Komanda: "sudo timedatectl set-timezone Asia/Tashkent". Natija quyidagicha:
![Part 3_02](/src/images/image3_02.png)<br>

3. Tarmoq interfeyslari nomlarini konsol buyruqlari orqali oldim. Komanda: "ip link show".
Natija quyidagicha:
![Part 3_03](/src/images/image3_03.png)<br>

4. DHCP server orqali ishlayotgan qurilmangizning IP manzilini oldim. Komanda: "ip addr show". Natija quyidagicha:
![Part 3_04](/src/images/image3_04.png)<br>

5. Tashqi IP manzilni va ichki (shlyuza) IP manzilni aniqlab, ekranga chiqarib oldim.
A* Tashqi IP manzil komandasi: curl ifconfig.me
![Part 3_05](/src/images/image3_05.png)<br>

5. B* Ichki (shlyuz) IP manzilini quyidagi komanda bilan ko'rdim: "ip route | grep default"
Natija quyidagicha:
![Part 3_06](/src/images/image3_06.png)<br>

6. Statik (qo‘lda kiritilgan) IP, GW, DNS sozlamalarini o‘rnatib, tarmoq sozlamalari faylini ushbu komanda bilan ochdim: "sudo nano /etc/netplan/01-netcfg.yaml".
![Part 3_07](/src/images/image3_07.png)<br>

Keyin faylni quyidagicha tahrir qildim:
network:
  version: 2
  ethernets:
    enp0s3:
      addresses: [192.168.1.100/24]
      gateway4: 192.168.1.1
      nameservers:
        addresses: [8.8.8.8, 1.1.1.1]
![Part 3_08](/src/images/image3_08.png)<br>

Sozlamalarni qo'lladim:
"sudo netplan apply"
![Part 3_09](/src/images/image3_09.png)<br>

7. A* Virtual mashinani "sudo reboot" bilan qayta yukladim va IP sozlamalarni ushbu komanda bilan tekshirdim: "ip addr show".
Natija quyidagicha:
![Part 3_10](/src/images/image03_10.png)<br>

B* "ip route show"
![Part 3_11](/src/images/image3_11.png)<br>

8. A* Uzoqdagi 1.1.1.1 va ya.ru xostlarini ushbu komanda yordamida ping qildim: "ping -c 4 1.1.1.1".
Natija quyidagicha:
![Part 3_12](/src/images/image3_12.png)<br>

8. B* "ping -c 4 ya.ru" komandasi bilan quyidagi natijani oldim:
![Part 3_13](/src/images/image3_13.png)<br>

## Part 4. Sistemadagi paketlarni yangilash
1. "sudo apt update" komandasi bilan quyidagi screen oldim:
![Part 4_01](/src/images/image4_01.png)<br>

2. Paketlarni oxirgi versiyaga yangilash uchun esa "sudo apt upgrade -y" buyrug'idan foydalandim. Natijada quyidagidek bo'ldi:
![Part 4_02](/src/images/image4_02.png)<br>

3. "sudo apt update" komandasini yana qaytadan terminalga kiritib, paketlar to'liq yangilangandan keyin, yangilanishlar yo'qligini tekshirib oldim.
![Part 4_03](/src/images/image4_03.png)<br>

## Part 5. **sudo** komandasidan foydalanish
1. Foydalanuvchiga "sudo" huquqini berish. Komanda: "sudo usermod -aG sudo new=user". Natija esa quyidagicha:
![Part 5_01](/src/images/image5_01.png)<br>

2. Foydalanuvchining yangi nomi bilan tizimga kirish uchun quyidagi komandadan foydalandim: 
"su - new=user". Natija quyidagicha:
![Part 5_02](/src/images/image5_02.png)<br>

3. **sudo** yordamida hostname-ni "sudo hostnamectl set-hostname new_name" o'zgartirdim. Natija quyidagicha:
![Part5_03](/src/images/image5_03.png)<br>

4. Hostname-ni "hostname" komandasi bilan tekshirdim.
![Part5_04](/src/images/image5_04.png)<br>

## Part 6. Vaqt zonasi xizmatini o'rnatish va sozlash
1. Vaqt zonasi vaqtini "timedatectl" yordamida ko'rsatdim. Natija quyidagicha:
![Part 6_01](/src/images/image6_01.png)<br>

2. NTP sinxronizatsiyasini "sudo timedatectl set-ntp true" komandasi bilan yoqish:
![Part 6_02](/src/images/image6_02.png)<br>

3. NTP sinxronizatsiya holatini "timedatectl show" komandasi bilan tekshirdim. Natija esa:
![Part 6_03](/src/images/image6_03.png)<br>

4. Vaqtni "date" komandasi bilan tekshirdim.
Natija quyidagicha:
![Part 6_04](/src/images/image6_04.png)<br>

## Part 7. Matn muharrirlarini o'rnatish va foydalanish
1. Matn muharrirlarini "sudo apt update" yordamida o'rnatdim.
![Part 7_01](/src/images/image7_01.png)<br>

- Keyin esa ushbu komandani terdim: "sudo apt install vim nano mc".
![Part 7_02](/src/images/image7_02.png)<br>

2. Vim da fayl yaratdim. "vim test_vim.txt" komandasi bilan vim fayl ochidim.
![Part 7_03](/src/images/image7_03.png)<br>

- Nickname yozdim va saqlash uchun ushbu algoritmdan foydalandim: 
* Yozish rejimiga o'tish: i tugmasini bosing.
* Nickname kiriting.
* Saqlash va chiqish uchun esa Esc → :wq → Enter tugmasini bosganimda quyidagi natija chiqdi:
![Part 7_04](/src/images/image7_04.png)<br>

- Nano-da fayl yaratdim. Uning uchun "nano test_nano.txt".
![Part 7_05](/src/images/image7_05.png)<br>

- Nickname yozish va saqlash uchun Ctrl+O → Enter → Ctrl+X algoritmini kiritganimda natija quyidagicha bo'ldi:
![Part 7_06](/src/images/image7_06.png)<br>

- MCEDIT bilan fayl yaratish uchun "mcedit test_mc.txt" komandasini terdim va quyidagi algoritmni kiritdim: Natija: F2 → 
![Part 7_07](/src/images/image7_07.png)<br>
→ F10
![Part 7_08](/src/images/image7_08.png)<br>

3. VIM faylni tahrirlash va saqlamasdan chiqish uchun ushbu buyruqdan foydalandim: "vim test_vim.txt". Keyin nickname o'rniga «21 School 21» yozib, saqlamasdan chiqish uchun esa quyidagi algoritmdan foydalandim: Esc → :q! → Enter.
![Part 7_09](/src/images/image7_09.png)<br>

- NANO faylni ochish uchun "nano test_nano.txt" terminalga kiritdim va nickname o'rniga «21 School 21» yozib, saqlamasdan chiqish uchun esa Ctrl+X → n → Enter algoritmini bajardim.
![Part 7_10](/src/images/image7_10.png)<br>

- MCEDIT da faylni ochish uchun "mcedit test_mc.txt" komandasini terdim va quyidagi amallarni bajardim:
* Nickname yozish va saqlash uchun Ctrl+O → Enter → Ctrl+X algoritmini kiritganimda natija quyidagicha bo'ldi:
F10 →
![Part 7_11](/src/images/image7_11.png)<br>

4. Qidiruv va almashtirish funksiyalarini ishlatish.
-  VIM faylni ochish va qidirish uchun "vim test_vim.txt" ni terminalga kiritdim va almashtirish funksiyasini bajardim. Undan keyin :%s/eski_so'z/yangi_so'z/g buyrug'ini bajardim hamda quyidagi natijani oldim:
![Part 7_12](/src/images/image7_12.png)<br>

- Nano. Faylni ochish va qidirish uchun "nano test_nano.txt" terminalga kiritib, Ctrl+W → So'z kiritib, Enter tugmasini bosdim.
![Part 7_13](/src/images/image7_13.png)<br>
Qidirgan so'zimni boshqa so'zga almashtirish uchun esa ushbu tartibni bajardim: Ctrl+W Ctrl+R. Natija quyidagicha:
![Part 7_14](/src/images/image7_14.png)<br>

- MCEDIT da faylni ochish uchun "mcedit test_mc.txt" komandasini terdim va quyidagi amallarni bajardim:
![Part 7_15](/src//images/image.7_15png)<br>

## Part 8. SSHD xizmatini o'rnatish va sozlash.
1. Bu qismda avval SSH xizmatini o'rnatdim. buning uchun "sudo apt update". kiritdim.
![Part 8_01](/src/images/image8_01.png)<br>

2. Keyin esa "sudo apt install openssh-server" ni kiritib, quyidagini oldim:
![Part 8_02](/src/images/image8_02.png)<br>

3. Avtostartni sozlash uchun "sudo systemctl enable ssh" ushbu bashni Ubuntuga kiritib, quyidagi natijani oldim:
![Part 8_03](/src/images/image8_03.png)<br>

4. SSH xizmatini "Port 2022" ga o'zgartirish uchun "sudo nano /etc/ssh/sshd_config" komandasini kiritdim va "Port 22" qatorini topib, "Port 2022" ga o'zgartirdim.
![Part 8_04](/src/images/image8_04.png)<br>

5. SSH jarayonining mavjudligini tekshirish uchun "ps aux | grep sshd" buyrug'idan foydalanib, ushbu natijani oldim:
![Part 8_05](/src/images/image8_05.png)<br>
* bu buyruq barcha jarayonlarni (a);
* foydalanuvchi ma’lumotlari bilan (u);
* kengaytirilgan ma’lumotlar (x) ko‘rsatadi.

6. Keyin "sudo reboot" buyrug'ini kiritib, ushbu natijani oldim.
![Part 8_06](/src/images/image8_06.png)<br>

7. netstat bilan portni tekshirish uchun "sudo apt install net-tools" hamda sudo netstart -tan | grep 2022" degan buyruqlani kiritdim. Natija esa quyidagicha bo'ldi:
![Part 8_07](/src/images/image8_07.png)<br>

8. Keyin esa "sudo netstat -tan | grep 2022" buyrug'ini kiritdim. Natija quyidagicha bo'ldi:
![Part 8_08](/src/images/image8_08.png)<br>
-t: TCP ulanishlarini ko‘rsatadi.
-a: Faol va tinglash rejimidagi portlarni ko‘rsatadi.
-n: Raqamli IP va portlarni ko‘rsatadi (DNS nomi emas).

## Part 9. Top va htop utilitlarini o'rnatish va ishlatish.
1. Top va htop utilitlarini o'rnatish uchun "sudo apt update" buyrug'ini kiritdim. Natija quyidagicha bo'ldi:
![Part 9_01](/src/images/image9_01.png)<br>

2. Keyin "sudo apt install top htop -y" buyrug'ini kiritib, ushbu natijani oldim:
![Part 9_02](/src/images/image9_02.png)<br>

3. "top" buyrug'ini ishga tushurganimda, natija quyidagicha bo'ldi:
![Part 9_03](/src/images/image9_03.png)<br>
Keyin quyidagilarni aniqladim:
* ish vaqti, ruxsat berilgan foydalanuvchilar soni, o'rtacha tizim yuki: top chiqishining yuqori qismi;
* jarayonlarning umumiy soni, CPU yuki, xotira yuki: top chiqishining "Tasks" va "CPU(s)" qismlari;
* eng yuqori xotiradan foydalanadigan jarayon PID: RES ustunidan topdim;
* eng ko'p CPU vaqtini oladigan jarayon PID: %CPU ustunidan topdim.

4. "Htop" buyrug'ini ishga tushirdim.
![Part 9_04](/src/images/image9_04.png)<br>
Htop bo'yicha ko'rsatmalar:
Tartiblash: F3 -> ustun tanlash (%CPU, %MEM, PID, TIME).
Filtrlash: F4 -> sshd yozish.
Syslog jarayonini qidirish: F3 -> syslog yozish.
Host nomi va soat chiqishi: Yuqori qismda avtomatik ko'rsatadi.

## Part 10. fdisk yordam dasturidan foydalanish.
1. ![Part 10.01](/src/images/image10.01.png)<br>
* disk nomi:
Disk /dev/sda: 12,51 GiB, 13421772800 bytes;
* disk hajmi:
Disk /dev/sda: 12,51 GiB;
* sektorlar soni:
Disk /dev/sda: 26214400 sectors;
* Almashtirish hajmi (Swap)
/dev/sda2  4096  3674111  3670016 1,8G  Linux filesystem

## Part 11. df yordam dasturidan foydalanish.
1. "df" buyrug'ini ishga tushirdim.
![Part 11_01](/src/images/image11_01.png)<br>

2. "df -Th /" buyrug'ini ishga tushirdim.
![Part 11_02](/src/images/image11_02.png)<br>

## Part 12. Du yordam dasturidan foydalanish.
1. "du -sh /home /var /var/log" buyrug'i orqali papka hajmini aniqladim:
![Part 12_01](/src/images/image12_01.png)<br>

2. "du -sh /var/log/* " /var/log ichidagi barcha elementlarning hajmini ko'rsatish buyrug'ini kiritdim.
![Part 12_02](/src/images/image12_02.png)<br>

## Part 13.  Ncdu ni o'rnatish va ishlatish.
1. Avval Ncdu ni "sudo apt update" hamda "sudo apt install ncdu" buyruqlari yordamida o'rnatdim.
![Part 13_01](/src/images/image13_01.png)<br>

2. Keyin papkalar hajmini ko'rish uchun quyidagi buyruqlardan foydalandim:
* ncdu /home ![Part 13_02](/src/images/image13_02.png)<br>
* ncdu /var ![Part 13_03](/src/images/image13_03.png)<br>
* ncdu /var/log ![Part 13_04](/src/images/image13_04.png)<br>

## Part 14. Tizim jurnallari bilan ishlash.
1. Jurnallarni ko'rish uchun buyruqlar:
* cat /var/log/dmesg ![Part 14_01](/src/images/image14_01.png)<br>
* cat /var/log/syslog ![Part 14_02](/src/images/image14_02.png)<br>
* cat /var/log/auth.log ![Part 14_03](/src/images/image14_03.png)<br>

2. So'nggi muvaffaqiyatli kirishni aniqlash uchun:
"grep "Accepted" /var/log/auth.log | tail -1", SSH xizmatini qayta ishga tushirish uchun esa "sudo systemctl restart sshd" buyruqlarini kiritdim. Natijada:
![Part 14_04](/src/images/image14_04.png)<br>

3. Xizmatni qayta ishga tushirish xabarini topish uchun grep "sshd" /var/log/syslog | tail -10 buyrug'ini kiritdim. Natija:
![Part 14_05](/src/images/image14_05.png)<br>

## Part 15. CRON ish rejalashtiruvchisidan foydalanish.
1. Har 2 daqiqada ish vaqti buyrug'ini bajarish uchun Cron vazifasini sozlash uchun "crontab -e" buyrug'ini kiritdim.
![Part 15_01](/src/images/image15_01.png)<br>

2. */2 * * * * date >> /tmp/cron_time.log
![Part 15_02](/src/images/image15_02.png)<br>

3. Bajarilgan ishni tizim jurnallarida tekshirdim:
grep CRON /var/log/syslog | tail -n 10
![Part 15_03](/src/images/image15_03.png)<br>

4. Joriy cron vazifalar ro'yxatini ko'rsatish buyrug'i "crontab -l":
![Part 15_04](/src/images/image15_04.png)<br>

5. Cron vazifalarini o'chirish buyrug'i "crontab -r":
![Part 15_05](/src/images/image15_05.png)<br>

## Xulosa.
* Har 2 daqiqada ish vaqti buyrug'ini bajarish uchun Cron vazifasini sozlash:
Cron fayliga yozganingizdan so'ng, har ikki daqiqada vaqtni /tmp/cron_time.log fayliga yozadi. Faylni tekshirish natijasi quyidagi buyruqda "cat /tmp/cron_time.log" ko'rinadi:
![Xulosa](/src/images/image16.png)<br>
