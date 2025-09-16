# Amazon_Bert
Tracing consumer emotion over time in 12k+ Amazon electronics reviews using BERTopic, NRC Emotion Lexicon, and TF-IDF to surface cluster-level tone shifts.

# Tracing Consumer Emotion Over Time
_A Clustered Sentiment Analysis of Amazon Electronics Reviews (2010–2017)_

This project tracks how emotion in Amazon electronics reviews evolves over time. It combines BERTopic for topic discovery, hierarchical clustering for thematic groups, the NRC Emotion Lexicon for emotion scoring, and TF-IDF to surface emotion-specific terms that shift from early to late periods.

## Why this matters
Most analyses stop at positive vs negative. This study shows how emotions like trust, anticipation, anger, and joy drift within product clusters such as charging accessories, remotes, and support themes.

## Methods
- **Dataset**: Amazon Electronics reviews, filtered to 2010–2017 (≈12,773 reviews after preprocessing)
- **Preprocessing**: NLTK lowercasing, stopword removal, lemmatization
- **Topic discovery**: BERTopic with UMAP for reduction and HDBSCAN for clustering
- **Thematic grouping**: Hierarchical clustering of topics into 15 clusters, 6 chosen for depth
- **Emotion scoring**: NRC Emotion Lexicon across 8 emotions plus polarity
- **Tone over time**: TF-IDF and c-TF-IDF to extract emotion-specific terms and track vocabulary shifts

## Key findings
- Overall tone stays positive and stable at the corpus level
- Cluster-level views reveal meaningful shifts, such as rising anticipation and frustration in support-related reviews
- TF-IDF highlights changing emotional vocabulary between early (2010–2013) and late (2015–2017) periods
