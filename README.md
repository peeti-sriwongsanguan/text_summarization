# Summarization and Question Answering
Showcase of using comparison between Summarization and Question Answering with T5

<p>One of the challenges faced by current neural systems is the size of the input they can manage. As a result most of these systems end up truncating the input in some fashion. Can you get a good summary if you only read in the first 500 words of a document? One solution to this is to use an older approach called extractive summarization. In this approach the content of the input document(s) is broken into sentences which are scored for their relevance to either the document or to a query. This notebook will demonstrate the use of text summarization on a wikipedia article.</p>

<br>

<h2>For this demonstration: I want to use transformer to summarize and give question and answer this statement below</h2>

<i>Hyperbaric (high-pressure) medicine uses special oxygen
chambers to increase the partial pressure of O 2 around the patient and, when needed,
the medical staff. Carbon monoxide poisoning, gas gangrene, and decompression sickness
(the ’bends’) are sometimes treated using these devices. Increased O 2 concentration
in the lungs helps to displace carbon monoxide from the heme group of hemoglobin.
Oxygen gas is poisonous to the anaerobic bacteria that cause gas gangrene, so increasing
its partial pressure helps kill them. Decompression sickness occurs in divers who
decompress too quickly after a dive, resulting in bubbles of inert gas, mostly nitrogen
and helium, forming in their blood. Increasing the pressure of O 2 as soon as possible
is part of the treatment.</i>

**For abstractive summarization example** <p>I will use T5 to summarize some input text. We do this because the text in -> text out interface as well as the multi-task fine tuning makes it a great vehicle for demonstration</p>


<li><h1>1. Setup</h1>¶


I'll use HuggingFace Transformers library for our extraction and abstractive summarization and question answering examples.

Now let's get a document to summarize. We'll use Wikipedia since it contains a large number of longer documents.


Then import tensorflow and T5 from Hugging Face

```
import tensorflow as tf
from transformers import T5Tokenizer, TFT5Model, TFT5ForConditionalGeneration

```

</li>

<h3>I am amazed by the results of those senarios.... please see the notebooks</h3>
