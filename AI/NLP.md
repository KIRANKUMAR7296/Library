# Natural Language Processing

### Text Mining | Text Analysis 
- Deriving **Meaningful Information** from Natural Language **Text** and **Speech**.

### NLP
- Computer Learn and Understand from Human Languages.
- Interaction between Computers and Humans using the Natural Language.

### Process :

1. Human Talk to Machine.
2. Machine Capture Audio.
3. Convert Audio to Text.
4. Process Text Data (Interpret > Convert)
5. Convert Text to Audio.
6. Machine Talk | Reply to Human.

### Applications :

1. Google Translate.
2. Word Processor | Grammer Check in Microsoft Word.
3. Grammerly Grammer and Spelling Checking in Gmail.
4. IVR | Interactive Voice Response in Call Centers.
5. Voice Assistant : OK Google, Siri, Cortana and Alexa.
6. Chatbots
7. Customer Feedback Sentiment Analysis ( 😊🙂😔😡 )

### Tokenization
- Break a **Sentence** into Words.
- Understand Each Word

### Stemming and Lemmatization
- Grouping and `Reduce` Variant Forms to `Base` Forms
- ( Consult, Consultation, Consulting ) > Consult

### Stop Word
- Meaningless Words in a Sentence
- Search Engine only Search on the Basis of `Keywords` and not by whole Sentence.

How to `Remove` Stopwords
Using NLTK
1. Tokenize 
2. Compare with List of Stopwords and Drop that Words ( Token for Token in Text if not in Stopwords.words( ) ) 

Using spaCy