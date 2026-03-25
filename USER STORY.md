## US-01 Məzmuna giriş və lisenziyalaşma
**User story**  
**As a** product owner  
**I want** kitabları yalnız lisenziyalı və ictimai domen məzmunu ilə başlamaq  
**So that** hüquqi risklər minimuma endirilsin və müəllif haqları qorunsun

**Acceptance criteria**
- **Given** naşir və ya müəlliflə müqavilə imzalanmayıb və kitab ictimai domen deyilsə,  
  **When** admin kitab yükləmək üçün interfeysə fayl əlavə edirsə,  
  **Then** sistem kitabı yayımlamadan əvvəl **lisenziya statusunu tələb etməli** və yayımlamağı bloklamalıdır.
- **Given** kitab ictimai domen kimi işarələnibsə,  
  **When** admin kitabı təsdiqləyirsə,  
  **Then** kitab kataloqa əlavə olunmalı və meta məlumatında **“ictimai domen”** göstərilməlidir.

---

## US-02 Dəstək olunan formatlar
**User story**  
**As a** reader  
**I want** kitabları **ePub** və **PDF** formatlarında oxuya bilmək  
**So that** müxtəlif cihazlarda rahat oxuma təcrübəsi əldə edim

**Acceptance criteria**
- **Given** kitab ePub və ya PDF formatında yüklənibsə,  
  **When** istifadəçi kitab səhifəsinə daxil olursa,  
  **Then** veb oxucu uyğun formatı avtomatik seçməli və kitabı göstərməlidir.
- **Given** kitabın formatı dəstəklənmirsə,  
  **When** istifadəçi kitab səhifəsinə daxil olursa,  
  **Then** sistem istifadəçiyə **format dəstəklənmir** xəbərdarlığı göstərməlidir.

---

## US-03 Veb oxucu əsas funksiyalar
**User story**  
**As a** reader  
**I want** səhifə çevirilməsi, font ölçüsü dəyişimi, gecə rejimi və qeyd/vurğulama funksiyalarını istifadə etmək  
**So that** oxuma təcrübəsini öz zövqümə uyğunlaşdıra bilim

**Acceptance criteria**
- **Given** istifadəçi kitabı açıb oxumağa başlayıb,  
  **When** istifadəçi səhifə çevir düyməsinə basır,  
  **Then** növbəti və ya əvvəlki səhifə göstərilməlidir.
- **Given** istifadəçi font ölçüsünü dəyişmək istəyirsə,  
  **When** font ölçüsü seçimi tətbiq edilirsə,  
  **Then** oxu görünüşü dərhal yenilənməlidir.
- **Given** istifadəçi gecə rejimini aktivləşdirirsə,  
  **When** rejim aktivdir,  
  **Then** fon və mətn rəngləri gecə rejiminə uyğun dəyişməlidir.
- **Given** istifadəçi mətn hissəsini vurğulamaq istəyirsə,  
  **When** vurğulama edilir,  
  **Then** vurğulama istifadəçinin hesabında saxlanmalı və sinxronizasiya üçün qeyd olunmalıdır.

---

## US-04 Axtarış və kateqoriya
**User story**  
**As a** reader  
**I want** müəllif, janr və populyar əsərlər üzrə axtarış edə bilmək  
**So that** maraqlandığım kitabları asanlıqla tapa bilim

**Acceptance criteria**
- **Given** istifadəçi axtarış sahəsinə sorğu daxil edibsə,  
  **When** axtarış göndərilir,  
  **Then** nəticələr müəllif, başlıq və janr üzrə uyğun kitabları sıralamalıdır.
- **Given** istifadəçi **populyar** filtrini seçirsə,  
  **When** filtr tətbiq olunur,  
  **Then** ən çox oxunan və ya ən çox qiymətləndirilən kitablar üstünlük sırasına görə göstərilməlidir.

---

## US-05 Offline yükləmə
**User story**  
**As a** subscribed reader  
**I want** müəyyən sayda kitabı offline yükləyə bilmək  
**So that** internet olmadan da oxuya bilim

**Acceptance criteria**
- **Given** istifadəçi aktiv abunəçidirsə,  
  **When** istifadəçi offline üçün kitab yükləmək istəyirsə və aylıq limit daxilindədirsə,  
  **Then** kitab cihazda **şifrələnmiş şəkildə** saxlanmalı və veb oxucu offline rejimdə açmalıdır.
- **Given** istifadəçi limitə çatıbsa,  
  **When** yeni offline yükləmə tələb edirsə,  
  **Then** sistem istifadəçiyə **limit çatdığını** bildirərək əlavə yükləməni bloklamalıdır.

---

## US-06 Monetizasiya abunə və pay per book
**User story**  
**As a** product owner  
**I want** abunə və kitab başına ödəniş modellərini dəstəkləmək  
**So that** istifadəçilər müxtəlif seçimlərlə ödəniş edə bilsinlər

