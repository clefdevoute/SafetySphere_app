Na základě analýzy kódu verze 2.5 a porovnáním s aktuální funkcionalitou verze 3.0, zde je přehled hlavních změn a aktualizovaný README:

## Hlavní změny od verze 2.5 do 3.0:

### Nové funkce:
1. **Nástroj pro kreslení 3D zón (buffer zóny)** - umožňuje vytvářet 3D buffery kolem bodů, linií nebo polygonů
2. **Nástroj pro kreslení 3D objektů** - přidávání základních 3D tvarů (krychle, válec, koule, kužel) do scény
3. **Legenda** - dynamická legenda zobrazující symboly a popisy vrstev
4. **Vyhledávání** - widget pro geokódování a vyhledávání lokalit
5. **Vylepšené UI** - reorganizace ovládacích prvků pro lepší uživatelský zážitek

### Vylepšení existujících funkcí:
- **Rozšířené možnosti screenshotu** - více formátů a kvalit
- **Vylepšená analýza viditelnosti** - pokročilejší nastavení parametrů
- **Lepší správa vrstev** - rozšířené možnosti ovládání viditelnosti vrstev
- **Optimalizace výkonu** - vylepšené načítání a vykreslování 3D scény

---

# SafetySphere_app v3.0
**Datum poslední aktualizace:** [11.2025]

**Autor:** Oto Weber (clefdevout@gmail.com)

**Technologie:** ArcGIS Maps SDK for JavaScript v4.x, HTML5, CSS3, Calcite Design System

**Webová aplikace:** Digitální dvojče Průmyslového Areálu ACHVL pro krizové řízení
*(Název v angličtině: Web Application: Digital Twin of ACHVL Industrial Complex for Crisis Management)*

Interaktivní webová aplikace vytvořená jako součást diplomové práce na Univerzitě J.E. Purkyně v Ústí nad Labem, Fakultě životního prostředí, Katedra geoinformatiky. Verze 3.0 přináší výrazné rozšíření funkcionality o pokročilé nástroje pro 3D analýzy a vizualizaci.

Aplikace slouží k vizualizaci a analýze detailního 3D digitálního dvojčete rozsáhlého průmyslového areálu ACHVL (Areál chemických výrob Lovosice). Hlavním účelem je demonstrovat praktické využití digitálního dvojčete a geoinformačních nástrojů pro podporu krizového a bezpečnostního managementu.

**Webová aplikace:** ►►► [Přístup k 3D scéně ACHVL] ◄◄◄  
*Uživatelské jméno: viewer_fzp  
Heslo: host_1234*

This interactive web application was developed as part of my diploma thesis at Jan Evangelista Purkyne University in Ústí nad Labem, Faculty of Environment, Department of Geoinformatics. Version 3.0 significantly extends the functionality with advanced tools for 3D analysis and visualization.

The application visualizes and allows for analysis of a detailed 3D digital twin of the large ACHVL industrial complex (Lovosice Chemical Plant). Its primary goal is to demonstrate the practical application of digital twins and geoinformation tools to support crisis and safety management.

## Klíčové vlastnosti (Key Features)

### Základní funkcionalita:
- **3D Vizualizace:** Interaktivní prohlížení vysoce detailního 3D modelu průmyslového areálu
- **3D Visualization:** Interactive viewing of a highly detailed 3D model of the industrial complex

### Analytické nástroje (ArcGIS Maps SDK for JS):
- **Měření vzdáleností** (3D Direct Line Measurement)
- **Measuring distances** (3D Direct Line Measurement)
- **Plošné měření** (3D Area Measurement)
- **Area measurement** (3D Area Measurement)
- **Generování 3D profilů** (Elevation Profile)
- **Generating 3D profiles** (Elevation Profile)
- **Analýza viditelnosti** (Viewshed Analysis) s interaktivním náhledem z pozice pozorovatele
- **Viewshed Analysis** with an interactive preview from the observer's perspective
- **Tvorba snímku obrazovky** (Screenshot) s automatickým stažením
- **Creating a screenshot** (Screenshot) with automatic download

### NOVÉ ve verzi 3.0:
- **Kreslení 3D zón** - vytváření buffer zón kolem objektů
- **3D Zone Drawing** - creating buffer zones around objects
- **Kreslení 3D objektů** - přidávání základních 3D tvarů do scény
- **3D Object Drawing** - adding basic 3D shapes to the scene
- **Interaktivní legenda** - dynamické zobrazení symboliky vrstev
- **Interactive Legend** - dynamic display of layer symbology
- **Vyhledávání lokalit** - geokódování a vyhledávání v mapě
- **Location Search** - geocoding and map search functionality
- **Vylepšené ovládání** - optimalizované uživatelské rozhraní
- **Enhanced Controls** - optimized user interface

### Podpora rozhodování:
Integrace s dalšími daty a vizualizacemi pro lepší situační povědomí v krizových situacích (včetně tematických vrstev a pokročilých 3D analýz).

### Decision Support:
Integration with additional data and visualizations for improved situational awareness in crisis situations (including thematic layers and advanced 3D analyses).

