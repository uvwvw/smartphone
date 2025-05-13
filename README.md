23年卷子

## 问题1：为什么人们更多使用移动网页的原因
**答案：(D) 所有选项**

**知识点详解：**
移动网页与原生应用的优势比较是移动开发中的重要概念。人们更多使用移动网页的原因包括：
- **易用性**：移动网页无需安装，直接通过浏览器访问，减少了用户的使用门槛
- **加载速度**：在某些情况下，轻量级的移动网页比功能复杂的应用加载更快，特别是对于不常用的服务
- **存储空间限制**：很多用户设备存储空间有限，不愿安装过多应用占用空间
- **经济因素**：许多用户不愿为应用付费，而网页版通常免费访问

移动网页与原生应用的选择是开发者需要权衡的重要决策，需要考虑用户习惯、功能需求和开发资源。

## 问题2：5G网络下载速度计算
**答案：(B) 0.296 sec**

**知识点详解：**
这道题考察网络速度计算的基本知识：
- 应用大小：37 MB (兆字节)
- 网络速度：1 Gbps (千兆比特/秒)
- 计算过程：
  1. 将MB转换为Mb：37 MB = 37 × 8 Mb = 296 Mb (1字节=8比特)
  2. 在1 Gbps = 1000 Mbps的网速下计算时间：
     时间 = 296 Mb ÷ 1000 Mbps = 0.296 秒

这体现了5G网络的高速特性，对于普通大小的应用能实现亚秒级下载速度。

## 问题3：关于Android的正确描述
**答案：(B) i) 和 iv) 只**

**知识点详解：**
Android系统架构是移动开发的基础知识：
- i) ✓ 应用框架层(Application Framework)确实允许开发者替换预构建组件，这是Android架构的灵活性体现
- ii) ✗ 在Android 4.4 KitKat中，Dalvik并没有被完全替换为ART，而是提供了ART作为可选运行时环境。直到Android 5.0 Lollipop才完全替换
- iii) ✗ ART不直接编译和运行.apk文件，而是处理其中的字节码
- iv) ✓ ART确实引入了预先编译(AOT)技术，这是相对Dalvik即时编译(JIT)的重要改进

Android运行时环境的演变反映了性能优化的不断发展，从JIT到AOT再到混合编译模式。

## 问题4：AndroidManifest.xml包含的信息
**答案：(D) 所有选项**

**知识点详解：**
AndroidManifest.xml是Android应用的核心配置文件，包含以下关键信息：
1. **活动和服务声明**：定义应用中的所有Activity和Service组件
2. **权限需求**：列出应用需要的系统权限，如网络访问、相机使用等
3. **SDK版本信息**：指定最低SDK版本(minSdkVersion)和目标SDK版本(targetSdkVersion)
4. **屏幕支持**：定义应用支持的屏幕尺寸和分辨率

这个文件对Android应用的安全性、兼容性和功能定义至关重要，是应用与系统交互的桥梁。

## 问题5：Monkey测试工具的正确描述
**答案：(C) ii) 和 iv) 只**

**知识点详解：**
Monkey是Android系统的重要测试工具：
- i) ✗ Monkey主要用于压力测试，不专门用于渗透测试
- ii) ✓ Monkey可以在模拟器和真实设备上运行，提供灵活的测试环境
- iii) ✗ Monkey是Android特有的工具，不能测试iOS应用
- iv) ✓ Monkey可以测试文本和图形输入，能模拟用户的各种交互行为

Monkey测试能通过生成伪随机事件流来发现应用在极端条件下的稳定性问题，是Android应用质量保证的重要工具。

## 问题6：关于iOS的正确描述
**答案：(A) i) 和 iii) 只**

**知识点详解：**
iOS开发生态的关键特点：
- i) ✓ 小型企业计划(Small Business Program)确实是开发者获取85%收益，苹果获取15%
- ii) ✗ 家庭共享(Family Sharing)最多允许6个人共享购买内容，而非10个人
- iii) ✓ Xcode开发环境确实只能在macOS平台上运行，这是开发iOS应用的硬性要求
- iv) ✗ SwiftUI支持iOS 13+和Xcode 11+，而非题目所述的iOS 12+和Xcode 10+

