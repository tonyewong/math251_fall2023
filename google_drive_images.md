### Embedding images from Google Drive

The need for the local file path poses a problem when you share notebooks with others (say, your lab partner, or instrutor) because you only really want to share your ipynb Jupyter notebook file. You don't want to need to keep track of all kinds of auxiliary files for images to embed because that would be very annoying.

Instead, we can be slick!

We can include images via an internet URL by replacing the local file path in parentheses above with a URL. You can get image URLs by right-clicking on an image and clicking "Copy image address". If you have your images on a server somewhere, great. If not, have no fear, as with many aspects of life, Google Drive is here to help.

You can get share links for items in your Google Drive in the usual way (right click, Get shareable link). If you go this route, be sure to change the settings so that *anyone* with the link can view, not just people at RIT.

Now, simply replacing the URL or local file path with the Google share link will **not** work. Suppose that for an image I want to embed in this Jupyter notebook, the full share link as copied out of Google Drive is [https://drive.google.com/file/d/1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ/view?usp=sharing](https://drive.google.com/file/d/1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ/view?usp=sharing).

I can include this image by taking the *file ID* of this file, prepending it with `https://docs.google.com/uc?export=download&id=`, and inserting *that* string within the parentheses for the image file. The file ID is the string of characters between the forward slashes after the `/d/` in the share link.  So, the file ID for my image is the string `1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ`.

To include the image, I would use the syntax below. Double click on the image itself to see this in action.

`![strange planet](https://docs.google.com/uc?export=download&id=1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ)`

![strange planet](https://docs.google.com/uc?export=download&id=1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ)

"Damn!" You might say, "That is a really large image! Is there some way to adjust the size?"

What a good question you have asked! There is.

We can use HTML code within Jupyter notebooks in order to have more control over the formatting of both images and text. To adjust the image to have a width of 500 pixels, we can use the HTML `img` command as shown below. Note that the URL used is the same as with the Markdown `![]()` syntax. Double click on this cell to verify that this is not deception.

`<img src="https://docs.google.com/uc?export=download&id=1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ" width="500px"/>`

<img src="https://docs.google.com/uc?export=download&id=1iy4EQQZy0jfhYlHDys1uQAS5wf2hXGmZ" width="500px"/>

