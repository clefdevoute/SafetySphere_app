# SafetySphere_app v1 250422
**Technologie:** ArcGIS Maps SDK for JavaScript v4.x, HTML5, CSS3
# Webová aplikace: Digitální dvojče Průmyslového Areálu ACHVL pro krizové řízení

**(Název v angličtině: Web Application: Digital Twin of ACHVL Industrial Complex for Crisis Management)**

Interaktivní webová aplikace vytvořená jako součást mé diplomové práce na **Univerzitě J.E. Purkyně v Ústí nad Labem, Fakultě životního prostředí, Katedra geoinformatiky**.

Aplikace slouží k vizualizaci a analýze detailního 3D digitálního dvojčete rozsáhlého průmyslového areálu ACHVL (Areál chemických výrob Lovosice). Hlavním účelem je demonstrovat praktické využití digitálního dvojčete a geoinformačních nástrojů pro podporu **krizového a bezpečnostního managementu**.

---

# Webová aplikace: Přístup

Usere name: viewer_fzp
Password: host_1234

---

This interactive web application was developed as part of my diploma thesis at **Jan Evangelista Purkyne University in Ústí nad Labem, Faculty of Environment, Department of Geoinformatics**.

The application visualizes and allows for analysis of a detailed 3D digital twin of the large ACHVL industrial complex (Lovosice Chemical Plant). Its primary goal is to demonstrate the practical application of digital twins and geoinformation tools to support **crisis and safety management**.

---

## Klíčové vlastnosti (Key Features)

*   **3D Vizualizace:** Interaktivní prohlížení vysoce detailního 3D modelu průmyslového areálu.
    *   *3D Visualization:* Interactive viewing of a highly detailed 3D model of the industrial complex.
*   **Analytické nástroje (ArcGIS Maps SDK for JS):**
    *   Měření vzdáleností a ploch (3D Measurement)
    *   Generování 3D profilů (Elevation Profile)
    *   Analýza viditelnosti (Viewshed Analysis)
    *   Tvorba 3D obalových zón (3D Buffers)
    *   *Analytical Tools (ArcGIS Maps SDK for JS):*
        *   Measuring distances and areas (3D Measurement)
        *   Generating 3D profiles (Elevation Profile)
        *   Viewshed Analysis
        *   Creating 3D buffer zones (3D Buffers)
*   **Podpora rozhodování:** Integrace s dalšími daty a vizualizacemi pro lepší situační povědomí v krizových situacích (v mé práci např. tematické vrstvy - *pozn. v tomto kódu pouze ukázka*).
    *   *Decision Support:* Integration with additional data and visualizations for improved situational awareness in crisis situations (e.g., thematic layers in my thesis - *note: this code contains only a demo*).

## Použité Technologie (Technologies Used)

*   **ArcGIS Maps SDK for JavaScript:** Hlavní knihovna pro tvorbu 3D mapové scény a integraci GIS funkcionalit.
*   **HTML5 / CSS3:** Struktura a styling webové stránky.
*   **JavaScript:** Aplikační logika a interaktivita.
*   **3D Model:** Aplikace pracuje s 3D modelem areálu ACHVL ve formátu SLPK (Scene Layer Package), hostovaným v ArcGIS Portal / Online.

---

*   **ArcGIS Maps SDK for JavaScript:** Primary library for creating the 3D map scene and integrating GIS functionalities.
*   **HTML5 / CSS3:** Structure and styling of the web page.
*   **JavaScript:** Application logic and interactivity.
*   **3D Model:** The application works with a 3D model of the ACHVL complex in SLPK (Scene Layer Package) format, hosted in ArcGIS Portal / Online.

## Spuštění aplikace (How to Run the Application)

1.  **Stáhněte si kód:** Naklonujte tento repozitář nebo si stáhněte ZIP archiv.
    *   *Download the code:* Clone this repository or download the ZIP archive.
