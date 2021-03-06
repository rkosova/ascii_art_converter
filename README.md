# ascii_art_converter
Converts grayscale matrix generated by [grayscale_converter](https://github.com/rkosova/grayscale_converter) to ASCII art. Thus, it is dependant on grayscale_converter.

## How to use
The `ASCIIArtist` class holds two methods, `generate_color_dict` and `generate_ascii_file`. It also takes the grayscale matrix as a constructor parameter.

### `generate_color_dict`
Generates appropriate dictionary of ASCII characters corresponding to the relative range of darkest-to-lightest values in the num_matrix
  * shade_consistent: boolean, if true, the generator will try to match the shade (or "darkness") of the cells/grayscaled pixels with an aproppriate character, defaults to False.
  * detail: float value in range (0, 1), determines the diversity of ASCII characters. The higher the float value, the more diversity
 
Returns a dictionary with spaced out RGB values and ASCII character values corresponding to those RGB values.

### `generate_ascii_file`
Generates .txt file with ASCII art.
  * ascii_diction: ditionary, color range dictionary generated by generate_color_dict()
  * fname: string, file name


WARNING: The ASCII text will be double the resolution of the original image, and thus it is reccomended to only be used with small images. 


```
g g g g g g g g g g g g y 8 i i i i i i i 8 y g g g g g g g g g g g g 
g g g g g g g g g y 8 i i i i i i i i i i i i i 8 y g g g g g g g g g 
g g g g g g g g 8 i i i i i i i i i i i i i i i i i 8 g g g g g g g g 
g g g g g g y i i i i i i i i i i i i i i i i i i i i i y g g g g g g 
g g g g g y i i i i i i i i i i i i i i i i i i i i i i i y g g g g g 
g g g g y i i i i i i i i i i i i i i i i i i i i i i i i i 8 g g g g 
g g g y i i i i i i i i i i i i i i i i i i i i i i i i i i i y g g g 
g g y 8 i i i i y y 8 i i i i i i i i i i i i i 8 y y i i i i i g g g 
g g 8 i i i i 8 g g g g 8 8 8 y y y y y 8 8 8 g g g g 8 i i i i 8 g g 
g y i i i i i 8 g g g g g g g g g g g g g g g g g g g 8 i i i i i y g 
g 8 i i i i i 8 g g g g g g g g g g g g g g g g g g g 8 i i i i i 8 g 
g i i i i i i 8 g g g g g g g g g g g g g g g g g g g 8 i i i i i i g 
y i i i i i i 8 g g g g g g g g g g g g g g g g g g g 8 i i i i i i y 
8 i i i i i i y g g g g g g g g g g g g g g g g g g g y 8 i i i i i 8 
i i i i i i 8 g g g g g g g g g g g g g g g g g g g g g y i i i i i i 
i i i i i i y g g g g g g g g g g g g g g g g g g g g g y i i i i i i 
i i i i i i y g g g g g g g g g g g g g g g g g g g g g y i i i i i i 
i i i i i i y g g g g g g g g g g g g g g g g g g g g g y i i i i i i 
i i i i i i y g g g g g g g g g g g g g g g g g g g g g y i i i i i i 
i i i i i i 8 g g g g g g g g g g g g g g g g g g g g g 8 i i i i i i 
i i i i i i i g g g g g g g g g g g g g g g g g g g g g 8 i i i i i i 
8 i i i i i i y g g g g g g g g g g g g g g g g g g g y i i i i i i 8 
y i i i i i i i y g g g g g g g g g g g g g g g g g y 8 i i i i i i y 
g i i i i i i i i y g g g g g g g g g g g g g g g y i i i i i i i i g 
g 8 i i i 8 i i i i 8 y g g g g g g g g g g g y 8 i i i i i i i i 8 g 
g y i i i y g 8 i i i i i 8 g g g g g g g 8 i i i i i i i i i i i y g 
g g 8 i i i y g 8 i i i i 8 g g g g g g g 8 i i i i i i i i i i 8 g g 
g g g 8 i i 8 g g 8 8 i 8 y g g g g g g g y i i i i i i i i i i y g g 
g g g y i i i 8 g g g y g g g g g g g g g g i i i i i i i i i y g g g 
g g g g y i i i y g g g g g g g g g g g g g i i i i i i i i y g g g g 
g g g g g y i i i 8 8 8 8 g g g g g g g g g i i i i i i i y g g g g g 
g g g g g g y i i i i i i y g g g g g g g g i i i i i 8 y g g g g g g 
g g g g g g g g 8 i i i i y g g g g g g g g i i i i 8 g g g g g g g g 
g g g g g g g g g y 8 i i g g g g g g g g g i i 8 y g g g g g g g g g 
```
