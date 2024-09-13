# Image-uploader-website-project
Image uploading is one of the main features of any modern web-applications. It allows the user to upload the image or picture on the server.


## Upload Images to Django : 
Most of the web applications deal with the file or images, this project consists of two model fields that allow the user to upload the images and files. These fields are **ImageField** and **DateTimeField**; basically ImageField is a specialized version that uses Pillow to confirm that file is an image.

#### models.py
We create the Image model that consists of two fields - photo and date. The image field will work as Django's file storage API. This API provides the facility to store and retrieve the files and also read and write them. The upload_to parameter specifies the file location where the image will be stored.

#### settings.py
Base url to serve media files  
MEDIA_URL = '/media/'  
  
Path where media is stored  
MEDIA_ROOT = os.path.join(BASE_DIR, 'media/')  

MEDIA_URL - It will serve the media files.

MEDIA_ROOT - It specifies the path of the root where file will be stored.

#### forms.py
The advantage of creating the Django model form is that it can handle the form verification without declaring it explicitly in the script. It will also create the form fields on the page according to the model fields mentioned in the model.py file.

To display this form, we need to create the **home.html file** under the template folder.

#### views.py
When we upload the image, the post request will be generated. The form is automatically validated and saved in the media folder. 

## Output
![image alt]https://github.com/Manideep1825/Image-uploader-website-project/blob/bfc8890872eb2cfb91f828bcc43cc43e5aa8421d/Screenshot%201.png

## Conclusion
This project provides the simple interface to perform image or file uploading. We just need to do some configuration and define an ImageField in the model form's field. We can also upload any file (.xml, .pdf, .word, .etc) by following the same procedure, but we will need to convert ImageField to FileField in the model's field.



