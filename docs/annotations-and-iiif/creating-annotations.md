---
title: Creating annotations
---

1. Navigate to http://mirador-2-demo.netlify.com
1. Add a IIIF manifest to Mirador
    > Try using the IIIF manifest that we were using before: https://purl.stanford.edu/hg676jb4964/iiif/manifest

1. Click the "Annotation" button

    ![mirador annotation](/img/mirador-annotate.jpg)

1. You can now use the annotation tools to add annotations.

Annotations are stored on an annotation server setup for this workshop. You can see the annotations stored for the given canvas here:

```html
https://annotot-app.herokuapp.com/annotations?uri=https://purl.stanford.edu/hg676jb4964/iiif/canvas/hg676jb4964_1&format=json
```

The URI parameter in this url is the canvas URI from the manifest. You can manually modify this parameter to see annotations for other canvases.
