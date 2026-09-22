# Sprawozdanie — Blok 1: Pozyskiwanie, Przekształcanie i Ładowanie Danych (ETL)

**Projekt:** Geoportal Miasto 15-Minutowe
**Przedmiot:** WebGIS

---

## Dane studenta

| Pole | Wartość |
|---|---|
| Imię i nazwisko | |
| Numer albumu | |
| Wybrane miasto | |
| Data wykonania ćwiczenia | |
| Link do repozytorium GitHub | |

---

## 1. Konfiguracja środowiska

- [ ] Uruchomiono QGIS 3.x i utworzono nowy projekt
- [ ] Ustawiono układ współrzędnych projektu na EPSG:2180
- [ ] Zainstalowano wtyczkę QuickOSM

---

## 2. Pobieranie danych wektorowych z OpenStreetMap

Krótko opisz przebieg pobierania danych (np. ewentualne problemy, modyfikacje zapytań QuickOSM):

> *(miejsce na opis)*

**Zrzut ekranu — panel QuickOSM z przykładowym zapytaniem:**

> *(wklej zrzut ekranu)*

### Zweryfikowane warstwy źródłowe

| Filar urbanistyczny | Kategoria POI | Liczba pobranych obiektów | Uwagi (duplikaty, obiekty odrzucone) |
|---|---|---|---|
| Obszar analizy | Granica miasta | | |
| Edukacja | Szkoły | | |
| Edukacja | Przedszkola i żłobki | | |
| Zdrowie | Przychodnie i szpitale | | |
| Zdrowie | Apteki | | |
| Handel i Usługi | Sklepy spożywcze i markety | | |
| Zieleń i Rekreacja | Parki, place zabaw, lasy miejskie | | |
| Transport | Przystanki komunikacji | | |

---

## 3. Standaryzacja geometrii i filtr przestrzenny

Opisz proces naprawy geometrii, generowania centroidów oraz przycinania do granic miasta:

> *(miejsce na opis)*

**Zrzut ekranu — przykład warstwy przed i po naprawie geometrii / konwersji do centroidów:**

> *(wklej zrzut ekranu)*

---

## 4. Łączenie warstw i standaryzacja atrybutów

Opisz sposób połączenia warstw tematycznych w 5 kategorii oraz standaryzację pól atrybutowych:

> *(miejsce na opis)*

**Zrzut ekranu — tabela atrybutów jednej ze scalonych warstw (np. `poi_zdrowie`) z widoczną kolumną `kategoria`:**

> *(wklej zrzut ekranu)*

---

## 5. Reprojekcja i zapis do GeoPackage

**Zrzut ekranu — panel Warstwy w QGIS z pełną listą warstw zapisanych w `Miasto15m.gpkg`:**

> *(wklej zrzut ekranu)*

### Lista zapisanych warstw

| Nazwa warstwy | Typ geometrii | Układ współrzędnych | Liczba obiektów |
|---|---|---|---|
| `granica_miasta` | Poligon | EPSG:2180 | |
| `poi_edukacja` | Punkt | EPSG:2180 | |
| `poi_zdrowie` | Punkt | EPSG:2180 | |
| `poi_handel` | Punkt | EPSG:2180 | |
| `poi_zielen` | Punkt | EPSG:2180 | |
| `poi_transport` | Punkt | EPSG:2180 | |

Nazwa pliku projektu: `Nazwisko_Blok1.qgz`

---

## 6. Zadania dodatkowe

Zaznacz wykonane zadania i uzupełnij wymagane elementy.

### D1: Przypisanie Dzielnic (+1 pkt)

- [ ] Wykonano

Opis / kolumna `nazwa_dzielnicy`:

> *(miejsce na opis)*

### D2: Przetwarzanie Wsadowe (+1 pkt)

- [ ] Wykonano

**Zrzut ekranu — poprawnie skonfigurowane okno przetwarzania wsadowego:**

> *(wklej zrzut ekranu)*

### D3: Zoptymalizowane Zapytanie do OSM (+3 pkt)

- [ ] Wykonano

**Zrzut ekranu — pomyślnie wykonane zapytanie XML w QuickOSM:**

> *(wklej zrzut ekranu)*

### D4: Podsumowanie statystyczne (+2 pkt)

- [ ] Wykonano

Treść zapytania SQL:

```sql

```

**Zrzut ekranu — wynik zapytania SQL:**

> *(wklej zrzut ekranu)*

---

## 7. Napotkane problemy i wnioski

> *(miejsce na krótkie podsumowanie — trudności, nietypowe przypadki w danych OSM, wnioski z wykonania ćwiczenia)*

---

## 8. Deklaracja samodzielności

Oświadczam, że powyższe sprawozdanie zostało wykonane samodzielnie w ramach indywidualnego studium przypadku.

Podpis (imię i nazwisko): _____________________________

---

## Ocena prowadzącego

### Zadania podstawowe

| Kryterium oceny | Punkty możliwe | Punkty przyznane | Komentarz |
|---|---|---|---|
| Poprawne pozyskanie danych przestrzennych w 5 filarach | 4 | | |
| Konwersja poligonów do punktów oraz docięcie obiektów do granicy miasta | 4 | | |
| Prawidłowe połączenie warstw tematycznych do 5 głównych kategorii | 4 | | |
| Usunięcie zbędnych pól OSM, dodanie i poprawne wypełnienie kolumny `kategoria` | 4 | | |
| Zapisanie dokładnie 6 przetransformowanych warstw (EPSG:2180) w jednym pliku `Miasto15m.gpkg` | 4 | | |
| **Suma — zadania podstawowe** | **20** | | |

### Zadania dodatkowe

| Zadanie | Punkty możliwe | Punkty przyznane | Komentarz |
|---|---|---|---|
| D1: Przypisanie Dzielnic | 1 | | |
| D2: Przetwarzanie Wsadowe | 1 | | |
| D3: Zoptymalizowane Zapytanie do OSM | 3 | | |
| D4: Podsumowanie statystyczne | 2 | | |
| **Suma — zadania dodatkowe** | **7** | | |

### Podsumowanie

| | |
|---|---|
| **Suma punktów za Blok 1** | **/ 27** |
| Data oceny | |
| Podpis prowadzącego | |

**Uwagi ogólne prowadzącego:**

> *(miejsce na komentarz)*
