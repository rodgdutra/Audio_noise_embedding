# Audio Embedding Analysis: Exploring Whisper Encoder Capabilities to Visualize and Categorize Noise

This project explores the capabilities of the Whisper encoder for audio embedding analysis, specifically focusing on visualizing and categorizing noise. The notebook demonstrates how to use the Whisper encoder to generate embeddings, reduce their dimensionality using UMAP, and perform clustering and classification tasks.

## Notebook Outline

1. **Whisper Encoder**  
   - The Whisper encoder is used to generate embeddings from audio samples. These embeddings capture the essential features of the audio, including noise and voice.

2. **UMAP for Dimensionality Reduction**  
   - UMAP (Uniform Manifold Approximation and Projection) is applied to reduce the high-dimensional Whisper embeddings to 2 dimensions for visualization.

3. **Plot and Cluster Using K-Means**  
   - The reduced embeddings are plotted in a 2D space, and K-Means clustering is used to group the samples into clusters (e.g., noise vs. voice).

4. **SVM Classification**  
   - A Support Vector Machine (SVM) is trained on the UMAP-reduced features using a training set. The model is then tested on a separate test set to classify audio samples as either "pure noise" or "pure voice."

5. **Results**  
   - Achieved **95% accuracy** on a balanced dataset of 600 samples, with 120 samples reserved for testing and the rest used for training. The dataset contains only two classes: pure noise and pure voice.

---

## TODO

- **Distinguish Different Human Voices**  
  - Extend the analysis to differentiate between different human voices.

- **Distinguish Different Phrases from the Same Human**  
  - Explore the ability to distinguish between different phrases spoken by the same individual.

- **Detect Presence or Absence of Noise**  
  - Develop a method to detect whether noise is present in an audio sample.

- **LoRA Whisper Encoder for Noise Handling**  
  - Investigate the use of LoRA (Low-Rank Adaptation) to fine-tune the Whisper encoder for better noise handling.

---

## Explore

- **Different Embeddings**  
  - Experiment with other embedding techniques (e.g., Wav2Vec, HuBERT) to compare their performance with Whisper.

- **Statistical Features**  
  - Incorporate statistical features (e.g., mean, variance, spectral features) to enhance the analysis.

---

## Usage

To run the notebook:
1. Clone this repository.
2. Install the required dependencies (e.g., Whisper, UMAP, scikit-learn).
3. Open the Jupyter notebook and execute the cells.

```bash
git clone https://github.com/rodgdutra/Audio_noise_embedding.git
cd Audio_noise_embedding
jupyter notebook audio_noise_embedding_whisper.ipynb
```

---

## License

This project is licensed under the APACHE 2.0 License. See the [LICENSE](LICENSE) file for details.
