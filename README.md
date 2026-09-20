# 🏙️ Analiza Dostępności Przestrzennej — Miasto 15-Minutowe: [Nazwa Miasta]

> **Projekt laboratoryjny z Systemów Informacji Geograficznej (GIS)**  
> **Autor:** [Imię i Nazwisko]  
> **Nr albumu:** [123456]  
> **Kierunek / Grupa:** [Kierunek Studiów, Grupa Lab]  
> **Prowadzący:** [Tytuł/Stopień Imię i Nazwisko Prowadzącego]  
> 🌐 **Geoportal Online (GitHub Pages):** [Wklej link do swojego GitHub Pages, np. https://twoj-nick.github.io/geoportal-miasto-15m/]

---

## 📌 O Projekcie

Celem projektu jest wielokryterialna ocena dostępności pieszej do podstawowych usług społeczno-gospodarczych w **[Nazwa Miasta]** w ramach koncepcji **Miasta 15-Minutowego**. 

W ramach 5 bloków laboratoryjnych dokonano pozyskania danych przestrzennych (OpenStreetMap), budowy siatki analitycznej, wyznaczenia izochron sieciowych, identyfikacji białych plam (deficytów usługowych) oraz wyznaczenia optymalnych lokalizacji dla nowych inwestycji miejskich.

---

## 📊 Kluczowe Wskaźniki Efektywności (KPI)

| Wskaźnik | Stan przed inwestycją | Stan po symulacji ("What-If") | Różnica ($\Delta$) |
| :--- | :---: | :---: | :---: |
| **Średni wskaźnik dostępności ($I_{15m}$)** | `[np. 54.2%]` | `[np. 68.7%]` | `[+14.5 pp]` |
| **Pokrycie miasta ($K_{15m} \ge 60\%$)** | `[np. 42.0%]` | `[np. 59.5%]` | `[+17.5 pp]` |
| **Liczba obszarów deficytowych ($I_{15m} < 35\%$)** | `[np. 38 heksagonów]` | `[np. 12 heksagonów]` | `[-26 heksagonów]` |

---

## 🛠️ Metodyka i Etapy Realizacji

Projekt został zrealizowany w oprogramowaniu **QGIS 3.x** oraz w środowisku **WebGIS** przy użyciu następującej ścieżki analitycznej:

- [x] **Blok 1: Pozyskiwanie i czyszczenie danych (ETL)**
  * Pobranie i filtrowanie obiektów POI oraz sieci drogowej z OpenStreetMap (`QuickOSM`).
  * Normalizacja atrybutów, usunięcie duplikatów i transformacja do układu państwowego **`EPSG:2180` (PUWG 1992)**.
- [x] **Blok 2: Geoprocesing i Modelowanie Wskaźnika $I_{15m}$**
  * Utworzenie siatki heksagonalnej ($250\text{ m}$).
  * Skonstruowanie algorytmu w **QGIS ModelBuilder** wyliczającego wagowy wskaźnik dostępności dla 5 kategorii usług (Edukacja, Zdrowie, Handel, Zieleń, Transport).
- [x] **Blok 3: Kartografia, Atlas Dzielnicowy i WebGIS**
  * Opracowanie spójnej wizualnie mapy syntetycznej A3.
  * Wygenerowanie wielostronicowego **Atlasu PDF** dla dzielnic miasta.
  * Eksport geoportalu internetowego za pomocą wtyczki `qgis2web`.
- [x] **Blok 4: Analizy Sieciowe, KDE i Optymalizacja Lokalizacji**
  * Wyznaczenie rzeczywistych izochron pieszego dojścia ($5, 10, 15\text{ min}$) we wtyczce `ORS Tools` / `QNEAT3`.
  * Delimitacja pustyń usługowych metodą **Estymacji Gęstości Jąder (KDE)**.
  * Wyznaczenie 3 optymalnych lokalizacji nowych usług przy użyciu algorytmu **K-Means**.
- [x] **Blok 5: Raportowanie i Interaktywny Dashboard**
  * Opracowanie Menedżerskiego Raportu PDF dla Zarządu Miasta.
  * Stworzenie interaktywnego pulpitu nawigacyjnego **HTML5/JS (Leaflet + Chart.js)** podglądanego w rozszerzeniu *VS Code Live Server*.

---

## 🚀 Rekomendowane Nowe Inwestycje

Na podstawie analizy przestrzennej wyznaczono 3 optymalne punkty dla nowych obiektów usługowych, które w największym stopniu redukują deficyty mieszkańców:

1. **Punkt A (Dzielnica [Nazwa]):** `[Krótki opis, np. Rekomendowana budowa przychodni rejonowej przy ul. X]`
2. **Punkt B (Dzielnica [Nazwa]):** `[Krótki opis, np. Rekomendowana budowa parku i centrum lokalnego]`
3. **Punkt C (Dzielnica [Nazwa]):** `[Krótki opis, np. Rekomendowany punkt przedszkolny]`

---

## 📁 Struktura Repozytorium

```text
├── Miasto15m.gpkg             # Główna spójna baza GeoPackage (EPSG:2180)
├── Blok5_Final_Project.qgz    # Główny plik projektu QGIS (ścieżki względne)
├── index.html                 # Interaktywny Geoportal / Dashboard (dla GitHub Pages)
├── data/                      # Dane GeoJSON wyeksportowane do aplikacji webowej
│   ├── siatka.geojson
│   └── nowe_poi.geojson
├── raporty/                   # Wygenerowane raporty końcowe
│   ├── Raport_Wykonawczy_15m.pdf
│   └── Atlas_Dzielnic_15m.pdf
├── wykresy/                   # Wykresy statystyczne (.png)
└── README.md                  # Dokumentacja projektu
