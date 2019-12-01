---
title: More about the Presentation API
---

## Sample Presentation API response

A simple IIIF Presentation API response looks something like this:

```json
{
  "@context": "http://iiif.io/api/presentation/2/context.json",
  "@id": "https://purl.stanford.edu/hg676jb4964/iiif/manifest",
  "@type": "sc:Manifest",
  "label": "(center) Martin Luther King Jr. & Joan Baez march to integrate schools,  Grenada, MS, 1966",
  "attribution": "Bob Fitch photography archive, © Stanford University Libraries",
  "logo": {
    "@id": "https://stacks.stanford.edu/image/iiif/wy534zh7137%2FSULAIR_rosette/full/400,/0/default.jpg",
    "service": {
      "@context": "http://iiif.io/api/image/2/context.json",
      "@id": "https://stacks.stanford.edu/image/iiif/wy534zh7137%2FSULAIR_rosette",
      "profile": "http://iiif.io/api/image/2/level2.json"
    }
  },
  "seeAlso": {
    "@id": "https://purl.stanford.edu/hg676jb4964.mods",
    "format": "application/mods+xml"
  },
  "metadata": [
    {
      "label": "Available Online",
      "value": "<a href='https://purl.stanford.edu/hg676jb4964'>https://purl.stanford.edu/hg676jb4964</a>"
    },
    {
      "label": "Title",
      "value": "(center) Martin Luther King Jr. & Joan Baez march to integrate schools,  Grenada, MS, 1966"
    },
    {
      "label": "Contributor",
      "value": "Fitch, Bob (Photographer)"
    },
    {
      "label": "Type",
      "value": "StillImage"
    },
    {
      "label": "Type",
      "value": "photographs"
    },
    {
      "label": "Type",
      "value": "documentary photographs"
    },
    {
      "label": "Date",
      "value": "1966"
    },
    {
      "label": "Format",
      "value": "1 photograph"
    },
    {
      "label": "Format",
      "value": "image/jpeg"
    },
    {
      "label": "Description",
      "value": "Contact sheet for this image is located in Box 52, Folder 1, sheet 796. Negative is located in Box 63, Folder 18, sheet 796."
    },
    {
      "label": "Subject",
      "value": "King, Martin Luther, Jr., 1929-1968"
    },
    {
      "label": "Subject",
      "value": "Baez, Joan"
    },
    {
      "label": "Coverage",
      "value": "Grenada (Miss.)"
    },
    {
      "label": "Identifier",
      "value": "M1994_MLK__0380_796-44"
    },
    {
      "label": "Identifier",
      "value": "M1994"
    },
    {
      "label": "Relation",
      "value": "Bob Fitch photography archive -- Martin Luther King Jr. gallery, 1965-1966"
    },
    {
      "label": "PublishDate",
      "value": "2018-07-25T21:40:28Z"
    }
  ],
  "description": "Contact sheet for this image is located in Box 52, Folder 1, sheet 796. Negative is located in Box 63, Folder 18, sheet 796.",
  "thumbnail": {
    "@id": "https://stacks.stanford.edu/image/iiif/hg676jb4964%2F0380_796-44/full/!400,400/0/default.jpg",
    "@type": "dctypes:Image",
    "format": "image/jpeg",
    "service": {
      "@context": "http://iiif.io/api/image/2/context.json",
      "@id": "https://stacks.stanford.edu/image/iiif/hg676jb4964%2F0380_796-44",
      "profile": "http://iiif.io/api/image/2/level2.json"
    }
  },
  "sequences": [
    {
      "@id": "https://purl.stanford.edu/hg676jb4964#sequence-1",
      "@type": "sc:Sequence",
      "label": "Current order",
      "viewingDirection": "left-to-right",
      "canvases": [
        {
          "@id": "https://purl.stanford.edu/hg676jb4964/iiif/canvas/hg676jb4964_1",
          "@type": "sc:Canvas",
          "label": "Image 1",
          "height": 3820,
          "width": 5426,
          "images": [
            {
              "@id": "https://purl.stanford.edu/hg676jb4964/iiif/annotation/hg676jb4964_1",
              "@type": "oa:Annotation",
              "motivation": "sc:painting",
              "resource": {
                "@id": "https://stacks.stanford.edu/image/iiif/hg676jb4964%2F0380_796-44/full/full/0/default.jpg",
                "@type": "dctypes:Image",
                "format": "image/jpeg",
                "height": 3820,
                "width": 5426,
                "service": {
                  "@context": "http://iiif.io/api/image/2/context.json",
                  "@id": "https://stacks.stanford.edu/image/iiif/hg676jb4964%2F0380_796-44",
                  "profile": "http://iiif.io/api/image/2/level2.json"
                }
              },
              "on": "https://purl.stanford.edu/hg676jb4964/iiif/canvas/hg676jb4964_1"
            }
          ]
        }
      ]
    }
  ]
}
```

Because this object only contains one image, its `Sequence` only contains one `Canvas`. A book might have more canvases, one representing each page.


## Request / Response cycle

While Image API requests can of course be made independently from Presentation API requests, they are often combined. Viewers will often 

![Request response cycle](/img/request_response.png)


## Linking other content

One really useful thing to note about the IIIF Presentation API is that it enables you to start linking other types of content to your manifest. A few different ways to link other content exist.

### `seeAlso`
> A link to a machine readable document that semantically describes the resource with the seeAlso property, such as an XML or RDF description. https://iiif.io/api/presentation/2.1/#seealso

An example:

```json
// From https://dms-data.stanford.edu/data/manifests/Parker/wz026zp2442/manifest.json
...
"seeAlso": {
  "@id": "https://purl.stanford.edu/wz026zp2442.mods",
  "format": "application/mods+xml"
},
...
```

### `otherContent`
The `otherContent` property enables you to link other content including `AnnotationList` to a manifest.

```json
// From https://dms-data.stanford.edu/data/manifests/Parker/wz026zp2442/manifest.json
...
"otherContent": [
  {
    "@type": "sc:AnnotationList",
    "@id": "https://dms-data.stanford.edu/data/manifests/Parker/wz026zp2442/list/1r.json"
  }
]
...
```

> **Question:** Now that we know more about the Presentation API, how could this be used to programatically access images for machine learning? How could you enhance resources using the Presentation API?
