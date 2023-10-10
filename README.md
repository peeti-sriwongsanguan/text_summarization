# Summarization and Question Answering
Showcase of using comparison between Summarization and Question Answering with T5

<p>One of the challenges faced by current neural systems is the size of the input they can manage. As a result most of these systems end up truncating the input in some fashion. Can you get a good summary if you only read in the first 500 words of a document? One solution to this is to use an older approach called extractive summarization. In this approach the content of the input document(s) is broken into sentences which are scored for their relevance to either the document or to a query. This notebook will demonstrate the use of text summarization on a wikipedia article.</p>

<br>

**For abstractive summarization example** <p>I will use T5 to summarize some input text. We do this because the text in -> text out interface as well as the multi-task fine tuning makes it a great vehicle for demonstration</p>


<li><h1>1. Setup</h1>¶
Let's set up our environment so we can grab the wikipedia page on Natural Language Processing. You can modify the string to find the Wikipedia page of your choice. We'll need NLTK to build our extractive summarizer.

We'll also need the HuggingFace Transformers library for our abstractive summarization and question answering examples.

Now let's get a document to summarize. We'll use Wikipedia since it contains a large number of longer documents.
```
!pip install -q wikipedia
!pip install -q sentencepiece
!pip install -q transformers
```

```
import nltk
import nltk.corpus
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```
Then import tensorflow and T5 from Hugging Face

```
import tensorflow as tf
from transformers import T5Tokenizer, TFT5Model, TFT5ForConditionalGeneration

```

</li>
