# Travel-Photo-Gallery
 Using Jquery to pop up pictures
 
The project is accesible at : https://kapilgautamin.github.io/Travel-Photo-Gallery/

This project builds a photo gallery using jQuery for your travel photo sharing site as shown in following picture.
When the document is loaded, an AJAX call is made, downloads the data.json file (it contains an array of image objects) and display images on a html page. When the user hovers over the image, you will show the larger version of the image along with the caption. See instructions for details.

Main Points:
1. The images are supplied in two folders: images/square (for the gallery) and images/medium (for the popup).

2.	Loop through the images array and using the appropriate jQuery DOM methods, add the appropriate `<img>` tags to the supplied `<ul class=“gallery”>` element. The image filenames are contained in the path property of each image object. Set the alt attribute of each `<img>` to the title property of the image object.

3.	Use jQuery to attach handlers for the mouseenter, mouseleave, and mousemove events of the square images in the gallery.

4.	For the mouseenter event, use jQuery to add the “gray” class to the square `<img>` under the mouse.

5.	Also for the mouseenter event, using jQuery to generate a `<div>` with an `id=“preview”` (the styling for #preview is defined in gallery.css). Within that `<div>` add an `<img>` element that displays the larger version of the image. Underneath that `<img>` add a `<p>` element for the caption (image title, city and date taken). The alt attribute of the square image under the mouse contains the image title. 

6.	Query is used to set the left and top CSS properties for the `#preview<div>`. We can retrieve the x, y coordinates (via the pageX and pageY properties) of the current mouse position from the event object that is passed to the event handler. We can calculate the new position by offsetting by some amount from the mouse x, y position.

7.	Finally, once the `#preview <div>` is constructed, simply append it to the <body>.

8.	For the mouseleave event, remove the “gray” class from the square image under the mouse. Also remove the `#preview<div>` from the body.

9.	For the mousemove event, simply set the left and top CSS properties for the `#preview <div>` using the same approach as described in point 6.
