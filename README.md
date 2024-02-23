# LLM_Learn

Wha is Transformers model? 
Transformer models have been trained by large amounts of raw text in a self-supervised fashion as _language models_.self-supervised  model develops a statistical understanding of the language it has been trained on

but it’s not very useful for specific practical tasks. Because of this, the general pretrained model then goes through a process called _transfer learning_. During this process, the model is fine-tuned in a supervised way — that is, using human-annotated labels — on a given task.

-------


How many type of transformer model do we have?
- GPT-like (also called _auto-regressive_ Transformer models)
- BERT-like (also called _auto-encoding_ Transformer models)
- BART/T5-like (also called _sequence-to-sequence_ Transformer models)
----
How can better performance be achieved in language models except DistilBERT?

A: The general strategy to achieve better performance is by increasing the models' sizes and the amount of data they are pretrained on.

----
Q: What challenges arise when training a large model?

A: Unfortunately, training a model, especially a large one, poses challenges due to the substantial amount of data required. This becomes costly in terms of time and compute resources, and it also translates to environmental impact, as depicted in the following graph.

----
Q: What is fine-tuning in the context of training a model?

A: Fine-tuning, on the other hand, refers to the training done after a model has been pretrained.

----
Why fine-tune instead of training from scratch?

A: Fine-tuning is preferred because the pretrained model has prior knowledge, requires less data, and reduces time and resource demands compared to training from scratch.

----
**Q: What is the role of the Encoder in the model?**

A: The Encoder is responsible for receiving an input and building a representation of it. It captures the essential features or characteristics of the input, optimizing the model for understanding the provided information.

**Q: Can you explain what "representation" and "features" mean in this context?**

A: In this context, "representation" refers to a modeled form that encapsulates the essential features of the input data. "Features" are the distinct characteristics or aspects of the input that the Encoder captures to form this representation.

**Q: What is the purpose of the Decoder in the model?**

A: The Decoder uses the representation generated by the Encoder (features) along with other inputs to generate a target sequence. It is optimized for the task of generating desired outputs based on the understanding acquired from the input.


-----

**Q: What is the role of attention layers in a model?**

A: Attention layers instruct the model to focus on specific words within a given sentence while potentially downplaying the importance of others. They enable the model to allocate its attention resources selectively, allowing for more nuanced and contextually relevant processing of input data.

----
**Q: How would you define "Checkpoints" in relation to these models?**

A: "Checkpoints" are specific weights or parameters associated with a trained instance of a model. They represent the learned knowledge of the model. Loading checkpoints into a specific architecture means applying the learned knowledge to that model structure.

-----

1. **Q: What are encoder-decoder models, and what is another name for them?**

    Encoder-decoder models, also known as sequence-to-sequence models, utilize both parts of the Transformer architecture.

1. **Q: How do the attention layers of the encoder and decoder differ in their access to words in a sentence in a Transformer-based model?

    - The attention layers of the encoder can access all the words in the initial sentence at each stage.
- In contrast, the attention layers of the decoder are limited to accessing words positioned before a given word in the input.


3. **Q: In the context of encoder-decoder models, what is the role of attention layers during each stage of processing?

During each stage of processing, attention layers play a crucial role in capturing and focusing on specific parts of the input data.
    
4. **Q: Can you explain the specific limitation of the attention layers in the decoder regarding their access to words in an input sentence?

The attention layers in the decoder can only access words that come before a given word in the input sentence, introducing a sequential constraint to the decoding process.
