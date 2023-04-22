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

### View is created or not
```
 YourView.viewTreeObserver.addOnGlobalLayoutListener(object : ViewTreeObserver.OnGlobalLayoutListener{
            override fun onGlobalLayout() {
                // Remove the listener to avoid continuously triggering this code
                YourView.viewTreeObserver.removeOnGlobalLayoutListener(this)
                
                // the view is created successfully
                val height = YourView.height
                val width = YourView.width
            }
        })
```   

> YourView is the view you want to check is created or not. And if the view is created then this listener will call and do whatever you want when the view is created successfully. </br>
> <b>Note</b> : that is you are trying to calculate recyclerview's height and width it returns 0 because the element inside recyclerview are still rendering so for that you need to set some listener or callback interface to check whether the element is drawn or not. 
