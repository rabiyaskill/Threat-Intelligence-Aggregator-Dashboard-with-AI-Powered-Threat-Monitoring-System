# Threat Intelligence Aggregator
Hackathon project (Sep 13, 2025)
## Overview
Aggregates cyber threat data from OTX, RSS (Krebs), and X posts. Uses spaCy for NLP, ARIMA for predictions, and Plotly for visualization.
## Setup
1. Install: `pip install requests spacy plotly pandas statsmodels`
2. Install spaCy model: `python -m spacy download en_core_web_sm`
3. Set OTX_API_KEY in code or env.
4. Run: `python threat_aggregator.py`
## Outputs
- Console: Threat summaries, entities, predictions
- dashboard.html: Interactive charts + table
## Team
[Your Names] | GitHub: [your-repo]
