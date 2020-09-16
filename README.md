# python-PIL-module

When using PIL, we typically create Image objects that hold the data associated with the images that we want to process. On these objects, we operate by calling different methods that either return a new image object or modify the data in the image, and then end up saving the result in a different file.

The resize method that returns a new image with the new size, and then we save it into a different file. 
For example, if we wanted to resize an image and save the new image with a new name, we could do it with:

`from PIL import Image`<br>
`im = Image("example.jpg")`<br>
`new_im = im.resize((640,480))`<br>
`new_im.save("example_resized.jpg")`

If we want to rotate an image, we can use code like this:

`from PIL import Image`<br>
`im = Image("example.jpg")`<br>
`new_im = im.rotate(90)`<br>
`new_im.save("example_rotated.jpg")`

We can combine the above operations into just one line that rotates, resizes, and saves:

`from PIL import Image`<br>
`im = Image("example.jpg")`<br>
`im.rotate(180).resize((640,480)).save("flipped_and_resized.jpg")`
