# Animal_Faces_Detection_Projects
Using OpenCV (Haar Cascade Classifier), Deep Learning (Yolov5) with own dataset and with pre-trained method

**This project is about detecting animal faces using 5 different methods which are :**

1.) **Using Haar_Cascade_Classifier**
Colab file name --> Option1_OpenCV_Haar_Cascade_Classifier(GitHub).ipynb
Based on the testing after train the model, it able to detect pos8.jpg as animal. It unable to detect the fake frog image (pos2.jpg). It also unable to detect some of the 
animal faces. Based on the bounding box on detected images, it shows that this model not only focusing on the animal face image but it's checking the entire image for animal 
detection as well as including the face checking. This model didn't detect any negative images as positive image (detected image). Since i only used 20 positive images, the
model is not so consistent like pre-trained model (which was trained with huge datasets).However, pre-trained model uses MS-COCO datasets and only able to detect 10 animals. 
It doesn't only focus on face of an animal, it checks the entire image.

2.) **Using Yolov5 (Pytorch)**
Colab file name --> OpenCv_(YOLOv5)Deep_Learning(Option2)_GitHub.ipynb
Based on the testing the model able to detect pos1_val.jpg and pos6.jpg animal face. But didn't detect pos5.jpg which is also an animal image. It also didn't detect the fake 
frog image pos2_val.jpg. Since I only use 20 positive images (animal images) and 20 negative images (background images), the model looks like not consistent. I also used the 
same image that I used to train this model for detection but unfortunately pos5.jpg is not detected but pos6.jpg is detected. However, the model didnt detect any negative
images (background images) as a positive image.

3.) **Using Pre-trained Models for Animal Detection, using OpenCV’s deep learning module (dnn) with pre-trained models YOLO.**
Colab file name --> Option3_DNN_YOLOv8n_(GitHub).ipynb
Based on the experiment, we are using coco.names pre-trained data. After loading images in content/ , the image file will be processed and saved into content/positives or 
content/negatives folder. Based on the testing, this model detection is not working well because some of the background (negative images) save into positive directory 
(content/positives). In conclusion, this model doesn't work well.

4.) **Using Yolov5 )Pre-Trained model , data=coco128.yaml**
Colab file name --> Pre_Trained(YOLOv5)_(GitHub).ipynb
Based on this experiment, this pre-trained model not focusing on detecting animal faces but it detects the whole animal image and gives the results. This pre-trained model is
not perfect because it detects pos4.jpg ( a tiger) as zebra. Pre-trained model using MS-COCO dataset which only can detect dog, cat, horse, sheep, cow, elephant, bear, zebra,
giraffe and bird. This pre-trained model able to detects pos1.jpg (a dog) and pos3.jpg (a zebra) accurately.

5.) **Using YOLOv8 pre-trained with Detection Api**
Colab file name --> Pre_Trained_Yolov8_Object_Detection_API(GitHub).ipynb
Based on this pre-trained model results, it detects pos1.jpg (a dog) and post15.jpg (a bear). However, it unable to detect pos2.jpg (fake frog image). It also detects
post18.jpg (a koala) as a giraffe. It's not consistent because it only able to detect few animals. Pre-trained model using MS-COCO dataset and only able to detect dog, cat, 
horse, sheep, cow, elephant, bear, zebra, giraffe and bird. This model checks whole image for animal detection, it does not only focus on animal faces.

Dataset
About 20 positive images and 20 negative images collected. 
The dataset were prepared together with dimension of the bounding box (which covers the faces of animals). This dimension of bounding box important to be used in 
Haar_Cascade_Classifier and Yolov5 Deep Learning using Pytorch. The file which contains the dataset is --> 
Image_Size(Dataset)_for_Deep_Learning_Yolov5_and_Haar_Cascade_Classfier(GitHub).ipynb
