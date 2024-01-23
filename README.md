### About

This is the dataset for the project [Error Analysis of Tigrinya-English Machine Translation Systems](https://openreview.net/pdf?id=BQVqNyzCxx). In this project, we evaluated the status of three state-of-the-art MT systems that support the translation of Tigrinya to and from English: Google translate, Microsoft translator, and Lesan. Tigrinya is a language that is spoken by more than 10 million native speakers mainly in Tigray, Ethiopia and Eritrea. The details of the dataset are described below:

### Schema

- **Source:** This is the source url where the original data is scraped from. Typically takes a URL of a web resource as value but in some cases it could be page number of a textbook.

- **Domain:** refers to the area from which the text was gathered. The dataset reflects a diverse content. This feature can take one of the following values: Art and Culture, Business and Economy, Politics as well as Science and Technology.

- **SourceText:** is the source text given as input to the system for translation.

- **SourceLanguage:** the language of the source text. This takes values: English (en) or Tigrinya (ti).

- **TargetLanguage:** the language of the target translation output. This takes values: English (en) or Tigrinya (ti).

- **OutputGoogle:** text translation output from Google Translate.

- **EvalSentenceLevelGoogle:** sentence level evaluation of translation output from Google Translate.

- **EvalSnippetLevelGoogle:** snippet level evaluation of translation output from Google Translate.

- **ErrorTypeGoogle:** one or more Error type(s) according to MQM on translation output from Google Translate.

- **OutputMicrosoft:** translation output from Microsoft Translator.

- **EvalSentenceLevelMicrosoft:** sentence level evaluation of translation output from Microsoft Translator

- **EvalSnippetLevelMicrosoft:** snippet level evaluation of translation output from Microsoft Translator.

- **ErrorTypeMcirosoft:** One or more Error type(s) according to MQM on translation output from Microsoft Translator.

- **OutputLesan:** translation output from Lesan translation system.

- **EvalSentenceLevelLesan:** sentence level evaluation of translation output from LesanTranslate.

- **EvalSnippetLevelLesan:** Snippet level evaluation of translation output from LesanTranslate.

- **ErrorTypeLesan:** One or more Error type(s) according to MQM on translation output from Lesan Translate.

### Translation Quality Evaluation Scheme

We performed evaluation both at the sentence and snippet levels. This is to understand if there is a marked difference in handling short and long range dependencies. We’re using a Likert scale of 5 to quantify the quality (severity level) of a translation output. Annotations were first done at sentence level and then the whole snippet at once.

- Translation Quality sentence level: Is the evaluation of the translation output at sentence level using a Likert scale of 5 running form 0 to 4. Where 0 means broken, 1 - major, 2 - minor, 3 - neutral, 4 - kudos.

- Translation Quality snippet level: is the evaluation of the translation output at snippet level. Similar to sentence level quality check, we use a Likert scale of 5 running from 0 to 4. Where 0 means broken, 1 - major, 2 - minor, 3 - neutral, 4 - kudos.

- Error Type: is the error type according to DQF-11 MQM[b] of the translation output from a given machine translation system. It could take up one or more of the following values: Mistranslation, Omission, Untranslated, Accuracy, Fluency, Terminology, Style, Punctuation, Spelling, Grammar.

### Basic Statistics

In this dataset we have a total of 805 source snippets (402 in English and Tigrinya each). There are 833 sentences in Tigrinya and 563 sentences in English. On average each snippet contains 2 sentences (2.07 for Tigrinya snippets, 1.85 for English snippets). We give the breakdown of the token and sentence length by language and category in the following table:

**Number of snippets per domain**
| Domain | English | Tigrinya | Total Snippets |
| ---------------------- | -------------------------- | --------------------------- | -------------- |
| Arts and Culture | 100 | 101 | 201 |
| Science and Technology | 104 | 101 | 205 |
| Politics | 100 | 100 | 200 |
| Business and Economics | 99 | 100 | 199 |
| **TOTAL** | **403** | **402** | **805** |

_**Table 1:** provides the distribution of snippets categorized by domain and source language. It includes the number of English and Tigrinya snippets for each domain, as well as the total number of snippets in each category._

**Distribution of words in the dataset**

- On average, there are 32.52 words in each snippet across the whole dataset.

The average number of tokens per snippet over each domain is discussed on Table 2.

**Average number of tokens per snippet**

| Domain                 | English | Tigrinya |
| ---------------------- | ------- | -------- |
| Arts and Culture       | 48.95   | 41.73    |
| Science and Technology | 29.6    | 32.52    |
| Politics               | 29.7    | 31.93    |
| Business and Economics | 34.8    | 32.62    |

_**Table 2:** displays the distribution of tokens per snippet categorized by domain and source language. The data provides insights into the token distribution across different subject areas._

### Annotation Guideline

annotation was done using the TAUS rating guideline for the error severity in both snippet level and sentence level wise and the DQF-11 MQM standard error typology is used to identify the types of error by two native Tignrigna speakers and fluent English speakers.[c]

### Annotation

“human ratings based on expert-based human evaluation via Multidimensional Quality Metrics (MQM)”

Two experts were involved in the project. Both are native tigrinya speakers and are both fluent in English. Each annotator did 50% of the work.

### Format

Dataset is now available in three formats tsv, xlsx and JSON.

### License

This dataset is licensed under the [MIT](https://opensource.org/licenses/MIT) License.
