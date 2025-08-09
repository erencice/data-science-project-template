<div align="center">

# 📊 Veri Bilimi Proje Rehberi

<img src="https://img.shields.io/badge/Python-3.10+-blue.svg" alt="Python Version">
<img src="https://img.shields.io/badge/UV-Package%20Manager-green.svg" alt="UV">
<img src="https://img.shields.io/badge/Git-Version%20Control-orange.svg" alt="Git">

*Modern Python ekosistemi ile veri bilimi projelerini profesyonelce yönetmek için kapsamlı rehber*

</div>

---

## 🎯 Genel Bakış

Bu rehber, **veri bilimi projelerini sıfırdan başlatmak, yönetmek ve geliştirmek** için gereken tüm araçları ve en iyi uygulamaları kapsar.

### 🔥 Öne Çıkan Özellikler
- 🚀 **UV** ile modern Python paket yönetimi
- 🐍 **Sanal ortam** kurulumu ve yönetimi
- 📦 **Bağımlılık** yönetimi ve versiyon kontrolü
- 🐙 **Git** ile versiyon kontrolü
- 📂 **Proje yapısı** organizasyonu

---

## 📑 İçindekiler

<details>
<summary>🔽 Bölümleri görüntülemek için tıklayın</summary>

- [✨ Proje Oluşturma ve Çalıştırma](#-proje-oluşturma-ve-çalıştırma)
- [📦 Bağımlılık Yönetimi](#-bağımlılık-yönetimi)
- [🐍 Sanal Ortam](#-sanal-ortam-virtual-environment)
- [🐙 Git Temelleri](#-git-temelleri)
- [📂 Klasör ve Dosya Yapısı](#-klasör-ve-dosya-yapısı)
- [⚙️ Konfigürasyon Dosyaları](#️-konfigürasyon-dosyaları)
- [🛠️ Yaygın Komutlar](#️-yaygın-kullanılan-ek-komutlar)
- [🚀 Hızlı Başlangıç](#-hızlı-başlangıç-adımları)

</details>

---

## ✨ Proje Oluşturma ve Çalıştırma

### 🆕 Yeni Proje Başlatma

```bash
# Yeni proje oluşturma
uv init my_project --python=3.11

# Proje dizinine geçiş
cd my_project
```

### ▶️ Projeyi Çalıştırma

```bash
# Ana dosyayı çalıştırma
uv run main.py

# Belirli bir scripti çalıştırma
uv run src/analysis.py
```

> 💡 **İpucu:** `uv init` komutu otomatik olarak `main.py`, `README.md` ve `pyproject.toml` dosyalarını oluşturur.

---

## 📦 Bağımlılık Yönetimi

### 📋 Ana Bağımlılıklar

```bash
# Temel veri bilimi paketleri
uv add numpy pandas matplotlib seaborn

# Makine öğrenmesi kütüphaneleri
uv add scikit-learn tensorflow pytorch

# Veri işleme araçları
uv add jupyter polars dask
```

### 🔧 Geliştirme Bağımlılıkları

```bash
# Test ve kod kalitesi araçları
uv add pytest black flake8 mypy --group dev

# Dokümantasyon araçları
uv add sphinx mkdocs --group docs

# Profiling ve debugging
uv add memory-profiler line-profiler --group debug
```

### 📊 Bağımlılık Yönetimi Komutları

| Komut | Açıklama |
|-------|----------|
| `uv add package` | Paket ekleme |
| `uv remove package` | Paket kaldırma |
| `uv sync` | Bağımlılıkları senkronize etme |
| `uv lock` | Lock dosyası güncelleme |

---

## 🐍 Sanal Ortam (Virtual Environment)

### 🔨 Sanal Ortam Oluşturma

```bash
# Python ile sanal ortam oluşturma
python3 -m venv .venv

# UV ile sanal ortam oluşturma (otomatik)
uv venv
```

### 🔄 Sanal Ortam Yönetimi

<table>
<tr>
<th>Platform</th>
<th>Aktivasyon</th>
<th>Deaktivasyon</th>
</tr>
<tr>
<td><strong>macOS/Linux</strong></td>
<td><code>source .venv/bin/activate</code></td>
<td rowspan="2"><code>deactivate</code></td>
</tr>
<tr>
<td><strong>Windows</strong></td>
<td><code>.venv\Scripts\activate</code></td>
</tr>
</table>

> ⚠️ **Önemli:** Her proje için ayrı sanal ortam kullanın!

---

## 🐙 Git Temelleri

### 🔧 Temel Git İş Akışı

```bash
# Projeyi başlatma
git init
git add .
git commit -m "🎉 İlk commit"

# Günlük iş akışı
git pull                           # Uzak değişiklikleri çek
git add .                          # Değişiklikleri sahneye al
git commit -m "✨ Yeni özellik"    # Commit yap
git push                           # Uzak repo'ya gönder
```

### 🌿 Branch Yönetimi

```bash
# Yeni branch oluştur ve geç
git checkout -b feature/new-analysis

# Branch'ler arası geçiş
git checkout main
git checkout feature/new-analysis

# Branch'i birleştir
git merge feature/new-analysis
```

---

## 📂 Klasör ve Dosya Yapısı

```
📁 my_data_science_project/
├── 📁 src/                    # 🎯 Ana kaynak kodları
│   ├── __init__.py
│   ├── data_processing.py
│   ├── models.py
│   └── utils.py
├── 📁 tests/                  # 🧪 Test dosyaları
│   ├── test_data_processing.py
│   └── test_models.py
├── 📁 notebooks/              # 📓 Jupyter Notebook'lar
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 03_modeling.ipynb
├── 📁 data/                   # 📊 Veri dosyaları
│   ├── raw/                   # Ham veri
│   ├── processed/             # İşlenmiş veri
│   └── external/              # Dış kaynak veriler
├── 📁 docs/                   # 📚 Dokümantasyon
├── 📁 scripts/                # 🔧 Yardımcı scriptler
├── 📄 main.py                 # 🚀 Ana giriş noktası
├── 📄 README.md               # 📖 Proje açıklaması
├── 📄 pyproject.toml          # ⚙️ Proje konfigürasyonu
├── 📄 .gitignore              # 🚫 Git ignore kuralları
└── 📁 .venv/                  # 🐍 Sanal ortam
```

---

## ⚙️ Konfigürasyon Dosyaları

### 📋 `pyproject.toml` Örneği

```toml
[project]
name = "my-data-science-project"
version = "0.1.0"
description = "Gelişmiş veri bilimi projesi"
authors = [
    { name = "Your Name", email = "your.email@example.com" }
]
readme = "README.md"
requires-python = ">=3.10"
license = { text = "MIT" }

dependencies = [
    "numpy>=1.24.0",
    "pandas>=2.0.0",
    "matplotlib>=3.7.0",
    "seaborn>=0.12.0",
    "scikit-learn>=1.3.0",
    "jupyter>=1.0.0"
]

[dependency-groups]
dev = [
    "pytest>=7.0.0",
    "black>=23.0.0",
    "flake8>=6.0.0",
    "mypy>=1.0.0"
]
docs = [
    "sphinx>=6.0.0",
    "sphinx-rtd-theme>=1.2.0"
]

[tool.black]
line-length = 88
target-version = ['py310']

[tool.pytest.ini_options]
testpaths = ["tests"]
python_files = ["test_*.py"]
```

### 🚫 `.gitignore` Örneği

```gitignore
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
*.egg-info/
.installed.cfg
*.egg

# Virtual Environment
.venv/
venv/
env/

# IDE
.vscode/
.idea/
*.swp
*.swo
*~

# Data files
*.csv
*.xlsx
*.parquet
*.pickle
*.pkl
data/raw/*
data/processed/*
!data/raw/.gitkeep
!data/processed/.gitkeep

# Jupyter Notebooks
.ipynb_checkpoints/
*.ipynb

# Logs
*.log
logs/

# OS
.DS_Store
Thumbs.db

# Machine Learning
models/
checkpoints/
wandb/
mlruns/
```

---

## 🛠️ Yaygın Kullanılan Ek Komutlar

### 📓 Jupyter & Notebook

```bash
# Jupyter Lab başlat
jupyter lab

# Jupyter Notebook başlat
jupyter notebook

# Notebook'u Python scriptine çevir
jupyter nbconvert --to python notebook.ipynb
```

---

## 🚀 Hızlı Başlangıç Adımları

<div align="center">

### 🎯 5 Dakikada Proje Kurulumu

</div>

```bash
# 1️⃣ Proje oluştur
uv init my_analysis --python=3.11
cd my_analysis

# 2️⃣ Sanal ortamı aktif et
source .venv/bin/activate  # macOS/Linux
# .venv\Scripts\activate   # Windows

# 3️⃣ Temel paketleri yükle
uv add numpy pandas matplotlib jupyter
uv add pytest black --group dev

# 4️⃣ Git deposu başlat
git init
git add .
git commit -m "🎉 İlk commit"

# 5️⃣ Jupyter başlat ve çalışmaya başla!
jupyter lab
```

---

<div align="center">

### 🎉 Artık Hazırsınız!

*Modern veri bilimi projesi geliştirme yolculuğunuzda başarılar!*

<img src="https://img.shields.io/badge/Made%20with-❤️-red.svg" alt="Made with Love">

</div>

---

<details>

- 📖 [UV Dokümantasyonu](https://docs.astral.sh/uv/)
- 🐙 [Git Dokümantasyonu](https://git-scm.com/doc)
- 🐍 [Python Rehberi](https://docs.python.org/3/)
