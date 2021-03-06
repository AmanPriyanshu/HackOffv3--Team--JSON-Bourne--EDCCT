# EDCCT

EDCCT ( Embedders for Deep Contextual Clustering of Tags ), a practical approach towards accurate contextual clustering of review tags.

## PROJECT NAME:

EDCCT - Embedders for Deep Contextual Clustering of Tags

## SYNOPSIS: 

EDCCT ( Embedders for Deep Contextual Clustering of Tags ), a practical approach towards accurate contextual clustering of review tags. We use linguistic embedders ([1]: Look Up Word embeddings, [2] Contextual Word Embeddings and [3] Sentence Embeddings) to derive vectorial representation of each of the tags, following which we used cosine similarity to cluster them.

## The problem it solves:

EDCCT solves the problem of multiple tags referring to the same thing by combining similar tags into a single tag-head. We approached this problem statement while keeping in mind recent development in the field of linguistic representation of words and sentences. It is able to geometrically cluster both, contextually and meaning based tags, thereby reducing repeating review tags.

## Challenges we ran into:

While approaching this problem, we ran into two major problems, we were able to overcome both of them. The first one being, frequency based tags, did not give accurate representation of product-reviews. Secondly, lookup word embeddings did not give accurate cluster results, therefore we finally propose a deep contextual representation using Universal Sentence Encoder to embed and cluster similar tags. We were able to solve both the problems we faced, by using contextual representation, thereby allowing us to get substantial results, you can check our results at [RESULTS](https://github.com/AmanPriyanshu/EDCCT-Embedders-for-Deep-Contextual-Clustering-of-Tags/blob/main/combined_tags_use.zip)

## Executing-our-Project:

0. Please install all the necessary libraries mentioned in `requirements.txt`
1. To extract reviews from JSON into CSV file please execute: `reader.py` which will return data in a CSV format: `reviews_Cell_Phones_and_Accessories_5.csv`
2. To extract product-wise reviews please execute: `product_wise_generator.py` which will geenrate a directory, with product-wise reviews: `product_wise_reviews` 
3. To generate tags based on frequency please execute: `tagger.py` which will generate a CSV file containing frequency based tags of reviews: `product_wise_tags.csv`
4. To cluster similar tags product wise please execute: `embedders.py` which will generate final clustered output in the directory: `combined_tags_use`
5. To look at results, please download: [https://github.com/AmanPriyanshu/EDCCT-Embedders-for-Deep-Contextual-Clustering-of-Tags/blob/main/combined_tags_use.zip](https://github.com/AmanPriyanshu/EDCCT-Embedders-for-Deep-Contextual-Clustering-of-Tags/blob/main/combined_tags_use.zip)

## Side-Note:

To install GloVe and BERT embeddings, some of the embeddings proposals we made, please follow the given steps, however, please be aware this is not required for the final execution and may be skipped.
```console
!wget --no-check-certificate https://storage.googleapis.com/laurencemoroney-blog.appspot.com/glove.6B.100d.txt -O /tmp/glove.6B.100d.txt
curl https://storage.googleapis.com/bert_models/2020_02_20/uncased_L-4_H-512_A-8.zip > uncased_L-4_H-512_A-8.zip
```

## Project-Demo:

We have analysed and worked with three embeddings, namely: Universal Sentence Encoders, BERT, GloVe. We finally propose Universal Sentence Encoder as the ideal embedder.
[Please Check Out Some of Our Examples](https://github.com/AmanPriyanshu/EDCCT-Embedders-for-Deep-Contextual-Clustering-of-Tags/blob/main/Final%20Tags%20Generated%20Examples.pdf)

```console
Product: B007FXMOV8
Orignal tags: [screen protector, rubber tip, rubber tipped, use stylus, touch screen, using stylus, stylus tip, screen use, pen great]
Generated tags after deleting similar tags: [using stylus, rubber tip]

Product: B0088U4YAG
Original tags: [car charger, works great, iphone 5, car chargers, two devices, charge phone, charger, charge, charge two devices, charging two devices, enough power charge, charger two ports]
Generated tags: [charge two devices, car charger]
```

## Technologies we used:

Python, Universal Sentence Encoder(DAN)

## Links:

GitHub: https://github.com/AmanPriyanshu/EDCCT-Embedders-for-Deep-Contextual-Clustering-of-Tags

Video Demo: 
YouTube: https://youtu.be/BzK9kgMfw88
