# Use the model to predict an image

Now that you can load your model and an image, it's time to pass the image to the model and see what it thinks it's looking at.

However, machine learning models can't actually understand images the way you or I might: They need to see everything as numbers. In the case of an image, that means the amount of red, green, and blue light in every pxiel of the image. So before you can give the image to your model, you'll need to convert it into lists of numbers. Luckily, the TensorFlow and NumPy libraries can help you do this.

--- task ---

Add code to the end of your `predict_image` function that uses the TensorFlow library to convert the image to an array (another name for a list) and then uses NumPy to reshape that array to exactly what the model expects:

```python3
  image = tf.keras.preprocessing.image.img_to_array(image)
  image = np.expand_dims(image, axis=0)
```

--- /task ---

If you want to see what the image looks like to your model, try printing out all those lists of numbers!

Next, you need to ask your model for a prediction based on your image. Convenietly enough, this uses the `predict` method of your model:

--- task ---

Get your model's prediction of the image and store it in a variable named `prediction_result`. 

Note that, as well as passing the model your image, you also have to tell it that it's only reciving one image, using the `batch_size` paramaeter. This is because you can ask the model to predict many images at once.

Add this line to the end of the `predict_image` function:

```python3
  prediction_result = model.predict(image, batch_size=1)
```

--- /task ---

If you print out the results the model has given back, you'll see that it's just lot of numbers. This is a long list of how likely the model thinks the image is to belong to every class it has been trained to recognise. In the case of the VGG16 model you're using here, that's 1000 classes!

Now, since you really only care about the few classifications that the model thinks are most likely — it's probably not confusing our image of a dog with one of a car, for example — the next thing to do is match up the highest of those prediction numbers with the labels for each of the categories. Luckily, yet again, there is a TensorFlow function for that!

--- task ---

Still working at the end of your `predict_image` function, create a variable called `predictions` and then use this rather long TensorFlow function to take `prediction_result` and get the labels for the top 15 results.

```python
  predictions = tf.keras.applications.imagenet_utils.decode_predictions(prediction_result, top=15)
```

--- /task ---

--- task ---

Finally, use the `print_predictions` function I provided to display the predicitons the model has made.

```python
  print_predictions(predictions)
```

Now run the code and see what your program predicts!

--- /task ---

Notice how most of the predictions are sensible — different kinds of dog. However, look at number 13 — 'tennis ball' — that's a bit different! Why might the model think that's what it's seeing? It's probably because of the way models are trained: they're shown images to learn from, and then give other images to test their learning. The image we've asked it to identify here is a dog and some grass. Do you think it's likely some pictures of dogs might show them playing with balls? Or that pictures of balls might show them on grass? You can see how the classifier might get confused!