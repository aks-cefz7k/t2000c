# VoiceWaveView
[![](https://jitpack.io/v/xfans/VoiceWaveView.svg)](https://jitpack.io/#xfans/VoiceWaveView)
[![GitHub stars](https://img.shields.io/github/stars/xfans/VoiceWaveView?style=plastic)](https://github.com/xfans/VoiceWaveView)
a voice wave view library
一个音频条形图的view,支持柱状音频，折线音频的样式

[https://github.com/xfans/VoiceWaveView](https://github.com/xfans/VoiceWaveView)

## Screenshot
![Screenshot2](pic/3.gif)![Screenshot1](pic/1.gif)

## Dependencies

```
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

```
implementation 'com.github.xfans:VoiceWaveView:1.0.2'
```
## Use

属性

 * `addHeader` - 添加图头的线(头尾的线不变化),百分数1-100，实际高度等于布局的`高度*百分数`
 * `addFooter`  - 添加图尾的线(头尾的线不变化)百分数1-100，实际高度等于布局的`高度*百分数`
 * `addBody` - 添加图上的线,百分数1-100
 * `lineSpace` - 线间距
 * `lineWidth` - 线宽
 * `duration` - 动画持续时间
 * `waveMode` - 线条动画模式，`up_down`上线变化，`left_right`从左往右移动
 * `lineType` - 线条样式，`line_graph`折线样式，`bar_chart`柱状样式
 * `lineColor` - 线条颜色
 * `gravity` - 图的位置，`center`，`bottom`等，同androd gravity

```
<me.xfans.lib.voicewaveview.VoiceWaveView
                android:id="@+id/voiceWaveView0"
                android:layout_width="wrap_content"
                android:layout_height="150dp"
                app:lineColor="@color/colorPrimary"
                app:waveMode="left_right"
                android:gravity="center"
        />
```
```
voiceWaveView?.apply {
            showGravity = Gravity.RIGHT or Gravity.TOP
            waveMode = WaveMode.UP_DOWN
            lineWidth = 30f
            lineSpace = 15f
            duration = 500
            lineColor = Color.parseColor("#F56B00")
            addHeader(4)
            addHeader(14)
            addBody(27)
            addBody(17)
            addBody(38)
            addBody(91)
            addBody(38)
            addBody(24)
            addBody(8)
            addBody(60)
            addBody(38)
            addBody(14)
            addBody(8)
            addFooter(4)
            addFooter(2)
            start()
        }
```

### License

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.