# schema-docs

Schema.org-style documentation for your schema.

## Installation

We recommend managing your schema in a Github repo and running this software automatically when the schema changes using a Github Workflow.

1. Create a Github repo with your JSON-LD application profile and schema files.
2. Copy `workflow.yml` to `/.github/workflows/` in your repo.
3. Go to `Repo settings > Code and automation > Actions > General` and set "Workflow permissions" to read and write. Note: you might have to enable this organization-wide.
5. Go to `Repo settings > Code and automation > Pages > Source` and set Github pages "source" to "Github Actions".
3. Copy `example-config.json` to the root of your repo and rename to `config.json`. Adjust the configuration according to your needs. Details can be found in the next section.

## Configuration

The configuration file can contain the following keys:

| Name          | Description   | Example |
| ------------- | ------------- | ------- |
| `schemas`  | List of paths of schemas to take into account. If a directory is added, all files in that directory must be schemas and will be loaded. | `["./schemas", "./my_schema.ttl"]` |
| `application_profile`  | Path to the application profile. For example: `./jsonldcontext.jsonld` |
| `domain` | List of properties that define the domain of a property in your schemas. Especially useful when using schema.org, which defines domain using their own [domainIncludes](https://schema.org/rangeIncludes) property | `["http://www.w3.org/2000/01/rdf-schema#domain", "https://schema.org/domainIncludes"]` |
| `range` | List of properties that define the range of a property in your schemas. Especially useful when using schema.org, which defines range using their own [rangeIncludes](https://schema.org/rangeIncludes) property | `["http://www.w3.org/2000/01/rdf-schema#range", "https://schema.org/rangeIncludes"]` |
| `title` | The title to use on the index page and the header of the docs. | `Documentation for My Profile` |
| `language` | | |
| `html_template` | The HTML template file to use | `./template.html` |
| `output_folder` | Path where the output HTML files will be outputted | `./doc` |

## Development of this project

`python -m venv venv`

`source ./venv/bin/activate`

`pip install -r requirements.txt`

`python main.py`
