---
title: More about annotations
---

Readers make marks in books. You bookmark pages in your browser. You quote a passage of text and comment on it. IIIF provides the platform for allowing for all different kinds of scholarly annotation.

Annotations can be useful for:

- Research
- Teaching
- Machines
- Crowdsourcing
- Conservation

![](/img/annotation-body-target.png)

An annotation target is a URI pointing in whole or in part (fragment) to a resources like:

- web pages
- audio video
- images
- IIIF canvases

Annotation bodies, the content of the comment/annotation, can be:

- text
- images
- audio
- video
- URIs

Annotations are created for different reasons like:

- painting
- commenting
- bookmarking

Adapted from [jronallo/iiif-workshop](https://raw.githubusercontent.com/jronallo/iiif-workshop-new/master/content/what-now/annotation.md)


### Open Annotation vs. Web Annotation

The IIIF Presentation v2.x APIs use the [Open Annotation](http://openannotation.org) Data Model for representing annotations. The examples in this workshop use this. However, in IIIF Presentation v3.0, the data model will be changed to use the W3C [Web Annotation](https://www.w3.org/TR/annotation-model/) Data Model. While these data models are fairly similar, its worth calling out the change as syntax and usage will be different.
