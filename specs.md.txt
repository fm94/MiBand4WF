## Properties of the json file

The json file is composed of nested dictionaries which contain many keys used to set the location, position and image to be displayed for each element of the watchface. These are some common keys:
- X: position in the x-axis (int)
- Y: position in the y-axis (int)
- ImageIndex: number of the first image (int)
- ImagesCount: images from *ImageIndex* to *ImageIndex + ImagesCount* (int)

Alternative to X and Y positions using distances:
- TopLeftX: (int)
- TopLeftY: (int)
- BottomRightX: (int)
- BottomRightY: (int)
- Alignment: (string) ["TopRight", "TopLeft", "BottomRight", "BottomLeft", ...]
- Spacing: (int)

The available keys and their usability are described below.

*Replace "int", "string", and "bool" with that type of data but with the value you want.*

### Table of Contents
1. [Background](#background)
2. [Time](#time)
3. [Date](#date)
4. [Activity](#activity)
5. [Status](#status)
6. [Battery](#battery)
7. [Weather](#weather)

### Background
It defines the image background:

<details>
  <summary>image</summary>
  <img src="/imgs/0000.png" width="100">
</details>

```json
"Background": {
  "Image": {
    "X": "int",
    "Y": "int",
    "ImageIndex": "int"
  }
}
```

### Time
It displays the time:

<details>
  <summary>images</summary>
  <img src="/imgs/0001.png" width="25">
  <img src="/imgs/0002.png" width="25">
  <img src="/imgs/0003.png" width="25">
  <img src="/imgs/0004.png" width="25">
  <img src="/imgs/0005.png" width="25">
  <img src="/imgs/0006.png" width="25">
  <img src="/imgs/0007.png" width="25">
  <img src="/imgs/0008.png" width="25">
  <img src="/imgs/0009.png" width="25">
  <img src="/imgs/0010.png" width="25">
</details>

```json
"Time": {
  "Hours": {
    "Tens": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    },
    "Ones": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    }
  },
  "Minutes": {
    "Tens": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    },
    "Ones": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    }
  },
  "Seconds": {
    "Tens": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    },
    "Ones": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    }
  },
  "AmPm": {
    "X": "int",
    "Y": "int",
    "ImageIndexAm": "int",
    "ImageIndexPm": "int"
  }
}
```

### Date
It represents the weekday, day and month:

<details>
  <summary>images</summary>
  <img src="/imgs/0001.png" width="15">
  <img src="/imgs/0002.png" width="15">
  <img src="/imgs/0003.png" width="15">
  <img src="/imgs/0004.png" width="15">
  <img src="/imgs/0005.png" width="15">
  <img src="/imgs/0006.png" width="15">
  <img src="/imgs/0007.png" width="15">
  <img src="/imgs/0008.png" width="15">
  <img src="/imgs/0009.png" width="15">
  <img src="/imgs/0010.png" width="15">
  <img src="/imgs/0051.png" width="10">
  <img src="/imgs/0031.png" width="40">
  <img src="/imgs/0032.png" width="40">
  <img src="/imgs/0033.png" width="40">
  <img src="/imgs/0034.png" width="40">
  <img src="/imgs/0035.png" width="40">
  <img src="/imgs/0036.png" width="40">
  <img src="/imgs/0037.png" width="40">
</details>

```json
"Date": {
  "WeekDay": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
  },
  "MonthAndDay": {
    "TwoDigitsMonth": "bool",
    "TwoDigitsDay": "bool",
    "Separate": {
      "Day": {
        "TopLeftX": "int",
        "TopLeftY": "int",
        "BottomRightX": "int",
        "BottomRightY": "int",
        "Alignment": "string",
        "Spacing": "int",
        "ImageIndex": "int",
        "ImagesCount": "int"
      },
      "Month": {
        "TopLeftX": "int",
        "TopLeftY": "int",
        "BottomRightX": "int",
        "BottomRightY": "int",
        "Alignment": "string",
        "Spacing": "int",
        "ImageIndex": "int",
        "ImagesCount": "int"
      }
    }
  },
  "OneLine": {
    "Number": {
      "TopLeftX": "int",
      "TopLeftY": "int",
      "BottomRightX": "int",
      "BottomRightY": "int",
      "Alignment": "string",
      "Spacing": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    },
    "DelimiterImageIndex": "int",
  }
}
```

### Activity
It shows the data regarding the calories, steps, pulse and distance the user does during the day:

<details>
  <summary>images</summary>
  <img src="/imgs/0001.png" width="10">
  <img src="/imgs/0002.png" width="10">
  <img src="/imgs/0003.png" width="10">
  <img src="/imgs/0004.png" width="10">
  <img src="/imgs/0005.png" width="10">
  <img src="/imgs/0006.png" width="10">
  <img src="/imgs/0007.png" width="10">
  <img src="/imgs/0008.png" width="10">
  <img src="/imgs/0009.png" width="10">
  <img src="/imgs/0010.png" width="10">
  <img src="/imgs/0012.png" width="30">
  <img src="/imgs/0014.png" width="12">
</details>

```json
"Activity": {
  "Calories": {
    "TopLeftX": "int",
    "TopLeftY": "int",
    "BottomRightX": "int",
    "BottomRightY": "int",
    "Alignment": "string",
    "Spacing": "int",
    "ImageIndex": "int",
    "ImagesCount": "int"
  },
  "Steps": {
    "TopLeftX": "int",
    "TopLeftY": "int",
    "BottomRightX": "int",
    "BottomRightY": "int",
    "Alignment": "string",
    "Spacing": "int",
    "ImageIndex": "int",
    "ImagesCount": "int"
  },
  "StepsGoal": {
    "TopLeftX": "int",
    "TopLeftY": "int",
    "BottomRightX": "int",
    "BottomRightY": "int",
    "Alignment": "string",
    "Spacing": "int",
    "ImageIndex": "int",
    "ImagesCount": "int"
  },
  "Pulse": {
    "TopLeftX": "int",
    "TopLeftY": "int",
    "BottomRightX": "int",
    "BottomRightY": "int",
    "Alignment": "string",
    "Spacing": "int",
    "ImageIndex": "int",
    "ImagesCount": "int"
  },
  "Distance": {
    "Number": {
      "TopLeftX": "int",
      "TopLeftY": "int",
      "BottomRightX": "int",
      "BottomRightY": "int",
      "Alignment": "string",
      "Spacing": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    },
    "SuffixImageIndex": "int",
    "DecimalPointImageIndex": "int"
  }
}
```

### Status
It references the different icons for the user to know the status of some functions of the watch:

<details>
  <summary>images</summary>
  <img src="/imgs/0099.png" width="15">
  <img src="/imgs/0098.png" width="16">
  <img src="/imgs/0097.png" width="11">
  <img src="/imgs/0093.png" width="11">
  <img src="/imgs/0091.png" width="17">
</details>

```json
"Status": {
  "Alarm": {
    "Coordinates": {
      "X": "int",
      "Y": "int"
    },
    "ImageIndexOn": "int"
  },
  "Bluetooth": {
    "Coordinates": {
      "X": "int",
      "Y": "int"
    },
    "ImageIndexOn": "int",
    "ImageIndexOff": "int"
  },
  "DoNotDisturb": {
    "Coordinates": {
      "X": "int",
      "Y": "int"
    },
    "ImageIndexOn": "int"
  },
  "Lock": {
    "Coordinates": {
      "X": "int",
      "Y": "int"
    },
    "ImageIndexOn": "int"
  }
}
```

### Battery
Data regarding the status of the battery of the watch:

<details>
  <summary>images</summary>
  <img src="/imgs/0001.png" width="10">
  <img src="/imgs/0002.png" width="10">
  <img src="/imgs/0003.png" width="10">
  <img src="/imgs/0004.png" width="10">
  <img src="/imgs/0005.png" width="10">
  <img src="/imgs/0006.png" width="10">
  <img src="/imgs/0007.png" width="10">
  <img src="/imgs/0008.png" width="10">
  <img src="/imgs/0009.png" width="10">
  <img src="/imgs/0010.png" width="10">
  <img src="/imgs/0061.png" width="12">
  <img src="/imgs/0053.png" width="25">
  <img src="/imgs/0054.png" width="25">
  <img src="/imgs/0055.png" width="25">
  <img src="/imgs/0056.png" width="25">
  <img src="/imgs/0057.png" width="25">
  <img src="/imgs/0058.png" width="25">
</details>

```json
"Battery": {
  "Icon": {
    "X": "int",
    "Y": "int",
    "ImageIndex": "int",
    "ImagesCount": "int"
  },
  "Text": {
    "TopLeftX": "int",
    "TopLeftY": "int",
    "BottomRightX": "int",
    "BottomRightY": "int",
    "Alignment": "string",
    "Spacing": "int",
    "ImageIndex": "int",
    "ImagesCount": "int"
  },
  "Scale": {
    "StartImageIndex": "int",
    "Segments": [
      {
        "X": "int",
        "Y": "int"
      }
    ]
  }
}
```

### Weather
Information about the weather such as current temperature or temperature during the day and during the night:

<details>
  <summary>images</summary>
  <img src="/imgs/0001.png" width="10">
  <img src="/imgs/0002.png" width="10">
  <img src="/imgs/0003.png" width="10">
  <img src="/imgs/0004.png" width="10">
  <img src="/imgs/0005.png" width="10">
  <img src="/imgs/0006.png" width="10">
  <img src="/imgs/0007.png" width="10">
  <img src="/imgs/0008.png" width="10">
  <img src="/imgs/0009.png" width="10">
  <img src="/imgs/0010.png" width="10">
  <img src="/imgs/0064.png" width="10">
  <img src="/imgs/0065.png" width="10">
  <img src="/imgs/0066.png" width="12">
  <img src="/imgs/0100.png" width="20">
  <img src="/imgs/0101.png" width="20">
  <img src="/imgs/0102.png" width="20">
  <img src="/imgs/0103.png" width="20">
  <img src="/imgs/0104.png" width="20">
  <img src="/imgs/0105.png" width="20">
  <img src="/imgs/0106.png" width="20">
  <img src="/imgs/0107.png" width="20">
  <img src="/imgs/0108.png" width="20">
  <img src="/imgs/0109.png" width="20">
  <img src="/imgs/0110.png" width="20">
  <img src="/imgs/0111.png" width="20">
  <img src="/imgs/0112.png" width="20">
  <img src="/imgs/0113.png" width="20">
  <img src="/imgs/0114.png" width="20">
  <img src="/imgs/0115.png" width="20">
  <img src="/imgs/0116.png" width="20">
  <img src="/imgs/0117.png" width="20">
  <img src="/imgs/0118.png" width="20">
  <img src="/imgs/0119.png" width="20">
  <img src="/imgs/0120.png" width="20">
  <img src="/imgs/0121.png" width="20">
  <img src="/imgs/0122.png" width="20">
  <img src="/imgs/0123.png" width="20">
  <img src="/imgs/0124.png" width="20">
  <img src="/imgs/0125.png" width="20">
  <img src="/imgs/0126.png" width="20">
</details>

```json
"Weather": {
  "Icon": {
    "CustomIcon": {
      "X": "int",
      "Y": "int",
      "ImageIndex": "int",
      "ImagesCount": "int"
    }
  },
  "Temperature": {
    "Today": {
      "OneLine": {
        "Number": {
          "TopLeftX": "int",
          "TopLeftY": "int",
          "BottomRightX": "int",
          "BottomRightY": "int",
          "Alignment": "string",
          "Spacing": "int",
          "ImageIndex": "int",
          "ImagesCount": "int"
        },
        "MinusSignImageIndex": "int",
        "DelimiterImageIndex": "int",
        "AppendDegreesForBoth": "bool",
        "DegreesImageIndex": "int"
      },
      "Separate": {
        "Day": {
          "Number": {
            "TopLeftX": "int",
            "TopLeftY": "int",
            "BottomRightX": "int",
            "BottomRightY": "int",
            "Alignment": "string",
            "Spacing": "int",
            "ImageIndex": "int",
            "ImagesCount": "int"
          },
          "MinusImageIndex": "int",
          "DegreesImageIndex": "int"
        },
        "Night": {
          "Number": {
            "TopLeftX": "int",
            "TopLeftY": "int",
            "BottomRightX": "int",
            "BottomRightY": "int",
            "Alignment": "string",
            "Spacing": "int",
            "ImageIndex": "int",
            "ImagesCount": "int"
          },
          "MinusImageIndex": "int",
          "DegreesImageIndex": "int"
        }
      }
    },
    "Current": {
      "Number": {
        "TopLeftX": "int",
        "TopLeftY": "int",
        "BottomRightX": "int",
        "BottomRightY": "int",
        "Alignment": "string",
        "Spacing": "int",
        "ImageIndex": "int",
        "ImagesCount": "int"
      },
      "MinusImageIndex": "int",
      "DegreesImageIndex": "int"
    }
  }
}
```
*Use OneLine or Separate in Temperature>Today, do not add both in order not to have duplicated information*
