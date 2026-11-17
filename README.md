# CPE C314 – Artificial Intelligence 2

**Jose Rizal University · College of Computer Studies and Engineering · Computer Engineering Department**
**Student:** Mohammad Rayan B. Gubat · **Section:** CPE C314 – 401G · **First Semester, SY 2026–2027**

A compilation of lab activities and performance tasks for CPE C314 Artificial Intelligence 2. The work starts with classical machine learning (regression, feature selection) and moves through the NLP pipeline to sentiment analysis, chatbots, and a retrieval-augmented generation (RAG) system.

---

## Contents

| # | File | Activity | What it covers |
|---|------|----------|----------------|
| 1 | `Lab1_1_LR_GUBAT,_Mohammad_Rayan.ipynb` | Lab 1.1 – Linear Regression | Predicting California median house value: correlation analysis, imputation, MinMax scaling, 70/30 split, MAE/MSE/R² evaluation. |
| 2 | `PTS2_LRwithFS_GUBAT, Mohammad Rayan (1).ipynb` | PTS2 – Linear Regression with Feature Selection | Full model vs. Recursive Feature Elimination vs. PCA, compared on the same metrics. |
| 3 | `Lab1_NLP_GUBAT.ipynb` | Lab 1 – NLP with Regex | Regex-based text cleaning, extraction of URLs, emails, and hashtags, stopword removal, and a spam/ham email preprocessing pipeline. |
| 4 | `LAB2_1_AWS_GUBAT (1).ipynb` · `LAB2-1_AWS_GUBAT (1).pdf` | Lab 2.1 – AWS NLP (SageMaker) | Detecting negative reviews with SageMaker LinearLearner on 70,000 reviews: preprocessing, pipelines, endpoint deployment, and testing. The PDF has the written answers. |
| 5 | `Lab5_BoW_GUBAT,_VILLARDE (1).ipynb` | Lab 5 – Bag of Words and TF-IDF | TF-IDF on a 30-sentence Taglish dataset with custom Tagalog and English stopwords, a weight table, heatmap, and word cloud. |
| 6 | `Lab6_SentimentAnalysis_GUBAT (1).ipynb` | Lab 6 – Sentiment Analysis | VADER (rule-based) vs. TF-IDF with Naive Bayes, Logistic Regression, and Linear SVM. |
| 7 | `Lab8_Implementing_Chatbots_GUBAT (2).ipynb` | Lab 8 – Implementing Chatbots | Rule-based (NLTK), retrieval-based (TF-IDF with cosine similarity), and ML-based (intent classifier, MLP) chatbots, plus a context-based chatbot with a widget UI. |
| 8 | `PT3_NLP_Pipeline_GUBAT_VILLARDE (1).ipynb` | PT3 – NLP Pipeline | End-to-end pipeline for Taglish text: language identification, tokenization, stemming, lemmatization, custom stopword corpus, hybrid POS tagging, and a pipeline diagram. |
| 9 | `LAB9_RAG_NER_GUBAT.ipynb` | Lab 9 – RAG Chatbot and NER | Scam-aware RAG chatbot over Philippine anti-scam and cyber-law documents, with cited answers, abstention, evaluation, and a chunk-size ablation. |

Activities marked "(with Villarde)" in the filenames were completed in pairs.

---

## Highlights

- **Regression (Lab 1.1, PTS2):** The full model reached R² ≈ 0.63 (MAE ≈ $51K). RFE (R² ≈ 0.51) and PCA (R² ≈ 0.53) with 4 features each performed worse than the full model.
- **Taglish NLP (Lab 5, PT3):** A custom pipeline for code-switched Filipino-English text, including a 218-word custom stopword corpus and rule-based Tagalog POS tagging, since standard NLTK tools are English-focused.
- **RAG Chatbot (Lab 9):** 100% top-1 and top-3 retrieval accuracy on 12 in-scope questions, 5/5 out-of-scope questions correctly refused, and about 4.5 s mean end-to-end latency. It uses `all-MiniLM-L6-v2` embeddings and `flan-t5-base`, with source file and page citations.

---

## Learning Outcomes

| CLO | Description | Demonstrated in |
|-----|-------------|-----------------|
| **CLO1** | Demonstrate significant understanding of machine learning, neural networks, computer vision, and natural language processing concepts. | Lab 1.1, PTS2, Lab 1, Lab 5, Lab 6, Lab 8, PT3 |
| **CLO2** | Use and apply appropriate AI tools and algorithms to solve real-world cases. | Lab 2.1, Lab 6, Lab 8, Lab 1.1, PTS2 |
| **CLO3** | Develop a research project that applies any of the domains of AI to real-world cases. | Lab 9, PT3, Lab 5 |

---

## Tools and Libraries

- **Language and environments:** Python, Jupyter, Google Colab, Amazon SageMaker
- **Data and ML:** pandas, NumPy, scikit-learn, XGBoost
- **NLP:** NLTK (including VADER), regex, spaCy
- **RAG and transformers:** sentence-transformers, Hugging Face Transformers (`flan-t5`), PyMuPDF
- **Visualization:** matplotlib, seaborn, WordCloud, ipywidgets
- **Cloud:** AWS (SageMaker, Pricing and IAM concepts from the AWS course)

---

## Running the Notebooks

1. Open a notebook in **Google Colab** (most notebooks were written there) or Jupyter.
2. Run the install cells at the top of each notebook, then restart the kernel if prompted.
3. Notes for specific notebooks:
   - **Lab 2.1** requires an Amazon SageMaker environment (AWS Academy lab) to deploy the endpoint. Delete the endpoint after use to avoid charges.
   - **Lab 9** needs the source documents (Philippine RA PDFs) uploaded to `docs/`, with the RA number kept in each file name. The GPU runtime in Colab is recommended.
   - **Lab 6** loads `customer_reviews.xlsx` through a Colab upload prompt.

---

## Notes

- All work is for academic purposes under CPE C314 – Artificial Intelligence 2.
