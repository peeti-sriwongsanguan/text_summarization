# text_summarization
Showcase of using Summarization and Question Answering with T5

<p>One of the challenges faced by current neural systems is the size of the input they can manage. As a result most of these systems end up truncating the input in some fashion. Can you get a good summary if you only read in the first 500 words of a document? One solution to this is to use an older approach called extractive summarization. In this approach the content of the input document(s) is broken into sentences which are scored for their relevance to either the document or to a query. This notebook will demonstrate the use of text summarization on a wikipedia article.</p>

<br>

<p>**For abstractive summarization example**, I will use T5 to summarize some input text. We do this because the text in -> text out interface as well as the multi-task fine tuning makes it a great vehicle for demonstration</p>
