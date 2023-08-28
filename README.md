# schema-docs

## Installation

1. Create a Github repo with your JSON-LD application profile and schema files.
2. Copy `workflow.yml` to `/.github/workflows/` in your repo.
3. Go to `Repo settings > Code and automation > Actions > General` and set "Workflow permissions" to read and write. Note: you might have to enable this organization-wide.
5. Go to `Repo settings > Code and automation > Pages > Source` and set Github pages "source" to "Github Actions".
3. Copy `example-config.json` to the root of your repo and rename to `config.json`. Adjust the location of your application profile and schema files.

## Development of this project

`python -m venv venv`

`source ./venv/bin/activate`

`pip install -r requirements.txt`

`python main.py`
