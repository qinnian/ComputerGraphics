# title: 计算机图形学知识点总结

## 一、填空题

>考点：图形学中涉及的坐标系、光栅扫描显示中的帧缓存的计算，平面几何投影的类型，曲线的逼近和拟合，基本几何变换定义。



### 1. 坐标系

（1）世界坐标系(WC,World Coordinate System)

又称用户坐标系，场景采用的坐标系，是直角右手坐标系，长度单位用户自定，取值范围整个实数域。


（2）局部坐标系(LC, Local Coordinate System) 

（3）观察坐标系(VC,Viewing Coordinate System) 

（4）规范化坐标系(NDC,Normalized Coordinate System)

一种虚拟的坐标系，与具体设备无关，其取值范围在0~1之间，起到将WC与DC联系起来的作用。

（5）设备坐标系(DC,Device Coordinate System)

依设备而定的坐标系，是二维直角坐标系，原点和轴的定义依设备不同而不同，长度单位是设备的步距，取值范围有限的整数。

![二维观察流程
](https://pic2.superbed.cn/item/5df9de2676085c32898d53a2.jpg)

>例：
>常用坐标系一般可以分为：建模坐标系、用户坐标系、观察坐标系、规格化设备坐标系、设备坐标系。

### 2. 帧缓存 

帧缓存大小的计算：` x 方向的像素点数× y 方向的像素点数× log2n（BYTE ）` 
其中：n是颜色数或灰度等级数。

1MB = 1024KB

1KB = 1024B(即字节)

1MB = 1024 X 1024 字节

>例：
>
>1. 当显示器分辨率是1024x768时,计算24位位图需要的帧缓冲内存?
>
>（1024 x 768 x 24bit）/ 8Byte/bit =2359296Byte = 2.25MB 
>
>2. 灰度等级为256级,分辨率为1024*1024的显示器,至少需要的帧缓存容量为多少？
>(1024 x 1024 x 8bit)/ 8Byte/bit = 1 M

### 3. 几何投影

平面几何投影的类型是 <u>平行投影</u> 和 <u>透视投影</u>

![](https://pic1.superbed.cn/item/5dface8376085c3289b586e7.jpg)

### 4. 曲线的逼近和拟合

用一组型值点来指定曲线曲面的形状时，形状完全通过给定的型值点列，该方法称为曲线曲面的 <u>拟合</u>

用控制点列来指定曲线曲面的形状时，得到的曲线曲面不一定通过控制点列，该方法称为曲线曲面称为 <u>逼近</u>

### 5. 基本几何变换定义

图形几何变换是指图形的 <u>平移</u> 、<u>比例</u>、<u>旋转</u> 。

![](https://pic2.superbed.cn/item/5dfac13076085c3289b369cb.jpg)


## 二、选择题 

>考点：
>
>颜色模型，图形变换，光照（漫反射、镜面反射、环境光、折射），齐次坐标，根据几何变换矩阵分析变换结果。

### 1. 颜色模型

RGB：用于扫描仪和显示设备、计算机系统

CMYK：用于打印机、印刷出版业

HSB/HSV/HSL/HSI：用于软件用户、艺术家

YUV/YIQ：用于视频和电视

CIE颜色空间：CIE XYZ、CIE Lab、CIE LUV

>例：
>
>计算机图形显示器一般使用（RGB）颜色模型。

### 2. 图形变换

定义：对图形的几何信息经过几何变换后产生新的图形。

主要包括：几何变换，坐标变换、观察变换、二维变换、三维变换等。

![](https://pic3.superbed.cn/item/5dfa216c76085c328999c93d.jpg)

### 3、光照（漫反射、镜面反射、环境光、折射）

简单光照模型的反射光由环境光、漫反射、镜面反射组成。

物体表面的反射光和透射光决定了物体呈现的颜色


>例：
>
>1. 当观察光照下的光滑物体表面时，在某个方向上看到高光或强光，这个现象称为 __镜面反射__。
>
>2. 在简单光反射模型中，由物体表面上点反射到视点的光强由(1)(2)(3)组成。
（1）环境光的反射光强；
（2）理想漫反射光强；
（3）镜面反射光强；

### 4、齐次坐标

基本思想：把一个 n 维空间的几何问题，转换到 n＋1 维空间中去解决。

![](https://pic1.superbed.cn/item/5dfac2af76085c3289b3a2bf.jpg)

![](https://pic3.superbed.cn/item/5dfac2f776085c3289b3ad0a.jpg)

### 5、根据几何变换矩阵分析变换结果



## 三、问答题

>考点：
>
>图形学、图像学、模式识别学科的概念。
>阴极射线管显示器的构成及各部分功能。
        
### 1、图形学

计算机图形学是研究怎样利用计算机表示、生成、 处理和显示图形的原理、 算法、 方法和技术的一门学科。

图形：狭义上又称为矢量图形或参数图形。按照数学方法定义的线条和曲线组成，含有几何属性。或者说更强调场景的几何表示，是由场景的几何模型和景物的物理属性共同组成的。

特点：

A 文件小。

B 可采取高分辨印刷。

C 图形可以无限缩放。


### 2、图像学

图像：狭义上又称为点阵图或位图图像。图像是指整个显示平面以二维矩阵表示，矩阵的每一点称为一个像素，由像素点所取亮度或颜色值不同所构成的二维画面。

特点：

A 文件所占的空间大。

B 位图放大到一定的倍数后会产生锯齿。

C 位图图像在表现色彩、色调方面的效果比矢量图更加优越。

### 3、模式识别

研究的是计算机图形学的逆过程。

指计算机对图形信息进行识别和分析描述，是从图形到描述的表达过程。

### 4、CRT

CRT 显示器学名为“阴极射线显像管”，是一种使用阴极射线管（Cathode Ray Tube）的显示器。

阴极：阴极被灯丝加热后，会发出电子，并形成发散的电子云。

电平控制器：控制电子束的强弱，改变形成亮点的明暗程度。

聚焦系统：使电子云汇聚成很细的电子束

加速系统：使电子束加速到轰击荧光屏应有的速度

磁偏转系统：将电子束引向荧光屏特定的位置

阳极荧光粉涂层：荧光粉发出可见光

![CRT](https://pic3.superbed.cn/item/5df9ccfc76085c328989ba44.jpg)

![CRT](https://pic.superbed.cn/item/5df9eb3776085c328990091b.jpg)

## 四、程序补充题

>考点：
>
>基本几何变换相关函数、程序设计

### 1. 平移函数

    void glTranslatef(GLfloat x,GLfloat y,GLfloat z);

函数功能：

  沿X轴正方向平移x个单位(x是有符号数)

  沿Y轴正方向平移y个单位(y是有符号数)

  沿Z轴正方向平移z个单位(z是有符号数)

### 2. 旋转函数

    void glRotatef(GLfloat angle,GLfloat x,GLfloat y,GLfloat z);

先解释一下旋转方向，做(0,0,0)到(x,y,z)的向量，用右手握住这条向量，大拇指指向向量的正方向，四指环绕的方向就是旋转的方向；

函数功能：以点(0,0,0)到点(x,y,z)为轴，旋转angle角度；

### 3. 比例缩放

    void glScalef(GLfloat x,GLfloat y,GLfloat z);

  沿X轴方向缩放比

  沿Y轴方向缩放比

  沿Z轴方向缩放比

    #include<iostream>
    using namespace std;
    #include<gl/glut.h>
    #include <windows.h>
    
    void display(){
        glMatrixMode(GL_MODELVIEW);
        glClear(GL_COLOR_BUFFER_BIT);  
        glColor3f(1.0,1.0,1.0);  
        glRectf(100.0,150.0,200.0,250.0);
        //平移变换
        glLoadIdentity();
        glColor3f(1.0,0.0,0.0);//红色
        glTranslatef(50.0,50.0,0.0);
        glRectf(100.0,150.0,200.0,250.0);
        //旋转
        glLoadIdentity();
        glColor3f(0.0,1.0,0.0);//绿色
        glRotatef(10.0,0.0,0.0,1.0);//绕z轴
        glRectf(100.0,150.0,200.0,250.0);
        //放缩
        glLoadIdentity();
        glColor3f(0.0,0.0,1.0);//蓝色
        glScalef(1.5,1.0,1.0);
        glRectf(100.0,150.0,200.0,250.0);
        glFlush();  
    }
    
    void reshape(int w,int h){ 
        glViewport(0,0,(GLsizei)w,(GLsizei)h); 
        glMatrixMode(GL_PROJECTION); 
        glLoadIdentity(); 
        gluOrtho2D(0.0,(GLsizei)w,0.0,(GLsizei)h); 
    } 
    
    int main(int argc,char **argv){  
        glutInit(&argc,argv);  
        glutInitDisplayMode(GLUT_RGB|GLUT_SINGLE);  
        glutInitWindowSize(500,500);   
        glutCreateWindow("练习");  
        glutDisplayFunc(display);  
        glutReshapeFunc(reshape);  
        glutMainLoop();  
        return 0;  
    } 

![](https://pic2.superbed.cn/item/5dfac88476085c3289b481b4.jpg)

![](https://pic3.superbed.cn/item/5dfac8bb76085c3289b48d1c.jpg)

![](https://pic3.superbed.cn/item/5dfac91b76085c3289b49ee5.jpg)

    void display()
    {
            glClear(GL_COLOR_BUFFER_BIT); //清屏

            glMatrixMode(GL_MODELVIEW);   //矩阵模式置设
            glLoadIdentity();             //清空矩阵堆栈
            gluLookAt(0.0, 2.0, 0.0, 0.0, 0.0, 0, 1, 0, 0.0);     //设置视点

            glMatrixMode(GL_PROJECTION);
            glLoadIdentity();
            glOrtho(-1, 1, -1, 1, -1,1);//定义观察体

            glColor3f(1.0, 1.0, 1.0);
            glutWireTeapot(0.5);   //绘制立方体，中心在坐标原点
            glFlush();   //用于强制刷新缓冲
    }


## 五、计算题

>1、根据 4 个点的坐标，构造三次贝塞尔曲线，贝塞尔曲线的参数表达式，根据参数 t 的值计算曲线上点的坐标值。 

![](https://pic3.superbed.cn/item/5dfa1cb976085c328998e18b.jpg)

>2、给定某图形的顶点坐标，绕任一直线做镜像，旋转等变换，变换矩阵、变换过程、变换后的坐标值。

![](https://pic3.superbed.cn/item/5dfabe2476085c3289b2e917.jpg)

![](https://pic2.superbed.cn/item/5dfacc4a76085c3289b52801.jpg)