# Experiment with your program

Now that you have a working program to identify images, it's time to have some fun with it!

--- task ---

Try loading a few different images into it to see what predictions it makes. You'll have to use images hosted on the internet. You can use [imagebb](https://imgbb.com/) to put your own images online and then supply the 'direct links' URL to your program. 

![The imagebb link window, with 'direct links' selected and a link URL displayed in the text box below.](images/direct_links.png)

You'll also have to make sure they're `.jpg` files, or modify the `get_image_from_url` function I supplied.

--- /task ---

--- task ---

Once you've done that a few times, and gotten an idea of how good the model is, you can try a different one to see how important it is to have a good model for the job. VGG16 is a big, well-trained model. MobileNetV2 is well trained too, but it's designed to run on a phone instead of a PC, so it's a lot smaller and less powerful. You can try it out by changing the line where you load your model and then re-running everything. This is the change you need to make:

```python
model = tf.keras.applications.MobileNetV2()
```

See what MobileNetV2 thinks our test dog picture is!

--- /task ---

Now that you've got a tool to use your image classification models with, you can move on to creating your own model in [Project 2](#).