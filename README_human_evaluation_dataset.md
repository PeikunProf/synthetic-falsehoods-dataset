README: Trial-Level Human Evaluation Dataset

##1. Overview

This dataset contains de-identified trial-level observations from the human evaluation experiment reported in the manuscript "Beyond human deception: Cognitive-Linguistic signatures of AI-Generated falsehoods".

The data support analyses of five response outcomes:

- perceived credibility;
- perceived factual accuracy;
- sharing intention;
- perceived deceptive intent; and
- information-source attribution.

Each record represents an observation associated with a de-identified participant and a stimulus identifier. The dataset also records the stimulus content, domain, experimental category, and the participant's responses.

The dataset is intended to support verification and reproduction of the analyses reported in the manuscript. It does not contain direct participant identifiers.


##2. File contents and structure

The example data use a tab-delimited, trial-level table. The columns observed in the supplied example are listed below. 
| Variable | Description |
|---|---|
| "pair_id" | Identifier for a stimulus or stimulus-pair grouping. The exact meaning of the grouping should follow the study's data-generation protocol. |
| "participant_id" | De-identified participant identifier. |
| "content" | Text of the stimulus presented for evaluation. |
| "domain" | Content domain assigned to the stimulus. |
| "category" | Experimental stimulus category. The example includes labels such as `HFI`, `HMI`, `AFI`, and `SF`; see Section 3. |
| "credibility" | Participant's perceived-credibility response for the trial. |
| "accuracy" | Participant's perceived-factual-accuracy response for the trial. |
| "sharing_intention" | Participant's reported intention to share the stimulus. |
| "deceptive_intent" | Participant's rating or judgment of the perceived deceptive intent associated with the stimulus. |
| "source_prediction" | Participant's attribution of the stimulus source (for example, `Human` or `AI`). |


##3. Experimental categories and coding

The supplied example contains the following category codes:

| Code | Interpretation suggested by the manuscript's experimental design |
|---|---|
| `HFI` | Human-generated factual information |
| `HMI` | Human-generated misinformation |
| `AFI` | AI-rewritten factual information |
| `SF` | synthetic falsehood |

The `source_prediction` field records the participant's source attribution response; it is not necessarily the experimentally assigned source. In particular, a participant may attribute an AI-produced item to a human source or vice versa. 



## 4. Response Variables and Coding

The dataset contains five response variables: `credibility`, `accuracy`, `sharing_intention`, `deceptive_intent`, and `source_prediction`.

The four rating variables—`credibility`, `accuracy`, `sharing_intention`, and `deceptive_intent`—were recorded on a 7-point scale, with higher values indicating higher perceived credibility, greater perceived factual accuracy, stronger sharing intention, and stronger perceived deceptive intent, respectively. Values outside the range of 1–7 were treated as missing. Missing values were excluded only from analyses requiring the corresponding variable.

The variable `source_prediction` records participants' perceived information source, coded as `Human` or `AI`. This variable represents participants' source-attribution judgments rather than the experimentally assigned source. The ground-truth source and truth status were determined by the stimulus category and were independent of participants' judgments. The four experimental conditions were H-FI (human-generated factual information), H-MI (human-generated misinformation), A-FI (AI-rewritten factual information), and SFs (AI-generated synthetic falsehoods).

For descriptive summaries, missing rating values were median-imputed within participant and experimental condition before calculating condition-level means and 95% confidence intervals. This procedure was used for descriptive summaries; inferential analyses excluded observations with missing values only for the outcome under analysis. Participant, stimulus, pair, and domain identifiers were retained to preserve the hierarchical structure of the data.

The dataset uses the following coding conventions:

| Variable | Description | Coding |
|---|---|---|
| `credibility` | Perceived credibility | Integer rating from 1 to 7; higher values indicate greater perceived credibility |
| `accuracy` | Perceived factual accuracy | Integer rating from 1 to 7; higher values indicate greater perceived accuracy |
| `sharing_intention` | Intention to share the information | Integer rating from 1 to 7; higher values indicate stronger sharing intention |
| `deceptive_intent` | Perceived deceptive intent | Integer rating from 1 to 7; higher values indicate stronger perceived deceptive intent |
| `source_prediction` | Participant's perceived information source | `Human` or `AI` |
| `category` | Experimentally assigned stimulus condition | `HFI`, `HMI`, `AFI`, or `SF`, as encoded in the dataset |

The numerical rating scale ranges from 1 to 7. The specific verbal anchors presented to participants are not reproduced here; users should consult the original questionnaire for the exact item wording and response labels. Missing ratings are represented according to the missing-value convention used in the deposited data.


5. Experimental design and unit of observation

The dataset is organized at the trial level and includes de-identified participant and stimulus identifiers. Participants may contribute multiple observations, and a stimulus may be evaluated by multiple participants. Accordingly, observations should not automatically be assumed to be statistically independent. For analyses that account for repeated observations, use the participant and stimulus/pair identifiers in accordance with the manuscript's statistical models.

6. Privacy and de-identification

Participant identifiers are de-identified. Direct personal identifiers and variables not required for the reported analyses are excluded. 

7. Version and updates

Dataset version: human evaluation data 1  
Release date: 2026-10-30  
Last updated: 2026-10-30