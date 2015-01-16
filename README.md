#ComboStars

ComboStars is a jQuery plugin that replaces combo boxes (selects) with star widgets that users can use to provide ratings.

##Using ComboStars

First, include the library.

```
<script src="/path/to/jquery.combostars.js"></script>
```

Next, invoke ComboStars on whatever selects you want to turn into star ratings.

```
$('select').combostars(params);
```

##Parameters

ComboStars requires that you specify a path to the image file that defines the stars. The star file should have two components: a filled-in part and an outline part. These pieces are used for star rendering. The filled-in part should be on top. The (absolute) path to this image should be passed as the ```starUrl``` parameter.

If you use a custom star file, you may also need to specify the width and height of the star image. These, respectively, are passed as integers to ```starWidth``` and ```starHeight```. By default, ```starWidth``` is 16 and ```starHeight``` is 15.

##Select Value

When a user clicks on the nth star, the value of the nth ```<option>``` is assigned to the select. This is one-based. That is, if the user clicks the third star and the value of the third ```<option>``` is "three," then ```select.val()``` will return "three."

##Events

ComboStars does not forward any events from the stars to the select except for ```change```.
