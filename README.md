**AI & Machine Learning (KAN-CINTO4003U) - Copenhagen Business School | Spring 2025**

***

### Group members
| Student name | Student ID |
| --- | --- |
| Jan Henrik Magnus Jacobsen | 176136 |

***

<br>

# Mandatory assignment 2

This repository contains the second mandatory assignment (MA2) for AIML25.  

* **Dev setup**: Just like for MA1, to complete this assignment, you need to follow the Development Setup guide. Please complete this setup before starting the assignment.

* **Guides**: Each of the sub-assignments has a corresponding *guide notebook*. Everything needed to complete the assignments is in those notebooks. The guide notebooks are there to help you understand and practice the concepts. Please refer to the table below:

    | Assignment | Assignment notebook | Guide notebook | Description |
    | --- | --- | --- | --- |
    | Part 1 | [assignments/bow.ipynb](assignments/bow.ipynb) | [guides/bow_guide.ipynb](guides/bow_guide.ipynb) | Bag-of-Words Models |
    | Part 2 | [assignments/bert.ipynb](assignments/bert.ipynb)| [guides/bert_guide.ipynb](guides/bert_guide.ipynb) | BERT |
    | Part 3 | [assignments/llm.ipynb](assignments/llm.ipynb) | [guides/llm_guide.ipynb](guides/llm_guide.ipynb) | LLMs |

* **Dataset**: The dataset for this assignment is [AG News](https://huggingface.co/datasets/fancyzhx/ag_news): AG is a collection of more than 1 million news articles - we will use a subset of these. The AG's news topic classification dataset is constructed by Xiang Zhang (xiang.zhang@nyu.edu) from the dataset above. It is used as a text classification benchmark in "*["Character-level Convolutional Networks for Text Classification"](https://arxiv.org/abs/1509.01626)*" by Xiang Zhang, Junbo Zhao and Yann LeCun (28, NIPS 2015).

* **Using Google Colab**: If you run into issues with memory or don't have access to a local GPU, Google Colab is a good alternative for part 2. Note that it should be possible to complete the assignment on a local machine without a GPU as well, although there might be some waiting time while models train, encode, or predict. If you do use Colab, please make sure to download the finished notebook and save it to your local machine before committing your code to GitHub and submitting the assignment.

## Part 1: Bag of Words (BoW)
In this part, you will implement a simple Bag of Words (BoW) model. You will use the `CountVectorizer` (or `TFidfVectorizer`) from `sklearn` to create a BoW representation of a text dataset. You will then use the BoW representation to train a simple classifier for the AG News dataset. Specifically, your task is to:

- Explore the guidelines in the `bow_guide.ipynb` notebook.
- Implement a BoW model to classify news articles in `assignments/bow.ipynb`.
- Train one or more classifiers (e.g., Logistic Regression) on the BoW representation.
- Experiment with different hyperparameters to (possibly) improve performance over the baseline in `bow.ipynb`.
- Briefly reflect on the performance of your system and your choices of hyperparameters for the BoW model and the classifier.
    - Write your analysis as a markdown cell in the bottom of the notebook.

## Part 2: BERT
In this part, you will embed the AG News dataset using a pre-trained BERT model. You will then use the BERT embeddings to train a simple classifier, similar to the BoW model in part 1. Specifically, your task is to:

- Explore the guidelines in the `bert_guide.ipynb` notebook.
- Implement a BERT model to classify news articles in `assignments/bert.ipynb`.
- Train one or more classifiers (e.g., Logistic Regression) on the BERT embeddings.
- Experiment with different hyperparameters to (possibly) improve performance over the baseline in `bert.ipynb`.
- Briefly reflect on the performance of your system and your choices of hyperparameters for the BERT model and the classifier.
    - Write your analysis as a markdown cell in the bottom of the notebook.

- __**Optional**__: Fine-tune a pre-trained BERT model to classify news articles as is done in [guides/bert_guide_finetuning.ipynb](guides/bert_guide_finetuning.ipynb), the same task as in part 1. As this requires more computational resources, this part is optional. If you do decide to complete this part, you will need to use a GPU (e.g., Google Colab) to train the model. (For reference, training on a 2020 Macbook Pro with 16GB RAM and an M1 chip results in an out-of-memory error). Therefore, we suggest that you use Google Colab or another cloud-based service with a GPU. You can easily upload the `bert_guide_finetuning.ipynb` notebook to Google Colab and run it there.

## Part 3: Language Models (LLMs)
In this part, you will choose and use an LLM from the WatsonX.ai platform to classify news articles, the same task as in part 1. Please follow the `WatsonX.ai guide` on Canvas to get access to the platform. Specifically, your task is to:

- Explore the guidelines in the `llm_guide.ipynb` notebook.
- Select one or more LLM model(s) from WatsonX.ai.
- Use different prompt engineering techniques to (possibly) improve performance over the baseline in `llm_guide.ipynb`.
- Experiment with different hyperparameters and evaluate the model(s) using the test set.
- Briefly reflect on the performance of your LLM system, your choices of prompt engineering techniques and how it compares to the BoW and BERT approaches.
    - Write your analysis as a markdown cell in the bottom of the notebook.

Please be mindful of token usage - but don't worry too much about it. The WatsonX.ai platform provides a generous amount of tokens for this assignment.
***

<br>

**Please see due dates and other relevant information in the assignment description on Canvas.**

<br>

***

## Getting started
Please see the relevant sections in the `Development setup guide` document on Canvas for instructions. To iterate, you need to:

1. Fork this repository to your own GitHub account.
2. Clone the forked repository to your local machine.
3. Create a virtual environment (from `environment.yml` with conda) and install the required packages.
4. Start working on the assignment.
5. Commit and push your changes to your GitHub repository.
6. Submit a link to your GH assignment repo on Canvas (make sure that your repository is public!).

___