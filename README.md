# A Million News Headlines – Clustering Project  

This repository contains my work for the **Kaggle dataset "A Million News Headlines"** [link](https://www.kaggle.com/datasets/therohk/million-headlines), completed as part of a Natural Language Processing (NLP) project.  
The objective was to cluster headlines using different text representation and clustering approaches, and to evaluate performance using **Silhouette Score**.  

## 📅 Project Info  
- Developed: December 2024  

## 📖 Project Overview  
- Dataset: **A Million News Headlines** (downsized to 50K headlines due to resource limits).  
- Goal: Cluster news headlines into meaningful groups using NLP and ML techniques.  
- Evaluation Metric: **Silhouette Score** (range -1 to 1, higher is better).  

Best silhouette score achieved: **0.73011 [TF-IDF + PCA + KMeans (11 clusters)]**  

## 📂 Repository Structure  
```
million-news-headlines/
│── report.pdf        # Full written report with analysis, methods, and results  
│── src              # Source code (data cleaning, clustering models, evaluation)  
```  

## 🧪 Models and Approaches  

### 🔹 KMeans Clustering  
- Applied to multiple text representations.  
- Best result: **TF-IDF + PCA (11 clusters) → Silhouette: 0.73011**  

### 🔹 Hierarchical Clustering  
- Used agglomerative clustering.  
- Best result: **TF-IDF + PCA → Silhouette: 0.72518**  

## 🔧 Improvement Methods  
- **Principal Component Analysis (PCA):** Reduced dimensionality, improved clustering performance.  
- **Latent Semantic Analysis (LSA):** Captured semantic meaning, improved clustering over raw TF-IDF.  
- **Stemming & Stopword Removal:** Reduced noise in text.  
- **Tokenization Methods:**  
  - **TF-IDF**: Performed best overall.  
  - **Word2Vec**: Captured semantic meaning, but performance was lower than TF-IDF.  

## 📊 Results  

### KMeans Results  
| Approach                       | Silhouette Score   | Notes                       |  
|--------------------------------|--------------------|-----------------------------|  
| TF-IDF + PCA + KMeans(11)      | **0.73011**        | Best overall result         |  
| TF-IDF + LSA + KMeans(10)      | 0.69462            | Strong semantic grouping    |  
| Word2Vec + LSA + KMeans(3)     | 0.38110            | Moderate performance        |  
| TF-IDF + KMeans(3)             | 0.001336           | Poor result, too much noise |  

### Hierarchical Clustering Results  
| Approach        | Silhouette Score   |  
|-----------------|--------------------|  
| TF-IDF + PCA    | 0.72518            |  
| TF-IDF + LSA    | 0.68697            |  
| Word2Vec + PCA  | 0.20874            |  
| Word2Vec + LSA  | 0.22713            |  

## ⚙️ Tools and Libraries  
- **Python**  
- **Pandas** – data manipulation  
- **NLTK** – tokenization, stopword removal, stemming  
- **Scikit-learn** – TF-IDF, KMeans, PCA, silhouette score  
- **Gensim** – Word2Vec  
- **Matplotlib** – result visualization  
- **Numpy** – numerical computations  

## 🚀 Getting Started  
1. Clone the repository:  
   ```bash
   git clone https://github.com/chloewongwy/a-million-news-headlines-clustering-project.git
   ```  
2. Navigate into the project folder:  
   ```bash
   cd a-million-news-headlines-clustering-project/src
   ```  
3. Run the scripts to preprocess data and reproduce results.  
4. Check `report.pdf` for detailed explanations.  

## 📸 Visualizations  
<img width="800" height="600" alt="Figure_1" src="https://github.com/user-attachments/assets/9f417d58-af67-4fc1-82f5-22a3a8a48d4b" />



