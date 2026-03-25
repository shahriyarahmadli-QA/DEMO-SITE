## Test Plan Ümumi Məlumat
**Məqsəd**  
MVP funksiyalarının qəbul meyarlarına uyğunluğunu yoxlamaq: məzmun lisenziyalaşması, formatlar, veb oxucu, axtarış, offline, monetizasiya, ödənişlər, təhlükəsizlik, analytics və dəstək.

**Test növləri**  
- **Funksional:** istifadəçi axınları və qəbul meyarları.  
- **İnteqrasiya:** ödəniş gateway, analytics, dəstək ticket sistemi.  
- **Təhlükəsizlik:** HTTPS, məlumatların şifrələnməsi, backup yoxlaması.  
- **İstifadəçi təcrübəsi:** oxucu və axtarışın əsas UX yoxlamaları.  
- **Regressiya:** düzəlişlərdən sonra kritik axınların təkrarlı yoxlanması.

**Test mühiti**  
- HTTPS ilə staging server; nümunə kataloq (100–500 kitab); ödəniş sandbox; analytics sandbox; dəstək ticket sandbox.  
- Cihazlar: Desktop (Chrome/Firefox), Mobil (Safari/Chrome), müxtəlif ekran ölçüləri.

---

## Rollar və Məsuliyyətlər
- **QA Lead:** test planı, cədvəl və yekun təsdiq.  
- **QA mühəndisləri:** test ssenarilərini icra və defekt qeydiyyatı.  
- **Dev Owner:** defektlərin düzəldilməsi və build təminatı.  
- **Product Manager:** qəbul meyarlarının təsdiqi və UAT təsdiqi.  
- **Support Lead:** dəstək iş axınının və SLA-ların yoxlanması.
