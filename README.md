# Google Colab

The goal of these [Google Colab](https://colab.research.google.com/) notebooks is to catpure the distribution of Steam banners and sample with a DCGAN.

## Usage

-   Run `download_steam_banners.ipynb` to download Steam banners.
-   Run `GAN.ipynb` to train one of the suggested GANs, preferably DCGAN, to generate Steam banners.

## Results

The dataset consists of 27,974 Steam banners with RGB channels and resized from 460x215 to 28x28 resolution.
For faster computations, the dataset is aggregated and stored as a NumPy structure (`.npy`) in a folder called `data/`.
 
A DCGAN model was trained for 500,000 updates with a mini-batch size of 128, which is about 2,300 epochs.
After the training is done, the generator and discriminator networks are stored as `.hd5` files in a folder called `checkpoints/`.

NB: A zip archive with 31,723 Steam banners, saved as .jpg files, with RGB channels and resized to 128x128 resolution,
is also [provided](https://drive.google.com/open?id=1YLhdwgnhyP-eC4gHOmTsmuiUSr0XN5XJ). The data comes from [another of my Github projects](https://github.com/woctezuma/download-steam-banners) based on Steam API instead of SteamSpy API.
This dataset is not used here, due to constraints of Google Colab (available RAM, and computation time before the hosted 
runtime is at risk to be killed), but it could be used in future projects such as StyleGAN for which image size is 
expected to have square proportions and to be a power of 2.

### Generated Steam banners

Results obtained with different numbers of iterations are shown [on the Wiki](https://github.com/woctezuma/google-colab/wiki).

A grid of generated Steam banners after 500,000 iterations: [4k display](https://github.com/woctezuma/google-colab/wiki/4k/500000_no_clip.png)
![Generated Steam banners after 500,000 iterations](https://github.com/woctezuma/google-colab/wiki/4k/500000.png)

### Real Steam banners

A grid of real Steam banners: [4k display](https://github.com/woctezuma/google-colab/wiki/4k/real_steam_banners_no_clip.png)
![Real Steam banners](https://github.com/woctezuma/google-colab/wiki/4k/real_steam_banners.png)

## References

-   [Goodfellow, Ian, et al. "Generative adversarial nets." Advances in neural information processing systems. 2014.](https://arxiv.org/abs/1406.2661)
-   [Radford, Alec, et al. "Unsupervised representation learning with deep convolutional generative adversarial networks." 2015.](https://arxiv.org/abs/1511.06434)
-   [Keras implementations of Generative Adversarial Networks (GAN)](https://github.com/eriklindernoren/Keras-GAN)
-   [Implementation of Deep Convolutional GAN](https://github.com/Newmu/dcgan_code)
-   [Image Completion with Deep Learning in TensorFlow, in 2016.](http://bamos.github.io/2016/08/09/deep-completion/)
-   [StyleGAN](https://github.com/NVlabs/stylegan)

