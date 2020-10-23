<h1 align="center"> 欢迎来到我的github主页 👋 </h1>


* 我叫聂洪 :blush:	 . 目前，我是[ 贵州电子信息职业技术学院 ](http://www.gzeic.com/)计算机科学系的三年级学生，专业是软件技术。 :satellite:

* 从高中开始就对编程产生了极大的兴趣，希望自己也能逐渐成为一名优秀的软件开发人员  :sparkles:.

* 熟悉JavaWeb、 微信小程序、Vue、nodeJs、Element-UI等 , 目标是通过自己的努力成为一名优秀的全栈开发工程师。 :file_cabinet: .

* 我目前正在复习我的技能 :bulb:.

* 联系方式：<a href="https://6465-develop-ic57t-1302419554.tcb.qcloud.la/github/IMG_8683(20201022-150331).JPG?sign=0afc512e30e32862c460f35deb0df810&t=1603350249"><img src="https://6465-develop-ic57t-1302419554.tcb.qcloud.la/github/ding.png?sign=81d6c6a1fc93c16351bf72c56d586908&t=1603350302"></a>   <a href="https://6465-develop-ic57t-1302419554.tcb.qcloud.la/github/wechatimg.JPG?sign=95f9c4e4b3296f8b4f6ce1b34ab1d10e&t=1603350658"><img src="https://6465-develop-ic57t-1302419554.tcb.qcloud.la/github/wechat.png?sign=2da83536c12ff2476fb2f67661017afa&t=1603350558"></a>


# Android开发笔记

<a name="30hVA"></a>
## 
<a name="MOCKB"></a>
## Adnroid Studio常用快捷键


| 显示类结构窗口 | ALT + 7 |
| --- | :---: |

![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586665167977-ced561ce-2df2-4370-a198-9db56194fdac.png#align=left&display=inline&height=730&margin=%5Bobject%20Object%5D&name=image.png&originHeight=730&originWidth=1493&size=541647&status=done&style=none&width=1493)<br />


| 上下移动选中的行 | Ctrl + Shift + Up / Down |
| --- | :---: |

| 将所选内容设置为：大写/小写 | Ctrl + Shift + U |
| --- | :---: |

| 删除光标所在行（选中行） | Ctrl + Y |
| --- | :---: |
| 复制光标所在的行（选中行） | Ctrl + D |

| 导入重载方法 | Ctrl + O  |
| --- | :---: |

| 实现接口所有方法 | Ctrl + I |
| --- | :---: |


<br />

<a name="4UfDt"></a>
## AndroidManifest

      - **本质：**AndroidManifest.xml是整个应用的主配置清单文件。
      - **包含：**该应用的包名、版本号、组件、权限等信息。
      - **作用：**记录该应用的相关的配置信息。
      - <br />



<a name="kvGK0"></a>
### 2. 组件篇（四大组件）
其属性可以设置：

   - 图标：android:icon
   - 标题：android:label
   - 主题样式：android:theme


<br />注意：

   - 一个清单文件只能包含一个application节点。
   - 启动一个在清单中没有定义的Activity会抛出一个运行时异常。
   - <br />



<a name="Gs34D"></a>
### 3. 权限篇（申请权限和定义权限）

   - （1）使用系统权限

<uses-permission><br />申请权限声明了哪些是由你定义的权限，而这些权限是应用程序正常执行所必需的。在安装程序的时候，你设定的所有权限将会告诉给用户，由他们来决定同意与否。对很多本地Android服务来说，权限都是必需的，特别是那些需要付费或者有安全问题的服务（例如，拨号、接收SMS或者使用基于位置的服务）。<br />注意：android6.0以后，对于一些危险的权限的使用，我们不仅要在AndroidManifest配置文件中配置，还需要动态申请后才能使用。<br />
<br />

<a name="kPOkk"></a>
## Activity(重要组件)
<a name="VT0t5"></a>
### 1. 什么是Activity?

      - Activity是一个应用程序组件。
      - 为应用程序提供一个可视化页面。
      - 用户通过Activity提供的页面与应用程序进行交互。



<a name="wGHDM"></a>
### 2. Activity启动流程

      - Manifest.xml（应用程序的主配置文件，应用程序所使用到的各种组件都需要在其中声明、注册以及应用程序要使用的系统权限都需在此文件中声明）。
      - MainActivity（主界面）。
      - layout（布局文件）。

启动流程图：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586375519307-42813af2-c4e2-4b74-8e74-6ba8623ce74d.png#align=left&display=inline&height=147&margin=%5Bobject%20Object%5D&name=image.png&originHeight=276&originWidth=1397&size=108777&status=done&style=none&width=746)
<a name="ygw4q"></a>
### 3. Activity与Layout(布局)之间的关系

      - 在Layout布局文件中定义的布局和控件都会在Activity中显示，也就是说Activity显示的内容取决于我们在Layout文件中定义的内容，通过更改Layout文件中的控件属性就可以更改Activity中显示的内容，但一般来说我们都是通过findViewbyId(要获取的xml对象ID)来在代码中动态修改属性值。



<a name="sya4U"></a>
### 4. Activity生命周期函数


   - 启动与销毁Activity
   - 暂停与恢复Activity
   - 停止与重启Activity
   - 重新创建Activity


<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1587101055713-b7b0ae4f-c727-43d0-8ba3-34a4de154c02.png#align=left&display=inline&height=321&margin=%5Bobject%20Object%5D&name=image.png&originHeight=326&originWidth=758&size=55839&status=done&style=none&width=746)

- **Resumed**：在这种状态下，Activity处于前台，且用户可以与其交互。（有时也称为“运行”状态。）
- **Paused**：在这种状态下，Activity被在前台中处于半透明状态或者未覆盖整个屏幕的另一个Activity—部分阻挡。暂停的Activity不会接收用户输入并且无法执行任何代码。
- **Stopped**：在这种状态下，Activity被完全隐藏并且对用户不可见；它被视为处于后台。停止时，Activity实例及其诸如成员变量等所有状态信息将保留，但它无法执行任何代码。
- 其他状态（“创建”和“开始”）是瞬态，

其它状态 (**Created**与**Started**)都是短暂的瞬态，系统会通过调用下一个生命周期回调方法从这些状态快速移到下一个状态。 也就是说，在系统调用 [onCreate()](http://developer.android.com/reference/android/app/Activity.html#onCreate(android.os.Bundle)) 之后，它会快速调用 [onStart()](http://developer.android.com/reference/android/app/Activity.html#onStart())，紧接着快速调用 [onResume()](http://developer.android.com/reference/android/app/Activity.html#onResume())。<br />

<a name="RrwHa"></a>
#### 1.启动与销毁Activity
启动Activity

- 指定程序首次启动的Activity
```xml
 <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
```

- 创建一个新的Activity

大多数app包括多个activity，使用户可以执行不同的动作。不论这个activity是当用户点击应用图标创建的main activtiy还是为了响应用户行为而创建的其他activity，系统都会调用新activity实例中的onCreate()方法。我们必须实现onCreate()方法来执行程序启动所需要的基本逻辑。例如可以在onCreate()方法中定义UI以及实例化类成员变量。_(onCreate里面尽量少做事情，避免程序启动太久都看不到界面)。_<br />一旦onCreate 操作完成，系统会迅速调用onStart() 与onResume()方法。我们的activity不会在Created或者Started状态停留。<br />
<br />销毁Activity<br />activity的第一个生命周期回调函数是 onCreate(),它最后一个回调是[onDestroy()](http://developer.android.com/reference/android/app/Activity.html#onDestroy()).当收到需要将该activity彻底移除的信号时，系统会调用这个方法。<br />除非程序在onCreate()方法里面就调用了finish()方法，系统通常是在执行了onPause()与onStop() 之后再调用onDestroy() 。在某些情况下，例如我们的activity只是做了一个临时的逻辑跳转的功能，它只是用来决定跳转到哪一个activity，这样的话，需要在onCreate里面调用finish方法，这样系统会直接调用onDestory，跳过生命周期中的其他方法。<br />

```kotlin
    override fun onDestroy() {
        super.onDestroy()
        Log.i(TAG,"onDestroy")
    }
```
<a name="tCxf0"></a>
### 
<a name="O1BCV"></a>
### 2.暂停与恢复Activity
暂停Activity<br />当系统调用activity中的onPause()，从技术上讲，意味着activity仍然处于部分可见的状态.但更多时候意味着用户正在离开这个activity，并马上会进入Stopped state. 通常应该在onPause()回调方法里面做以下事情:

- 停止动画或者是其他正在运行的操作，那些都会导致CPU的浪费.
- 提交在用户离开时期待保存的内容(例如邮件草稿).
- 释放系统资源，例如broadcast receivers, sensors (比如GPS), 或者是其他任何会影响到电量的资源。
```kotlin
    override fun onPause() {
        super.onPause()
        Log.i(TAG,"onPause")
    }
```
恢复activity<br />当用户从Paused状态恢复activity时，系统会调用onResume()方法。<br />请注意，系统每次调用这个方法时，activity都处于前台，包括第一次创建的时候。所以，应该实现onResume()来初始化那些在onPause方法里面释放掉的组件，
```kotlin
    override fun onResume() {
        super.onResume()
        Log.i(TAG,"onResume")
    }
```
<a name="gWdc8"></a>
### 
<a name="aBVuH"></a>
### 3.停止与重启Activity
停止与重启在activity中是很重要的，在activity生命周期中，他们能确保用户感知到程序的存在并不会丢失他们的进度。在下面一些关键的场景中会涉及到停止与重启：

- 用户打开最近使用app的菜单并从我们的app切换到另外一个app，这个时候我们的app是被停止的。如果用户通过手机主界面的启动程序图标或者最近使用程序的窗口回到我们的app，那么我们的activity会重启。
- 用户在我们的app里面执行启动一个新activity的操作，当前activity会在第二个activity被创建后stop。如果用户点击back按钮，第一个activtiy会被重启。
- 用户在使用我们的app时接收到一个来电通话。



停止Activity

当activity调用onStop()方法, activity不再可见，并且应该释放那些不再需要的所有资源<br />

```kotlin
    override fun onStop() {
        super.onStop()
        Log.i(TAG,"onStop")
    }
```

<br />我们在onStop里面做了哪些清除的操作，就该在onStart里面重新把那些清除掉的资源重新创建出来。<br />当activity从Stop状态回到前台时，它会调用onRestart().系统再调用onStart()方法，onStart()方法会在每次activity可见时被调用。
```kotlin
    override fun onRestart() {
        super.onRestart()
        Log.i(TAG,"onRestart")
    }
```
使用onRestart()来恢复activity状态是不太常见的,我们一般都使用onStart()作为onStop()所对应方法。
```kotlin
    override fun onRestart() {
        super.onRestart()
        Log.i(TAG,"onRestart")
    }
```

---

<a name="StziN"></a>
## View
<a name="ILgWR"></a>
### 1. 什么是View?

      - 在屏幕内所显示的内容，都可以称为View或View的子类。
<a name="6PLjs"></a>
### 2. 代码获取View对象

      - 通过findViewById(要获取的xml对象ID)来获取到要操作的对象。
<a name="vqcva"></a>
### 3. 通过代码动态修改控件属性

      - 通过刚刚获取的对象.set方法即可设置View属性。


<br />获取控件并动态修改控件属性代码示例：<br />layout布局文件
```xml
<TextView
    android:layout_centerInParent="true"
    android:id="@+id/textview"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello World!"
   />
```

<br />Activity代码文件
```kotlin
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.TextView

class MainActivity : AppCompatActivity() {
   override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //拿到该控件对象
        var tv = findViewById<TextView>(R.id.textview)
        //通过对象.方法来修改想要改变的控件属性值
        tv.text = "动态修改文本内容成功"
	}
}
```


<a name="QRy4w"></a>
### 4. 监听器入门

<br />代码示例：<br />layout布局文件
```xml
<Button
    android:layout_centerInParent="true"
    android:id="@+id/btn"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="button"
   />
```

<br />Activity代码文件
```kotlin
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.TextView
import android.widget.Toast

class MainActivity : AppCompatActivity() {
	override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //拿到该控件对象
        var button = findViewById<TextView>(R.id.btn)
        //设置并开始监听
        button.setOnClickListener { Toast.makeText(applicationContext,"点我干嘛",Toast.LENGTH_LONG).show()}
	}
}
```

---

<a name="RcCvS"></a>
## Layout布局
<a name="q5MNG"></a>
### 1. 什么是Layout

      - 如果把UI控件比喻成餐盘，那么Activity就是餐桌，那么该如何餐盘才能让餐桌美观大方，让食客流连忘返就是Layout需要完成的，简单来说，所有的UI控件的摆放位置就是由Layout布局文件控制的，例如控制Activity中控件的大小、位置、颜色等等。
<a name="Q8rT0"></a>
### 2. Layout与ViewGroup之间的关系

      - 结构图：

![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586406351258-48ec0315-9536-4a46-b75d-9e58885cd830.png#align=left&display=inline&height=258&margin=%5Bobject%20Object%5D&name=image.png&originHeight=528&originWidth=887&size=118632&status=done&style=none&width=434)

   - **ViewGroup:**
      - ViewGroup是一个容器，而这个容器是继承于View的。
      - ViewGroup是一个基类，并且是Layout和一些组件的基类。
<a name="S8iAJ"></a>
### 3. Layout实现方式

      - 通过XML布局文件实现控件布局。（降低了代码与布局的耦合度）
      - 通过代码实现控件布局。（更灵活）
<a name="9oDw6"></a>
### 4. Layout的种类

      - 常用布局：Linear Layout（线性布局）、Relative Layout（相对布局）。对于真正的开发来说，常用相对布局来进行页面的布局，对我们屏幕的适配有一定的帮助。
      - AdapterView(带适配器的View): 相比于常用布局来说，它已经将布局定义好了，我们只需要往里面填写内容就可以了，如：ListView，GirdView。
<a name="08tJ4"></a>
### 5. 编写XML布局文件

      - 每一个Layout布局文件有且仅有一个根标签（元素），必须为View或ViewGroup对象。
      - 在根标签下，添加子元素，并逐渐建立一个View层次来定义你的Layout。
<a name="F7iPV"></a>
### 6. 常用单位：

      - 控件大小单位：dp（与设备无关）。
      - 字体大小单位：sp（根据系统字体大小自动改变自身大小）。
<a name="B2tqv"></a>
### 7. Linear Layout(属性介绍)

   - 设置控件排列方向属性：
      - orientation:（vertical垂直/horizontal水平）
   - 设置各子控件占屏幕多少的比重：
      - android:layout_weight
      - android:weightSum="50"//在LinearLayout标签里可以设置比重值的总和
      - 注意：要设置某个控件宽或者高的比重时，记得将对应的宽高设置为0dp

例如：我们想实现在水平方向上让三个TextView平分屏幕宽度
```xml
   <?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:orientation="horizontal"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:weightSum="30">

    <TextView
        android:gravity="center"
        android:text="我是TextView1"
        android:textColor="@color/white"
        android:layout_weight="10"
        android:layout_width="0dp"
        android:layout_height="50dp"
        android:background="@color/colorPrimaryDark"/>
    <TextView
        android:gravity="center"
        android:text="我是TextView1"
        android:textColor="@color/white"
        android:layout_weight="10"
        android:layout_width="0dp"
        android:layout_height="50dp"
        android:background="@color/colorAccent"/>
    <TextView
        android:gravity="center"
        android:text="我是TextView1"
        android:textColor="@color/white"
        android:layout_weight="10"
        android:layout_width="0dp"
        android:layout_height="50dp"
        android:background="@color/colorPrimary"/>
</LinearLayout>
```

   - 设置控件的及控件内容的对齐方式：
      - android:gravity：
      - 用于设置该控件中内容相对于该控件的对齐方式
      - android:layout gravity：
      - 用于设置该控件相对于父控件的对齐方式

gravity属性值：

| **top ** | **将对象放在其容器的顶部，不改变其大小** |
| :---: | --- |
| **bottom ** | **将对象放在其容器的顶部，不改变其大小** |
| **left ** | **将对象放在其容器的左侧，不改变其大小** |
| **right ** | **将对象放在其容器的右侧，不改变其大小** |
| **center-vertical** | ** |
| **        center_horizontal** | **水平对齐方式：水平方向上居中对齐** |
| **center** | ** |


---

<a name="0eXYX"></a>
### 8. 属性解析
直接在background属性后添加颜色（android:background="#AA00FF"）
```xml
    <Button
        android:layout_centerInParent="true"
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="button"
        android:background="#AA00FF"
       />
```
<a name="zCf59"></a>
#### 1. 颜色引用
**使用@color设置颜色，如 background（@color）**

   - **在android项目下的res目录的values目录下找到名为colors的xml文件，**
   - **在其中用<color name = 别名>具体颜色</color>**

**第一步：找到名为colors的xml文件。**<br />**![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586433998942-35dddd09-95c6-4bd6-ae43-ef1dd52c7285.png#align=left&display=inline&height=370&margin=%5Bobject%20Object%5D&name=image.png&originHeight=370&originWidth=343&size=12725&status=done&style=none&width=343)**<br />**第二步：在colors中通过<color>标签来定义我们需要的颜色，并取一个别名。**
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="colorPrimary">#6200EE</color>
    <color name="colorPrimaryDark">#3700B3</color>
    <color name="colorAccent">#03DAC5</color>
    <color name="blue">#0000FF</color>
</resources>
```
第三步：引用该颜色，如（ android:background="@color/blue"）。
```xml
    <Button
        android:layout_centerInParent="true"
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="button"
        android:background="@color/blue"
       />
```


<a name="VUbGT"></a>
#### 2. 图片资源引用
引用图片资源，如background（@drawable）。<br />第一步：将图片复制到res目录下的drawable文件夹中。<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586435134208-fbb10af2-fd05-45a4-b648-bad535ec27bd.png#align=left&display=inline&height=375&margin=%5Bobject%20Object%5D&name=image.png&originHeight=375&originWidth=363&size=16998&status=done&style=none&width=363)<br />第二步：在要引用的地方加上@drawable/图片名称实现引用，如（android:background="@drawable/test"）。
```xml
      <Button
        android:id="@+id/btn"
        android:layout_width="331dp"
        android:layout_height="351dp"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="96dp"
        android:background="@drawable/test"
        android:text="button" />
```


<a name="L3xqr"></a>
#### 3.字符串引用
@String引用字符串<br />第一步：找到res目录下名为values文件夹下的名为strings的xml文件。<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586435614051-d4e28cb5-c1c0-4a6b-90ff-04d7b8fc46d9.png#align=left&display=inline&height=382&margin=%5Bobject%20Object%5D&name=image.png&originHeight=382&originWidth=350&size=15159&status=done&style=none&width=350)<br />第二步：在其中通过<string>标签定义我们需要显示的文本。
```xml
<resources>
    <string name="app_name">notepad</string>
    <string name="title">我是TextView控件中的文本哦</string>
</resources>
```
第三步：通过@string/要引用的文本别名，如（ android:text="@string/title" ）。
```xml
    <Button
        android:gravity="top|center_horizontal"
        android:id="@+id/btn"
        android:layout_width="331dp"
        android:layout_height="351dp"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="96dp"
        android:background="@drawable/test"
        android:textColor="@color/white"
        android:text="@string/title" />
```


<a name="yeuS5"></a>
#### 3.布局文件中的尺寸数值引用
@dimen引用<br />第一步：在res目录下名为values文件夹下新建一个名为dimen的xml文件。<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586588934946-6dd51854-de26-463e-9721-439e31745eb5.png#align=left&display=inline&height=368&margin=%5Bobject%20Object%5D&name=image.png&originHeight=368&originWidth=291&size=12070&status=done&style=none&width=291)<br />第二步：在其中通过<dimen>标签定义我们需要显示的文本。
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <dimen name="text">25sp</dimen>
</resources>
```
第三步：通过@dimen/要引用的数值别名，如（ android:textSize="@dimen/text" ）。
```xml
 <TextView
        android:text="0"
        android:textSize="@dimen/text"
        android:id="@+id/textview"
        android:layout_below="@id/seekerbar"
        android:layout_centerHorizontal="true"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```

<br />


---

<a name="pnKw9"></a>
## 常用控件
<a name="o9dvG"></a>
### 1. TextView
**autoLink****属性(自动跳转链接)，可以跳转拨号、浏览器、电子邮件等等。**<br />如在TextView中添加自动跳转“百度”
```xml
    <TextView
        android:gravity="top|center_horizontal"//通过“|”可为控件属性同时设置多个属性值
        android:id="@+id/btn"
        android:layout_width="331dp"
        android:layout_height="351dp"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="96dp"
        android:background="@drawable/test"
        android:textColor="@color/white"
        android:text="点击百度：http://www.baidu.com"
        android:autoLink="web"/>
```

<br />控制TextView中的text显示几行及是否加上省略号

         - android:ellipsize="end"//指定在哪里添加省略号
         - android:lines="1"//指定显示几行

如：我想在TextView里最多显示2行，多余的在末尾显示省略号代替
```xml
    <TextView
        android:gravity="top"
        android:id="@+id/btn"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="96dp"
        android:ellipsize="end"
        android:lines="2"
       android:text="djfkdjflksjdlkfjlksdjfdskfkddjfkdjflksjdlkfjlksdjfdskfkdjflksdlfjlkdsfsdlkflkdkfjsdkjfkdjsfjdsfdjdklfjlsdjfjflksdlfjlkdsfsdlkflkdkfjsdkjfkdjsfjdsfdjdklfjlsdjf"
        />
```

---



<a name="xOCTY"></a>
### 2.Button
Button是TextView的子类，所以将继承来自TextView的各种属性。
<a name="NAFYx"></a>
#### 监听器实现方式

   - 创建成员内部类
   - 创建匿名内部类
   - Activity直接实现监听器接口
   - 通过XML布局文件定义onClick属性

---



<a name="Qk1nd"></a>
### 3. EditText
 EditText是TextView的子类，所以将继承来自TextView的各种属性。
<a name="SQHvm"></a>
#### 1. 修改EditText中输入文本的显示类型：
属性：android:inputType="输入的类型限定"<br />如，我们要做一个密码输入框：
```xml
    <EditText
        android:text="1234"
        android:inputType="textPassword"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
```
<a name="5gIAB"></a>
#### 2. EditText中的提示内容
属性：android:hint="提示内容"<br />           android:textColorHint="提示内容的颜色"
```xml
    <EditText
        android:gravity="center_horizontal"
        android:hint="请输入密码"
        android:textColorHint="@color/blue"
        android:inputType="textPassword"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
```
<a name="nKa2Z"></a>
#### 3. 限制输入框文本长度
属性：android:maxLength="具体的长度（数字表示）"，建议再加上hint属性提示，更加友好。
```xml
  <EditText
        android:maxLength="5"
        android:gravity="center_horizontal"
        android:hint="请输入密码(最多5位)"
        android:textColorHint="@color/blue"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
```
<a name="iYH9U"></a>
#### 4.输入框内容实时监听
```kotlin
class MainActivity : AppCompatActivity() {

    private val logTag = "tag"
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //当输入框里内容改变时（包括输入的实时监听）
        etInput.addTextChangedListener(object:TextWatcher{
            override fun afterTextChanged(s: Editable?) {
                Log.i(logTag,"after:s[$s]")
            }

            override fun beforeTextChanged(s: CharSequence?, start: Int, count: Int, after: Int) {
                Log.i(logTag,"before:s[${s.toString()}],start:[$start],after:[$after]")
            }

            override fun onTextChanged(s: CharSequence?, start: Int, before: Int, count: Int) {
                Log.i(logTag,"Text:s[${s.toString()}],start:[$start],count:[$count]")
                if (count < 8){
                    tvHint.text = "你输入的字符太少，请至少再输入：${s.toString().length}"
                }
            }
        })
    }
}
```

---



<a name="2m8Xi"></a>
### 4. ImageView
装载图片的可视控件
<a name="pizPC"></a>
#### 1. 引用图片资源
```xml
    <ImageView
        android:src="@drawable/test"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```
<a name="hfbmJ"></a>
#### 2. 缩放类型
当缩放类型为"center"时，在ImageView中居中显示图片资源，图片可能拉伸。
```xml
    <ImageView
        android:scaleType="center"
        android:src="@drawable/test"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
当缩放类型为"centerInside"时，也在ImageView中居中显示图片资源，但图片不会拉伸。
```xml
 <ImageView
        android:scaleType="centerInside"
        android:src="@drawable/test"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
当缩放类型为"centerCrop"时，将图片资源等比放大后铺满整个ImageView中。（适用于应用的启动页面）
```xml
    <ImageView
        android:scaleType="centerCrop"
        android:src="@drawable/test"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
当缩放类型为"fitStart"时，将图片资源显示到ImageView控件的顶部。
```xml
    <ImageView
        android:scaleType="fitStart"
        android:src="@drawable/test"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
当缩放类型为"fitEnd"时，将图片资源显示到ImageView控件的底部。
```xml
    <ImageView
        android:scaleType="fitEnd"
        android:src="@drawable/test"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```
当缩放类型为"fitCenter"时，将图片资源显示到ImageView控件的居中位置。
```xml
    <ImageView
        android:scaleType="fitCenter"
        android:src="@drawable/test"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```

---



<a name="78t9E"></a>
### 5. CheckBox
<a name="NK4ev"></a>
#### 1. 如果要默认选中某一个CheckBox控件，可以在CheckBox的XML属性中设置：
属性：android:checked="true"
```xml
    <CheckBox
        android:checked="true"
        android:text="篮球"
        android:id="@+id/basketball"
        android:layout_marginTop="50dp"
        android:layout_below="@id/my_toolbar"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
```
当然也可以通过Kotlin代码的方式设置：
```kotlin
 basketball.isChecked = true
```

<br />

<a name="Vs34H"></a>
#### 2. CheckBox的监听
```kotlin
class Main2Activity : AppCompatActivity() {
   	private var list = ArrayList<CheckBox>()
	override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main2)

        //将所有checkbox添加进集合中
        list.add(basketball)
        list.add(playGames)

        //判断打篮球是否选中
        Toast.makeText(this,"${basketball.isChecked}",Toast.LENGTH_LONG).show()

        //为集合中的每一个checkbox添加监听器，当选中或取消选中时通过Toast显示当前状态
        for(index in list){
           index.setOnCheckedChangeListener { buttonView, isChecked ->
               Toast.makeText(buttonView.context,"控件名字："+buttonView.text+"，是否选中：" + isChecked,Toast.LENGTH_LONG).show()
           }
        }
  	}
 }
```

---



<a name="lRlzS"></a>
### 6. RadioButton

   - RadioGroup是个可以容纳多个RadioButton的容器。
   - 在RadioGroup中的RadioButton控件可以有多个，但同时有且仅有一个可以被选中。
- 单选按钮实现

1、在布局文件中定义RadioGroup<br />2、在RadioGroup中添加RadioButton<br />3、在Java代码中获取控件对象
<a name="n7nTN"></a>
#### 1.XML布局示例
```xml
   <RadioGroup
        android:layout_centerInParent="true"
        android:layout_marginTop="30dp"
        android:orientation="horizontal"
        android:layout_below="@id/basketball"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content">
        <RadioButton
            android:text="听歌"
            android:id="@+id/music"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"/>
        <RadioButton
            android:text="跳舞"
            android:id="@+id/dance"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"/>
       <!--  默认选中此单选按钮 -->
        <RadioButton
            android:checked="true"
            android:text="睡觉"
            android:id="@+id/sleep"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"/>
    </RadioGroup>
```
<a name="a4eQ1"></a>
#### 2. RadioButton的监听
```kotlin
class Main2Activity : AppCompatActivity() {
   	private var radiobtn = ArrayList<RadioButton>()
	override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main2)

        radiobtn.add(music)
        radiobtn.add(dance)
        radiobtn.add(sleep)

        for (index in radiobtn){
            index.setOnCheckedChangeListener { buttonView, isChecked ->
                Toast.makeText(buttonView.context,"控件名字："+buttonView.text+"，是否选中：" + isChecked,Toast.LENGTH_LONG).show()
            }
        }
  	}
 }
```

---

<a name="pgZqZ"></a>
### 
<a name="6xrXn"></a>
### 7. SeekerBar
可拖拽进度条。
<a name="5AnAM"></a>
#### SeekerBar的监听
```kotlin
  class MainActivity : AppCompatActivity() {

    @RequiresApi(Build.VERSION_CODES.O)
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        seekerbar.min = 1
        seekerbar.max = 200

        textview.text = "当前进度值：${seekerbar.progress}"
        textview1.text = "触摸状态：未开始"

        //设置监听
        seekerbar.setOnSeekBarChangeListener(object:SeekBar.OnSeekBarChangeListener{
            override fun onProgressChanged(seekBar: SeekBar?, progress: Int, fromUser: Boolean) {
                textview.text = "当前进度值：$progress, 是否为用户手指触摸：$fromUser"
            }

            override fun onStartTrackingTouch(seekBar: SeekBar?) {
               textview1.text = "触摸状态：开始"
            }

            override fun onStopTrackingTouch(seekBar: SeekBar?) {
                textview1.text  = "触摸状态：取消"
            }
        })
    }
}
```

---


<br />

<a name="U0u7c"></a>
### 8. ProgressBar

   - ProgressBar样式
   - ProgressBar进度
   - ProgressBar常用方法



<a name="oiMB1"></a>
#### 1. ProgressBar样式
主要分为两种：一种是圆形样式，一种是水平线样式。（默认为圆形样式，可通过style属性更改为水平线样式）当我们不确定当前操作的准备进度值时可以采用圆形进度条的样式，比如页面的刷新，加载。

属性：<br />max：最大进度值<br />progress：当前进度<br />SecondaryProgress：次要进度（比如播放视频时的缓冲进度）<br />style：进度条样式<br />style属性说明：<br />style="?android:attr/progressBarStyleHorizontal"    水平线样式<br />进度条的进度设置：<br />incrementProgressBy(2)//当前进度累加“每次增加的数值”<br />incrementSecondaryProgressBy(50)//次要进度累加“每次增加的数值”<br />

<a name="gCw1G"></a>
#### 案例：点击按钮改变进度条的进度
效果展示：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586594042668-53ed3718-941b-4161-8d9e-91f6b3e5d420.png#align=left&display=inline&height=386&margin=%5Bobject%20Object%5D&name=image.png&originHeight=864&originWidth=423&size=124414&status=done&style=none&width=189)<br />XML布局示例：
```xml
 <?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:id="@+id/main_layout">


    <TextView
        android:text="0"
        android:textSize="26dp"
        android:layout_marginTop="50dp"
        android:id="@+id/progress_text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"/>

    <ProgressBar
        android:max="300"
        android:progress="200"
        android:layout_width="300dp"
        android:id="@+id/progressbar"
        android:layout_marginTop="20dp"
        android:secondaryProgress="300"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"
        android:layout_below="@id/progress_text"
        style="?android:attr/progressBarStyleHorizontal" />

    <LinearLayout
        android:gravity="center_horizontal"
        android:layout_below="@id/progressbar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        <Button
            android:text="-"
            android:id="@+id/btn1"
            android:layout_marginRight="50dp"
            android:layout_below="@id/progressbar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"/>
        <Button
            android:text="+"
            android:id="@+id/btn2"
            android:layout_toRightOf="@id/btn1"
            android:layout_below="@id/progressbar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"/>
    </LinearLayout>

</RelativeLayout>
```
代码文件：
```kotlin
 class MainActivity : AppCompatActivity() {

    private var btnList = ArrayList<Button>();
    private var count:Int = 0

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //将按钮添加到集合中
        btnList.add(btn1)
        btnList.add(btn2)

        //显示进度条的默认值
        progress_text.text = "当前进度值：${progressbar.progress}"

        //为集合中的按钮设置监听事件
        for (index in btnList){
            index.setOnClickListener {
                when (it.id){
                    btn1.id -> progressbar.progress -= 1
                    btn2.id -> progressbar.progress += 1
                }
                //将设置后的进度值更新到TextView中
                progress_text.text = "当前进度值：${progressbar.progress}"
            }
        }
    }
}
```

---


<br />

<a name="daDHe"></a>
### 9. RatingBar
星级评分条。<br />属性：<br />android:rating="5"//默认评分。<br />android:isIndicator="true"//是否允许交互（true为只显示评分，不能响应用户点击）。<br />android:numStars="8"//星星的个数。<br />android:stepSize="0.5"//每次累加的数值(1为每次加一个星星)。
<a name="hgaIj"></a>
#### 1.XML布局示例
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:id="@+id/main_layout">


    <TextView
        android:text="0"
        android:textSize="26dp"
        android:layout_marginTop="50dp"
        android:id="@+id/ratingbar_text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"/>

  <RatingBar
      android:rating="5"
      android:id="@+id/ratingbar"
      android:isIndicator="false"
      android:numStars="8"
      android:stepSize="0.5"
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"/>

</RelativeLayout>
```
<a name="tOGHX"></a>
#### 2.代码文件
```kotlin
class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)


        //显示星级评分条的默认值
        ratingbar_text.text = ratingbar.rating.toString()

        //设置监听事件
        ratingbar.setOnRatingBarChangeListener { ratingBar, rating, fromUser ->
            ratingbar_text.text = rating.toString()+"是否为用户点击：$fromUser,控件id为：${ratingBar.id}"
        }
    }
}
```

---


<br />

<a name="5YoAL"></a>
### 10. TimePicker与DatePicker
属性：<br />android:timePickerMode="spinner"//将TimePicker设置为滚动样式<br />android:datePickerMode="spinner"//将DatePicker设置为滚动样式<br />android:calendarViewShown="false"//将DatePicker中的日历面板隐藏<br />效果：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586601342558-d9fdad6a-0d90-4366-8442-6f68d61e1e82.png#align=left&display=inline&height=456&margin=%5Bobject%20Object%5D&name=image.png&originHeight=849&originWidth=421&size=125640&status=done&style=none&width=226)
<a name="nDgHU"></a>
#### <br />
<a name="sosvR"></a>
#### 1. XML布局示例
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:id="@+id/main_layout">
    <TimePicker
        android:id="@+id/timepicker"
        android:numbersBackgroundColor="#00ff00"
        android:numbersSelectorColor="@color/colorPrimary"
        android:timePickerMode="spinner"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
    <DatePicker
        android:calendarViewShown="false"
        android:datePickerMode="spinner"
        android:layout_below="@id/timepicker"
        android:id="@+id/datepiker"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>
</RelativeLayout>
```
<a name="Fuy7O"></a>
#### 2. 代码文件
```kotlin
class MainActivity : AppCompatActivity() {
    private var year:Int = 0
    private var month:Int = 0
    private var day:Int = 0
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        //获取系统时间对象
        var c:Calendar = Calendar.getInstance()
        //拿到年，月，日
        year = c.get(Calendar.YEAR)
        month = c.get(Calendar.MONTH)
        day = c.get(Calendar.DAY_OF_MONTH)

        Toast.makeText(applicationContext,"$year / ${month+1} / $day",Toast.LENGTH_SHORT).show()

        //设置时间控件的“时”，“分”
        timepicker.hour = 20
        timepicker.minute = 10
        //时间显示格式是否为24小时制
        timepicker.setIs24HourView(true)

        //为时间控件设置监听器
        timepicker.setOnTimeChangedListener { view, hourOfDay, minute ->
            Toast.makeText(applicationContext,"${hourOfDay}/${minute}",Toast.LENGTH_SHORT).show()
        }

        //为日期控件初始化并设置监听器
        datepiker.init(year,month,day) { view, year, monthOfYear, dayOfMonth ->
            Toast.makeText(applicationContext,"${year}/${monthOfYear+1}/${dayOfMonth}",Toast.LENGTH_SHORT).show()
        }
    }
}
```

---

<a name="7wnED"></a>
### <br />
<a name="TmTCP"></a>
### <br />
<a name="H9maB"></a>
### 11. DrawerLayout
实现侧滑菜单效果的控件<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1587700627795-557a1782-78c7-4ef2-8ade-c6855dbd4c16.png#align=left&display=inline&height=557&margin=%5Bobject%20Object%5D&name=image.png&originHeight=616&originWidth=385&size=21939&status=done&style=none&width=348)
<a name="TN0D2"></a>
#### 1. XML布局示例
```xml
<androidx.drawerlayout.widget.DrawerLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent">
            <Button
                android:layout_width="100dp"
                android:layout_height="100dp"/>
        </LinearLayout>
        <LinearLayout
            android:background="@color/colorPrimaryDark"
            android:layout_gravity="end"//表示从右边侧滑出侧滑菜单，“start”表示从左边侧滑
            android:layout_width="match_parent"
            android:layout_height="match_parent">
            <Button
                android:text="侧滑菜单项"
                android:layout_width="50dp"
                android:layout_height="20dp"/>
        </LinearLayout>
</androidx.drawerlayout.widget.DrawerLayout>
```

---

<a name="T7d79"></a>
## <br />
<a name="WLqZo"></a>
### 12. ScrollView(滚动条)

   - ScrollView和HorizontalScrollView是为控件或者布局添加滚动条。
   - ScrollView和HorizontalScrollView只能有一个子控件。
   - ScrollView用于设置垂直滚动条，HorizontalScrollView用于设置水平滚动。



<a name="zIKC9"></a>
#### ScrollView - XML布局示例
```xml
<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <LinearLayout
            android:orientation="vertical"
            android:layout_width="match_parent"
            android:layout_height="match_parent">
            <Button
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginTop="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
        </LinearLayout>
    </ScrollView>
</LinearLayout>

```


<a name="BIBCu"></a>
#### HorizontalScrollView - XML布局示例
```xml
<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <HorizontalScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <LinearLayout
            android:orientation="horizontal"
            android:layout_width="match_parent"
            android:layout_height="match_parent">
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
            <Button
                android:layout_marginRight="10dp"
                android:layout_width="match_parent"
                android:layout_height="100dp"
                android:background="@color/colorPrimaryDark"/>
        </LinearLayout>
    </HorizontalScrollView>
</LinearLayout>

```

---

<a name="ofyih"></a>
## <br />
<br />
<a name="0RXwK"></a>
## Toast
<br />

- 给用户一个提示信息，不需要用户响应。

<br />
<a name="xgUYf"></a>
### 构建Toast

   - 静态方法makeText()
   - 需通过构造函数（它将接受一个Context参数）创建一个新Toast实例



<a name="FWE4Y"></a>
#### 1. 静态方法makeText()
```kotlin
class MainActivity : AppCompatActivity() {
    
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
         Toast.makeText(this,"我是Toast",Toast.LENGTH_SHORT).show()
    }
}
```
当我们项目中没引入anko库时，也可以将Toast处理一下了方便我们调用
```kotlin
class MainActivity : AppCompatActivity() {  
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        toast("你好啊，我是Toast!")
    }
    fun Context.toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()
}
```

<br />

<a name="hXL3M"></a>
#### 2. 构造函数构建
```kotlin
class MainActivity : AppCompatActivity() {
    
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        btnToast.setOnClickListener {
            var toast = Toast(this@MainActivity)
            toast.view = LayoutInflater.from(this@MainActivity).inflate(R.layout.toast_item,null)
            toast.duration = Toast.LENGTH_SHORT
            toast.show()
        }
    }
}
```

---



<a name="a2KeP"></a>
## AlertDialog
<br />

   - 模态对话框。
   - AlertDialog将弹出并获取焦点，一直显示，直到被用户关闭。
   - 用于提醒关键信息。



<a name="rL7md"></a>
### 1. 简单对话框

```kotlin
class MainActivity : AppCompatActivity() {
    
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        button2.setOnClickListener {
            var alertDialog = androidx.appcompat.app.AlertDialog.Builder(this@MainActivity)
            alertDialog.setIcon(R.drawable.ic_launcher_background)//设置图标
                    .setTitle("消息提示框")//设置标题
                    .setMessage("你的手机性能")//设置提示内容
                    .setPositiveButton("确定",null)//设置右边按钮
                    .setNegativeButton("中",null)//设置中间按钮
                    .setNeutralButton("取消",null)//设置左边按钮
                    .create()//创建

            alertDialog.show()//显示
        }
    }
}
```


效果<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1588078229319-700bd4fb-3135-475a-b3b4-443678976ab4.png#align=left&display=inline&height=414&margin=%5Bobject%20Object%5D&name=image.png&originHeight=749&originWidth=515&size=63120&status=done&style=none&width=285)

<a name="TtASz"></a>
### 2. 列表对话框
![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1588079175219-b4ff4e50-b0ef-44c8-bd1a-acdebc278a0a.png#align=left&display=inline&height=386&margin=%5Bobject%20Object%5D&name=image.png&originHeight=612&originWidth=514&size=50499&status=done&style=none&width=324)
```kotlin
class MainActivity : AppCompatActivity() {

    fun Context.toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        button2.setOnClickListener {
            var alertDialog = androidx.appcompat.app.AlertDialog.Builder(this@MainActivity)

            alertDialog.setIcon(R.drawable.message)
                    .setTitle("列表对话框")
                    .setItems(arrayOf("选项一","选项二","选项三","选项四","选项五")) { _, which ->
                        when (which){
                            0 -> toast("我是选项一")
                            1 -> toast("我是选项二")
                            2 -> toast("我是选项三")
                            3 -> toast("我是选项四")
                            4 -> toast("我是选项五")
                        }
                    }
                    .show()
        }
    }
}

```
监听器为：DialogInterface.OnClickListener，代码中我们使用了lambda表达式进行监听器的创建。
<a name="3YEkb"></a>
### <br />
<a name="64fWE"></a>
### 3. 单选对话框
和列表对话框的区别仅仅只是将setItems改为setSingleChoiceItems,但要注意的是，setSingleChoiceItems方法的第二个参数为我们默认选中的菜单项。           
```kotlin

class MainActivity : AppCompatActivity() {


    //通过懒加载的方式创建出单选对话框,然后在按钮被点击的时候显示出来，这样就避免了每点一次按钮就创建出一个新的对话框，而导致上一次所选择的菜单项被重置为默认值。
    private val alertDialog by lazy {
        var alertDialog = androidx.appcompat.app.AlertDialog.Builder(this@MainActivity)
        alertDialog.setIcon(R.drawable.message)
                .setTitle("列表对话框")
                .setSingleChoiceItems(arrayOf("选项一","选项二","选项三","选项四","选项五"),0) { dialog, which ->
                    when (which){
                        0 -> toast("我是选项一")
                        1 -> toast("我是选项二")
                        2 -> toast("我是选项三")
                        3 -> toast("我是选项四")
                        4 -> toast("我是选项五")
                    }
                }.create()
    }


    fun Context.toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        button2.setOnClickListener {
            alertDialog.show()
        }
    }
}

```

<br />效果：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1588080762638-cee97576-27b5-426e-a023-919ae2414ff6.png#align=left&display=inline&height=511&margin=%5Bobject%20Object%5D&name=image.png&originHeight=511&originWidth=516&size=57204&status=done&style=none&width=516)<br />
<br />

<a name="1HghL"></a>
### 4. 多选对话框

<br />通过setMultiChoiceItems方法来设置对话框为多选对话框，第二个参数为默认选中的菜单项。
```kotlin

class MainActivity : AppCompatActivity() {

    private val alertDialog by lazy {
        var alertDialog = androidx.appcompat.app.AlertDialog.Builder(this@MainActivity)
        alertDialog.setIcon(R.drawable.message)
                .setTitle("列表对话框")
                .setMultiChoiceItems(arrayOf("1","2","3","4","5"), booleanArrayOf(true,false,false,true,false)) { _, which, isChecked ->
                    if (isChecked){
                        when (which){
                            0 -> toast("1")
                            1 -> toast("2")
                            2 -> toast("3")
                            3 -> toast("4")
                            4 -> toast("5")
                        }
                    }
                }
                .create()
    }


    fun Context.toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        button2.setOnClickListener {
            alertDialog.show()
        }
    }
}


```
效果：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1588083226484-bc8d3b11-f12d-4753-be95-a34fa003c881.png#align=left&display=inline&height=553&margin=%5Bobject%20Object%5D&name=image.png&originHeight=553&originWidth=513&size=51874&status=done&style=none&width=513)<br />
<br />

<a name="PHnD9"></a>
## 适配器模型及简单使用


   - Android的适配器(Adapter)负责为选择部件提供数据源，也负责将单独的数据元素转换为显示在选择部件中的特定视图。就是将数据转换为控件能显示的内容。



<a name="d4fx2"></a>
### ArrayAdapter

- ArrayAdapter接受3个参数
   - 要使用的上下文（通常就是当前的activity的实例）
   - 要使用的视图的资源ID
   - 要实际显示的选项数组或列表



<a name="3jZCC"></a>
### SimpleAdapter


<a name="XbR9Q"></a>
#### 1. 主布局示例
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    >

    <ListView
        android:id="@+id/lvTest"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>

</RelativeLayout>
```


<a name="liZPz"></a>
#### 2. ListView自定义布局示例
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ImageView
        android:id="@+id/iv"
        android:src="@drawable/bank"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <TextView
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:background="@color/colorPrimaryDark"
        android:text="first"
        android:id="@+id/text"
        android:textSize="28dp"
        android:gravity="center_horizontal"
        android:layout_width="100dp"
        android:layout_height="wrap_content"/>

</LinearLayout>
```


<a name="jq8lE"></a>
#### 2. 代码文件
```kotlin

class MainActivity : AppCompatActivity() {

    private val nameArr = arrayOf("张高三","王小二","杰克","艾伦","琳达","张高三","王小二","杰克","艾伦","琳达","张高三","王小二")
    private val picArr = intArrayOf(R.drawable.bank,R.drawable.fund,R.drawable.light,R.drawable.money,R.drawable.phone,R.drawable.bank,R.drawable.fund,R.drawable.light,R.drawable.money,R.drawable.phone,R.drawable.money,R.drawable.phone)

    fun Context.toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        var data =  ArrayList<HashMap<String,String>>()
        for (index in 0..10){
            var tempMap  = HashMap<String,String>()
            tempMap["name"] = nameArr[index]
            tempMap["pic"] = picArr[index].toString()
            data.add(tempMap)
        }

        var adapter = SimpleAdapter(
            applicationContext,//上下文
            data,//数据源
            R.layout.listview_item,//项布局(自定义的listView布局文件)
            arrayOf("name","pic"),//数据源key值
            intArrayOf(R.id.text,R.id.iv)//显示数据的控件id
        )
        lvTest.adapter = adapter//设置已经设置好的适配器给listView

        //为listView添加监听器
        lvTest.setOnItemClickListener { _, _, _, id ->
            toast("$id")//显示用户当前点击的项
        }
    }
}

```

<br />效果：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1588133300251-e185b832-aeca-4dd5-a1c6-f59d4a75b629.png#align=left&display=inline&height=420&margin=%5Bobject%20Object%5D&name=image.png&originHeight=751&originWidth=526&size=203785&status=done&style=none&width=294)<br />
<br />

<a name="637Yr"></a>
### BaseAdapter
<a name="QuwOC"></a>
#### 1. 主布局示例
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
  
    <ListView
        android:id="@+id/lvTest"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>

</RelativeLayout>
```


<a name="EDH6F"></a>
#### 1. ListView自定义布局示例
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android" 
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ImageView
        android:id="@+id/iv"
        android:src="@drawable/bank"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"/>

    <TextView
        android:layout_marginLeft="50dp"
        android:paddingTop="10dp"
        android:paddingBottom="10dp"
        android:background="@color/colorPrimaryDark"
        android:text="first"
        android:id="@+id/text"
        android:textSize="28dp"
        android:gravity="center_horizontal"
        android:layout_width="100dp"
        android:layout_height="wrap_content"/>

</LinearLayout>
```
<a name="PdLus"></a>
#### 1. BaseAdapter代码文件
```kotlin
class MyAdapter : BaseAdapter{

    var context : Context? = null
    private val names = arrayOf("小天","小王","小明","小美","小赵","小浩","小刘","小小怪","小张","小米渣","小土豆")
    private val pics = intArrayOf(R.drawable.phone,R.drawable.money,R.drawable.light,
        R.drawable.phone,R.drawable.money,R.drawable.light,R.drawable.phone,R.drawable.money,R.drawable.light,R.drawable.phone,R.drawable.money)

    constructor(context:Context){
      this.context = context
    }

    override fun getView(position: Int, convertView: View?, parent: ViewGroup?): View {

        var listView1:View
        if (convertView == null){
            listView1 = LayoutInflater.from(this.context).inflate(R.layout.listview_item,null)
        } else {
            listView1 = convertView
        }

        var ivPic = listView1.findViewById<ImageView>(R.id.iv)
        var tvName = listView1.findViewById<TextView>(R.id.text)

        ivPic.setOnClickListener {
            Toast.makeText(this.context,"$position",Toast.LENGTH_SHORT).show()
        }

        ivPic.setImageResource(pics[position])
        tvName.text = names[position]

        return listView1
    }

    override fun getItem(position: Int): Any {
        return names[position]
    }

    override fun getItemId(position: Int): Long {
        return position.toLong()
    }

    override fun getCount(): Int {
        return names.size
    }
}

```


<a name="1CVDG"></a>
#### MainActivity代码文件
```kotlin

class MainActivity : AppCompatActivity() {

    fun Context.toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        lvTest.adapter = MyAdapter(this)
    }
}

```

---


<br />

<a name="EO37Z"></a>
## GridView

   - 显示文本内容
   - 显示图片与文本
   - 以网格方式进行显示


<br />

<a name="Cya6t"></a>
## Fragment


<a name="630Go"></a>
### Fragment的概念

   - Fragment是在Android 3.0（API level11）开始引入新的API技术。
   - 为了提高代码重用性和改善用户体验，我们将Activity中的UI组件进行分组和模块化管理。这些分组后的UI组件就是Fragment。
   - 一个Activity页面中可以包含多个Fragment模块，而同一个Fragment模块也可以被多个Activity使用。
   - 每个Fragment有自己的布局，有自己的生命周期。
   - Fragments必须放在一个Activity中
   - Fragments有它自己的生命周期，而且受到它所在的宿主Activity的生命周期的影响
   - Fragments可以接收它自己的事件
   - 一个Fragment可以放在多个Activity中，一个Activity中也可以放置多个FragmentsFragments


<br />
<br />
<br />


---


<br />
<br />

<a name="1egRg"></a>
## LayoutInflater
将一个XML视图转化为一个View。

---

<a name="mFFL8"></a>
### <br />
<a name="2dM0e"></a>
## 自定义控件
<br />
<a name="xKRly"></a>
#### View是怎么工作的

1. 构造器 -> 初始化
1. onMesure（）定大小
1. onLayout（）定位置
1. onDraw（）绘制
1. invalidate（）刷新

---

<a name="C4jqM"></a>
## <br />
<a name="aw1YR"></a>
## <br />
<a name="g8G2A"></a>
## Activity配置与Activity间的通讯
<br />
<a name="5E1wV"></a>
### 1. Activity的配置
必须在AndroidManifest中通过Activity标签做相应的配置。
<a name="wL0HK"></a>
### 2. Activity间的通讯
<a name="dHqK3"></a>
### <br />
<a name="zOa3m"></a>
### <br />
<a name="idiz8"></a>
## 广播机制
<br />

- 1.Android的广播机制介绍
- 2.BroadcastReceiver的作用
- 3.BroadcastReceiver的编写方法
- 4.BroadcastReceiver的生命周期

---



<a name="ZwpSV"></a>
## Service那些事

   - Service是一种Android的组件，可以在后台长时间运行
   - Service不提供界面交互
      - 即便用户跳转至另一个应用后，Service仍旧在后台运行任意
      - 应用组件都可以绑定服务，甚至可以用来完成进程间通讯的任务
         - 需要下载时
         - 播放音乐
         - 文件1/0



<a name="NEbsl"></a>
### Service的启动方式

- Service可以通过两种方式来调用
   - start ：一旦某个组件start一个Service后，Service开始独立运行，不在与原来的组件产生任何关系。(独立运行)。



   - bind ：某个组件bind一个service后，Service为组件提供一个接口，近似于客户端，会进行互相的交互。(可以交互)，需要注意的是，如果对应的Activity被销毁掉，那么这个服务也应该被销毁掉。我们可以在Activity里的onDestroy卸载相应服务。

---

<a name="DO5aW"></a>
## <br />
<a name="NhiTk"></a>
## <br />
<br />
<a name="nxHyu"></a>
## Handler

   - Android采用一种复杂的Message Queue机制保证线程间通信。
   - Message Queue是一个消息队列，用来存放通过Handler发布的消息。
   - Android在第一次启动程序时会默认为Ul线程创建一个关联的消息队列，用来管理程序的组件，如Activity，Service，Broatcast Receiver等。
   - 可以在工作线程中创建Handler与Ul线程通信。

![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1587701565428-2bb64cb5-7841-48bc-9346-5cdb908ab5ef.png#align=left&display=inline&height=418&margin=%5Bobject%20Object%5D&name=image.png&originHeight=418&originWidth=951&size=86846&status=done&style=none&width=951)

   - 工作线程可以通过Handler对象和主线程通讯。
   - Handler对象的所有工作将在主线程中执行。
   - Handler类需要实现handleMessage（）方法，来处理消息队列中取出的Message对象。
   - handleMessage（）方法由主线程调用，可以在需要的时候更新UI界面。但是，必须确保此方法快速完成，因为其他UI操作会等待它完成才能执行。
   - 可以在Message中附加不同的参数。
<a name="iVYk6"></a>
### Handler的编程接口
![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1587701810759-fa7b067f-c443-411b-971e-07209f677795.png#align=left&display=inline&height=289&margin=%5Bobject%20Object%5D&name=image.png&originHeight=352&originWidth=906&size=316679&status=done&style=none&width=744)

<a name="qpcTI"></a>
#### 1. XML布局示例
```xml
<LinearLayout  xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <androidx.drawerlayout.widget.DrawerLayout

    android:id="@+id/drawerlayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <LinearLayout
        android:orientation="vertical"
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <TextView
            android:id="@+id/tvMsg"
            android:text="0"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"/>
        <Button
            android:text="主菜单"
            android:id="@+id/btnOpenLayout"
            android:layout_width="100dp"
            android:layout_height="100dp"/>
    </LinearLayout>
    <LinearLayout
        android:orientation="vertical"
        android:background="@color/colorPrimaryDark"
        android:layout_gravity="end"
        android:layout_width="200dp"
        android:layout_height="match_parent">
        <Button
            android:text="我的"
            android:layout_width="200dp"
            android:layout_height="80dp"/>
        <Button
            android:text="购物车"
            android:layout_marginTop="3dp"
            android:layout_width="200dp"
            android:layout_height="80dp"/>
        <Button
            android:text="设置"
            android:layout_marginTop="3dp"
            android:layout_width="200dp"
            android:layout_height="80dp"/>
    </LinearLayout>
</androidx.drawerlayout.widget.DrawerLayout>
</LinearLayout>

```



<a name="UuvC2"></a>
#### 2.代码文件
```kotlin
class TouchDemoActivity : AppCompatActivity() {

    private var handler  = object : Handler() {
            override fun handleMessage(msg: Message) {
                when (msg.what) {
                    0x0001 -> tvMsg.text = msg.arg1.toString()
                }
                super.handleMessage(msg)
            }
        }


    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_touch_demo)


        btnOpenLayout.setOnClickListener {
            object:Thread(){
                override fun run() {
                    for (index in 0..10){
                        var msg = Message()
                        msg.what = 0x0001
                        msg.arg1 = index
                        handler.sendMessage(msg)
                        sleep(1000)
                    }
                }
            }.start()
        }
    }
}


```

---

<a name="EAOqR"></a>
### 


<a name="X0gl3"></a>
## XML解析
Android项目中XML文件资源位于res/xml目录下，它们在部署时将被编译为有效的二进制形式，根据需要可以自定义XML结构，Android中使用pull方式来解析XMLAndroid中使用pull方式来解析XML。<br />

<a name="RqUBj"></a>
#### 1. 待解析的XML文件
```xml
<?xml version="1.0" encoding="utf-8"?>
<words >
    <xxoo value="one">1</xxoo>
    <xxoo value="two">2</xxoo>
    <xxoo name="three">3</xxoo>
    <xxoo name="four">4</xxoo>
    <xxoo name="five">5</xxoo>
</words>
```


<a name="J3J1N"></a>
#### 2.代码文件
```kotlin
package com.kotlinandroiddemo.ontouchdemo

import android.content.res.Resources
import android.graphics.drawable.Drawable
import android.os.Bundle
import android.os.Handler
import android.os.Message
import android.util.Log
import androidx.appcompat.app.AppCompatActivity
import androidx.core.content.ContextCompat
import androidx.core.content.res.ResourcesCompat
import org.xmlpull.v1.XmlPullParser


class TouchDemoActivity : AppCompatActivity() {

    private var handler = object : Handler() {
        override fun handleMessage(msg: Message) {
            if (msg.what == 0x0001) {
                var resultList: ArrayList<String> = msg.obj as ArrayList<String>
                Log.i(PULLTAG, "-------------------------------------------")
                for (obj in resultList) {
                    Log.i(PULLTAG, obj.toString())
                }

            }
            super.handleMessage(msg)
        }
    }

    companion object {
        const val PULLTAG = "PULLTAG"
    }

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_touch_demo)

        var xmlPullParser = resources.getXml(R.xml.demoxml)//拿到需要解析的XML文件



        xmlPull(xmlPullParser)
    }

    private fun xmlPull(xmlPullParser: XmlPullParser) {
        //因为xml文件的解析一般来说是个耗时的过程，所以有必要为它开启一个子线程，解析完后再通知主线程
        object : Thread() {
            override fun run() {

                var eventType = xmlPullParser.eventType//拿到事件类型
                var resultList = ArrayList<String>()

                //判断当前的事件类型是否等于文档结束类型，如果是，证明xml文件解析结束
                while (eventType != XmlPullParser.END_DOCUMENT) {
                    //判断时间类型
                    when (eventType) {
                        //元素解析开始
                        XmlPullParser.START_TAG ->
                            //比对元素名字是否不为根元素“words”
                            if (xmlPullParser.name.toString() != "words") {
                                Log.i(
                                    PULLTAG,
                                    "元素名字：[${xmlPullParser.name.toString()}]， " + "当前的事件类型为：START,属性值为：[${xmlPullParser.getAttributeValue(
                                        0
                                    )}]，" + "属性名为：[${xmlPullParser.getAttributeName(0)}]"
                                )
                                //添加进集合
                                resultList.add(
                                    "元素名字：[${xmlPullParser.name.toString()}]， " + "当前的事件类型为：START,属性值为：[${xmlPullParser.getAttributeValue(
                                        0
                                    )}]，" + "属性名为：[${xmlPullParser.getAttributeName(0)}]"
                                )
                            }

                        //元素解析结束
                        XmlPullParser.END_TAG ->
                            if (xmlPullParser.name.toString() != "words") {
                                Log.i(PULLTAG, "元素名字：[${xmlPullParser.name.toString()}], 当前的事件类型为：END-TAG")
                            }
                    }
                    //往下继续解析
                    eventType = xmlPullParser.next()
                    sleep(500)
                }

                    var msg = Message()
                    msg.what = 0x0001

                    msg.obj = resultList
                    handler.sendMessage(msg)
            }
        }.start()
    }
}



```

---


<br />

<a name="g7vYn"></a>
## JSON解析

   - JSON（javascript object notation），是一种轻量级的数据储存和交换格式。
   - 它是完全独立于语言的文本格式。
   - JSON易于阅读、编写，也易于机器解析和生成。
   - 实际上JSON就是一个文本文件。
      - 示例：

String data = "{}"<br />

<a name="qQz19"></a>
#### JSON基本格式

      - 键值对对象格式：用“{}”包围。
      - 数组格式：用“[]”包围。 


<br />
<br />
<br />
<br />
<br />


---

<a name="dbTmw"></a>
### 


<a name="BitVL"></a>
## 数据存储


<a name="OXO64"></a>
### 一、SharedPreference

   - 数据存储的意义
         - 保存用户私有数据和配置
         - 比如音效设置，音乐文件，视频文件，短信，联系人
         - 需要在关机后重启仍能有效>需要存储到外部介质中
   - 存储的内容
      - 一种轻量级的数据存取方法，以键值对来存储应用程序的配置信息
      - 只能存储基本的数据类型：boolean，float，int，long，string
      - 以XML文件的格式保存，位于/data/data/Package_Name/shared_prefs目录下



```kotlin
class MainActivitySharedPreference : AppCompatActivity() {

    //得到SharedPreferences对象,通过getSharedPreferences方法得到，第一个参数为数据存储的文件名,第二个参数为存储的模式
    private val preference by lazy {
        getSharedPreferences("test", Context.MODE_PRIVATE)
    }

    private fun toast(msg:String) = Toast.makeText(this,msg,Toast.LENGTH_SHORT).show()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main_shared_preference)

        btnWrite.setOnClickListener {

            //得到“编辑者”对象
            var editor = preference.edit()

            //储存数据：以键值对的方式进行存储
            editor.putString("index",etText.text.toString())
            editor.putString("index1","你好")

            //别忘记要提交哦
            editor.commit()
            toast("写入成功！")
        }

        btnRead.setOnClickListener {
            //通过刚刚储存时指定的key值取出value,
            var read = preference.getString("index","-1").toString()
            etText.setText(read+"，${preference.getString("index1","-1").toString()}")
            toast("读取成功！")
        }
    }
}

```

<br />

<a name="GsP6i"></a>
### 案例：
<a name="W0Kxw"></a>
#### 1.图片切换案例
案例：使用ImageView和RadioButton控件来实现不同图片的切换，包括了一个图片全屏启动缩放动画的实现。<br />效果展示：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586584547107-78aa16ff-eba0-4574-b1af-531eec0aadae.png#align=left&display=inline&height=451&margin=%5Bobject%20Object%5D&name=image.png&originHeight=851&originWidth=421&size=380595&status=done&style=none&width=223)![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586584506087-5d054034-7b63-4250-aa21-8db7f279de51.png#align=left&display=inline&height=451&margin=%5Bobject%20Object%5D&name=image.png&originHeight=844&originWidth=415&size=309137&status=done&style=none&width=222)![image.png](https://cdn.nlark.com/yuque/0/2020/png/1159653/1586584462335-b68e75a8-6c34-4d80-843b-0d76f4489f98.png#align=left&display=inline&height=451&margin=%5Bobject%20Object%5D&name=image.png&originHeight=846&originWidth=405&size=355150&status=done&style=none&width=216)<br />
<br />项目的github地址：[点击进入项目github下载页面](https://github.com/sweetheart-january/AndroidDemo1)

---


<br />
<br />
<br />
<br />

   - 记录选择器
      - 新建一个xml文件，并以selector作为根元素，通过itme来指定每一种状态下的行为。


<br /><?xml version="1.0" encoding="utf-8"?><br /><selector xmlns:android="http://schemas.android.com/apk/res/android">    <br /><item android:state_focused ="true" android:drawable="@drawable/edittextshapeselected"></item>               <item android:state_focused ="false" android:drawable="@drawable/edittextshape"></item><br /></selector>

常用状态：<br />当我们需要指定一个button按下时的状态：android:state_checked<br />选择输入框：android:state_focused


