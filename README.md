# LLM-Recommendation-Systems

# Fine-Tuning LLMs for Text-Based Recommendations

This project explores the potential of fine-tuning large language models (LLMs) specifically for text-based recommendations, aiming to improve accuracy and user satisfaction. It introduces a novel prompt mechanism that transforms relationship information into natural language text, enabling the LLM to interpret user interactions and make more informed recommendations.

## Project Overview

Key Points:

1. Utilized the 2018 Amazon Review Dataset to develop a personalized product recommendation system.
2. Implemented and compared the performance of two large language models: Mistral-7B and TinyLlama.
3. Applied advanced techniques like LoRA (Low-Rank Adaptation) and QLoRA (Quantized LoRA) for efficient model fine-tuning.
4. Developed a novel prompting strategy to transform user interaction history into natural language inputs for the models.
5. Achieved over 98% accuracy in predicting users' next product purchases using the fine-tuned TinyLlama model.
6. Demonstrated that smaller, specialized models can outperform larger models for specific tasks when properly fine-tuned.
7. Conducted error analysis to identify patterns in incorrect predictions and potential areas for improvement.
8. Explored the balance between model size, computational efficiency, and prediction accuracy in recommendation systems.

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
