# Projectors Have Worse Contrast Ratio Than OLED Panels

The contrast of OLED is between 10x and 100x that of a projector.

When an OLED pixel is off, it reflects ambient light to some degree, but OLED panels are black and have
an anti-glare polarizer that dramatically attenuates scattered ambient
light. When that same OLED pixel goes on at full brightness, we see the light
it emits, plus the small amount of glare from when it was off. Here is the contrast of a
display panel:

~~~
Intensity when pixel is off = ambient light * panel reflectance
Intensity when pixel is on = Intensity when pixel is off + Intensity from pixel
Contrast = Intensity when pixel is on / Intensity when pixel is off 
         = 1 + intensity from pixel / (ambient light * panel reflectance)
~~~

Because the panel reflectance is very low for OLED displays, this ratio is very large.

With projectors, when a pixel is off, the screen scatters the ambient light.
When the pixel turns on, we see the scattered ambient light plus the light from
the projector.  Here is the contrast calculation for a projector assuming a
Lambertian screen (sometimes called a screen with “gain 1.0”):

~~~
Intensity when pixel is off = ambient light * screen reflectance
Intensity when pixel is on = Intensity when pixel is off + light from projector * screen reflectance
Contrast = Intensity when pixel is on / Intensity when pixel is off 
         = 1 + light from projector / ambient light
~~~

Unlike OLED panels, the reflectance of the screen has no effect on contrast. A
diffuse white screen offers the same contrast as a gray one. In these
calculations, I’ve assumed an off pixel emits no light at all. In reality,
projectors leak a significant amount of light for off pixels, further impairing
contrast. 

Inside a typical home, where the ambient light is around 100 lux, the contrast
for a projector is around 40:1
[citation](https://octaneseating.com/blog/lighting-home-movie-theater/). In
that setting, an OLED display on a phone would exhibit a contrast ratio of
500:1, and a TV’s OLED display would exhibit a contrast ratio of 2000:1
[citation](https://opg.optica.org/oe/fulltext.cfm?uri=oe-25-26-33643&id=380371).

These observations are inherent to projection. Sadly, improvements in light
engines won’t yield better contrast ratios. To get better contrast, one has to
do something outside the projector, either on the screen, or near the viewer’s
eyes. To get high contrast, Navdy employed a carefully engineered screen. It
had a carefully selected curvature, had an aluminized backing, and its surface
was covered in microscopic lenses. These features caused it to bounce ambient
light away from the viewer’s eye, while reflecting the light from the projector
toward the viewer’s eye. This sort of optimization isn’t possible for most
projection applications, especially ones that try to make every-day objects
feel alive.

