This is a little modification of Corona's default slideview.lua
The origin slideview can only insert table of image as it's data, which
is unconvinient.
This modification based on the design of tableview.lua that user
can write their own "callback" function when creating slideview.
The callback function define how object to be layout. 
So you can insert such as:
data = {
{photo1, photo2, text1, text2}
{photo1, photo2, text1, text2}
{photo1, photo2, text1, text2}
}
as the parameter.

And then in callback function write
callback = function(row1)
	local image1 = display.newImage(row1[1])
	local image2 = display.newImage(row1[2])
	local text1 = display.newImage(row1[3])
	local text2 = display.newImage(row1[4])
end

So you can have many image or text object in one slide.

---

Example:
I have put an Example in this repository: the "main.lua", please follow the step below to test it:
	Step 1: put slideview.lua into the Sample Code directory provided by Corona SDK, renamed as slideview_new.lua
	Step 2: created myPhotos5.jpg to myPhotos8.jpg (duplicate 1~4 or put new images, etc.)
	Step 3: Then run the main.lua, I think it will work. :)

