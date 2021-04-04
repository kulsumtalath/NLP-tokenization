# Sentence Tokenization


```python
from nltk.tokenize import sent_tokenize
```


```python
text="""A paragraph is a brief piece of writing that's around seven to ten sentences long.
The paragraph form refers to a group of sentences focusing on a single topic."""
```


```python
sent_tokenize(text)
```




    ["A paragraph is a brief piece of writing that's around seven to ten sentences long.",
     'The paragraph form refers to a group of sentences focusing on a single topic.']



# Word Tokenization

It does not seperates the words using punctuation and spaces


```python
from nltk.tokenize import word_tokenize
```


```python
text="What a beautiful day it is!! It's been raining from morning."
```


```python
word_tokenize(text)
```




    ['What',
     'a',
     'beautiful',
     'day',
     'it',
     'is',
     '!',
     '!',
     'It',
     "'s",
     'been',
     'raining',
     'from',
     'morning',
     '.']




```python
from nltk.tokenize import TreebankWordTokenizer
tokenizer=TreebankWordTokenizer()
tokenizer.tokenize(text)
```




    ['What',
     'a',
     'beautiful',
     'day',
     'it',
     'is',
     '!',
     '!',
     'It',
     "'s",
     'been',
     'raining',
     'from',
     'morning',
     '.']



# PunktWordTokenizer

It seperates the punctuation from the words


```python
from nltk.tokenize import WordPunctTokenizer
```


```python
tokenizer=WordPunctTokenizer()
```


```python
tokenizer.tokenize("What a beautiful day it is!! It's been raining from morning.")
```




    ['What',
     'a',
     'beautiful',
     'day',
     'it',
     'is',
     '!!',
     'It',
     "'",
     's',
     'been',
     'raining',
     'from',
     'morning',
     '.']



Using regular expression


```python
from nltk.tokenize import RegexpTokenizer
```


```python
tokenizer=RegexpTokenizer("[\w]+")
text="What a beautiful day it is!! It's been raining from morning."
tokenizer.tokenize(text)
```




    ['What',
     'a',
     'beautiful',
     'day',
     'it',
     'is',
     'It',
     's',
     'been',
     'raining',
     'from',
     'morning']




```python

```
