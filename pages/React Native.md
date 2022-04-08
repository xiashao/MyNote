# Day1

## 一、移动端APP开发方式介绍

#### **1.1、app的分类(按开发方式)**

大致可以分为这3种：

- native app（原生app :    iOS或安卓）
- web app  (APIclound)
- hybrid app（混合app）

#### 1.2、各类开发方式的APP介绍

**原生应用程序（NativeAPP）**

原生(Native)应用程序是某一个移动平台（比如iOS或安卓）所特有的，使用相应平台支持的开发工具和语言（比如iOS平台支持Xcode和Objective-C,Swift，安卓平台支持Eclipse和Java）。原生应用程序外观和运行起来（性能）是最佳的。

 

**H5应用程序（H5APP/WEBAPP）**

HTML5应用程序使用标准的Web技术，通常是HTML5、JavaScript和CSS。这种只编写一次、可到处运行的移动开发方法构建的跨平台移动应用程序可以在多个设备上运行。虽然开发人员单单使用HTML5和JavaScript就能构建功能复杂的应用程序，但截至本文截稿时仍然存在一些重大的局限性，具体包括会话管理、安全离线存储以及访问原生设备功能（摄像头、日历和地理位置等）。

 

**混合应用程序（HybridAPP）**

混合(Hybrid)应用程序让开发人员可以把HTML5应用程序嵌入到一个细薄的原生容器里面，集原生应用程序和HTML5应用程序的优点（及缺点）于一体。



![img](assets/u=3751435793,1229583550&fm=26&gp=0.jpg) 

#### 1.3、各类app的优缺点 

**native app**
 **优点：**

- 提供最佳用户体验，最优质的用户界面，流畅的交互
- 可以访问本地资源
- 可以调用移动硬件设备，比如摄像头、麦克风等

**缺点：**

- 开发成本高。每种移动操作系统都需要独立的开发项目，针对不同平台提供不同体验；
- 发布新版本慢。下载是用户控制的，很多用户不愿意下载更新（比如说，版本发布到了3.0，但还是有很多1.0的用户，你可能就得继续维护1.0版本的API）
- 应用商店发布审核周期长。安卓平台大概要1~3天，而iOS平台需要的时间更长

 

 **web app**
 **优点：**

- 整体量级轻，开发成本低
- 不需要用户进行手动更新，由应用开发者直接在后台更新，推送到用户面前的都是全新版本，更便于业务的开展
- 基于浏览器，可以跨平台使用

**缺点：**

- 资源的都在远程服务器。在网速受到限制时，交互效果也会受到限制。页面跳转费力，不稳定感更强。
- 无法操作很多手机原生设备，摄像头，麦克风，不支持多点触控等。

 

**Hybrid app**
这类app集合了上面两种app各自的优势：

- 在实现更多功能的前提下，使得app安装包不至于过大

- 在应用内部打开web网页，省去了跳转浏览器的麻烦

- 主要功能区相对稳定下，部分功能区采用web 形式，使得迭代更加方便

- 融合了原生APP和WebApp优点（速度快，跨平台）

  

![img](assets/timg.jpg) 



## 二、ReactNative简介

React Native使你只使用JavaScript也能编写原生移动应用。 它在设计原理上和React一致，通过声明式的组件机制来搭建丰富多彩的用户界面。 

React Native最终产品很贴近移动应用，从使用感受上和用Objective-C或Java编写的应用相比几乎是无法区分的。 React Native所使用的基础UI组件和原生应用完全一致。 你要做的就是把这些基础组件使用JavaScript和React的方式组合起来。 所以有React基础，那么学习 RN会非常轻松。 

ReactNative官网：http://facebook.github.io/react-native

ReactNative中文官网： <https://reactnative.cn/> 



## 三、搭建RN开发环境前的说明

注意：**RN开发环境对版本要求极高，所有环境严格按照指定版本来安装，版本不一致会导致无法正常运行**

各个环境的搭建遵循的三步曲：

1、安装环境     ====>    2、配置环境变量    ====>    3、检测使用

## 四、Python环境安装

python下载网址：https://www.python.org/getit/    找到对应版本下即可

#### 4.1、安装python 2.x版本

![1575840007692](assets/1575840007692.png)

![1575840112631](assets/1575840112631.png)

![1575840118911](assets/1575840118911.png)

安装路径不用更改，记录下来：

C:\Python27\

(然后一直Next......，直到安装结束)

#### 4.2、配置环境变量

桌面”此电脑“右键，点击”属性“，点击右侧高级系统设置

![1575841307278](assets/1575841307278.png)

新建环境变量PYTHON_HOME

![1575840530190](assets/1575840530190.png)



![1575841062517](assets/1575841062517.png)

#### 4.3、检测使用

命令行窗口中键入python，看到以下  Python2.7.XX 字样则表示安装成功

![1575841487304](assets/1575841487304.png)



## 五、Java环境安装

Java JDK下载网址:  https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

#### 5.1、安装Java jdk 1.8版本

![1575841953550](assets/1575841953550.png)

![1575841962215](assets/1575841962215.png)

这里不建议更改安装路径，记录下这个环境路径：C:\Program Files\Java\jdk1.8.0_151

继续安装jre  ， 注意：jdk和jre安装在同一目录下

![1575841973789](assets/1575841973789.png)

#### 5.2、配置环境变量

新建环境变量JAVA_HOME

![1575842350362](assets/1575842350362.png)



![1575842600150](assets/1575842600150.png)

#### 5.3、检测使用

**关闭刚才的命令行窗口，重新打开命令行窗口**

命令行窗口中键入java

![1575843685995](assets/1575843685995.png)

命令行窗口中键入javac

![1575843729317](assets/1575843729317.png)

键入java和javac，看见以上表示安装成功

## 六、Android环境安装

下载网址：http://www.androiddevtools.cn

![1575842907454](assets/1575842907454.png)

![1575842929071](assets/1575842929071.png)

#### 6.1、安装Android Studio 3.14版本

![1575842947777](assets/1575842947777.png)

![1575842963003](assets/1575842963003.png)

#### 拷贝SDK（Android运行环境）到Android目录下，解压

![1575843426373](assets/1575843426373.png)



#### 6.2、配置环境变量

新建环境变量 ANDROID_HOME

![1575843517223](assets/1575843517223.png)



Path环境：%ANDROID_HOME%\platform-tools

![1575843898709](assets/1575843898709.png)

#### 6.3、检测使用

命令行窗口中键入  adb devices

![1575844036585](assets/1575844036585.png)

命令能成功执行，安装成功

## 七、Android模拟器安装

#### 7.1、Genymotion软件和依赖的vbox虚拟器环境



Genymotion官网地址：<https://www.genymotion.com>

安装Genymotion

![1575844372984](assets/1575844372984.png)

建议换个路径，不在装在C盘(建议在刚才的Android目录下)，安装成功后弹出安装虚拟机盒子：

![1575844346983](assets/1575844346983.png)

![1575844503403](assets/1575844503403.png)

继续下一步默认选项即可(**虚拟机不要更改安装路径，并且路径不能有中文**)

安装完成后有个安装后引导，取消这个勾即可

![1575844680159](assets/1575844680159.png)

安装成功后会多出3个图标：

![1573724075427](assets/1573724075427.png)

#### 7.2、注册Genymotion账号

注册Genymotion账号网址：<https://www.genymotion.com/account/create/> 

注册成功后自己保存好账号密码！！！！后面要用！

![1575845081336](assets/1575845081336.png)

#### 7.3、使用Genymotion

双击图标

![1575845229845](assets/1575845229845.png)

点击登录：

![575845281989](assets/1575845281989.png)

![1575845417723](assets/1575845417723.png)

键入用户名密码后点击登录：

![1575845459783](assets/1575845459783.png)

点击Sign in登录后会继续弹出：

![1575845644268](assets/1575845644268.png)

点击Personal Use  个人使用：

弹出同意协议页面：

![1575845730276](assets/1575845730276.png)

勾上，点击Accept

![1575845789918](assets/1575845789918.png)

看见以上界面表示登录成功

#### 7.4、下载手机模拟器

![1575845953046](assets/1575845953046.png)

![1575846007030](assets/1575846007030.png)

再点击Next即可自动下载手机模拟器了

注意：这个下载过程很容易断开，一旦发现过了很久之后进度条仍然不动，可以尝试点击Cancle按钮然后重新点击下载，它会在原来的基础上继续下载。

下载完成后：

![1575846164000](assets/1575846164000.png)

![1575846468828](assets/1575846468828.png)

#### 7.5、检测模拟器or真机是否连接成功

  命令行窗口 输入adb devices 检测和计算机连接的Android设备列表：

![1575846699968](assets/1575846699968.png)

## 八、ReactNative脚手架的创建

**操作前先！确保Node是v12.10.0版本   (nvm use v12.10.0)**

```
如果未安装12.10.0版本：
nvm install v12.10.0
nvm use v12.10.0
npm install -g yarn
```



Yarn设置镜像源：

yarn config set registry https://registry.npm.taobao.org --global 

yarn config set disturl https://npm.taobao.org/dist --global

```
reactnative的项目无法使用cnpm安装依赖。所以，需要使用facebook团队提供的yarn包管理工具：
	yarn global add react-native-cli   

	检测是否安装成功：
	F:\RN>react-native -v
	'react-native' 不是内部或外部命令，也不是可运行的程序或批处理文件。

	如果不成功， 使用下面的命令安装脚手架：
	npm install -g yarn react-native-cli
	
	重新检测是否安装成功：
	F:\RN>react-native -v
	react-native-cli: 2.0.1
	react-native: n/a - not inside a React Native project directory
```

## 九、创建ReactNative项目

react-native init  项目名  --version 0.55.4  （**要求必须跟上版本号**）       

注意：**项目名和项目路径不能有中文**

	例如：react-native init rn_demo --version 0.55.4

等待下载完毕即可...



