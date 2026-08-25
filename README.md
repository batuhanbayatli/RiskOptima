# 🛡️ RiskOptima Labs // Enterprise InsurTech Analytics Suite
> **Geleceğin Riskini Bugünün Verisiyle Yönetin**  
> *Real-Time Automated Fraud Scoring & Actuarial Claims Intelligence Infrastructure*

<p align="left">
  <a href="https://risk-optima.vercel.app/"><img src="https://img.shields.io/badge/Canlı%20Demo-Vercel-0284c7?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel Canlı Demo"></a>
  <img src="https://img.shields.io/badge/Ecosystem-bGroup-0f172a?style=for-the-badge" alt="bGroup">
  <img src="https://img.shields.io/badge/Stack-Vanilla%20JS%20%7C%20Tailwind%20%7C%20ApexCharts-38bdf8?style=for-the-badge" alt="Tech Stack">
  <img src="https://img.shields.io/badge/License-MIT-10b981?style=for-the-badge" alt="License">
</p>

---

## 📌 Proje Özeti

**RiskOptima Labs**, sigortacılık ve reasürans operasyonlarındaki hasar (claims) süreçlerini optimize etmek, suistimal (fraud) kaynaklı maliyet kaçaklarını önlemek ve aktüeryal rezerv tahminlerini anlık verilerle desteklemek amacıyla geliştirilmiş yeni nesil bir **InsurTech Analitik Dashboard** platformudur.

Harici sunucu bağımlılığı olmadan, istemci tarafında yüksek performansla çalışan aktüeryal skorlama algoritmaları, canlı veri simülasyon motoru ve sayfalama destekli portföy kuyruğu ile acente ve sigorta şirketleri için karar destek altyapısı sunar.

---

## ✨ Temel Yetenekler & Modüller

* 📊 **Anlık Finansal Metrikler & KPI Bandı:** Toplam işlenen dosya hacmi, bloke edilen şüpheli hasar tutarı (şirketin kurtardığı nakit akışı) ve onaylanan jet ödemeleri anlık olarak hesaplar.
* ⚡ **Gerçek Zamanlı Simülasyon Motoru (Live Data Stream):** Borsa/finans terminali mantığında, arka planda dinamik vakalar üreterek sistemi stres testine tabi tutar.
* 📑 **Sayfalamalı Hasar Kuyruğu (Pagination):** Veri havuzunu 10'arlı sayfalara bölerek performans kaybını ve arayüz karmaşasını önler.
* 📈 **Aktüerya & BI Metrikleri:** Aylık hasar trendleri, saatlik hasar yoğunluk anomalileri ve moral risk dağılımını interaktif **ApexCharts** grafikleri ile görselleştirir.
* 🔍 **Detaylı Dosya İnceleme & Anomali Logları:** Her dosyanın aktüeryal karnesini ve sistemin kaldırdığı kırmızı bayrakları (Red Flags) ayrıntılı modal üzerinde listeler.
* 💾 **Kalıcı Tarayıcı Hafızası:** LocalStorage API ile verileri oturumlar arasında güvenle saklar.

---

## ⚙️ Risk Skorlama & İş Mantığı (Actuarial Logic)

RiskOptima Engine Core, teknik sigortacılık prensipleri doğrultusunda her hasar ihbarını 4 ana risk dikeyinde matematiksel filtrelemeye tabi tutar:

| Risk Faktörü (Kriter) | Operasyonel Durum | Risk Puanı Katsayısı | Sektörel Mantık & Gerekçe |
| :--- | :--- | :--- | :--- |
| **Poliçe Yaşı (Kritik Dönem)** | `< 30 Gün`<br>`31 - 90 Gün` | `+35 Puan`<br>`+15 Puan` | Tanzimden hemen sonra gelen hasarlar yüksek moral risk (kasıtlı beyan) barındırır. |
| **Hasar Saati (Gece Kuşağı)** | `00:00 - 05:00` | `+20 Puan` | Gece yarısı kazalarında sürücü değişikliği ve alkol raporu şüphesi artar. |
| **Geçmiş Hasar Frekansı** | `> 2 Hasar`<br>`0 Hasar (Temiz)` | `+25 Puan`<br>`-10 Puan (Bonus)` | Hasarsızlık geçmişi sigortalının sadakat ve risk profilini doğrular. |
| **Mali Kritik Eşik** | `> 50.000 ₺` | `+20 Puan` | Şirket mali risk toleransını aşan hasarlar doğrudan sıkı incelemeye alınır. |

### 🎯 Karar Mekanizması Eşikleri
* **%70 ve Üzeri:** 🚨 `Şüpheli - Eksper Atandı` (Mali blokaj uygulanır).
* **%35 - %69 Arası:** ⚠️ `İncelemede / Belge Bekleniyor` (Ek evrak talep edilir).
* **%35 Altı:** ❇️ `Jet Onay - Ödeme Sırasında` (Otomatik mutabakat & anında ödeme).

---

## 🛠️ Teknoloji Mimarisi

* **Arayüz / Tasarım:** Semantic HTML5, Tailwind CSS (Slate / Light FinTech Design System)
* **Grafik & Görselleştirme:** ApexCharts.js, Lucide Icons
* **Çekirdek Motor:** Vanilla ES6+ JavaScript (Zero Backend Dependency)
* **Veri Yönetimi:** Browser LocalStorage API
* **Dağıtım / CI-CD:** Vercel Edge Network

---

## 🚀 Yerel Kurulum ve Çalıştırma

```bash
# Repoyu klonlayın
git clone [https://github.com/batuhanbayatli/RiskOptima.git](https://github.com/batuhanbayatli/RiskOptima.git)

# Proje dizinine geçin
cd RiskOptima

# index.html dosyasını herhangi bir tarayıcıda açın veya canlı demoyu ziyaret edin:
# [https://risk-optima.vercel.app/](https://risk-optima.vercel.app/)
