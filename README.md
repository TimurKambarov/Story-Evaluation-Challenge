# Story Evaluation Challenge

An automated story evaluation system that leverages multiple Large Language Models to assess narrative quality across six literary dimensions.

## Overview

This project uses three state-of-the-art LLMs (LLaMA 3.1 70b, Qwen 3 30b, and DeepSeek R1 70b) to provide objective literary analysis of stories. The system evaluates narratives across six key metrics:

- **Relevance** - Thematic significance and purpose
- **Coherence** - Logical flow and consistency
- **Empathy** - Emotional connection and character depth
- **Surprise** - Plot twists and unexpected elements
- **Engagement** - Reader interest and pacing
- **Complexity** - Narrative sophistication and depth

The evaluation compares two prompting approaches (few-shot with literary examples vs. zero-shot) to analyze how different models assess story quality.

## Features

- Multi-model evaluation for cross-validation
- Interactive interface for evaluating custom stories
- Visual comparison of model assessments
- Side-by-side analysis of high vs. low quality narratives
- Comprehensive scoring system (0-10 scale per metric)

## Setup

1. Clone this repository
2. Install required packages:
```bash
   pip install jupyter pandas matplotlib ollama
```
3. Copy `config.example.py` to `config.py`
4. Edit `config.py` and add your Ollama server URL:
```python
   SERVER_URL = "your-ollama-server-url-here"
```
5. Ensure you have access to the required models on your Ollama server

## Usage

### Running Existing Evaluations

1. Open the notebook in Jupyter
2. Connect to your Ollama server (first cell)
3. Run all cells sequentially (Cell → Run All)
4. Wait for model responses (approximately 10-15 minutes)
5. Review visualizations and analysis

### Evaluating Your Own Stories

1. Navigate to the last cell (Interactive Evaluation Interface)
2. Run the cell
3. Select a model (1: LLaMA, 2: Qwen, 3: DeepSeek)
4. Choose prompt type (1: Few-shot, 2: Zero-shot)
5. Paste your story
6. Review the detailed evaluation results

## Results Interpretation

The notebook generates two main visualizations:

1. **Model Comparison** - Shows how each model scores stories across all six metrics, comparing few-shot vs zero-shot approaches
2. **Good vs Bad Story** - Demonstrates the system's ability to discriminate between high and low quality narratives

### Score Guide
- 9-10: Exceptional quality
- 7-8: Strong, professional level
- 5-6: Competent but unremarkable
- 3-4: Significant weaknesses
- 1-2: Poor quality

## Requirements

- Python 3.8+
- Jupyter Notebook
- Ollama server with LLaMA 3.1 70b, Qwen 3 30b, and DeepSeek R1 70b models
- Dependencies: pandas, matplotlib, ollama

## License

[Choose appropriate license]

## Acknowledgments

Test stories sourced from classic literature and contemporary examples. Full references available in the documentation.