# Generational Music Cycles: Are Older Songs Making a Comeback?

**ISA 401 Final Project | Fall 2026 | Team 25 | Section A**

## Project Overview

Our team is investigating whether older songs experience renewed popularity in patterns consistent with generational music-cycle theories. Using historical Billboard Hot 100 chart data, MusicBrainz release information, and structured extraction from articles, we aim to identify songs that have experienced a resurgence and examine when and why they returned to popularity.

Our primary theoretical framework is Matt Bailey's Generational Music Theory. We will examine whether the timing of older songs' renewed chart success aligns with generational music-cycle patterns. We will also consider cultural influences, such as TikTok, television, movies, and other events that may contribute to a song's resurgence.

Our analysis focuses on Billboard Hot 100 chart history from 1990 onward. We plan to use the broader chart data to identify patterns and select approximately 10–15 songs for more detailed case studies.

The final results will be presented through an interactive Tableau or Power BI dashboard.

## Submission

| Item | Link |
|---|---|
| Dashboard (Tableau Public or Power BI) | [To be added] |
| Recorded technical presentation (YouTube, unlisted) | [To be added] |
| This repository | [Team25SpotifyTeam](https://github.com/wwalrath13/Team25SpotifyTeam) |

## Team

| Member | What I built / Responsibility | Portfolio project entry |
|---|---|---|
| Westin Walrath | Billboard Hot 100 web scraping and historical chart data acquisition | [To be added] |
| Elizabeth Culbertson | LLM-based structured extraction of articles discussing older songs and their resurgence | [To be added] |
| Zina Dupal | MusicBrainz API acquisition, recording data cleaning, and release-year investigation | [To be added] |

All team members will contribute to data integration, validation, dashboard development, and the final presentations.

Each member will also add the project to their individual portfolio and update the Skills section of their portfolio and `business_intelligence` repository.

## The Question

**To what extent do Billboard Hot 100 resurgences of older songs align with Matt Bailey's Generational Music Theory?**

Our team aims to investigate whether songs originally released decades earlier experience renewed popularity on the Billboard Hot 100 and whether these resurgences exhibit patterns consistent with generational music cycles.

We will examine three related questions:

1. **Resurgence timing:** How old are songs when they return to the Billboard Hot 100?
2. **Resurgence performance:** How frequently do older songs return, and how well do they perform?
3. **Resurgence explanations:** What documented cultural or media events are associated with renewed popularity?

This question is interesting because digital streaming, social media, television, and movies have created additional opportunities for listeners to discover music from earlier decades.

By combining historical chart rankings with original release information and article-based evidence, we hope to better understand the relationship between song age, renewed popularity, and generational music trends.

### Theoretical Framework

Our primary framework is **Matt Bailey's Generational Music Theory**, which explores recurring patterns in music preferences and cultural change across generations.

We will use Billboard chart histories to examine whether the observed timing of older songs' resurgences is consistent with the framework.

Additional background frameworks include:

- **Guy Zapoleon's Music Cycle Theory:** Examines recurring phases in contemporary popular music.
- **Strauss–Howe Generational Theory:** Proposes broader recurring generational patterns in society and culture.

These frameworks provide context for interpreting our findings. Our analysis is exploratory and will not attempt to establish that any theory is definitively true or false.

### Operational Definitions

For consistency, our team proposes the following definitions, subject to review as the project develops.

| Term | Proposed definition |
|---|---|
| Older song | A song originally released at least 20 years before the chart appearance being analyzed |
| Song age | Chart appearance year minus original release year |
| Billboard resurgence | An older song re-entering the Hot 100 after at least 52 consecutive weeks absent, followed by at least two appearances within six weeks |
| Resurgence year | Year of the qualifying Billboard re-entry |
| Resurgence strength | Number of weeks charted after re-entry and best chart position during that period |
| Resurgence explanation | A documented cultural, media, or other event associated with renewed popularity |

These thresholds are research-defined rather than official Billboard classifications. We will distinguish confirmed Billboard resurgences from cultural resurgences that do not meet the chart-based criteria.

## Data Sources

Our project uses three real-world sources and three acquisition methods: web scraping, API access, and LLM-based structured extraction.

| Source | Link | Method | One row represents | Code |
|---|---|---|---|---|
| Billboard Hot 100 | [Billboard Charts](https://www.billboard.com/charts/hot-100/) | Web scraping | One song's position on a weekly Hot 100 chart | `markdowns/01_acquire.Rmd` |
| MusicBrainz | [MusicBrainz API](https://musicbrainz.org/doc/MusicBrainz_API) | API | One MusicBrainz recording returned for a song and artist search | `markdowns/01_acquire.Rmd` |
| Music-related articles | [Article URLs to be documented] | LLM-based structured extraction | One structured article observation about a song's resurgence | [To be added] |

### Billboard Hot 100 — Westin

Billboard provides historical chart information, including song titles, artists, chart dates, and rankings.

We plan to use weekly Hot 100 data beginning in 1990 to identify older songs appearing on the charts and investigate potential resurgences.

The chart data will serve as the primary source for measuring popularity and chart performance.

### MusicBrainz — Zina

MusicBrainz provides recording and release information through its public API.

Our initial acquisition tested five songs:

1. "Billie Jean" — Michael Jackson
2. "Dreams" — Fleetwood Mac
3. "Running Up That Hill" — Kate Bush
4. "Bohemian Rhapsody" — Queen
5. "Everybody Wants to Rule the World" — Tears for Fears

The initial five-song acquisition returned **125 candidate recording entries**, with 25 results per search.

We identified 21 missing release years and no duplicate recording IDs in the collected sample.

The cleaning process standardizes text fields, converts release years to integers, and checks for duplicate recording identifiers.

Because MusicBrainz may return alternate recordings, remasters, or later releases, recording dates cannot automatically be interpreted as original song release dates. Original release years will require additional verification.

### Article-Based Structured Extraction — Elizabeth

Articles discussing older songs and renewed popularity will be used to identify documented factors associated with resurgence.

Potential factors include:

- TikTok and other social media platforms
- Television and film appearances
- Viral trends
- Artist-related events
- Other cultural influences

The structured extraction process is planned to capture song titles, artists, publication dates, reported resurgence events, and supporting evidence.

These observations will provide context for interpreting Billboard chart patterns.

## Pipeline

All core acquisition, cleaning, transformation, merging, and validation work will be performed in R.

| Step | File | What it does |
|---|---|---|
| 1. Acquire | `markdowns/01_acquire.Rmd` | Collect data from the MusicBrainz API and document acquisition; other source scripts will be incorporated |
| 2. Clean and transform | `markdowns/02_clean.Rmd` | Standardize data types, clean text fields, identify missing values, and remove duplicate records |
| 3. Merge | `markdowns/03_merge.Rmd` | Match songs across Billboard, MusicBrainz, and article-derived data |
| 4. Validate and summarize | `markdowns/04_validate.Rmd` | Check data quality, identify failed joins, and produce exploratory summaries |

Raw data are stored in `data/raw/`.

Cleaned and merged data are stored in `data/processed/`.

### Current Progress

- MusicBrainz API connection and initial recording searches completed.
- Five-song MusicBrainz test dataset acquired.
- MusicBrainz cleaning and initial data-quality checks completed.
- Billboard historical chart acquisition in progress.
- Article-based structured extraction in progress.
- Full dataset merging, validation, and dashboard development pending.

## How to Reproduce

1. Clone the team repository:

   `https://github.com/wwalrath13/Team25SpotifyTeam`

2. Open the project in RStudio.

3. Install the R packages required by the acquisition and cleaning scripts. The current MusicBrainz workflow uses `httr`, `jsonlite`, `dplyr`, and `readr`.

4. Configure any credentials required by other data sources using a local `.Renviron` file. Do not commit API keys or credentials to GitHub. The current MusicBrainz API workflow does not require an API key.

5. Run the acquisition scripts to obtain raw source data.

6. Run the cleaning scripts to create standardized datasets.

7. Run the merge and validation scripts after all three source datasets are available.

8. Load the final processed dataset into Tableau or Power BI to reproduce the dashboard.

The complete reproduction procedure, including any additional packages, source-specific scripts, and execution order, will be finalized when the full pipeline is integrated.

## The Final Dataset

**Planned file:** `data/processed/final_music_resurgence.csv`

**Planned unit of observation:** One song and its identified resurgence event, with associated chart performance, release information, and available article-based evidence.

The final dataset structure will be confirmed after the sources are integrated.

### Planned Variables

| Column | Type | Description | Source |
|---|---|---|---|
| `song_title` | Character | Standardized song title | Billboard / MusicBrainz |
| `artist` | Character | Standardized artist name | Billboard / MusicBrainz |
| `original_release_year` | Integer | Verified original song release year | MusicBrainz / verification |
| `resurgence_year` | Integer | Year of qualifying chart return | Billboard |
| `song_age` | Integer | Age of song at resurgence | Calculated |
| `peak_chart_position` | Integer | Best chart ranking during resurgence | Billboard |
| `weeks_on_chart` | Integer | Number of chart appearances during the defined resurgence period | Billboard |
| `resurgence_platform` | Character | Reported platform or cultural influence | Article extraction |
| `resurgence_event` | Character | Documented event associated with renewed popularity | Article extraction |
| `source_url` | Character | Supporting article URL | Article extraction |

These are proposed fields, not yet the confirmed columns of the merged dataset.

## Data Issues and How We Handled Them

### Missing Values

The initial MusicBrainz sample contains 21 records with missing release years.

These values were retained as missing rather than replaced with unverified dates.

### Duplicate Records

The initial MusicBrainz dataset contained no duplicate recording IDs.

The cleaning process nevertheless includes a duplicate-removal step based on the searched song, artist, and recording identifier.

### Multiple Recording Versions

MusicBrainz may return multiple recordings for the same song, including alternate performances, edits, and remasters.

We retain distinct recording identifiers while investigating which release information is appropriate for establishing the original song's age.

### Inconsistent Song and Artist Names

Song and artist names may differ across sources because of punctuation, capitalization, featured artists, and alternate titles.

The team will document matching and standardization decisions during the merge process.

### Incomplete Historical Coverage

The Billboard data begins in 1990, which may exclude earlier chart appearances.

Consequently, the first observed appearance in our dataset does not necessarily represent a song's original Billboard debut.

## Validation Table

The final validation table will be produced in `markdowns/04_validate.Rmd`.

| Rule | Current findings or planned check | Action |
|---|---|---|
| Missing MusicBrainz release year | 21 of 125 initial records | Preserve missing values and investigate original releases separately |
| Duplicate recording IDs | 0 in the initial sample | Check and remove duplicates where appropriate |
| Invalid release years | To be checked | Flag implausible years |
| Missing Billboard chart dates or ranks | To be checked | Flag incomplete observations |
| Invalid Billboard positions | To be checked | Flag positions outside 1–100 |
| Unmatched song and artist records | To be checked | Review and document failed joins |
| Unverified resurgence classification | To be checked | Separate confirmed, possible, and nonqualifying cases |

## Limitations

Our analysis has several limitations:

1. **Billboard coverage:** Chart observations beginning in 1990 do not provide complete historical chart information for songs released earlier.
2. **Release-date accuracy:** MusicBrainz recording dates may not reflect original song release dates.
3. **Popularity measurement:** Billboard Hot 100 performance measures chart success rather than total listening activity or cultural popularity.
4. **Generational interpretation:** Billboard rankings do not directly identify the ages or generations of listeners.
5. **Causation:** Articles may identify events associated with renewed popularity, but those associations do not necessarily establish causation.
6. **Case-study selection:** A limited number of featured songs cannot represent all older music or establish the universal validity of a generational theory.

Our conclusions will therefore focus on observed patterns and the extent to which they are consistent with the theoretical framework.

## Dashboard

The final dashboard will be created in Tableau or Power BI using the cleaned and merged dataset.

Planned visualizations include:

- Number of qualifying resurgences by original release decade
- Distribution of song ages at resurgence
- Chart performance of selected older songs
- Timelines of original releases and later chart appearances
- Reported cultural factors associated with renewed popularity

The dashboard will include interactive filters where useful and will be designed to communicate the main findings to a nontechnical audience.

## Presentations

The team will prepare two presentations:

**Recorded technical presentation (8–12 minutes):** Explain the research question, data acquisition, cleaning, merging, validation, and reproducibility of the R pipeline.

**In-class presentation (8–9 minutes):** Present the research question, dashboard, major findings, limitations, and conclusions.

All team members will participate in the in-class presentation.

## References and Frameworks

- [Matt Bailey — Introducing the Generational Music Theory](https://medium.com/@radiomatt1/introducing-the-generational-music-theory-d48e18e3f678)
- Guy Zapoleon — Music Cycle Theory (supporting framework; source to be added)
- Strauss–Howe Generational Theory (background framework; source to be added)
- [Billboard Hot 100](https://www.billboard.com/charts/hot-100/)
- [MusicBrainz API Documentation](https://musicbrainz.org/doc/MusicBrainz_API)
