# Apartman Yoneticisi AI - Urun Gereksinim Belgesi (PRD)

## 1. Urun Tanimi ve Vizyon
Apartman Yoneticisi AI, cok katli konut yonetimlerinde yasanan finansal takip hatalarini ve iletisim kopukluklarini minimize etmek amaciyla gelistirilmis, yapay zeka entegreli bir Yonetim Bilisim Sistemidir (MIS). Sistem, operasyonel verimliligi artirirken tum paydaslar icin "denetlenebilir" bir platform sunar.

---

## 2. Hedef Kullanici Personaları

| Persona | Problem | Cozum |
| :--- | :--- | :--- |
| **Yonetici** | Manuel aidat takibi, surekli gelen telefonlar ve resmi duyuru yazma zorlugu. | Otomatize edilmis finansal paneller ve AI destekli duyuru asistani. |
| **Sakin** | Odeme gecmisine ulasamama, ariza bildirimlerinin sonucunu bilememe. | Self-servis borc sorgulama ve seffaf ariza takip arayuzu. |

---

## 3. Fonksiyonel Gereksinimler (Functional Requirements)

### 3.1. AI-Powered Iletisim Modulu
* **Duyuru Optimizasyonu:** Yonetici tarafindan girilen "ham veri" LLM (Large Language Model) katmanina gonderilir. Sistem, bu veriyi imla kurallarina uygun, apartman kulturune yakisir ve anlasilir bir duyuru metnine donusturur.
* **Akilli Soru-Cevap (RAG Temelli):** Bina yonetim plani ve kurallari sisteme PDF/Metin olarak tanimlanir. Sakinler, "Bahce kullanimi saat kacta bitiyor?" gibi sorularina AI uzerinden anlik yanit alir.

### 3.2. Finansal Yonetim ve Kayit Modulu
* **Dinamik Borclandirma:** Ayin belirli gunlerinde tum dairelere otomatik aidat tahakkuk ettirilmesi.
* **Mizan ve Dashboard:** Yonetici panelinde toplam alacak, toplam tahsilat ve aylık gider dagiliminin grafiksel gosterimi.
* **Kisisel Ekstre:** Sakinlerin gecmise donuk odeme makbuzlarina ve borc dokumlerine dijital erisimi.

### 3.3. Ariza Takip ve Biletleme (Ticketing)
* **Kategorik Yonlendirme:** Ariza tipine gore (Elektrik, Tesisat vb.) talebin ilgili is akisina alinmasi.
* **Onceliklendirme Algoritmasi:** AI, talep aciklamasini analiz ederek "yangin", "su baskini" gibi anahtar kelimeler gectiginde talebi "Kritik" statusune yukseltir.

---

## 4. Teknik Mimari ve Gereksinimler

### 4.1. Teknoloji Yigini (Tech Stack)
* **Frontend:** React.js / Next.js (Responsive Design)
* **Backend:** Python / FastAPI (Asenkron AI islemleri icin)
* **Veritabani:** PostgreSQL (Iliskisel veri ve ACID uyumlulugu)
* **AI Katmani:** OpenAI GPT-4o-mini (API Entegrasyonu)

### 4.2. Veri Modeli Taslagi (Schema)
* **Users:** `id, name, flat_no, role, auth_token`
* **Finance:** `id, user_id, amount, type (aidat/ekstra), status, due_date`
* **Tickets:** `id, user_id, category, description, priority, status (open/closed)`

---

## 5. Kullanici Akislari (User Flows)

### 5.1. Yonetici Duyuru Akisi
1. Yonetici "Duyuru Oluştur" ekranina girer.
2. Taslak bilgileri yazar (Orn: "Yarin asansor bakimi var 10-12 arasi").
3. AI "Kurumsal Metne Donustur" butonuna basilir.
4. AI'nin urettigi metin onaylanir ve tum sakin panellerine duser.

### 3.2. Sakin Ariza Bildirim Akisi
1. Sakin mobil/web arayuzunden "Ariza Bildir" formunu doldurur.
2. Sistem talep numarasini uretir ve yonetici dashboard'una dusurur.
3. Yonetici durumu "Islemde" olarak guncellediginde sakin anlik bildirim alir.

---

## 6. Kalite ve Kabul Kriterleri (Acceptance Criteria)
* **Performans:** AI metin uretim suresi 3 saniyenin altinda olmalidir.
* **Veri Guvenligi:** Kullanicilar sadece kendi dairelerine ait finansal verileri gorebilmelidir.
* **Hata Yonetimi:** Veritabani islemlerinde "rollback" mekanizmasi ile finansal veri kaybi onlenmelidir.

---