**Acceptance criteria**
- **Given** istifadəçi abunə paketini seçibsə,  
  **When** ödəniş uğurla tamamlanır,  
  **Then** istifadəçi abunə hüququ ilə qeydiyyata alınmalı və **premium funksiyalara giriş** əldə etməlidir.
- **Given** istifadəçi tək kitab almaq istəyirsə,  
  **When** ödəniş tamamlanır,  
  **Then** həmin kitab istifadəçinin hesabına əlavə olunmalı və oxuma hüququ verilməlidir.
- **Given** ödəniş uğursuz olarsa,  
  **When** istifadəçi ödəniş prosesini tamamlamır,  
  **Then** sistem istifadəçiyə **xətanı göstərməli** və təkrar cəhd üçün istiqamətləndirmə verməlidir.

---

## US-07 Ödəniş inteqrasiyası
**User story**  
**As a** user  
**I want** yerli və beynəlxalq kartlarla və mobil ödənişlərlə ödəyə bilmək  
**So that** rahat və etibarlı ödəniş təcrübəsi əldə edim

**Acceptance criteria**
- **Given** istifadəçi ödəniş səhifəsinə keçibsə,  
  **When** kart məlumatı daxil edilir və ödəniş göndərilir,  
  **Then** ödəniş gateway vasitəsilə təsdiqlənməli və nəticə istifadəçiyə göstərilməlidir.
- **Given** mobil ödəniş seçilibsə,  
  **When** ödəniş tamamlanır,  
  **Then** sistem ödənişi təsdiqləməli və abunə/satışı aktiv etməlidir.

---

## US-08 Təhlükəsizlik və backup
**User story**  
**As a** admin  
**I want** SSL, istifadəçi məlumatlarının şifrələnməsi və backup mexanizmləri olsun  
**So that** istifadəçi məlumatları və məzmun təhlükəsiz saxlanılsın

**Acceptance criteria**
- **Given** istifadəçi saytla əlaqə qurursa,  
  **When** HTTP sorğusu göndərilir,  
  **Then** bütün trafik **HTTPS** üzərindən olmalıdır.
- **Given** istifadəçi şəxsi məlumat daxil edirsə,  
  **When** məlumat saxlanılır,  
  **Then** məlumat bazasında **şifrələnmiş formada** saxlanmalıdır.
- **Given** sistem backup planı tətbiq olunubsa,  
  **When** gündəlik backup icra edilir,  
  **Then** backup uğurla tamamlandığına dair **log** yaradılmalıdır.

---

## US-09 Analytics DAU MAU və event tracking
**User story**  
**As a** product manager  
**I want** DAU, MAU və əsas eventləri izləmək  
**So that** istifadəçi bağlılığını və məhsul sağlamlığını ölçə bilim

**Acceptance criteria**
- **Given** istifadəçi platformada fəaliyyət göstərirsə,  
  **When** `session_start`, `page_turn`, `highlight`, `download_offline`, `purchase` kimi eventlər baş verirsə,  
  **Then** hər event **analytics sisteminə göndərilməli** və **DAU/MAU hesabatları** avtomatik yenilənməlidir.
- **Given** analytics dashboard açılıbsa,  
  **When** product manager 30 günlük dövrü seçirsə,  
  **Then** **MAU, DAU və DAU/MAU nisbəti** göstərilməlidir.

---

## US-10 Əsas dəstək kanalı
**User story**  
**As a** reader  
**I want** e‑mail və in‑app chat vasitəsilə dəstək ala bilmək  
**So that** problemlərim tez həll olunsun

**Acceptance criteria**
- **Given** istifadəçi **support@lovable.dev** ünvanına e‑mail göndəribsə,  
  **When** yeni ticket yaranır,  
  **Then** sistem avtomatik təsdiq cavabı göndərməli və **ticket nömrəsi** yaratmalıdır.
- **Given** istifadəçi in‑app chat vasitəsilə mesaj göndəribsə,  
  **When** mesaj daxil olur,  
  **Then** agentlər üçün ticket yaradılmalı və **ilk cavab SLA daxilində (<24 saat)** verilməlidir.
- **Given** kritik hüquq və ya müəllif hüquqları şikayəti daxil olarsa,  
  **When** ticket yaradılır,  
  **Then** **eskalasiya prosesi** avtomatik işə düşməli və həll müddəti prioritetləşdirilməlidir.

---

## Prioritetləşdirmə və növbəti addımlar
- **Yüksək prioritet:** US-01, US-03, US-06, US-07, US-09, US-10  
- **Orta prioritet:** US-02, US-04, US-05, US-08

---

## Qısa yoxlama siyahısı
- [ ] Hüquqi lisenziyalaşma başlanılıb  
- [ ] 100–500 kitab kataloqu toplanıb  
- [ ] Veb oxucu MVP hazırdır  
- [ ] İstifadəçi qeydiyyatı və abunə ödəniş sistemi inteqrasiya edilib  
- [ ] Analytics və əsas dəstək kanalı aktivdir

---
