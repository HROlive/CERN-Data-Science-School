## Looking For Anomalies in Space

### Watson Studio

https://dataplatform.cloud.ibm.com

### GPUs
https://medium.com/ibm-watson/gpu-powered-notebook-is-coming-to-watson-studio-56876f60c056


## Data Source

Data from

https://www.spacetelescope.org/projects/fits_liberator/m31data/

## Overlay a grid on a existing image, with help of ImageMagick (convert) & Scripts

Script used to overlay can be found http://www.fmwconcepts.com/imagemagick/grid/index.php

```
./grid -c "yellow" -s 112,112 m31_composite_cropped.png m31_112_112.png
./grid -c "yellow" -s 224,224 m31_composite_cropped.png m31_224_224.png
```

## Actual Slice the Original Image into smaller subimages

http://www.imagemagick.org/Usage/crop/#crop_equal

```
convert m31_composite_cropped.png -crop 112x112 +repage  +adjoin data/crop_112/m31_composite_112_112_%03d.png

convert m31_composite_cropped.png -crop 224x224 +repage  +adjoin data/crop_224/m31_composite_224_224_%03d.png
```

## Image of Found Enhanced Anomaly

https://imgur.com/a/m8Fq4sf