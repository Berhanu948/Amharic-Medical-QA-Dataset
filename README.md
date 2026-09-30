## AmhMedQA: Amharic Medical Question–Answer Dataset
**Overview**

AmhMedQA.csv is an Amharic medical question–answer dataset developed for research on Amharic medical question answering and question-type classification. Each record consists of a question, its corresponding answer, and a question-category label. The dataset is intended to support research on natural language processing (NLP), particularly in medical question answering,
question classification, and transformer-based language models for Amharic.
The released dataset contains 1,000 question–answer pairs, represented as question–answer–category triplets.

**Dataset Structure**
The dataset is provided as a comma-separated values (CSV) file:

AmhMedQA.csv

Each row represents one question–answer–category triplet.

| Field      | Description                                                                               |
| ---------- | ----------------------------------------------------------------------------------------- |
| `question` | An Amharic medical question posed by a user or derived from a medical information source. |
| `answer`   | The corresponding answer to the medical question.                                         |
| `category` | The question-type category assigned to the question.                                      |

Example

| question                    | answer                                                             | category   |
| --------------------------  | ------------------------------------------------------------------ | ---------- |
| የወባ በሽታ ምልክቶች ምንድን ናቸው?/What are the symptoms of malaria? / | የወባ በሽታ ምልክቶች ትኩሳት፣ ብርድ ብርድ ማለት፣ ላብ እና የራስ ምታት ሊሆኑ ይችላሉ።/Signs of malaria can be fever, chills, sweating, and headaches. | List       |
| ወባ ምንድን ነው?/What is malaria? /     | ወባ በፕላዝሞዲየም ጥገኛ ተውሳክ የሚከሰት በትንኝ ንክሻ የሚተላለፍ በሽታ ነው።/Malaria is a disease you get from mosquito bites, caused by a plasmodium parasite/       | Definition |

*The examples above illustrate the schema and are provided for documentation purposes.*

## Question Categories

The `category` field represents the type of information requested by the question. The dataset uses four categories:

| Category        | Definition                                                                                                                                   |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Factoid**     | Questions seeking a specific fact, value, entity, symptom, cause, treatment, or other concise piece of information.                          |
| **List**        | Questions requesting multiple items, characteristics, symptoms, causes, treatments, prevention methods, or other enumerated information.     |
| **Definition**  | Questions asking for the meaning, definition, or explanation of a medical term, disease, condition, or concept.                              |
| **Description** | Questions requesting a broader explanation or description of a medical condition, procedure, process, intervention, or health-related topic. |

These categories are designed to distinguish different information needs expressed through medical questions.

**Data Format**

The CSV file contains three columns:
question,answer,category

All textual content is represented in UTF-8 encoding to preserve Amharic characters correctly.

When loading the dataset with Python and pandas:

```python
import pandas as pd

# 1. Load the dataset
# ------------------------------------------------------------

file_path = "AmhMedQA.csv"

df = pd.read_csv(
    file_path,
    encoding="utf-8"
)
print("Dataset shape:")
print(df.shape)

print("\nColumn names:")
print(df.columns.tolist())

```
**Source Provenance**

The question–answer pairs were constructed from a range of medical and health-information resources. The source materials include, where applicable:
* Medical and health-information documents, and educational materials such as from Bahir Dar Tibebe Gion Hospital, the Ethiopian Health Institute.
* Medical books and reference materials.
* Other relevant medical education and health-information resources.

The source materials were used to develop questions and corresponding answers for the dataset. Because the dataset contains medical information,
source provenance is important for enabling researchers to understand and verify the information represented in the question–answer pairs.
Where source-level metadata are available, they may include the document title, organization or publisher, bibliographic information or URL, publication/update information, and access date.
For source materials that cannot be publicly redistributed because of institutional, copyright, or access restrictions, 
the relevant documentation or source information may be made available **through the corresponding author upon reasonable request**, subject to applicable restrictions.

**Data Quality and Annotation**

The question–answer pairs were reviewed to improve the consistency and relevance of the dataset. Question categories were assigned according to predefined category definitions.
The dataset is intended primarily for NLP and machine-learning research. It should not be interpreted as a substitute for professional medical advice, diagnosis, or treatment.


**Intended Applications**

AmhMedQA.csv can be used for research and experimentation involving:

* Amharic medical question answering
* Medical question-type classification
* Amharic NLP
* Transformer-based text classification
* Multilingual and low-resource language modeling
* Medical information retrieval
* Question–answer dataset analysis
* Evaluation of Amharic language models
* Development of educational and research-oriented medical NLP systems

Researchers may use the dataset to develop and evaluate models such as BERT, mBERT, RoBERTa, XLM-R, AfroXLM-R, AmhBERT, and other transformer-based architectures.

**Limitations**
Several limitations should be considered when using the dataset:

1. The dataset is relatively small compared with large-scale English medical QA datasets.
2. The questions and answers represent selected medical and health-information topics rather than comprehensive coverage of all medical conditions.
3. The dataset is intended for research and NLP development and should not be used as an independent source for clinical decision-making.


**Encoding**

The dataset is encoded using UTF-8.

UTF-8 encoding is required to correctly read and display Amharic characters like:
```
df = pd.read_csv(
    "AmhMedQA.csv",
    encoding="utf-8")
```
**Repository Contents**

The repository distinguishes the **final released dataset** from supplementary research materials.

The principal released dataset is:AmhMedQA.csv
Supplementary code, notebooks, intermediate files, or experimental results, if included in the repository, are provided separately and should not be considered part of the final dataset release.

## Citation

If you use the AmhMedQA dataset in your research, please cite:

```bibtex
@dataset{bogale2026amhmedqa,
  author    = {Bogale Desta, Berhanu and
               Tegegne Asfaw, Tesfa and
               Teferra Abate, Solomon and
               Belay Gebremeskel, Gebeyehu},
  title     = {AmhMedQA: An Amharic Medical Question-Answer Dataset},
  year      = {2026},
  publisher = {GitHub},
  url       = {https://github.com/Berhanu948/Amharic-Medical-QA-Dataset}
}
```
**Ethical and Responsible Use**

AmhMedQA.csv is intended for academic and research purposes. Users should consider the potential consequences of applying automated NLP systems to medical information.

Model outputs generated using this dataset should be independently evaluated before being used in applications involving patients, healthcare professionals, or clinical decision-making.

Researchers should also respect the licensing, copyright, and access conditions associated with the original source materials.


**Contact**

For questions concerning the dataset, source documentation, or supporting materials, please contact the **corresponding author:berhanubogale0101@gmail.com**.
