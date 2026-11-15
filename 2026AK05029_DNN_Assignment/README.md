# DNN Assignment 2

Working folder for the individual RNN, LSTM, GRU and Transformer assignment. Rename this folder to `<StudentID>_DNN_Assignment` before creating the final ZIP.

## Assignment choices

The professor's clarification says to ignore the variants table and FAQ entry. Choose one hidden size `h` shared by the RNN, LSTM and GRU, one Transformer width `d` divisible by the number of heads, and three experiment seeds. Record those choices on the report title page and here before running experiments. Recompute all parameter counts using the chosen values.

Chosen Problem 1 values: `h=48`; model seeds `13`, `29` and `47`.

Chosen Problem 2 value: Transformer width `d=96`, divisible by the 1-, 4- and 8-head settings. Use model seeds `13`, `29` and `47` for the 3-seed runs and keep all choices fixed.

The adding-data generator's required data seeds remain 0 (train), 1 (validation), and 2 (test); these are separate from model experiment seeds.

## Environment and run order

Use Python 3.10+ and PyTorch 2.x, with NumPy, pandas, Matplotlib and scikit-learn. A Colab T4 is recommended for the full Transformer experiments. Run `problem1/problem1.ipynb` and `problem2/problem2.ipynb` from top to bottom with saved outputs. Record exact package versions used for the final results in `requirements.txt`.

The Problem 1 notebook downloads UCI HAR from the assignment's official URL and extracts it to the sibling `../har_data` cache. The dataset stays outside the submission folder and ZIP. Tiny Shakespeare can be downloaded by the Problem 2 notebook from its specified public source.

## Required output checklist

- `problem1/problem1.ipynb`: HAR and adding-problem results, custom-cell verification, gradient/size/ablation studies and required figures under `problem1/figures/`.
- `problem2/problem2.ipynb`: attention and encoder tests, HAR classifier, language model, ablations and required figures under `problem2/figures/`.
- `results.csv`: one row per run using the exact header already provided.
- `problem2/generated_samples.txt`: three generated samples, each exactly 500 characters, labelled by temperature 0.2, 0.8 and 1.5.
- `report.pdf`: at most 6 A4 pages, 11 pt or larger, margins at least 2 cm. Number and caption every figure/table and refer to each in the text. Include the AI-use statement and references after the six-page report body.

The specification estimates 25-30 hours. Do not invent results: populate tables, plots and report claims only from saved experiment outputs. Keep the final ZIP under 25 MB, exclude datasets/checkpoints/environments, verify it opens, and retain the portal confirmation.

## AI-use and academic integrity

The assignment permits AI for explaining concepts, debugging errors and tidying plots, but explicitly prohibits AI-written implementations of the from-scratch RNN/LSTM/GRU cells and Problem 2 attention, multi-head attention and encoder block. Those cells are intentionally left for you to write. Declare all AI use truthfully in the report; do not submit generated explanations or measurements as personal experimental findings.

## Deadline note

The DOCX says November 14, 2026 at 11:59 PM but labels it Friday; the professor's email clarifies November 14 is Saturday and gives the due date without a time. Confirm the portal's exact deadline. The document lists a late window through November 15 at 11:59 PM with a 20% deduction.
