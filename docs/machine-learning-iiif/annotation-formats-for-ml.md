---
title: Annotation formats for machine learning
---

### Third-party service annotations

We saw from our last exercise, that the Microsoft Cognitive Services Computer Vision API can return annotations about the image. The annotation response format is unique to Microsoft.

```json
[
  {
    "rectangle": {
      "x": 207,
      "y": 119,
      "w": 53,
      "h": 168
    },
    "object": "person",
    "confidence": 0.638
  },
  {
    "rectangle": {
      "x": 0,
      "y": 91,
      "w": 115,
      "h": 267
    },
    "object": "person",
    "confidence": 0.848
  },
  {
    "rectangle": {
      "x": 334,
      "y": 134,
      "w": 43,
      "h": 169
    },
    "object": "person",
    "confidence": 0.661
  }
]
```

As you work with other machine learning cloud providers you will find that many have their own custom responses that they use.

### Training data annotation formats

Several other formats exist for providing annotations in training data.

 - [Common Objects in Context (COCO)](http://cocodataset.org/#format-data) - A JSON format for providing annotations about the COCO image dataset.
      ```txt
         annotation{
          "id": int,
          "image_id": int,
          "category_id": int,
          "segmentation": RLE or [polygon],
          "area": float,
          "bbox": [x,y,width,height],
          "iscrowd": 0 or 1,
         }
      ```
 - [PASCAL VOC format](http://host.robots.ox.ac.uk/pascal/VOC/voc2008/htmldoc/) - Used by [ImageNet](http://image-net.org/download-bboxes) to provide annotations about objects in images
      ```xml
      <annotation>
        <folder>GeneratedData_Train</folder>
        <filename>000001.png</filename>
        <path>/my/path/GeneratedData_Train/000001.png</path>
        <source>
          <database>Unknown</database>
        </source>
        <size>
          <width>224</width>
          <height>224</height>
          <depth>3</depth>
        </size>
        <segmented>0</segmented>
        <object>
          <name>21</name>
          <pose>Frontal</pose>
          <truncated>0</truncated>
          <difficult>0</difficult>
          <occluded>0</occluded>
          <bndbox>
            <xmin>82</xmin>
            <xmax>172</xmax>
            <ymin>88</ymin>
            <ymax>146</ymax>
          </bndbox>
        </object>
      </annotation>
      ```
 - [Open Images Dataset](https://storage.googleapis.com/openimages/web/download.html#dataformats) - "Open Images is a dataset of ~9M images annotated with image-level labels, object bounding boxes, object segmentation masks, and visual relationships" 
      ```csv
      ImageID,Source,LabelName,Confidence,XMin,XMax,YMin,YMax,IsOccluded,IsTruncated,IsroupOf,IsDepiction,IsInside
      0001eeaf4aed83f9,xclick,/m0cmf2,1,0.022673031,0.9642005,0.07103825,0.80054647,0,0,0,0,0
      000595fe6fee6369,xclick,/m02xwb,1,0.45655376,0.6097202,0.20399113,0.50554323,0,0,1,0,0
      00075905539074f2,xclick,/m04yx4,1,0.020477816,0.32935154,0.0956023,0.665392,0,0,0,1,0
      000a1249af2bc5f0,xclick,/m/ 09j2d,1,0.56911767,0.99852943,0.0022172949,0.93569845,1,1,0,0,0
      ```

> **Question** Compare and contrast these formats with Open Annotation / Web Annotation.


> **Question** Could IIIF be used to help standardize this?
