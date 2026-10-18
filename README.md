# INSTRUKCJA UŻYTKOWNIKA – POGODZINKA (PWA)

Witaj w **Pogodzince** – nowoczesnej, precyzyjnej aplikacji pogodowej PWA (Progressive Web App). Niniejszy poradnik krok po kroku wyjaśnia wszystkie funkcjonalności aplikacji, sposób instalacji na telefonie i komputerze oraz interpretację zaawansowanych parametrów meteorologicznych i astronomicznych.

---

## SPIS TREŚCI
1. [Instalacja na telefonie i komputerze (PWA)](#1-instalacja-na-telefonie-i-komputerze-pwa)
2. [Praca w trybie offline (brak internetu)](#2-praca-w-trybie-offline-brak-internetu)
3. [Wybór lokalizacji i ulubione miasta](#3-wybór-lokalizacji-i-ulubione-miasta)
4. [Główny panel pogodowy i telemetria IMGW](#4-główny-panel-pogodowy-i-telemetria-imgw)
5. [Nawigacja w czasie: 13-dniowy horyzont (-6 .. Dziś .. +6 dni)](#5-nawigacja-w-czasie-13-dniowy-horyzont--6--dziś---6-dni)
6. [Interaktywny wykres pogodowy](#6-interaktywny-wykres-pogodowy)
   - [Tryb 24-godzinny (dla wybranego dnia)](#tryb-24-godzinny-dla-wybranego-dnia)
   - [Tryb 13-dniowy (Przegląd wielodniowy / Tydzień)](#tryb-13-dniowy-przegląd-wielodniowy--tydzień)
7. [Fizyka atmosfery i parametry lotnicze](#7-fizyka-atmosfery-i-parametry-lotnicze)
8. [Panel astronomiczny i fazy światła (Złota i Błękitna Godzina)](#8-panel-astronomiczny-i-fazy-światła-złota-i-błękitna-godzina)
9. [24-godzinny rozkład godzinowy](#9-24-godzinny-rozkład-godzinowy)

---

## 1. INSTALACJA NA TELEFONIE I KOMPUTERZE (PWA)

Aplikacja **Pogodzinka** została stworzona w standardzie PWA (Progressive Web App). Oznacza to, że działa jak natywna aplikacja ze sklepu, nie zajmuje miejsca w pamięci telefonu i nie wymaga pobierania ze sklepu Google Play ani App Store.

### 📱 Android (Google Chrome / Brave / Edge / Samsung Internet):
1. Otwórz aplikację w przeglądarce w telefonie.
2. Na dole ekranu lub w menu przeglądarki (trzy kropki w prawym górnym rogu) pojawi się komunikat: **„Dodaj do ekranu głównego”** lub **„Zainstaluj aplikację”**.
3. Kliknij **Zainstaluj**.
4. Ikona Pogodzinki pojawi się na pulpicie Twojego telefonu i otworzy się w pełnym oknie, bez pasków adresu przeglądarki.

### 🍏 iPhone / iPad (Safari):
1. Otwórz stronę w przeglądarce **Safari**.
2. Kliknij ikonę **Udostępnij** (kwadrat ze strzałką w górę na dolnym pasku).
3. Przewiń listę w dół i wybierz **„Do ekranu początkowego”** (Add to Home Screen).
4. Kliknij **Dodaj** w prawym górnym rogu.

### 💻 Komputer PC / Mac (Chrome, Edge, Opera):
1. W pasku adresu przeglądarki po prawej stronie kliknij ikonę monitora ze strzałką (**„Zainstaluj Pogodzinka”**).
2. Potwierdź instalację – aplikacja uruchomi się w osobnym, dedykowanym oknie roboczym.

---

## 2. PRACA W TRYBIE OFFLINE (BRAK INTERNETU)

Dzięki wbudowanemu mechanizmowi **Service Worker** i pamięci lokalnej:
- Nawet po utracie łączności z siecią (np. w górach, na działce, w samolocie), aplikacja uruchamia się natychmiast.
- Wyświetlane są ostatnio pobrane dane pogodowe, wykresy i fazy słońca.
- U góry ekranu pojawi się dyskretny pomarańczowy wskaźnik **„Tryb offline (dane z pamięci)”**, informujący o pracy bez połączenia z siecią. Gdy tylko odzyskasz zasięg, dane zaktualizują się automatycznie.

---

## 3. WYBÓR LOKALIZACJI I ULUBIONE MIASTA

- **Wyszukiwarka z autouzupełnianiem**: Wpisz nazwę miejscowości (np. *Zakopane*, *Gdańsk*, *Wrocław*). System wyszukuje miejscowości w czasie rzeczywistym, obsługując polskie znaki.
- **Przycisk GPS (Lokalizator)**: Kliknij ikonę celownika obok wyszukiwarki, aby automatycznie pobrać pogodę dla Twojej bieżącej pozycji GPS.
- **Szybkie kafelki miast**: Bezpośrednio pod wyszukiwarką znajdują się skróty do najpopularniejszych miast w Polsce.
- **Ulubione lokalizacje**: Kliknij gwiazdkę przy nazwie miasta, aby zapisać je na stałe do listy ulubionych na pasku szybkiego dostępu.

---

## 4. GŁÓWNY PANEL POGODOWY I TELEMETRIA IMGW

Górny panel prezentuje najważniejsze warunki panujące w danej chwili:
- **Temperatura aktualna**: Duża, wyraźna wartość w stopniach Celsjusza.
- **Temperatura odczuwalna (Perceived / RealFeel)**: Uwzględnia wpływ wiatru i wilgotności na ludzkie ciało.
- **Zakres dobowy (Min / Max)**: Najniższa i najwyższa przewidywana temperatura dla bieżącego dnia.
- **Kluczowe metryki w kafelkach**:
  - **Wilgotność względna (%)**
  - **Ciśnienie atmosferyczne (hPa)**
  - **Prędkość i porywy wiatru (km/h)** wraz z kierunkiem na róży wiatrów
  - **Indeks promieniowania UV** (od 0 do 11+) z ostrzeżeniem o ochronie przeciwsłonecznej
  - **Stopień zachmurzenia nieba (%)**
- **Plakietka Telemetrii IMGW**:
  Dla lokalizacji w Polsce aplikacja automatycznie łączy się z najbliższą naziemną stacją synoptyczną **IMGW-PIB**. Plakietka pozwala porównać fizyczny pomiar ze stacji meteorologicznej z globalnym modelem matematycznym.

---

## 5. NAWIGACJA W CZASIE: 13-DNIOWY HORYZONT (-6 .. DZIŚ .. +6 DNI)

Pogodzinka oferuje unikalną oś czasu obejmującą **13 pełnych dni**:
- **Dni -6 do -1**: Analiza historyczna rzeczywistych warunków, jakie panowały w ubiegłym tygodniu.
- **Dzień 0 (Dziś)**: Warunki bieżące z precyzyjnym rozkładem godzina po godzinie.
- **Dni +1 do +6**: Średnioterminowa prognoza numeryczna.

### Przyciski nawigacji:
- **Poprzedni / Następny**: Płynne przeskakiwanie dzień po dniu w przód lub w tył.
- **Dziś**: Natychmiastowy powrót do dnia dzisiejszego.
- **Tydzień**: Przełącza całą aplikację w tryb przekrojowego wykresu wielodniowego (13 dni).

---

## 6. INTERAKTYWNY WYKRES POGODOWY

Wykres w Pogodzince to autorski, płynny silnik graficzny Canvas zoptymalizowany pod kątem ekranów dotykowych smartfonów.

### Tryb 24-godzinny (dla wybranego dnia)
W widoku 24-godzinnym możesz przełączać dwie dedykowane zakładki:
1. **Temperatura & Opady**:
   - Płynna linia temperatury z kolorowym gradientem.
   - Pionowe słupki na dole wykresu pokazujące intensywność deszczu lub śniegu (w milimetrach) dla każdej godziny.
2. **Zachmurzenie & Wiatr**:
   - Fioletowy profil zachmurzenia (0–100%).
   - Zielona linia prędkości wiatru oraz porywów (km/h).

**Interakcja (Scrubbing)**:
- Przesuń palcem lub kursorem myszy wzdłuż wykresu: pojawi się pionowa linia pomocnicza z pływającym dymkiem, pokazująca precyzyjną temperaturę, opad, wiatr i zachmurzenie dla wybranej godziny.
- Na wykresie dnia dzisiejszego zielona pulsująca linia oznacza aktualną godzinę.

---

### Tryb 13-dniowy (Przegląd wielodniowy / Tydzień)
Uruchamiany przyciskiem **„Tydzień”**:
- Prezentuje 3 równoległe, wygładzone krzywe termiczne:
  - 🔴 **Czerwona krzywa**: Maksymalna temperatura w ciągu dnia.
  - 🟡 **Bursztynowa krzywa**: Średnia temperatura dobowa.
  - 🔵 **Niebieska krzywa**: Minimalna temperatura nocna.
- Na dole wykresu widoczne są słupki sumy dobowej opadów (mm).
- **Punkty dni**: Na linii znajdują się kropki reprezentujące poszczególne dni. Aktualny dzień oznaczony jest wyróżniającym się zielonym punktem.
- **Wybór dnia**: Dotknij dowolnego dnia na wykresie – pod wykresem wyświetli się elegancka karta podsumowania wybranego dnia (temperatury, opady, wiatr, wschód i zachód słońca).
- **Przycisk „Zobacz pełny rozkład”**: Znajduje się na dole karty podsumowania – kliknięcie natychmiast przenosi do pełnego, 24-godzinnego rozkładu wybranego dnia.
- **Powrót**: Aby powrócić do widoku 24h, wystarczy ponownie nacisnąć podświetlony przycisk **„Tydzień”** na pasku nawigacyjnym (działa jako wygodny dwukierunkowy przełącznik).

---

## 7. FIZYKA ATMOSFERY I PARAMETRY LOTNICZE

Karta dedykowana pasjonatom meteorologii, wędrowcom górskim, pilotom dronów i lotniarzom:
1. **Punkt Rosy ($T_d$)**: Temperatura, przy której powietrze osiąga 100% nasycenia parą wodną. Jeśli temperatura powietrza spada do punktu rosy, pojawia się gęsta mgła, rosa lub szron.
2. **Wysokość Podstawy Chmur (Cloud Base wg wzoru Henniga)**:
   Szacowana wysokość w metrach nad poziomem gruntu, na której zaczynają formować się chmury konwekcyjne (Cumulus):
   $$\text{Wysokość} = (T - T_d) \times 125\text{ m}$$
   *Przykład*: Jeżeli temperatura wynosi 20°C, a punkt rosy 12°C, podstawa chmur znajduje się na około 1000 m nad gruntem.
3. **Gęstość Powietrza**: Rzeczywista masa jednego metra sześciennego powietrza (zwykle ok. 1.20–1.28 kg/m³). Kluczowy wskaźnik przy lotach dronami, samolotami oraz w balistyce.
4. **Wskaźnik Niestabilności Burzowej**: Ocenia energię termodynamiczną i wilgotność w dolnych warstwach troposfery, informując o ryzyku nagłych wyładowań atmosferycznych i burz gradowych.

---

## 8. PANEL ASTRONOMICZNY I FAZY ŚWIATŁA (ZŁOTA I BŁĘKITNA GODZINA)

Niezastąpione narzędzie dla fotografów, filmowców, spacerowiczów i wędkarzy:
- **Wschód i Zachód Słońca**: Dokładny czas pojawienia się i zniknięcia tarczy słonecznej za horyzontem.
- **Długość Dnia i Nocy**: Wyliczona z dokładnością do minuty wraz z informacją, o ile minut dzień jest dłuższy/krótszy od przesilenia.
- **Złota Godzina (Golden Hour)**: Czas tuż po wschodzie i przed zachodem słońca, gdy światło ma ciepłą, miękką, złocistą barwę – idealne warunki do portretów i zdjęć krajobrazowych.
- **Błękitna Godzina (Blue Hour)**: Czas tuż przed wschodem i po zachodzie słońca, gdy niebo przybiera głęboki, nasycony szafirowy odcień.
- **Południe Słoneczne**: Moment, w którym słońce osiąga najwyższy punkt na niebie (górowanie).

---

## 9. 24-GODZINNY ROZKŁAD GODZINOWY

Poziomy, przewijany horyzontalnie ciąg kafelków dla wszystkich 24 godzin wybranego dnia:
- Godzina (np. 08:00, 14:00, 21:00)
- Graficzna ikona stanu pogody (słońce, przelotny deszcz, burza, śnieg)
- Temperatura powietrza
- Prawdopodobieństwo i wielkość opadu (w mm)
- Prędkość i porywy wiatru
