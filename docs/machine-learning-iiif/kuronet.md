---
title: Case study: KuroNet
---

The [KuroNet project](http://codh.rois.ac.jp/kuronet/), or "KuroNet Koji Character Recognition Service", is a service that can take any IIIF Image API service and runs the KuroNet Koji OCR model against it.

## More about the project

"Kuzushiji, a cursive writing style, was used in Japan for over a thousand years, beginning in the 8th century. Over 3 million books, on a diverse array of topics such as literature, science, mathematics and cooking are preserved today. However, the standardization of Japanese textbooks known as the “Elementary School Order” in 1900, removed Kuzushiji from regular school curriculum, as modern japanese print became popular. As a result, most Japanese natives today cannot read books written or printed just 120 years ago." - https://www.kaggle.com/c/kuzushiji-recognition/overview/about-kuzushiji
 
 
 - [How Machine Learning Can Help Unlock the World of Ancient Japan](https://thegradient.pub/machine-learning-ancient-japan/)
 - [KuroNet: Pre-Modern Japanese Kuzushiji Character Recognition with Deep Learning](https://arxiv.org/pdf/1910.09433v1.pdf)
 - [Kaggle Competition: Kuzushiji Recognition](https://www.kaggle.com/c/kuzushiji-recognition)

## Kaggle Competition

The KuroNet Kaggle competition offered $15,000 in prize money to develop better algorithms for the KuroNet model. The winning solutions achieved 95% accuracy.

To learn more about the Kaggle competition and the Kuzushiji dataset its worth checking out [the visualization kernel](https://www.kaggle.com/anokas/kuzushiji-visualisation/notebook).

## Usage of IIIF

A new service can now use the KuroNet model against any IIIF Image API service. Here is an example.

![](/img/kuronetexample.png)

[Demo of KuroNet](http://codh.rois.ac.jp/kuronet/iiif-curation-viewer/?manifest=http://codh.rois.ac.jp/pmjt/book/200003080/manifest.json&pos=6&lang=en)
