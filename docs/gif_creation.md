# Gif creation

```shell
ffmpeg -i input.mov -vf "fps=15,scale=iw:ih:flags=lanczos,palettegen" palette.png
ffmpeg -i input.mov -i palette.png -filter_complex "fps=15,scale=iw:ih:flags=lanczos[x];[x][1:v]paletteuse=dither=bayer" new_class_snippet.gif
```
