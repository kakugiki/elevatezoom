[jQuery Zoom Plugin](http://www.elevateweb.co.uk/image-zoom/)
================================

elevateZoom - A jQuery image zoom plugin


## Getting Started

Include jQuery and the plugin on a page. Include your images and initialise the plugin.

```html
<img id="zoom_01" src='images/small/image1.png' data-zoom-image="images/large/image1.jpg"/>

<script>
    $('#zoom_01').elevateZoom();
</script>
```

For more information on how to setup and customise, [check the examples](http://www.elevateweb.co.uk/image-zoom/examples).

## Bug
```
self.zoomContainer = $('<div class="zoomContainer" style="-webkit-transform: translateZ(0);position:absolute;left:' + self.nzOffset.left + 'px;top:' + self.nzOffset.top + 'px;height:' + self.nzHeight + 'px;width:' + self.nzWidth + 'px;"></div>');
			$('body').append(self.zoomContainer);
```
There is a bug in above code if used with carousel, it will keep appending a new div.zoomContainer.
A quick fix is to remove the div before calling the zoom function: ```$('.zoomContainer').remove();```

## License
Copyright (c) 2012 Andrew Eades
Dual licensed under the GPL and MIT licenses.
