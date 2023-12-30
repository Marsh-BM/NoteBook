# COMP338

# Lecture01 Introduction

## 1.Module Syllabus

![image-20231005171733675](D:\笔记\笔记图片\image-20231005171733675.png)

![image-20231005171812354](D:\笔记\笔记图片\image-20231005171812354.png)

![image-20231005172223702](D:\笔记\笔记图片\image-20231005172223702.png)



### What is Computer Version?

![image-20231005172251949](D:\笔记\笔记图片\image-20231005172251949.png)

* 从数据图像中获得所需要的信息，包括世界的形象，现实物体的交互等



* **Researchers in AI have attempted to make the computers that have ability to “see” and “sense” the world around them**
* 人工智能研究人员试图让计算机能够“看到”和“感知”周围的世界

* Teach computers to gain **understanding** from digital images or videos -> Computer Vision
* 教计算机从数字图像或视频中获得理解->计算机视觉

* Understanding: transfer raw visual inputs to meaningful descriptions, e.g., keypoints, features, segments, image category, objects, etc.
* 理解:将原始视觉输入转换为有意义的描述，例如关键点、特征、片段、图像类别、物体等。



* 相关分支

![image-20231005173506171](D:\笔记\笔记图片\image-20231005173506171.png)

* **Image processing**– manipulation of an image
* **图像处理**--对图像的处处理

* **Computer graphics**– digitally synthesizing images	
* 计算机制图--数字合成图像	
  * Image Processing: Image → Image	
  * 图像处理： 图像 → 图像	
  * Computer Vision: Image → Description	
  * 计算机视觉： 图像 → 描述
  * Computer Graphics: Description → Image
  * 计算机图形学： 描述→图像
* **Pattern recognition**– recognise & classify stimuli in images/other datasets
* **模式识别-**-识别图像/其他数据集中的刺激物并进行分类
* **Photogrammetry**– obtaining measurements from images
* **摄影测量**--从图像中获取测量结果
* **Biological Vision**– understanding visual perception in humans and animals (studied in Neuroscience, Psychology, Psychophysics)
* **生物视觉**--了解人类和动物的视觉感知（在神经科学、心理学、心理物理学中进行研究）

![image-20231005173736342](D:\笔记\笔记图片\image-20231005173736342.png)

![image-20231005173806633](D:\笔记\笔记图片\image-20231005173806633.png)



![image-20231005173857378](D:\笔记\笔记图片\image-20231005173857378.png)

![image-20231005173907867](D:\笔记\笔记图片\image-20231005173907867.png)

* Optical character recognition (OCR) converts scanned documents to text.
* 光学字符识别 (OCR) 可将扫描文件转换为文本。
* Automatic number plate recognition (ANR) reads car licence plates.
* 自动车牌识别（ANR）可读取汽车牌照。

![image-20231005173923593](D:\笔记\笔记图片\image-20231005173923593.png)

![image-20231005173941903](D:\笔记\笔记图片\image-20231005173941903.png)

![image-20231005173957910](D:\笔记\笔记图片\image-20231005173957910.png)

![image-20231005174008092](D:\笔记\笔记图片\image-20231005174008092.png)

![image-20231005174021354](D:\笔记\笔记图片\image-20231005174021354.png)

![image-20231005174032755](D:\笔记\笔记图片\image-20231005174032755.png)



# Lecture02 Topic in Computer Science

## 2.Why is vision difficult?

![image-20231005174454363](D:\笔记\笔记图片\image-20231005174454363.png)

* If we replace the image by its numerical representation, the transformation into a description is less obvious.
* 如果我们用数字表示来代替图像，转化为描述就不那么明显了。
* Major Challenges:
  * 1**.One image → many interpretations problem is ill-posed**
  * 一个图像可能有多种不同的解释，这使得图像到描述的转换是一个复杂的问题。
  * 2.**One object → many images problem is exponentially large**
  * 表示一个物体可能在许多不同的图像中以不同的方式出现，这使得识别问题的规模指数级增长。

### 2.1 Vision is an ill-posed problem

* Mapping from world to image (3D to 2D) is **unique (well-posed).**
* 从世界到图像(3D到2D)的映射是**独特的**(良好的定位)。
* 这表示在三维空间中的物体或场景，通过某种方式被映射到二维图像上，这个映射是唯一的和明确定义的。通常，这是因为从三维到二维的映射是可逆的，你可以唯一地**确定三维空间中的点对应到二维图像中的像素。**
  *  This is a “forward problem” (i.e. imaging).
* Mapping from image to world (2D to 3D) is **NOT unique (ill-posed)**
* 从图像到世界(2D到3D)的映射不是唯一的(病态的)
* 从二维图像到三维空间的映射通常是不唯一的，因**为从二维到三维的映射是一个信息丢失的过程**。在一个二维图像上，你可能无法确定物体在三维空间中的确切位置和方向，**因为一个像素可能对应于多个可能的三维坐标**。这使得这个问题变得模糊和不明确，因此被称为"ill-posed"。
  * This is an “inverse problem” (i.e. vision)

* For any given image there are many objects that could have generated that image.
* 对于任何给定图像，都有许多物体 可以生成该图像。
* **<font color=red>Solved using constraints or priors: which make some interpretations more likely than others</font>** (usually the brain produces one interpretation from the many possible ones)
* **使用约束条件或先验条件来解决：这些约束条件或先验条件使 使某些解释比其他解释更有可能** (通常大脑会从众多可能的解释中 从众多可能的解释中产生一种解释）

![image-20231005180313193](D:\笔记\笔记图片\image-20231005180313193.png)

### 2.2 Viewpoint affects appearance 视角影响

![image-20231005180539945](D:\笔记\笔记图片\image-20231005180539945.png)

* **Viewpoint affects appearance**
* **视角影响外表**
* A single object seen from different viewpoints can vary greatly in appearance (object orientation, retinal location, scale, etc. all affect appearance).
* 从不同的角度看同一个物体，其外观会有很大的差异(物体的方向、视网膜的位置、尺度等都会影响外观)。
* The resulting images have very little similarity
* 同一个结果图会很少相似

### 2.3 Illumination affects appearance 光照影响

* **Illumination affects appearance**
* **光照影响外观**

![image-20231005181131927](D:\笔记\笔记图片\image-20231005181131927.png)

* A single object seen under different lighting conditions can vary greatly in appearance.
  The resulting images have little similarity.
* 同一个物体在不同的光照条件下，其外观会有很大的不同。得到的图像几乎没有相似之处。

### 2.4 Non-rigid deformations affect appearance 非刚性变化影响

![image-20231005181301109](D:\笔记\笔记图片\image-20231005181301109.png)

* **Non-rigid deformations affect appearance**
* **非刚性变形影响外观**
* A single object can undergo deformations which cause it to vary greatly in appearance. The resulting images have little similarity
* 单个物体会发生变形，导致其外观变化很大。得到的图像几乎没有相似之处

### 2.5 Within-category variation in appearance 类别内外观影响

![image-20231005181545446](D:\笔记\笔记图片\image-20231005181545446.png)

* **Within-category variation in appearance**
* **类别内外观的变化**
* Objects forming a single category can vary greatly in appearance. The resulting images have little similarity.
* 形成单一类别的物体在外观上可能差别很大。得到的图像几乎没有相似之处。



## 3. Topics Computer Vision

### 3.1 Image classification 图像分类

![image-20231005182034186](D:\笔记\笔记图片\image-20231005182034186.png)

* Input: Image
* Output: image class(es)
* Common datasets
  * MNIST: hand-writing digits
  * CIFAR10, CIFAR100
  * ImageNet (with 1000 classes)

### 3.2 Object detection 物体检测

![image-20231005182232918](D:\笔记\笔记图片\image-20231005182232918.png)

* Input: image
* Output: object bounding boxes and labels
* Dataset:
  * Pascal VOC (20 object classes)
  * MS-COCO (80 object classes)

### 3.3 Image Segmentation 图像分割

![image-20231005182433226](D:\笔记\笔记图片\image-20231005182433226.png)

![image-20231005183611583](D:\笔记\笔记图片\image-20231005183611583.png)



### 3.4 Semantic segmentation 语义分割

![image-20231005182640759](D:\笔记\笔记图片\image-20231005182640759.png)

![image-20231005183630613](D:\笔记\笔记图片\image-20231005183630613.png)

* **<font color=red>在这种任务中，我们关注的是图像中的物体类别，而不考虑相同类别中不同实例之间的区别。</font>**

### 3.5 Instance segmentation 实例分割

![image-20231005182734214](D:\笔记\笔记图片\image-20231005182734214.png)

![image-20231005183652644](D:\笔记\笔记图片\image-20231005183652644.png)

* **<font color=red>与语义分割不同，实例分割区分同一类别中不同的物体实体，允许在图像中精确地定位和标识各个物体实例。</font>**



### 3.6 Image search 图像搜索

![image-20231005182847029](D:\笔记\笔记图片\image-20231005182847029.png)

### 3.7 Image Generation 图像生成

![image-20231005182920059](D:\笔记\笔记图片\image-20231005182920059.png)

![image-20231005182941346](D:\笔记\笔记图片\image-20231005182941346.png)

# Lecture03 Image Formation

How to tackle the challenges in vision?

如何应对视觉方面的挑战?

![image-20231020182056720](D:\笔记\笔记图片\image-20231020182056720.png)

* 不变的特征

![image-20231020182137009](D:\笔记\笔记图片\image-20231020182137009.png)

![image-20231020182217803](D:\笔记\笔记图片\image-20231020182217803.png)

![image-20231020182241308](D:\笔记\笔记图片\image-20231020182241308.png)

## 4.Image Formation  图像形成

![image-20231020182404811](D:\笔记\笔记图片\image-20231020182404811.png)

![image-20231020182754704](D:\笔记\笔记图片\image-20231020182754704.png)

* Light from a radiation source is reflected by surfaces in the world.
* 来自辐射源的光被物体表面反射。
* Reflected light from  hits the sensor.
* 来自传感器的反射光。

* **<font color=red>Images are formed when a SENSOR registers RADIATION that has interacted with PHYSICAL OBJECTS</font>**
* **<font color=red>当传感器记录与物理对象相互作用的辐射时，图像就形成了</font>**

![image-20231020183042395](D:\笔记\笔记图片\image-20231020183042395.png)

* **“Focus”** means that all rays coming from a scene point converge into a single image point.
* **"聚焦 "**是指从一个场景点射出的所有光线都汇聚到一个成像点。
* **“Exposure”** is the time needed to allow enough light through to form an image (the smaller the aperture, the longer the exposure time).
* **"曝光 "**是指让足够的光线通过以形成图像所需的时间（光圈越小，曝光时间越长）。
* The longer the exposure the more blurred an image is likely to be.
* 曝光时间越长，图像就可能越模糊。



* **Restricts the flow of light** (using a small hole) so that only one ray from each point in the world reaches the sensor.
* **限制光流（使用 一个小孔）**，使世界上每一点只有一条 光线到达传感器。到达传感器。

### 4.1 Perspective Camera Model 透视摄像机模型

![image-20231020183134348](D:\笔记\笔记图片\image-20231020183134348.png)

* P: a scene point with coordinates (x,y,z), 
* P: 场景点，坐标为 (x,y,z)、 
* P': its image with coordinates (x', y',z')
* P'：其图像，坐标为（x', y',z')
* **O: origin (pin hole)**
* **O：原点（针孔）**
* C’: image centre (intersection of optical axis and image plane)
*  C'：图像中心（光轴与图像平面的交点）

* **Image plane Π'** is located at a distance f’ from the pinhole along the vector k 
* **图像平面 Π'** 位于针孔与矢量 k 的距离 f' 处 
* **Optical axis**: line perpendicular to image plane and passing through O
* **光轴**：垂直于像平面并通过 O 的直线

![image-20231218020804452](D:\笔记\笔记图片\image-20231218020804452.png)

* 这里是一个简单的三角形相似来求解的公式

![image-20231218021023345](D:\笔记\笔记图片\image-20231218021023345.png)

* All coordinates are relative to camera reference frame [mm] 
  – i.e., axes rigidly attached to camera with origin at pinhole
* 所有坐标都是相对于照相机参照系 [mm毫米] 的。
  - 即与相机刚性连接的轴，原点位于针孔处

![image-20231218022054957](D:\笔记\笔记图片\image-20231218022054957.png)

### 4.2 Relating pixels to camera coordinates  像素与摄像机坐标的关系

* Relating pixels to camera coordinates

* 像素与摄像机坐标的关系

* **To convert from camera reference frame[mm] to image reference frame [pixel],we need to take account of:**

