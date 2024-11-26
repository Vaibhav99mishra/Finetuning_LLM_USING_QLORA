# Finetuning_LLM_USING_QLORA

Step 1: Creating a Custom Dataset
For the needs of this tutorial, I created a custom dataset containing questions and answers regarding the recently announced Apple Vision Pro product. I wrote the questions and answers using the information published on wikipedia. The dataset is in JSON format .

Step 2: Loading the Pretrained Model
Next, we'll load the pretrained LLM model and tokenizer. We'll also configure the quantization settings using BitsAndBytesConfig.

Step 3: Preparing the Training Dataset
We'll now prepare the training dataset by loading it from a JSON file using the load_dataset function and applying necessary preprocessing (tokenization, padding, etc.).

Step 4: Launching the Training
With the model, tokenizer, and training dataset ready, we can now launch the fine-tuning process. We'll define the training configuration using transformers.TrainingArguments and create a Trainer instance to handle the training. Note that for this experiment, I used the falcon-7b model, but you can use any other LLM you want.

Step 5: Performing Inference
Once the training is complete, we can perform inference on the trained model. We ask the model to described the vision pro of apple in 3 sentences.

The given answer should be this one:
The Vision Pro is a high-end VR headset developed by Apple. It offers a 120-degree field of view, 4K resolution, and a 120Hz refresh rate. The device is powered by a custom-built processor, allowing for a smooth and immersive experience.

The Vision Pro is a high-end VR headset developed by Apple. It offers a 120-degree field of view, 4K resolution, and a 120Hz refresh rate. The device is powered by a custom-built processor, allowing for a smooth and immersive experience.
Please note that the final model is not available in this repository, as it is way too large.
