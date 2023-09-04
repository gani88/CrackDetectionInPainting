# Painting Digital Restoration using Convolutional Neural Network
## This repository is for University Final Project.

Restoration of old artworks that have been degraded and the age of the artwork has made some artworks difficult to recognise, especially paintings. In paintings, there are factors that must be
considered in detecting damaged parts or parts that have cracks. The application of traditional crack detection methods cannot work effectively because these traditional methods cannot accurately detect paintings that have been converted to higher resolutions and paintings that have been converted to other forms, such as conversion into infrared or negative paintings. There are some paintings that have complex patterns and compositions, which in turn will make the crack detection process more difficult.
In this research, the method used to perform digital restoration is Convolutional Neural Network based on Image Classification to detect cracks more accurately and another method is General Adversarial
Network (GAN) which has two networks namely Generative Network and Discriminant Network. The crack detection method provides two models that have different accuracy and loss where the highest
accuracy results in 98% and the lowest loss at 6%. The GAN method provides results that are close to the original painting and increases the resolution of the painting image. In this study, it is concluded
that the use of crack detection methods without Custom Preprocessing (Image Transformation) provides better results and the GAN method provides good restoration results if the painting has facial objects. The use of larger and varied datasets and dataset augmentation is needed to perform restoration on more and wider objects.

Keywords: Convolutional Neural Network, Image Classification, General Adversarial Network,
Generative Network, Discriminant Network


### Dataset
1.	Data yang digunakan pada penelitian ini bersumber dari beberapa arsip online yaitu Web Gallery of Art (https://www.wga.hu/index1.html) dan ArtCyclopedia (http://www.artcyclopedia.com)
2.  Lukisan yang digunakan untuk dataset merupakan lukisan dari abad 14 - abad 16.

![image](https://github.com/gani88/CrackDetectionInPainting/assets/79634101/7834880f-7e47-4597-9bbb-5425076b2f5c)

### Dataset Preprocessing
Each data (raw image) will undergo a transformation process using the custom_preprocessing function. This function will enhance the contrast of cracks in the painting using one of the morphological operations, namely the top-hat transformation. Subsequently, a dilation operation will be applied to increase the boundaries of the cracks in the painting, making them easier to detect and more visible. This will be particularly helpful for paintings with small and transparent cracks.

![image](https://github.com/gani88/CrackDetectionInPainting/assets/79634101/c2452a18-ebba-47f4-ae71-f7bbe3986750)

### Model Architecture
![image](https://github.com/gani88/CrackDetectionInPainting/assets/79634101/f3855ccd-7391-4293-952e-065a66c5b0cc)

### Result
This is result from the model, accuracy and loss.
![image](https://github.com/gani88/CrackDetectionInPainting/assets/79634101/06425a3f-14d2-4d8b-bc7d-4b15ed4737cd)


Next is result from restoration.
![image](https://github.com/gani88/CrackDetectionInPainting/assets/79634101/0a4c9677-ae9e-4663-9bbf-00198a568aaa)

# Conclusion
This project provides two models used in the digital restoration of old paintings using Convolutional Neural Network algorithms. In this study, the first model is a detection model for cracks in old paintings, which has two versions resulting in different accuracy and loss outcomes. In this research, the second version performs better compared to the first version. In the second version, the model does not use Custom Preprocessing, resulting in higher accuracy and minimizing loss compared to the first version.

Next, the second model, a GAN model, is used for restoration and patching of paintings that were detected to have cracks by the first model. The model produces good results in restoring paintings while simultaneously improving the resolution of the painting after patching the damaged areas. However, the model performs well only on paintings that contain human faces, and it cannot perform better in restoration if human faces are absent in the painting.

For future research, it is recommended to enhance the restoration results for paintings with cracks by improving the model's ability to detect objects other than human faces. This improvement can be achieved by training the pretrained model on a larger dataset that includes objects other than human faces. Additionally, augmenting the dataset is necessary to increase the data's diversity and coverage.
