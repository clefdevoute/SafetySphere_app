# SafetySphere_app v2.5
**Datum poslední aktualizace: [23.05.2024]**

Autor: Oto Weber (clefdevout@gmail.com)

Technologie: ArcGIS Maps SDK for JavaScript v4.x, HTML5, CSS3

## Webová aplikace: Digitální dvojče Průmyslového Areálu ACHVL pro krizové řízení
(Název v angličtině: Web Application: Digital Twin of ACHVL Industrial Complex for Crisis Management)

Interaktivní webová aplikace vytvořená jako součást mé diplomové práce na Univerzitě J.E. Purkyně v Ústí nad Labem, Fakultě životního prostředí, Katedra geoinformatiky. Tato verze (v2.5) rozšiřuje původní funkcionalitu o nové nástroje.

Aplikace slouží k vizualizaci a analýze detailního 3D digitálního dvojčete rozsáhlého průmyslového areálu ACHVL (Areál chemických výrob Lovosice). Hlavním účelem je demonstrovat praktické využití digitálního dvojčete a geoinformačních nástrojů pro podporu krizového a bezpečnostního managementu.

### Webová aplikace: ►►► ►► ► Přístup k 3D scéně ACHVL ◄ ◄◄ ◄◄◄
Usere name: `viewer_fzp`
Password: `host_1234`

---

This interactive web application was developed as part of my diploma thesis at Jan Evangelista Purkyne University in Ústí nad Labem, Faculty of Environment, Department of Geoinformatics. This version (v2.5) extends the original functionality with new tools.

The application visualizes and allows for analysis of a detailed 3D digital twin of the large ACHVL industrial complex (Lovosice Chemical Plant). Its primary goal is to demonstrate the practical application of digital twins and geoinformation tools to support crisis and safety management.

## Klíčové vlastnosti (Key Features)

*   **3D Vizualizace:** Interaktivní prohlížení vysoce detailního 3D modelu průmyslového areálu.
    *   *3D Visualization: Interactive viewing of a highly detailed 3D model of the industrial complex.*
*   **Analytické nástroje (ArcGIS Maps SDK for JS):**
    *   Měření vzdáleností (3D Direct Line Measurement)
        *   *Measuring distances (3D Direct Line Measurement)*
    *   **NOVÉ (v2.5):** Plošné měření (3D Area Measurement)
        *   ***NEW:** Area measurement (3D Area Measurement)*
    *   Generování 3D profilů (Elevation Profile)
        *   *Generating 3D profiles (Elevation Profile)*
    *   Analýza viditelnosti (Viewshed Analysis) s interaktivním náhledem z pozice pozorovatele
        *   *Viewshed Analysis with an interactive preview from the observer's perspective*
    *   **NOVÉ (v2.5):** Tvorba snímku obrazovky (Screenshot) s automatickým stažením
        *   ***NEW:** Creating a screenshot (Screenshot) with automatic download*
    *   *(Poznámka: Funkce 3D obalových zón (3D Buffers) byla součástí původního konceptu DP, v této verzi kódu není implementována)*
*   **Podpora rozhodování:** Integrace s dalšími daty a vizualizacemi pro lepší situační povědomí v krizových situacích (v mé práci např. tematické vrstvy - pozn. v tomto kódu pouze ukázka základní funkcionality).
    *   *Decision Support: Integration with additional data and visualizations for improved situational awareness in crisis situations (e.g., thematic layers in my thesis - note: this code contains only a demo of basic functionality).*

## Použité Technologie (Technologies Used)

*   **ArcGIS Maps SDK for JavaScript (v4.31):** Hlavní knihovna pro tvorbu 3D mapové scény a integraci GIS funkcionalit.
    *   *ArcGIS Maps SDK for JavaScript (v4.31): Primary library for creating the 3D map scene and integrating GIS functionalities.*
*   **HTML5 / CSS3:** Struktura a styling webové stránky.
    *   *HTML5 / CSS3: Structure and styling of the web page.*
*   **JavaScript (ES6+):** Aplikační logika a interaktivita.
    *   *JavaScript (ES6+): Application logic and interactivity.*
*   **3D Model:** Aplikace pracuje s 3D modelem areálu ACHVL ve formátu SLPK (Scene Layer Package), hostovaným v ArcGIS Portal / Online, nebo s jakoukoliv jinou Web Scénou.
    *   *3D Model: The application works with a 3D model of the ACHVL complex in SLPK (Scene Layer Package) format, hosted in ArcGIS Portal / Online, or any other Web Scene.*

