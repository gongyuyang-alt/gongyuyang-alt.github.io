---
permalink: /
#title: "Host"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


Hi! I am **Yuyang Gong**. Welcome to my personal homepage!
I am a third-year student in the School of Information Management at **Wuhan University**.  
Currently, I work in the [**Knowledge Mining and Information Retrieval Institute**](http://39.103.203.133/), Wuhan University, supervised by [**Dr. Jiawei Liu**](https://scholar.google.cz/citations?hl=zh-CN&user=xUpTKD8AAAAJ) and [**Prof.Wei Lu**](https://scholar.google.cz/citations?hl=zh-CN&user=mRdnCQ4AAAAJ).  

I am deeply fascinated by the field of **Trustworthy Artificial Intelligence (AI)**. The importance of building robust, fair, and reliable AI systems inspires me to continuously learn and explore innovative solutions. I aspire to deepen my understanding and contribute to advancing this critical area through dedicated research and collaboration.

Now, I am actively seeking **summer internship opportunities** in 2025 and preparing to apply for a **PhD program starting in Fall 2026**!


---

## Current Research Focuses

- Retrieval Augmented Generation (RAG) Security  
- Robustness of Neural Ranking Models (NRM)  
- Trustworthy Large Language Models (LLMs)  

---

## Publications

- **Yuyang Gong**, Zhuo Chen, Miaokun Chen, Fengchang Yu, Wei Lu, Xiaofeng Wang, Xiaozhong Liu, Jiawei Liu.   
  *Topic-FlipedRAG: Topic-Orientated Adversarial Opinion Manipulation Attacks against RAG models*.  
  *Usenix Security* (under review)(will be in arxiv soon!).  

- Zhuo Chen, **Yuyang Gong**, Miaokun Chen, Haotan Liu, Qikai Cheng, Fan Zhang, Wei Lu, Xiaozhong Liu, and Jiawei Liu.  
  [**FlipedRAG: Black-Box Opinion Manipulation Attacks to Retrieval-Augmented Generation of Large Language Models**](https://arxiv.org/abs/2501.02968).  
  *IEEE S&P* (under review).  


## Publication Details
### Topic-FlipRAG: Topic-Oriented Adversarial Opinion Manipulation Attacks Against RAG Models

### Background: Limitations in Current RAG Security Research
1. **Narrow Focus on Specific Queries**: Most existing studies target attacks on specific queries, which are not practical for real-world scenarios.
2. **Limited Focus on Fact-based Questions**: Current research mainly targets fact-based questions, which have limited impact and are easily defendable. There is insufficient exploration of open-ended opinion-based questions, especially for controversial topics.
3. **Predominance of White-Box Attacks**: The majority of existing research focuses on white-box attack scenarios.

### Attack Method:
We propose a novel attack by poisoning and modifying a small number of documents (without altering their core content or semantics), enabling them to be retrieved by multiple queries related to the same topic. This modified content is then fed into the large model, significantly influencing the RAG-generated opinions. The attack operates under a **black-box** setting, where the retrieval mechanism and LLM parameters are not accessible, and only the end-to-end inputs and outputs of the RAG system are available.

### Contributions and Innovations:
1. **Task-Level Innovation**: By poisoning a small set of documents, our attack enables the retrieval of these documents by multiple queries related to the same topic. This allows us to influence the user's perception based on their information needs. Compared to sentiment manipulation, our approach impacts the topic-level opinions more deeply and broadly. Unlike single-query attacks, our method operates on topic groups, making it more efficient, covert, and far-reaching in terms of user influence.
   
2. **Proposed Topic-Oriented Black-Box RAG Attack**: We introduce a knowledge-guided, multi-granular topic-oriented approach to black-box RAG attacks, a significant advancement in the manipulation of opinion generation for large language models.
   
3. **Experimental Validation**: Extensive experiments demonstrate that Topic-FlipedRAG significantly outperforms baseline methods. We conduct thorough ablation experiments and real-world user experiments to validate the practical threats posed by this attack.
   
4. **Ineffectiveness of Current Defense Methods**: Current defense strategies, such as perplexity-based, random masking, and reranking approaches, are ineffective against the Topic-FlipedRAG attack.

---

### FlipedRAG: Black-Box Opinion Manipulation Attacks to Retrieval-Augmented Generation of Large Language Models
For more details in [arXiv: 2501.02968](https://arxiv.org/abs/2501.02968)

### Key Contributions:
1.	Novel Attack Proposal: We introduce FlipedRAG, a transfer-based opinion manipulation attack against RAG systems in LLMs within a black-box setting. Unlike previous research, which assumes direct access to IR ranking results, our approach simulates the IR model’s behavior by training a surrogate model using RAG‘s end-to-end outputs and then generates adversarial triggers . This method closely mirrors real-world scenarios, where attackers lack direct access to internal ranking mechanisms.
2. First Exploration of Adversarial Opinion Manipulation in RAG: To the best of our knowledge, this is the first study exploring adversarial opinion manipulation in RAG systems, specifically for open-ended and controversial topics.
3. Demonstrated Effectiveness: Through automated evaluations and user experiments, we show that our transfer-based attack can significantly manipulate the opinions generated by RAG systems in a desired direction, achieving an average success rate improvement of 16.7%.