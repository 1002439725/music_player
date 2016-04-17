# music_player
This a music player ,and i will optimize it , i will show you the process that i optimize !!
activity_main界面：
<RelativeLayoutxmlns:android ="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width= "match_parent"
    android:layout_height= "match_parent"
    android:paddingBottom= "@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight= "@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context=".MainActivity"
    tools:ignore="HardcodedText" >

    <!-- 底部的播放控制区域 -->

    <RelativeLayout
        android:id= "@+id/rl_controller"
        android:layout_width= "match_parent"
        android:layout_height= "wrap_content"
        android:layout_alignParentBottom ="true" >

        <ImageButton
            android:id= "@+id/ib_play_or_pause"
            android:layout_width= "wrap_content"
            android:layout_height= "wrap_content"
            android:layout_centerInParent ="true"
            android:contentDescription= "@null"
            android:src= "@android:drawable/ic_media_play" />

        <ImageButton
            android:id= "@+id/ib_previous"
            android:layout_width= "wrap_content"
            android:layout_height= "wrap_content"
            android:layout_alignTop= "@+id/ib_play_or_pause"
            android:layout_toLeftOf= "@+id/ib_play_or_pause"
            android:contentDescription= "@null"
            android:src= "@android:drawable/ic_media_previous" />

        <ImageButton
            android:id= "@+id/ib_next"
            android:layout_width= "wrap_content"
            android:layout_height= "wrap_content"
            android:layout_alignTop= "@+id/ib_play_or_pause"
            android:layout_toRightOf= "@+id/ib_play_or_pause"
            android:contentDescription= "@null"//这一条是为了去除报错
            android:src= "@android:drawable/ic_media_next" />
       
        <Button
            android:id= "@+id/btn_play_mode"
            android:layout_width= "wrap_content"
            android:layout_height= "wrap_content"
            android:text= "顺"
            android:layout_alignTop= "@+id/ib_play_or_pause"
            android:layout_alignParentLeft ="true"
            />
    </RelativeLayout >

    <!-- 信息显示区域 -->

    <RelativeLayout
        android:id= "@+id/rl_music_info"
        android:layout_width= "match_parent"
        android:layout_height= "wrap_content"
        android:layout_above= "@+id/rl_controller" >

        <TextView
            android:paddingTop= "6dp"
            android:paddingBottom= "6dp"
            android:id= "@+id/tv_music_title"
            android:layout_width= "match_parent"
            android:layout_height= "wrap_content"
            android:singleLine= "true"
            android:text= "请选择歌曲 ... ..." />

        <SeekBar
            android:id= "@+id/sb_music_progress"
            android:layout_width= "match_parent"
            android:layout_height= "wrap_content"
            android:layout_below= "@+id/tv_music_title"
            android:max= "100"//设置最大进度
            android:progress= "0" />//设置初始进度值

        <TextView
            android:id= "@+id/tv_music_current_position"
            android:layout_width= "wrap_content"
            android:layout_height= "wrap_content"
            android:layout_alignParentLeft ="true"
            android:layout_below= "@+id/sb_music_progress"
            android:text= "00:00"//设置显示形式
            android:textSize= "12sp" />

        <TextView
            android:id= "@+id/tv_music_duration"
            android:layout_width= "wrap_content"
            android:layout_height= "wrap_content"
            android:layout_alignParentRight ="true"
            android:layout_below= "@+id/sb_music_progress"
            android:text= "00:00"
            android:textSize= "12sp" />
    </RelativeLayout >

    <!-- ListView：歌曲列表 -->

    <ListView
        android:id= "@+id/lv_musics"
        android:layout_width= "match_parent"
        android:layout_height= "wrap_content"
        android:layout_above= "@+id/rl_music_info"
        android:layout_alignParentTop ="true" >
    </ListView >

</RelativeLayout>
