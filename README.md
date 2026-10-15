# BUS5001 Assessment 3 – Experiment Evidence (Q3 and Q4)

**Student ID:** 22623173
**Unit:** BUS5001 Cloud Platforms and Analytics, La Trobe University

This repository holds the experiment logs and evidence for Q3 and Q4 of Assessment 3.
All test messages and organisations are fictional or publicly available. No real personal data is used.

## Q3 – Using an LLM to triage ESG messages

Scenario: Acceler Commercial Properties (a fictional organisation created for this assessment).

| File | What it contains |
|---|---|
| `Q3/22623173_BUS5001_A3_Q3_triage.ipynb` | Google Colab notebook with all code and saved outputs: starter prompt, improved prompt, validation and fallback, consistency test, keyword-rule baseline, Hugging Face zero-shot baseline, and comparison tables |
| `Q3/results/experiment_log.md` | Model version, settings, run date, accuracy summary and consistency results |
| `Q3/results/starter_prompt_outputs.json` | Outputs from the starter prompt given in the brief |
| `Q3/results/improved_prompt_outputs.json` | Outputs from the improved prompt for all six test messages |
| `Q3/results/consistency_test.json` | Results from running each message three more times |
| `Q3/results/comparison_table.csv` | Gemini, keyword rules and zero-shot results for each message |
| `Q3/results/accuracy_summary.csv` | Accuracy of each method for category and urgency |

**Setup:** Google Gemini (gemini-3.1-flash-lite) via the Google AI Studio API, temperature 0 and JSON mode for the improved prompt. Baseline zero-shot model: MoritzLaurer/deberta-v3-base-zeroshot-v2.0.
The API key is stored in Colab Secrets and is not included in this repository.

## Q4 – Evaluating NotebookLM for academic use

| File | What it contains |
|---|---|
| `Q4/22623173_BUS5001_A3_Q4_log.docx` | Scenario, sources, five test prompts, NotebookLM's unedited outputs, checks performed and evaluation of each test |

Sources tested: AASB S2 Climate-related Disclosures, ASIC Regulatory Guide 280 and the Dexus 2026 Annual Report.
