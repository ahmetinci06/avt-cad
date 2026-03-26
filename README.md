# 🖊️ AVT Racing — Teknik Çizim Ekibi

## 📊 İlerleme & Çalışma Akışı

- [🔄 WORKFLOW.md](WORKFLOW.md) — Çalışma akışı ve PR kuralları
- [📊 PROGRESS.md](PROGRESS.md) — Görev durumları ve ilerleme
- [🐛 BUGS.md](BUGS.md) — Bug raporları ve debug takibi

> Her değişiklik PR ile yapılır. Review: @ahmetinci06 (Aİ) & Yaver (AI CTO)

---



> **avt-cad** — CAD dosyaları, teknik çizimler ve tasarım dökümanlarının merkezi deposu.

[![Ana Hub](https://img.shields.io/badge/Ana%20Hub-avt--hub--dev-blue)](https://github.com/ahmetinci06/avt-hub-dev)
[![TEKNOFEST 2026](https://img.shields.io/badge/TEKNOFEST-2026-red)](https://teknofest.org)

---

## 📋 Hakkında

Bu repo, AVT Racing aracının tüm mekanik tasarım ve teknik çizim dosyalarını barındırır. Chassis, süspansiyon, powertrain ve diğer mekanik bileşenlerin CAD modelleri burada saklanır.

**Merkezi Hub:** [avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)

---

## 👥 Teknik Çizim Ekibi

| İsim | Rol |
|------|-----|
| Mahir Cengiz | Teknik Çizim |
| Muhammet Yahya Karataş | Teknik Çizim |
| Utku Esirgen | Teknik Çizim |
| Büşra Duymuş | Teknik Çizim |

---

## 📁 Klasör Yapısı

```
avt-cad/
├── chassis/                # Şasi tasarımları
│   ├── v1/                 # İlk versiyon
│   └── v2/                 # Revize versiyon
├── suspension/             # Süspansiyon sistemi
│   ├── front/              # Ön süspansiyon
│   └── rear/               # Arka süspansiyon
├── powertrain/             # Motor ve aktarma organları
├── bodywork/               # Kaporta ve dış yüzey
├── steering/               # Direksiyon sistemi
├── brakes/                 # Fren sistemi
├── drawings/               # 2D teknik çizimler (DXF, PDF)
│   ├── assembly/           # Montaj çizimleri
│   └── manufacturing/      # Üretim çizimleri
├── exports/                # Dışa aktarılan dosyalar (STEP, STL)
│   ├── step/               # STEP formatları
│   └── stl/                # STL (3D baskı) formatları
├── references/             # Referans ve standart dosyalar
└── docs/
    ├── GITHUB-GUIDE.md     # GitHub kullanım rehberi
    └── design-notes.md     # Tasarım notları
```

---

## 🔧 Kullanılan Yazılımlar

| Yazılım | Format | Açıklama |
|---------|--------|----------|
| SolidWorks | `.SLDPRT`, `.SLDASM` | Ana CAD yazılımı |
| CATIA | `.CATPart`, `.CATProduct` | Alternatif CAD |
| AutoCAD | `.DWG`, `.DXF` | 2D teknik çizimler |
| FreeCAD | `.FCStd` | Açık kaynak alternatif |
| Universal | `.STEP`, `.IGES` | Paylaşım formatı |

**Not:** Büyük CAD dosyaları (>100MB) için Git LFS kullanılır. Çok büyük dosyalar Google Drive'a yüklenir, link docs/ klasörüne eklenir.

---

## 🌿 Branch Yapısı

```
main          ← Onaylanmış, final tasarımlar
  └── develop ← Aktif geliştirme ve revizeler
        ├── design/chassis-v2
        ├── design/front-suspension-revize
        └── design/bodywork-aerodynamik
```

### Branch İsimlendirme
```
design/<bileşen-adı>        # Yeni tasarım
fix/<bileşen>-revize         # Tasarım düzeltmesi
docs/<konu>                  # Döküman güncellemesi
```

---

## 📤 Dosya Yükleme Kuralları

1. **Kaynak dosyaları** (`.SLDPRT`, `.DWG` vb.) repoya ekle
2. **STEP/IGES export** her tasarım için `exports/step/` klasörüne ekle
3. **PDF teknik çizim** `drawings/` klasörüne ekle
4. Dosya ismi: `avt-[bileşen]-v[versiyon].[uzantı]`
   - Örnek: `avt-chassis-v1.2.STEP`

---

## 🚀 Hızlı Başlangıç

```bash
# Repo'yu klonla
git clone git@github.com:ahmetinci06/avt-cad.git
cd avt-cad

# Develop branch'ine geç
git checkout develop

# Kendi branch'ini oluştur
git checkout -b design/yaptığın-iş

# Değişikliklerini yap, sonra:
git add .
git commit -m "design: [bileşen adı] v[versiyon] eklendi"
git push origin design/yaptığın-iş

# GitHub'da Pull Request aç
```

Detaylı rehber için: [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md)

---

## 📚 Kaynaklar

- [CONTRIBUTING.md](CONTRIBUTING.md) — Katkı ve PR kuralları
- [docs/GITHUB-GUIDE.md](docs/GITHUB-GUIDE.md) — Git başlangıç rehberi
- [Ana Hub — avt-hub-dev](https://github.com/ahmetinci06/avt-hub-dev)

---

*🏎️ AVT Racing — TEKNOFEST 2026 | Teknik Çizim Ekibi*