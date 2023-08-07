# Gram-AODE
This repository contains an implementation of the Gram-based Attentive Neural Ordinary Differential Equations Network for Video Nystagmography Classification (ICCV 2023)
## Requirements
```
torch
torchdiffeq
PIL
pyts(optional)
```
## DataSets
The UCR Time Series Classification datasets can be downloaded at http://www.timeseriesclassification.com/index.php

This repository provides some sample VNG data. The rest of the dataset will be available after the data anonymization process is completed. To protect personal privacy, we will adjust the precision of the VNG data during data processing.

The `pyts` library can be conveniently used to convert time series into Gram features map. The examples in this repository are taken from the [official documentation](https://pyts.readthedocs.io/en/stable/auto_examples/image/plot_dataset_gaf.html#sphx-glr-auto-examples-image-plot-dataset-gaf-py) of `pyts`.

## Basic Usage
```shell
python train.py --network odenet --attention no --ode_solver dopri5 --nepochs 50
```

## References
```
@misc{torchdiffeq,
	author={Chen, Ricky T. Q.},
	title={torchdiffeq},
	year={2018},
	url={https://github.com/rtqichen/torchdiffeq},
}

@article{JMLR:v21:19-763,
  author  = {Johann Faouzi and Hicham Janati},
  title   = {pyts: A Python Package for Time Series Classification},
  journal = {Journal of Machine Learning Research},
  year    = {2020},
  volume  = {21},
  number  = {46},
  pages   = {1-6},
  url     = {http://jmlr.org/papers/v21/19-763.html}
}

@inproceedings{bolya2022hydra,
  title={Hydra attention: Efficient attention with many heads},
  author={Bolya, Daniel and Fu, Cheng-Yang and Dai, Xiaoliang and Zhang, Peizhao and Hoffman, Judy},
  booktitle={European Conference on Computer Vision},
  pages={35--49},
  year={2022},
  organization={Springer}
}
```

