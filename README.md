# Workshop: Feinstaub-Messwerte in Bayern analysieren

In Binder öffnen: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/byte-bayern/open-bydata-notebook-feinstaub/HEAD?urlpath=%2Fdoc%2Ftree%2Ffeinstaub_messwerte.ipynb)

## Workshop-Ziele und Inhalte

Dieser Workshop richtet sich an Einsteiger:innen und Interessierte, die sich mit offenen Daten beschäftigen möchten. Gemeinsam analysieren wir Luftqualitätsdaten aus Bayern und lernen dabei, wie man öffentlich verfügbare Daten nutzt, aufbereitet und visualisiert.

### Was erwartet Sie?

In diesem Workshop arbeiten wir mit einem Jupyter Notebook, das die Emissionswerte von **Stickstoffmonoxid (NO)** und **Ozon (O₃)** aus den Jahren 2015 bis 2024 analysiert. Sie lernen:

- **Daten laden und vorbereiten**: Wie man Daten aus öffentlichen Quellen herunterlädt und für die Analyse aufbereitet
- **Daten analysieren**: Welche Stationen haben die höchsten Emissionswerte? Wie haben sich die Werte über die Jahre entwickelt?
- **Visualisierungen erstellen**: Zeitreihen, Tagesverläufe und geografische Karten erstellen
- **Muster erkennen**: Zusammenhänge zwischen Standorten, Zeitpunkten und Emissionswerten identifizieren

#### Vorbereitung
- [ ] Notebook über MyBinder öffnen (siehe Anleitung unten)
- [ ] Sich mit der Jupyter Notebook-Oberfläche vertraut machen
- [ ] Die ersten Zellen durchlesen und verstehen

#### Während des Workshops
- [ ] Schritt für Schritt durch das Notebook arbeiten
- [ ] Code-Zellen ausführen und Ergebnisse interpretieren
- [ ] Eigene Experimente durchführen (z.B. andere Städte auswählen, andere Zeiträume analysieren)
- [ ] Fragen zu den Ergebnissen stellen und diskutieren

#### Nach dem Workshop
- [ ] Eigene Analysen mit anderen Emissionswerten durchführen (PM2.5, NO₂, SO₂)
- [ ] Weitere Datenquellen erkunden (z.B. Wetterdaten, Verkehrsdaten)
- [ ] Die erlernten Methoden auf andere Datensätze anwenden

### Notebook mit MyBinder starten

**MyBinder** ermöglicht es Ihnen, das Notebook direkt im Browser zu öffnen, ohne etwas auf Ihrem Computer installieren zu müssen.

1. **Öffnen Sie den folgenden Link in Ihrem Browser:**
   ```
   https://mybinder.org/v2/gh/[IHR-REPO-PFAD]/HEAD?labpath=notebooks%2Ffeinstaub%2Ffeinstaub_messwerte.ipynb
   ```
   *(Hinweis: Ersetzen Sie `[IHR-REPO-PFAD]` mit dem tatsächlichen GitHub-Repository-Pfad)*

2. **Warten Sie, bis die Umgebung geladen ist** (dies kann 1-2 Minuten dauern)

3. **Das Notebook öffnet sich automatisch** und Sie können sofort loslegen!

**Tipp:** Beim ersten Laden kann es etwas länger dauern. Alle notwendigen Pakete werden automatisch installiert.

### Ziele des Notebooks

Das Notebook führt Sie durch eine vollständige Datenanalyse-Pipeline:

1. **Datenvorbereitung**: Laden und Aufbereiten der Emissionsdaten von öffentlichen Quellen
2. **Explorative Analyse**: Identifikation von Mustern und Auffälligkeiten
3. **Zeitliche Analyse**: Entwicklung der Emissionswerte über die Jahre
4. **Räumliche Visualisierung**: Darstellung der Messstationen auf einer interaktiven Karte
5. **Interpretation**: Diskussion der Ergebnisse und möglicher Ursachen

### Inspirationen für weitere Analysen

Nach dem Workshop können Sie das Notebook erweitern und eigene Analysen durchführen:

