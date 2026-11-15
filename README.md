# DNN Assignment 2

**Student ID:** 2026AK05029 
**Course:** Deep Neural Networks (DNN)  
**Assignment:** Programming Assignment 2 – RNN, LSTM, GRU and Transformer

---

## Experiment Configuration

Following the instructor clarification email, references to the variants table were ignored.

### Problem 1 Configuration

- Hidden Size (h): 64
- Model Seeds: 42, 123, 999
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 128

Adding Problem dataset seeds:

- Training Seed: 0
- Validation Seed: 1
- Test Seed: 2

Sequence lengths used:

- T = 50
- T = 100
- T = 200
- T = 400

Hidden-size sweep:

- 16
- 32
- 64
- 128

Task 5(c) ablation:

- LSTM forget-gate bias = 0 versus 1

---

### Problem 2 Configuration

- Model Width (d): 128
- Number of Attention Heads: 4
- Number of Transformer Layers: 4
- Context Length: 128
- Model Seeds: 42, 123, 999

Positional Encoding Experiments:

- None
- Sinusoidal
- Learned

Head Ablation:

- 1 Head
- 4 Heads
- 8 Heads

Context-Length Profiling:

- 64
- 128
- 256
- 512

---

## Environment

The notebooks were developed and tested using:

- Python 3.10+
- PyTorch 2.x
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn

Exact package versions are listed in `requirements.txt`.

A Google Colab T4 GPU was used for the main experiments.

---

## Project Structure

```
<StudentID>_DNN_Assignment/
│
├── README.md
├── requirements.txt
├── report.pdf
├── results.csv
│
├── problem1/
│   ├── problem1.ipynb
│   └── figures/
│
└── problem2/
    ├── problem2.ipynb
    ├── generated_samples.txt
    └── figures/
```

---

## Execution Instructions

### Problem 1

Open:

```
problem1/problem1.ipynb
```

Run all cells from top to bottom.

The notebook will:

- Download and preprocess the UCI HAR dataset
- Verify custom RNN, LSTM and GRU implementations
- Run HAR classification experiments
- Run Adding Problem experiments
- Generate required plots and tables
- Update `results.csv`

### Problem 2

Open:

```
problem2/problem2.ipynb
```

Run all cells from top to bottom.

The notebook will:

- Verify custom Transformer components
- Train HAR Transformer models
- Train the Tiny Shakespeare language model
- Generate attention heatmaps
- Run all required ablation studies
- Generate `generated_samples.txt`
- Update `results.csv`

---

## Expected Outputs

### Problem 1

Generated under:

```
problem1/figures/
```

including:

- Class balance plot
- HAR confusion matrix
- Adding-problem learning curves
- MSE versus sequence length
- Gradient norm plots
- Hidden-size sweep plots
- Ablation plots

### Problem 2

Generated under:

```
problem2/figures/
```

including:

- Attention heatmaps
- HAR Transformer plots
- Language-model learning curves
- Head-count ablation plots
- Causal-mask ablation plots
- Context-length profiling plots

Additional generated file:

```
problem2/generated_samples.txt
```

containing three temperature-controlled samples:

- Temperature = 0.2
- Temperature = 0.8
- Temperature = 1.5

---

## Runtime

Approximate execution times on a Google Colab T4 GPU:

| Component | Approximate Time |
|------------|------------|
| Problem 1 | XX minutes |
| Problem 2 | XX minutes |
| Total | XX minutes |

(Update after the final run.)

---

## Notes

All required models, experiments, figures, tables and result files were generated from the submitted notebooks using the fixed random seeds listed above.

No pretrained models or external datasets were used.