## Použité Technologie (Technologies Used)

- **ArcGIS Maps SDK for JavaScript (v4.31+):** Hlavní knihovna pro tvorbu 3D mapové scény a integraci GIS funkcionalit
- **ArcGIS Maps SDK for JavaScript (v4.31+):** Primary library for creating the 3D map scene and integrating GIS functionalities
- **Calcite Design System:** Moderní UI komponenty pro konzistentní uživatelské rozhraní
- **Calcite Design System:** Modern UI components for consistent user interface
- **HTML5 / CSS3:** Struktura a styling webové stránky
- **HTML5 / CSS3:** Structure and styling of the web page
- **JavaScript (ES6+):** Aplikační logika a interaktivita
- **JavaScript (ES6+):** Application logic and interactivity
- **3D Model:** Aplikace pracuje s 3D modelem areálu ACHVL ve formátu I3S/Scene Layer, hostovaným v ArcGIS Online/Enterprise
- **3D Model:** The application works with a 3D model of the ACHVL complex in I3S/Scene Layer format, hosted in ArcGIS Online/Enterprise

## Spuštění aplikace (How to Run the Application)

1. **Stáhněte si kód:** Naklonujte tento repozitář nebo si stáhněte ZIP archiv
2. **Download the code:** Clone this repository or download the ZIP archive

3. **Webový server:** Protože aplikace načítá externí zdroje (ArcGIS SDK), je nutné ji spouštět přes lokální webový server, nikoliv přímo otevřením souboru v prohlížeči (kvůli CORS)
4. **Web Server:** Since the application loads external resources (ArcGIS SDK), it must be served via a local web server, not directly by opening the file in a browser (due to CORS)

   **Doporučení:** Použijte jednoduchý lokální server jako `http-server` (Node.js) nebo `python -m http.server`
   **Recommendation:** Use a simple local server like `http-server` (Node.js) or `python -m http.server`

5. **Nastavení 3D Scény:**
   - Aplikace umožňuje načíst jakoukoliv veřejně dostupnou Web Scénu z ArcGIS Online/Portalu zadáním jejího Portal Item ID
   - Při prvním spuštění je k dispozici vstupní pole pro ID scény a několik ukázkových tlačítek
   - ID naposledy načtené scény se ukládá do lokálního úložiště prohlížeče
6. **3D Scene Configuration:**
   - The application allows loading any publicly available Web Scene from ArcGIS Online/Portal by entering its Portal Item ID
   - On first launch, a scene ID input field and several sample buttons are available
   - The ID of the last loaded scene is stored in the browser's local storage

   **Důležité:** 3D model areálu ACHVL použitý v diplomové práci není veřejně dostupný. Pro testování použijte ID vlastní scény nebo jedno z poskytnutých ukázkových ID
   **Important:** The 3D model of the ACHVL complex used in the diploma thesis is not publicly available. For testing, use your own scene ID or one of the provided sample IDs

7. **Otevřete v prohlížeči:** Spusťte lokální server v kořenovém adresáři repozitáře a otevřete `index.html` v prohlížeči (např. `http://localhost:8080/`)
8. **Open in Browser:** Start your local server in the repository's root directory and open `index.html` in your browser (e.g., `http://localhost:8080/`)

## Struktura Projektu (Project Structure)

- `index.html` - Hlavní HTML soubor definující strukturu stránky, obsahující CSS styly a JavaScriptovou logiku aplikace
- `index.html` - Main HTML file defining the page structure, containing CSS styles, and the application's JavaScript logic
- `ujep_logo.png`, `fzp_logo.png` - Obrázky log použité na úvodní obrazovce
- `ujep_logo.png`, `fzp_logo.png` - Logo images used on the splash screen

## Diplomová práce (Diploma Thesis)

Plný text diplomové práce "Tvorba digitálního dvojčete průmyslového areálu s využitím bezkontaktních metod sběru prostorových dat jako základ pro prostorové analýzy a simulace krizových situací", která popisuje celý výzkum včetně metodiky sběru dat, zpracování, fúze a podrobných analýz:

[https://www.researchgate.net/profile/Oto-Weber?ev=hdr_xprf]

The full text of the diploma thesis, "Creation of a digital twin of an industrial area using non-contact methods of spatial data collection as a basis for spatial analyses and simulations of crisis situations," describing the entire research including data acquisition methodology, processing, fusion, and detailed analyses:

[https://www.researchgate.net/profile/Oto-Weber?ev=hdr_xprf]

## Poděkování (Acknowledgments)

Rád bych poděkoval svému vedoucímu práce doc. Ing. Janu Pacinovi, Ph.D. za cenné rady a podporu během celého projektu. Dále děkuji vývojářům a komunitě Esri za poskytnutí nástrojů a zdrojů, na jejichž základě byla tato aplikace vytvořena.

I would like to thank my supervisor doc. Ing. Jan Pacina, Ph.D. for his valuable guidance and support throughout the project. I also thank the Esri developers and community for providing the tools and resources upon which this application was built.

## Licence (License)

Tento projekt je zveřejněn pod [MIT License].

This project is licensed under the [MIT License].
