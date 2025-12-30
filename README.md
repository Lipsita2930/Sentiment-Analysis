**Overview**

This system processes large-scale customer review datasets to categorize sentiment (positive, negative, neutral) with contextual understanding. Unlike traditional surveys, it provides real-time, automated sentiment analysis to drive data-driven marketing decisions.
Key Achievement: F-score of 0.709 on Amazon Video Games review dataset (144K+ reviews)
Features

**Advanced Text Processing Pipeline**

TreeBank Tokenization for structural analysis
WordNet Lemmatization for semantic normalization
Part-of-Speech tagging for contextual understanding


**Multi-Method Sentiment Scoring**

SynSet-based lexical analysis
Opinion Lexicon integration
Sentiment polarity scoring (range: -1 to +1)


**Production Capabilities**

Handles large-scale datasets (144K+ reviews processed)
Null value handling and data preprocessing
Customer and product-level sentiment tracking



**Architecture**

Input Reviews → Preprocessing → Tokenization → POS Tagging → Lemmatization → Sentiment Scoring → Classification → Insights


**Tech Stack**

Core: Python 3.8+
NLP Libraries: NLTK (TreeBank Tokenizer, WordNet, SentiSynset, Opinion Lexicon)
Data Processing: Pandas, NumPy
Visualization: Seaborn, Matplotlib

**Dataset**
Trained and evaluated on Amazon Customer Reviews Dataset:

Source: Amazon Video Games Reviews
Size: 144,724 reviews
Format: TSV converted to CSV
Features: Product ID, Customer ID, Star Rating, Review Text

Methodology

**1. Data Preprocessing and Cleaning**

Null Value Handling: Systematic removal of incomplete records using dropna() methodology
Format Conversion: TSV to CSV transformation for efficient processing
Data Visualization: Exploratory analysis using Seaborn library for pattern identification
Quality Assurance: Filtering to retain only rated and inspected reviews

**2. Text Tokenization and Normalization**

TreeBank Tokenization: Regex-based sentence decomposition preserving syntactic structure
Comparative Analysis: TreeBank tokenizer demonstrated superior performance over Casual tokenizer
Lemmatization: WordNet-based reduction to canonical forms while preserving semantic meaning
Context Preservation: Maintains relationships between words for accurate sentiment interpretation

**3. Linguistic Feature Extraction**

Part-of-Speech Tagging: Penn TreeBank tag generation for grammatical context
Tag Conversion: Transformation of Penn TreeBank tags to simplified WordNet compatible tags
Contextual Analysis: Understanding word roles within sentence structure for nuanced sentiment detection

**4. Sentiment Scoring Mechanism**

SynSet Library Integration: Semantic grouping of words with similar meanings
Dual Scoring System: Parallel calculation of positive and negative sentiment scores
Score Range: Normalized sentiment values within [-1, 1] interval
SentiSynset Analysis: Fine-grained word-level sentiment assessment considering context
NLTK Opinion Lexicon: Pre-processed sentiment dictionary for baseline scoring

**5. Classification and Aggregation**

Multi-dimensional Analysis: Integration of Product ID and Customer ID for granular insights
Star Rating Correlation: Validation of sentiment scores against user-provided ratings
Threshold-based Classification: Categorization into positive, negative, and neutral sentiments
Weighted Averaging: Composite sentiment calculation across multiple reviews

**6. Evaluation and Validation**

Confusion Matrix Analysis: Comprehensive assessment of classification accuracy
Performance Metrics: Calculation of Precision, Recall, and F-Score
Cross-validation: Verification against star ratings for model reliability
Comparative Benchmarking: Performance assessment against existing sentiment analysis approaches

Performance Metrics
MetricScoreF-Score0.709PrecisionCalculated via TP/(TP+FP)RecallCalculated via TP/(TP+FN)



