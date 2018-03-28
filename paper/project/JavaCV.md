# 基于JavaCV的直播系统设计与实现

## 1.基于JavaCV的摄像头调用

    首先在[官网github](https://github.com/bytedeco/javacv)下学习相关使用方式，参考[博客](https://blog.csdn.net/eguid_1/article/details/51659578)进行相关的开发。

### 1.1 项目创建

    首先通过IDEA创建一个Maven项目，并在`pom.xml`加入如下配置

    ```xml
    <dependencies>
        <dependency>
            <groupId>org.bytedeco</groupId>
            <artifactId>javacv-platform</artifactId>
            <version>1.4</version>
        </dependency>
    </dependencies>
    ```

    测试获取摄像头并将内容显示出来
    1. 通过新建的`OpenCVFrameGrabber`对象中`start`函数启动摄像头
    2. 新建`CanvasFrame`对象用来显示摄像头中的内容，设置`CloseOperation`为`EXIT_ON_CLOSE`
    3. 循环将`grabber.grab()`抓取到的图像传送给`canvas.showImage`就可以显示图像，通过线程睡眠降低刷新频率
    4. 当`canvas.isDisplayable`为`false`的时候`grabber.stop`,退出程序