# navigationBack
顶部回退按钮
1. <android.support.v7.widget.Toolbar
            android:id="@+id/toolbar"
            android:layout_width="match_parent"
            android:layout_height="?attr/actionBarSize"
            android:background="?attr/colorPrimary"
            toolbar:navigationIcon="@mipmap/navigation_back_white"
            app:popupTheme="@style/ToolbarTheme" >
            <EditText
                android:id="@+id/edit_search"
                android:layout_width="match_parent"
                android:layout_height="match_parent"/>
        </android.support.v7.widget.Toolbar>
    </android.support.design.widget.AppBarLayout>

2.最近看来好多关于android顶部导航栏回退的实现如下图效果
点击返回上级页面，网上的大部分都实现特别繁琐，其实安卓自带BUFF,在Manifest清单文件中一句代码就能搞定，特别easy，下面贴方法

 
    <activity android:name=".SearchActivity"  
                      android:parentActivityName=".MainActivity">   <!--上一级Activity--> 


只需要在AndroidManifest文件中对应的Activity增加一个parent Activity属性就ok了。