这些特点体现了Apple对生态系统的严格控制，以及对开发工具链和技术栈的管理策略。

## 问题7：Swift中可选整型变量声明
**答案：(A) var x : Int?**

**知识点详解：**
Swift的可选类型(Optional)是该语言的特色功能：
- `var x : Int?`：正确的可选整型变量声明，表示x可以是整数或nil
- `let x: Int?`：技术上也是正确的可选整型常量声明，但题目明确要求变量
- `var x: Int!`：这是隐式解包的可选类型，不是标准可选类型
- 可选类型是Swift类型安全的重要机制，帮助开发者明确处理可能为空的值

可选类型的使用能有效防止空指针异常，提高代码的健壮性。

## 问题8：Swift中可能失败的强制类型转换标识
**答案：(B) as!**

**知识点详解：**
Swift中类型转换的不同操作符：
- `as`：用于安全的向上转换(upcasting)或类型桥接，不会失败
- `as!`：强制向下转换(downcasting)，如果转换失败会导致运行时错误
- `as?`：条件向下转换，转换失败会返回nil而不是崩溃
- Swift中没有`cast`或`cast!`关键字

类型转换是Swift类型系统的重要组成部分，尤其在处理继承关系和协议遵循时非常关键。

## 问题9：Xcode Storyboard中添加新页面的方法
**答案：(C) View Controller**

**知识点详解：**
在Xcode Storyboard界面设计中：
- 添加新页面需要从组件库中拖拽**View Controller**到故事板
- **Navigation Controller**用于页面导航管理，不是单独页面
- **Page Controller**用于管理多个页面间的滑动切换
- Xcode没有"Scene Controller"这一标准组件

理解故事板和视图控制器的关系是iOS界面设计的基础知识点。

## 问题10：Xcode SwiftUI中包含UI定义和编程逻辑的文件
**答案：(B) ContentView**

**知识点详解：**
SwiftUI项目结构的核心文件：
- **ContentView.swift**：包含应用的UI定义和相关逻辑
- **\<ProjectName\>App.swift**：包含应用入口点和生命周期管理
- **ViewController**是UIKit中的概念，在SwiftUI项目中不存在
- **Assets**主要包含图片、颜色等资源，不包含UI定义或逻辑

SwiftUI采用声明式UI设计范式，将界面元素和业务逻辑整合在同一个文件中，区别于传统MVC模式。

## 第二部分：Android十进制到二进制转换器应用

### (a) match_parent和wrap_content的含义
**知识点讲解：**
- **match_parent**：视图将填充父容器允许的最大空间，即与父容器一样大
- **wrap_content**：视图将只占据足够容纳其内容的空间，根据内容自适应大小
这两个属性是Android布局中最基本的尺寸设置方式，影响UI的灵活性和适应性。

### (b) 应用布局
应用是一个垂直线性布局(LinearLayout)，包含：
- "Decimal:"标签(TextView)
- 十进制输入框(EditText)
- "Binary:"标签(TextView)
- 二进制结果显示区(TextView)
- "Convert"按钮(Button)

### (c) MainActivity.java中的缺失部分
```java
(A) AppCompatActivity
(B) R.layout.activity_main
(C) R.id.decimalNumber
(D) R.id.binaryNumber
(E) R.id.convert
(F) new converter()
```

**知识点讲解：**
- AppCompatActivity是支持库中的活动基类，提供较新特性的向后兼容
- R.layout引用XML布局资源，R.id引用视图ID
- setOnClickListener设置点击事件监听器，使按钮可以响应点击

