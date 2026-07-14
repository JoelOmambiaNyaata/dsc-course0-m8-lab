# Aviation Accident & Safety Analysis

An exploratory data analysis (EDA) and visualization project focused on historical aviation incident data. The primary objective is to assist an aviation insurance underwriter in establishing data-driven premium tiers, identifying high-risk assets, and selecting the safest aircraft makes and models for fleet investment.

---

## Key Executive Recommendations

### 1. Small Aircraft Fleet Recommendations (< 20 Seats)
*   **Recommended Manufacturers (Makes):** **Cessna**, **Piper**, and **Beech** consistently demonstrate the lowest mean fatal/serious injury fractions and lowest structural hull loss rates within the small aircraft category.
*   **Recommended Models:** The **Cessna 172** and **Piper PA-28** stand out as safety leaders. Because of their forgiving aerodynamic profiles and lower operational speeds, accidents involving these models heavily cluster around zero severe injuries.
*   **Underwriting Action:** Establish lower entry-level premiums for operators employing these standardized utility platforms, while applying surcharges to low-volume, experimental, or amateur-built small makes.

### 2. Large Aircraft Fleet Recommendations (>= 20 Seats)
*   **Recommended Manufacturers (Makes):** **Boeing**, **Airbus**, and **Embraer** display world-class structural containment profiles, with average injury fractions clustered tightly near `0.0`.
*   **Recommended Models:** Commercial standards like the **Boeing 737** and **Airbus A320** series display exceptional safety redundancy. Even during reported mechanical anomalies, passenger casualty rates remain statistically negligible.
*   **Underwriting Action:** Prioritize these multi-engine, commercially crewed models for preferred-tier liability rates.

---

## Visualizing Fleet Safety Profiles

Our analysis separated manufacturers into "Small" (< 20 seats) and "Large" (>= 20 seats) airplane cohorts to prevent general aviation utility planes from skewing the risk profiles of commercial airliners.

### Distribution of Injury Fractions for Top Small Aircraft Makes
![Small Aircraft Injury Distribution]![Top small Aircraft Makes](<manufacturer safety metrics.png>)

*   **Observation:** While small aircraft makes like **Cessna** and **Piper** have a strong cluster at `0.0` (no severe injuries), their distributions show elongated "necks" extending all the way up to `1.0`. This indicates that when accidents do occur in utility or training aircraft, there is a persistent risk of high-severity outcomes.

### Distribution of Injury Fractions for Top Large Aircraft Makes
!![Top large aircraft makes](<manufacturer safety metris 2.png>)

*   **Observation:** Commercial airliner makes (**Boeing**, **Airbus**, **Embraer**, **Bombardier**) display extremely bottom-heavy violin distributions. The data points are almost entirely concentrated at `0.0`, proving that modern commercial safety systems, dual-pilot operations, and strict regulations keep the actual passenger risk incredibly low even in anomalous events.

---

## Analysis of Operational Risk Factors

To further refine underwriting rules, we analyzed how environmental and mechanical factors affect aircraft damage and injury outcomes.

### Factor 1: Weather Conditions (Visual vs. Instrument Flight Rules)
*   **Finding:** Accidents occurring under **Instrument Meteorological Conditions (IMC)** (low visibility, heavy fog) result in a significantly higher mean injury fraction and hull destruction rate compared to those in **Visual Meteorological Conditions (VMC)**.
*   **Action:** Insurance policies should mandate higher premiums or specific pilot rating endorsements (e.g., active Instrument Rating) for operations regularly flying in non-visual corridors.

### Factor 2: Engine Configuration (Reciprocating vs. Gas Turbine)
*   **Finding:** **Reciprocating engines** (typical of single-engine light aircraft) carry substantially higher injury and destruction rates when emergencies occur. **Turbofan** and **Turbojet** configurations exhibit excellent safety buffers, benefiting from rigorous commercial maintenance regulations and multi-engine redundancies.
*   **Action:** Apply a risk premium credit to twin-engine turbine fleets and adjust single-engine reciprocating premiums upward.

---

## Technical Stack & Libraries Used
*   **Language:** Python
*   **Environment:** Jupyter Notebook / VS Code
*   **Core Libraries:** `pandas` (Data aggregation/wrangling), `matplotlib.pyplot` (Visualization engine), and `seaborn` (Statistical plotting and formatting)