2.  **Webový server:** Protože aplikace načítá externí zdroje (např. ArcGIS SDK), je nutné ji spouštět přes lokální webový server, nikoliv přímo otevřením `index.html` souboru v prohlížeči (kvůli omezením CORS).
    *   *Web Server:* Since the application loads external resources (e.g., ArcGIS SDK), it must be served via a local web server, not directly by opening the `index.html` file in a browser (due to CORS restrictions).
    *   **Doporučení (Recommendation):** Můžete použít jednoduchý lokální server jako např. [http-server](https://www.npmjs.com/package/http-server) (Node.js) nebo modul `http.server` v Pythonu (`python -m http.server`).
3.  **Nastavení 3D Modelu:**
    *   **Důležité:** 3D model areálu ACHVL použitý v mé diplomové práci **není veřejně dostupný** v tomto repozitáři.
    *   Aplikace načítá 3D scénu z ArcGIS Portal/Online pomocí jejího `portalItem.id` v souboru JavaScriptu (viz např. `script.js`, proměnná `webscene` nebo obdobně).
    *   Chcete-li aplikaci spustit s jiným 3D modelem, nahraďte `id` v kódu za `id` vaší vlastní veřejné nebo vámi dostupné WebScene (SCENE ID). Příklad WebScene ID pro demo: `"e9d0034d1e75463f9798d948e28f8d28"`
    *   *3D Model Configuration:*
        *   **Important:** The 3D model of the ACHVL complex used in my diploma thesis is **not publicly available** in this repository.
        *   The application loads a 3D scene from ArcGIS Portal/Online using its `portalItem.id` in the JavaScript file (e.g., `script.js`, variable `webscene` or similar).
        *   To run the application with a different 3D model, replace the `id` in the code with the `id` of your own public or accessible WebScene (SCENE ID). Example demo WebScene ID: `"e9d0034d1e75463f9798d948e28f8d28"`
4.  **Otevřete v prohlížeči:** Spusťte lokální server v kořenovém adresáři repozitáře a otevřete `index.html` v prohlížeči (např. `http://localhost:8080/`).
    *   *Open in Browser:* Start your local server in the repository's root directory and open `index.html` in your browser (e.g., `http://localhost:8080/`).

## Struktura Projektu (Project Structure)

*   `index.html`: Hlavní HTML soubor definující strukturu stránky a načítající styly a skripty.
*   `style.css`: Soubor s CSS styly pro vzhled aplikace.
*   `script.js`: Hlavní JavaScript soubor obsahující logiku aplikace, inicializaci 3D scény a nástrojů.
*   *(`přílohy/` nebo jiné složky - pokud tam máte např. obrázky pro readme)*

---

*   `index.html`: Main HTML file defining the page structure and loading styles and scripts.
*   `style.css`: CSS file for the application's styling.
*   `script.js`: Main JavaScript file containing the application logic, 3D scene, and tools initialization.
*   *(`attachments/` or other folders - if you have e.g., images for the readme)*

## Diplomová práce (Diploma Thesis)

Plný text diplomové práce "Tvorba digitálního dvojčete průmyslového areálu s využitím bezkontaktních metod sběru prostorových dat jako základ pro prostorové analýzy a simulace krizových situací", která popisuje celý výzkum včetně metodiky sběru dat, zpracování, fúze a podrobných analýz:

[Odkaz na vaši diplomovou práci - např. na repozitáři školy, pokud je veřejně dostupná]

---

The full text of the diploma thesis, describing the entire research including data acquisition methodology, processing, fusion, and detailed analyses:

[Link to your diploma thesis - e.g., on your university's repository, if publicly available]

## Poděkování (Acknowledgments)

Rád bych poděkoval svému vedoucímu práce **doc. Ing. Janu Pacinovi, Ph.D.** za cenné rady a podporu během celého projektu a vývojářům a komunitě ESRI developers  na základě čehož byla vytvořena tato apliakce.

---

I would like to thank my supervisor **doc. Ing. Jan Pacina, Ph.D.** for his valuable guidance and support throughout the project.

## Licence (License)

Tento projekt je zveřejněn pod [Zde vložte název licence, např. licencí MIT](LICENSE).

---

This project is licensed under the [Insert License Name Here, e.g., MIT License](LICENSE).
