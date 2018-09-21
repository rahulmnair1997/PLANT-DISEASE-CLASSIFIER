# ImageClassification-Server
Image classification with Web API and UI.<br>
It's is written in Django along with Tensorflow uing [Google's Inception v3 model]<br>
The web interface is made using materializecss and jQuery<br>
It is extension of [this](https://github.com/DeepBlueCitzenService/Tensorflow-Server) project.

## Usage

To run the server on localhost:

```
$ pip3 install -r requirements.txt
$ python3 manage.py collectstatic
$ python3 manage.py runserver
```

#### Input
you need to send either 'image' or 'image64' of leaves of tomato since only this model has been currently been trained on tomato dataset. It can furthr be improved by trained it with more classes.

#### Result
Parameter    | Type                | Description
------------ | ------------------- | --------------------------------------------
success      | bool                | Whether classification was sucessfuly or not 
confidence   | category, float     | pair of category and it's confidence

Note: *category* is not paramater name but string of the category.<br> 
Example:  {"success": true, "confidence": {  "mongoose": 0.87896, "hare": 0.00123 }}


## Using Retrained Inception Model
* Retrain the model using your images. Refer [here](https://www.tensorflow.org/tutorials/image_retraining).
* [Fork](https://github.com/CCD-1997/image-classify-server#fork-destination-box) this repo
* Replace the generated graph and label files in `/classify_image/inception_model/`
* Deploy the Django project

## Contribute
I am just beginner. If you find any bugs or want to improve the project, fell free to do it uisng pull request. And I have used various resources, even files from some github repositories, like image classify server, etc.
