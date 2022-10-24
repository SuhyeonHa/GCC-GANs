# Toward Realistic Image Compositing with Adversarial Learning (CVPR 2019)

## Example Results (to be updated)
<img src="imgs/single_results.jpg" width="800"></img>
description

## Usage
### Prerequisites (to be updated)
- Python 3.7
- Pytorch 0.4.1
...

### Getting Started
#### Installation
Clone this repo:
```bash
git clone https://github.com/SuhyeonHa/GCC-GANs
cd GCC-GANs
```
#### Dataset
- [MS-COCO(train2014)](http://images.cocodataset.org/zips/train2014.zip) for content dataset

#### Data Pre-Processing
You can download validAnns_train.pkl, validAnns_dict_train.pkl, top5_dict_train.pkl, validAnns_val.pkl, validAnns_dict_val.pkl, and top5_dict_val.pkl (skipping procedure from 1 to 3).

When the phase is "train",

~~1. "generate_valid_anns.ipynb": to filter small objects and generate validAnns_train.pkl~~

~~2. "list-to-dict.ipynb": to generate validAnns_dict_train.pkl using validAnns_train.pkl~~

~~3. "top5-gcc-n0000.ipynb": to compare IoU between objects within the same category and pick top 5 items~~

4. "mask-operation.ipynb": to save five different triplet images for a single object with validAnns_train.pkl and top5_dict_train.pkl

When the phase is "test",

1. "test-dataset-generation-top5-bg.ipynb": to save testing triplet images with validAnns_val.pkl and top5_dict_val.pkl

#### Before Training
Please make sure all directories are set right.
```python
ann_dir = '/data/COCOdataset2017', # COCO dataset
data_dir = '/GCCdataset/alltypes', # GCC-GANs dataset
save_model_dir = '/GCC-GANs/models/', # Saving folder
```
