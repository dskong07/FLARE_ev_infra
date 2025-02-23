This repo contains work done by Daniel Kong, Ethan Deng, Jason Gu, Irving Zhao on the DSC 180B UCSD capstone project.\
Requirements for reproducibility are included in an environment file, and additionally include a Hugging Face account and Segments.ai account (for login tokens via api).

- segtest.py includes the code for trivial segmentation on a given image in grayscale, developed as preliminary viability testing for semantic segmentation.
- semseg folder includes notebook and code, as well as partial saved models (full model size too large to upload), for a semantic segmentation model built on the base of Nvidia's mit-b0 lightweight transformer model, and trained on the hugging-face semantic-sidewalk dataset.
- the notebook file included in semseg includes all requirements and steps for external frameworks to function.
- environment.yml file is included for the purposes of reproducibility and testing
- custom_segformer_training.ipynb contains code for development of our custom dataset semantic segmentation model.
- variations for publicly available repos for our dataset, including annotations and masks, can be found at
  - https://app.segments.ai/dskong07/chargers/samples (including all unlabeled/annotated images and filetypes)
  - https://app.segments.ai/dskong07/chargers-full (only jpeg, annotated and labeled images; used in the training of our most up-to-date model)
- publicly available model hosted on Hugging Face, found at https://huggingface.co/dskong07/segformer-b0-finetuned-segments-chargers-2-15

example of preliminary training output:\
![image](https://github.com/user-attachments/assets/a541db33-6169-40e1-9044-4c973a30012d)
