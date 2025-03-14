**FastAI and the First Two Lessons**
I started the FastAI course to get an introduction to ML and must admit I was initially surprised, then fascinated by its hands-on approach. From the first chapter, you begin interacting with models directly. The course creators emphasize this intentional learning style, and its effectiveness is immediately apparent.

FastAI is an organization focused on democratizing ML, enabling anyone to leverage its power without requiring expertise in calculus or advanced ML theory. We began with a computer vision use case using the FastAI library, which allows training models with custom data. If you lack data, you can download and auto-label images from the internet.

Before training, you define a dataloader to specify input data type, transformations, labels, and the training-validation split. Once data is stored in a path-accessible location, the loader is created, and training begins. Here, we learn about epochs—complete passes through the dataset during fine-tuning. The number of epochs is specified upfront, as we use pretrained models (ideal for recognizing basic patterns). Without a pretrained model, you'd "fit" a model from scratch.

After each epoch, metrics like `train_loss`, `val_loss`, and error rate are displayed (all configurable). Training loss quantifies misclassifications on training data, validation loss does the same for validation data, and error rate measures total incorrect predictions. Avoid excessive epochs: overfitting occurs when the model memorizes training data instead of generalizing patterns for unseen data—like memorizing math answers rather than learning problem-solving.

A counterintuitive best practice: don't clean your dataset before fine-tuning. Instead, run a few epochs, generate a confusion matrix to pinpoint high-error areas (e.g., mislabeled or irrelevant data), then clean the dataset and retrain.

Post-training, a test dataset evaluates performance. Once finalized, the model is exported via `learn.export()` as a `.pkl` file containing both architecture (the mathematical function template) and trained weights.

With the exported model, you can build a UI wrapper (using FastAI's tools) to load it and run inference via the `predict` method. 

For example, I created a [Hugging Face Space](https://huggingface.co/spaces/radubutucelea23/Warning-lamp-classifier) using Gradio to classify dashboard warning lamps—though performance is currently poor. Next steps might involve switching to a state-of-the-art pretrained model or further fine-tuning, as explored in later chapters.