### (d) onClick方法实现
```java
@Override
public void onClick(View view) {
    try {
        // 获取输入文本并转换为整数
        String decimalStr = decimalNumber.getText().toString();
        int decimal = Integer.parseInt(decimalStr);
        
        // 将十进制转换为二进制字符串
        String binary = Integer.toBinaryString(decimal);
        
        // 显示结果
        binaryNumber.setText(binary);
    } catch (NumberFormatException e) {
        // 处理无效输入
        binaryNumber.setText("无效输入");
    }
}
```

**知识点讲解：**
- 输入验证与异常处理是应用健壮性的关键
- Integer.toBinaryString()是Java中将整数转换为二进制字符串的便捷方法
- setText()方法用于更新UI显示内容

## 第三部分：Android UI控制规则与网络编程

### (a) 移动应用UI控制的两个规则
**规则1：不要阻塞UI线程**
**规则2：只能从UI线程更新UI**

**知识点讲解：**
- 规则1确保应用始终响应用户输入，防止"应用无响应"(ANR)对话框
- 规则2防止并发更新UI导致的不一致状态，所有UI更新必须在主线程执行
- 这两条规则看似矛盾但实际互补，需要结合异步编程模式（如AsyncTask、Thread+Handler等）

### (b) 图片下载代码分析
**结论：图片无法正确显示**

**知识点讲解：**
代码尝试在UI线程上直接执行网络操作（下载图片），这违反了第一条UI规则。网络操作是耗时操作，应在后台线程执行，然后使用Handler或post方法将结果传回UI线程更新界面。正确做法应使用AsyncTask、Retrofit或其他异步网络库。

### (c) Thread和Handler的关键区别
**知识点讲解：**
- **Thread**：代表独立的执行路径，可并行运行，但不能直接更新UI
- **Handler**：消息处理机制，关联某个线程的MessageQueue，负责线程间通信，特别是非UI线程向UI线程发送更新请求
- 两者结合使用是Android异步编程的基础模式

### (d) JSON处理结果
```
Temp1 = "2023"
Temp2 = "Priscilla"
Temp3 = "Ellen"
Temp4 = "Sonia"
Array1 = ["Chow Chow", "Ming Ming", "Ben Sir"]
```

**知识点讲解：**
- JSON是移动应用中常用的数据交换格式
- getString获取JSON对象的字符串值
- JSONArray需要使用索引遍历获取内容
- as操作符用于类型转换

