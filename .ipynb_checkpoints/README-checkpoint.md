# Dataset of 17th century Dutch Painters
## webscraped from Wikipedia and Wikidata

The data contains wikipedia articles from over 400 Dutch 18th century painters, and metadeta about their yeor of birth, year of death, place of birth, place of death, gender and their wikidata identifiers.

Possible uses for this dataset could be finding which cities birthed renowned Dutch painters, or researsch which painters have the longest wikipedia articles. 

Other kinds of analysis can be done by looking gender, birth years, or locations. It is also possible to reconcile geogrpahical data for the birth and death places and make geographical visual representations, for example.

Textual analysis or NLP methods can also be performed on the Wikipedia articles in this dataset.

## 1. Data Collection

The data in this dataset has been scraped from both [Wikipedia](wikipedia.org) and [Wikidata](wikidata.org).
Wikipedia

The [Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Policy%3ATerms_of_Use) state that:

"You are free to:

- Read and Print our articles and other media free of charge.
- Share and Reuse our articles and other media under free and open licenses.
- Contribute To and Edit our various websites or Projects."

This dataset, including wikipedia articles and metadata about 17th century Dutch painters, is therefore published with no rights reserved.

The source code of the webscraping can be found in the webscraper.ipynb file in this repo. Pleaso note that I have included json files that can be used so you don't have to perform the https requests for the 'links' and the 'wikidata_links' variables, which take several minutes to complete. Within the Jupyter Notebook, there is code that imports these json files back into Python variables which can be used to perform the rest of the code. (These json files have been created on Decemebr 4th 2025)

### 1.1 Text Cleaning

The citations (like [1] and [3]) have been removed from the strings that contain the Wikipedia articles. Please note that no further preprocessing steps have been performed (lowercasing, punctuation removal).

## 2. Metadata

The main dataset can be found in the following file:
#### cleaned_data.csv

| Columns         | Description     |
|-----------------|-----------------|
| Name|Name of the painter (from wikidata) |
| Wikidata Identifier| Qnumber of the painter's wikidata item|
| Wikiepedia Article|Article collected from Wikipedia about the painter, citations removed|
| Gender |Gender of the painter (from wikidata)|
| Year of Birth| Birthyear of the painter (from wikidata)|
| Year of Death| Deathyear of the painter (from wikidata)|
| Place of Birth|Place of birth of painter (from wikidata)|
| Place of Death|Place of death of painter (from wikidata)|


