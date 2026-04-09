Historical Mood-Based Content Generator
===
1. **Mood-History-Generator:**

 Analyzing the Collective Vibe Shift

2. **Description:**

This project investigates the relationship between the "background energy" of a societal crisis and the music choices of a population. Focusing specifically on the United States from 2019 to 2022, the study uses data to determine if external stress causes a shift in emotional resonance. By analyzing Spotify’s acoustic metrics against health reports, the goal is to prove whether society uses art as a Mirror (to reflect the crisis) or a Shield (to escape it).

3. **Tech Stack:**

Language: Python

Data Libraries: Pandas, NumPy

Statistics: SciPy (Pearson Correlation & Hypothesis Testing)

Visualization: Matplotlib, Seaborn

Logic: Object-Oriented Programming (OOP)

4. **Main Features:**

This project specifically focuses on a refined analysis of the United States from 2019 to 2022. While the original datasets provided global coverage, I strategically reduced the scope to a single region to ensure a higher level of analytical accuracy and a direct synchronization between the events and the population’s response. Our primary discovery was the "Escapism Effect": a statistically significant positive correlation (0.1608) with a p-value of $1.24 \times 10^{-5}$, proving that as crisis intensity rose, Americans reached for "brighter," higher-valence music to lift their spirits. Furthermore, I identified an "Energy Stability Paradox." While listeners significantly shifted the emotional mood of their music toward positivity, their preference for the physical intensity (Energy/Volume) of the tracks remained stable ($p = 0.369$). This reveals that while the crisis changed how we wanted to feel, it did not alter our acoustic preference for high-energy, active sounds, suggesting that we seek positivity without sacrificing the "drive" of our daily music.

5. **Feature Selection**

I selected specific columns to represent the "Emotional DNA" of the US population during the pandemic:

**Spotify Metrics (The "Internal Mood"):**

- af_valence: Measures musical "positivity." Used to track if the collective happiness of the nation shifted (the primary metric for Escapism).

- af_energy: Tracks intensity, loudness, and tempo. Used to see if the "drive" of music changed when the country went into lockdown.

- af_acousticness: Identifies tracks using natural instruments. Used to test if listeners sought "raw" or "honest" sounds for comfort.

- region: Filtered strictly for the United States to ensure regional alignment between the music and the crisis events.

- date: Our primary "anchor" column used to merge the two datasets and align them on a daily timeline.

**COVID-19 Metrics (The "External Event"):**

- new_confirmed: Represents Rising Anxiety. Each new case served as a "Stress Signal" in the daily US news cycle.

- new_deceased: Represents Collective Sadness. These figures show the tragedy and gravity of the event, allowing us to see if the national mood became more serious.

6. **How to run the Project:**

This project is designed to run in a Jupyter Notebook environment within VS Code. Follow these steps to execute the analysis:

**Prerequisites**

Ensure you have Python installed along with the necessary data science libraries. You can install them by running this command in your terminal:

Bash
pip install pandas matplotlib seaborn scipy

**Data Access**

Because the raw data exceeds GitHub's file size limits (2.8GB), the CSVs must be downloaded separately:

Download spotify.csv from Google Drive -> https://drive.google.com/file/d/1l3grfjWPG83gvx7cKn5CHnYav9CJ4tI6/view?usp=drive_link

Download covid_data.csv -> https://health.google.com/covid-19/open-data/raw-data

**Step-by-Step Execution:**

- Environment Setup: Open VS Code and ensure the Jupyter extension is installed.

- Data Placement: Place the following raw data files in the same folder as the project notebook:

    spotify.csv (The US music dataset)

    covid_data.csv (The US pandemic health reports)

- Loading Data: The script is optimized to load only the necessary columns (usecols) to save memory. Simply run the first cell to initialize the dataframes.

- Merge & Process: Execute the processing cells to synchronize the datasets using the date column. This creates a unified 731-day timeline.

- Statistical Analysis: Run the SciPy cell to calculate the Pearson Correlation and p-values. The results will print directly below the cell.

- Visualization: Run the final cell to generate the dual-axis "Vibe Shift" graph. The plot will be displayed in the notebook.

7. **Conclusion**

This project demonstrates that digital consumption is a real-time mirror for Public Mental Health. The findings suggest that music acts as a form of "emotional medicine," helping a population maintain psychological resilience during difficult historical moments.

Event-Timeline Mapping: Filters Spotify Top 200 data into "Before," "During," and "After" event phases.

Statistical Mood Proving: Uses SciPy T-Tests to determine if shifts in musical happiness (Valence) are statistically significant.

Historical Mood Generator: A recommendation engine that suggests music based on the "collective energy" of a specific historical date.
