# ScreenAdapter
一个宽度基于360dpi的安卓适配

原理：
基于设计图的宽度作为基准（项目默认360dp），根据设备的宽度，通过dimens来调整使宽度比例一致，从而打到每个屏幕显示效果一致。

使用：
implementation 'com.github.RikiLau.ScreenAdapter:screenAdapter:v2.2'

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto">
    
    <View
        android:id="@+id/view"
        android:layout_width="@dimen/dp_300"
        android:layout_height="@dimen/dp_200"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        android:background="#0f0"/>
    
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#f00"
        android:text="hello world"
        android:textColor="@color/white"
        android:textSize="@dimen/sp_20"
        app:layout_constraintTop_toTopOf="@id/view"
        app:layout_constraintBottom_toBottomOf="@id/view"
        app:layout_constraintStart_toStartOf="@id/view"
        app:layout_constraintEnd_toEndOf="@id/view"/>
</androidx.constraintlayout.widget.ConstraintLayout>

参考：
https://www.jianshu.com/p/1302ad5a4b04
