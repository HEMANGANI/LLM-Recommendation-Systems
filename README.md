# LLM-Recommendation-Systems

# Fine-Tuning LLMs for Text-Based Recommendations

This project explores the potential of fine-tuning large language models (LLMs) specifically for text-based recommendations, aiming to improve accuracy and user satisfaction. It introduces a novel prompt mechanism that transforms relationship information into natural language text, enabling the LLM to interpret user interactions and make more informed recommendations.

## Project Overview

The project focuses on demonstrating the efficiency of fine-tuning LLMs for recommendation tasks using a diverse and expansive dataset. The implementation includes the following phases:

1. **Data Extraction and Preprocessing**:
    - Extracted subsets of Amazon review data and converted them into DataFrames.
    - Removed unnecessary columns.
    - Filtered out users with insufficient purchase histories.
    - Transformed the remaining data into prompts, forming the input for the LLM.

2. **Prompt Engineering**:
    - Explored various prompting techniques.
    - Settled on a three-part structure for each prompt: instruction, input details, and ground truth output.
    - This structure provides the model with a clear task, relevant information, and the desired output format.

3. **Model Implementation**:
    - Utilized the Unsloth AI and HuggingFace libraries for pre-trained models and customization tools.
    - Considered QLoRA, a technique for improving model performance.
    - Created consolidated `SFTTrainer` and `TrainingArguments` objects to centralize hyperparameter adjustments during training.