- **Weitere Schadstoffe**: Analysieren Sie Feinstaub (PM2.5), Stickstoffdioxid (NO₂) oder Schwefeldioxid (SO₂)
- **Längere Zeiträume**: Erweitern Sie die Analyse auf historische Daten ab 1980
- **Vergleiche**: Vergleichen Sie verschiedene Städte oder Regionen miteinander
- **Korrelationen**: Untersuchen Sie Zusammenhänge mit Wetterdaten, Verkehrsdaten oder saisonalen Mustern
- **Gesundheitsrelevanz**: Vergleichen Sie die Messwerte mit WHO-Empfehlungen und Grenzwerten
- **COVID-19-Effekte**: Analysieren Sie, wie sich die Emissionswerte während der Pandemie verändert haben
- **Stadt-spezifische Analysen**: Nutzen Sie zusätzliche Datensätze aus Augsburg oder Nürnberg

---

## Lokale Installation

Wenn Sie das Notebook auf Ihrem eigenen Computer ausführen möchten, folgen Sie diesen Schritten:

### Voraussetzungen

- Python 3.12 oder höher
- pip

### Installation

1. **Repository klonen oder herunterladen:**
   ```bash
   git clone [REPOSITORY-URL]
   cd openbydata/notebooks/feinstaub
   ```

2. **Virtuelle Umgebung erstellen (empfohlen):**
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. **Abhängigkeiten installieren:**
   ```bash
   pip install pandas matplotlib seaborn folium geopy openpyxl
   ```

   Oder verwenden Sie die `environment.yml` mit conda:
   ```bash
   conda env create -f environment.yml
   conda activate demo_feinstaub
   ```

4. **Jupyter Notebook starten:**
   ```bash
   jupyter notebook feinstaub_messwerte.ipynb
   ```

### Benötigte Pakete

- `pandas`: Datenmanipulation und -analyse
- `matplotlib`: Grundlegende Visualisierungen
- `seaborn`: Erweiterte statistische Visualisierungen
- `folium`: Interaktive Karten
- `geopy`: Geocoding für Koordinaten
- `openpyxl`: Excel-Dateien lesen (für pandas)

---

## MyBinder-Setup

Dieses Notebook wurde für die Verwendung mit **MyBinder** konfiguriert, um eine reproduzierbare und zugängliche Umgebung zu schaffen.

### MyBinder-Konfiguration

Die MyBinder-Konfiguration basiert auf der `environment.yml`-Datei, die alle notwendigen Abhängigkeiten definiert:

- **Python 3.12**: Basis-Interpreter
- **Conda-Umgebung**: Verwaltung der System-Abhängigkeiten
- **pip-Pakete**: Python-Bibliotheken (pandas, matplotlib, seaborn, folium, geopy, etc.)

### Wie MyBinder funktioniert

1. **Repository-Verbindung**: MyBinder verbindet sich mit dem GitHub-Repository
2. **Umgebung bauen**: Basierend auf `environment.yml` wird eine Docker-Container-Umgebung erstellt
3. **Pakete installieren**: Alle in der YAML-Datei definierten Pakete werden installiert
4. **Jupyter starten**: Ein JupyterLab-Server wird gestartet und im Browser bereitgestellt

### Anpassungen der Umgebung

Um die MyBinder-Umgebung anzupassen, bearbeiten Sie die `environment.yml`:

- **Python-Version ändern**: Ändern Sie `python=3.12.12` auf die gewünschte Version
- **Pakete hinzufügen**: Fügen Sie neue Pakete unter `pip:` hinzu
- **System-Abhängigkeiten**: Fügen Sie conda-Pakete unter `dependencies:` hinzu

### Troubleshooting

- **Lange Ladezeiten**: Beim ersten Start baut MyBinder die Umgebung neu auf (5-10 Minuten). Spätere Starts sind schneller.
- **Paket-Fehler**: Überprüfen Sie die Versionsnummern in `environment.yml`
- **Memory-Probleme**: Große Datensätze können die Standard-MyBinder-Ressourcen überschreiten

---

---

# Workshop: Analyzing Fine Dust Measurements in Bavaria

## Workshop Goals and Content

This workshop is designed for beginners and those interested in working with open data. Together, we will analyze air quality data from Bavaria and learn how to use, prepare, and visualize publicly available data.

### What to Expect

In this workshop, we work with a Jupyter Notebook that analyzes emission values of **nitrogen monoxide (NO)** and **ozone (O₃)** from 2015 to 2024. You will learn:

- **Loading and preparing data**: How to download data from public sources and prepare it for analysis
- **Analyzing data**: Which stations have the highest emission values? How have values developed over the years?
- **Creating visualizations**: Creating time series, daily patterns, and geographic maps
- **Identifying patterns**: Recognizing relationships between locations, time points, and emission values

### Workshop TODOs

