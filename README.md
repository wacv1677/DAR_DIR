## Implementation for submission 1677 for WACV2024 
Code for our WACV2024 paper: "Evaluation of Video Masked Autoencoders’ Performance and Uncertainty Estimations for Driver Action and Intention Recognition"

## Dependencies
* pytorch==2.0.0 
* torchmetrics
* scikit-learn==1.3.0
* pytorchvideo
* numpy
* accelerate==0.22.0
* transformers==4.32.1
* torchvision==1.13.0
* bayesian-torch==0.4.0
* tqdm

## Preparation 
Dataset download:
* [Brain4Cars](http://brain4cars.com/)
* [HDD](https://usa.honda-ri.com/hdd) (Note that you need your official university e-mail to request and sign an agreement to get access to the dataset).

For the Brain4Cars dataset, you can also run the startup.sh file.
This script downloads the data, and the repository from [Rong et al (2020)](https://github.com/yaorong0921/Driver-Intention-Prediction) and creates folders with symlinks to the video files for the five folds. 
Our implementation expects the videos to use that folder structure (e.g., _"./brain4cars_data/[train, val]/fold0/[rturn, lturn, rchange, lchange, end action]/*.avi"_.
```
bash startup.sh
```

Additionally, to be sure there is no overlap between train/test partitions, you can run the following script.
This checks for every test partition if an instance is part of the other test partitions and not part of the train set of that particular fold.

```
python utils/dataset_check.py
```

## Training

### Deterministic

### Probabilistic

## Validation
### Deterministic

### Probabilistic


## Models
| Modalities | Fold 0 - Dataset 1 Link | Fold 1 - Dataset 2 Link | Fold 2 - Dataset 3 Link | Fold 3 - Dataset 1 Link | Fold 4 - Dataset 2 Link |
|------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| in-cabin   | [Link](url_to_dataset1) | [Link](url_to_dataset1) | [Link](url_to_dataset1) | [Link](url_to_dataset1) | [Link](url_to_dataset1) | 
| exterior   | [Link](url_to_dataset2) | [Link](url_to_dataset2) | [Link](url_to_dataset2) | [Link](url_to_dataset2) | [Link](url_to_dataset2) | 
| both       | [Link](url_to_dataset3) | [Link](url_to_dataset3) | [Link](url_to_dataset3) | [Link](url_to_dataset3) | [Link](url_to_dataset3) | 


### Acknowledgements

We gracefully made use from the code from [Rong et al.(2020)](https://github.com/yaorong0921/Driver-Intention-Prediction), [Torch Multimodal](https://github.com/facebookresearch/multimodal/blob/main/torchmultimodal/modules/layers/attention.py)