### (e) 网络应用通常需要的权限
```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

**知识点讲解：**
- INTERNET权限允许应用访问网络
- ACCESS_NETWORK_STATE权限允许应用检查网络连接状态
- Android权限系统是保障用户隐私和安全的关键机制

## 第四部分：iOS数独应用开发

### (a) 缺失部分
```swift
(A) UIViewController
(B) UITextField
(C) UILabel
(D) @IBAction
(E) viewDidLoad
```

**知识点讲解：**
- UIViewController是iOS中视图控制器的基类
- UITextField用于文本输入，UILabel用于文本显示
- @IBAction用于将方法与界面元素动作连接
- viewDidLoad是视图控制器生命周期方法，在视图加载后调用

### (b) check()函数实现
```swift
func check() {
    // 尝试将文本转换为整数，如果失败则提示错误
    guard let val00 = Int(cell00.text ?? ""), 
          let val01 = Int(cell01.text ?? ""), 
          let val02 = Int(cell02.text ?? ""),
          let val10 = Int(cell10.text ?? ""), 
          let val11 = Int(cell11.text ?? ""), 
          let val12 = Int(cell12.text ?? ""),
          let val20 = Int(cell20.text ?? ""), 
          let val21 = Int(cell21.text ?? ""), 
          let val22 = Int(cell22.text ?? "") else {
        result.text = "Wrong! Invalid input"
        return
    }
    
    // 计算每行总和
    let row0Sum = val00 + val01 + val02
    let row1Sum = val10 + val11 + val12
    let row2Sum = val20 + val21 + val22
    
    // 计算每列总和
    let col0Sum = val00 + val10 + val20
    let col1Sum = val01 + val11 + val21
    let col2Sum = val02 + val12 + val22
    
    // 检查是否所有总和相等
    if row0Sum == row1Sum && row1Sum == row2Sum && 
       col0Sum == col1Sum && col1Sum == col2Sum && 
       row0Sum == col0Sum {
        result.text = "Correct! Sum = \(row0Sum)"
    } else {
        result.text = "Wrong!"
    }
}
```

**知识点讲解：**
- Swift的guard语句用于早期验证和安全解包
- 可选类型(??)处理缺失值的方式
- 字符串插值(\())用于组合文本和变量
- 多重条件判断确保数独规则得到满足

### (c) 连接UI组件与ViewController的方法
**知识点讲解：**
在Xcode中，连接UI组件和代码有几种方式：
1. 按住Control键从UI元素拖动到代码中（创建Outlet或Action）
2. 使用Interface Builder的连接检查器面板
3. 右键点击UI元素并拖动到代码中相应位置

### (d) weak关键字的含义
**知识点讲解：**
weak是引用类型修饰符，表示弱引用，不会增加对象的引用计数。它帮助避免循环引用（内存泄漏），允许ARC（自动引用计数）在没有强引用时释放对象。在UI元素引用中使用weak特别重要，因为视图控制器已经持有这些元素的强引用。

### (e) SwiftUI vs Storyboard
**优势**：
- SwiftUI使用声明式语法，使UI开发更直观且易于理解
- 提供实时预览功能，无需编译运行就能看到UI变化

**劣势**：
- 对旧iOS版本兼容性有限（需要iOS 13+）
- 相对较新，某些复杂功能可能仍需结合UIKit使用

## 第五部分：Swift函数定义与开发环境

### (a) Swift函数定义中的参数标签和参数名
**知识点讲解：**
- **参数标签**：在调用函数时使用，出现在函数调用中
- **参数名**：在函数实现中使用，出现在函数体内
这种设计使Swift函数调用更具可读性，同时保持函数体内代码的简洁性。

### (b) 函数调用示例
(i) `Sum(num1: 75, num2: 6)`
(ii) `Sum(num1: 75, and: 6)`
(iii) `Sum(75, 6)`

**知识点讲解：**
Swift函数调用必须遵循函数定义中的参数标签规范：
- 标准形式使用标签：参数值
- 使用_可省略参数标签
- 参数标签和参数名可以不同（如例ii中的num1 n1）

### (c) 设置默认参数值
```swift
func Sum(num1: Int32, num2: Int32 = 0) -> Int32 { ... }
```

**知识点讲解：**
Swift通过在参数类型后加上赋值表达式来设置默认参数值，这使得函数调用更灵活，对于经常使用特定值的参数特别有用。

### (d) 官方渠道下载Xcode的两个理由
**知识点讲解：**
1. **安全性**：官方下载经过苹果验证和签名，最小化恶意软件风险
2. **自动更新**：App Store提供通知和自动更新，确保使用最新版本，包含bug修复和安全补丁
3. **兼容性**：官方版本确保与macOS和iOS SDK的最佳兼容性
4. **技术支持**：非官方版本可能无法获得苹果完整支持

### (e) Android Studio与Xcode签名过程的关键区别
**知识点讲解：**
- **Android Studio**：
  - 使用开发者管理的keystore文件(.jks)
  - 允许自签名用于开发和发布
  - 签名流程相对简单且灵活

- **Xcode**：
  - 使用通过Apple Developer账户管理的证书和配置文件
  - 需要苹果批准和验证
  - 实施更集中的签名流程和应用验证
  - 需要开发者计划会员资格($99/年)

### (f) Google Play商店应用数量多于App Store的原因
**知识点讲解：**
1. **入门门槛低**：Google Play注册费用更低（一次性$25 vs 苹果$99/年）
2. **审核流程宽松**：Google Play审核更加自动化，相比苹果的人工严格审核更快
3. **更大灵活性**：Android允许侧载和第三方应用商店，鼓励更多开发者
4. **设备多样性**：Android设备市场份额和多样性都超过iOS，吸引了更广泛的开发者
