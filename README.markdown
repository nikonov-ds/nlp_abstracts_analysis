# Mapping NLP Research Trends: Analyzing and Clustering Paper Abstracts

This project analyzes 1,000 research paper abstracts related to Natural Language Processing (NLP) from arXiv to identify key research trends and topics using advanced NLP techniques. By leveraging state-of-the-art tools like BERTopic and K-Means clustering, the project uncovers prominent themes in the field, such as multilingual NLP and ethical considerations like privacy and hate speech detection.

## Objectives

- Collect and preprocess 1,000 NLP-related abstracts from arXiv.
- Perform clustering and topic modelling to identify research trends.
- Visualize the results through UMAP plots, word clouds, and crosstab analysis.

## Methodology

1. **Data Collection**: Abstracts are fetched using the arXiv API with the query "NLP".
2. **Preprocessing**: Text data is cleaned using `spacy_cleaner` to remove stopwords, punctuation, and apply lemmatization.
3. **Embedding Generation**: Semantic embeddings are generated for each abstract using the `SentenceTransformer` model (`all-MiniLM-L6-v2`).
4. **Clustering**: K-Means clustering is applied to the embeddings, with the optimal number of clusters determined by the elbow method.
5. **Topic Modelling**: BERTopic is used to extract 18 distinct topics from the abstracts.
6. **Visualization**: Results are visualized using UMAP for dimensionality reduction, word clouds for topic representation, and crosstab analysis to link topics to clusters.

## Key Findings

- **Topics**: The analysis identified 18 topics, including a strong focus on multilingual NLP (Topic 8, 79 papers) and ethical issues like privacy (Topic 6) and hate speech detection (Topic 4).
- **Clusters**: Abstracts were grouped into 10 clusters, revealing patterns in research focus, such as the intersection of multilingual models and low-resource languages.


## Visualizations

- **UMAP Plots**: Visualize the high-dimensional embeddings in 2D space.
- **Word Clouds**: Display key terms for each of the 18 topics.
- **Crosstab Analysis**: A table linking topics to clusters, highlighting dominant research areas.

## Conclusion

This project provides a comprehensive analysis of current NLP research trends using advanced NLP and machine learning techniques. The findings highlight the growing importance of multilingual models and ethical considerations in NLP, offering valuable insights for researchers and practitioners in the field. Future work could involve scaling the analysis to a larger dataset or exploring temporal trends in research focus.
