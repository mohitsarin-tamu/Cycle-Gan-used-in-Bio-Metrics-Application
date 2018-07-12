Generative adversarial networks are generative models which have
achieved great success in unsupervised learning in various fields including
image generation, image styling, in-painting and 3D object generation. My
aim through this project was to understand how generative adversarial
networks (GANs) work and implement the same to some bio-metrics
dataset of finger , plam and the techniques used to make it better. We
were trying to make a new type of model which can distinguish better pairs
of images of bio-metrics data of two different persons.

Divide datasets as Train A and Train B , Test A and Test B accordingly.
Datasets are stored in horse2zebra folder as Train A , Train B , Test A , Test B.
Checkpoints will be made and saved accordingly.


Prerequisites:
tensorflow r1.1
numpy 1.11.0
scipy 0.17.0
pillow 3.3.0


Train a model:
CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=horse2zebra
Use tensorboard to visualize the training details:
tensorboard --logdir=./logs
Test
Finally, test the model:
CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=horse2zebra --phase=test --which_direction=AtoB
Training and Test Details
To train a model,

CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=/path/to/data/ 
Models are saved to ./checkpoints/ (can be changed by passing --checkpoint_dir=your_dir).

To test the model,

CUDA_VISIBLE_DEVICES=0 python main.py --dataset_dir=/path/to/data/ --phase=test --which_direction=AtoB/BtoA
