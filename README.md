# Intel Virtual Assistant Chatbot

## :gear: Problem Statement 
Running GenAI on Intel AI Laptops and Simple LLM Inference on CPU and fine-tuning of LLM Models using Intel® OpenVINO™ 

## :detective: Our Solution:
-> Fine-tuned Llama2-7b model on Intel Products and Services FAQ custom Dataset.

-> Comverted to OpenVINO IR Format for optimized inferencing, being 56% faster than the original model.


## :tv: Demo ([Youtube](https://youtu.be/1fdKZiXexSU))

<a href="https://youtu.be/1fdKZiXexSU" target="_blank">
  <img src="https://github.com/user-attachments/assets/4bfd73b4-0e4b-4288-b8de-e7bfafc73fa7" width="700"/>
</a>

## :running_man: Workflow 
![image](https://github.com/user-attachments/assets/2f5ebda2-d4be-470a-b2e1-1d2e0a8a0518)



## :open_file_folder: Dataset
The dataset was prepared by scraping data regarding Intel Product and Services from the Intel FAQ and help websites. The capability of this model is limited to the dataset used, which includes the below Intel Products

#### 📊 Intel Products

- 🚀 Intel Gaudi
- 🔧 POP Intel
- ⚡ Intel Optane
- 🛠️ IPP Intel
- 🔗 Intel MPI Library
- 🧠 Intel OpenVINO

#### ❓ FAQ Categories

- 🛡️ Product Support FAQ
- 📦 Product Installation FAQ
- 🌐 General Intel Information

## 🏃‍♂️ How to perform inference with the fine-tuned Intel OpenVINO Model?

1. Install packages required for using [Optimum Intel](https://huggingface.co/docs/optimum/intel/index) integration with the OpenVINO backend:

```
pip install optimum[openvino]
```

2. Import and initialize the model from HuggingFace:

```
from transformers import AutoTokenizer
from optimum.intel.openvino import OVModelForCausalLM

model_name = "OjasPatil/intel-llama2-7b-ov"
tokenizer = AutoTokenizer.from_pretrained(model_name)
base_model = OVModelForCausalLM.from_pretrained(model_name)
```

3. Perform Inference with the OpenVINO Optimized Fine-tuned Intel Virutal Assistant:

```
message = "What is Intel OpenVINO?"
prompt = f"[INST] {message} [/INST]"
inputs = tokenizer(prompt, return_tensors="pt")
outputs = base_model.generate(**inputs, max_new_tokens=50)
response = tokenizer.decode(outputs[0], skip_special_tokens=True).replace(prompt+" ", "")
print(response)
```

## 🌠 Results
The OpenVINO IR Format Model performs **56% faster** than the original model.

![Performance Comparison](https://github.com/user-attachments/assets/a672e14d-f935-4b4c-8845-48bf832a747f)

<p align="center">
  <em>Figure: Performance comparison between the OpenVINO IR Format Model and the original model.</em>
</p>

The performance of the model is also evaluated using ROUGE scores:

-> ROUGE-1: 35.23

-> ROUGE-2: 18.97

-> ROUGE-L: 28.82

## Demo Video Link: [Project Demo](https://youtu.be/1fdKZiXexSU)


## :handshake: Team Aurora
- **Harinee J**
- **Mhanjhusriee Baskar**
- **Amit Das**
- **Ojas Patil**
