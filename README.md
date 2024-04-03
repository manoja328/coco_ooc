# Out of Context detection
Official dataset repo for the IJCAI paper: Detecting Out-Of-Context Objects Using Graph Contextual Reasoning Network. Read the paper here https://www.ijcai.org/proceedings/2022/89

## Abstract
This paper presents an approach for detecting out-of-context (OOC) objects in images. Given an image with a set of objects, our goal is to determine if an object is inconsistent with the contextual relations and detect the OOC object with a bounding box. In this work, we consider common contextual relations such as co-occurrence relations, the relative size of an object with respect to other objects, and the position of the object in the scene. We posit that contextual cues are useful to determine object labels for in-context objects and inconsistent context cues are detrimental to determining object labels for out-of-context objects. 

## Download Images
The images used in the dataset are derived from [COCO](http://cocodataset.org/) dataset. All the images can be downloaded from https://visualqa.org/download.html (COCO train/val images)

## Download COCO-OOC dataset
Please, download the dataset using [this link](https://drive.google.com/file/d/19eePaTTdEnxHZtsTPDC7IdR6CXWyrFCd/view?usp=sharing). The zipped file contains npy files and corresponding jpeg images. The json entries in the dataset contains the following fields:
```
annotation = {}
annotation['original_ann_ids'] = ann_ids # COCO annotation ids
annotation['image_id'] = image_id  # COCO image id
annotation['ooc_annotation'] = {'image_id': image_id_j, #OOC object source from the from the COCO dataset
                                 'coco_ann_id': single_id_j,  # OOC object source annotation_id from the COCO dataset
                                 'bbox': bbox, #  OOC object bounding-box co-ordinates in (xmin, ymin, w, h) format
                                }

```

Please cite this work using the following bibtex:
```
@inproceedings{ijcai2022p89,
  title     = {Detecting Out-Of-Context Objects Using Graph Contextual Reasoning Network},
  author    = {Acharya, Manoj and Roy, Anirban and Koneripalli, Kaushik and Jha, Susmit and Kanan, Christopher and Divakaran, Ajay},
  booktitle = {Proceedings of the Thirty-First International Joint Conference on
               Artificial Intelligence, {IJCAI-22}},
  publisher = {International Joint Conferences on Artificial Intelligence Organization},
  editor    = {Lud De Raedt},
  pages     = {629--635},
  year      = {2022},
  month     = {7},
  note      = {Main Track},
  doi       = {10.24963/ijcai.2022/89},
  url       = {https://doi.org/10.24963/ijcai.2022/89},
}
```
