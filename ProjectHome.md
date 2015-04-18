# jsMovie #
Inspired by some transparent flash animations all over the web, I decided to have something other then flash to get similar results. So i created a jquery-plugin to animate image sequences.

## Changes ##
Current Version 1.4.4
  * added the possibility to set performStop in the settings
  * fixed some miner issues
  * it's now possible to write an angular directive for jsMovie
1.4.3b
  * fixed some spelling (I'm german)
  * added comments to all methods
  * added an extra parameter to the play method. now its possible to let the movie only pause and not stop after the animation has finished. was requested by a lot of users that would use the tool for 3D animations
1.4.2
  * added a performStop value in the play method -> when ending a movie you can now pause by setting it to false and stop on true
  * better documentation of the source code in the uncompressed file

1.4.1
  * fixed a bug where adding a clip staring from frame 1 didn't work
  * new default for showPreLoader is false

1.4.0
  * introduced clips
  * fixed preloader bug
  * fixed setting object from being overwritten

## Website ##
Checkout the official [Website](http://jsmovie.burkhardt-medienproduktion.de) an get some nice [examples und tutorials](http://jsmovie.burkhardt-medienproduktion.de/?page=tutorial).

## Documentation ##
Find the documentation in the uncompressed javascript file

## Example ##
Find an example in the download section.

html code:
```
<html>
    <head>
        <script type='text/javascript' src='jquery.jsmovie.min.js'></script>
    </head>
    <body>
        <div id='movie'></div>
        <div id='play'>play</div>
        <div id='stop'>stop</div>
        <div id='pause'>pause</div>
    </body>
</html>
```

js code:
```
$(document).ready(function(){

    $('#movie').jsMovie({
        sequence: 'animation####.jpg',
        from: 1,
        to: 120,
        folder : "ani/",
	height:200,
        width:300,
        loader: {path:"img/preloader.png",height:50,width:50,rows:2,columns:4},        
    });

    $('#play').click(function(){
        $('#movie').jsMovie('play');
    });

    $('#stop').click(function(){
        $('#movie').jsMovie('stop');
    });

    $('#pause').click(function(){
        $('#movie').jsMovie('pause');
    });

});
```