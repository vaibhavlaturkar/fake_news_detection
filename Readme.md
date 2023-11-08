# Fake News Detection using Neural Networks

This repository contains the implementation of a binary classification model that aims to detect fake news. The model is built using a neural network and trained on a dataset that has been preprocessed and transformed, incorporating advanced NLP techniques and embedding layers for categorical and text features.

## Dataset

The dataset originally pertains to a multi-class classification problem but has been converted into a binary classification problem, where the target is to identify news as either `True` or `Fake`. The dataset includes various features such as `title`, `source_title`, `content_text`, and several categorical features like `verifiedby`, `country`, and `lang`.

## Preprocessing

The data has been preprocessed to handle missing values, duplicates, and irrelevant data points. Categorical features have been transformed using embedding layers to capture more nuanced information than traditional encoding methods. Text features have been handled using transfer learning embeddings from pre-trained models to leverage semantic information contained in the news content.

## Neural Network Model

The neural network model is constructed using TensorFlow and Keras libraries. It is designed with separate input layers for categorical, numerical, and text data, which are then combined into a unified architecture. The model uses embedding layers for the categorical features and leverages pre-trained BERT embeddings for the text features.

### Embedding Implementation

- **Categorical Features**: Each categorical feature is passed through its own embedding layer that transforms it into a dense vector of a fixed size. These vectors are then concatenated with the numerical features and the text embeddings.
  
- **Text Features**: Text data is tokenized and encoded using a pre-trained BERT model to obtain dense vector representations. These embeddings capture the context and semantics of the words in the text.

## Evaluation

The model's performance has been evaluated using metrics such as accuracy, precision, recall, and F1-score, as well as a confusion matrix and precision-recall curves to better understand the model's performance, especially in the context of an imbalanced dataset.

## Repository Structure

- `data/clean_data.xlsx`: The preprocessed and cleaned dataset used for training the model.
- `code/Indentify_Fake_News_EDA_Feature_Engineering.ipynb`: The Jupyter Notebook that contains the code for Data Preprocessing, EDA and Feature Engineering.
- `code/Indentify_Fake_News_Modelling.ipynb`: The Jupyter Notebook that contains the code for training the neural network model.

## Usage

To train the model and evaluate its performance, run the `Indentify_Fake_News_Modelling.ipynb` notebook. Ensure that you have all the dependencies installed.

## Contributions

Contributions to this project are welcome. You can improve the preprocessing steps, try different embeddings or model architectures, or work on hyperparameter tuning.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.

## Acknowledgments

- Thanks to all the contributors who have helped with the creation and maintenance of this project.
- Special thanks to [Data Source/Provider] for providing the dataset.
