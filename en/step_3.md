## Load your model and image
First, you need to bring in the model you're going to use from the `tensorflow` library. The model is the set of rules the computer follows to complete a task — in this project a set of rules to decide which object appears in an image. This is called decision classification, and each possible answer — each type of object — is called a class. The model you'll use is called VGG16. VGG16 is trained to recognise a wide variety of objects, and it's very quick to get into your program.

--- task ---

In the first empty code cell, create a model variable and load the VGG16 model from TensorFlow into that variable.

```python
model = tf.keras.applications.VGG16()
```

--- /task ---

Now that you have a model, you need an image for it to identify. A function, called `get_image_from_url`, has been provided for you to use. You need to include `get_image_from_url` in a larger function to get your model's **classifications** of the image and print them out into the notebook.

--- task ---

In the second of the three empty code cells, create a function called `classify_image` that takes `image_url` as an parameter. Have it call `get_image_from_url`, passing the URL to it. Then have TensorFlow load the image and use Matplotlib to display it. 
```python
def classify_image(image_url):
  # Fetch the image from the URL
  image_path = get_image_from_url(image_url)
  # Prepare the image for use by the model
  image = tf.keras.preprocessing.image.load_img(image_path, target_size=(224, 224))

  plt.figure()
  plt.imshow(image)
```

--- /task ---

Notice that, at the same time as you load the image, you tell TensorFlow to resize it to 224 x 224 pixels. That's because this is the size of image VGG16 was trained to recognise. This does mean that you should try to use images that are close to square.

--- task ---

In the third empty cell, add a call to `classify_image` and pass it the URL to the test image.

```python
predict_image('https://dojo.soy/predict-dog')
```

--- /task ---

--- collapse ---
---
title: About the photograph
---

This is an almost square photograph of a dog by Chris Barber, which you can see on the Wikipedia page about dogs. We're able to reuse it here because he shared it under the [Creative Commons 2.0 Attribution](https://creativecommons.org/licenses/by/2.0/) license. 

Creative Commons Attribution licenses allow people to reuse others' work as long as they give credit, like we're doing right here. When you start producing your own art or code that you want to share online, you should think about how you want to license it too!

--- /collapse ---

--- task ---
Now to run all the code, go to the `Runtime` menu and choose `Run all`. 

You need to wait a few seconds for things to load, but you should see your image displayed in the notebook.
--- /task ---

![The output of the code: Text reading 'Downloading data from https://dojo.soy/predict-dog 16384/16291 [==============================] - 0s 1us/step' followed by an image of a dog with numbered axies for the width and height of the image.](images/load_image.png)

--- save ---
