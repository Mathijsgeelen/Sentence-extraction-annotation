# Sentence-extraction-annotation
This repository provides the code needed to train a sentence boundary detection model, as well as an artefact capable of extracting sentences from an image and highlight token-level classification results (NER in the artefact)

The sentence boundary detection module provides a script capable of fine-tuning BERT, RoBERTa, or any other model having a similar architecture on the legal sentence boundary detection dataset by Savelka et al. (2017). 

Savelka, Jaromir, Vern R. Walker, Matthias Grabmair and Kevin D. Ashley. "Sentence Boundary Detection in Adjudicatory Decisions in the United States." TAL 58.2 (2017).

The Sentence extraction and Annotation artefact uses document layout analysis to extract text blocks from an image, OCR to extract text from an image, fine-tuned DeBERTa (using the sentence boundary detection script) to identify sentence boundaries, and a set of hand-crafted to extract entire sentences, as well as the coordinates of the sentence boundaries. It further provides the ability to highlight words in a copy of a PDF without affecting the original layout. Currently it highlights NER results. To use the artefact open it in Google Colab and download one of the test files from the test files folder. Also download the DeBERTa model and upload both manually in Google Colab or preferably add them to your Google Drive. Both are required for the script to work.


!!!
When using the extract-annotate module, download the DeBERTa_legal_SBD model and upload it to your google drive or in the google colab environment.
When training a custom SBD model, download the datasets by Savelka et al. (2017) and upload these to your google dive or in the google colab environment.
