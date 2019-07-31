# UMSN-Face-Deblurring
Deblurring Face Images using Uncertainty Guided Multi-Stream Semantic Networks

[Rajeev Yasarla](https://sites.google.com/view/rajeevyasarla/home), [Federico Perazzi](https://research.adobe.com/person/federico-perazzi/), [Vishal M. Patel](https://engineering.jhu.edu/ece/faculty/vishal-m-patel/)

[Paper Link](https://arxiv.org/pdf/1907.13106.pdf)

We propose a novel multi-stream architecture and training methodology that exploits semantic labels for facial image deblurring. The proposed Uncertainty Guided MultiStream Semantic Network (UMSN) processes regions belonging to each semantic class independently and learns to combine their outputs into the final deblurred result. Pixel-wise semantic labels are obtained using a segmentation network. A predicted confidence measure is used during training to guide the network towards challenging regions of the human face such as the eyes and nose. The entire network is trained in an endto-end fashion.

## Prerequisites:
1. Linux
2. Python 2 or 3
3. CPU or NVIDIA GPU + CUDA CuDNN (CUDA 8.0)

## To test UMRL:
python test_face_deblur.py --dataroot ./facades/github/ --valDataroot <path_to_test_data> --netG ./pretrained_models/Deblur_epoch_Best.pth

## To train UMRL:
python train_face_deblur.py --dataroot <path_to_train_data> --valDataroot ./facades/github/ --exp ./face_deblur --batchSize 10

- input should be clean image. blurry images for trained are generated by the code it self.


