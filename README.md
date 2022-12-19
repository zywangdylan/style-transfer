## Style Transfer of Images and Videos

### Introduction
In this repository, we implement style transfer and analyze various design choices in the algorithm, which is important for learning from the artistic styles of existing artworks and generating new visually pleasing results. We implement two versions of style transfer. The first version requires a long runtime for images with high resolution. We explore many possible solutions and implement the second version that provides a significant speedup. We are able to efficiently stylize high resolution on GPU and scale up to stylizing videos, which requires transforming a large number of frames of the videos.

### For Developers
#### Setup 🛠
1. Clone the repository
2. Upload the folder `style_transfer` you just cloned to your Google Drive/Colab under the path `/content/drive/MyDrive/`
3. Open the notebook `Version1_NST.ipynb` or `Version2_NST.ipynb` in Colab
4. Modify configurations and paths according to the detailed instructions below 
5. Run the code in the notebook 🚀

#### Version 1
The first version of style transfer is implemented in the notebook `Version1_NST.ipynb`. 

Several reminders to run the code in the notebook:
1. **Colab or Local Machine?** The notebook is designed to run on Google Colab. You can run the code on your local machine, but you need to install the required packages and change the path to the dataset.
2. **GPU or CPU?** The notebook is able to run on GPU. You can change the runtime type to GPU in the notebook. CPU is also supported, but it will take a long time to run the code.
3. **Path?** By default, `ROOT = '/content/drive/MyDrive/style_transfer'` will be the correct path to the folder `style_transfer` you cloned from the repository. If you run the code on your local machine or put the folder elsewhere in Google Drive, you need to change the path to the folder `style_transfer`.
4. **Image Sizes?** In this version, you are able to transform the images up to 1024x1024 for GPU and 512x512 for CPU. If you want to run the code on images with different sizes, you need to change the `gpu_output_image_size` and `cpu_output_image_size` in the notebook.

#### Version 2
The second version of style transfer is implemented in the notebook `Version2_NST.ipynb`.

1. **Configs** To better support the stylization of images and videos, we implement a config cell to store the parameters of the algorithm. You can change the parameters, such as `MODE`, path, weights, in the config cell and run the code in the notebook.

2. **Takes a while to run?** Yes, it will take a while to run the code when downloading COCO dataset and training the model. If you want to have a quick look at your stylized images, you can change the `MODE` to `IMAGE`, setup your Image Style Transfer Configs and run the code in the notebook. The result image will be waiting for you in the folder `images/result_images`. 

3. **Folder structure?** Please keep the folder structure the same as the way shown below so that you don't need to configure most of the paths in the notebook.
    ```
    .
    ├── images                                    # Image folder
    │   ├── content_images          
    │   ├── style_images        
    │   └── result_images
    ├── videos                                    # Image folder 
    │   ├── content_videos                
    │   └── result_videos
    ├── training_checkpoints                      # Folder to save model checkpoints
    ├── trained_transformations                   # Trained weights of styles
    ├── pretrained_loss_network                   # Folder to save pretrained weights of backbones
    ├── Version2_NST.ipynb
    └── Version1_NST.ipynb
    ```


### Report
If you are curious about the logic of the algorithm, report is ready for you in `final_project_report.pdf` with detail explanation and evaulations.

**Happy Painting!** 🎨
