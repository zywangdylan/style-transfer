## Style Transfer of Images and Videos

### Introduction
In this repository, we implement style transfer and analyze various design choices in the algorithm, which is important for learning from the artistic styles of existing artworks and generating new visually pleasing results. We implement two versions of style transfer. The first version requires a long runtime for images with high resolution. We explore many possible solutions and implement the second version that provides a significant speedup. We are able to efficiently stylize high resolution on GPU and scale up to stylizing videos, which requires transforming a large number of frames of the videos.

### For Developers
#### Setup 🛠
1. Clone the repository
2. Upload the folder `style_transfer` you just cloned to your Google Drive/Colab under the path `/content/drive/MyDrive/`
3. Open the notebook `Version1_NST.ipynb` or `Version2_NST.ipynb` in Colab
4. Run the code in the notebook 🚀

#### Usage


