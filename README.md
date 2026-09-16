# Geoportal: Analiza Dostępności „Miasto 15-Minutowe”

## 🌐 Link do Aplikacji Webowej
👉 **[Kliknij tutaj, aby otworzyć Geoportal Live](https://TWOJ-NICK.github.io/miasto-15-minut/)**

---

## 📌 O Projekcie
Aplikacja przedstawia przestrzenną analizę dostępności pieszej do podstawowych usług społeczno-gospodarczych (szkoły, apteki, markety, parki) w wybranym obszarze urbanistycznym.

- **Obszar badań:** Warszawa (Centrum)
- **Rozmiar komórki analitycznej:** Heksagon 300m
- **Układ współrzędnych analitycznych:** PL-1992 (EPSG:2180)

---

## 🛠️ Stos Technologiczny
* **ETL & Analityka Przestrzenna:** Python (`requests`, `qgis.core`, `QgsSpatialIndex`)
* **Źródło Danych:** OpenStreetMap (Overpass API)
* **Wizualizacja Kartograficzna:** QGIS (Rule-based renderer, HTML MapTips)
* **Web Mapping:** Leaflet (`qgis2web`), HTML5 / CSS3
* **Hosting:** GitHub Pages

---

## 📐 Metodyka Wyliczania Wskaźnika
Wskaźnik dostępności 15-minutowej ($Indeks$) wyliczany jest według wzoru:

$$Indeks = \left( \frac{N_{kategorii\_w\_heksagonie}}{N_{wszystkich\_badanych\_kategorii}} \right) \times 100\%$$

Gdze $N_{wszystkich\_badanych\_kategorii} = 4$ (Sklep spożywczy, Apteka, Szkoła, Park).

---

## 👨‍💻 Autor
* **Imię i Nazwisko:** Daniel Zaszewski
* **Kierunek:** GGG, GIS 5
* **Prowadzący:** Daniel Zaszewski i Marcin Stępień
