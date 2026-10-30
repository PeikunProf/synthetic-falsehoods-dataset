README: Corpus documents.csv

##1. Dataset overview

The principal corpus-level dataset supports the manuscript's computational analyses of human-generated factual information, human-generated misinformation, AI-rewritten factual information, AI-rewritten misinformation and synthetic falsehoods. The full study corpus is designed to contain 10,000 documents, evenly distributed across five information categories (2,000 documents per category):

- H-FI: human-generated factual information
- H-MI: human-generated misinformation 
- A-FI: AI-rewritten factual information
- A-MI: AI-rewritten misinformation
- SFs: synthetic falsehoods

The corpus spans four topical domains: politics, public health, science, and social affairs. Each document is associated with a document/pair identifier, a category, and a topical domain. Additional metadata are included where available and applicable to the document's production condition and source context.


## 2. Workbook organization

The supplied Excel workbook is organized into five worksheets, one for each information category:

| Worksheet | Category | Records in supplied workbook |
|---|---|---:|
| "H-FI" | Human-generated factual information | 2000 |
| "H-MI" | Human-generated misinformation | 2000 |
| "A-FI" | AI-rewritten factual information | 2000 |
| "A-MI" | AI-rewritten misinformation | 2000 |
| "SFs" | AI-generated synthetic falsehoods | 2000 |
| Total | | 10000 |

Each row represents one document. The "content" field contains the document text. The "pair_id" field identifies the corresponding item or matched item across categories, according to the corpus construction scheme. The same "pair_id" values occur in different category worksheets; therefore, "pair_id" should not be treated as a globally unique document identifier by itself. For analyses requiring a unique document key, combine the category label with "pair_id" or use the unique identifier supplied in the complete deposited dataset.


## 3. Variables and metadata

Column availability differs across worksheets. The following fields are present in the supplied workbook:

| Variable | Description | Availability / notes |
|---|---|---|
| "pair_id" | Identifier for the document or matched item/pair | Present in all five worksheets; values are reused across category worksheets. |
| "domain" | Topical domain of the document | Present in all worksheets. Observed values include 'politic', 'health', 'science', and 'social'. |
| "content" | Full textual content of the document | Present in all worksheets, subject to applicable copyright, data-use, and ethical restrictions. |
| "Time" | Date associated with the source document | Present in 'H-FI' only in the supplied workbook. |
| "Source" | Source/publisher label for the human factual document | Present in 'H-FI' only in the supplied workbook; observed examples include 'BBC', 'NPR', 'Reuters', 'SciFact', 'The Guardian	Politico'. |

| "model" | Generative model used to produce the document | Present in 'A-FI', 'A-MI', and 'SFs'. |
| "provider" | Provider/organization associated with the model | Present in 'A-FI' and 'SFs'; not present in the supplied 'A-MI' worksheet. |
| "temperature" | Model-generation temperature recorded for the document | Present in 'A-FI', 'A-MI', and 'SFs'. |
| "timestamp" | Date and time recorded for AI text generation | Present in 'A-FI', 'A-MI', and 'SFs'. |

The supplied workbook contains the following observed model labels: 'gpt-5.5', 'grok-4.6', and 'deepseek-v4-flash'. Provider labels observed in the workbook include 'OpenAI' and 'xAI'. These are metadata values as recorded in the workbook; they should not be interpreted as evidence of model versioning or generation settings beyond the fields explicitly provided.

## 4. Category definitions and distinctions

The five categories represent different combinations of production source and truth status:

| Category | Production source | Truth status | Description |
|---|---|---|---|
| H-FI | Human | Factual | Factual information produced by human sources. |
| H-MI | Human | False | Human misinformation produced by human sources. |
| A-FI | AI | Factual | Factual information produced by AI systems. |
| A-MI | AI | False | False information produced by AI systems. |
| SFs | AI | False | AI-generated synthetic falsehoods, distinguished as a separate category in the manuscript. |

The distinction between A-MI and SFs should follow the manuscript's operational definitions and stimulus-generation protocol. The category labels should be preserved as recorded in the deposited data; do not merge A-MI and SFs unless a specific analysis requires it and the recoding is documented.


## 5. Topical domains
The corpus is intended to cover four topical domains:

- `politic` — politics
- `health` — public health / health
- `science` — science
- `social` — social affairs

The labels above reflect the values observed in the supplied workbook. 

## 6. Identifiers and matched structure

The workbook uses 'pair_id' to link corresponding or related items across category worksheets. Because identifiers are reused across worksheets, 'pair_id' alone is not a globally unique document identifier. A category-qualified identifier (for example, category plus 'pair_id') can distinguish records across worksheets.

## 7. Version information

Dataset version: Corpus documents version 1 
Release date: 2026-10-30  
Last updated: 2026-10-30


