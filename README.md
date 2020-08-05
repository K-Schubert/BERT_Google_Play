# BERT_Google_Play

# Summary

Using the pretrained BERT base model to do sentiment analysis on Google Play reviews.

# Details

About 14'000 Google Play reviews are collected using the ```google-play-scraper``` module. The reviews are then sampled to create 3 balanced categories (negative, neutral and positive sentiment) using their "star" ratings.

The model is trained for 10 epochs on a GPU (~40 mins), val and train accuracy get better but val loss increases as well from epoch 1. The model is probably making more confident "bad" predictions so the Cross Entropy loss increases, but at the same time is getting better at classifying reviews. This might be due to the small validation set size and should be increased. Final test accuracy of ~84%.

Many thanks to Venelin Valkov's great tutorials!
