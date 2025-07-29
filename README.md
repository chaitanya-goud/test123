##  Explainable Cyberbullying Detection: A Hybrid Transformer-Based Approach with Groq API Integration

**Abstract**

Cyberbullying, a pervasive issue in the digital age, poses significant threats to mental well-being and safety. This research presents a novel, explainable cyberbullying detection system leveraging a hybrid architecture combining a pre-trained DistilBERT transformer and stacked Bidirectional GRU layers. Trained on a curated dataset of 100,000 anonymized social media texts, the model achieves high accuracy (over 96%) in binary classification. However, addressing the lack of transparency inherent in deep learning models, the system integrates the Groq API with the gemma2-9b-it large language model, providing human-readable explanations, confidence scores, and highlighted trigger terms for each prediction. This approach enhances user trust and facilitates informed decision-making by moderators and educators. The platform's open-source nature, cloud-ready infrastructure, and modular design enable its deployment across diverse settings, contributing to safer and more inclusive online communities.

**1. Introduction**

The proliferation of digital platforms has created unprecedented opportunities for connection and communication. However, this interconnectedness has also given rise to cyberbullying, a pervasive form of online harassment that can have devastating consequences for victims (Hinduja & Patchin, 2015). Cyberbullying encompasses a range of abusive behaviors, including verbal abuse, threats, social exclusion, and the spread of rumors or embarrassing content (Kowalski et al., 2014). Its impact extends beyond emotional distress, potentially leading to anxiety, depression, social isolation, and even suicidal ideation (Patchin & Hinduja, 2016).

Traditional methods for addressing cyberbullying rely heavily on human intervention, which is often reactive and unsustainable given the sheer volume of online content. The need for automated detection systems has become increasingly urgent. However, developing effective cyberbullying detection systems presents significant challenges. Cyberbullying often manifests in subtle and nuanced ways, employing sarcasm, slang, code words, and evolving language patterns that can evade traditional natural language processing (NLP) techniques (Suler, 2004).

This research proposes a novel, explainable cyberbullying detection system that addresses these challenges. The system leverages a hybrid architecture combining the contextual understanding of transformer-based models with the interpretability of explainable AI (XAI) techniques.

**2. Related Work**

Previous research on cyberbullying detection has explored various approaches, including:

* **Bag-of-Words (BoW) and TF-IDF:** These methods represent text as a collection of words, disregarding word order and context (Manning & Schütze, 1999). While simple to implement, they often struggle to capture the nuances of language used in cyberbullying.

* **Word Embeddings (Word2Vec, GloVe):** These techniques represent words as dense vectors, capturing semantic relationships (Mikolov et al., 2013; Pennington et al., 2014). However, they still lack the ability to fully understand context and long-range dependencies in text.

* **Recurrent Neural Networks (RNNs):** RNNs, particularly Long Short-Term Memory (LSTM) networks, can process sequential data and capture some degree of context (Hochreiter & Schmidhuber, 1997). However, they can be computationally expensive and prone to vanishing gradients.

* **Transformer-Based Models:** Transformer architectures, such as BERT and DistilBERT, have demonstrated superior performance in various NLP tasks, including text classification (Devlin et al., 2018; Sanh et al., 2019). Their ability to capture long-range dependencies and contextual relationships makes them well-suited for cyberbullying detection.

**3. Methodology**

The proposed cyberbullying detection system employs a hybrid architecture combining a pre-trained DistilBERT transformer with stacked Bidirectional GRU layers.

* **DistilBERT:** DistilBERT is a distilled version of the BERT model, offering comparable performance with reduced computational requirements (Sanh et al., 2019). It is pre-trained on a massive text corpus, enabling it to understand contextual relationships and semantic nuances in language.

* **Bidirectional GRU Layers:** Bidirectional GRU layers are stacked on top of the DistilBERT output, capturing sequential information and refining the representation of the input text. The bidirectional nature allows the model to consider both past and future context, improving its ability to understand the overall meaning of the text.

**3.1. Dataset**

The system was trained on a curated dataset of 100,000 anonymized social media texts. The dataset encompasses both binary (cyberbullying vs. not) and multi-class labels relevant to race, gender, and religion.

**3.2. Training and Evaluation**

The model was trained using a combination of binary and multi-class classification objectives. The DistilBERT layers were frozen to prevent overfitting, while only the weights of the GRU layers were trained. The training process involved splitting the dataset into training, validation, and test sets. The model's performance was evaluated using accuracy, precision, recall, and F1-score metrics.

**4. Results**

The hybrid architecture achieved outstanding results in binary cyberbullying classification, exceeding 96% accuracy. Precision and recall were also strong, indicating the model's ability to accurately identify both true positives and true negatives.

However, the model's performance in multi-class discrimination was less satisfactory, particularly when dealing with overlapping categories or imbalanced datasets. This highlights the inherent challenges in multi-class classification, especially in the context of nuanced and context-dependent language used in cyberbullying.

**5. Discussion**

The high accuracy achieved in binary classification demonstrates the effectiveness of the hybrid architecture in identifying cyberbullying. The combination of DistilBERT's contextual understanding and the GRU layers' sequential processing capabilities allows the model to capture the subtle patterns and nuances of abusive language.

The limitations in multi-class classification underscore the need for further research and development in this area. Addressing class imbalance and overlapping categories remains a significant challenge for cyberbullying detection systems.

**6. Conclusion**

This research presents a novel, explainable cyberbullying detection system that combines the power of transformer-based models with the transparency of XAI techniques. The system achieves high accuracy in binary classification while providing human-readable explanations for each prediction, enhancing user trust and facilitating informed decision-making.

The open-source nature and cloud-ready infrastructure of the platform enable its deployment across diverse settings, contributing to safer and more inclusive online communities. While challenges remain in multi-class classification, this work demonstrates the potential of explainable AI to address the complex issue of cyberbullying and empower individuals and organizations to create safer online spaces.


**References**

* Devlin, J., Chang, M. W., Lee, K., & Toutanova, K. (2018). Bert: Pre-training of deep bidirectional transformers for language understanding. arXiv preprint arXiv:1810.04805.

* Hinduja, S., & Patchin, J. W. (2015). Bullying beyond the schoolyard: Preventing and responding to cyberbullying. Routledge.

* Hochreiter, S., & Schmidhuber, J. (1997). Long short-term memory. Neural computation, 9(8), 1735-1780.

* Kowalski, R. M., Giumetti, G. W., Schroeder, A. N., & Lattanner, M. R. (2014). Bullying in the digital age: A critical review of cyberbullying research. Psychological Science in the Public Interest, 15(1), 3-22.

* Manning, C. D., & Schütze, H. (1999). Foundations of statistical natural language processing. MIT press.

* Mikolov, T., Sutskever, I., Chen, K., Corrado, G. S., & Dean, J. (2013). Distributed representations of words and phrases and their compositionality. Advances in neural information processing systems, 26.

* Patchin, J. W., & Hinduja, S. (2016). Cyberbullying: An overview. In Bullying prevention and intervention (pp. 227-249). Routledge.

* Pennington, J., Socher, R., & Manning, C. D. (2014). Glove: Global vectors for word representation. In Proceedings of the 2014 conference on empirical methods in natural language processing (pp. 1532-1543).

* Sanh, V., Debut, L., Chaumond, J., & Wolf, T. (2019). Distilbert: A distilled version of bert: smaller, faster, cheaper and lighter. arXiv preprint arXiv:1910.01108.

* Suler, J. (2004). The psychology of cyberspace. CyberPsychology & Behavior, 7(3), 323-326.
