# Classify your own image
Now that you have a working program to identify images, it's time to have some fun with it!

You're going to load a few different images into the program to see what predictions it makes. You'll have to use images hosted on the internet, but you can use your Google Drive to store an image online.    

--- task ---

Go to [drive.google.com](https://drive.google.com/) and drag an image from your computer to the drive. Wait for it to finish uploading.

--- /task ---


--- task ---

Once the image is in drive, right-click on it and choose **Get shareable link**. 

![The Google Drive 'Get link' dialogue.](images/get_shareable_link.png)

--- /task ---

--- task ---

In the dialogue box that opens, change who has permission to view the image from **Restricted** to **Anyone with the link**.

![The Google Drive 'Get link' dialogue, with the permissions menu open.](images/link_permissions.png)

--- /task ---

--- task ---

There should now be a link highlighted in the dialogue box.

![The Google Drive 'Get link' dialogue, showing that anyone with the link can access the file. The link to the file is highlighted.](images/link_updated.png)

In this link you can find the ID code for the file between `/d/` and `/view?usp=sharing`. It should look something like this:

```
1xunlhWWxA6e59gSL_gTo_CiZYBNqbMDy
```

Copy this ID.

--- /task ---

--- task ---

Use the ID you have just copied to complete this URL, inserting it in place of `[IMAGE ID]`:

```
https://drive.google.com/uc?export=download&id=[IMAGE ID]
```

You should get something like this:

```
https://drive.google.com/uc?export=download&id=1xunlhWWxA6e59gSL_gTo_CiZYBNqbMDy
```

--- /task ---

--- task ---

Now paste the URL you have created as a parameter to the `predict_image` function call in your program, and see how your program classifies the image!

--- /task ---
