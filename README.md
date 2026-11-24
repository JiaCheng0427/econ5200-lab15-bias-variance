## Bias, Variance and an Unbiased Cross-Validation Score

### Objective
I wanted to understand how model selection affects cross-validation scores and how bias, variance and noise affect prediction error.

### Methodology
- I tested polynomial degrees from 1 to 12 using 80 simulated data points.
- I selected degree 5, which had the lowest CV error of 0.1853.
- I tested the selected model on 20,000 new points and got a true error of 0.2330.
- I used nested cross-validation and obtained an error of 0.1910.
- I separated the expected error into bias squared, variance and noise.
- I wrote a k-fold cross-validation function and got an error of 0.1921 using 10 folds.

### Key Findings
I found that choosing the model with the lowest CV error can make the reported error too optimistic. Nested cross-validation helps reduce this problem. I also learned that more complex models do not always perform better, and the noise of 0.2025 cannot be removed by improving the model.
