# text-mining-test

This repository contains my solution to the text mining task (task-specific comments are in the notebook, not in the readme).

## Installation

To run the code, you need a jupyter lab and `spacy` and `pandas` libraries (you can install the latter with the following command)
```
$ python3 -m venv env
$ . env/bin/activate
$ pip install -r requirements.txt
$ pip install jupyterlab
$ jupyter lab
```

## Usage

See the solution [`here`](./solution.ipynb).

Output:
- [`0_processed_data.json`](./data/processed/0_processed_data.json): contains data in semi-structured format where each object represents a sentence with entities stored in a separate 'entities' key, as requested
- [`1_text_and_metadata.csv`](./data/processed/1_text_and_metadata.csv): represents the data in a tabular format, with each row containing a sentence from the document along with its identifiers (document_id, paragraph_id, sentence_id).
- [`2_entities.csv`](./data/processed/2_entities.csv): contains extracted entities, with each named entity represented in one row and linked to the metadata table through foreign keys
- [`3_aggregated_entities.csv`](./data/processed/3_aggregated_entities.csv): contains an aggregate table where each unique entity is represented in one row, showing its frequency across all documents and a list of documents where these entities were found (comma-separated).