* **要将摄像机参照系[毫米]转换为图像参照系[像素]，我们需要考虑以下因素：**

  * Origin of image (in corner, not centre)
  * 图像的原点（在角落，而不是中心）
  * Pixel size (sx, sy [mm/pixel])
  * 像素大小（sx、sy[毫米/像素）

  ![image-20231218022611109](D:\笔记\笔记图片\image-20231218022611109.png)

* **Intrinsic camera parameters**
* **摄像机固有参数**
* This is only an approximation, due each individual camera having small manufacturing errors (i.e. the image plane may not be perfectly perpendicular to the optical axis, or may be rotated slightly about the optical axis ('skew’))
* 这只是一个近似值，因为每台摄像机都有微小的制造误差（即图像平面可能不完全垂直于光轴，或可能围绕光轴略有旋转（"偏斜"））。

### 4.3 Relating pixels to world coordinates 像素与现实世界的坐标关系

![image-20231218023029412](D:\笔记\笔记图片\image-20231218023029412.png)

![image-20231218023338963](D:\笔记\笔记图片\image-20231218023338963.png)

* 相机内参和相机外参和投影





# Lecture04 Low Level Vision

* **<Font color=red size=5>projection 投影</font>**

![image-20231218221953142](D:\笔记\笔记图片\image-20231218221953142.png)

![image-20231218222003360](D:\笔记\笔记图片\image-20231218222003360.png)

### 5.Digitalization 数字化

![image-20231218222056726](D:\笔记\笔记图片\image-20231218222056726.png)

* The **<font size=5>scene</font>** is a continuous function, is sampled at discrete points (called picture elements or pixels for short).
* 场景是一个连续的函数，在离散的点（称为图像元素，简称像素）上采样。
* Value of each pixel = measure of light intensity at that point. 
* 每个像素的值=该点的光照强度。 

* ![image-20231218222109639](D:\笔记\笔记图片\image-20231218222109639.png)

* **A digital image is usually denoted as I. 数字图像通常用 I 表示。**
  * I is a matrix of pixel values
  * I 是像素值矩阵
  * Origin is top left corner
  * 原点为左上角

* Note: in mathematics (and Python, Matlab etc), I(r,c) would refer to the rth row and the cth column of I, so I is the transpose of a matrix in standard format. 
* 注：在数学（以及 Python、Matlab 等）中，I(r,c) 指 I 的第 r 行和第 c 列，因此 I 是标准格式矩阵的转置。



### 6.Image representation 图像表示法

* **<font size=5 color=red>Monochrome 单色</font>**

* **Binary or Monochrome:**
* **二进制或单色：**
  * 1 binary value per pixel, 1-bit ⇒ 2 discrete levels. 
  * 每个像素 1 个二进制值，1 位 ⇒ 2 个离散级。
  * I(p) = 0 or 1.
  * I(p) = 0 或 1。
* **Greyscale or Intensity:**
* **灰度或强度：**
  * 1 real value per pixel, typically 8-bit ⇒ 256 discrete levels.
  * 每个像素 1 个实值，通常为 8 位 ⇒ 256 个离散级别。
  * I(p) ∈ [0,1]

![image-20231218223145211](D:\笔记\笔记图片\image-20231218223145211.png)



![image-20231218223241459](D:\笔记\笔记图片\image-20231218223241459.png)

* Colour image representation (RGB)
* 彩色图像表示法（RGB）



![image-20231218223347849](D:\笔记\笔记图片\image-20231218223347849.png)

* RGB(红蓝绿)转换为灰度图像

![image-20231218224612449](D:\笔记\笔记图片\image-20231218224612449.png)



![image-20231218224638786](D:\笔记\笔记图片\image-20231218224638786.png)

![image-20231219001136671](D:\笔记\笔记图片\image-20231219001136671.png)



### 7. Image manipulation 图像处理

*  Shrinking and zooming  缩小和放大
* Shrinking / sub-sampling– Can be seen as **under sampling  缩小/次采样--可视为采样不足** 
* Zooming / up-sampling 缩放/上采样
  * – Can be seen as **over sampling**
  * 可视为**过度采样**
    * – Creation of new pixel locations
    * 创建新的像素位置
    * – Assignment of grey level to those locations 
    * 为这些位置分配灰度级 
  * Interpolation 
  * 插值 

![image-20231218224819140](D:\笔记\笔记图片\image-20231218224819140.png)

#### 7.1 Shrinking/sub-sampling 收缩/子采样

##### 7.1.1**<font size=5>Pixels are removed according to a given pattern</font>**

* **根据给定模式删除像素**

![image-20231218225210450](D:\笔记\笔记图片\image-20231218225210450.png)



##### 7.1.2 **<font size=5>Pixels are removed according to a given pattern</font>**

* **根据给定模式删除像素**

![image-20231218225522989](D:\笔记\笔记图片\image-20231218225522989.png)



#### 7.2 Zooming/up-sampling 放大/扩采样

* Objective
* 目标
  * – to increase **the resolution** 
  * 提高**分辨率**
* Procedure 程序
  * – requires generation of **additional pixels** from available ones – usually geometric transforms require interpolation 
  * 需要从现有像素中生成**额外像素** - 通常几何变换需要插值 
* Example
  * – the simplest form is approximation by the **nearest** available pixel 
  * 最简单的形式是用最近的可用像素逼近

![image-20231218230011860](D:\笔记\笔记图片\image-20231218230011860.png)





##### 7.2.1 Nearest Neighbour Interpolation 最近邻插值

![image-20231218232947918](D:\笔记\笔记图片\image-20231218232947918.png)

*  Nearest Neighbour Interpolation   最近邻插值
* **<font size=5>Copies an adjacent pixel value from the same colour channel.</font>** 
* **复制同一颜色通道的相邻像素值。**
  * Pro: Fast
  * 专业 快速
  * Con: Inaccurate
  * 缺点：不准确

![image-20231218233053954](D:\笔记\笔记图片\image-20231218233053954.png)



* **<font size=5>Takes average value of nearest two or four pixels from the same colour channel.</font>**
* **取同一颜色通道中最接近的两个或四个像素的平均值**。
  * Fast
  * 快速
  * **Accurate in smooth regions, inaccurate at <font color=violet size=5>edges</font>**
  * **在平滑区域准确，在边缘不准确**

![image-20231218233426267](D:\笔记\笔记图片\image-20231218233426267.png)

![image-20231218234506826](D:\笔记\笔记图片\image-20231218234506826.png)



#### 7.3 Transformations 转变

![image-20231218234533834](D:\笔记\笔记图片\image-20231218234533834.png)

##### 7.3.1 Spatial Transformations 空间变换



![image-20231218234541243](D:\笔记\笔记图片\image-20231218234541243.png)



* **Moves a point to a new location by**
* **通过在点的坐标上添加平移量**
* **– adding translation amounts to the coordinates of the point** 
* **将点移动到新位置**

![image-20231218234548580](D:\笔记\笔记图片\image-20231218234548580.png)

#### 7.3.2  Scaling缩放 and rotation 旋转



![image-20231218234555965](D:\笔记\笔记图片\image-20231218234555965.png)

![image-20231218234604958](D:\笔记\笔记图片\image-20231218234604958.png)

![image-20231218234615514](D:\笔记\笔记图片\image-20231218234615514.png)



# Lecture05 Low Level Vision

* **<font color=red size=5>Filtering and convolution</font>**
* **滤波和卷积**
* **<font color=red size=5>Example filters/masks</font>**
* **滤波器/掩码示例**

![image-20231112002655937](D:\笔记\笔记图片\image-20231112002655937.png)

* 滤波和卷积

![image-20231112002816303](D:\笔记\笔记图片\image-20231112002816303.png)

![image-20231112002833846](D:\笔记\笔记图片\image-20231112002833846.png)

## 5.Filtering and Convolution 滤波和卷积

* **<font color=red>Doing convolution using different filters/kernels</font>**
* **使用不同的滤波器/核进行卷积**

![image-20231112003004330](D:\笔记\笔记图片\image-20231112003004330.png)

![image-20231112003312928](D:\笔记\笔记图片\image-20231112003312928.png)

* 1. Multiply each mask element by the corresponding image pixel value
* 2. Sum these products and write answer in corresponding pixel location in the output image
* 1. 将每个掩码元素乘以相应的图像像素值
* 2. 将这些乘积相加，并将答案写入 输出图像中的相应像素位置 图像

![image-20231112004345393](D:\笔记\笔记图片\image-20231112004345393.png)

* 这里解释一下什么是滤波
* **滤波在图像处理中指通过滤波器（即卷积核）对图像进行修改或增强的过程**
* 你看，这里很明显**<font color=red>将一个3X3的矩阵变成了一个1X1的矩阵</font>**。
* 在图像处理中，当我们使用一个滤波器（或称为卷积核）进行卷积操作时，滤波器覆盖图像的一小块区域（在这个例子中是一个3x3的区域），并将这块区域内的像素值与滤波器的相应权重相乘后求和，这个求和的结果就是新图像在该位置的单个数值。
* 这个操作的目的是将覆盖区域内多个像素的信息综合到一个像素值中，**<font color=red>通常是为了提取特征</font>**（如边缘或纹理）或者实现某种效果（如模糊或锐化）。每个滤波器设计成具有不同的权重，可以捕捉不同的图像特性。例如，边缘检测滤波器能够识别像素值突变的区域，模糊滤波器则平滑像素值的变化。



* 另外，因为图像的边缘没有足够的像素点来覆盖整个区域，一般会采用其他方法来解决这个问题。
* **填充 (Padding)**: 在图像周围添加额外的像素。填充的像素可以是零（零填充），可以是边缘像素的复制（边缘复制），或者是镜像边缘像素（镜像填充）。
* **忽略边缘 (Ignore edges)**: 只在卷积核可以完全覆盖图像区域的地方应用卷积。这将导致输出图像比输入图像小。
* **裁剪 (Crop)**: 在卷积后，只保留中心区域，移除边缘像素。

![image-20231112010445617](D:\笔记\笔记图片\image-20231112010445617.png)

![image-20231112022143941](D:\笔记\笔记图片\image-20231112022143941.png)

![image-20231112022204625](D:\笔记\笔记图片\image-20231112022204625.png)

* **这里的边缘值被视为0, 不考虑边缘值**，所以
  * -1 * -1 + -1 * -1 + 0 * 1 + 1 * -1 + 2 * 0 + 2 * 1 + 0 * 0 + 1 * 1 + 4 * 1 = 6

![image-20231112052349352](D:\笔记\笔记图片\image-20231112052349352.png)

![image-20231112052401636](D:\笔记\笔记图片\image-20231112052401636.png)

![image-20231112052411462](D:\笔记\笔记图片\image-20231112052411462.png)

![image-20231112052419465](D:\笔记\笔记图片\image-20231112052419465.png)

![image-20231112052428718](D:\笔记\笔记图片\image-20231112052428718.png)

![image-20231112052621740](D:\笔记\笔记图片\image-20231112052621740.png)

![image-20231223143422862](D:\笔记\笔记图片\image-20231223143422862.png)

* **No border handling**
* **无边框处理**
  * **Border is not filtered**
  * **不过滤边框**
* **Change filter size along the border**
* **沿边框改变过滤器大小**
* **Padding: Put values outside image border**
* **填充： 将值置于图像边框外**
  * Fill with zeros (clipping)
  * 用零填充（削边）
  * Periodic extension of the image
  * 图像的周期性扩展
  * Mirror the borders
  * 镜像边界

![image-20231112052926609](D:\笔记\笔记图片\image-20231112052926609.png)

### 5.1 Example masks/filter

* The values chosen for the mask determine the effects of the convolution
* 为掩码选择的值决定了卷积的效果

![image-20231112053051000](D:\笔记\笔记图片\image-20231112053051000.png)

* 每一个像素都被自己替换，所以没什么用

![image-20231112053150397](D:\笔记\笔记图片\image-20231112053150397.png)

![image-20231112053302709](D:\笔记\笔记图片\image-20231112053302709.png)

![image-20231112053330266](D:\笔记\笔记图片\image-20231112053330266.png)



* 每一个像素都被它左边的像素替换，作用不大**（这里好像写错了，应该是全部向右移动）**

![image-20231112053345432](D:\笔记\笔记图片\image-20231112053345432.png)



![image-20231112053956724](D:\笔记\笔记图片\image-20231112053956724.png)

![image-20231112054016192](D:\笔记\笔记图片\image-20231112054016192.png)

![image-20231112054023349](D:\笔记\笔记图片\image-20231112054023349.png)



# Lab 03_Image Manipulation

* 图像的阈值处理

![image-20231112063731263](D:\笔记\笔记图片\image-20231112063731263.png)

![image-20231112073348036](D:\笔记\笔记图片\image-20231112073348036.png)



# Lecture06 Low Level Vision

## 6.1 Edge Detection 边缘检测

![image-20231223143959587](D:\笔记\笔记图片\image-20231223143959587.png)

* 顾名思义，检测一个图片物体的边缘，具体可以惨Lecture02
* Convert a 2D image into a set of curves
* 将二维图像转换成一组曲线
* Extracts salient features of the scene
* 提取场景的显著特征
* More compact than pixels
* 比像素更紧凑

### 6.1.1 Origins of edges 边缘的起源

* **surface normal discontinuity**
* **表面法线不连续**
* **depth discontinuity**
* **深度不连续性**
* **surface color / illumination discontinuity**
* **表面颜色/光照不连续**

![image-20231223150257798](D:\笔记\笔记图片\image-20231223150257798.png)

![image-20231223144357568](D:\笔记\笔记图片\image-20231223144357568.png)

![image-20231223150321365](D:\笔记\笔记图片\image-20231223150321365.png)

![image-20231223150332417](D:\笔记\笔记图片\image-20231223150332417.png)



![image-20231223150341761](D:\笔记\笔记图片\image-20231223150341761.png)



![image-20231223151009845](D:\笔记\笔记图片\image-20231223151009845.png)



* 高中的求导，这里计算斜率来判断边缘，因为按照图像的亮度变化速度，这个方法可以检测出图像中亮度变化最大的地方。
* ![image-20231223151356254](D:\笔记\笔记图片\image-20231223151356254.png)
* 分数求导公式
* <img src="D:\笔记\笔记图片\images.jpeg" alt="分数求导公式" style="zoom:200%;" />

![image-20231223151439600](D:\笔记\笔记图片\image-20231223151439600.png)

![image-20231223151452849](D:\笔记\笔记图片\image-20231223151452849.png)

#### 6.1.1.1 Discrete derivative in 1D

![image-20231223151643748](D:\笔记\笔记图片\image-20231223151643748.png)

* 感觉这里的Central出现了一些问题需要解决，因为dx似乎不太对



![image-20231223152847132](D:\笔记\笔记图片\image-20231223152847132.png)



![image-20231223152823866](D:\笔记\笔记图片\image-20231223152823866.png)



#### 6.1.1.2 Discrete derivate in 2D

![image-20231223153229132](D:\笔记\笔记图片\image-20231223153229132.png)

* <font color=red size=5>Gradient 梯度， Magnitude大小</font>

![image-20231223153414367](D:\笔记\笔记图片\image-20231223153414367.png)

* **这里是一个与之相关的例子**

![image-20231223153519556](D:\笔记\笔记图片\image-20231223153519556.png)



![image-20231223153852833](D:\笔记\笔记图片\image-20231223153852833.png)

* 这里分别在X方向上和Y方向上应用了一个滤波器来进行卷积操作。
* **<font color=red>X轴卷积操作会突出显示水平方向上亮度变化显著的区域，即垂直边缘。</font>**
* **<font color=red>Y轴卷积操作会突出显示垂直方向上亮度变化显著的区域，即水平边缘。</font>**

![image-20231223154133296](D:\笔记\笔记图片\image-20231223154133296.png)

* An edge is a place of rapid change in the image intensity function.
* 边缘是图像强度函数快速变化的地方

![image-20231223154239491](D:\笔记\笔记图片\image-20231223154239491.png)



* <font color=red size=5>这里先解释一下什么是梯度：**在数学上，梯度是一个向量，它指向函数增长最快的方向，并且其长度（或大小）是增长率的度量。**</font>



* 那么我们通过Roberts和Sobel矩阵（卷积核）与图像的每个像素及其邻域像素进行卷积运算，输出一个新的图像，其亮度值代表了原始图像在对应点的梯度大小。较大的梯度值通常表示边缘的存在。通过这些方法，可以从原始图像中提取出有用的结构信息，如物体的轮廓和形状。



![image-20231223155309363](D:\笔记\笔记图片\image-20231223155309363.png)





##### 6.1.1.2.1 Edge Operators 边缘运算符

![image-20231223160105079](D:\笔记\笔记图片\image-20231223160105079.png)



* 一个高斯，一个拉普拉斯也是用于边缘检测，但是目的和Roberts和Sobel有所不同

![image-20231223160430431](D:\笔记\笔记图片\image-20231223160430431.png)





# Lecture07 Feature Extraction

![image-20231223181014279](D:\笔记\笔记图片\image-20231223181014279.png)

* Why is a feature needed?
* Histogram features
* 直方图特征
* LBP features
* LBP 特征

## 7.1 Why is a feature needed?

* Correspondence Problem
* 对应问题
  * Finding matching image elements across views
  *  在不同视图中查找匹配的图像元素

![image-20231223181246789](D:\笔记\笔记图片\image-20231223181246789.png)

![image-20231223181414861](D:\笔记\笔记图片\image-20231223181414861.png)

* **Feature-based methods** 
* **基于特征的方法** 
  * Advantages
    * **− Relatively insensitive to illumination and size changes**
    * **对光照和尺寸变化相对不敏感**
  * Disadvantages
    * − Provides sparse correspondence map 
    * 提供稀疏的对应图 (这意味着只会观察图像中的某一小部分显示的特征点，比如边缘，并不涵盖每一个图像)
      * if correspondence required at intermediate locations this needs to be interpolated
      * 如果需要在中间位置进行对应，则需要进行内插  
      * **关于内插intermediate：**
      * ![image-20231223183204526](D:\笔记\笔记图片\image-20231223183204526.png)
      * sufficient for many applications
      * 足以满足许多应用
    * − Only suitable when “good” interest points can be extracted from the scene	
    * 只适合在场景中提取出好的兴趣点
      * doesn’t perform well with textured/random regions 	
      * 在纹理丰富或随机的区域，这种方法可能表现不佳，因为在这些区域可能难以找到稳定且可重复检测到的特征点。
      * choice of interest points is important 
      * 选择哪些兴趣点进行追踪和识别是非常重要的，这需要根据应用场景和目标任务来决定。

![image-20231223181425366](D:\笔记\笔记图片\image-20231223181425366.png)





## 7.2 Histogram Features 直方图特征

![image-20231223183347939](D:\笔记\笔记图片\image-20231223183347939.png)

* 在这张图里，我们可以得到关于相关的数值
* 左边有一个矩阵，代表数字图像的一部分。矩阵中的每个单元对应于图像中的一个像素，每个单元中的数字代表该像素的强度值。该特定图像使用非常有限的像素值范围（从 0 到 7），这可能表示灰度图像，其中 0 是黑色，7 是白色，中间的值是灰色阴影。
* 右侧有一个用作直方图的表格。它在第一列中列出离散像素值，在第二列中列出每个像素值在图像中出现的次数。该表是通过计算矩阵中每个像素值的频率来构建的。例如，像素值0出现86次，像素值1出现14次，等等。

![image-20231223183353667](D:\笔记\笔记图片\image-20231223183353667.png)

![image-20231223183427344](D:\笔记\笔记图片\image-20231223183427344.png)

* Histogram of an image with gray levels in the range [0, L-1] is a discrete function
* 灰度范围为 [0, L-1] 的图像的直方图是一个离散函数
* h (rk) = nk 
* **where rk is the kth gray level**
* **其中，rk 是第 k 个灰度级**
* **<font color=red size=5>nk is the number of pixels in the image having gray level rk</font>**
* **nk 是图像中具有 rk 灰度级的像素数**
* 例如，如果 *rk* 是灰度级128，而 *nk* 是200，这意味着图像中有200个像素的灰度值是128。

* nk是具有rk灰度级的像素数量

![image-20231224120324713](D:\笔记\笔记图片\image-20231224120324713.png)

* Normalized histogram (probability) 
* 归一化直方图（概率） 
* **归一化直方图是一个表示图像中像素强度分布的工具，其中每个强度值的频率被转换为概率。**
* **p(rk )= nk / n** 
* **where n is the total number of pixels in the image.** 
* **其中，n 是图像中像素的总数。**

![image-20231224120907220](D:\笔记\笔记图片\image-20231224120907220.png)

* 将获得的直方图进行归一化，将nk/n，将直方图归一化

![image-20231224121505896](D:\笔记\笔记图片\image-20231224121505896.png)

![image-20231224122557385](D:\笔记\笔记图片\image-20231224122557385.png)

![image-20231224122654528](D:\笔记\笔记图片\image-20231224122654528.png)

* **Histogram is a many-to-one mapping** 
* **直方图是多对一的映射** 
* **Different images can have the same histogram**      
* **不同的图像可以具有相同的直方图** 
  * **Non invertible mapping!** 
  * **不可逆映射！**

![image-20231224122915123](D:\笔记\笔记图片\image-20231224122915123.png)

* Histogram is invariant to certain geometric image operations 
* 直方图不受某些几何图像操作的影响 
  * Rotation 
  * 旋转 
  * Scaling 
  * 缩放 
  * Mirroring 
  * 镜像 
  * Skew
  * 倾斜

![image-20231224123001942](D:\笔记\笔记图片\image-20231224123001942.png)

## 7.3 LBP Descriptors LBP 描述符

* describes the surroundings of a pixel 
* 描述像素周围的环境
* LBP 通过将每个相邻像素与中心像素进行比较来对像素周围的局部结构进行编码。结果是一个表示局部邻域模式的二进制数。
* generates a bit-code from the binary derivatives of a pixel 
* 根据像素的二进制导数生成位码
* based on the assumption that texture has locally two complementary aspects: 
* 基于纹理在局部上有两个互补方面的假设： 
  * a pattern, and 
  * its strength 

![image-20231224123440732](D:\笔记\笔记图片\image-20231224123440732.png)

* For each pixel p, create an 8-bit number **b1 b2 b3 b4 b5 b6 b7 b8** 
* 为每个像素 p 创建一个 8 位数字 **<font color=red>b1 b2 b3 b4 b5 b6 b7 b8</font>**
  * – if bi>C, bi=1      
  * 如果 bi>C, bi=1 
  * – else, if bi <=C, bi=0 
  * 否则，如果 bi <=C, bi=0 
* Represent the texture in the image (or a region) by **the histogram** of these numbers 
* 用这些数字的**直方图**表示图像（或区域）的纹理 

![image-20231225144122460](D:\笔记\笔记图片\image-20231225144122460.png)

![image-20231225145920963](D:\笔记\笔记图片\image-20231225145920963.png)

* 从原始图像中选择一个子图像。在这个子图像中，中心像素的值用来与它的邻居进行比较。
* 每个邻居的像素值如果大于或等于中心像素的值，则在二进制表示中相应的位置被标记为1；如果小于中心像素的值，则被标记为0。
* 这些二进制位串联起来形成一个新的二进制数。在这个例子中，从左上角开始顺时针（或者按照你选择的任何一致顺序）比较中心像素周围的像素值。这个顺序在LBP的提取过程中必须保持一致。
* **得到的二进制数（在幻灯片中是00111101）转换为十进制数，这个十进制数是LBP的索引。**
* **通过计算图像中每个像素的LBP索引，可以构建一个直方图，该直方图记录了整个图像中所有可能LBP值的频率。**

![image-20231225150254143](D:\笔记\笔记图片\image-20231225150254143.png)

![image-20231225151038492](D:\笔记\笔记图片\image-20231225151038492.png)



![image-20231225151208616](D:\笔记\笔记图片\image-20231225151208616.png)

![image-20231225151220866](D:\笔记\笔记图片\image-20231225151220866.png)





# Lecture08 FeatureBasedApplications - ImageClassification

## 8.1 Image Classification

* **<font color=red>Assigning an input image one label from a fixed set of categories</font>**
* **<font color=red>从一组固定类别中为输入图像指定一个标签</font>**

![image-20231225152034246](D:\笔记\笔记图片\image-20231225152034246.png)



### 8.1.1 Image Classification Challenges 图像分类的挑战

* viewpoint variation 视角变化

![image-20231225152802326](D:\笔记\笔记图片\image-20231225152802326.png)

* illumination conditions 照明条件

![image-20231225152938809](D:\笔记\笔记图片\image-20231225152938809.png)

* Scale variation  规模变化

![image-20231225152956522](D:\笔记\笔记图片\image-20231225152956522.png)

* Deformation 变形

![image-20231225153139287](D:\笔记\笔记图片\image-20231225153139287.png)

* Occlusion 闭塞

![image-20231225153206955](D:\笔记\笔记图片\image-20231225153206955.png)

* Background clutter 背景杂乱

![image-20231225153329158](D:\笔记\笔记图片\image-20231225153329158.png)

* Intra-class variation 同类差异

![image-20231225153552224](D:\笔记\笔记图片\image-20231225153552224.png)



### 8.1.2 Image Classification – Traditional Approach 传统方法

![image-20231225153644545](D:\笔记\笔记图片\image-20231225153644545.png)

* 这是一种传统的图像分类方法，查找边缘->查找角点->分类

![image-20231225154349116](D:\笔记\笔记图片\image-20231225154349116.png)

### 8.1.3 Image Classification – Machine Learning Approach 机器学习方法

![image-20231225154437847](D:\笔记\笔记图片\image-20231225154437847.png)

![image-20231225154452999](D:\笔记\笔记图片\image-20231225154452999.png)



* **Collect a dataset of images and labels**
* **收集图像和标签数据集**
* **Train a classifier**
* **训练分类器**
* **Evaluate on new images**
* **在新图像上进行评估**



### 8.1.4 Image Classification -KNN KNN方法

* kNN classifier takes a test image

  kNN 分类器获取测试图像

* Compare it to all training images

* 将其与所有训练图像进行比较

* Predict the label of the closest training image.

* 预测最接近训练图像的标签。

![image-20231225154826759](D:\笔记\笔记图片\image-20231225154826759.png)



### 8.1.5 Image Classification – Distance Metric 距离公制



![image-20231225154918569](D:\笔记\笔记图片\image-20231225154918569.png)



* 46+12+14+1+82+13+39+33+12+10+0+30+2+32+22+108 = 456



* **曼哈顿距离（Manhattan distance）**:也称为城市街区距离（City block distance），它通过计算两点在各维度上的绝对差值之和来度量距离。

* **L2距离（Euclidean distance）**: 这是最常见的距离度量方式，通常简称为欧几里得距离。它通过计算两点在各维度上差值的平方和，然后取平方根来度量距离。

![image-20231225160553038](D:\笔记\笔记图片\image-20231225160553038.png)





### 8.1.4 Image Classification – kNN

![image-20231225160916236](D:\笔记\笔记图片\image-20231225160916236.png)

![image-20231225161131818](D:\笔记\笔记图片\image-20231225161131818.png)

![image-20231225161121875](D:\笔记\笔记图片\image-20231225161121875.png)

![image-20231225161152470](D:\笔记\笔记图片\image-20231225161152470.png)



* Not effective in practice
* 实际效果不佳
* Slow testing time
* 测试时间慢
* Very slow when having more points – the curse of dimensionality
* 点数越多，速度越慢--维度诅咒

![image-20231225161447319](D:\笔记\笔记图片\image-20231225161447319.png)



![image-20231225171911770](D:\笔记\笔记图片\image-20231225171911770.png)

![image-20231225171903173](D:\笔记\笔记图片\image-20231225171903173.png)









#  Lecture09 Feature Based Application-Image Segmentation 图像分割



## 9.1 Image Segmentation

![image-20231225172443102](D:\笔记\笔记图片\image-20231225172443102.png)

![image-20231225172538744](D:\笔记\笔记图片\image-20231225172538744.png)



## 9.2 Image Segmentation Challenges 图像分割的挑战

![image-20231225172819947](D:\笔记\笔记图片\image-20231225172819947.png)

* Oversegmentation: 过度分割。**当算法将图像划分为过多的片段或部分时，就会发生这种情况。**在提供的图像中，蒙娜丽莎的头发被分割成多个部分，而理想情况下，它应该被识别为一个连续的部分。
* Undersegmentation:分割不足。**当分割算法将应分离的不同对象或特征组合在一起时，就会发生这种情况。**在图像中，水与树木被归为一组，这表明该算法没有检测到它们之间的清晰边界。

![image-20231225172848597](D:\笔记\笔记图片\image-20231225172848597.png)

## 9.3 Image Segmentation Applications 图像分割的应用

* 用于交通方面

![image-20231225173403707](D:\笔记\笔记图片\image-20231225173403707.png)

* 用于医学

![image-20231225173549558](D:\笔记\笔记图片\image-20231225173549558.png)

## 9.4 Image Segmentation - Approaches 图像分割的方法

![image-20231225173646486](D:\笔记\笔记图片\image-20231225173646486.png)

* Splitting 分割
  * start with **<font color=red>single region</font>** covering entire image
  * 从覆盖整个图像的**单一区域**开始
  * repeat: split inhomogeneous regions
  * 重复：分割不均匀区域
  * even better:
  * 更好
    * **repeat split cluster to yield two distant components (difficult)**
    * **重复：分割群集以产生两个相距较远的部分（困难）**
* Merging
* 合并
  * start with **each pixel** as a separate region
  * 开始时将每个**像素**作为一个单独的区域
  * repeat:  merge adjacent regions if union is homogeneous -> **<font color=red>Region Growing</font>**
  * 重复：如果合并是同质的，则合并相邻区域 -> **区域生长**
  * even better
  * 甚至更好
  * **repeat: merge two closest clusters -> <font color=red>Region Merging</font>**
  *  **重复：合并两个最接近的集群 -> 区域合并**



*  Methods:
  * Thresholding
  * 阈值处理
  * Region-based
  * 基于区域
  * Watershed algorithm
  * 分水岭算法
  * Normalized (graph) cuts
  * 归一化（图形）切割



### 9.4.1 Segmentation - Thresholding

![image-20231225181126205](D:\笔记\笔记图片\image-20231225181126205.png)

* **Regions defined by differences in brightness.**
* **根据亮度差异定义区域。**
  * I'(x,y) = 1, if I(x,y)>threshold
  * 如果 I(x,y)>阈值，则 I'(x,y) = 1
  * I'(x,y) = 0, otherwise
  * I'(x,y) = 0，否则
* This results in two groups, i.e.,  foreground and background.
* 这样就产生了两组，即前景和背景。
* 将一张正常图像转换成了黑白图像

![image-20231225181214654](D:\笔记\笔记图片\image-20231225181214654.png)

![image-20231225181544643](D:\笔记\笔记图片\image-20231225181544643.png)

![image-20231225181602655](D:\笔记\笔记图片\image-20231225181602655.png)

## 9.5 Region based Image Segmentation

* A fundamental drawback of thresholding is that **<font color=red>it does not take into account spatial information.</font>**
* 阈值法的一个**基本缺点是不考虑空间信息**
* Region based segmentation methods take into account **the location** of each pixel as well as **its intensity,** or **colour**, or **texture** (or which ever other features or combination of features are being used to define similarity).
*  基于区域的分割方法既考虑每个**像素的位置**，也考虑其**强度**、**颜色或纹理**（或其他用于定义相似性的特征或特征组合）

![image-20231225182839149](D:\笔记\笔记图片\image-20231225182839149.png)

### 9.5.1 Region based-Region growing

* Start with one “seed” pixel, chosen **arbitrarily**
* 从任意选择的一个 "种子 "像素开始
  * **Give this pixel a label (defining the region it belongs to)**
  * **给这个像素一个标签（定义它所属的区域）** 
  * **Examine all the unlabelled pixels neighbouring labelled pixels**
  * **检查所有与已贴标签像素相邻的未贴标签像素** 
  * **If they are within similarity threshold, give them the same region label** 
  * **如果它们在相似性阈值内，则给它们贴上相同的区域标签** 
* Repeat until region stops growing, **then choose another seed pixel which does not yet belong to any region and start again.** 
* 重复上述过程，直到区域停止增长，**然后选择另一个不属于任何区域的种子像素，重新开始。**
* Repeat the whole process until **all pixels have been assigned to a region.**
* 重复整个过程，**直到所有像素都被分配到一个区域。**

![image-20231225182929129](D:\笔记\笔记图片\image-20231225182929129.png)

### 9.5.2 Region based – Region merging

* Start with each pixel (or small square regions of pixels, e.g. 2x2, or 4x4 pixels) labelled as separate regions. 
* 将每个像素（或像素的小方形区域，如 2x2 或 4x4 像素）标记为单独的区域。
  * **A region's properties are compared with those of an adjacent region** 
  * **将一个区域的属性与相邻区域的属性进行比较** 
  * **If they match, they are merged into a larger region and the properties of the new region are computed.** 
  * **如果匹配，则合并为一个更大的区域，并计算新区域的属性。**
* Continue merging adjacent regions until **a region cannot be merged with any of its neighbours, it is marked `final'.** 
* 继续合并相邻区域，**直到某个区域无法与其任何相邻区域合并为止，并标记为 "最终"。**
* The whole process repeats until **all image regions are marked final.** 
* 整个过程重复进行，**直到所有图像区域都被标记为最终区域。**

![image-20231225183721319](D:\笔记\笔记图片\image-20231225183721319.png)

### 9.5.3 Region based - Clustering

* **A general class of methods for unsupervised classification of data (i.e. classes are not predefined).**
* **对数据进行无监督分类（即不预先确定类别）的一类通用方法。**
* These methods can be used to **group image elements based on similarity.**
* 这些方法可用于根据相似性对图像元素进行分组。

![image-20231225184240780](D:\笔记\笔记图片\image-20231225184240780.png)



#### 9.5.3.1 Clustering – k-means Clustering 聚类 - k 均值聚类

* A simple algorithm which assumes that there are k clusters (k is a parameter input to the algorithm)
* 假设有 k 个聚类（k 是输入给算法的参数）的简单算法

0. Randomly choose k points to act as cluster centres

   随机选择 k 个点作为聚类中心

1. Allocate each element to the cluster with the closest centre 

   将每个元素分配到中心最近的聚类中 

2. Compute new cluster centres as the mean position of the elements in each cluster

   计算新的聚类中心，作为每个聚类中元素的平均位置

3. Until the cluster centres are unchanged redo from step 1 

   直到簇中心不变，从步骤 1 开始重做 

* This process attempts to minimize the distance of each point to the centre of its cluster and will converge to a local minimum of: 
* 此过程试图最小化每个点到其聚类中心的距离，并将收敛到一个局部最小值：

![image-20231225185251257](D:\笔记\笔记图片\image-20231225185251257.png)

* where x_j is a vector representing the properties of the j_tℎ data point, and μ_i are the average properties of the data points in cluster i. 
* 其中，x_j 是表示 j_t 搭配数据点属性的向量，μ_i 是第 i 个群组中数据点的平均属性。

![image-20231225185343466](D:\笔记\笔记图片\image-20231225185343466.png)

* 无监督学习
* 需要要求k值
* **需要选择 k 的值**：在 k-means 聚类算法中，k 是要形成的簇的数量。选择正确的 k 值对于找到有意义的数据分组至关重要，这个值通常是根据数据集的特性和分析需求预先确定的。

![image-20231225185459339](D:\笔记\笔记图片\image-20231225185459339.png)

* **局部最优**：k-means 聚类可能会收敛到局部最优解，而不是全局最优解。这意味着算法可能会找到一个相对较好的解，但不一定是最佳的数据分组方式。

![image-20231225185749303](D:\笔记\笔记图片\image-20231225185749303.png)

* **需要选择 k 的值**：在 k-means 聚类算法中，k 是要形成的簇的数量。选择正确的 k 值对于找到有意义的数据分组至关重要，这个值通常是根据数据集的特性和分析需求预先确定的。
* **局部最优**：k-means 聚类可能会收敛到局部最优解，而不是全局最优解。这意味着算法可能会找到一个相对较好的解，但不一定是最佳的数据分组方式。
* **数据性质**：k-means 算法对数据的分布有一定的假设，它假设簇是凸形的（比如球形或椭圆形）。如果数据的实际分布不符合这些假设，k-means 算法可能无法很好地执行聚类。

![image-20231225185904502](D:\笔记\笔记图片\image-20231225185904502.png)

![image-20231225190425674](D:\笔记\笔记图片\image-20231225190425674.png)

* 图二仅使用颜色进行聚类
* 图三使用颜色和位置进行聚类



# Lecture10 Feature Extraction & Matching

## 10.1 Feature Extraction

* Feature/Descriptor Overview

* 功能/描述符概述

* Hand-crafted Features/Descriptor:

* 手工制作的特征/描述符：

  * Scale Invariant Feature Transform (SIFT)

    尺度不变特征变换（SIFT）

  * SURF: Speeded Up Robust Features (SURF)

  * SURF：加速鲁棒特征（SURF）

  * ORB: An efficient alternative to SIFT or SURF

  * ORB：SIFT 或 SURF 的高效替代方法

* Feature Matching and Its applications

* 特征匹配及其应用

![image-20231226223107066](D:\笔记\笔记图片\image-20231226223107066.png)



* **Definition: A distinctive attribute or aspect of something**
* **定义： 事物与众不同的属性或方面**
* How to distinguish one from others?
* 如何将一个人与其他人区分开来？
  * Height 身高
  * Gender 性别
  * w/wo glasses 戴眼镜
  * Hair color 头发颜色
  * Dress color 衣服颜色

![image-20231226223135217](D:\笔记\笔记图片\image-20231226223135217.png)

![image-20231226223342988](D:\笔记\笔记图片\image-20231226223342988.png)

![image-20231226223351631](D:\笔记\笔记图片\image-20231226223351631.png)

* To illumination 照明
* To translation 平移
* To scale 缩放
* To rotation 旋转
* To perspective projection 透视投影

![image-20231226223412443](D:\笔记\笔记图片\image-20231226223412443.png)



### 10.1.1 illumination 光照

![image-20231226224429906](D:\笔记\笔记图片\image-20231226224429906.png)

### 10.1.2 Scale

![image-20231226224437546](D:\笔记\笔记图片\image-20231226224437546.png)

### 10.1.3 Rotation 旋转

![image-20231226224446457](D:\笔记\笔记图片\image-20231226224446457.png)

### 10.1.4 Full Perspective 不同的视角

![image-20231226224453562](D:\笔记\笔记图片\image-20231226224453562.png)



## 10.2 What is a Feature/Descriptor?

* We want to represent a small region as a vector
* 我们希望用一个向量来表示一个小区域

![image-20231226224608015](D:\笔记\笔记图片\image-20231226224608015.png)

### 10.2.1 A Simple Normalized Descriptor 一个简单的标准化描述符

* **<font color=red>The simple descriptor just subtracts the center value from each of the neighbors to get the absolute value, including itself to normalize for lighting and exposure.</font>**
* **简单描述器只是从每个相邻值中减去中心值，得到绝对值，包括自身值，以便对光照和曝光进行归一化处理。**
* 为了提高效率，我们可以将其存储为一维向量: **156 145 1 155 0 1 116 100 96**

![image-20231226225214068](D:\笔记\笔记图片\image-20231226225214068.png)

#### 10.2.1.1 Properties of our Descriptor 描述符的性质

![image-20231226225655080](D:\笔记\笔记图片\image-20231226225655080.png)

* **<font color=red>Translation Invariant</font>**
* **<font color=red>平移不会改变描述符</font>**
* **<font color=red>Not scale invariant</font>**
* **<font color=red>尺寸变化会改变描述符</font>**
* **<font color=red>Not rotation invariant</font>**
* **<font color=red>旋转会改变描述符</font>**
* **<font color=red>Somewhat invariant to lighting changes</font>**
* **<font color=red>描述符对光照变化有一定的不变性，这意味着即使光照条件发生变化，描述符也能保持相对稳定，但这种不变性可能不是完全的。</font>**



#### 10.2.1.2 How to make our Descriptor “Rotation invariance” and “Translation invariance”?????????????????????????????????????????????

* Rotate patch（这里指的应该是一个小块） according to its dominant gradient orientation
* 通过梯度的方向来旋转补丁

![image-20231226230613071](D:\笔记\笔记图片\image-20231226230613071.png)

* 这个过程比较难以理解，大概如下

![image-20231226231302936](D:\笔记\笔记图片\image-20231226231302936.png)

* **其实意思就是，当你识别某个特征点时，有意的将其的方向与需要对比的描述符的方向保持一致来创造出即使旋转图像仍然可以识别的描述符。**



* Translation invariance 平移不变
* **描述符具有平移不变的特性，因为即使移动后，相对于该patch周围的图像依然没有改变，仍然保持在图像中的位置，所以Descriptor不会发生任何改变。可以使用直方图来说明**

![image-20231226231431323](D:\笔记\笔记图片\image-20231226231431323.png)

![image-20231226231849411](D:\笔记\笔记图片\image-20231226231849411.png)



### 10.2.1.3  Image Matching and Its applications

![image-20231226232004167](D:\笔记\笔记图片\image-20231226232004167.png)



![image-20231226232013141](D:\笔记\笔记图片\image-20231226232013141.png)



![image-20231226232021534](D:\笔记\笔记图片\image-20231226232021534.png)











# Lecture11 Feature Extraction & Matching__SIFT Feature



## 11.1 Recap: Designing a Descriptor 设计描述符

![image-20231113064050568](D:\笔记\笔记图片\image-20231113064050568.png)

Designing a Descriptor 设计描述符

* Translation Invariant
* 平移不变
* Not scale invariant
* 不具有比例不变性
* Not rotation invariant
* 不具有旋转不变性
* Somewhat invariant to lighting changes
* 对光照变化有一定的不变性

![image-20231113064310737](D:\笔记\笔记图片\image-20231113064310737.png)



## 11.2 Recap: Image Matching and Its Applications 图像匹配及其应用

![image-20231113065230389](D:\笔记\笔记图片\image-20231113065230389.png)

## 11.3 Scale Invariant Feature Transform (SIFT) 尺度不变特征变换 (SIFT)
![image-20231113065258574](D:\笔记\笔记图片\image-20231113065258574.png)

* A well-known approach to compute features in 2D images
* 在二维图像中计算特征的著名方法
* Extracts features that are
* **提取的特征**
  * **<font color=red>invariant to rotation and scaling</font>**
  * **不受旋转和缩放影响**
  * **<font color=red>partially invariant to changes in illumination</font>**
  * **部分不受光照变化的影响**
  * **<font color=red>partially invariant to affine transformations</font>**
  * **对仿射变换部分不变**
  * ![image-20231227001140361](D:\笔记\笔记图片\image-20231227001140361.png)
* The features generated are **highly distinctive**
* 生成的特征非常**独特**



### 11.3.1 SIFT – Main steps to extract SIFT features 提取 SIFT 特征的主要步骤

* Determine approximate location and scale of salient feature points (also called keypoints)
* 确定突出特征点（又称关键点）的大致位置location和比例scale
* Refine their location and scale
* 完善其位置location和规模scale
* Determine orientation(s) for each keypoint
* 确定每个关键点的方向
* Determine descriptors for each keypoint.
* 确定每个关键点的描述符。

![image-20231227001459598](D:\笔记\笔记图片\image-20231227001459598.png)



#### 11.3.1.1 Step 1: Approximate Key points detection 检测关键点的近似值

* **Look for intensity changes using the difference of Gaussians at two nearby scales:**
* **利用两个邻近尺度的高斯差来寻找强度变化：**

![image-20231227001607941](D:\笔记\笔记图片\image-20231227001607941.png)

* 

![image-20231227002401002](D:\笔记\笔记图片\image-20231227002401002.png)

* 这里使用了不同的Scale Space来分析图像

![image-20231227002643885](D:\笔记\笔记图片\image-20231227002643885.png)



![image-20231227002855556](D:\笔记\笔记图片\image-20231227002855556.png)

![image-20231227002914854](D:\笔记\笔记图片\image-20231227002914854.png)

![image-20231227002930661](D:\笔记\笔记图片\image-20231227002930661.png)

![image-20231227002938395](D:\笔记\笔记图片\image-20231227002938395.png)

![image-20231227002949535](D:\笔记\笔记图片\image-20231227002949535.png)

* 如果关键点的绝对值大于某个值，则保留它。如果小于，则移除。

![image-20231227003418712](D:\笔记\笔记图片\image-20231227003418712.png)



#### 11.3.1.2 Step 2: Refining keypoint location 步骤 2：完善关键点定位

* The keypoint location and scale is discrete - we can **interpolate** for greater accuracy.
* 关键点的位置和比例是离散的--我们可以通过**插值**来获得更高的精度。
* For this, we express the DoG function in a small 3D neighborhood around a keypoint (x1,y,,σ) by a second-order Taylor-series:
* 为此，我们用二阶泰勒序列来表示关键点 (x1,y,,σ) 周围小范围三维空间的 DoG 函数：

![image-20231227003903667](D:\笔记\笔记图片\image-20231227003903667.png)



* To find an extremum of the DoG values in this neighborhood, set the derivative of D(.) to 0.This gives us:
* 要在这一邻域找到 DoG 值的极值，可将 D(.) 的导数设为 0。将 D(.) 的导数设为 0：
* The keypoint location is updated.
* 更新关键点位置。
* **<font size=5>All extrema with |Dextremal| < 0.03, are discarded as “weak extrema" or “low contrast points”.</font>**
* **将所有 |Dextremal| < 0.03 的极值作为 "弱极值 "或 "低对比点 "丢弃。**
* |M| is the determinant of matrix M.
* |M|是矩阵 M 的行列式。

![image-20231227004600291](D:\笔记\笔记图片\image-20231227004600291.png)

* **<font size=5>Eliminating edge points</font>**
* **消除边缘点**
* Such a point has large principal curvature across the edge but a small one in the perpendicular direction
* 这样的点在边缘上的主曲率大，但在垂直方向上的主曲率小
* The principal curvatures can be calculated from a Hessian function or covariance matrix of gradient (Harris detector)
* 主曲率可通过赫塞斯函数或梯度协方差矩阵计算得出（哈里斯检测器）

![image-20231227005033426](D:\笔记\笔记图片\image-20231227005033426.png)

* The eigenvalues of H or C are proportional to the principal curvatures, so two eigenvalues shouldn't differ too much.
* H 或 C 的特征值与主曲率成正比，因此两个特征值不会相差太多。

![image-20231227005044655](D:\笔记\笔记图片\image-20231227005044655.png)

![image-20231227005100294](D:\笔记\笔记图片\image-20231227005100294.png)

![image-20231227005255197](D:\笔记\笔记图片\image-20231227005255197.png)

#### 11.3.1.3 Step 3: Assigning orientations 调整方向

![image-20231227005409593](D:\笔记\笔记图片\image-20231227005409593.png)

* 计算梯度的大小和方向在一个小窗口周围的关键点-在适当的规模。

![image-20231227005439256](D:\笔记\笔记图片\image-20231227005439256.png)



#### 11.3.1.4 Step 4: Descriptors for each keypoint

![image-20231227005642289](D:\笔记\笔记图片\image-20231227005642289.png)

![image-20231227005649878](D:\笔记\笔记图片\image-20231227005649878.png)



### 11.3.2 SIFT properties

* Very robust 
* 非常强大
* Can handle changes in viewpoint 
* 可以处理
  * up to about 60 degree out of plane rotation 
  * 平面外旋转最多约 60 度 
* Can handle significant changes in illumination 
* 能处理光照的重大变化
  * day vs. night 
* Fast and efficient
* 快速高效
  * can run in real time 
  * 可实时运行



# Lecture12 MachineLearning For Vision

![image-20231227141124202](D:\笔记\笔记图片\image-20231227141124202.png)



# 12.1 Image Classification

![image-20231227161346371](D:\笔记\笔记图片\image-20231227161346371.png)

![image-20231227161400037](D:\笔记\笔记图片\image-20231227161400037.png)

![image-20231227161425103](D:\笔记\笔记图片\image-20231227161425103.png)

### 12.1.1 Image Classification – Fashion MNIST Dataset

![image-20231227161440498](D:\笔记\笔记图片\image-20231227161440498.png)

### 12.1.2 Image Classification - CIFAR10 Dataset

![image-20231227161453979](D:\笔记\笔记图片\image-20231227161453979.png)

### 12.1.3 Image Classification - ImageNet Dataset

![image-20231227161459867](D:\笔记\笔记图片\image-20231227161459867.png)

![image-20231227161508903](D:\笔记\笔记图片\image-20231227161508903.png)





## 12.2 Parametric approach 参数方法

![image-20231227161940108](D:\笔记\笔记图片\image-20231227161940108.png)

![image-20231227161953030](D:\笔记\笔记图片\image-20231227161953030.png)

![image-20231227162008997](D:\笔记\笔记图片\image-20231227162008997.png)

* x: input image 输入图像
* W: learning weights (params) 学习权重
* b: bias 偏差



* **将扁平张量转换成向量**

![image-20231227162141892](D:\笔记\笔记图片\image-20231227162141892.png)

* ![image-20231227162711422](D:\笔记\笔记图片\image-20231227162711422.png)

![image-20231227162506873](D:\笔记\笔记图片\image-20231227162506873.png)

### 12.2.1 Linear Classifier Example

![image-20231227162747699](D:\笔记\笔记图片\image-20231227162747699.png)

* 根据绘制的直线的结果来判断图片物品属于哪一个类

![image-20231227162755709](D:\笔记\笔记图片\image-20231227162755709.png)



### 12.2.2 How to find W and b?

![image-20231227162950657](D:\笔记\笔记图片\image-20231227162950657.png)

* Start with random W and b, then find an optimal W and b that can minimize the loss
* 从随机的 W 和 b 开始，然后找出能使损失最小的最优 W 和 b
* **<font color=red size=5>Propagation 传播</font>**

![image-20231227163005641](D:\笔记\笔记图片\image-20231227163005641.png)

## 12.3 Loss Function 损失函数

* 损失函数是一个衡量分类器当前性能好坏的指标。它计算了分类器对于单个数据点的预测输出与真实标签之间的差距
* A loss function tells how good our current classifier is

![image-20231227163312005](D:\笔记\笔记图片\image-20231227163312005.png)

* ![image-20231227164208335](D:\笔记\笔记图片\image-20231227164208335.png)

![image-20231227164047608](D:\笔记\笔记图片\image-20231227164047608.png)

### 12.3.1 Multiclass Support Vector Machine (SVM) loss 多类支持向量机 (SVM) 损失

![image-20231227164945515](D:\笔记\笔记图片\image-20231227164945515.png)

![image-20231227164252709](D:\笔记\笔记图片\image-20231227164252709.png)

![image-20231227165058999](D:\笔记\笔记图片\image-20231227165058999.png)

* 这里很明显把猫认成车了。

![image-20231227165146901](D:\笔记\笔记图片\image-20231227165146901.png)

![image-20231227165700978](D:\笔记\笔记图片\image-20231227165700978.png)

![image-20231227165650580](D:\笔记\笔记图片\image-20231227165650580.png)

![image-20231227165720940](D:\笔记\笔记图片\image-20231227165720940.png)

* SVM loss function wants the score of the correct class to be larger than the incorrect class scores by at least by Δ (delta)
* SVM 损失函数希望正确类别的得分至少比不正确类别的得分大 Δ (delta)

![image-20231227165807916](D:\笔记\笔记图片\image-20231227165807916.png)

# Lecture13 Artificial Neural Networks

![image-20231227173207887](D:\笔记\笔记图片\image-20231227173207887.png)

## 13.1 What is Deep Learning?

* **<font color=red>Deep Learning is a family of methods that use deep architectures to learn high-level feature representations.</font>**
* **深度学习是一系列使用深度架构来学习高级特征表征的方法。**
* **通过图中可以得到，机器学习往往需要人工特征提取，深度学习不需要。所有深度学习都是机器学习，但不是所有机器学习都是深度学习。**

![image-20231227173329659](D:\笔记\笔记图片\image-20231227173329659.png)

* 简单的神经网络往往只有一个隐藏层，但是深度学习的神经网络往往有多个隐藏层

![image-20231227173722159](D:\笔记\笔记图片\image-20231227173722159.png)

### 13.1.1 Different types of deep architectures

* **Convolutional Networks**
* **卷积网络**
  * for e.g. image classification
  * 图像分类
* **Auto Encoders**
* **自动编码器**
  * for dimensionality reduction
  * 降维
* **Recurrent Networks**
* **递归网络**
  * for learning patterns in sequential data e.g. text, audio, video etc.
  * 用于学习连续数据（如文本、音频、视频等）中的模式



## 13.2 Applications of Deep Learning

* 物品识别
* 场景分割
* 3D面部模型重建

![image-20231227174433536](D:\笔记\笔记图片\image-20231227174433536.png)

* 自动驾驶

![image-20231227174520617](D:\笔记\笔记图片\image-20231227174520617.png)

* 机械化

![image-20231227200316422](D:\笔记\笔记图片\image-20231227200316422.png)

## 13.3 Artificial Neural Networks 人工神经网络

* 从现实中的神经网络到人工神经网络

![image-20231227200432808](D:\笔记\笔记图片\image-20231227200432808.png)

### 13.3.1 How do NNs and ANNs work?

* NNs are able to **learn by adapting their connectivity patterns** so that the organism improves its behavior in terms of reaching certain (evolutionary) goals.
* 神经网络能够通过调整连接模式进行学习，从而改善生物体的行为，达到某些（进化）目标。
* The strength of a connection, or whether it is excitatory or inhibitory, depends on the state of a receiving **neuron’s synapses**.
* 连接的强度，或者说是兴奋性连接还是抑制性连接，取决于接收神经元突触的状态。
* The NN achieves **learning** by a**ppropriately adapting the states of its synapses.**
* 神经网络通过适当调整突触状态来实现学习。



![image-20231227200848014](D:\笔记\笔记图片\image-20231227200848014.png)



### 13.3.2 The Activation Function

* An activation function determines if a neuron should be activated or not activated. 
* 激活函数决定神经元是否应被激活。

![image-20231227200935505](D:\笔记\笔记图片\image-20231227200935505.png)

* Non-linear activation function can **enhance the representation ability** of the network
* 非线性激活函数可**增强网络的表征能力**



![image-20231227201107284](D:\笔记\笔记图片\image-20231227201107284.png)

#### 13.3.2.1 The Activation Function– Sigmoidal Neurons 乙状神经元

* Very common type of artificial neuron, especially in learning networks
* 非常常见的人工神经元类型，尤其是在学习网络中
* 将数据压缩到0-1

![image-20231227201132604](D:\笔记\笔记图片\image-20231227201132604.png)

![image-20231227201544233](D:\笔记\笔记图片\image-20231227201544233.png)

* The parameter ？（这个符号打不出来） controls the slope of the sigmoid, while the parameter  controls the horizontal offset in a way similar to the threshold neurons.
* 参数  控制着曲线的斜率，而参数  则以类似于阈值神经元的方式控制着水平偏移。

![image-20231227201752621](D:\笔记\笔记图片\image-20231227201752621.png)

* **<font color=red>下面是一些关于Sigmoid Function的性质</font>**
* ![image-20231227202138897](D:\笔记\笔记图片\image-20231227202138897.png)

![image-20231227201932222](D:\笔记\笔记图片\image-20231227201932222.png)

![image-20231227203223440](D:\笔记\笔记图片\image-20231227203223440.png)



### 13.3.3 Binary Analogy: Threshold Logic Units (TLUs)二进制类比： 阈值逻辑单元 (TLU)

* TLUs in technical systems are similar to the threshold neuron model, except that TLUs only accept binary inputs (0 or 1).
* 技术系统中的 TLU 与阈值神经元模型类似，但 TLU 只接受二进制输入（0 或 1）。

![image-20231227203735267](D:\笔记\笔记图片\image-20231227203735267.png)

* TLUs can implement various simple logical functions.
* TLU 可以实现各种简单的逻辑功能。

![image-20231227203838627](D:\笔记\笔记图片\image-20231227203838627.png)

* Impossible! TLUs can only realize linearly separable functions.
* 不可能！TLU 只能实现线性可分函数。

![image-20231227203919855](D:\笔记\笔记图片\image-20231227203919855.png)



### 13.3.4 Linear Separability 线性可分

* A function f:{0, 1}n -> {0, 1} is linearly separable if the space of input vectors yielding 1 can be separated from those yielding 0 by a linear surface (hyperplane) in n dimensions.
* 一个函数 f:{0, 1}n -> {0, 1}是线性可分的，如果输入的空间可以分成两部分，一部分是1，另一部分是0，在n维的条件下。

![image-20231227205357660](D:\笔记\笔记图片\image-20231227205357660.png)



![image-20231227210042826](D:\笔记\笔记图片\image-20231227210042826.png)



* Of course, the same applies to our original function f of the TLU using binary input values.
* 当然，这同样适用于使用二进制输入值的 TLU 原始函数 f。
  * The only difference is the restriction in the input values.
  * 唯一不同的是输入值的限制。
* Obviously, we cannot find a straight line to realize the XOR function:
* 显然，我们无法找到一条直线来实现 XOR 函数：



### 13.3.5 Multi-Layered XOR Network 多层XOR网络

![image-20231227210247931](D:\笔记\笔记图片\image-20231227210247931.png)

![image-20231227210649158](D:\笔记\笔记图片\image-20231227210649158.png)



* The first layer, called input layer, just contains the input vector and does not perform any computations.
* 第一层称为输入层，只包含输入向量，不进行任何计算。
* The second layer, called hidden layer, receives input from the input layer, processes the input data and sends its output to the output layer.
* 第二层称为隐藏层，接收来自输入层的输入，处理输入数据，并将输出发送到输出层。

![image-20231227232656975](D:\笔记\笔记图片\image-20231227232656975.png)



# Lecture14 Backpropagation



## 14.1 Feed-Forward Neural Network 前馈神经网络

![image-20231227232913571](D:\笔记\笔记图片\image-20231227232913571.png)

![image-20231227232950438](D:\笔记\笔记图片\image-20231227232950438.png)

* **Typically: supervised learning**
* **典型：监督学习**
* In supervised learning, we train an ANN with a set of vector pairs, so-called examples or training data.
* 在监督学习中，我们用一组向量对（即所谓的示例或训练数据）来训练 ANN。
* By providing enough examples, the network may learn good features that describe the data “in general”
* 通过提供足够多的示例，网络可以学习到 "一般 "描述数据的良好特征

![image-20231227233535433](D:\笔记\笔记图片\image-20231227233535433.png)



* Each training pair (x, y) consists of an input vector x and a corresponding output vector y. 
* 每个训练对 (x, y) 都由输入向量 x 和相应的输出向量 y 组成。
  * Whenever the network receives input x, we would like it to provide output y.
  * 每当网络接收到输入 x，我们都希望它能提供输出 y。
  * The examples thus describe the function that we want the network to learn.
  * 因此，示例描述了我们希望网络学习的功能。
* Besides learning the exemplars, we would like our network to generalize well, that is, given some new inputs that the network had not been trained with, the model can also provide accurate predictions.
* 除了学习示例之外，我们还希望网络能够很好地泛化，也就是说，在网络没有接受过训练的情况下，如果有新的输入，模型也能提供准确的预测。

![image-20231227233815932](D:\笔记\笔记图片\image-20231227233815932.png)



## 14.2 Accuracy VS Generalization

* **There is a trade off between a network’s ability to precisely learn the given examples and its ability to generalize.**
* **网络精确学习给定示例的能力与其泛化能力之间存在权衡。**
* This problem is similar to fitting a function to a given set of data points.
* 这个问题类似于将一个函数拟合到一组给定的数据点。
  * Let’s assume that we want to find a fitting function f:ℝ->ℝ for a set of three data points.
  * 假设我们要为一组三个数据点找到拟合函数 f:ℝ->ℝ。
  * We can try to do this with polynomials of different degrees (different complexity).
  * 我们可以尝试用不同度数的多项式（复杂程度不同）来实现这一目标。

![image-20231227234103570](D:\笔记\笔记图片\image-20231227234103570.png)

![image-20231227234057766](D:\笔记\笔记图片\image-20231227234057766.png)

![image-20231227234137416](D:\笔记\笔记图片\image-20231227234137416.png)

![image-20231227234219315](D:\笔记\笔记图片\image-20231227234219315.png)

* Basic idea: define error function and measure error for untrained data (testing set)
* 基本思路：定义误差函数并测量未训练数据（测试集）的误差

![image-20231227234305384](D:\笔记\笔记图片\image-20231227234305384.png)





## 14.3 Backward Propagation 向后传播

* The backpropagation algorithm was popularized by Rumelhart, Hinton, and Williams in 1986.

  反向传播算法由 Rumelhart、Hinton 和 Williams 于 1986 年推广使用。

* This algorithm solved the “credit assignment” problem, i.e., crediting or blaming individual neurons across layers for particular outputs.

* 该算法解决了 "信用分配 "问题，即各层神经元的特定输出应归功于或归咎于单个神经元。

* **涉及计算神经网络中的每个神经元对最终输出的贡献程度。**

* The error at the output layer is propagated backwards to units at lower layers, so that the weights of all neurons can be adapted appropriately.

* 输出层的误差会向后传播到更低层的单元，这样所有神经元的权重都能得到适当调整。

![image-20231228163341179](D:\笔记\笔记图片\image-20231228163341179.png)

* **The goal of the backpropagation algorithm is to modify the network’s weights so that its output vector**
* **反向传播算法的目标是修改网络的权重，使其输出向量**
  * o_p=(o_p,1,o_p,2,…,o_p,K)
  * is as close as possible to the desired output vector
  * 尽可能接近预期输出向量
  * d_p=(d_p,1,d_p,2,…,d_p,K)
  * for K output neurons and input patterns p=1,…,P.
  * 对于 K 个输出神经元和输入模式 p=1,...,P。
* The set of input-output pairs (examples){(x_p,d_p):p=1,…,P} constitutes the training set.
* 输入输出对（示例）{(x_p,d_p):p=1,...,P} 的集合构成训练集。

![image-20231228163404340](D:\笔记\笔记图片\image-20231228163404340.png)





* 首先，我们需要一个要最小化的累积误差函数
* First, we need a cumulative error function that is to be minimized
* Typical choice: mean square error (MSE)
* 典型选择：均方误差 (MSE)

![image-20231228163800688](D:\笔记\笔记图片\image-20231228163800688.png)
### 14.3.1 Gradient Descent 

* **Gradient descent** is a very common technique to find the absolute minimum of a function.
* **梯度下降**是寻找函数绝对最小值的常用技术。
* It is especially useful for high-dimensional functions.
* 对于高维函数尤其有用。
* **<font color=red>It is used to iteratively minimize the network’s (or neuron’s) error by finding the gradient of the error surface in weight-space and adjusting the weights in the opposite direction.</font>**
* **它通过寻找权重空间中误差曲面的梯度并反向调整权重，迭代使网络（或神经元）的误差最小化。**

![image-20231228164024548](D:\笔记\笔记图片\image-20231228164024548.png)



* Gradient-descent example: finding the absolute minimum of a one-dimensional error function f(x):
* 梯度下降示例：寻找一维误差函数 f(x) 的绝对最小值：
* 简单来说就是计算f(x)函数的最小值
* ![image-20231228170846939](D:\笔记\笔记图片\image-20231228170846939.png)

![image-20231228164349519](D:\笔记\笔记图片\image-20231228164349519.png)



* **Arrows in the contour plot indicate the gradient of the function at different locations. The gradient is always pointing in the direction of the steepest increase of the function. In order to find the function’s minimum, we should always move against the gradient.**
* **等值线图中的箭头表示函数在不同位置的梯度。梯度总是指向函数最陡峭的上升方向。为了找到函数的最小值，我们应该始终逆着梯度移动。**

![image-20231228170906347](D:\笔记\笔记图片\image-20231228170906347.png)

* 求导

![image-20231228171120503](D:\笔记\笔记图片\image-20231228171120503.png)

* **<font color=red>比较关键的在于导数的链式法则</font>**
* ![image-20231228171329024](D:\笔记\笔记图片\image-20231228171329024.png)

![image-20231228171159743](D:\笔记\笔记图片\image-20231228171159743.png)

![image-20231228171840463](D:\笔记\笔记图片\image-20231228171840463.png)



????????????????????????????????????????????????????????????????????????????????????????????????????????????????????

![image-20231228172140993](D:\笔记\笔记图片\image-20231228172140993.png)

# Lecture15 ConvolutionalNeuralNetworks



## 15.1 Recap: Convolution

### 15.1.1 Convolution1

![image-20231228172710232](D:\笔记\笔记图片\image-20231228172710232.png)

### 15.1.2 Stride 步长

* Stride 步长，指每一次filter移动的距离。

![image-20231228172749265](D:\笔记\笔记图片\image-20231228172749265.png)

![image-20231228172954574](D:\笔记\笔记图片\image-20231228172954574.png)

![image-20231228173019530](D:\笔记\笔记图片\image-20231228173019530.png)



![image-20231228173050125](D:\笔记\笔记图片\image-20231228173050125.png)

![image-20231228173058363](D:\笔记\笔记图片\image-20231228173058363.png)

![image-20231228173107349](D:\笔记\笔记图片\image-20231228173107349.png)

![image-20231228174839222](D:\笔记\笔记图片\image-20231228174839222.png)

* **<font color=red size=5>Output size: (N-F)/stride+1</font>**

![image-20231228174902419](D:\笔记\笔记图片\image-20231228174902419.png)



### 15.1.3 Padding

![image-20231228175259573](D:\笔记\笔记图片\image-20231228175259573.png)

* In general, common to se**e CONV layers with stride 1, filters of size FxF, and zero-padding with <font color=red size=5>(F-1)/2</font>.** (will preserve size spatially)
* 一般来说，常见的 CONV 层**步长为 1**，**滤波器大小为 FxF**，**零填充为 (F-1)/2**。(将在空间上保持大小）
* e.g., F=3 => zero pad with 1
           F=5 => zero pad with 2
           F=7 => zero pad with 3

![image-20231228175320608](D:\笔记\笔记图片\image-20231228175320608.png)



### 15.1.4 Convolution2

* Convolve the filter with the image,i.e., “slide over the image spatially, computing dot products”
* 将滤波器与图像卷积、即 "在图像上滑动，计算点积"

![image-20231228175640565](D:\笔记\笔记图片\image-20231228175640565.png)

* Filters always extend the full depth of the input volume
* 滤波器始终扩展整个输入的深度

![image-20231228175903426](D:\笔记\笔记图片\image-20231228175903426.png)

* 滤波器与 5x5x3 小块图像之间的点积结果（即 5*5*3 = 75-d 点积 + 偏差）
* The result of taking a dot product between the filter and a small 5x5x3 patch of the image (i.e., 5*5*3 = 75-d dot product +bias)

![image-20231228180210216](D:\笔记\笔记图片\image-20231228180210216.png)

* 注意：x为32X32X3的相关图像， W为5X5X3的滤波器，这个可以最后得到结果是两个矩阵相乘。



![image-20231228180532748](D:\笔记\笔记图片\image-20231228180532748.png)

![image-20231228180540677](D:\笔记\笔记图片\image-20231228180540677.png)

![image-20231228180549066](D:\笔记\笔记图片\image-20231228180549066.png)

![image-20231228180557883](D:\笔记\笔记图片\image-20231228180557883.png)

* Convolve (slide) over all **<font size=5>spatial空间</font>** locations
* 对所有空间位置进行卷积（幻灯片）处理
* <font color=red>**注意：这里得到的结果只有一层**</font>

![image-20231228180609138](D:\笔记\笔记图片\image-20231228180609138.png)

![image-20231228180759710](D:\笔记\笔记图片\image-20231228180759710.png)

* If we have 6 5x5x3 filters, we get 6 separate activation maps. And we stack these up to get a ”new image” of size 28x28x6.
* 如果我们有 6 个 5x5x3 过滤器，就会得到 6 个独立的激活图。将这些激活图叠加起来，就能得到一个大小为 28x28x6 的 "新图像"。

![image-20231228180808998](D:\笔记\笔记图片\image-20231228180808998.png)

* Previous layer: a volume of size W1 x H1 x D1
* 上一层：大小为 W1 x H1 x D1 的体积
* Four hyperparameters are required:
* 需要四个超参数
  * Number of filters K
  * 滤波器数量 K
  * Filter size F
  * 滤波器大小 F
  * The stride S
  * 跨距 S
  * The amount of zero padding P
  * 零填充量 P
* Next layer: a volume of size W2 x H2 x D2
* 下一层：大小为 W2 x H2 x D2 的体积
  * **W2 = (W1 - F +2P) / S +1**
  * **H2  = (H1 - F +2P) / S +1**
  * **D2 = K**  

![image-20231228181027066](D:\笔记\笔记图片\image-20231228181027066.png)

* ![image-20231228181757080](D:\笔记\笔记图片\image-20231228181757080.png)

## 15.2 Convolutional Neural Networks (ConvNet) 卷积神经网络

* ConvNet is a sequence of convolution layers, interspersed with activation functions
* ConvNet 是一系列卷积层，中间穿插激活函数

![image-20231228182009490](D:\笔记\笔记图片\image-20231228182009490.png)

* 

![image-20231228182042819](D:\笔记\笔记图片\image-20231228182042819.png)



![image-20231228182202387](D:\笔记\笔记图片\image-20231228182202387.png)



# Lecture16 ConvolutionalNeuralNetworks

## 16.1 Convolutional Neural Networks (Cont.)

### 16.1.1 Pooling Layer 池化层

* Pooling layer 池化层
* **Make the representations smaller and more manageable**
* **使表征更小、更易于管理**
* **Operates over each activation map independently**
* **对每个激活图独立运行**



* Function
  * Aggregate information
  * 汇总信息
  * Reduce computation cost
  * 降低计算成本
  * Reduce memory
  * 减少内存

![image-20231228182310108](D:\笔记\笔记图片\image-20231228182310108.png)

#### 16.1.1.1 Pooling Layer - Max Pooling 最大池化

* 在左边的图示中，给出了一个最大池化的例子。有一个数字矩阵，这代表了一个激活图（activation map）。
* 使用一个2x2的滤波器（Filter），**<font color=red>这个滤波器在激活图上以2个单位的步长（Stride = (2, 2)）移动，不重叠地覆盖矩阵的区域。</font>**
* 在每个2x2的区域内，**最大池化选择区域内的最大值**，并将这个值放入新的输出矩阵中。
* 结果是一个缩小的特征图，其中包含了原始激活图中每个2x2区域的最大值

![image-20231228183122102](D:\笔记\笔记图片\image-20231228183122102.png)

#### 16.1.1.2 Pooling Layer - Average Pooling 平均池化

* 与最大池化类似，不同之处在于：
* 在每个2x2的区域内，**平均池化计算区域内的平均值**，并将这个值放入新的输出矩阵中。

![image-20231228183556437](D:\笔记\笔记图片\image-20231228183556437.png)

#### 16.1.1.3 最大池化和平均池化的缺点

* 黑白图a
* **输入特征图**：白色和黑色代表不同的像素值，白色为255，黑色为0。这个特征图显示了一个白色的对角线。
* **最大池化后**：由于最大池化只选择最大值，因此保留了所有的255值，丢失了黑色的0值信息。
* **平均池化后**：计算了区域内所有值的平均值，因此结果中保留了一些黑色区域的信息（如灰度值128），但同时减弱了白色区域的强度。
* 黑白图b
* **输入特征图**：展示了一个白色的边缘和黑色的背景。
* **最大池化后**：最大池化保留了边缘区域的特征（255值），但内部的黑色区域（0值）被忽略了。
* **平均池化后**：由于平均池化计算了所有值的平均，边缘的强度被大大减弱，结果中白色边缘变得更不明显。

![image-20231228222445094](D:\笔记\笔记图片\image-20231228222445094.png)

* 计算池化层的大小和卷积层不同，这里的D1=D2，且不存在填充边框。

![image-20231228222527230](D:\笔记\笔记图片\image-20231228222527230.png)



### 16.1.2 Fully Connected(FC) Layer 全连接层

* Contains neurons that connect to the entire input volume
* 包含连接整个输入音量的神经元

![image-20231228223450041](D:\笔记\笔记图片\image-20231228223450041.png)

![image-20231228222805055](D:\笔记\笔记图片\image-20231228222805055.png)



### 16.1.3 Batch Normalization Layer 批量归一化层

**为什么使用Batch Normalization（Why）：**

- 为了减少所谓的内部协变量偏移（internal covariate shift），这种现象是指网络中间层分布的改变，这会导致训练过程中学习速度下降。
- 通过**标准化层的输入，可以使用更高的学习率而不会那么容易发生过拟合**，这样可以加快网络训练速度并提高性能。

**Batch Normalization层的作用（用途）：**

- **它可以使每层输入的分布更加稳定，从而使网络更容易学习。**

![image-20231228223945824](D:\笔记\笔记图片\image-20231228223945824.png)

* Without batch Normalization
*  The distributions are very strange for each layer 
*  每一层的分布都很奇怪
* The distributions are unknown and vary for each iteration
* 分布未知，每次迭代都不同
* No big learning rate
*  学习率不高
* Accurate initialization
* 精确初始化
* No too many network layers
* 有过多的网络层
* Otherwise, it will not converge.
* 否则将无法收敛

![image-20231228224019355](D:\笔记\笔记图片\image-20231228224019355.png)

* Make the outputs of each layer follow the same distribution.
* 怎么样让每一层的输出都遵循相同的分布。

![image-20231228224614311](D:\笔记\笔记图片\image-20231228224614311.png)

* **With Batch Normalization**
* **批量规范化**
* **Use big learning rate**
* **使用大学习率**
* **Random initialization**
* **随机初始化**
* **Accurate the convergence**
* **精确收敛**

![image-20231228224655202](D:\笔记\笔记图片\image-20231228224655202.png)



![image-20231228224821393](D:\笔记\笔记图片\image-20231228224821393.png)



### 16.1.4 Dropout Layer 滤波器层

* For a network with a relatively large number of parameters, if there are insufficient training samples, overfitting often occurs. **<font color=red>Dropout is a technique to overcome the overfitting problem.</font>**
* 对于参数相对较多的网络，如果训练样本不足，往往会出现过拟合。**Dropout 是一种克服过拟合问题的技术。**
* 在训练过程中，Dropout随机地丢弃（即在前向传播过程中将其输出置为零）网络中的一些神经元（以及它们的连接），这是临时的，在每个训练批次中随机选择。

![image-20231228224941736](D:\笔记\笔记图片\image-20231228224941736.png)

* **<font color=red>Function: Improve the generalization ability of the model and overcome overfitting problem</font>**
* **功能 提高模型的泛化能力，克服过拟合问题**

![image-20231228225252256](D:\笔记\笔记图片\image-20231228225252256.png)



![image-20231228225437038](D:\笔记\笔记图片\image-20231228225437038.png)





### 16.1.5 ReLU layer ReLU 层

* **<font color=red>Function: Improve the non-linear representation ability of the network</font>**
* **功能 提高网络的非线性表示能力**

![image-20231228225543818](D:\笔记\笔记图片\image-20231228225543818.png)





### 16.1.6 Deconvolution layer 解卷积层

* **<font color=red>Deconvolution, also known as transposed convolution. It is used to upsample the feature maps to a bigger size.</font>**
* **解卷积，又称转置卷积。它用于将特征图上采样到更大的尺寸。**
* 反卷积层对输入的特征图进行上采样，使其尺寸变大。这对于那些需要输出更高分辨率的图像或特征图的应用尤为重要，比如图像分割任务，其中网络需要输出与输入图像同等大小的分割掩码。

![image-20231228225723389](D:\笔记\笔记图片\image-20231228225723389.png)

* **<font color=red>A general grasp of the principles is enough; it won't be assessed in the exam.</font>**
* **只需大致掌握原理即可，考试中不会对其进行评估。**

![image-20231228230156955](D:\笔记\笔记图片\image-20231228230156955.png)







# Lecture17 Regularization 正则化

![image-20231228231927818](D:\笔记\笔记图片\image-20231228231927818.png)

## 17.1 Regularization 正则化

* Regularization is an important technique in neural network training to **prevent overfitting and improve the generalization** of the model.  The functions of the regularization can be summarized as:
* 正则化是神经网络训练中的一项重要技术，可以防止过拟合，提高模型的泛化能力。 正则化的功能可概括为
  *  **Prevent overfitting problem** 
  * **防止过拟合问题** 
  * **Improve model generalization ability** 
  * **提高模型泛化能力** 
  * **Stabilize the training process** 
  * **稳定训练过程**
  * **Reduce model complexity**
  * **降低模型复杂度**

![image-20231228231853816](D:\笔记\笔记图片\image-20231228231853816.png)

### 17.1.1 Training-validation-test set 培训-验证-测试集

* Training-validation-test set 培训-验证-测试集

![image-20231228232127796](D:\笔记\笔记图片\image-20231228232127796.png)

#### 17.1.1.2 N-Fold Cross-Validation  N倍交叉验证

* N-Fold Cross-Validation 
* N 倍交叉验证
* **Sometimes your dataset is so small,** that splitting it 80/20 will still **result in a large amount of variance.** One solution to this is to perform N-Fold Cross-Validation. The central idea here is that we’re going to do this entire process N times and average the accuracy. For example, in 10-fold cross-validation.
* **有时，您的数据集非常小**，将其按 80/20 的比例分割仍会产生大量差异。**解决方法之一就是进行 N 倍交叉验证。**这里的中心思想是，我们要将整个过程进行 N 次，然后平均准确率。例如，在 10 倍交叉验证中。

![image-20231228232220807](D:\笔记\笔记图片\image-20231228232220807.png)

-------------------------------------------------------------------------------------------------------------------

**<font size=5>Back to Training-validation-test set</font>**

* Train/validation/test set
* 训练集/验证集/测试集
* Training set: Training models
* 训练集： 训练模型
* Validation set: Test the model trained on training set and select the best performed model
* 验证集： 测试在训练集上训练的模型，并选择性能最佳的模型
* Testing set: Test the model
* 测试集： 测试模型
* Training set vs validation set: 80% vs 20% or 90% vs 10%
* 训练集与验证集： 80% vs 20% 或 90% vs 10%
* Training vs validation vs testing set: 60%-20%-20%
* 训练集 vs 验证集 vs 测试集 60%-20%-20%
* No standard rule, if a large amount data, e.g., 1,000,000. It is possible to have 98%-1%-1%
* 没有标准规则，如果数据量很大，例如 1,000,000. 可能有 98%-1%-1% 的数据
* It is possible that there are only training and validation set  (In some data competitions, the test set is not available to us)
* 有可能只有训练集和验证集（在某些数据竞赛中，我们无法获得测试集）

![image-20231228232722385](D:\笔记\笔记图片\image-20231228232722385.png)



#### 17.1.1.3 Evaluation Metrics in validation/test set 验证/测试集的评价指标

* **TP (True Positive):** The classifier predicts a positive sample, and it is indeed a positive sample. In other words, it represents the number of positive samples that have been **<font color=red>correctly</font>** identified.
* TP（真阳性）： 分类器预测出一个阳性样本，而它确实是一个阳性样本。换句话说，它代表正确识别出的阳性样本的数量。
* **FP (False Positive):** The classifier predicts a positive sample, but it is actually a negative sample. This corresponds to the number of negative samples that were **<font color=red>incorrectly</font>** identified as positive.
* FP（假阳性）： 分类器预测出一个阳性样本，但它实际上是一个阴性样本。这相当于被错误识别为阳性的阴性样本的数量。
* **TN (True Negative):** The classifier predicts a negative sample, and it is indeed a negative sample. This represents the number of negative samples that have been **<font color=red>correctly</font>** identified.
* TN（真阴性）： 分类器预测出一个阴性样本，但它确实是一个阴性样本。这代表被正确识别的阴性样本的数量。
* **FN (False Negative):** The classifier predicts a negative sample, but it is actually a positive sample. This indicates the number of positive samples that were missed or **<font color=red>incorrectly</font>** identified as negative.
* FN（假阴性）： 分类器预测出一个阴性样本，但它实际上是一个阳性样本。这表示被遗漏或错误识别为阴性的阳性样本数。

![image-20231228233246518](D:\笔记\笔记图片\image-20231228233246518.png)

* **<font color=red>重点在于这几个公式，非常重要！！！</font>**

![image-20231228233728137](D:\笔记\笔记图片\image-20231228233728137.png)

* Overfitting vs Underfitting
* 过度拟合与欠拟合

![image-20231228234109239](D:\笔记\笔记图片\image-20231228234109239.png)

* 

![image-20231228234151379](D:\笔记\笔记图片\image-20231228234151379.png)

* How to handle Overfitting and Underfitting

* 如何处理过度拟合和欠拟合

* - **Underfitting:**    

  - **不拟合：**

    - **Use larger network, e.g., more layers, more hidden units**   
    - **使用更大的网络，如更多层、更多隐藏单元** 
    - **Train the network with more epochs or iterations**
    - **用更多的历时或迭代来训练网络**   
    - **Design a new network architecture**
    - **设计新的网络架构**

    

  - **Overfitting:**

  - **过拟合：**  

    - **Use more training data**
    - **使用更多训练数据**  
    - **Add regularization**  
    - **添加正则化** 
    - **Design a new network architecture**
    - **设计新的网络架构**

![image-20231228234243037](D:\笔记\笔记图片\image-20231228234243037.png)

### 17.1.2 L1/L2 Regularization L1/L2 正则化

* **L1正则化（Lasso Regularization）**：在损失函数中增加系数的绝对值之和（L1范数）。这种方法倾向于产生稀疏的系数，即模型的一些系数会变为零，从而**<font color=red>实现特征选择的效果。</font>**
* **L2正则化（Ridge Regularization）**：在损失函数中增加系数的平方和（L2范数）。这种方法倾向于使系数值接近零，但不会完全为零，它可以减少模型参数的大小，**<font color=red>防止参数值过大导致的过拟合</font>**



![image-20231229012923839](D:\笔记\笔记图片\image-20231229012923839.png)

![image-20231229012511858](D:\笔记\笔记图片\image-20231229012511858.png)

### 17.1.3 Dropout 滤波

* 0.5 chance removing or keeping each node
* 删除或保留每个节点的概率为 0.5
* Keep_prob for each layer
* 各层的保留概率

![image-20231229013225835](D:\笔记\笔记图片\image-20231229013225835.png)

![image-20231229013323181](D:\笔记\笔记图片\image-20231229013323181.png)

* No dropout during testing
* 测试过程中不使用dropout

![image-20231229013539755](D:\笔记\笔记图片\image-20231229013539755.png)

#### 17.1.3.1 Why dropout？

* Intuition 1: 理念1
* Every iteration, it works on a smaller network
* 每次迭代都在更小的网络上运行

![image-20231229013618639](D:\笔记\笔记图片\image-20231229013618639.png)

* Intuition 2: 理念2
* Cannot rely on any one single feature, but spread out the weights
* 不能依赖任何单一特征、 而是分散权重

![image-20231229013900794](D:\笔记\笔记图片\image-20231229013900794.png)

* Cannot rely on any one single feature
* 不能依赖任何单一功能
* Never put too much weight to one single unit/feature as it may be go away 
* 切勿过分看重某一 单一单元/功能，因为它可能会消失

![image-20231229013852255](D:\笔记\笔记图片\image-20231229013852255.png)

* Intuition 3: 直觉3
* It can be seen as a model ensemble strategy in the model training
* 可将其视为模型训练中的模型集合策略

![image-20231229014032439](D:\笔记\笔记图片\image-20231229014032439.png)



### 17.1.3 Early Stopping 提前停止

* **早停法的概念**：
  - 早停法是一种防止机器学习模型过拟合的技术。在训练过程中，随着训练次数（epoch）的增加，模型在训练集上的性能通常会提高，即错误率下降。
  - 然而，如果模型在训练集上学习得太好，就可能开始学习到训练数据中的噪声和特定的模式，而这些可能不适用于未见过的数据。
  - 通过在验证集上监控性能，**早停法能够在验证错误率开始增加时停止训练，即使训练错误率还在下降。这个点通常被认为是模型开始过拟合训练数据的地方。******

![image-20231229014216787](D:\笔记\笔记图片\image-20231229014216787.png)

* Iteration: One iteration is forward and backward one batch of examples
* 迭代： 一次迭代是向前和向后迭代一批示例
* Batch size: Batch size is the total number of training examples present in a single iteration
* 批量大小： 批量大小是指单次迭代中出现的训练示例总数
* Epoch: One Epoch is when an ENTIRE dataset is passed forward and backward through the neural network only ONCE
* 历时： 一次迭代是指整个数据集只通过神经网络向前和向后传递一次

![image-20231229014529614](D:\笔记\笔记图片\image-20231229014529614.png)

### 17.1.4 Data Augmentation 数据扩充

* When Should You Use Data Augmentation?  
* 何时应该使用数据扩充？ 
  * To prevent models from overfitting.
  * 防止模型过度拟合。
  * The initial training set is too small.
  * 初始训练集太小。
  * To improve the model accuracy.
  * 提高模型准确性。
  * To reduce the annotation cost.  Save Money
  * 降低标注成本。**省钱**

![image-20231229014820962](D:\笔记\笔记图片\image-20231229014820962.png)

![image-20231229015000865](D:\笔记\笔记图片\image-20231229015000865.png)

![image-20231229015013687](D:\笔记\笔记图片\image-20231229015013687.png)

![image-20231229015028757](D:\笔记\笔记图片\image-20231229015028757.png)



![image-20231229015049024](D:\笔记\笔记图片\image-20231229015049024.png)

![image-20231229015055626](D:\笔记\笔记图片\image-20231229015055626.png)

# Lecture18 NetworkTraining

## 18.1 Networks Training Pipeline 网络训练管道

* ![image-20231229020109299](D:\笔记\笔记图片\image-20231229020109299.png)

![image-20231229015652418](D:\笔记\笔记图片\image-20231229015652418.png)

* Loop
* 循环
  * **Sample** a batch of data
  * 采样一批数据
  * **Forward** prop it through the network, get loss
  * 通过网络向前推进，获取损耗
  * 将这批数据送入神经网络，通过每一层计算对应的输出直至最终获得预测结果，并计算损失（loss）。损失是网络预测值与真实值之间差异的量度
  * **Backprop** to calculate the gradients
  * 反推计算梯度
  * 使用损失函数的结果，通过网络反向传播来计算每个权重对于损失的贡献，即梯度（gradient）。
  * **Update** the parameters using the gradient
  * 利用梯度更新参数


![image-20231229015729293](D:\笔记\笔记图片\image-20231229015729293.png)

### 18.1.1 Sample a batch of data

* Sample a batch of data
* 对一批数据进行采样
* Data preprocessing:
* 数据预处理：
  * Data normalization
  * 数据规范化

![image-20231229153233429](D:\笔记\笔记图片\image-20231229153233429.png)

* **数据标准化**：
  - **原始数据（Original Data）**：图的左侧展示了未经处理的原始数据分布。
  - **零中心化数据（Zero-centered Data）**：通过从每个数据点中减去每个特征的平均值，数据被移动至以原点为中心。这通常有助于优化算法更快地收敛。
  - **标准化数据（Normalized Data）**：进一步的步骤是除以每个特征的标准差，使得数据的分布具有单位方差。这有助于确保所有特征都在相同的尺度上，让训练过程更加稳定。



* Sample a batch of data
* 对一批数据进行采样
  * Data preprocessing:
  * 数据预处理：
  * **Data augmentation :** flip, scale, rotate, mixup/cutout/cutmix
  * **数据增强：**翻转、缩放、旋转、混合/剪切/混剪

![image-20231229153624245](D:\笔记\笔记图片\image-20231229153624245.png)



* Epoch:
  * Each sample in the training dataset has had an opportunity to update the internal model parameters. An epoch is comprised of one or more batches.
  * 训练数据集中的每个样本都有机会更新内部模型参数。一个历元由一个或多个批次组成。
* Mini-batch: a baby training set
* 迷你批次：迷你训练集
  * - Making updates using small part of data
    - 使用小部分数据进行更新
    - - When training data is split into small batches, each batch is a minibatch. 
      - 当训练数据被分成小批时，每批数据就是一个迷你批次。
      - 1<𝑠𝑖𝑧𝑒(𝑚𝑖𝑛𝑖-𝑏𝑎𝑡𝑐ℎ)<𝑠𝑖𝑧𝑒(𝑡𝑟𝑎𝑖𝑛𝑖𝑛𝑔𝑑𝑎𝑡𝑎)
      - Suppose that the training data has 32,000 instances. If the size of a mini-batch (i.e., batch size) is set to 32. Then there will be 1,000 minibatches (iterations) for each epoch.
      - 假设训练数据有 32,000 个实例。如果将迷你批量（即批量大小）的大小设为 32。那么每个 epoch 将有 1,000 个迷你批（迭代）。

![image-20231229153804407](D:\笔记\笔记图片\image-20231229153804407.png)



### 18.1.2 Forward prop it through the network, get loss (error) 在网络中转发，出现丢失（错误）

* **<font color=red>一组训练数据向前传播Forward，然后每一个训练样本都有一个对应的标签，这个标签指示样本的正确类别，然后将预测结果与实际结果进行比较，最后在使用Backward来调整权重</font>**

![image-20231229154337608](D:\笔记\笔记图片\image-20231229154337608.png)

* **Forward prop it through the network, calculate the loss (error)**
* **通过网络转发，计算损失（误差）**
  * **Weight initialization: Small random numbers**    
  * **权重初始化： 小随机数**
    * e.g. Constant initialization, Xavier initialization
    * 例如常数初始化、泽维尔初始化
  * **Set up the  network structure**    
  * **建立网络结构**
    * e.g. AlexNet, VGGNet, ResNet ect.
    * 如 AlexNet、VGGNet、ResNet 等。
  * **Set up loss function**    
  * **设置损失函数**
    * e.g. Cross entropy loss, Sigmoid loss, Focal loss etc.
    * 如交叉熵损失、西格码损失、焦点损失等。

![image-20231229154347589](D:\笔记\笔记图片\image-20231229154347589.png)

* Proper initialization is an active area of research:
* 适当的初始化是一个活跃的研究领域：





### 18.1.3 Loss Functions 损失函数

![image-20231229161531990](D:\笔记\笔记图片\image-20231229161531990.png)

* Softmax函数的输出范围在 00 到 11 之间，所有类别的概率加起来总和为 11，形成了一个概率分布。

* ![image-20231229162116212](D:\笔记\笔记图片\image-20231229162116212.png)

![image-20231229161703131](D:\笔记\笔记图片\image-20231229161703131.png)





![image-20231229163040533](D:\笔记\笔记图片\image-20231229163040533.png)

![image-20231229163010495](D:\笔记\笔记图片\image-20231229163010495.png)

* **Loss function: A loss function tells how good our current classifier is**

* **损失函数 损失函数告诉我们当前分类器的性能如何**

  * Classification: cross entropy loss

    分类：交叉熵损失

![image-20231229163153138](D:\笔记\笔记图片\image-20231229163153138.png)

* 交叉熵损失函数的公式如下图所示
* 其中 *n* 是样本数量，*k* 是类别数量，*t*i*,*j 是真实标签的独热编码，*pi*,*j* 是模型预测的概率。
* **因为独热编码中，只有真实类别对应的位置是1，其他位置都是0，所以损失函数中只有一个项是非零的，其他项因为乘以0都消失了。**

![image-20231229193649539](D:\笔记\笔记图片\image-20231229193649539.png)

* Loss function: A loss function tells how good our current classifier is
* 损失函数： 损失函数告诉我们当前的分类器有多好
* Regression: Mean Squared Error (MSE)
* 回归： 平均平方误差 (MSE)

![image-20231229194929715](D:\笔记\笔记图片\image-20231229194929715.png)

### 18.1.4 Optimizer 优化器

* Optimizer 优化器     
* **<font color=red size=5>Adjust the model’s parameters during training to minimize the loss</font>**
* **在训练过程中调整模型参数，尽量减少损失**



* **<font color=red>Gradient Descent</font>**
* 梯度下降
* **<font color=red>Stochastic Gradient Descent （SGD）</font>**
* 随机梯度下降（SGD）
* **<font color=red>Min-batch Gradient Descent</font>**
* 最小批次梯度下降
* Momentum
* 动量
* Nesterov accelerated gradient（NAG）
* 奈斯特罗夫加速梯度（NAG）

![image-20231229195056583](D:\笔记\笔记图片\image-20231229195056583.png)

* ![image-20231229195903850](D:\笔记\笔记图片\image-20231229195903850.png)
* Iteration: One iteration is process of forward and backward one mini-batch of the data in the model training.
* 迭代： 一次迭代是在模型训练中向前和向后移动一个小批量数据的过程。
* Batch (Mini-batch) size: Batch size is the total number of training examples present in a single iteration.
* 批次（迷你批次）大小： 批量大小是指单次迭代中训练实例的总数。
* Epoch: One Epoch is when an ENTIRE dataset is passed forward and backward through the neural network only ONCE
* 周期： 一个周期是指整个数据集只通过神经网络向前和向后传递一次
* Learning Rate: Determines the updating steps that model takes.
* 学习率： 决定模型的更新步骤。

![image-20231229195504185](D:\笔记\笔记图片\image-20231229195504185.png)

![image-20231229200127854](D:\笔记\笔记图片\image-20231229200127854.png)

#### 18.1.4.1 Update parameters

* Update our trainable parameters, e.g., W and b after backpropagation.
* 在反向传播后更新可训练参数，如 W 和 b。

![image-20231229200430153](D:\笔记\笔记图片\image-20231229200430153.png)

* **<font color=red size=5>分别代表损失函数*L*关于权重和偏置项的偏导数，也就是梯度。</font>**

![image-20231229200233277](D:\笔记\笔记图片\image-20231229200233277.png)

#### 18.1.4.2 Learning Rate 学习率

* **<font color=red size=5>Learning rate (α, λ or    ) is one such hyper-parameter that defines the adjustment in the weights of our network with respect to the loss gradient descent. It determines how fast or slow we will move towards the optimal weights.</font>**
* **学习率（α、λ 或 ）就是这样一个超参数，它定义了网络权重在损失梯度下降过程中的调整。它决定了我们向最优权重移动的快慢。**

![image-20231229200755689](D:\笔记\笔记图片\image-20231229200755689.png)

* **<font color=red>With a small learning rate, updates to the weights are small, which will guide the optimizer gradually towards the minima. However, the optimizer may take too long to converge or get stuck in an undesirable local minima;</font>**
* **学习率越小，权重的更新就越小，这将引导优化器逐渐趋向最小值。然而，优化器可能需要太长时间才能收敛，或陷入不理想的局部极小值；**
* **<font color=red>With a large learning rate, the algorithm learns fast, but it may also cause the algorithm to oscillate around or even jump over the minima. Even worse, a high learning rate equals large weight updates, which might cause the weights to overflow, not converge;</font>**
* **学习率大，算法学习速度快，但也可能导致算法在最小值附近振荡，甚至跳过最小值。更糟糕的是，高学习率等于大权重更新，这可能导致权重溢出，而不是收敛；**
* **<font color=red>A good learning rate is a tradeoff between the coverage rate and overshooting. It’s not too small so that our algorithm can converge swiftly, and it’s not too large so that our algorithm won’t jump back and forth without reaching an undesirable local minima.</font>** 
* **好的学习率是在覆盖率和溢出之间的权衡。学习率不能太小，这样我们的算法才能迅速收敛；学习率也不能太大，这样我们的算法才不会来回跳跃，而不会达到不理想的局部极小值。**

![image-20231229200828102](D:\笔记\笔记图片\image-20231229200828102.png)

#### 18.1.4.3 Learning rate decay strategy 学习率下降策略

* **Multi-step LR decay** allows for specifying the interval of decay epochs. In this case [50, 60, 70, 100]
* 多步 LR 衰减允许指定衰减时间间隔。在本例中为 [50、60、70、100]。
* **Exponential decay** refers to a StepLR where the learning rate decreases every epoch. 
* **指数衰减指的是 StepLR**，其学习率每隔一个纪元就会降低一次。
* Other LR decay strategies, such as StepLR, CosineAnnelingLR, Warmup based strategies.
* 其他 LR 衰减策略，如 StepLR、CosineAnnelingLR 和基于热身的策略。

![image-20231229201217640](D:\笔记\笔记图片\image-20231229201217640.png)



# Lecture19 Deep Learning Frameworks

## 19.1 Overview of different Deep Learning frameworks 不同深度学习框架概述

![image-20231229205721585](D:\笔记\笔记图片\image-20231229205721585.png)

![image-20231229205733545](D:\笔记\笔记图片\image-20231229205733545.png)

![image-20231229205742110](D:\笔记\笔记图片\image-20231229205742110.png)

### 19.1.1 Performance Comparison 性能比较

* Performance Comparison 性能比较

* The table shows the training speed for the two models using 32-bit floats. Throughput is measured in **images per second** for different network architectures, such as AlexNet, VGG-19, etc.
* 下表显示了两种模型使用 32 位浮点数的训练速度。吞吐量以不同网络架构（如 AlexNet、VGG-19 等）的每秒图像数为单位。

![image-20231229205754992](D:\笔记\笔记图片\image-20231229205754992.png)



### 19.1.2 Training Accuracy & Time 训练准确度和训练时间

* Training Accuracy & Time 训练准确度和训练时间

![image-20231229210100997](D:\笔记\笔记图片\image-20231229210100997.png)



### 19.1.3 Ease of Use 易于使用

* Another major difference lies in how developers go about debugging. Effective debugging with TensorFlow requires a special debugger tool that enables you to examine how the network nodes are doing their calculations at each step. PyTorch can be debugged using one of the many widely available Python debugging tools (for example, Python’s pdb and ipdb tools).
* 另一个主要区别在于开发人员如何进行调试。使用 TensorFlow 进行有效调试需要一个特殊的调试工具，它能让你检查网络节点在每一步是如何进行计算的。PyTorch 可以使用许多广泛使用的 Python 调试工具（例如 Python 的 pdb 和 ipdb 工具）进行调试。

![image-20231229210252378](D:\笔记\笔记图片\image-20231229210252378.png)

### 19.1.4 Open-source Codebase 开发代码库

![image-20231229210401803](D:\笔记\笔记图片\image-20231229210401803.png)



![image-20231229210411761](D:\笔记\笔记图片\image-20231229210411761.png)

![image-20231229210418293](D:\笔记\笔记图片\image-20231229210418293.png)

## 19.2 PyTorch

![image-20231229210448786](D:\笔记\笔记图片\image-20231229210448786.png)

![image-20231229210456375](D:\笔记\笔记图片\image-20231229210456375.png)

### 19.2.1 Matrix Operations 矩阵操作

![image-20231229210504680](D:\笔记\笔记图片\image-20231229210504680.png)

![image-20231229210511646](D:\笔记\笔记图片\image-20231229210511646.png)



### 19.2.2 0与1

![image-20231229210523327](D:\笔记\笔记图片\image-20231229210523327.png)

### 19.2.3 PyTorch to Numpy and Vice versa

![image-20231229210642184](D:\笔记\笔记图片\image-20231229210642184.png)

*  Fit a t**hird order polynomial** to sine function with Pytorch and Numpy, respectively.
*  分别用 Pytorch 和 Numpy 拟合三阶多项式和正弦函数。

![image-20231229210728167](D:\笔记\笔记图片\image-20231229210728167.png)

* 分别用 Pytorch 和 Numpy 拟合三阶多项式和正弦函数。

![image-20231229210813094](D:\笔记\笔记图片\image-20231229210813094.png)

![image-20231229210858790](D:\笔记\笔记图片\image-20231229210858790.png)

![image-20231229210912376](D:\笔记\笔记图片\image-20231229210912376.png)

![image-20231229210926277](D:\笔记\笔记图片\image-20231229210926277.png)

![image-20231229210932716](D:\笔记\笔记图片\image-20231229210932716.png)

![image-20231229210940788](D:\笔记\笔记图片\image-20231229210940788.png)



# Lecture20 Deep Models

## 20.1 Typical Deep Models 典型深度模型

![image-20231229212837067](D:\笔记\笔记图片\image-20231229212837067.png)

### 20.1.1 LeNet5

![image-20231229212846838](D:\笔记\笔记图片\image-20231229212846838.png)

* **<font color=red>下面这个图还是比较重要的，讲解了LeNet5的基本模型结构</font>**

* ![image-20231229213349019](D:\笔记\笔记图片\image-20231229213349019.png)

![image-20231229213254196](D:\笔记\笔记图片\image-20231229213254196.png)

* 转换滤波器为 5x5，应用于第 1 步，无填充。子采样（池化）层为 2x2，应用于步长 2 
  即架构为[CONV-POOL-CONV-POOL-CONV-FC-FC]。
* Conv filters were 5x5, applied at stride 1 and without padding.  Subsampling (Pooling) layers were 2x2 applied at stride 2 
  i.e., architecture is [CONV-POOL-CONV-POOL-CONV-FC-FC]

* Usually, when calculating the number of layers, we only consider the layers with parameters, excluding pooling, ReLU, and BN (Batch Normalization) layers.
* 通常，在计算层数时，我们只考虑有参数的层，不包括池化、ReLU 和 BN（批量归一化）层。

![image-20231229213924322](D:\笔记\笔记图片\image-20231229213924322.png)



![image-20231229213941996](D:\笔记\笔记图片\image-20231229213941996.png)

#### 20.1.1.1 LeNet的参数的计算

C1

* 注意：一个卷积核是一个通常较小的矩阵，用于图像这样的大型数据矩阵上的滑动窗口操作。
* 注意：在原始的LeNet-5架构中，第一个卷积层（C1层）使用的是6个5x5的卷积核。

![image-20231229223901805](D:\笔记\笔记图片\image-20231229223901805.png)

S2：![image-20231229223933448](D:\笔记\笔记图片\image-20231229223933448.png)

![image-20231229214335245](D:\笔记\笔记图片\image-20231229214335245.png)

![image-20231229224618642](D:\笔记\笔记图片\image-20231229224618642.png)

![image-20231229224024011](D:\笔记\笔记图片\image-20231229224024011.png)

* ImageNet 挑战

![image-20231229224646038](D:\笔记\笔记图片\image-20231229224646038.png)

* **<font color=red>[CONV1-MaxPOOL1-CONV2-MaxPOOL2-CONV3-CONV4-CONV5-MaxPOOL3-FC6-FC7-FC8]</font>** 
* Input: 227x227x3 images
* 输入：227x227x3 幅图像
* First layer (CONV1) 96 11x11 filters applied at stride 4 without padding.
* 第一层 (CONV1) 96 个 11x11 过滤器，应用于步长 4，无填充。
* What is the output volume size? Recall: (N-F)/S+1
* 输出卷的大小是多少？回顾：(N-F)/S+1

![image-20231229224908869](D:\笔记\笔记图片\image-20231229224908869.png)



* Input: 227x227x3 images (224x224x3 in original paper, one typo)
* 输入：227x227x3 幅图像（原论文为 224x224x3，有一处错字）
* First layer (CONV1) 96 11x11 filter applied at stride 4Output volume [55x55x96]
* 第一层 (CONV1) 96 11x11 过滤器应用于第 4 步 输出量 [55x55x96］
* What is the total number of parameters in this layer?  (Suppose we have bias)
* 这一层的参数总数是多少？ (假设有偏差）

![image-20231229225154492](D:\笔记\笔记图片\image-20231229225154492.png)

![image-20231229225219054](D:\笔记\笔记图片\image-20231229225219054.png)

![image-20231229225241981](D:\笔记\笔记图片\image-20231229225241981.png)

![image-20231229225249431](D:\笔记\笔记图片\image-20231229225249431.png)



![image-20231229225258385](D:\笔记\笔记图片\image-20231229225258385.png)

![image-20231229225312674](D:\笔记\笔记图片\image-20231229225312674.png)



![image-20231229225910065](D:\笔记\笔记图片\image-20231229225910065.png)

* first use of ReLU- used Norm layers (not common anymore) 
* - 首次使用 ReLU--使用 Norm 层（不再常用）
- heavy data augmentation
- - 大量数据扩充
- dropout 0.5- batch size 128
- - 丢弃率 0.5- 批量大小 128
- SGD Momentum 0.9
- - SGD 动量 0.9
- Learning rate 1e-2, reduced by 10 manually when val accuracy plateaus
- - 学习率 1e-2，当估值精确度达到峰值时手动降低 10
- L2 weight decay 5e-4
- - L2 权重衰减 5e-4

![image-20231229225919069](D:\笔记\笔记图片\image-20231229225919069.png)

* ImageNet Large Scale Visual Recognition Challenge (ILSRC) winners
* ImageNet 大型视觉识别挑战赛 (ILSRC) 获奖者

![image-20231229230038066](D:\笔记\笔记图片\image-20231229230038066.png)



# Lecture21 Deep Models

## 21.1 Typical Deep Models 典型深度模型

![image-20231230113455395](D:\笔记\笔记图片\image-20231230113455395.png)

### 21.1.1 VGG-16

* In total, there are 16 convolutional/fc layers
* 总共有 16 个卷积/fc 层
* 2-3 convolutional layers between the pooling layers
* 池化层之间有 2-3 个卷积层

![image-20231229230920606](D:\笔记\笔记图片\image-20231229230920606.png)

* Small filters, Deeper networks 
* 小过滤器，更深的网络 
* 8 layers (AlexNet)-> 16 - 19 layers (VGG16Net or VGG19Net) 
* 8 层 (AlexNet)-> 16 - 19 层 (VGG16Net 或 VGG19Net) 
* Only 3x3 CONV stride 1, pad 1 and 2x2 MAX POOL stride 2 11.7% top 5 error in ILSVRC’13 (ZFNet)-> 7.3% top 5 error in ILSVRC’14 
* 只有 3x3 CONV 步长 1、垫 1 和 2x2 MAX POOL 步长 2 ILSVRC'13 前 5 名错误率为 11.7%（ZFNet）-> ILSVRC'14 前 5 名错误率为 7.3 

![image-20231229230932373](D:\笔记\笔记图片\image-20231229230932373.png)

* **In most cases, when we reduce the size of feature map, we will increase the depth of the feature map.**
* **在大多数情况下，当我们缩小特征图的尺寸时，就会增加特征图的深度。**

![image-20231230113940816](D:\笔记\笔记图片\image-20231230113940816.png)

![image-20231230114100149](D:\笔记\笔记图片\image-20231230114100149.png)

* Why use small filters? (3x3 conv)
* 为什么使用小型滤波器？(3x3 滤波器）
* Stack of two 3x3 conv (stride 1) layers has the same effective receptive field as one 5x5 conv layer, suppose we only have one filter without bias.
* 假设我们只有一个无偏滤波器，那么两个 3x3 滤波器（步长 1）层的叠加有效感受野与一个 5x5 滤波器层的有效感受野相同。
* And fewer parameters: 2* (32) vs. 52
* 而且参数更少：2* (32) 对 52

![image-20231230114116692](D:\笔记\笔记图片\image-20231230114116692.png)

* Effective Receptive Field
* The Effective Receptive Field (ERF) in a neural network refers to the region in the input data that influences the activation of a particular neuron in the network's feature maps or output. It represents the area over which the network's weights are applied to capture information.

![image-20231230114326590](D:\笔记\笔记图片\image-20231230114326590.png)