## Spuštění aplikace (How to Run the Application)

1.  **Stáhněte si kód:** Naklonujte tento repozitář nebo si stáhněte ZIP archiv.
    *   *Download the code: Clone this repository or download the ZIP archive.*
2.  **Webový server:** Protože aplikace načítá externí zdroje (např. ArcGIS SDK), je nutné ji spouštět přes lokální webový server, nikoliv přímo otevřením `index.html` souboru v prohlížeči (kvůli omezením CORS).
    *   *Web Server: Since the application loads external resources (e.g., ArcGIS SDK), it must be served via a local web server, not directly by opening the `index.html` file in a browser (due to CORS restrictions).*
    *   **Doporučení (Recommendation):** Můžete použít jednoduchý lokální server jako např. `http-server` (Node.js) nebo modul `http.server` v Pythonu (`python -m http.server`).
3.  **Nastavení 3D Scény (Web Scene):**
    *   Aplikace umožňuje načíst jakoukoliv veřejně dostupnou Web Scénu z ArcGIS Online/Portalu zadáním jejího Portal Item ID.
    *   Při prvním spuštění je k dispozici vstupní pole pro ID scény a několik ukázkových tlačítek.
    *   ID naposledy načtené scény se ukládá do lokálního úložiště prohlížeče.
    *   *3D Scene Configuration (Web Scene):*
        *   *The application allows loading any publicly available Web Scene from ArcGIS Online/Portal by entering its Portal Item ID.*
        *   *On first launch, a scene ID input field and several sample buttons are available.*
        *   *The ID of the last loaded scene is stored in the browser's local storage.*
    *   **Důležité:** 3D model areálu ACHVL použitý v mé diplomové práci není veřejně dostupný. Pro testování použijte ID vlastní scény nebo jedno z poskytnutých ukázkových ID.
        *   *Important: The 3D model of the ACHVL complex used in my diploma thesis is not publicly available. For testing, use your own scene ID or one of the provided sample IDs.*
4.  **Otevřete v prohlížeči:** Spusťte lokální server v kořenovém adresáři repozitáře a otevřete `index.html` v prohlížeči (např. `http://localhost:8080/`).
    *   *Open in Browser: Start your local server in the repository's root directory and open `index.html` in your browser (e.g., `http://localhost:8080/`).*

## Struktura Projektu (Project Structure)

*   `index.html`: Hlavní HTML soubor definující strukturu stránky, obsahující CSS styly a JavaScriptovou logiku aplikace.
    *   *`index.html`: Main HTML file defining the page structure, containing CSS styles, and the application's JavaScript logic.*
*   `ujep_logo.png`, `fzp_logo.png`: Obrázky log použité na úvodní obrazovce.
    *   *`ujep_logo.png`, `fzp_logo.png`: Logo images used on the splash screen.*
*   `(přílohy/ nebo jiné složky - pokud tam máte např. obrázky pro readme)`
    *   *(attachments/ or other folders - if you have e.g., images for the readme)*

## Diplomová práce (Diploma Thesis)

Plný text diplomové práce "Tvorba digitálního dvojčete průmyslového areálu s využitím bezkontaktních metod sběru prostorových dat jako základ pro prostorové analýzy a simulace krizových situací", která popisuje celý výzkum včetně metodiky sběru dat, zpracování, fúze a podrobných analýz:

**[Odkaz na vaši diplomovou práci - zatím není veřejně publikována]**

---

The full text of the diploma thesis, "Creation of a digital twin of an industrial area using non-contact methods of spatial data collection as a basis for spatial analyses and simulations of crisis situations," describing the entire research including data acquisition methodology, processing, fusion, and detailed analyses:

**[Link to your diploma thesis - e.g., on your university's repository**

## Poděkování (Acknowledgments)

Rád bych poděkoval svému vedoucímu práce doc. Ing. Janu Pacinovi, Ph.D. za cenné rady a podporu během celého projektu. Dále děkuji vývojářům a komunitě Esri za poskytnutí nástrojů a zdrojů, na jejichž základě byla tato aplikace vytvořena.

---

I would like to thank my supervisor doc. Ing. Jan Pacina, Ph.D. for his valuable guidance and support throughout the project. I also thank the Esri developers and community for providing the tools and resources upon which this application was built.

## Licence (License)

Tento projekt je zveřejněn pod **[MIT]**.

---

This project is licensed under the **[Insert License Name Here, e.g., MIT License]**.
