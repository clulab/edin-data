<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>

# Description

This repository contains "silver" biomolecular event mentions mined from the full text of a subset of [PubMed Central](https://www.ncbi.nlm.nih.gov/pmc/) publications using [Reach](https://github.com/clulab/reach/tree/d6a84be099a155b2bedb69f2102493d5db9399fb) (commit [`d6a84be099a155b2bedb69f2102493d5db9399fb`](https://github.com/clulab/reach/tree/d6a84be099a155b2bedb69f2102493d5db9399fb)).  A portion of this data was used to supplement the training of [`edin`](https://github.com/ZhengTang1120/Interpretation-Decoder-for-Neural-Network/tree/master).


## Rules
[`rules.yml`](./data/rules.yml) contains the [Odin rules](https://arxiv.org/abs/1509.07513) referenced in the event json data.

## Events
| File                                        | Event           |
|---------------------------------------------|-----------------|
| [`ph_events.jsonl`](./data/ph_events.jsonl) | Phosphorylation |
| [`lo_events.jsonl`](./data/lo_events.jsonl) | Localization    |
| [`ge_events.jsonl`](./data/ge_events.jsonl) | Gene Expression |

### Structure
Each `.jsonl` is a [JSON lines](http://jsonlines.org/) file contains a list of JSON objects where each object represents an event mention in the schema defined in [`oas3-data-schema.yml`](./data/oas3-data-schema.yml).  [Click this link](https://editor.swagger.io/?url=https://raw.githubusercontent.com/clulab/edin-data/dev/data/oas3-data-schema.yml) to render the schema in an editor.


#### Quick view
This command will pretty print the first gene expression event listed in [`ge_events.jsonl`](./data/ge_events.jsonl):

```bash
head -n 1 ge_events.jsonl | python -m json.tool
```
