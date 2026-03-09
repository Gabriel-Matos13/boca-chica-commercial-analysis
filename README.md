# boca-chica-commercial-analysis
Geospatial data extraction and B2B market gap analysis of the commercial ecosystem in Boca Chica, DR, using Python and Excel.
# 📊 Boca Chica Commercial Census & Market Gap Analysis

**Author:** Gabriel Matos | Data Scientist & Analytics Partner

## 🎯 Project Overview
This project maps the commercial ecosystem of Boca Chica, a major tourist municipality in the Dominican Republic. By extracting real-time geospatial data, the goal was to structure a comprehensive commercial census, analyze industry density, and identify structural market gaps and B2B opportunities. 

Because the essence is in the details, this analysis goes beyond simply counting businesses. It uncovers a critical "Digitalization Gap" separating the booming tourist economy from the local supply chain.

## 🛠️ Tech Stack & Tools
* **Language:** Python 3
* **Libraries:** `requests` (API Calls), `pandas` (Data Cleaning, Deduplication & Structuring), `time` (Pagination handling).
* **Data Source:** Google Maps Places API (Nearby Search).
* **Visualization & Modeling:** Microsoft Excel (VLOOKUP categorizations, advanced Pivot Tables, and Pivot Charts).

## 🗺️ Methodology
1. **Automated Extraction:** Deployed a Python script to query the Google Places API within a 3-kilometer radius of Boca Chica's center (covering the tourist hub, the main highway, and the local residential areas). The script iterated through a master list of 50+ specific industry types to bypass API output limits.
2. **Data Cleaning:** Extracted JSON responses were normalized into a Pandas DataFrame. Duplicate entries were removed using unique `Place_ID` identifiers, resulting in a clean dataset of **693 unique businesses**.
3. **Macro-Sector Mapping:** To generate executive-level insights, the raw `Main_Classification` data (containing dozens of highly specific sub-categories) was mapped into **8 functional Macro Sectors** using a custom dictionary and `VLOOKUP` logic in Excel.

## 💡 Key Analytical Insights
The visualization of the 693 structured records revealed significant anomalies in the local economic infrastructure:

* **The HORECA Monopoly:** The ecosystem is overwhelmingly dominated by the **Hospitality & Tourism** sector (289 businesses) and **Retail & Shopping** (127 businesses), confirming the area's massive consumer-driven economy.
* **The B2B & Logistics Deficit:** Despite having a cluster of over 400 consumer-facing businesses that require constant supply and maintenance, the **B2B & Logistics** sector registered only **15 businesses** (e.g., industrial laundries, hardware stores, courier services).
* **The Digitalization Gap (Collection Bias):** The extreme lack of B2B support services on the map strongly suggests a *Collection Bias*. These businesses likely exist physically but lack any digital footprint (Google Business Profiles). This represents a massive opportunity for digital onboarding consulting and B2B service expansion.

## 🚧 Next Steps: Phase 2 (Cross-Referencing Official Data)
This repository represents **Phase 1** of an ongoing market research project. 

To calculate the exact digitalization deficit of the municipality, **Phase 2** will involve acquiring the official physical commercial registry from the local City Council (*Ayuntamiento de Boca Chica*). By cross-referencing the official government tax records with this digital census, the next phase will reveal the precise percentage of businesses operating completely "offline," turning current hypotheses into quantified facts.

---
*Note: The `API_google.txt` file containing the Google Cloud credentials has been intentionally excluded from this repository for security purposes.*
