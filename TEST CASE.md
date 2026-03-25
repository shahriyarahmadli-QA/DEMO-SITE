### TC-01 — Məzmun lisenziyalaşmasının bloklanması  
**US:** US-01  
**Şərt:** Admin hesabı; lisenziya metadatası olmayan kitab yüklənir.  
**Addımlar:**  
1. Admin lisenziya məlumatı olmayan kitab yükləyir.  
2. Nəşr etməyə çalışır.  
**Gözlənilən nəticə:** Sistem nəşri bloklayır və "lisenziya tələb olunur" mesajı göstərir.  
**Keçid meyarı:** Nəşr bloklanır və lisenziya sahəsi məcburi olur.

### TC-02 — İctimai domen kitabın nəşri  
**US:** US-01  
**Şərt:** Admin kitabı ictimai domen kimi işarələyib.  
**Addımlar:**  
1. Admin kitabı yükləyir və public domain olaraq işarələyir.  
2. Nəşr edir.  
**Gözlənilən nəticə:** Kitab kataloqa əlavə olunur və meta məlumatında **Public Domain** göstərilir.  
**Keçid meyarı:** Kitab görünür və meta düzgün göstərilir.

### TC-03 — Dəstəklənən formatların göstərilməsi  
**US:** US-02  
**Şərt:** ePub və PDF formatlı kitablar mövcuddur.  
**Addımlar:**  
1. ePub kitab səhifəsini aç.  
2. PDF kitab səhifəsini aç.  
**Gözlənilən nəticə:** Veb oxucu uyğun formatı avtomatik seçir və göstərir.  
**Keçid meyarı:** Hər iki format düzgün render olunur.

### TC-04 — Dəstəklənməyən format xəbərdarlığı  
**US:** US-02  
**Şərt:** .mobi kimi dəstəklənməyən format yüklənib.  
**Addımlar:**  
1. Kitab səhifəsini aç.  
**Gözlənilən nəticə:** "Format dəstəklənmir" mesajı göstərilir.  
**Keçid meyarı:** Xəbərdarlıq görünür və oxucu açılmır.

### TC-05 — Səhifə çevirmə funksionallığı  
**US:** US-03  
**Şərt:** İstifadəçi daxil olub kitab açıb.  
**Addımlar:**  
1. Növbəti səhifəyə keç.  
2. Əvvəlki səhifəyə geri dön.  
**Gözlənilən nəticə:** Səhifələr düzgün dəyişir, performans normaldır.  
**Keçid meyarı:** Keçidlər səhvsiz və sürətlidir.

### TC-06 — Oxucu fərdiləşdirmə (font, gecə rejimi, vurğulama)  
**US:** US-03  
**Şərt:** İstifadəçi oxucu görünüşündədir.  
**Addımlar:**  
1. Font ölçüsünü dəyiş.  
2. Gecə rejimini aktiv et.  
3. Mətn vurğula.  
**Gözlənilən nəticə:** UI dərhal yenilənir; vurğulamalar istifadəçi hesabında saxlanır.  
**Keçid meyarı:** Dəyişikliklər səhifə yenilənməsindən sonra da qalır.

### TC-07 — Axtarış və filtr (müəllif/janr/populyar)  
**US:** US-04  
**Şərt:** Kataloq etiketlənib.  
**Addımlar:**  
1. Müəllif adı ilə axtar.  
2. Janr ilə axtar.  
3. Populyar filtrini tətbiq et.  
**Gözlənilən nəticə:** Uyğun nəticələr qaytarılır; populyar sıralama istifadəçi metriklərinə əsaslanır.  
**Keçid meyarı:** Nəticələr sorğuya uyğundur.

### TC-08 — Offline yükləmə limiti  
**US:** US-05  
**Şərt:** Aktiv abunə; aylıq offline limit 5 kitab.  
**Addımlar:**  
1. Kitabları yüklə (limitə qədər).  
2. Bir daha yükləməyə çalış.  
**Gözlənilən nəticə:** İlk yükləmələr uğurlu; sonuncu cəhd bloklanır və limit mesajı göstərilir.  
**Keçid meyarı:** Fayllar şifrələnmiş saxlanır və limit tətbiq olunur.

