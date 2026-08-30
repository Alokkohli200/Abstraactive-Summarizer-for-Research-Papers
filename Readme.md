# Abstractive Summarizer for Scientific Papers

A hybrid NLP pipeline that extracts and summarizes lengthy academic papers. It uses a dynamic TF-IDF extraction strategy (400-400-200 token budget) to isolate key sentences from a document's Introduction, Methodology, and Conclusion, and feeds them into a fine-tuned DistilBART model for cohesive abstract generation.

## Hosted Model
The fine-tuned model weights are hosted on Hugging Face: [alokkohli200/Alok_ATML_project](https://huggingface.co/alokkohli200/Alok_ATML_project)

## Repository Contents
* `training_pipeline.ipynb`: The workflow for loading the `ccdv/arxiv-summarization` dataset, applying TF-IDF truncation, and training the DistilBART model.
* `inference.ipynb`: Script to read a local `.docx` research paper, apply the extraction logic, and generate the final abstractive summary.
* `requirements.txt`: Project dependencies.

## Usage
1. Clone the repository and install dependencies:
   `pip install -r requirements.txt`
2. Open `inference.ipynb` and replace `FILE_PATH` with your `.docx` file.
3. Run the cells to generate the summary.