#### Preparation
- [ ] Open the notebook via MyBinder (see instructions below)
- [ ] Familiarize yourself with the Jupyter Notebook interface
- [ ] Read and understand the first cells

#### During the Workshop
- [ ] Work through the notebook step by step
- [ ] Execute code cells and interpret results
- [ ] Conduct your own experiments (e.g., select other cities, analyze different time periods)
- [ ] Ask questions about the results and discuss them

#### After the Workshop
- [ ] Conduct your own analyses with other emission values (PM2.5, NO₂, SO₂)
- [ ] Explore additional data sources (e.g., weather data, traffic data)
- [ ] Apply the learned methods to other datasets

### Starting the Notebook with MyBinder

**MyBinder** allows you to open the notebook directly in your browser without installing anything on your computer.

1. **Open the following link in your browser:**
   ```
   https://mybinder.org/v2/gh/[YOUR-REPO-PATH]/HEAD?labpath=notebooks%2Ffeinstaub%2Ffeinstaub_messwerte.ipynb
   ```
   *(Note: Replace `[YOUR-REPO-PATH]` with the actual GitHub repository path)*

2. **Wait until the environment is loaded** (this may take 1-2 minutes)

3. **The notebook opens automatically** and you can start immediately!

**Tip:** The first load may take a bit longer. All necessary packages are installed automatically.

### Notebook Goals

The notebook guides you through a complete data analysis pipeline:

1. **Data Preparation**: Loading and preparing emission data from public sources
2. **Exploratory Analysis**: Identifying patterns and anomalies
3. **Temporal Analysis**: Development of emission values over the years
4. **Spatial Visualization**: Displaying measurement stations on an interactive map
5. **Interpretation**: Discussion of results and possible causes

### Inspiration for Further Analyses

After the workshop, you can extend the notebook and conduct your own analyses:

- **Additional Pollutants**: Analyze fine dust (PM2.5), nitrogen dioxide (NO₂), or sulfur dioxide (SO₂)
- **Longer Time Periods**: Extend the analysis to historical data from 1980
- **Comparisons**: Compare different cities or regions with each other
- **Correlations**: Investigate relationships with weather data, traffic data, or seasonal patterns
- **Health Relevance**: Compare measurement values with WHO recommendations and limit values
- **COVID-19 Effects**: Analyze how emission values changed during the pandemic
- **City-Specific Analyses**: Use additional datasets from Augsburg or Nuremberg

---

## Local Installation

If you want to run the notebook on your own computer, follow these steps:

### Prerequisites

- Python 3.12 or higher
- pip

### Installation

1. **Clone or download the repository:**
   ```bash
   git clone [REPOSITORY-URL]
   cd openbydata/notebooks/feinstaub
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install pandas matplotlib seaborn folium geopy openpyxl
   ```

   Or use the `environment.yml` with conda:
   ```bash
   conda env create -f environment.yml
   conda activate demo_feinstaub
   ```

4. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook feinstaub_messwerte.ipynb
   ```

### Required Packages

- `pandas`: Data manipulation and analysis
- `matplotlib`: Basic visualizations
- `seaborn`: Advanced statistical visualizations
- `folium`: Interactive maps
- `geopy`: Geocoding for coordinates
- `openpyxl`: Reading Excel files (for pandas)

---

## MyBinder Setup

This notebook has been configured for use with **MyBinder** to create a reproducible and accessible environment.

### MyBinder Configuration

The MyBinder configuration is based on the `environment.yml` file, which defines all necessary dependencies:

- **Python 3.12**: Base interpreter
- **Conda environment**: Management of system dependencies
- **pip packages**: Python libraries (pandas, matplotlib, seaborn, folium, geopy, etc.)

### How MyBinder Works

1. **Repository Connection**: MyBinder connects to the GitHub repository
2. **Build Environment**: Based on `environment.yml`, a Docker container environment is created
3. **Install Packages**: All packages defined in the YAML file are installed
4. **Start Jupyter**: A JupyterLab server is started and provided in the browser

### Customizing the Environment

To customize the MyBinder environment, edit the `environment.yml`:

- **Change Python version**: Change `python=3.12.12` to the desired version
- **Add packages**: Add new packages under `pip:`
- **System dependencies**: Add conda packages under `dependencies:`

### Troubleshooting

- **Long loading times**: On first start, MyBinder rebuilds the environment (5-10 minutes). Subsequent starts are faster.
- **Package errors**: Check version numbers in `environment.yml`
- **Memory issues**: Large datasets may exceed standard MyBinder resources