### TC-09 — Abunə aktivləşməsi  
**US:** US-06, US-07  
**Şərt:** Test istifadəçisi abunə deyil; ödəniş sandbox mövcuddur.  
**Addımlar:**  
1. Abunə planı seç.  
2. Ödənişi tamamla (sandbox).  
**Gözlənilən nəticə:** Abunə aktiv olur; premium funksiyalar açılır.  
**Keçid meyarı:** İstifadəçi dərhal premiuma daxil ola bilir.

### TC-10 — Tək kitab satınalma  
**US:** US-06, US-07  
**Şərt:** Kitab tək satış üçün mövcuddur.  
**Addımlar:**  
1. Checkout ilə kitab al.  
**Gözlənilən nəticə:** Kitab istifadəçi kitabxanasına əlavə olunur; əməliyyat qeyd olunur.  
**Keçid meyarı:** Giriş verilir və tranzaksiya loglanır.

### TC-11 — Ödəniş uğursuzluğu idarəsi  
**US:** US-06, US-07  
**Şərt:** Ödəniş gateway uğursuz cavab qaytarır.  
**Addımlar:**  
1. Uğursuz kartla ödəniş et.  
**Gözlənilən nəticə:** Xəta göstərilir; istifadəçi təkrar cəhd üçün yönləndirilir.  
**Keçid meyarı:** Abunə aktivləşmir və aydın xəta mesajı görünür.

### TC-12 — HTTPS məcburiyyəti  
**US:** US-08  
**Şərt:** Staging həm HTTP, həm HTTPS-də əlçatandır.  
**Addımlar:**  
1. http:// ünvanını aç.  
**Gözlənilən nəticə:** HTTPS-ə yönləndirmə olur.  
**Keçid meyarı:** Bütün trafik HTTPS üzərindən xidmət edilir.

### TC-13 — Məlumatların şifrələnməsi (at rest)  
**US:** US-08  
**Şərt:** İstifadəçi şəxsi məlumatları saxlanılıb.  
**Addımlar:**  
1. Saxlama qatını yoxla.  
**Gözlənilən nəticə:** Həssas sahələr şifrələnmişdir.  
**Keçid meyarı:** DB və ya storage konfiqurasiyasında şifrələmə təsdiqlənir.

### TC-14 — Backup icrası və loglar  
**US:** US-08  
**Şərt:** Backup planı konfiqurasiya olunub.  
**Addımlar:**  
1. Backup işini işə sal. 2. Logları yoxla.  
**Gözlənilən nəticə:** Backup tamamlanır və log yaradılır.  
**Keçid meyarı:** Backup faylı mövcuddur və log uğuru göstərir.

### TC-15 — Event tracking və DAU/MAU  
**US:** US-09  
**Şərt:** Analytics inteqrasiyası aktivdir.  
**Addımlar:**  
1. `session_start`, `page_turn`, `highlight`, `download_offline`, `purchase` eventlərini icra et.  
2. Analytics dashboard-da 1 günlük və 30 günlük pəncərəni aç.  
**Gözlənilən nəticə:** Eventlər görünür; DAU və MAU yenilənir.  
**Keçid meyarı:** Eventlər analytics-də və DAU/MAU hesabatında əks olunur.

### TC-16 — Support e‑mail ilə ticket yaradılması  
**US:** US-10  
**Şərt:** support@lovable.dev ticket sistemi ilə bağlıdır.  
**Addımlar:**  
1. Support ünvanına e‑mail göndər.  
**Gözlənilən nəticə:** Avtomatik təsdiq cavabı gəlir və ticket yaradılır.  
**Keçid meyarı:** Ticket sistemdə mövcuddur və auto‑reply alınır.
