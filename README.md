# MesoNet
## Requirements

- Python 3.5
- Numpy 1.14.2
- Keras 2.1.5

If you want to use the complete pipeline with the face extraction from the videos, you will also need the following librairies :

- [Imageio](https://pypi.org/project/imageio/)
- [FFMPEG](https://www.ffmpeg.org/download.html)
- [face_recognition](https://github.com/ageitgey/face_recognition)

## Dataset

### Aligned face datasets

|Set|Size of the forged image class|Size of real image class|
|---|---|---|
|Training|5111|7250|
|Validation|2889|4259|

- Training set (~150Mo)
- Validation set (~50Mo)

[Download link for the dataset](https://my.pcloud.com/publink/show?code=XZLGvd7ZI9LjgIy7iOLzXBG5RNJzGFQzhTRy)

## Pretrained models

You can find the pretrained weight in the `weights` folder. The `_DF` extension correspond to a model trained to classify deepfake-generated images and the `_F2F` to Face2Face-generated images.
