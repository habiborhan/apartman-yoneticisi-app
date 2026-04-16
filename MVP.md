# Apartman Yoneticisi AI - MVP Kapsam Dokumani

## 1. Proje Vizyonu ve Stratejik Amac
Bu MVP (*Minimum Viable Product*) calismasi, apartman yonetimindeki geleneksel ve verimsiz yontemleri, yapay zeka destekli bir platform ile dijitallestirmeyi hedefler. Temel amac, yonetici uzerindeki operasyonel yuku minimize ederken, sakinler icin seffaf ve erisilebilir bir bilgi ekosistemi kurmaktir.

---

## 2. Sistem Tasarim Ilkeleri
Sistemin gelistirilme surecinde asagidaki temel prensipler esas alinmistir:

* **Fonksiyonel Odak (Logistik ve Finans):** Yonetimin en cok vakit ayirdigi aidat takibi ve ariza yonetimi sureclerine oncelik verilmistir.
* **Veri Butunlugu:** Finansal kayitlarin tek bir kaynak uzerinden dogrulanabilir (*Single Source of Truth*) sekilde tutulmasi saglanacaktir.
* **Kullanici Odakli Deneyim:** Teknoloji okuryazarligi farkli olan kullanici gruplari icin dusuk ogrenme egrisi hedeflenmistir.
* **AI Yardimli Verimlilik:** Rutin iletisim gorevlerinin Dogal Dil Isleme (NLP) teknikleriyle otomatize edilmesi saglanacaktir.

---

## 3. Fonksiyonel Gereksinimler

### 3.1. Yetkilendirme ve Rol Yonetimi
Sistem, **RBAC** (*Role-Based Access Control*) prensibine gore iki ana rolde kurgulanmistir:

| Rol | Yetkiler |
| :--- | :--- |
| **Admin (Yonetici)** | Bina konfigurasyonu, sakin kaydi, finansal girdi saglama ve duyuru yönetimi. |
| **End-User (Sakin)** | Kisisel borc takibi, ariza bildirimi ve yapay zeka ile bilgi sorgulama. |

### 3.2. Finansal Izleme ve Yonetim Modulu
Yonetim ve sakinler arasindaki mali guveni tesis etmek amaciyla asagidaki ozellikler sunulur:
* **Daire Bazli Defter-i Kebir:** Her dairenin aidat borcu, odeme durumu ve son odeme tarihi takibi.
* **Gider Katalogu:** Apartman genel giderlerinin (elektrik, su, asansor bakimi vb.) kategorize edilerek listelenmesi.
* **Finansal Raporlama:** Yonetici icin tahsilat takip listeleri; sakinler icin kisisel odeme gecmisi raporlari.

### 3.3. Teknik Servis ve Ariza Yonetimi
Iletisim kopukluklarini onlemek amaciyla merkezi bir takip sistemi kurulmustur:
* **Biletleme Sistemi (Ticketing):** Sakinlerin Su, Elektrik, Asansor, Temizlik kategorilerinde ariza kaydi acmasi.
* **Durum Yasam Dongusu:** Taleplerin `Acik`, `Islemde` ve `Tamamlandi` statuslerinde uctan uca yonetilmesi.
* **Gecmis Kayitlar:** Tekrarlayan sorunlarin tespiti icin veri tabaninda kronolojik saklama.

### 3.4. Yapay Zeka (AI) Entegrasyonu
Sistemi rakiplerinden ayiran akilli katman asagidaki yetenekleri kapsar:
* **NLP Tabanli Duyuru Motoru:** Yoneticinin verdigi ham bilgileri kurumsal ve nazik bir duyuru metnine donusturme.
* **Otomatik Hatirlatici Asistani:** Geciken aidatlar icin kisiye ozel, yapici ve net bilgilendirme mesajlari uretilmesi.
* **Akilli Bilgi Yonetimi (AI Q&A):** Bina kurallari ve yonetim plani uzerinden sakinlerin sorularina anlik yanit verilmesi.

---

## 4. Teknik Kisitlar ve Kapsam Disi Unsurler
Projenin **Phase 1** asamasinda asagidaki ozellikler kapsam disi (*Out of Scope*) olarak belirlenmistir:
* Sanal POS ve direkt kredi karti tahsilat entegrasyonu.
* Banka API'lari uzerinden otomatik ekstre okuma.
* Anlik bildirim (*Push Notification*) servisleri.
* WhatsApp Bot ve SMS Gateway entegrasyonu.
* Coklu site/apartman yonetim hiyerarsisi.

---

## 5. Proje Basari Metrikleri (KPI)
Projenin basarisi asagidaki somut verilerle olculecektir:

1.  **Zaman Tasarrufu:** Yoneticinin rutin duyuru ve takibe ayirdigi surenin **%60** oraninda azaltilmasi.
2.  **Seffaf Yonetim:** Sakinlerin gider ve borc sorgularina cevap alma suresinin **minimuma** indirilmesi.
3.  **Hata Payi:** Finansal kayitlardaki manuel hesaplama hatalarinin **tamamen** ortadan kaldirilmasi.

---