**启动手机模拟器**(或者连入手机，手机必须是调试模式/开发者模式）
在终端执行adb devices    （只要有一个设备即可）

	F:\RN>adb devices
	List of devices attached
	xxxxxxxxxxx        device


**启动项目**：

进入到项目目录下：执行  **react-native run-android** 命令  启动项目

**再次强调项目目录不要出现中文！！！！！！**

第一次启动项目会很慢，耐心等待... ...



![1575848725767](assets/1575848725767.png)



看到以上界面说明项目启动成功

# 

# Day2

## 一、自定义组件

RN中自定义组件和react中自定义组件类似，但在使用RN基本组件的时候，需要先进行引入：

```js
import {View, Text, StyleSheet} from 'react-native'
```

但是样式的书写和react不同，是通过react-native模块中的  StyleSheet.create()方法来书写，然后在组件中的style属性值中引用。

RN中视图中出现文字的地方一定要用<Text></Text>组件包起来

书写步骤：

创建RN项目后，删除app.js，新建components文件夹，在components文件夹中新建App1.js：

```jsx
// 引入核心库
import React, { Component } from 'react'
import {View, Text, StyleSheet} from 'react-native'

// 创建并到处类(组件)
export default class App1 extends Component {
    render() {
        return (
            <View style={styles.box1}>
                <Text style={styles.text1}>hello,你好！</Text>
            </View>
        )
    }
}

// 创建样式
const styles = StyleSheet.create({
    box1:{
        backgroundColor: 'pink'
    },
    text1:{
        fontSize:20,
        fontFamily:"宋体"
    }
})
```

在index.js中，修改引入组件的路径

```js
import { AppRegistry } from 'react-native';
import App from './components/App1';

AppRegistry.registerComponent('rn_demo', () => App);
```

## 二、View组件

View组件是容器组件，用它来装载其他组件，类似于div。

使用StyleSheet API来创建样式。

在RN中，组件主要使用style属性来接收样式定义。



需要注意的是，超出View组件的内容是不会显示的。如果想要实现溢出可见，则需要配合ScrollView组件。

```jsx
import React, { Component } from 'react'
import {View, Text, StyleSheet} from 'react-native'

export default class App1 extends Component {
    render() {
        return (
            <View style={styles.box1}>
                <Text style={styles.text1}>hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！</Text>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    box1:{
        backgroundColor: 'pink',
        width:100,
        height:100
    },
    text1:{
        fontSize:20,
        fontFamily:"宋体"
    }
})
```

## 三、初步了解ScrollView组件

在上面案例中，如果需要展示盒子溢出内容，View组件中嵌入ScrollView组件。例如：

```jsx
<View style={styles.box1}>
    {/* 配合ScrollView组件，实现溢出可以出现滚动条 
    如果需要出现横向滚动条，需要给ScrollView组件加上 horizontal
    */}
    <ScrollView horizontal={true}>
    <Text style={styles.text1}>hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！hello,你好！</Text>    
    </ScrollView>
</View>
```

## 四、RN获取屏幕宽高及屏幕像素比

文档：https://reactnative.cn/docs/height-and-width/

RN中通过Dimensions组件来获取屏幕宽高

```jsx
import React, { Component } from 'react'
import {ScrollView, Text, StyleSheet, View, Dimensions} from 'react-native'

const {width, height} = Dimensions.get("window")

export default class App1 extends Component {
    render() {
        return (
            <View style={styles.box1}>
                <Text>屏幕宽度是：{width}，屏幕高度是：{height}</Text>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    box1:{
        backgroundColor: 'pink',
    }
})
```

获取像素比:

```jsx
// width宽度逻辑像素
// height高度逻辑像素  对于不同像素的屏幕，屏幕逻辑像素不一样
// scale缩放比
const {width, height, scale} = Dimensions.get("window")


export default class App1 extends Component {
    render() {
        return (
            <View style={styles.box1}>
                <Text>屏幕宽度是：{width}，屏幕高度是：{height}</Text>
                <Text>屏幕缩放比是：{scale}</Text>
                {/*  对于不同像素的屏幕(即不同型号手机)，屏幕逻辑像素不一样，即宽度不一定都是360*/}
                {/* 缩放比对不同的手机也可能不一样，不是固定值 */}

            </View>
        )
    }
}

```

面试题： 为什么获取屏幕分辨率，为什么获取的屏幕高度和真实高度不一致？
Dimensions.get("window")获取的是屏幕可用范围的宽高(不是绝对宽高)



注意：

对于不同像素的屏幕(即不同型号手机)，屏幕逻辑像素不一样，即宽度不一定都是360

缩放比对不同的手机也可能不一样，不是固定值

## 五、练习题

1、书写一个满屏的盒子

2、书写一条最细的线

```jsx
// 书写一个满屏的盒子
// 书写一个最细的线

import React, { Component } from 'react'
import {ScrollView, Text, StyleSheet, View, Dimensions} from 'react-native'

const {width, height, scale} = Dimensions.get("window")


export default class App1 extends Component {
    render() {
        return (
            <View style={styles.box1}>
                <Text>屏幕宽度是：{width}，屏幕高度是：{height}</Text>
                <Text>屏幕缩放比是：{scale}</Text> 
                <View style={styles.line}></View>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    // box1:{
    //     width,
    //     height,
    //     backgroundColor: 'pink',
    // },
    box1:{
        flex:1,
        backgroundColor: 'green',
    },
    line:{
        width,
        height:1/scale,   //最细的线   
        backgroundColor: '#000',
    }
})
```

## 六、Flex布局

官方文档原话：

我们在 React Native 中使用 flexbox 规则来指定某个组件的子元素的布局。Flexbox 可以在不同屏幕尺寸上提供一致的布局结构。

一般来说，使用`flexDirection`、`alignItems`和 `justifyContent`三个样式属性就已经能满足大多数布局需求。

#### 6.1、display属性

display 设置此组件的显示类型。它的值只支持'flex'和'none'。'flex'是默认值。

#### 6.2、flex属性

在React Native 中，flex的值是一个正数，它的大小将与其弹性值成比例。

#### 6.3、flexDirection属性

flexDirection控制主轴的方向

flexDirection的4个值：'row'，'row-reverse'，'column'，'column-reverse'

'row'  设置主轴为水平正向     123

'row-reverse'  设置主轴为水平反向     321

 'column'  设置主轴为垂直正向    123

 'column-reverse'  设置主轴为垂直反向     321

布局如下：

```jsx
...
	<View style={styles.container}>
        <View style={styles.box1}><Text>1</Text></View>
        <View style={styles.box2}><Text>2</Text></View>
        <View style={styles.box3}><Text>3</Text></View>
    </View>

...

const styles = StyleSheet.create({
    container:{
        flexDirection:'column-reverse',
        flex:1
    },
    box1:{
        width:100,
        height:100,
        backgroundColor:"#ccc"
    },
    box2:{
        width:100,
        height:100,
        backgroundColor:"#fcf",
    },
    box3:{
        width:100,
        height:100,
        backgroundColor:"#cff",
    }
})
```

#### 6.4、justifyContent属性

justifyContent控制主轴的对齐方式

justifyContent的5个值：'flex-start'，'flex-end'，'center'，'space-between'，'space-around'

'flex-start': 左(或顶)对齐  默认值

'flex-end' 右(或底)对齐

'center' 居中对齐 

'space-between' 中间留白

'space-around' 中间及两侧留白

```jsx
const styles = StyleSheet.create({
    container:{
        flexDirection:'row',
        flex:1,
        justifyContent:'flex-start'
    },
    ...
})
```

#### 6.5、alignItems属性

alignItems属性控制侧轴对其方式

alignItems属性的5个值：  'flex-start'，'flex-end'，'center'，'stretch'，'baseline'

'flex-start': 左(或顶)对齐  默认值

'flex-end' 右(或底)对齐

'center' 居中对齐 

'stretch' 设置侧轴拉伸，此时侧轴方向(宽或者高)不要给固定数值，才能看得见拉伸效果

'baseline' 设置基线对齐，文字底部对齐

```jsx
			<View style={styles.container}>
                <View style={styles.box1}><Text style={{fontSize:20}}>1</Text></View>
                <View style={styles.box2}><Text style={{fontSize:10}}>2</Text></View>
                <View style={styles.box3}><Text style={{fontSize:40}}>3</Text></View>
            </View>
            ...
 const styles = StyleSheet.create({
    container:{
        flexDirection:'row',
        flex:1,
        justifyContent:'flex-start',
        alignItems:'baseline'
    },
    box1:{
        width:100,
        height:100,
        backgroundColor:"#ccc",
    },
    box2:{
        width:100,
        height:100,
        backgroundColor:"#fcf",
    },
    box3:{
        width:100,
        // height:100,
        backgroundColor:"#cff",
    }
})
```

## 七、Flex布局练习

![1575924619738](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day02/assets/1575924619738.png)

```jsx
import React, { Component } from 'react'
import {Text, View, Dimensions, StyleSheet} from "react-native"

const {width} = Dimensions.get("window")
export default class App3 extends Component {
    render() {
        return (
            <View style={styles.container}>
                <Text style={{marginBottom:15,fontSize:20}}>Flex布局</Text>
                <View style={styles.box}>
                    <View style={styles.row}>
                        <View style={styles.item1}><Text>1</Text></View>
                        <View style={styles.item2}><Text>2</Text></View>
                        <View style={styles.item3}><Text>3</Text></View>
                    </View>
                    <View style={styles.row}>
                        <View style={styles.item1}><Text>1</Text></View>
                        <View style={styles.item2}><Text>2</Text></View>
                        <View style={styles.item3}><Text>3</Text></View>
                    </View>
                    <View style={styles.row}>
                        <View style={styles.item1}><Text>1</Text></View>
                        <View style={styles.item2}><Text>2</Text></View>
                        <View style={styles.item3}><Text>3</Text></View>
                    </View>
                </View>
            </View>
        )
    }
}
const styles = StyleSheet.create({
    container:{
        marginTop:50,
        flex:1,
        alignItems:'center'
    },
    box:{
        width:width*0.9,
        height:200,
        backgroundColor:"#fcf",
    },
    row:{
        flex:1,
        borderWidth:1,
        borderColor:"#000",
        flexDirection:'row',
    },
    item1:{
        flex:1.5,
        borderWidth:1,
        borderColor:"red",
    },
    item2:{
        flex:1,
        borderWidth:1,
        borderColor:"red",
    },
    item3:{
        flex:2,
        borderWidth:1,
        borderColor:"red",
    }
})
```



## 八、Button组件

RN中，展示按钮使用的是 Bttton组件，https://reactnative.cn/docs/button/，

```jsx
<Button style={styles.btn} title="点我！" color="pink" onPress={this.handlePress}></Button>
```

Button 组件的几个重要属性：   

title 按钮上的展示文字

color 按钮的背景颜色（安卓），或者文本颜色（IOS）

onPress  按压事件(即点击事件)

```jsx
import React, { Component } from 'react'
import {View, Text, Button, StyleSheet} from 'react-native'

export default class App7 extends Component {

    constructor(props){
        super(props)
        this.state = {
            num:89
        }
        this.handlePress = this.handlePress.bind(this)
    }

    handlePress(){
        this.setState({
            num:this.state.num+1
        })
    }

    render() {
        return (
            <View>
                <Text>{this.state.num}</Text>
                <Button style={styles.btn} title="点我！" color="pink" onPress={this.handlePress}></Button>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    btn:{
        width:100
    }
})
```

## 九、自定义按钮组件TouchableOpacity

因为Button样式本身有局限性。TouchableOpacity组件可以自由定义组件样式。

```jsx
import React, { Component } from 'react'
import {View, Text, Button, StyleSheet, TouchableOpacity} from 'react-native'

export default class App7 extends Component {

    constructor(props){
        super(props)
        this.state = {
            num:89
        }
        this.handlePress = this.handlePress.bind(this)
    }

    handlePress(){
        this.setState({
            num:this.state.num+1
        })
    }

    render() {
        return (
            <View>
                <TouchableOpacity style={styles.myBtn} onPress={this.handlePress}>
                    <Text>自定义按钮</Text>
                </TouchableOpacity>
                <Text>{this.state.num}</Text>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    myBtn:{
        width:100,
        height:100,
        backgroundColor:"pink",
        borderRadius:50,
        justifyContent:"center",
        alignItems:"center"
    }
})
```

## 十、Image组件

**引入方式一**：

```jsx
import ImgUrl from '../res/banner1.png'
<Image source={ImgUrl}/>
```

**引入方式二**：

```jsx
<Image source={require('../res/logo.png')}/>
```

**引入方式三**：

```jsx
<Image source={{ uri:"https://www.baidu.com/img/baidu_resultlogo@2.png" }}  style={styles.st2}/> 
注意：这种引入方式需要给图片添加宽高样式，才能看得见图片
```



## 十一、WebView组件

WebView组件相当于在app内部内嵌一个浏览器，可以通过它的source属性中的uri，写入对应网页地址，从而展示一个页面。

```jsx
import React, { Component } from 'react'
import {WebView} from 'react-native'

export default class App10 extends Component {
    render() {
        return (
            <WebView source={{ uri: "https://m.jd.com/"}} ></WebView>    
        )
    }
}

```

通过上面的代码可以在应用中直接打开看到京东H5页面

# Day3

## 一、图片的另一种引入方式

在\android\app\src\main\res\ 目录下新建drawable文件夹，存放资源图片。

```jsx
<Image source={{ uri:"图片名" } }  style={styles.st1} />    
```

引入的是app内部资源图片

注意:

1    uri后面直接书写图片名称，不需要后缀名，同样需要设置宽高样式

2    重新编译应用(重新执行react-native run android)

​	重新编译引用可能会报错: java.io.IOException 的问题, 此时只要把 android目录下的缓存清理掉即可，清理缓存的命令如下:

```
cd android

gradlew clean    (执行之前建议先在模拟器中关掉项目，否则有可能报错)

再退回项目根目录

重新执行react-native run-android
```



## 二、FlatList组件的使用 

FlatList的使用：

```jsx
<View >
    <FlatList
        numColumns={1}		//每行显示个数
        data={ this.state.arr_data }	//数据源
        renderItem={ this.renderData }	//渲染函数
        />    
</View>

... ...

renderData({item}){  // item 就是数组数据中的每一项对象
    return (
        <View >
            <Text>{item.id}、{item.data}</Text>    
        </View> 
    ) 
}
```



完整代码

```jsx
import React, { Component } from 'react'
import {View, Text, FlatList} from 'react-native'

const arr_data=[
    {
        id:1,
        data:10
    },
    {
        id:2,
        data:20
    },
    {
        id:3,
        data:30
    },
    {
        id:4,
        data:40
    },
]

export default class App1 extends Component {
    constructor(props){
        super(props)

        this.state = {
            arr_data
        }
    }
    renderData({item}){  // item 就是数组数据中的每一项对象
        return (
            <View >
                <Text>{item.id}、{item.data}</Text>    
            </View> 
        ) 
    }
    render() {
        return (
            <View >
                <FlatList
                    numColumns={1}		//每行显示个数
                    data={ this.state.arr_data }	//数据源
                    renderItem={ this.renderData }	//渲染函数
                />    
            </View>
        )
    }
}

```

## 三、图片展示的练习

![1581030846248](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day03/assets/1581030846248.png)

```jsx
import React, { Component } from 'react'
import {View, StyleSheet, Image, Text, FlatList} from 'react-native'


const img_data=[
    {
        name:"p01",
        des:"Puma Defy 赛琳娜限定"
    },
    {
        name:"p02",
        des:"圣罗兰 口红礼盒"
    },
    {
        name:"p03",
        des:"大豆家  方头奶奶鞋"
    },
    {
        name:"p04",
        des:"小狗图案不锈钢皂"
    },
    {
        name:"p05",
        des:"YSL限量眼影银盘"
    },
    {
        name:"p06",
        des:"可折叠加厚双面使用榻榻米床垫"
    }

]

export default class App1 extends Component {
    constructor(props){
        super(props)

        this.state = {
            img_data
        }
    }
    renderData({item}){
        return (
            <View style={styles.itemBox}>
                
                <Image source={{uri:item.name}}  style={{width:100,height:100}}/>

                <Text style={styles.tit}>{item.des}</Text>    
            </View> 
        ) 
    }
    render() {
        return (
            <View style={styles.container}>
                <View style={styles.boxs}>

                    <Image source={{uri:"tit_50x16"}} style={{width:50,height:16, marginTop:10,marginBottom:10}}/>
                    
                    
                    <FlatList
                        numColumns={3}		//每行显示个数
                        data={ this.state.img_data }	//数据源
                        renderItem={ this.renderData }	//渲染函数
                    />    
                    
                    
                   
                </View>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    container:{
        flex:1,
        backgroundColor:"#ddd",
        alignItems:"center"
    },
    boxs:{
        width:340,
    },
    imgs:{
        flexDirection:"row"
    },
    tit:{
        fontSize:12,
        height: 16,
        lineHeight:16
    },
    itemBox:{
        width:100,
        marginRight:20,
        marginBottom:10
    }

})
```

## 四、TextInput 组件

TextInput文本输入组件的使用：

```jsx
import React, { Component } from 'react'
import {View, StyleSheet, TextInput} from 'react-native'

export default class App3 extends Component {
    render() {
        return (
            <View>
                <TextInput 
                    style={styles.txt}
                    placeholder="请输入..."     // 占位符设置(提示文本)
                    placeholderTextColor="#ccc"    //   占位符颜色设置
                    // maxLength = {6}         //  可以输入的最大长度
                    // underlineColorAndroid='transparent'   // 底线设置透明
                    // secureTextEntry = {true}    //安卓下的密码设置
                />
            </View>
        )
    }
}
const styles = StyleSheet.create({
    txt:{
        borderWidth:1,
        // height:40,
    }
})
```

## 五、登录界面的实现

![2020-02-06_214151](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day03/assets/2020-02-06_214151.jpg)



完整代码：

```jsx
import React, { Component } from 'react'
import {View, StyleSheet,Dimensions, Image, Text, TextInput, TouchableOpacity} from 'react-native'
const {height,scale} = Dimensions.get("window")
export default class App3 extends Component {
    render() {
        return (
            <View style={styles.container}>
                <View  style={styles.wrap}>
                    {/* 头像 */}
                    <Image source={require('../res/avatar.jpg')}  style={styles.avatar}/>
                    {/* 两个输入框 */}
                
                    <TextInput 
                        // style={Object.assign({},styles.txt)}
                        style={[styles.username,styles.txt]}
                        placeholder="请输入用户名"     // 占位符设置(提示文本)
                        placeholderTextColor="#ccc"    //   占位符颜色设置
                        underlineColorAndroid='transparent'   // 底线设置透明
                    />
                    <TextInput 
                        style={styles.txt}
                        placeholder="请输入密码"     // 占位符设置(提示文本)
                        placeholderTextColor="#ccc"    //   占位符颜色设置
                        underlineColorAndroid='transparent'   // 底线设置透明
                        secureTextEntry = {true}    //安卓下的密码设置
                    />
                    {/* 登录按钮 */}
                    <TouchableOpacity style={styles.loginBtn} activeOpacity={0.7}>
                        <Text style={styles.loginText}>
                            登 录
                        </Text>
                    </TouchableOpacity>
                    {/* 忘记密码和注册账号 */}
                    <View style={styles.newUser}>
                        <TouchableOpacity activeOpacity={0.8}>
                            <Text style={{fontSize:10}}>
                                忘记密码
                            </Text>
                        </TouchableOpacity>
                        <TouchableOpacity activeOpacity={0.8}>
                            <Text style={{fontSize:10}}>
                                注册新用户
                            </Text>
                        </TouchableOpacity>
                    </View>
                    {/* 其他方式登录 */}    
                    <View style={styles.others}>
                        <View style={styles.line}></View>
                        <View style={styles.othersTitle}><Text  style={{fontSize:12}}>其他方式登录</Text></View>
                        <View style={styles.icons}>
                            <TouchableOpacity activeOpacity={0.8}>
                                <Image source={require("../res/icon1.png")} style={styles.icon}/>
                            </TouchableOpacity>
                            <TouchableOpacity activeOpacity={0.8}>
                                <Image source={require("../res/icon2.png")} style={[styles.icon,styles.iconSnd]}/>
                            </TouchableOpacity>
                            <TouchableOpacity activeOpacity={0.8}>
                                <Image source={require("../res/icon3.png")} style={styles.icon}/>
                            </TouchableOpacity>
                            
                        </View>
                    </View>
                </View>
                
                
            </View>
        )
    }
}


const styles = StyleSheet.create({
    container:{
        flex:1,
        backgroundColor:"#eee",
        alignItems:"center"
    },
    wrap:{
        width:320,
        height,
        alignItems:"center"
    },
    avatar:{
        width:60,
        height:60,
        borderRadius:30,
        borderWidth:1,
        borderColor:"#fff",
        marginBottom:30,
        marginTop:50,
    },
    txt:{
        width:"100%",
        height:40,
        backgroundColor:"#fff",
        paddingLeft:10,
    },
    username:{
        marginBottom:3
    },
    loginBtn:{
        width:"100%",
        height:30,
        alignItems:"center",
        backgroundColor:"skyblue",
        borderRadius:4,
        marginTop:20
    },
    loginText:{
        lineHeight:30,
        color:"#fff"
    },
    newUser:{
        flexDirection:"row",
        justifyContent:"space-between",
        width:"100%",
        marginTop:10
    },
    others:{
        width:"100%",
        position:"absolute",
        bottom:50,
        alignItems:"center"
    },
    line:{
        width:"100%",
        height:1/scale,
        backgroundColor:"#999"
    },
    othersTitle:{
        marginTop:-8,
        backgroundColor:"#eee",
        paddingLeft:10,
        paddingRight:10,

    },
    icons:{
        flexDirection:"row",
        marginTop:10
    },
    icon:{
        width:30,
        height:30,
        borderRadius:15
    },
    iconSnd:{
        marginLeft:15,
        marginRight:15,
    }
})
```

## 六、ScrollView的使用 

使用ScrollView组件实现横向多屏：

```jsx
<ScrollView style={styles.box}
	horizontal={true}		//水平排列
	pagingEnabled={true}	//滚动条倍数滚动
	showsHorizontalScrollIndicator={false} 	//不显示横向滚动条（用小圆点代替）
>
	{/* 多屏展示 */}
	<View><Text>第1屏</Text></View>
	<View><Text>第2屏</Text></View>
</ScrollView>
```

完整代码如下：

```jsx
import React, { Component } from 'react'
import {View, StyleSheet, Text,ScrollView} from 'react-native'

export default class App5 extends Component {
    render() {
        return (
            <View >
                <ScrollView horizontal={true} pagingEnabled={true} showsHorizontalScrollIndicator={false}>
                    <View style={[styles.itemBox,styles.itemBox1]}>
                        <Text>第1屏</Text>
                    </View>
                    <View style={[styles.itemBox,styles.itemBox2]}>
                        <Text>第2屏</Text>
                    </View>
                    <View style={[styles.itemBox,styles.itemBox3]}>
                        <Text>第3屏</Text>
                    </View>
                </ScrollView>
                
            </View>
        )
    }
}
const styles = StyleSheet.create({
    itemBox:{
        width:360,
        height:100
    },
    itemBox1:{
        backgroundColor:"#fcf"
    },
    itemBox2:{
        backgroundColor:"#ccc"
    },
    itemBox3:{
        backgroundColor:"#ffc"
    }
})

```

## 七、图片和文字的展示案例

![2020-02-07_032753](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day03/assets/2020-02-07_032753.jpg)

```jsx
import React, { Component } from 'react'
import {View, StyleSheet, Image, Text, ScrollView} from 'react-native'

export default class App5 extends Component {
    render() {
        return (
            <View >
                <ScrollView horizontal={true} pagingEnabled={true} showsHorizontalScrollIndicator={false}>
                    <View style={styles.itemBox}>
                        <Image source={require('../res/banner1.png')} style={{width:360,height:201}}></Image>
                        <View style={styles.titleBox}>
                            <Text  style={styles.titleTxt}>前端让IT互联有魅力</Text>
                        </View>
                    </View>
                    <View style={styles.itemBox}>
                        <Image source={require('../res/banner2.png')} style={{width:360,height:201}}></Image>
                        <View style={styles.titleBox}>
                            <Text style={styles.titleTxt}>Java薪未来</Text>
                        </View>
                    </View>
                    <View style={styles.itemBox}>
                        <Image source={require('../res/banner3.png')} style={{width:360,height:201}}></Image>
                        <View style={styles.titleBox}>
                            <Text style={styles.titleTxt}>全栈UI设计</Text>
                        </View>
                    </View>
                </ScrollView>
            </View>
        )
    }
}
const styles = StyleSheet.create({
    itemBox:{
        width:360
    },
    titleBox:{
        position:"absolute",
        bottom:0,
        backgroundColor:"rgba(0, 0, 0, 0.3)",
        height:30,
        width:360
    },
    titleTxt:{
        color:"#fff",
        lineHeight:30,
        marginLeft:10
    }
    
})

```

## 八、适配其他分辨率的做法

在上一天的学习中，我们了解到，每种机型的Dimensions 宽度、高度、像素比是有可能不一样的，即在我们现在使用的360宽度，在其他机型上就不一定完全适配。

如果出现不适配的情况，可以使用以下解决方案：

比如，我们要在1080(360 x 3)像素的机型上书写340宽度的盒子，则其他机型(width x scale)要书写多少宽度？

推导过程如下：

```
const {width,scale} = Dimensions.get('window')

340/360*3 = ？/width*scale

所以 ？= width*scale*340/1080

所以 ？= (width*scale/1080)*340

即在书写的时候，我们可以先抽取这个物理比率
const wuli = width * scale/1080   

然后让这个物理比率乘以 我们本来要书写的宽度340

所以，适配所有机型的宽度可以这么写：  width: wuli*340
```



完整写法：

```jsx
import React, { Component } from 'react'
import {View, StyleSheet,Dimensions, Image, Text, FlatList} from 'react-native'

const {width,scale} = Dimensions.get('window')
const wuli = width * scale/1080   

... ...

const styles = StyleSheet.create({
    box:{
        width: wuli*340,
        height: wuli*200
    },
})

```

## 九、关闭所有黄色警告的代码

把下面代码添加在index.js中的AppRegistry.registerComponent()前面：

```
console.ignoredYellowBox = ['Warning: BackAndroid is deprecated. Please use BackHandler instead.','source.uri should not be an empty string','Invalid props.style key'];
 
console.disableYellowBox = true // 关闭全部黄色警告
```

# Day4

## 一、搭建环境

1、创建项目

```
react-native init LifeServices --version 0.55.4
```

LifeServices为项目名称

2、打包并运行项目

```
react-native run-android
```



备注：

唤醒手机模拟器中菜单的两种方式：

1、手机模拟器中 Ctrl+m

2、终端中项目目录下执行：  adb shell input keyevent 82

## 二、搭建项目目录

目录结构：

![1576077145388](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day04/assets/1576077145388.png)

先删除项目自带的app.js

/app/App.js中：

```jsx
import React, { Component } from 'react'
import Launcher from './launcher/Launcher'

export default class App extends Component {
    render() {
        return (
            <Launcher />
        )
    }
}

```

/app/launcher/Launcher.js中：

```jsx
import React, { Component } from 'react'
import {View, Text} from 'react-native'

export default class Launcher extends Component {
    render() {
        return (
            <View>
                <Text>LifeServices欢迎页面</Text>
            </View>
        )
    }
}
```

/index.js中修改入口组件的引入路径

```js
import App from './app/App';
```



## 三、启动页面的使用

（使用我们前面讲的第四种方式引入启动图片）

/app/launcher/Launcher.js中：

```jsx
import React, { Component } from 'react'
import {Image, Dimensions} from 'react-native'

const {width,height} = Dimensions.get('window')

export default class Launcher extends Component {
    render() {
        return (
            {/*使用我们前面讲的第四种方式引入启动图片*/}
            <Image source={{uri: "launcher_image"}} style={{width,height}}/>
        )
    }
}

```

在LifeServices/android/app/src/main/res 中新建drawable文件夹，把项目涉及的资源图片放进去

删除 LifeServices/android/app/build 文件夹， 注意！！！**删除的是app下的build文件夹**

再重新启动项目： react-native run-android，即可看到启动图片



## 四、启动图片切换到导航界面

需求：启动图片2秒钟后切换到导航界面



/app/nav目录下新建Nav.js：

```jsx
import React, { Component } from 'react'
import {View, Text} from 'react-native'

export default class Nav extends Component {
    render() {
        return (
           <View>
               <Text>导航界面</Text>
           </View>
        )
    }
}
```

/app/App.js中：

```jsx
import React, { Component } from 'react'
import Launcher from './launcher/Launcher'
import Nav from './nav/Nav'

export default class App extends Component {

    constructor(props){
        super(props)

        this.state = {
            isShowLauncher:true   //通过这个属性来决定是否展示启动界面
        }
    }
    componentDidMount(){
        setTimeout(()=>{
            this.setState({
                isShowLauncher:false
            })
        },2000)
    }
    render() {
        return (
            this.state.isShowLauncher?
            <Launcher />:
            <Nav />
        )
    }
}
```



## 五、导航页面的初步实现

我们使用React Navigation来实现导航效果。React Navigation是Facebook，Expo和React社区的开发者们合作的结果：它取代并改进了React Native生态系统中的多个导航库。

React Navigation官网：https://www.reactnavigation.org.cn/

tabnavigator的使用：https://www.reactnavigation.org.cn/docs/tabnavigator

项目目录下安装React Navigation：

```
yarn add react-navigation@2.18.1 -D
```



在导航页面Nav.js中:

```js
import {TabNavigator} from 'react-navigation'

import Food from '../food/Food'
import Movie from '../movie/Movie'
import Hotel from '../hotel/Hotel'
import Bank from '../bank/Bank'


export default  MyApp = TabNavigator({
    Food: {
        screen: Food,   //Food为组件
    },
    Movie: {
        screen: Movie,
    },
    Hotel: {
        screen: Hotel,
    },
    Bank: {
        screen: Bank,
    },
})
```

Food.js中：（其他几个组件Movie、Hotel、Bank也以下面代码进行书写）

```jsx
import React, { Component } from 'react'
import {View, Text} from 'react-native'

export default class Food extends Component {
    static navigationOptions = {
      tabBarLabel: '美食',
      // Note: By default the icon is only shown on iOS. Search the showIcon option below.
    //   tabBarIcon: ({ tintColor }) => (
    //     <Image
    //       source={require('./chats-icon.png')}
    //       style={[styles.icon, {tintColor: tintColor}]}
    //     />
    //   ),
    };
  
    render() {
      return (
        <View>
            <Text>美食页面的内容</Text>
        </View>
      );
    }
 }
```

注意：此时需要给App.js需要一个满屏的盒子，才能装得下导航和对应页面

App.js中

```jsx
... ...
	render() {
        return (
            <View style={styles.container}>
                {
                    this.state.is_launcher?
                    <Launcher />:
                    <Nav />
                }
            </View>
        )
    }
}
const styles = StyleSheet.create({
    container:{
        flex:1
    }
})
```



## **六、关闭所有黄色警告的代码**

把下面代码添加在index.js中的AppRegistry.registerComponent()前面：

```
console.ignoredYellowBox = ['Warning: BackAndroid is deprecated. Please use BackHandler instead.','source.uri should not be an empty string','Invalid props.style key'];
 
console.disableYellowBox = true // 关闭全部黄色警告
```



## 七、导航页面配置react-navigation

Nav.js中：

```jsx
export default  MyApp = TabNavigator({
    Food: {
        screen: Food,   //food为组件
    },
    Movie: {
        screen: Movie,
    },
    Hotel: {
        screen: Hotel,
    },
    Bank: {
        screen: Bank,
    },
},{
    tabBarPosition: 'bottom',
    animationEnabled: false,
    tabBarOptions: {
        activeTintColor: globalStyle.baseColor,  //选中时候的颜色
        inactiveTintColor: '#000000', //未选中颜色
        showIcon: true,
        style: {
            backgroundColor: '#eee',
            height: 60
          },
        indicatorStyle: { //下面一条线的样式
            height: 0
        }
    },
})
```

Food.js中:(其他三个页面处理方式一致)

```jsx
import React, { Component } from 'react'
import {View, Text, Image} from 'react-native'  //1、引入Image
import globalStyle from '../globalStyle';  //2、引入全局样式

export default class Food extends Component {
    static navigationOptions = {
      tabBarLabel: '美食',
      // Note: By default the icon is only shown on iOS. Search the showIcon option below.
      tabBarIcon: ({ tintColor }) => (
        <Image
          source={{uri:"icon_food"}}   //3、引入资源图片
          style={[globalStyle.navIcon, {tintColor: tintColor}]}   //4、设置icon样式
        />
      ),
    };
  
    render() {
      return (
        <View>
            <Text>美食页面的内容</Text>
        </View>
      );
    }
  }
```

在app下引入全局样式globalStyle.js：

```js
export default {
    baseColor : "#f40",
    navIcon:{
        width: 28,
        height: 28
    }
}
```



## 八、首页头部的实现

food目录下新建FoodTop.js

```jsx
import React, { Component } from 'react'
import { View, Text , StyleSheet, Image, Dimensions, TextInput} from 'react-native' 
let { width, height } = Dimensions.get('window')
import globalStyle from '../globalStyle'
//顶栏
export default class FoodMenu extends Component {
  render() {
    return (
      <View style={styles.container} >
          <Text style={styles.title}>广州市▼</Text>
          <View style={styles.searchView}>
              <Image style={styles.icon} source={{uri: 'icon_search'}} />
              <TextInput 
                placeholder={'请输入...'} 
                style = {{height: 40, flex: 0.95}} 
                underlineColorAndroid='transparent'/>
          </View>
          <Image style={styles.userIcon} source={{uri: 'icon_user'}} />
      </View>
    )
  }
}

const styles = StyleSheet.create({
    container: {
        backgroundColor: globalStyle.baseColor,
        height: 40,
        flexDirection: 'row',
        alignItems: 'center',
        justifyContent: 'space-around'
    },
    icon: {
        width: 20,
        height: 20
    },
    searchView: {
        backgroundColor: '#FFF',
        borderRadius: 20,
        height: 30,
        width: width - 30 - 56 - 20,// 图标30 文字56(单个文字默认大小为14) 其他间隙20(自定义)
        flexDirection: 'row',
        alignItems: 'center',
        paddingLeft: 5
    },
    userIcon: {
        width: 30,
        height: 30
    },
    title: {
        color: '#FFF',
    }
})
```



## 九、美食菜单的实现

#### 9.1、使用ScrollView组件实现横向多屏

文档： https://reactnative.cn/docs/scrollview/

```jsx
<ScrollView style={styles.box}
	horizontal={true}		//水平排列
	pagingEnabled={true}	//滚动条倍数滚动
	showsHorizontalScrollIndicator={false} 	//不显示横向滚动条（用小圆点代替）
>
	{/* 多屏展示 */}
	<View><Text>第1屏</Text></View>
	<View><Text>第2屏</Text></View>
</ScrollView>
```



具体代码：

在food目录中新建FoodMenu.js：

```jsx
import React, { Component } from 'react'
import {View, Text, Image, StyleSheet, ScrollView, Dimensions} from 'react-native'
const {width} = Dimensions.get('window')

export default class FoodMenu extends Component {
    render() {
        return (
            <View style={styles.box}>
                <ScrollView 
                    horizontal={true}		//水平排列
                    pagingEnabled={true}	//滚动条倍数滚动
                    showsHorizontalScrollIndicator={false} 	//不显示横向滚动条
                >
                    {/* 多屏展示 */}
                    <View style={styles.box1}><Text>屏1</Text></View>
                    <View style={styles.box2}><Text>屏2</Text></View>
                </ScrollView>    
            </View>
            
        )
    }
}

const styles = StyleSheet.create({
    box:{
        marginTop: 6
    },
    box1:{
        width,
        height:100,
        backgroundColor: 'pink',
    },
    box2:{
        width,
        height:100,
        backgroundColor: 'green',
    }
})

```



#### 9.2、使用FlatList组件实现列表循环

文档： https://reactnative.cn/docs/flatlist/ 

FlatList的使用：

```jsx
<View style={{height: 160,width: width}}>

    <FlatList
        numColumns={5}		//每行显示个数
        data={ menu.data[i] }	//数据源
        renderItem={ this.renderIcon }	//渲染函数
    />

</View>

...
...

//渲染图标
renderIcon({item}){
    return (
        <View style={styles.icon_box}>
        	<Image source={{uri: item.image}} style={{width: 45, height: 45}} />
        	<Text style={{fontSize: 12}}>{item.title}</Text>
        </View>
    )
}
```



具体项目代码：

```jsx
import React, { Component } from 'react'
import {View, Text, Image, StyleSheet, ScrollView, Dimensions, FlatList} from 'react-native'
const {width} = Dimensions.get('window')
import featrueData from '../json/FeatureData.json'

export default class FoodMenu extends Component {
    render() {
        return (
            <View style={styles.box}>
                <ScrollView 
                    horizontal={true}		//水平排列
                    pagingEnabled={true}	//滚动条倍数滚动
                    showsHorizontalScrollIndicator={false} 	//不显示横向滚动条
                >
                    {/* 多屏展示 */}
                    <View style={styles.box1}>
                        <FlatList
                            numColumns={5}		//每行显示个数
                            data={ featrueData.data[0] }	//数据源
                            renderItem={ this.renderIcon }	//渲染函数
                        />
                        <FlatList
                            numColumns={5}		//每行显示个数
                            data={ featrueData.data[1] }	//数据源
                            renderItem={ this.renderIcon }	//渲染函数
                        />
                    </View>
                    <View style={styles.box1}>

                        <FlatList
                            numColumns={5}		//每行显示个数
                            data={ featrueData.data[2] }	//数据源
                            renderItem={ this.renderIcon }	//渲染函数
                        />
                        <FlatList
                            numColumns={5}		//每行显示个数
                            data={ featrueData.data[3] }	//数据源
                            renderItem={ this.renderIcon }	//渲染函数
                        />
                    </View>
                </ScrollView>    
            </View>
            
        )
    }

    renderIcon({item}){
        return (
            <View style={styles.iconBox}>
                <Image source={{uri: item.image}} style={{width: 45, height: 45}} />
                <Text style={{fontSize: 12}}>{item.title}</Text>
            </View>
        )
    }
}

const styles = StyleSheet.create({
    box:{
        marginTop: 5,
    },
    box1:{
        width,
        // backgroundColor: 'pink',
        paddingBottom:5,
        paddingTop:5,
    },
    iconBox: {
        width: width / 5,
        justifyContent: 'center',
        alignItems: 'center',
        marginBottom:5,
    }
})

```



#### 9.3、小圆点的添加

最后给添加小圆点样式及其当前样式


事件函数中，可以通过  e.nativeEvent.contentOffset.x;   来获取事件源相对于父级的偏移量

具体代码：

```jsx
	constructor(props) {
        super(props)
  
        this.state = {
            curPage: 1    
        }
        this.handleMomentumScrollEnd = this.handleMomentumScrollEnd.bind(this)
    }

    handleMomentumScrollEnd(e){
        //获取滑动的偏移量
        let offSetX = e.nativeEvent.contentOffset.x;

        this.setState({
            curPage: offSetX==360?2:1
        })
    }

... ...

				</ScrollView>   
                <View style={styles.pointBox} >
                    <View style={this.state.curPage==1? styles.currentPoint : styles.point
                    }></View>
                     <View style={this.state.curPage==2? styles.currentPoint : styles.point
                    }></View>
                </View>

......

	pointBox:{
        height:10,
        flexDirection:"row",
        justifyContent: 'center',
        alignItems: 'center',
    },
    //小圆点默认样式
    point: {
        backgroundColor: '#ccc',
        width: 5,
        height: 5,
        borderRadius: 5,
        marginRight: 3
    },
    //当前的小圆点
    currentPoint: {
        backgroundColor: globalStyle.baseColor,
        width: 5,
        height: 5,
        borderRadius: 5,
        marginRight: 3
    },
```



# Day5

## 一、超值特惠基本布局

/app/food/目录中新建FoodSale.js：

```jsx
import React, { Component } from 'react'
import { View , StyleSheet, Text} from 'react-native'
import globalStyle from "../globalStyle"

export default class FoodSale extends Component {
    render() {
        return (
            
            <View style={styles.container}>
                <View style={styles.titleBox}>
                    <Text  style={styles.title}>超值特惠</Text>
                    <Text>更多特惠></Text>
                </View>
            </View>
        )
    }
    
}
const styles = StyleSheet.create({
    container:{
        marginTop:5,
        backgroundColor:"#fff",
        padding:6
    },
    titleBox:{
        flexDirection:"row",
        alignItems:"baseline",
        justifyContent:"space-between",
        marginBottom:5,
    },
    title:{
        fontSize:16,
        color:globalStyle.baseColor,
        fontWeight:"bold"
    }
})

```

Food.js中：

```jsx
import FoodSale from "./FoodSale"		
...		
			<View  style={styles.container}>
                <FoodTop />
                <FoodMenu />
                <FoodSale />
            </View>
```



## 二、超值特惠列表布局

FoodSale.js中

```jsx
			<View style={styles.container}>
    
                ... ...
    
                <View style={styles.listBox}>
                    {
                        Discounts.map((v,k)=>{
                            return (
                                <View style={styles.disBox} key={k}>
                                    <Image source={{uri:v.pic}} style={styles.img}/>
                                    <Text  style={styles.listBoxTitle}>{v.title}</Text>
                                    <View style={styles.priceBox}>
                                        <Text style={styles.vipPrice}>&yen;{v.vipPrice}</Text>
                                        <Text style={styles.salePrice}>&yen;{v.salePrice}</Text>
                                    </View>
                                </View>
                            )
                        })
                    }
                    

                </View>
            </View>

... ...
const styles = StyleSheet.create({
    
    ... ...
    
    listBox:{
      
        flexDirection:"row",
        justifyContent:"space-between",
        // backgroundColor:"pink",
    },
    img:{
        width:(width-12-12)/3,
        height:70
    },
    listBoxTitle:{
        fontSize:12
    },
    priceBox:{
        flexDirection:"row",
        alignItems:"baseline"
    },
    vipPrice:{
        color:globalStyle.baseColor,
        marginRight:3
    },
    salePrice:{
        fontSize:10,
        textDecorationLine:"line-through",
        paddingBottom:1
    }
})

```



## 三、周边美食布局

/app/food/目录中新建FoodPos.js：

```jsx
import React, { Component } from 'react'
import { View , StyleSheet, Text, Image} from 'react-native'

import globalStyle from "../globalStyle"  

export default class FoodPos extends Component {
    render() {
        return (
            <View style={styles.container}>
                <Text style={styles.title}>周边美食</Text>

                <View style={styles.list}>
                    <View style={styles.item}>
                        <Image source={{uri:"mrfish"}} style={{width:80,height:80}}/>
                        <View style={styles.itemRight}>
                            <Text style={styles.itemTitle}>天河店天河店</Text>
                            <View style={styles.scoreAndPrice}>
                                <Text style={styles.score}>评分：4.0</Text>
                                <Text style={styles.price}>&yen; 90</Text>
                            </View>
                            <Text style={styles.itemType}>中式菜；中式菜</Text>
                        </View>
                    </View>

                   
                </View>
            </View>
        )
    }
}
const styles = StyleSheet.create({
    container:{
        marginTop:5,
        backgroundColor:"#fff",
        padding:6
    },
    title:{
        color:"#333",
        fontSize:16,
        fontWeight:"bold"
    },
    item:{
        marginTop:8,
        marginBottom:8,
        flexDirection:"row"
    },
    scoreAndPrice:{
        marginTop:2,
        marginBottom:10,
        flexDirection:"row",
        justifyContent:"space-between"
    },
    itemRight:{
        flex:1,
        marginLeft:10
    },
    itemTitle:{
        color:"#333",
        fontWeight:"bold"
    },
    score:{
        color:"#999",
    },
    price:{
        fontSize:16,
        color:globalStyle.baseColor,
    },
    itemType:{
        color:"#ccc",
    }
})

```

Food.js中：

```jsx
import FoodPos from "./FoodPos"		
...		
			<View  style={styles.container}>
              	<ScrollView>
                	<FoodTop />
                	<FoodMenu />
                	<FoodSale />
                	<FoodPos />
              	</ScrollView>
            </View>
```



## 四、获取手机定位的经度纬度

H5的通过navigator.geolocation对象可以直接获取当前手机的定位，即手机所在地的经度和纬度

```js
navigator.geolocation.getCurrentPosition((pos)=> {
    var coords = pos.coords; //坐标对象
    // coords.longitude经度      coords.latitude  纬度
    alert(coords.longitude+","+ coords.latitude)
})
```

**！！！但是在使用之前需要先开启手机的定位权限：**

```xml
Android: 需要先让用户授权，获得访问GPS设备的权限 
在android/app/src/main/AndroidMainifest.xml新增
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```

修改权限后重新删除 /android/app下的build文件夹，再重新打包启动应用 react-native run-android



## 五、修改手机模拟器定位

手机模拟器需要手动修改定位！**修改之后重新启动这个功能才能生效，点两下上面的off和on按钮**

![1576184586050](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day05/assets/1576184586050.png)

但是，假设我们现在想要设置手机模拟器位置在  天河棠下乐天大厦 ，但是我们又不知道乐天大厦的经度和纬度，这就需要借助其他API来获取所在地的经纬度。在这里我们使用免费的高德API。



## 六、高德API的使用前准备

高德API官方网址：https://lbs.amap.com/api/



在项目中我们使用高德API的**web服务**。这就需要我们先注册账号，进入控制台创建应用，创建key。

先注册账号：https://lbs.amap.com/dev/id/choose  

注册后登录来到控制台，并创建应用

![1576183191113](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day05/assets/1576183191113.png)

创建应用后，为应用添加Key值：

![1576183435687](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day05/assets/1576183435687.png)



## 七、使用高德API获取指定地点的经纬度

现在我们使用高德API来获取指定地点的经纬度：

https://lbs.amap.com/api/webservice/guide/api/georegeo#geo

![1576185169246](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day05/assets/1576185169246.png)

然后把这个经纬度设置到手机模拟器上，使手机的定位就在我们指定的位置  天河棠下乐天大厦。

这样我们接下来就可以来实现手机所在 周边美食 数据的加载。（周边美食数据依旧使用高德API来获取）

## 八、使用高德API获取周边美食数据

高德API周边搜索网址：https://lbs.amap.com/api/webservice/guide/api/search#around

![1576185710479](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day05/assets/1576185710479.png)

把这个网址补充完整之后粘贴到地址栏上，就可以得到指定位置的周边美食数据了。

注意：把types参数去掉才能看到数据。

如下图：

![1576186070273](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day05/assets/1576186070273.png)

## 九、在项目中获取周边数据

项目录下安装axios： **yarn add axios@0.18.0**

```jsx
	constructor(props) {
        super(props)
    
        this.state = {
          pois: []      //周边信息数组
        }
      }
    
    componentDidMount(){
        
        navigator.geolocation.getCurrentPosition((pos)=> {
            var coords = pos.coords; //坐标对象
            // coords.longitude经度      coords.latitude  纬度
            // alert(coords.longitude+","+ coords.latitude)
            axios.get("https://restapi.amap.com/v3/place/around",{
                params:{
                    //https://restapi.amap.com/v3/place/around?key=b3a54cf1a0c414681fde360359eed5e3&location=113.377355,23.132797&keywords=%E7%BE%8E%E9%A3%9F&&radius=1000&offset=20&page=1&extensions=all
                    key:Key.gdKey,
                    location:coords.longitude+","+ coords.latitude,
                    keywords:"美食",
                    radius:10000,
                    offset:20,
                    page:1,
                    extensions:"all"
                }
            }).then((resp)=>{
                // alert(JSON.stringify(resp.data))
                this.setState({
                    pois: resp.data.pois     //周边信息数组
                })
            })
        })
    }
```

## 十、将周边数据渲染到页面上

```jsx
			<View style={styles.container}>
                <Text style={styles.title}>周边美食</Text>

                <View style={styles.list}>
                    {
                        this.state.pois.map((v,k)=>{
                            return(
                                <View style={styles.item}>
                                    <Image source={{uri: v.photos.length == 0 ? 'img404' : v.photos[0].url}} style={{width:80,height:80}}/>
                                    <View style={styles.itemRight}>
                                        <Text style={styles.itemTitle}>{v.name}</Text>
                                        <View style={styles.scoreAndPrice}>
                                            <Text style={styles.score}>评分：{v.biz_ext.rating}</Text>
                                            <Text style={styles.price}>&yen; {v.biz_ext.cost}</Text>
                                        </View>
                                        <Text style={styles.itemType}>{v.type}</Text>
                                    </View>
                                </View>    
                            )
                        })
                    }
                </View>
            </View>
```

# Day6

## 一、自动轮播的定时器书写

在day03的学习中，我们使用ScrollView书写了手动滑屏切换图片的效果，这一节我们加上定时器添加轮播效果

```jsx
// 自动轮播的实现
import React, { Component } from 'react'
import {View, StyleSheet, Image, Text, ScrollView} from 'react-native'

export default class App5 extends Component {

    componentDidMount(){
        let sv = this.refs.scrollView
        
        let currentPage = 0

        setInterval(()=>{
            currentPage++;

            if(currentPage==3){
                currentPage=0    
            }

            sv.scrollTo({
                x: currentPage*360, //这个值是已经滚动的值
                y: 0, 
                animated: true
            })
        },1000)
        
    }
   
    render() {
        return (
            <View style={styles.banner}>
                <ScrollView ref="scrollView" horizontal={true} pagingEnabled={true} showsHorizontalScrollIndicator={false}>
                    <View style={styles.itemBox}>
                        <Image source={require('../../res/banner1.png')} style={{width:360,height:201}}></Image>
                        <View style={styles.titleBox}>
                            <Text  style={styles.titleTxt}>前端让IT互联有魅力</Text>
                        </View>
                    </View>
                    <View style={styles.itemBox}>
                        <Image source={require('../../res/banner2.png')} style={{width:360,height:201}}></Image>
                        <View style={styles.titleBox}>
                            <Text style={styles.titleTxt}>Java薪未来</Text>
                        </View>
                    </View>
                    <View style={styles.itemBox}>
                        <Image source={require('../../res/banner3.png')} style={{width:360,height:201}}></Image>
                        <View style={styles.titleBox}>
                            <Text style={styles.titleTxt}>全栈UI设计</Text>
                        </View>
                    </View>
                </ScrollView>
            </View>
        )
    }
}
const styles = StyleSheet.create({
    banner:{
        width:360
    },
    itemBox:{
        width:360
    },
    titleBox:{
        position:"absolute",
        bottom:0,
        backgroundColor:"rgba(0, 0, 0, 0.3)",
        height:30,
        width:360
    },
    titleTxt:{
        color:"#fff",
        lineHeight:30,
        marginLeft:10
    }
    
})

```

以下提供无缝写法(了解下即可)

```js
componentDidMount(){
    let sv = this.refs.scrollView
    let currentPage = 00

    setInterval(()=>{
        currentPage++;

        if(currentPage==4){  //第4张可以被看见，所以3可以取，到第5张要瞬间切换到第1张，并跳转到第2张
            currentPage=1      //决定下一次跳转到那一张
            sv.scrollTo({    //瞬间切换到第1张
                x: 0, 
                y: 0, 
                animated: false
            })
        }

        sv.scrollTo({
            x: currentPage*360, //这个值是已经滚动的值
            y: 0, 
            animated: true
        })
    },1000)
}
```



## 二、使用react-native-swiper实现轮播图 

react-native-swiper是专门用来实现轮播图的模块

```
安装：npm i react-native-swiper --save
查看：npm view react-native-swiper
删除：npm rm react-native-swiper --save
```



swiper的一些属性：

![1581376261185](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day06/assets/1581376261185.png)

![1581376307065](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day06/assets/1581376307065.png)

![1581376356749](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day06/assets/1581376356749.png)

![1581376402947](/Users/mxshang/Desktop/React Native移动跨平台开发从零基础入门到项目实战-6天-资料/day06/assets/1581376402947.png)

#### 2.1、基本使用的代码

```jsx
// react-native-swiper组件的使用,轮播图
import React, { Component } from 'react'
import {
    StyleSheet,
    Text,
    View,
    Image,
    Dimensions
  } from 'react-native';
  import Swiper from 'react-native-swiper';
  const {width} = Dimensions.get('window'); 
  export default class App extends Component{
    render() {
      return (
          <View style={styles.container}>
              {/*设置horizontal为竖向排列 autoplay为自动播放*/}
               <Swiper style={styles.wrapper} horizontal={true} autoplay autoplayTimeout={1} >
                    <View style={styles.slide1}>
                        <Text style={styles.text}>Hello Swiper</Text>
                    </View>
                  <View style={styles.slide2}>
                      <Text style={styles.text}>Beautiful</Text>
                  </View>
                  <View style={styles.slide3}>
                      <Text style={styles.text}>And simple</Text>
                  </View>
              </Swiper>
          </View>
      );
    }
  }

  const styles = StyleSheet.create({
    container: {
        height:200
    },

    wrapper: {
    },

    slide: {
        flex: 1,
        justifyContent: 'center',
        backgroundColor: 'transparent'
    },

    slide1: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#9DD6EB'
    },
    slide2: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#fcc'
    },
    slide3: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#cff'
    },
    text: {
        color: '#fff',
        fontSize: 30,
        fontWeight: 'bold'
    }
});
```

#### 2.2、使用Swiper完成上节的轮播

```jsx
import React, { Component } from 'react'
import {
    StyleSheet,
    Text,
    View,
    Image,
    Dimensions
  } from 'react-native';
  import Swiper from 'react-native-swiper';
  const {width} = Dimensions.get('window'); 
  export default class App extends Component{
    render() {
      return (
          <View style={styles.container}>
              <Swiper style={styles.wrapper}  autoplay
                      dot={<View style={{backgroundColor:'#ccc', width: 8, height: 8,borderRadius: 4, marginLeft: 3, marginRight: 3, marginTop: 3, marginBottom: 3,}} />}
                      activeDot={<View style={{backgroundColor: 'yellow', width: 8, height: 8, borderRadius: 4, marginLeft: 3, marginRight: 3, marginTop: 3, marginBottom: 3}} />}
                      paginationStyle={{
                          bottom: 5, left: null, right: 10
                      }}
  
                      loop>
                  <View style={styles.slide} >
                      
                      <Image resizeMode='stretch' style={styles.image} source={require('../../res/banner1.png')} />
                      <View style={styles.titleBox}>
                            <Text  style={styles.titleTxt}>前端让IT互联有魅力</Text>
                        </View>
                  </View>
                  <View style={styles.slide}>
                      
                      <Image resizeMode='stretch' style={styles.image} source={require('../../res/banner2.png')} />
                      <View style={styles.titleBox}>
                            <Text  style={styles.titleTxt}>前端让IT互联有魅力</Text>
                        </View>
                  </View>
                  <View style={styles.slide} >
                      
                      <Image resizeMode='stretch' style={styles.image} source={require('../../res/banner3.png')} />
                      <View style={styles.titleBox}>
                            <Text  style={styles.titleTxt}>前端让IT互联有魅力</Text>
                        </View>
                  </View>
                  
              </Swiper>
          </View>
  
      );
    }
  }

  const styles = StyleSheet.create({
    container: {
        height:201
    },
    slide: {
        flex: 1,
        justifyContent: 'center',
        backgroundColor: 'transparent'
    },

    slide1: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#9DD6EB'
    },
    slide2: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#fcc'
    },
    slide3: {
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
        backgroundColor: '#cff'
    },
    text: {
        color: '#fff',
        fontSize: 30,
        fontWeight: 'bold'
    },

    image: {
        width:width,
        height:201,
    },
    titleBox:{
        position:"absolute",
        bottom:0,
        backgroundColor:"rgba(0, 0, 0, 0.3)",
        height:30,
        width:360
    },
    titleTxt:{
        color:"#fff",
        lineHeight:30,
        marginLeft:10
    }
});
```





## 三、StackNavigator 组件的使用

前面我们在实现项目底部导航栏的时候，使用的是ReactNavigation的TabNavigator 组件。

而ReactNavigation还有其他两个核心组件：StackNavigator 和 DrawerNavigator 

React Navigation官网：https://www.reactnavigation.org.cn/

StackNavigator 的使用：<https://www.reactnavigation.org.cn/docs/stacknavigator> 

我们可以使用StackNavigator 实现界面的转场

#### 3.1、StackNavigator 基本使用

先定义视图所对应的组件：

```js
import {StackNavigator} from 'react-navigation'
export default ModalStack = StackNavigator({
    Home: {
      screen: Home,   //对应组件
    },
    Page1: {
      screen: Page1,  //对应组件
    },
  },{
    headerMode:"none"  //隐藏顶部的导航栏
});
```

然后使用以下onPress事件来实现转场效果:

```js
onPress={() => this.props.navigation.navigate('Page1')}
```

具体代码：

Home1.js中：

```jsx
import React, { Component } from 'react'
import {
    Text,
    View,
  } from 'react-native';
import {StackNavigator} from 'react-navigation'

import Page1 from "./navigators/Page1"

class Home extends Component {
    render() {
      return (
          <View>
            <Text onPress={() => this.props.navigation.navigate('Page1')}>跳转到Page1</Text>
          </View>
        
      );
    }
  }
  
export default ModalStack = StackNavigator({
    Home: {
      screen: Home,   //对应组件
    },
    Page1: {
      screen: Page1,  //对应组件
    },
  },{
    headerMode:"none"  //隐藏顶部的导航栏
});
```

Page1.js中：

```jsx
import React, { Component } from 'react'
import {
    Text,
    View,
  } from 'react-native';

// import {navigation} from 'react-navigation'
export default class Page1 extends Component {
    render() {
        return (
            <View>
                <Text>欢迎来到page1</Text>
            </View>
        )
    }
}
```

#### 3.2、StackNavigator 携带参数的跳转

在onPress事件中this.props.navigation.navigate('Page1')，再传入一个对象作为传递参数

```js
onPress={() => this.props.navigation.navigate('Page2', {name: 'wolfcode'})}
```

定义对应关系的时候书写path属性：

```js
Page2: {
	path: 'page2/:name',
	screen: Page2,
},
```

接收参数：

```jsx
const {navigation} = this.props
return (
	<Text>{navigation.state.params.name}</Text>
)
```

返回上一页：

```jsx
<Text onPress={()=>{
   	navigation.goBack()
}}>返回到上一页</Text>
```



Home2.js中

```jsx
import React, { Component } from 'react'
import {
    Text,
    View,
  } from 'react-native';
import {StackNavigator} from 'react-navigation'

import Page2 from "./navigators/Page2"
class Home extends Component {
    render() {
        return (
            <View>
                <Text onPress={() => this.props.navigation.navigate('Page2', {name: 'wolfcode'})}>
                    跳转到Page2
                </Text>
            </View>
        
        );
    }
  }
  
export default ModalStack = StackNavigator({
    Home: {
      screen: Home,
    },
    Page2: {
      path: 'page2/:name',
      screen: Page2,
    },
  },{
    headerMode:"none"  //隐藏顶部的导航栏
});
```

Page2中：

```jsx
import React, { Component } from 'react'
import {
    Text,
    View,
  } from 'react-native';

export default class Page2 extends Component {
    render() {
        const {navigation} = this.props
        return (
            <View>
                <Text>这是page2,接收到参数为：</Text>
                <Text>{navigation.state.params.name}</Text>
                <Text onPress={()=>{
                    navigation.goBack()
                }}>返回到上一页</Text>
            </View>
        )
    }
}
```

#### 3.3、StackNavigator 一些样式的配置

 StackNavigator() 的第二个参数可以设置全局的样式

```jsx
export default ModalStack = StackNavigator({
    Home: {
      screen: Home,
      navigationOptions:{   //对单个页面进行配置
          title:"首页",
      }
    },
    Page1: {
      screen: Page1,
      navigationOptions:{
        // header:null   //设置page1不需要标题
        title:"Page1标题",
        // headerStyle:{
        //     height:40
        // }
    }
    },
  },{    //全局配置
    navigationOptions:{
      headerStyle:{//头部样式
          height:40
      }, 
      headerTitleStyle:{//头部标题文字样式
          backgroundColor:"#f40",
          fontSize:14,   
          color:"blue",   
          textAlign:"center",
      },
    }
  }
);
```

## 四、DrawerNavigator组件

DrawerNavigator组件是ReactNavigation第三个核心组件

React Navigation官网：https://www.reactnavigation.org.cn/

DrawerNavigator的使用：<https://www.reactnavigation.org.cn/docs/drawernavigator>  

DrawerNavigator组件可以用来制作抽屉类型的导航，也可以用来制作自定义内容的抽屉。

#### 4.1、DrawerNavigator的基本使用(打开抽屉) 

点击函数中通过：this.props.navigation.openDrawer() 打开抽屉

```jsx
import React, { Component } from 'react'
import {
    Button,
  } from 'react-native';
import {DrawerNavigator} from 'react-navigation'

class MyHome extends Component {


    // navigation.openDrawer()  打开抽屉
    render() {
        return (
            <Button
                onPress={() => this.props.navigation.openDrawer()}
                title="点我打开抽屉"
            />
        );
    }
}

export default MyApp = DrawerNavigator({

    //这里定义的页面就会出现在抽屉当中
    Home: {
      screen: MyHome,
    },
    
});
```

#### 4.2、DrawerNavigator核心用法 

DrawerNavigator本身使用来做抽屉导航，通过点击抽屉中某一项切换到另外一个页面中

```jsx
import React, { Component } from 'react'
import {
    Text,
    View,
    Button,
  } from 'react-native';
import {DrawerNavigator} from 'react-navigation'

class MyHome extends Component {


    // navigation.openDrawer()
    render() {
        return (
            <Button
                onPress={() => this.props.navigation.openDrawer()}
                title="点我打开抽屉"
            />
        );
    }
}
  
class Page1 extends Component {
  
    render() {
        return (
            <View>
                <Text>Page1</Text>
                <Button onPress={() => this.props.navigation.goBack()} title="点我返回"></Button>
            </View>
            
        );
    }
}

export default MyApp = DrawerNavigator({

    //这里定义的页面就会出现在抽屉当中
    Home: {
      screen: MyHome,
    },
    P1: {
      screen: Page1,
    },
});
```

#### 4.3、DrawerNavigator一些配置，以及自定义抽屉内容

```jsx
import React, { Component } from 'react'
import {
    Text,
    View,
    Button,
    ScrollView,
  } from 'react-native';
import {DrawerNavigator, DrawerItems, SafeAreaView} from 'react-navigation'

class MyHome extends Component {


    // navigation.openDrawer()
    render() {
        return (
            <Button
                onPress={() => this.props.navigation.openDrawer()}
                title="点我打开抽屉"
            />
        );
    }
}
  
class Page1 extends Component {
  
    render() {
        return (
            <View>
                <Text>Page1</Text>
                <Button onPress={() => this.props.navigation.goBack()} title="点我返回"></Button>
            </View>
            
        );
    }
}

export default MyApp = DrawerNavigator({

    //这里定义的页面就会出现在抽屉当中
    Home: {
      screen: MyHome,
    },
    P1: {
      screen: Page1,
    //   navigationOptions:{
    //     title:"P1页面"
    //   }
    },
  },{
    drawerWidth:200,    //设置抽屉的宽度
    drawerPosition:"right",   //设置抽屉的方向
    
    // 以下contentComponent属性可以自定义抽屉内容
    contentComponent:(props) => (
        <ScrollView style={{backgroundColor:'#ccc',flex:1}}>
            <SafeAreaView forceInset={{ top: 'always', horizontal: 'never' }}>
                <DrawerItems {...props} />
            </SafeAreaView>
            {/* <Text>设置其他组件</Text> */}
        </ScrollView>
    )
  });
```

#### 4.4、从自定义抽屉中传递参数到页面 

```jsx
// 从自定义抽屉中传递参数到页面
import React, { Component } from 'react'
import {
    Text,
    View,
    Button,
    ScrollView
  } from 'react-native';
import {DrawerNavigator} from 'react-navigation'

class MyHome extends Component {


    // navigation.openDrawer()
    render() {
        return (
            <Button
                onPress={() => this.props.navigation.openDrawer()}
                title="点我打开抽屉"
            />
        );
    }
}
  
class Page1 extends Component {
  
    render() {
        return (
            <View>
                <Text>Page1</Text>
                {/* 接收从抽屉中传来的参数name */}
                <Text>{this.props.navigation.state.params.name}</Text> 
                <Button onPress={() => this.props.navigation.goBack()} title="点我返回"></Button>
            </View>
            
        );
    }
}

export default MyApp = DrawerNavigator({

    //这里定义的页面就会出现在抽屉当中
    Home: {
        screen: MyHome,
    },
    P1: {
        screen: Page1,
    },
},{
    contentComponent:(props) => (
        <ScrollView style={{backgroundColor:'#ccc',flex:1}}>
            
            {/* 在抽屉中点击按钮返回 P1几面，并传递了参数*/}
            <Button
                onPress={() => props.navigation.navigate("P1",{name:"wolfcode"})}
                title="点我回到P1"
            />
        </ScrollView>
    )
});
```

## 五、使用FlatList组件实现下拉刷新

步骤：

1、准备isLoading变量和数据源

```js
const CITY_NAMES = ["北京市","上海市","深圳市","广州市","成都","杭州"]

... ...
constructor(props){
    super(props)

    this.state = {
        isLoading:false,
        dataArr: CITY_NAMES
    }
}
```

2、书写FlatList组件

```jsx
<FlatList 
    data = {this.state.dataArr}
    renderItem = {this.renderItem}

    refreshing={this.state.isLoading}  //  是否正在加载数据
    onRefresh = {this.loadData.bind(this)} //  刷新的时候执行这个方法
/>
```

3、刷新时候执行loadData函数

```js
loadData(){
    this.setState({
        isLoading:true,
    })

    //模拟异步请求
    setTimeout(()=>{
        let data = CITY_NAMES.reverse()  //把数组反转，模拟新数据的获取
        this.setState({
            isLoading:false,
            dataArr: data
        })

    },500)
}
```



完整代码如下：

```jsx
// 下拉刷新
import React, { Component } from 'react'
import {
    Text,
    View,
    FlatList,
    StyleSheet
  } from 'react-native';

const CITY_NAMES = ["北京市","上海市","深圳市","广州市","成都","杭州"]

export default class App9 extends Component {

    //1 准备isLoading和数据源
    constructor(props){
        super(props)

        this.state = {
            isLoading:false,
            dataArr: CITY_NAMES
        }
    }

    renderItem({item}){
        return(
            <View style={styles.itemBox}>
                <Text style={styles.itemBoxTxt}>{item}</Text>
            </View>
        )
    }

    //3 修改数据源
    loadData(){
        this.setState({
            isLoading:true,
        })

        //模拟异步请求
        setTimeout(()=>{
            let data = CITY_NAMES.reverse()  //把数组反转，模拟新数据的获取
            this.setState({
                isLoading:false,
                dataArr: data
            })
            
        },500)
    }
    render() {
        return (
            <View>
                <FlatList 
                    data = {this.state.dataArr}
                    renderItem = {this.renderItem}
                    
                    refreshing={this.state.isLoading}  //2 是否正在加载数据
                    onRefresh = {this.loadData.bind(this)} //2  刷新的时候执行这个方法
                />
            </View>
        )
    }
}

const styles = StyleSheet.create({
    itemBox:{
        width:320,
        height:200,
        backgroundColor:"#ccc",
        marginLeft:20,
        marginBottom:20
    },
    itemBoxTxt:{
        textAlign:"center",
        lineHeight:200
    }
})
```

## 六、使用FlatList组件实现滑动到底部加载更多 (上拉加载更多)

步骤

1、FlatList组件的使用

```jsx
<FlatList 
    data = {this.state.dataArr}
    renderItem = {this.renderItem}

    ListFooterComponent={this.genIndicator}  //一、定义尾部组件，用来书写加载的符号
    onEndReached={this.loadData.bind(this)} //三、到达底部调用加载数据的函数
/>
```

2、书写加载符号

```jsx
import {  ... ...，
    ActivityIndicator
} from 'react-native';

genIndicator(){ //二、书写加载的符号
    return <View>
        <ActivityIndicator 
            size="large"
            animating={true}
            color="red"
            />
        <Text style={{ textAlign:"center", flex:1, marginBottom:10}}>正在加载数据...</Text>
    </View>
}
```

3、修改数据源

```js
//四 修改数据源
loadData(){
    this.setState({
        isLoading:true,
    })

    //模拟异步请求
    setTimeout(()=>{
        let data = this.state.dataArr.concat(CITY_NAMES)  //合并数组，模拟加载新数据
        this.setState({
            isLoading:false,
            dataArr: data
        })

    },2000)
}
```

## 七、AsyncStorage的使用

AsyncStorage是一个简单的、异步的、持久化的 Key-Value 存储系统，它对于 App 来说是全局性的。可用来代替 LocalStorage。 

AsyncStorage也是React Native官方推荐的数据存储方式，旨在代替LocalStorage 。

Android下，AsyncStorage会将数据存储在RocksDB或者SQLite中，具体存在RocksDB中还是SQLite中这取决于设备支持哪一种存储方式。 

IOS下，如果存储的内容较小，那么AsyncStorage会将存储的内容放在一个序列化的字典中，如果存储的内容较大，那么AsyncStorage会将存储的内容放在一个单独的文件中。



三个主要的方法：

```js
AsyncStorage.setItem(键名,值,回调函数)    //保存数据
AsyncStorage.getItem(键名,回调函数)    //获取数据
AsyncStorage.removeItem(键名,回调函数)    //删除数据
```

具体代码：

```jsx
// AsyncStorage的使用
import React, { Component } from 'react'
import {
    View,
    TextInput,
    Button,
    AsyncStorage
  } from 'react-native';

export default class App11 extends Component {

    constructor(props){
        super(props)

        this.state = {
            val:""
        }
    }
    onSet(){
        AsyncStorage.setItem("Key",this.state.val,(error)=>{
            if(!error){
                alert("保存成功！")
            }else{
                alert("保存失败！")
            }
        })
    }

    onGet(){
        AsyncStorage.getItem("Key",(error,ret)=>{
            if(!error){
                alert("获取成功！Key的值为："+ret)
            }else{
                alert("获取失败！")
            }
        })
    }

    onRemove(){
        AsyncStorage.removeItem("Key",(error,ret)=>{
            if(!error){
                alert("删除成功！")
            }else{
                alert("删除失败！")
            }
        })
    }

    handleChange(text){
        this.setState({
            val:text
        })
    }
    render() {
        return (
            <View>
                <TextInput placeholder="请输入"  onChangeText={this.handleChange.bind(this)}/>

                <Button title="设置" onPress={this.onSet.bind(this)}/>
                <Button title="获取" onPress={this.onGet} />
                <Button title="删除" onPress={this.onRemove} />
            </View>
        )
    }
}

```





