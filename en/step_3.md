## Load your model and image
The first thing you need to do is bring in the model you're going to use from the `tensorflow` library. The model you'll be using is called VGG16 and it's very quick to get it into your program.

--- task ---

In the first empty code cell, create a model variable and load the VGG16 model from TensorFlow into that variable.

```python
model = tf.keras.applications.VGG16()
```

--- /task ---

Now that you have a model, you'll need to get an image for it to identify. I've written a function, called `get_image_from_url`, that you can use as part of this. My function will fetch an image from a URL (a web address) and store it in your Google Drive. You need to include it in a larger function which will prepare that image, give it to the model, and then take the model's predictions and print them out into the notebook. For now, you're just going to get the image, load it up, and make sure it looks like you expect it to.

--- task ---

In the second of the three empty code cells create a function called `predict_image` that takes `image_url` as an argument. Have it call `get_image_from_url`, passing the URL to it. Then have TensorFlow load the image and use Matplotlib to display it. 
```python
def predict_image(image_url):
  image_path = get_image_from_url(image_url)
  
  image = tf.keras.preprocessing.image.load_img(image_path, target_size=(224, 224))

  plt.figure()
  plt.imshow(image)
```

--- /task ---

Notice that, at the same time as loading the image, you're tellling TensorFlow to resize it to 224 x 224 pixels, because this is the size of image VGG16 was trained to recognise. This does mean that you should try to use images that are close to square.

--- task ---

In the third empty cell, add a call to `predict_image` and pass it the URL to our test image.

```python
predict_image('https://i.ibb.co/Y2s0WH6/test-dog.jpg')
```

--- /task ---

--- collapse ---
---
title: About the photograph
---

This is a lovely, and almost square, photograph of a dog by Chris Barber, which you can see on the Wikipedia page about dogs. We're able to reuse it here because he shared it under the [Creative Commons 2.0 Attribution](https://creativecommons.org/licenses/by/2.0/) license. 

Creative Commons Attribution licenses allow people to reuse others' work as long as they give credit. When you start producing your own art or code that you want to share online, you should think about how you want to license it too!

--- /collapse ---

--- task ---
Now run all the code by going to the `Runtime` menu and choosing `Run all`. 

You'll need to wait a few seconds for things to load, but you should see your image displayed in the notebook.
--- /task ---
