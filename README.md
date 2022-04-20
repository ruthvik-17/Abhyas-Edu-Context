# Abhyas-Edu-Context
### Submission for TigerGraph Graph for All Challenge
TigerGraph based tool to find the context of a topic in a child's educational journey.

**Contact Info**: Ruthvik Reddy SL | ruthvikreddy.sankepalli@gmail.com

**Graph for All Demo Video**: [link](https://www.youtube.com/watch?v=YYeh53WhcCk) 

**Devpost Submission**: [link](https://devpost.com/software/abhyas-edu-context)
 
**Project Abhyas Site**: [link](www.tinyuel.com/Project-Abhyas)

<!-- **Problem Statement addressed (or explain your own):**
 -->
## Problem
Imagine that you're a teacher in a grossly underfunded system, where only a quarter of your students have grade-level educational competency and are going through severe socio-economic challenges in societies that cannot dream because they are too busy surviving. English is the desired medium of instruction, but you as a teacher are not familiar with it. Along with this, you're forced to do redundant paperwork each day.

This is the reality of 5M teachers in 1M public schools of India, struggling to uplift their 185M students of one of the world's youngest countries.

And then the pandemic hit.

Now, the teachers have to deal with their students' learning losses while there is a surge in student enrollment in public schools due to the loss of parental income.

In India, due to globalization, not many are willing to send their kids to anything other than an English medium school. But the problem is that not many teachers in Indian public schools know English. 

To tackle this issue, we at Project Abhyas are creating lesson readings. These are audio recordings of textbook chapters in English, aided by vernacular explanations. While writing scripts for the pilot run, our writers wanted to know how a specific concept taught in a lower grade is used in other subjects and subsequent grades. 

## Challenge
To build a tool to find similar topics across textbooks to help not only our scriptwriters but also the teachers and the students to understand the bigger picture. Building context-aware search solution is tricky, and TigerGraph, with its dynamic nature, opens up a world of possibilities for storing and analyzing data.

## Our Solution 

We parsed textbooks across grades and extracted keywords from each sentence using BERT-based deep learning models for the data. These keywords are stemmed and stored in a TigerGraph along with contextual information like the sentence, page number, grade, and subject.

When the user inputs a query, we extract keywords, stem them, and then query TigerGraph for sentences connected to these keywords. We then convert the resulting sentences into embeddings using deep learning models to perform sentence similarity and show the topics with the best context match.

Abhyas edu context has implications across the topics of Impact, Innovation, Ambition and Application.			

- Contextual learning is imperative to become an informed learner.

- With our schema, we can filter concepts at the book, subject levels and grade ranges to see the topic progression.

- As a part of the Abhyas Teacher Assistant platform, Edu Context can directly help millions of students in India and many more indirectly.

- The solution can be extended to include n-grams, and similarities at para, section, chapter levels by extracting key components at respective levels and creating embeddings.

- With further additions to data processing and schema, we can build a general purpose dashboard/api based platform to allow anyone to upload documents and provide context aware search.

- A public, domain specific search library for common use cases (board/stream specific textbook search) can be pre loaded for usage at scale.

## This transcends the education domain and has applications across industries.

Other additions: 

 - **Data**: We parsed textbooks(included in the repo) across grades and extracted keywords from each sentence using BERT based deep learning models.
These keywords are stemmed and stored in a TigerGraph along with contextual information like the sentence, page number, book name, grade and subject.
 
 - **Technology Stack**: TigerGraph, PyTigerGraph, Python, NLTK, Deep Learning  
<!--  - **Visuals**: Feel free to include other images or videos to better demonstrate your work. -->

## Dependencies

Mentioned in the jupyter notebooks.

## Installation

### For data preparation (not needed as the data file is already created and is at Data/csv/11_python.csv)
### Note: 11_python.csv contains all the data (6th - 10th grade Science and 11th Python) unlike the name sugests.

1. Clone repository
2. Open read_data.ipynb
3. Run cells from the start to install dependencies
4. You'll find the data at Data/csv/11_python.csv

### For Abhyas Edu Context Testing

1. Clone repository
2. Use the **TG_tar/export_184196893.tar.gz** file to setup TigerGraph Cloud machine
3. Load **11_python.csv** with has header **'check the box'**, delimiter **'|'** and enclosing character **'"' (double quote)**
4. Open **Query_TigerGraph.ipynb** on Google colab, use GPU runtime
5. Set **credentials** for pyTigerGraph to access your graph from the notebook
6. Run all the cells from the top (includes library dependencies and assets)

## Known Issues and Future Improvements

- The solution can be extended to include n-grams, and similarities at para, section, chapter levels by extracting key components at respective levels and creating embeddings.

## Reflections

- It has been gruelling but fun few days learning TigerGraph, building and submitting the project.
- The end and the begining. :)

## References

- https://www.sbert.net/
- https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2
- https://github.com/MaartenGr/KeyBERT
