<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [background][1]
-   [tint][2]
-   [greyscale][3]
-   [grayscale][4]
-   [toColourspace][5]
-   [toColorspace][6]

## background

Set the background for the `embed`, `flatten` and `extend` operations.
The default background is `{r: 0, g: 0, b: 0, alpha: 1}`, black without transparency.

Delegates to the _color_ module, which can throw an Error
but is liberal in what it accepts, clipping values to sensible min/max.
The alpha value is a float between `0` (transparent) and `1` (opaque).

**Parameters**

-   `rgba` **([String][7] \| [Object][8])** parsed by the [color][9] module to extract values for red, green, blue and alpha.


-   Throws **[Error][10]** Invalid parameter

Returns **Sharp** 

## tint

Tint the image using the provided chroma while preserving the image luminance.
An alpha channel may be present and will be unchanged by the operation.

**Parameters**

-   `rgb` **([String][7] \| [Object][8])** parsed by the [color][9] module to extract chroma values.


-   Throws **[Error][10]** Invalid parameter

Returns **Sharp** 

## greyscale

Convert to 8-bit greyscale; 256 shades of grey.
This is a linear operation. If the input image is in a non-linear colour space such as sRGB, use `gamma()` with `greyscale()` for the best results.
By default the output image will be web-friendly sRGB and contain three (identical) color channels.
This may be overridden by other sharp operations such as `toColourspace('b-w')`,
which will produce an output image containing one color channel.
An alpha channel may be present, and will be unchanged by the operation.

**Parameters**

-   `greyscale` **[Boolean][11]**  (optional, default `true`)

Returns **Sharp** 

## grayscale

Alternative spelling of `greyscale`.

**Parameters**

-   `grayscale` **[Boolean][11]**  (optional, default `true`)

Returns **Sharp** 

## toColourspace

Set the output colourspace.
By default output image will be web-friendly sRGB, with additional channels interpreted as alpha channels.

**Parameters**

-   `colourspace` **[String][7]?** output colourspace e.g. `srgb`, `rgb`, `cmyk`, `lab`, `b-w` [...][12]


-   Throws **[Error][10]** Invalid parameters

Returns **Sharp** 

## toColorspace

Alternative spelling of `toColourspace`.

**Parameters**

-   `colorspace` **[String][7]?** output colorspace.


-   Throws **[Error][10]** Invalid parameters

Returns **Sharp** 

[1]: #background

[2]: #tint

[3]: #greyscale

[4]: #grayscale

[5]: #tocolourspace

[6]: #tocolorspace

[7]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[8]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[9]: https://www.npmjs.org/package/color

[10]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Error

[11]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[12]: https://github.com/jcupitt/libvips/blob/master/libvips/iofuncs/enumtypes.c#L568
