# SuperSpineViewer

[**For English User**](https://github.com/Aloento/SuperSpineViewer/blob/master/README-Eng.md)

Test

一个拿来加载与导出Spine动画的工具  
需要 **Java 21 21 21**  
需要 像素缓冲区支持  
导出 MOV 需要 FFmpeg  
当前版本：2.1.0

![霜叶](https://i0.hdslb.com/bfs/album/98b4fd8a12bc6dbf691b967bed625db67713dff0.png@518w.png "明日方舟 - 霜叶")

## 获得SuperSpineViewer

[**发布的稳定版本**](https://github.com/Aloento/SuperSpineViewer/releases/latest)

```bash
java -XX:MaxRAMPercentage=75.0 --enable-preview -jar SuperSpineViewer.jar
```

### 性能设置参考

* 高分辨率 (Camera) = 高内存需求
* 高质量 (Quality) = 成倍增加的内存需求

**RAM**:

    4G+ = Extreme (240FPS)
    2G~ = Standard (120FPS)
    1G~ = Fast (60FPS)

### 序列使用参考

以导入After Effects为例  
默认30FPS时，伸缩设置

    Extreme = 800%
    Standard = 400%
    Fast = 200%

## 功能与兼容性

### 实现的功能

* 加载Spine的Skel和Json
* 重载骨骼与贴图
* 查看与播放动画
* 查看与切换皮肤
* 变换大小
* 调整位置
* 调整速度
* 循环播放
* 播放暂停
* 导出透明MOV
* 导出透明PNG
* 调整性能质量

### 支持的版本

| 版本        | 支持情况 |
|-----------|------|
| Spine 1.x | 不支持  |
| Spine 2.x | 不完全  |
| Spine 3.1 | 不完全  |
| Spine 3.2 | 不完全  |
| Spine 3.3 | 不完全  |
| Spine 3.4 | √    |
| Spine 3.5 | √    |
| Spine 3.6 | √    |
| Spine 3.7 | √    |
| Spine 3.8 | √    |
| Spine 4.0 | √    |
| Spine 4.1 | √    |
| Spine 4.2 | √    |

## 画廊

<html>
    <table style="margin-left: auto; margin-right: auto;">
        <tr>
            <td>
                <img src="https://i0.hdslb.com/bfs/album/73fdec47d907dc42e96a2d0d21482680fd7efb3f.png" alt="首屏加载画面">
                <img src="https://i0.hdslb.com/bfs/album/697ebe690460ee8a1f50a7bb4c4f973331b244dd.png" alt="Spine信息与导出">
                <img src="https://i0.hdslb.com/bfs/album/98b4fd8a12bc6dbf691b967bed625db67713dff0.png" alt="明日方舟 - 霜叶">
                <img src="https://i0.hdslb.com/bfs/album/79dbdaee161130460b77411f4664b4ecbd53d68e.png" alt="明日方舟 - 德克萨斯">
            </td>
            <td>
                <img src="https://i0.hdslb.com/bfs/album/56d918333fd302f9c221680008d7109fe090fb39.png" alt="明日方舟 - 闪灵">
                <img src="https://i0.hdslb.com/bfs/album/8ad8f6ca661f68909b30edce518d47614162a78f.png" alt="公主连结 - 凯留">
                <img src="https://i0.hdslb.com/bfs/album/51ee6aa61652191d4ab6c27a6e18bf8dc1997fdc.png" alt="方舟指令 - 湊阿库娅">
                <img src="https://i0.hdslb.com/bfs/album/0919e8d269e355c9b451d52e887c314a84f47faa.png" alt="万象物语">
            </td>
        </tr>
    </table>
</html>

## 构建

重写 `org.lwjgl.lwjgl：lwjgl` 的 `MANIFEST.MF`，使 `Sealed: false`
