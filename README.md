# GesturesLock
手势解锁。
```java
GestureLockView 手势解锁View
//设置密码
gestureLockView.setKey("0124678");
//手势完成后回调
gestureLockView.setOnGestureFinishListener(new OnGestureFinishListener() {
	@Override
	public void OnGestureFinish(boolean success, String key) {
		if(success)
		{
			textview.setTextColor(Color.parseColor("#FFFFFF"));
			textview.setVisibility(View.VISIBLE);
			textview.setText("密码正确！");
			textview.startAnimation(animation);
		}else{
			textview.setTextColor(Color.parseColor("#FF2525"));
			textview.setVisibility(View.VISIBLE);
			textview.setText("密码错误！");
			textview.startAnimation(animation);
		}
	}
	});
```

``` xml
<com.rxx.view.GestureLockView 
        android:id="@+id/gestureLockView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content">
        </com.rxx.view.GestureLockView>
```
