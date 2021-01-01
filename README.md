# Pix2Pix GAN for image to image translation
#### a Generative adversial network to investigate cGANs as a genral all purpose solution o differen types of image to image translation problems.

### Introduction

**Image-to-Image Translation**: The process of translating one possible representation of a scene into another.
Some examples: edges to photo, aerial image to map, semantic labels to photo

### Methodology 
- **Generator**: Its goal is to generate realistic-looking fake data that match their labels.
- **Discimantor**: Its goal is to distinguish between fake example-label pairs coming from the Generator and real example-label pairs coming from the training dataset.
- For the cGAN, he generator follows a **U-Net** architecture whereas the discriminator follows a **PatchGAN** architecture.


### Dataset
- In the Original paper, experiments are performed on 6 datasets
- This implementation is done on **Cityscapes** and **Maps**
- Both datasets are avavailable in Pix2Pix-cGAN-Keras/Assets/datsets
  -**cityscapes**
    -train
    -val
  -**maps**
    -train
    -val
- The dataset contains images wih 2 halvs, input image along with it's expected output
- **Maps** : Map <-> Aerial Photo 
- **Cityscapes** : Semantic Labels <-> Photo



### Respository Structure
Note: The model was trained and results were calculated on colab

- Do not change the names of the folders as code **pix2pix.ipynb** follows same naming convention.
- Upload the folder **Pix2Pix-cGAN-Keras** on your google drive
  -The google drive link for the whole folder:
  -https://drive.google.com/drive/folders/1WKSymZRCmlTAOFgQN7zh-uVOO672k8mx?usp=sharing
- Only **Assets** folder is uploaded on github. The rest is available on the google drive link
- The directory should look like 
  - **Assets** folder: **/content/drive/My Drive/Pix2Pix-cGAN-Keras/Assets**  
  - **models** folder: **/content/drive/My Drive/Pix2Pix-cGAN-Keras/models**
- Open and run the **pix2pix.ipynb** on colab
- Compressed Dataset saved at Pix2Pix-cGAN-Keras/Assets/
  - **cityscapes.npz**
  - **maps.npz**
- models are saved after every 10 epochs in the models folder mentioned above
- change location if training the model, use model .hp5 files if using the pre trained model value
- option to resume training using a saved model file in the code
- Generated Result images at 
  - Pix2Pix-cGAN-Keras/Assets/Plots/cityscapes
  - Pix2Pix-cGAN-Keras/Assets/Plots/maps

