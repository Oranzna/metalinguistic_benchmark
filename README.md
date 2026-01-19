A Metalinguistic Benchmark Based on WALS

### Overview 
This is a large-scale multilingual benchmark that evaluates metalinguistic knowledge in large language models using typological features from the World Atlas of Language Structures (WALS). 

The benchmark covers 192 linguistic features across 2,660 languages.

### Task Definition
Given a linguistic question derived from a WALS feature with a set of possible answers for a specific language, the model must predict the correct typological category for that language. 

### Prompt
The benchmark is evaluated using a single prompt. The prompt template used in our experiments is provided in a separate file. 

### Data Splits
| Split | Samples |
| :--- | :--- |
| Training | 134 |
| Validation | 29 |
| Test | 29 |

### Data Format
Each feature is stored in JSONL format: 
{"feature_id": "1A", 
"feature_name": "Consonant Inventories", 
"domain": "Phonology", 
"question": "How large is the consonant inventory in the `<LANGUAGE>` language?", 
"possible_answers": "Small; Moderately small; Average; Moderately large; Large", 
"ground_truth": {"Abipón": "Moderately small", "Abkhaz": "Large", "Alabama": "Small", "Aché": "Small" /* additional languages omitted/}}

`<LANGUAGE>` is replaced with a specific language name at inference time. 

### Linguistic Feature Coverage
| Category | Samples |
| :--- | :--- |
| Word Order | 56 |
| Nominal Categories | 29 |
| Simple Clauses | 26 |
| Phonology | 20 |
| Verbal Categories | 17 |
| Lexicon | 13 |
| Morphology | 12 |
| Nominal Syntax | 8 |
| Complex Sentences | 7 |
| Sign Languages | 2 |
| Clicks (Other) | 1 |
| Writing System (Other) | 1 |

### Language Coverage
Total number of languages covered: 2,660 world languages. 

### Evaluation
Predictions are evaluated by comparing model outputs to the WALS ground-truth categories. 

### Licence
The original WALS data is licensed under CC BY 4.0. The data has been adapted for use in this benchmark. 

Source:
Dryer, Matthew S. & Haspelmath, Martin (eds.).  
World Atlas of Language Structures Online.  
Max Planck Institute for Evolutionary Anthropology.  
https://wals.info


