To get the main camera
```cs
Camera.main;
```

Get the aspect ratio of the camera
<u>Note</u> This will be `width / height`
```cs
Camera.main.aspect;
```

Camera's half size in orthographic mode
```cs
Camera.main.orthographicSize;
```

Example: Get width of current screen
```cs
float width = Camera.main.aspect * Camera.main.orthographicSize * 2;
```

**<u>Note</u>** The position of center of camera view is (0, 0) not like other drawing canvas where (0, 0) starts on the top-left corner