# Utility-Functions-Android
List of common functions that we used in every day task related to Android development

### Screen Height & Width
  ```
  public static int getScreenWidth() {
    return Resources.getSystem().getDisplayMetrics().widthPixels;
  }

  public static int getScreenHeight() {
    return Resources.getSystem().getDisplayMetrics().heightPixels;
  }
```

> you don't need context to get screen height or width by this code snippet. <br/>
[reference link](https://stackoverflow.com/a/31377616/12543430)
