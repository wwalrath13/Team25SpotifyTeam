# Are Older Songs Popular Today?

ISA 401 Final Project, Fall 2026, Team 25, Section A

## Project Overview 

Our team plans to investigate whether older songs remain popular in today's music streaming environment. Using Spotify Charts, MusicBrainz, and Last.fm, we aim to compare the popularity of songs released in different decades and explore whether older music continues to compete with newer releases. We plan to collect current music rankings, historical release information, and listening statistics to examine patterns across artists, genres, and countries. By combining these sources, we hope to create visualizations that show how song age relates to present-day popularity and identify older songs that continue to attract listeners.

## Submission

| Item | Link |
|---|---|
| Dashboard (Tableau Public or Power BI) | [link] |
| Recorded technical presentation (YouTube, unlisted) | [link] |
| This repository | [link] |

## Team

| Member | What I built | Portfolio project entry |
|---|---|---|
| Westin Walrath | [for example: the API pulls and the merge] | [https://USERNAME.github.io/portfolio/#...] |
| Elizabeth Culbertson | [ ] | [ ] |
| Zina Dupal | [ ] | [ ] |

Each member adds this project to their own portfolio site, in their own words, with a link
back to this repository and the dashboard, and updates the Skills section of their portfolio
and of their `business_intelligence` README with skills they used in this project.

## The Question

Are older songs still popular among today's music listeners, and how does their popularity compare to newer releases? Our team plans to investigate whether songs released in previous decades continue to appear on modern music charts and whether their popularity varies across artists, genres, and countries.

This question is interesting because music consumption is no longer limited to newly released songs. Streaming platforms allow listeners to rediscover older music, potentially giving songs a longer lifespan or renewed popularity years after their original release. By combining current music rankings with historical release information and listening statistics, we hope to identify patterns that would not be apparent from analyzing a single music dataset.

## Data Sources

At least three real-world sources, collected with at least two methods (web scraping, API,
LLM extraction from text).

| Source | Link | Method | One row is | Code |
|---|---|---|---|---|
| Spotify Charts | https://charts.spotify.com/home | Web scraping | One song's ranking for a country and chart date | `markdowns/01_acquire.Rmd` |
| MusicBrainz | https://musicbrainz.org/doc/MusicBrainz_API  | API | 	One recording or release record | [ ] |
| Last.fm | https://www.last.fm/api  | API | One artist or track's listening statistics | [ ] |

## Pipeline

| Step | File | What it does |
|---|---|---|
| 1. Acquire | `markdowns/01_acquire.Rmd` | [ ] |
| 2. Clean and transform | `markdowns/02_clean.Rmd` | [ ] |
| 3. Merge | `markdowns/03_merge.Rmd` | [ ] |
| 4. Validate and summarize | `markdowns/04_validate.Rmd` | [ ] |

Raw files go in `data/raw/`; the cleaned and merged files go in `data/processed/`.

## How to Reproduce

1. R version: [4.x.x]. Packages: [list them, or point to the setup chunk that installs them].
2. API keys: create a `.Renviron` file in this folder with these names (values are your own):
   - `[KEY_NAME]=`
3. Knit the four files in `markdowns/` in order, 01 to 04.

## The Final Dataset

- File: `data/processed/[name].csv`
- One row is: [ ]
- Rows and columns: [ ]

| Column | Type | Description | Source |
|---|---|---|---|
| [ ] | [ ] | [ ] | [ ] |

## Data Issues and How We Handled Them

[Missing values, inconsistent formats, duplicate records, mismatched keys: what you found and what you did.]

## Validation Table

The observations that break an expected rule (impossible values, duplicates, invalid labels or
codes, failed joins). Produced in `markdowns/04_validate.Rmd`.

| Rule | Rows that break it | What we did |
|---|---|---|
| [ ] | [ ] | [ ] |

## Limitations

[Assumptions, gaps in the data, and what the dataset cannot answer.]
