# IMDB Movie Reviews Sentiment Analysis

## Overview
A sentiment analysis project that classifies IMDB movie reviews as positive or negative using a Simple Recurrent Neural Network (RNN) model. The project includes data preprocessing, model training, and a Streamlit-based user interface for interactive predictions.

## Project Structure
- `app.py`: Streamlit application for user input and sentiment prediction
- `embedding.ipynb`: Jupyter notebook demonstrating word embedding techniques using Keras
- `prediction.ipynb`: Notebook for loading pre-trained model and performing sentiment analysis
- `simplernn.ipynb`: Notebook containing model training code and IMDB dataset processing

## Requirements
The following Python libraries are required:
```bash
pip install tensorflow numpy streamlit keras
```

## Installation and Usage

### Training the Model
1. Open and run `simplernn.ipynb`
2. The notebook will:
   - Load and preprocess the IMDB dataset
   - Train the RNN model with embeddings
   - Save the trained model as `simple_rnn_imdb.h5`

### Running the Web Interface
```bash
streamlit run app.py
```

### Making Predictions
Use `prediction.ipynb` to:
- Load the pre-trained model
- Process new review texts
- Generate sentiment predictions

## Technical Details

### Model Architecture
- Input Layer: Word indices
- Embedding Layer: Dense vector representation
- Simple RNN Layer: 128 units with ReLU activation
- Dense Layer: Single unit with sigmoid activation

### Data Preprocessing
- Word-to-index conversion using IMDB vocabulary
- Sequence padding (length: 500)

## Performance
- Current validation accuracy: ~50%
- Model performance requires improvement
- Limitations due to simple architecture

## Future Improvements
1. Model Architecture
   - Implement LSTM/GRU layers
   - Experiment with Transformer models
   - Increase network complexity

2. Training Optimization
   - Hyperparameter tuning
   - Data augmentation strategies
   - Transfer learning implementation

3. Deployment
   - Flask/FastAPI service implementation
   - Cloud deployment options
   - API documentation

