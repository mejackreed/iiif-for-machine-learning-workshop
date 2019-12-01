---
title: IIIF Presentation API Basics
---

The IIIF Image API provides a machine-readable mechanism to retrieve pixels. But when we want to know more about the context of the image, such as its rights, title, description, and related information, and when we are working with structured sets of several images, we need the presentation API.

> The Presentation API presents "just enough metadata to drive a remote viewing experience". 

![IIIF Presentation API Definition](/img/presentation_api_slide.png)


### Manifest
The term "manifest" is used commonly in the IIIF universe. You will likely hear it used to refer to an "object". An object in this case could be a book, images of a statue, or a photograph. A manifest contains the information necessary to represent the object in an online viewing experience.

> The manifest can give information on how images are related to each other like the order that images should display, the structure of a document like a table of contents, and descriptive information for the resource and individual images. http://ronallo.com/iiif-workshop-new/presentation-api/manifest.html

>  The overall description of the structure and properties of the digital representation of an object. https://iiif.io/api/presentation/2.1/#overview-manifest

### Collection
A IIIF Presentation API response can also represent multiple objects/manifests, we call this a collection. A collection can also reference other collections. 

> An ordered list of manifests, and/or further collections. https://iiif.io/api/presentation/2.1/#overview-collection

### Sequence

> The order of the views of the object. https://iiif.io/api/presentation/2.1/#overview-sequences

There can be multiple sequences and these can 

### Canvas

> A virtual container that represents a page or view and has content resources associated with it or with parts of it. https://iiif.io/api/presentation/2.1/#overview-canvas

Think, a PowerPoint slide here.


## More resources
 - [**Manifest**](http://ronallo.com/iiif-workshop-new/presentation-api/manifest.html) - http://ronallo.com/iiif-workshop-new/presentation-api/manifest.html
 - [**Introduction to the Presentation API**](https://www.youtube.com/watch?v=fdWzwDc85EU) - https://www.youtube.com/watch?v=fdWzwDc85EU
