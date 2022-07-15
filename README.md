ScrollMe uses a simple declarative syntax: just include jQuery + ScrollMe, add some bits to your markup and ScrollMe will do the rest.
Two classes are used to define the elements that ScrollMe works with: scrollme & animateme.

The scrollme class defines a container for animated elements. The progression of the animations is based on the scrolling through this element.

The animateme class defines the animated elements. Any number of these can be added within a container element. These elements also take the options that describe how and when the animation occurs.

Both scrollme and animateme classes can be applied to the same element if desired.

<div class="scrollme">
    <div
        class="animateme"
        data-when="enter"
        data-from="0.5"
        data-to="0"
        data-opacity="0"
        data-translatex="-200"
        data-rotatez="90"
    >
        Yup, that's all.
    </div>
</div>
Compatibility
ScrollMe works fine with just about any up to date browser. It also works in IE10 but if you want support for IE9 you will need to use a polyfill for requestAnimationFrame.

Having trouble?
If ScrollMe isn't doing what you expect it to please post an issue on GitHub. You can also get my attention on Twitter: @nickpearson

Options
Options are added as attributes to scrollme elements with the data- prefix.

when
Determines when the scrolling boundaries start and end.

"enter": From when the top of the container enters the viewport to when it exits.
"exit": From when the bottom of the container enters the viewport to when it exits.
"span": From when the top of the container enters the viewport to when the bottom exits.
from & to
Specifies the position within through the scrolling boundaries at which the animation starts and ends. The animated properties are set to their default value up to the from position then transition to the value defined in the options as scrolling progresses to the to position.

It is important to note that the from value can be larger than the to value. This would typically be the case if elements are being animated as they enter the viewport.

Value: 0 – 1

easing (optional)
Sets the easing function to apply to the animation.

"easeout": Starts abruptly and comes to a gradual stop (default).
"easein": Starts gradually and comes to an abrupt stop.
"easeinout": Starts and comes to a stop gradually.
"linear": No easing.
crop (optional)
Limits the effect scrolling boundaries to the boundaries of the document. Leaving the boundaries uncropped allows elements to remain unaffected by enter effects when they are near the top of the page or, vice versa, by exit effects near the bottom.

"true": Crops scrolling boundaries to fit within the document boundaries (default).
"false": Allows scrolling boundaries to exist outside the document boundaries.
opacity (optional)
Specifies the opacity of the animated element when scrolling arrives at the the to position.

Value: 0 – 1

scale, scalex, scaley & scalez (optional)
Specifies the scale of the animated element (optionally along the X, Y & Z axis) when scrolling arrives at the the to position.

Value: Scaling factor

rotatex, rotatey & rotatez (optional)
Specifies the angle of rotation of the animated element along the X, Y & Z axis when scrolling arrives at the the to position.

Value: angle of rotation in degrees

translatex, translatey & translatez (optional)
Specifies the distance to translate the animated element along the X, Y & Z axis when scrolling arrives at the the to position.

Value: distance in pixels

A jQuery plugin for adding simple scrolling effects to web pages.

Demo and usage guide: http://scrollme.nckprsn.com.

Play with it on CodePen: http://codepen.io/nckprsn/pen/IGpmc
