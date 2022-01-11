# Flood-fill
An algorithm to solve maze

<h2>Problem statement:</h2>
  A maze image,start cell coordinate and end cell coordinate will be provided. We have to find the path. Note that maze is given as an image.(So, image preprocessing stuff is involved here!!). Maze to be considered as 10*10 cells.
<br>
<br>
<b>Given maze:</b>
<br>
<img src="maze00.jpg">
<br>
<h2>Solution:</h2>
<br>
First, lets interpret the maze image. Given is a 3 channel image, walls and boundries are black and free spaces are white. Since the image is a 3d matrix of numbers lets normalize it to 1d matrix for easy processing.
<br><br>
<b>Image normalization:</b>
<br>
Image is converted into single channel, where walls hold 0s and free spaces as 1
<br><br>
<b>Flood fill</b>
<br>
<i>Flood the matrix</i>
The algorithm proceed in the following way,<br>
1.Initialize marker variable value to 0<br>
2.Fill marker value to end cell and increment marker value<br>
3.Fill adjacent cell without wall inbetween with marker value<br>
4.Increment marker value<br>
5.Repeat step 3 and 4 till every cell in the matrix is filled.<br>
<br>

Once I filled the above maze it look like this,<br>
<img src="filled_maze.png"/>
<br><br>

<b>Tracing the path</b>
<br>
Once, The matrix is filled the path can be traced by starting from the intial cell and moving to adjacent cell(Without wall inbetween) which has smallest value.
<br>
So, for above maze<br>
<img src="solved.png"/>

