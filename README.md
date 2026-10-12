# Movies & Shows Data Cleaning

A Python/pandas coursework project exploring a movies-and-shows cast dataset. The original notebook's saved inspection reports **85,579 rows and 9 columns**. Rows represent cast/credit entries; this is not a count of unique movies or shows.

## Work demonstrated
- Standardize column names and correct a malformed actor-name entry.
- Filter actor credits and extract unique titles by IMDb rating and release decade.
- Build reusable functions for cast lookup and score categorization.
- Handle missing scores without incorrectly categorizing them as low-rated.

## Run locally
Use Python 3.10 or newer in a virtual environment:

```bash
pip install -r requirements.txt
jupyter lab
```

Obtain the course-provided `movies_and_shows.csv` through your authorized course access and place it in `data/movies_and_shows.csv`. Alternatively set `MOVIES_DATA_PATH` to its path. Open `movies_shows_analysis.ipynb` and run cells in order. The source dataset is excluded; redistribution permission is not assumed.

## Portfolio improvements and limits
This copy adds portable loading, whitespace-based column normalization, value-based correction of `In??s Prieto`, a returned cast string rather than printing inside the function, and an explicit missing-score category. The original submission remains separate. Outputs are cleared because these edits have not been rerun against the source dataset. The original environment was not version-pinned.

The coursework functions named `get_unique_top_movies` and `get_top_movies_from_decade` include both movies and shows. The strict >9.0 example differs intentionally from the >= threshold function. Cast lookup matches titles exactly; different productions sharing a title may be combined. Score categorization uses the first matching row, so conflicting scores across same-name titles are not resolved. This is a pandas fundamentals project, not an ML model or recommendation engine.
