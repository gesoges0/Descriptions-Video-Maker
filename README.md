# Descriptions Video Maker
This is "Video as Code" Project.

## usage
### Make Project File
```commandline
# Make project direcotry 
mkdir projects/projectX

# Edit Json File
vim projects/projectX/setting.json

# Edit Descriptions
vim projects/projectX/descriptions.tsv

# test json and tsv
pytest

# make each image and a concatenated image
python make-images --project projectX

# make video as .mp4
python make-video --project projectX
```

## example
### [setting.json](https://github.com/gesoges0/descriptions-video-maker/blob/main/projects/projectX/setting.json)
```commandline
{
  "description_image": {
    "height": 780,
    "width": 320,
    "layers": {
      "image_layer": {
        "description_type": "image",
        "height": [
          0, 320
        ],
        "width": [
          0, 320
        ],
        "background_color": [
          0, 0, 0
        ]
      },
      "title_layer": {
        "description_type": "string",
        "height": [
          320, 440
        ],
        "width": [
          0, 320
        ],
        "background_color": [
          33, 33, 33
        ]
      },
      "description_layer": {
        "description_type": "string",
        "height": [
          440, 780
        ],
        "width": [
          0, 320
        ],
        "background_color": [
          0, 0, 0
        ]
      }
    }
  }
}
```

### [description.tsv](https://github.com/gesoges0/descriptions-video-maker/blob/main/projects/projectX/descriptions.tsv)
```commandline
image_layer	title_layer	description_layer
projects/projectX/input/ai.png	TITLE_A	AAAAA AAAAA AAAAAAA AAAAA
projects/projectX/input/aisowarai.png	TITLE_B	BBBBBBBB BBBBBBBBBBBBBBBB BBBBB
projects/projectX/input/shuden.png	TITLE_C	CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC
projects/projectX/input/shuden.png	TITLE_D	DDDDDD DD DDDD DDDDDDDDDD
projects/projectX/input/shuden.png	TITLE_E	EE EEEEE EEE EEEEEEEEE
projects/projectX/input/shuden.png	TITLE_F	FFFFF FFFFFFF FFF FFFFFFF
projects/projectX/input/shuden.png	TITLE_F	FFFFF FFFFFFF FFF FFFFFFF
projects/projectX/input/shuden.png	TITLE_F	FFFFF FFFFFFF FFF FFFFFFF
projects/projectX/input/shuden.png	TITLE_F	FFFFF FFFFFFF FFF FFFFFFF

```

### test
test projectX/setting.json and projectX/description.tsv
```commandline
pytest
```

### make images
```commandline
python manage.py make-images --project projectX
```

![output](output/projectX/concat/output.png "output")

### make video
```commandline
python manage.py make-video --project projectX
```

https://user-images.githubusercontent.com/33025417/153738612-d905eea6-5dad-48f7-a6e7-c526754b8534.mp4


# other example
```commandline
python manage.py make-images --project projectY
python manage.py make-video --project projectY
```
![output](output/projectY/concat/output.png "output")


https://user-images.githubusercontent.com/33025417/154841199-10b40483-d6bc-487c-b35e-3dee20df8758.mp4




