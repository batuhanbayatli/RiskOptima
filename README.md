# 🛡️ RiskOptima Analytics

> **InsurTech Lab // Real-Time Automated Fraud Scoring & Claims Management Infrastructure**
> 
> Sigortacılık sektöründeki hasar (claims) süreçlerini optimize etmek ve mali suistimal (fraud) risklerini minimize etmek amacıyla geliştirilmiş veri odaklı, minimalist bir analitik dashboard simülatörüdür.

---

## ✨ Öne Çıkan Özellikler

*   **📊 Canlı Finansal Sayaçlar (KPI Metrics):** Toplam işlenen dosya hacmini, engellenen suistimal tutarını (şirketin kurtardığı nakit akışı 💰) ve onaylanan jet ödemeleri anlık olarak hesaplar.
*   **📉 Dinamik CSS Portföy Grafiği:** Kütüphane yükü olmadan, saf CSS ve JS mimarisiyle portföydeki risk dağılımını (Güvenli / İnceleme / Şüpheli) canlı olarak görselleştirir.
*   **⚡ Akıllı Risk Motoru (Risk Engine Core v2.4):** Girilen hasar parametrelerini aktüeryal katsayılarla süzerek saniyeler içinde `%0 - %100` arası bir sahtecilik indeksi üretir.
*   **🔍 Detaylı Risk Gerekçe Logları:** Şüpheli dosyaların altına sistemin *neden* kırmızı bayrak (Red Flag) kaldırdığını gerekçeleriyle listeler.

---

## ⚙️ Risk Skorlama Algoritması & İş Mantığı (Business Logic)

RiskOptima, SEGEM ve teknik sigortacılık dinamiklerini arkasına alarak her hasar ihbarını 4 kritik dikeyde matematiksel teste tabi tutar:

| Risk Faktörü (Kriter) | Operasyonel Durum | Risk Puanı Katsayısı | Sektörel Mantık |
| :--- | :--- | :--- | :--- |
| **Poliçe Yaşı (Kritik Dönem)** | < 30 Gün <br> 31 - 90 Gün | **+35 Puan** <br> **+15 Puan** | Poliçe tanziminden hemen sonra gelen hasarlar yüksek moral risk barındırır. |
| **Hasar Saati (Gece Kuşağı)** | 00:00 - 05:00 | **+20 Puan** | Gece yarısı kazalarında alkol raporu veya sürücü değiştirme şüphesi artar. |
| **Geçmiş Hasar Frekansı** | > 2 Hasar <br> 0 Hasar (Temiz) | **+25 Puan** <br> **-10 Puan (Bonus)** | Hasarsızlık geçmişi müşterinin sadakatini ve moralitesini doğrular. |
| **Hasar / Prim Oranı** | > 50.000 ₺ | **+20 Puan** | Şirket mali risk eşiğini aşan hasarlar doğrudan sıkı takibe alınır. |

### 🎯 Karar Mekanizması:
*   **%70 ve Üzeri:** 🚨 `Şüpheli - Eksper Atandı` (Mali blokaj uygulanır).
*   **%35 - %69 Arası:** ⚠️ `İncelemede / Belge Bekleniyor`.
*   **%35 Altı:** ❇️ `Jet Onay - Ödeme Sırasında` (Otomatik mutabakat).

---

## 🛠️ Teknoloji Yığını (Tech Stack)

Projenin en büyük gücü **hafifliği, şeffaflığı ve taşınabilirliğidir**. Hiçbir ağır framework veya `node_modules` bağımlılığı olmadan, saf performans odaklı inşa edilmiştir:

*   **UI/UX:** Semantic HTML5 & Minimalist "Old Money" CSS Design
*   **Engine:** Vanilla JavaScript (ES6+) Core Logic
*   **Deployment:** GitHub Pages / Vercel (Zero-Config)

---

## 💻 Kurulum ve Çalıştırma

Proje tek bir bağımsız dosyadan oluştuğu için bilgisayarınızda çalıştırmak sadece 2 saniyenizi alır:

```bash
# Projeyi klonlayın
git clone [https://github.com/batuhanbayatli/RiskOptima.git](https://github.com/batuhanbayatli/RiskOptima.git)

# Proje klasörüne girin
cd RiskOptima

# index.html dosyasına çift tıklayarak tarayıcıda anında çalıştırın!
