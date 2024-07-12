## Intel-QA-Chatbot

### Overview

Intel-QA-Chatbot is a project developed by Team Aurora that focuses on creating and fine-tuning Large Language Models (LLMs) for efficient inference using Intel OpenVINO™ on Intel AI Laptops. The project demonstrates the potential of leveraging Intel hardware and the OpenVINO™ toolkit for optimizing model deployment and inference, specifically for question-answering tasks.

### Problem Statement

The main objective of this project is to enable seamless execution of Generative AI (GenAI) models on Intel AI Laptops, with a focus on:
- Efficiently running LLM inference on CPUs.
- Fine-tuning LLM models using Intel® OpenVINO™.

### Team Aurora

- **Harinee J**
- **Mhanjhusriee Baskar**
- **Amit**
- **Ojas**

### Project Components

1. **Model Loading and Inference**:
   - Utilizing the OVModelForCausalLM and AutoTokenizer from the Hugging Face Transformers library to load and run inference with a pre-trained model.
   - Implementing a text generation pipeline to generate responses based on user prompts.

2. **Model Fine-Tuning**:
   - Fine-tuning a base model from the Hugging Face hub using the PEFT (Parameter-Efficient Fine-Tuning) approach with LoRA (Low-Rank Adaptation).
   - Configuring the fine-tuning parameters, including learning rate, batch size, gradient accumulation steps, and more, to optimize the training process.
   - Splitting the dataset into training and evaluation sets for model training and validation.

3. **Model Evaluation**:
   - Evaluating the fine-tuned model using the ROUGE metric to measure the quality of generated responses.
   - Loading and processing datasets, generating responses for evaluation, and computing ROUGE scores to assess model performance.

4. **Deployment and Integration**:
   - Saving the fine-tuned model and tokenizer.
   - Pushing the fine-tuned model to the Hugging Face hub for easy access and deployment.

### Installation and Setup

To get started with the Intel-QA-Chatbot project, you need to set up the required environment and dependencies. This includes installing necessary libraries such as `accelerate`, `peft`, `bitsandbytes`, `transformers`, and `trl`.

### Contribution

We welcome contributions to enhance and expand the functionality of this project. If you are interested in contributing, please follow the standard GitHub workflow:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make the necessary changes and commit them.
4. Push your changes to your forked repository.
5. Submit a pull request to the main repository.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

### Contact

For any inquiries or further information, please contact Team Aurora:
- **Harinee J**
- **Mhanjhusriee Baskar**
- **Amit**
- **Ojas**

This project highlights the capabilities of Intel AI Laptops and the OpenVINO™ toolkit in optimizing LLM inference and fine-tuning, providing a practical solution for running advanced AI models on Intel hardware.
