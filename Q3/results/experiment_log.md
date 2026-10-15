# Q3 Experiment Log

- Date run: 2026-10-03 03:28
- LLM: Google Gemini via the Google AI Studio API
- Model requested: gemini-3.1-flash-lite
- Model version that answered: gemini-3.1-flash-lite
- Note: gemini-flash-latest returned 503 'high demand' errors, so Flash-Lite was used
- Improved prompt: temperature 0.0, JSON response mode on
- Starter prompt: temperature 1.0 (Gemini's normal setting)
- Consistency runs per message: 3
- Zero-shot baseline model: MoritzLaurer/deberta-v3-base-zeroshot-v2.0
- Rule-based baseline: keyword matching (Step 9)
- Test data: 6 fictional messages for Acceler Commercial Properties (fictional organisation)
- Data note: no real personal data used; free-tier API inputs may be used by the provider to improve its products

## Accuracy summary
                                   Method Category correct Urgency correct Can flag for human review Handles two issues
                 Gemini (improved prompt)              3/6             6/6                       Yes                Yes
                            Keyword rules              4/6             4/6                        No                 No
Zero-shot (deberta-v3-base-zeroshot-v2.0)              3/6             2/6                        No                 No

## Consistency (category, urgency, review flag)
- M1_clear_leak: STABLE [('Facilities', 'HIGH', 'N'), ('Facilities', 'HIGH', 'N'), ('Facilities', 'HIGH', 'N')]
- M2_angry_recycling: STABLE [('Waste & Recycling', 'LOW', 'N'), ('Waste & Recycling', 'LOW', 'N'), ('Waste & Recycling', 'LOW', 'N')]
- M3_energy: STABLE [('Energy', 'MEDIUM', 'N'), ('Energy', 'MEDIUM', 'N'), ('Energy', 'MEDIUM', 'N')]
- M4_two_issues: STABLE [('Health & Safety', 'HIGH', 'Y'), ('Health & Safety', 'HIGH', 'Y'), ('Health & Safety', 'HIGH', 'Y')]
- M5_injection: STABLE [('Health & Safety', 'CRITICAL', 'Y'), ('Health & Safety', 'CRITICAL', 'Y'), ('Health & Safety', 'CRITICAL', 'Y')]
- M6_sensitive: STABLE [('Waste & Recycling', 'HIGH', 'Y'), ('Waste & Recycling', 'HIGH', 'Y'), ('Waste & Recycling', 'HIGH', 'Y')]