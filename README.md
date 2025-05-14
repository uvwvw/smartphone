# 23年卷子

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
**规则1：Do not block the Ul thread不要阻塞UI线程**
**规则2：Do not access the Ul toolkit from outside the Ul thread只能从UI线程更新UI**
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

好的，我们来详细解答这份关于移动应用开发的题目，并对其中涉及的知识点进行中文讲解。

# 22年卷子
## Question 1: Android 六合彩应用

这个题目考察的是 Android 应用的基础知识，包括布局文件 (XML) 的理解、Activity 的生命周期、UI 控件的获取和事件处理。

**(a) 解释 activity_main.xml 中的 `match_parent` 和 `wrap_content` 的含义。(2%)**

*   **`match_parent`**:
    *   中文含义：**匹配父容器**。
    *   解释：当一个视图 (View) 的 `layout_width` 或 `layout_height` 属性设置为 `match_parent` 时，该视图的宽度或高度会扩展到与它的直接父容器 (Parent View Group) 的宽度或高度相同。简单来说，就是“有多大，我就占多大”。
*   **`wrap_content`**:
    *   中文含义：**包裹内容**。
    *   解释：当一个视图 (View) 的 `layout_width` 或 `layout_height` 属性设置为 `wrap_content` 时，该视图的宽度或高度会根据其自身内容的大小来调整，刚好能包裹住其内容即可。简单来说，就是“内容多大，我就占多大”。

**(b) 画出下面 Android 应用的布局。(4%)**

根据 `activity_main.xml` 文件，这是一个垂直方向的线性布局 (`LinearLayout` with `android:orientation="vertical"`)。它包含了六个 `TextView` (用于显示数字) 和一个 `Button` (用于生成数字)。

布局示意图如下：

```
+-----------------------------------+
| [ Number 1                      ] |  <-- TextView (id: number1)
| [ Number 2                      ] |  <-- TextView (id: number2)
| [ Number 3                      ] |  <-- TextView (id: number3)
| [ Number 4                      ] |  <-- TextView (id: number4)
| [ Number 5                      ] |  <-- TextView (id: number5)
| [ Number 6                      ] |  <-- TextView (id: number6)
| [ GENERATE ]                      |  <-- Button (id: btn_generate)
+-----------------------------------+
```

*   所有 `TextView` 和 `Button` 的 `layout_width` 都设置为 `wrap_content`，所以它们的宽度会根据其文本内容自适应。
*   `LinearLayout` 的 `orientation` 是 `vertical`，所以这些控件会从上到下垂直排列。

**(c) 填写 MainActivity.java 中的空白部分 (A), (B), (C), (D), (E), (F), (G) 和 (H)。(4%)**

这些空白部分是用来关联 Java 代码中的对象和 XML 布局文件中定义的 UI 控件的。

*   **(A) `setContentView(______(A)______);`**
    *   作用：这个方法用于设置 Activity 的用户界面布局。它需要一个布局资源的 ID。
    *   答案：`R.layout.activity_main`
    *   知识点：`R` 类是 Android 项目中自动生成的一个类，它包含了项目中所有资源的 ID。`R.layout.activity_main` 指向 `res/layout/activity_main.xml` 这个布局文件。

*   **(B) 到 (G) `findViewById(______(B-G)______);`**
    *   作用：这个方法用于在当前加载的布局中根据 ID 查找一个特定的 View 对象。
    *   答案：
        *   (B): `R.id.number1`
        *   (C): `R.id.number2`
        *   (D): `R.id.number3`
        *   (E): `R.id.number4`
        *   (F): `R.id.number5`
        *   (G): `R.id.number6`
    *   知识点：`R.id.some_id` 指向 XML 布局文件中通过 `android:id="@+id/some_id"` 定义的控件。

*   **(H) `final Button btn_generate = (Button) findViewById(______(H)______);`**
    *   答案：`R.id.btn_generate`

所以，完整的填写如下：
(A): `R.layout.activity_main`
(B): `R.id.number1`
(C): `R.id.number2`
(D): `R.id.number3`
(E): `R.id.number4`
(F): `R.id.number5`
(G): `R.id.number6`
(H): `R.id.btn_generate`

**(d) `MainActivity.java` 中的 `chooseNumbers` 方法有什么功能？(4%)**

`chooseNumbers` 方法的功能是**生成6个不重复的、范围在 [0, 48] 之间的随机整数，并通过一个布尔数组 `chosen` 来标记哪些数字被选中了。**

详细解释：
1.  `Random random = new Random();`: 创建一个随机数生成器实例。
2.  `for (int i = 0; i < 49; i++) { chosen[i] = false; }`: 初始化 `chosen` 数组，将所有元素都设置为 `false`，表示初始时没有任何数字被选中。这个数组的大小是49，对应索引 0 到 48。
3.  `for (int i = 0; i < 6; i++) { ... }`: 这个循环执行6次，目的是选出6个数字。
4.  `int temp = random.nextInt(49);`: 生成一个 `[0, 49-1]` 即 `[0, 48]` 范围内的随机整数。
5.  `while (chosen[temp] == true) { temp = random.nextInt(49); }`: 检查这个随机数 `temp` 对应的位置在 `chosen` 数组中是否已经是 `true`（即该数字是否已经被选过了）。如果是，就重新生成一个随机数，直到找到一个尚未被选中的数字。这确保了选出的6个数字是互不相同的。
6.  `chosen[temp] = true;`: 将新选中的数字 `temp` 在 `chosen` 数组中对应的位置标记为 `true`。

**注意**：题目要求是生成 `[1, 49]` 范围的数字，但此方法生成的数字索引是 `[0, 48]`。在使用这些数字时，通常需要加 1 来满足 `[1, 49]` 的要求。

**(e) 完成 `onClick` 方法的实现，使得6个随机生成的数字显示在6个文本视图中。(6%)**

我们需要在 `onClick` 方法中调用 `chooseNumbers` 方法，然后遍历 `chosen` 数组，将那些被标记为 `true` 的数字（记得加1）显示在对应的 `TextView` 上。

```java
public void onClick(View dummy) {
    boolean[] chosenNumbers = new boolean[49]; // 创建一个布尔数组来接收选中的数字
    chooseNumbers(chosenNumbers); // 调用方法生成随机数

    int count = 0; // 用于追踪已经填充了多少个TextView
    for (int i = 0; i < 49 && count < 6; i++) { // 遍历0到48
        if (chosenNumbers[i]) { // 如果这个数字被选中了
            // 将数字 (i+1) 设置到对应的TextView中
            // tv_number 是在onCreate中初始化的TextView数组
            tv_number[count].setText(String.valueOf(i + 1));
            count++; // 移动到下一个TextView
        }
    }
}
```

**完整的 `MainActivity.java` (包含(e)的实现):**

```java
package hk.hkucs.marksix;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import java.util.Random;

public class MainActivity extends AppCompatActivity {

    // 将tv_number声明为成员变量，以便在onClick中访问
    TextView[] tv_number = new TextView[6];

    void chooseNumbers(boolean[] chosen) {
        Random random = new Random();
        for (int i = 0; i < 49; i++) {
            chosen[i] = false;
        }
        for (int i = 0; i < 6; i++) {
            int temp = random.nextInt(49); // 生成 [0, 48] 的随机数
            while (chosen[temp] == true) {
                temp = random.nextInt(49);
            }
            chosen[temp] = true;
        }
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main); // (A)

        tv_number[0] = (TextView) findViewById(R.id.number1); // (B)
        tv_number[1] = (TextView) findViewById(R.id.number2); // (C)
        tv_number[2] = (TextView) findViewById(R.id.number3); // (D)
        tv_number[3] = (TextView) findViewById(R.id.number4); // (E)
        tv_number[4] = (TextView) findViewById(R.id.number5); // (F)
        tv_number[5] = (TextView) findViewById(R.id.number6); // (G)

        final Button btn_generate = (Button) findViewById(R.id.btn_generate); // (H)

        Button.OnClickListener listener = new Button.OnClickListener() {
            public void onClick(View dummy) {
                boolean[] chosenNumbers = new boolean[49];
                chooseNumbers(chosenNumbers);

                int textViewIndex = 0;
                for (int i = 0; i < 49 && textViewIndex < 6; i++) {
                    if (chosenNumbers[i]) {
                        // 数字范围是 1-49，所以用 i+1
                        tv_number[textViewIndex].setText(String.valueOf(i + 1));
                        textViewIndex++;
                    }
                }
            }
        };
        btn_generate.setOnClickListener(listener);
    }
}
```

## Question 2: Android UI 和线程

这部分考察 Android UI 更新规则、网络操作的线程问题以及 Handler 的使用。

**(a) 我们讨论了 Android UI 控制的2条规则。这些规则也适用于其他移动平台。它们是什么？(2%) 简要解释其背后的基本原理。(4%)**

这两条规则是：

1.  **UI 操作必须在主线程 (UI 线程) 中执行。**
    *   **中文解释**：所有更新用户界面的操作，比如修改文本、改变颜色、显示图片等，都必须在应用程序的主线程（通常也称为 UI 线程）中进行。
    *   **基本原理**：
        *   **线程安全 (Thread Safety)**：Android UI 工具包不是线程安全的。如果多个线程同时修改 UI 元素，可能会导致不可预测的行为、数据竞争和界面状态不一致，甚至崩溃。
        *   **简化开发 (Simplicity)**：将所有 UI 操作限制在单个线程中，可以简化 UI 框架的设计和开发者的编程模型。开发者不需要处理复杂的 UI 并发控制。
        *   **响应性 (Responsiveness)**：虽然 UI 操作本身在主线程，但耗时操作（如网络请求、磁盘 I/O）应该在工作线程中进行，以避免阻塞主线程，从而保持应用的响应性。

2.  **不要在主线程 (UI 线程) 中执行耗时操作。**
    *   **中文解释**：任何可能花费较长时间的操作，例如网络请求、大量数据处理、文件读写等，都不应该在主线程中执行。
    *   **基本原理**：
        *   **避免 ANR (Application Not Responding)**：如果主线程被长时间阻塞（通常超过5秒没有响应输入事件，或超过10秒没有完成 BroadcastReceiver），Android 系统会认为应用程序无响应，并向用户显示 ANR 对话框，提示用户关闭应用。
        *   **用户体验 (User Experience)**：阻塞主线程会导致界面卡顿、掉帧，用户无法与应用交互，极大地降低用户体验。流畅的 UI 响应是良好用户体验的关键。

**(b) 在某个 Android 应用中，一个按钮的 `OnClickListener` 实现如下。希望能从互联网下载一个 JPEG 文件并显示在一个名为 `myImageView` 的 `ImageView` 字段中，该字段在 `OnClickListener` 之外定义。**
```java
myButton.setOnClickListener(new View.OnClickListener() {
@Override
 public void onClick(View v) {
 try {
 String url = "https://i.cs.hku.hk/~comp7506/welcome.jpg";
 Bitmap bitmap = BitmapFactory.decodeStream(
 (InputStream)new URL(url).getContent());
 myImageView.setImageBitmap(bitmap);
 } catch (Exception e) {
 e.printStackTrace();
 }
 };
});
```
**当按钮被点击时会发生什么，图片能正常显示吗？(2%) 请解释你的答案。(2%)**

*   **会发生什么及图片能否正常显示？**
    *   当按钮被点击时，应用程序很可能会抛出 `NetworkOnMainThreadException` 异常并崩溃。因此，图片**不能**正常显示。

*   **解释**：
    *   `OnClickListener` 的 `onClick` 方法是在**主线程 (UI 线程)** 中执行的。
    *   代码中的 `new URL(url).getContent()` 和 `BitmapFactory.decodeStream(...)` 涉及网络请求和数据流读取，这些都是耗时操作。
    *   根据 Android UI 的第二条规则（不要在主线程中执行耗时操作），在主线程中直接进行网络请求是不被允许的。从 Android Honeycomb (API level 11) 开始，如果在主线程中执行网络操作，系统会主动抛出 `NetworkOnMainThreadException` 来阻止这种行为，以避免 ANR。
    *   即使没有抛出异常（例如在非常旧的 Android 版本或特定情况下），这种做法也会导致 UI 卡顿，用户体验极差。

**(c) 建议如何将 `View.post(Runnable)` 方法整合到上述代码中。(4%) 对于修改后的版本，当按钮被点击时会发生什么，图片能正常显示吗？(2%) 请解释你的答案。(2%)**

*   **整合 `View.post(Runnable)` 的修改建议：**
    `View.post(Runnable)` 方法可以将一个 `Runnable` 对象投递到与该 View 相关联的 UI 线程的消息队列中。这意味着 `Runnable` 中的代码将在未来的某个时间点在 UI 线程上执行。然而，`View.post(Runnable)` 本身并不能解决在主线程执行网络请求的问题。它主要用于在工作线程完成后，将更新 UI 的操作切换回主线程。
    为了正确下载图片，我们需要将网络请求放到一个单独的**工作线程**中，然后在工作线程完成图片下载后，使用 `View.post(Runnable)` (或者 `Activity.runOnUiThread()` 或 Handler) 将设置图片的操作切换回 UI 线程。

    修改后的代码如下：

    ```java
    myButton.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            new Thread(new Runnable() { // 1. 创建一个新的工作线程
                @Override
                public void run() {
                    try {
                        final String url = "https://i.cs.hku.hk/~comp7506/welcome.jpg";
                        // 2. 在工作线程中执行网络请求和图片解码
                        final Bitmap bitmap = BitmapFactory.decodeStream(
                                (InputStream) new URL(url).getContent());

                        // 3. 使用 View.post() 将更新 UI 的操作切换回主线程
                        myImageView.post(new Runnable() {
                            @Override
                            public void run() {
                                if (bitmap != null) {
                                    myImageView.setImageBitmap(bitmap);
                                }
                            }
                        });
                    } catch (Exception e) {
                        e.printStackTrace();
                        // 可以在这里通过 post 更新UI提示错误
                        myImageView.post(new Runnable() {
                            @Override
                            public void run() {
                                // 例如：myImageView.setImageResource(R.drawable.error_placeholder);
                                // 或者弹出一个Toast提示
                            }
                        });
                    }
                }
            }).start(); // 4. 启动工作线程
        }
    });
    ```

*   **修改后的版本，当按钮被点击时会发生什么，图片能正常显示吗？**
    *   当按钮被点击时，网络请求会在一个新的工作线程中执行，不会阻塞主线程。下载完成后，`myImageView.post(Runnable)` 会将 `myImageView.setImageBitmap(bitmap)` 操作调度到主线程执行。
    *   因此，图片**可以**正常显示（假设网络连接正常且图片 URL 有效），并且应用不会崩溃或卡顿。

*   **解释**：
    *   网络操作（下载图片）被移到了一个单独的工作线程中，这遵循了“不要在主线程执行耗时操作”的规则，避免了 `NetworkOnMainThreadException` 和 UI 卡顿。
    *   UI 更新操作 (`myImageView.setImageBitmap(bitmap)`) 通过 `myImageView.post()` 被安全地放回到了主线程的消息队列中执行，这遵循了“UI 操作必须在主线程中执行”的规则。

**(d) 解释 Android 中线程 (thread) 和处理器 (handler) 之间的主要区别。(2%)**

*   **线程 (Thread)**:
    *   中文含义：**线程**。
    *   解释：线程是操作系统能够进行运算调度的最小单位。在 Android 中，每个应用都有一个主线程（UI 线程），负责处理用户交互和更新界面。开发者可以创建额外的工作线程（后台线程）来执行耗时操作，以避免阻塞主线程。线程是执行代码的实际单元。
    *   主要作用：执行任务，特别是耗时任务，以实现并发。

*   **处理器 (Handler)**:
    *   中文含义：**处理器**或**消息处理器**。
    *   解释：Handler 是 Android 提供的一种机制，用于在不同线程之间发送和处理消息 (Message) 和可运行对象 (Runnable)。每个 Handler 实例都与一个特定的线程（通常是创建它的线程）及其消息队列 (MessageQueue) 相关联。
    *   主要作用：
        1.  **线程间通信**：允许一个线程（如工作线程）发送消息或 Runnable 给另一个线程（如主线程）的消息队列，由目标线程的 Handler 来处理。最常见的用途是从工作线程将结果传递给主线程以更新 UI。
        2.  **任务调度**：可以安排消息或 Runnable 在未来的某个时间点执行，或者以固定的延迟重复执行。

*   **主要区别**：
    *   **角色与功能**：
        *   **线程**是**执行者**，是代码运行的载体，负责执行具体的计算任务。
        *   **Handler**是**调度者/通信者**，它本身不直接执行耗时任务，而是负责将任务（以 Message 或 Runnable 的形式）从一个线程传递到另一个线程的消息队列中，或者安排任务在特定线程上执行。
    *   **关注点**：
        *   **线程**关注的是**并发执行**和**任务的隔离**。
        *   **Handler**关注的是**线程间的同步**、**消息传递**和**任务的调度到特定线程**。
    *   **使用场景**：
        *   当你需要执行一个独立的、可能耗时的操作序列时，你会创建一个**线程**。
        *   当你需要从一个工作线程安全地更新 UI（在主线程上），或者需要在特定线程上安排一个任务时，你会使用**Handler**（通常与 Looper 和 MessageQueue 配合）。

简单来说，线程是“干活的工人”，而 Handler 是“派发任务和传递消息的调度员”。Handler 使得工人之间（不同线程）可以有效地沟通和协调工作。

## Question 3: iOS 计数器应用

这部分考察 iOS 开发基础，使用 Swift 语言，涉及 UI 事件处理、数据类型溢出、`weak` 关键字以及 Swift 函数调用。

**(a) 请完成 `btn_add()` 和 `btn_reset()` 函数的实现，它们分别是“Add”和“Reset”按钮的监听函数。特别地，它们应该适当地更新变量 `counter` 并在标签中显示更新后的值。(6%)**

```swift
import UIKit

class ViewController: UIViewController {
    var counter: Int8 = 0 // 初始值为 0
    @IBOutlet weak var lbl_counter: UILabel!

    @IBAction func btn_add(_ sender: Any) {
        counter += 1 // 增加计数器的值
        lbl_counter.text = String(counter) // 更新标签显示的文本
    }

    @IBAction func btn_reset(_ sender: Any) {
        counter = 0 // 重置计数器的值为 0
        lbl_counter.text = String(counter) // 更新标签显示的文本
    }

    override func viewDidLoad() {
        super.viewDidLoad()
        // counter = 0 // 这行代码可以保留，也可以在声明时直接初始化
        lbl_counter.text = String(counter) // 确保初始时标签显示正确的值
    }
}
```

**知识点讲解**:
*   `@IBOutlet weak var lbl_counter: UILabel!`: `IBOutlet` 表示这个属性连接到了 Interface Builder (Storyboard 或 XIB 文件) 中的一个 UI 控件 (这里是 `UILabel`)。`weak` 是内存管理关键字，稍后会解释。`!` 表示这是一个隐式解包可选类型 (Implicitly Unwrapped Optional)，意味着我们假设这个 `UILabel` 在使用前一定会被连接好。
*   `@IBAction func btn_add(_ sender: Any)`: `IBAction` 表示这个方法连接到了 Interface Builder 中的一个 UI 事件 (比如按钮点击)。`sender` 参数通常是触发事件的控件。
*   `counter += 1`: 增加 `counter` 变量的值。
*   `lbl_counter.text = String(counter)`: `UILabel` 的 `text` 属性用于设置其显示的文本。由于 `counter` 是 `Int8` 类型，需要通过 `String()` 转换为字符串才能赋给 `text` 属性。

**(b) 假设 `btn_add()` 和 `btn_reset()` 函数已正确实现。在 Priscilla 点击按钮128次后，应用程序崩溃了。解释为什么？(3%) 请提出修复此问题的方法。(3%)**

*   **为什么会崩溃？**
    *   变量 `counter` 被声明为 `Int8` 类型。
    *   `Int8` 是一个8位有符号整数类型。它的取值范围是 **-128 到 127**。
    *   当 Priscilla 点击 "Add" 按钮：
        *   第1次点击：`counter` 变为 1。
        *   ...
        *   第127次点击：`counter` 变为 127 (这是 `Int8` 能表示的最大正数)。
        *   第128次点击：`counter` 尝试从 127 增加到 128。由于 128 超出了 `Int8` 的最大表示范围，会发生**整数溢出 (integer overflow)**。在 Swift 中，默认情况下，整数溢出会导致运行时错误，从而使应用程序崩溃。

*   **修复问题的方法：**
    *   最直接的修复方法是**将 `counter` 变量的数据类型更改为一个能够容纳更大数值范围的类型**。
    *   例如，可以将其更改为：
        *   `Int`：这是 Swift 中推荐的通用整数类型，其大小与平台的原生字长相同（在32位平台上是 `Int32`，在64位平台上是 `Int64`）。它通常足够大，可以容纳远超128的数字。
        *   `Int16`, `Int32`, `Int64`: 如果需要明确指定位数。
        *   `UInt8`, `UInt16`, `UInt32`, `UInt64`: 如果计数器永远不会是负数，可以使用无符号整数类型，这样正数的表示范围会更大 (例如 `UInt8` 的范围是 0 到 255)。

    修改后的代码（使用 `Int`）：
    ```swift
    import UIKit

    class ViewController: UIViewController {
        var counter: Int = 0 // 修改为 Int 类型
        @IBOutlet weak var lbl_counter: UILabel!

        @IBAction func btn_add(_ sender: Any) {
            counter += 1
            lbl_counter.text = String(counter)
        }

        @IBAction func btn_reset(_ sender: Any) {
            counter = 0
            lbl_counter.text = String(counter)
        }

        override func viewDidLoad() {
            super.viewDidLoad()
            lbl_counter.text = String(counter)
        }
    }
    ```
    使用 `Int` 后，`counter` 可以安全地增加到远大于128的值而不会溢出。

**(c) 上述程序中 `weak` 的含义是什么？(2%)**

*   在 `@IBOutlet weak var lbl_counter: UILabel!` 中，`weak` 是一个**内存管理所有权修饰符**，用于 ARC (Automatic Reference Counting - 自动引用计数)。
*   **含义**：
    1.  **避免强引用循环 (Retain Cycles)**：`weak` 表示对所引用的对象 (`lbl_counter` 指向的 `UILabel` 实例) 是一个**弱引用**。这意味着该引用**不会增加**被引用对象的引用计数。
    2.  **自动置为 nil**：如果被 `weak` 引用的对象被销毁（其引用计数变为0），那么这个 `weak` 引用会自动被设置为 `nil`。因此，`weak` 声明的属性必须是可选类型 (Optional)，因为它们可能在某个时刻变为 `nil`。在题目中，`UILabel!` 是隐式解包可选类型，它本质上也是可选类型。

*   **为什么 `IBOutlet` 通常是 `weak`？**
    *   View Controller (视图控制器) 通常通过其 `view` 属性强引用其主视图。主视图则强引用其所有的子视图 (subviews)，包括这个 `UILabel`。
    *   如果 View Controller 也强引用这个 `UILabel` (即没有 `weak`，默认是 `strong`)，那么就可能形成一个强引用循环：
        *   `ViewController` -> `view` (strong)
        *   `view` -> `UILabel` (strong, 作为子视图)
        *   `ViewController` -> `UILabel` (strong, 如果 `lbl_counter` 是 `strong`)
    *   虽然在这种特定的父子视图关系中，View Controller 对子视图的直接强引用通常不会导致经典的“孤岛式”强引用循环（因为父视图通常是所有者），但将 `IBOutlet` 声明为 `weak` 是一种安全且推荐的做法。这是因为 View Controller 的生命周期由其父控制器或窗口管理，而其视图层次结构有其自身的生命周期。当视图可以从视图层级中移除时（例如，在低内存警告时，非当前显示的视图可能被卸载），如果 IBOutlet 是 `strong`，它可能会不必要地持有视图对象，阻止其被正确释放。
    *   简单来说，`UILabel` 的所有权主要由其父视图（`ViewController` 的 `view`）管理。`ViewController` 只需要一个指向它的引用来操作它，而不需要拥有它。使用 `weak` 可以确保当 `UILabel` 从视图层级中移除并被释放时，`lbl_counter` 不会阻止这个过程，并会自动变为 `nil`。

**(d) 建议如何更改标签中文本的字体大小。(2%)**

可以通过以下几种方式更改 `UILabel` 中文本的字体大小：

1.  **在 Interface Builder (Storyboard 或 XIB) 中设置**：
    *   选中 `UILabel`。
    *   在右侧的 **Attributes Inspector** (属性检查器) 中，找到 **Font** 属性。
    *   点击字体选择器，可以更改字体类型和**大小 (Size)**。

2.  **通过代码设置**：
    在 `viewDidLoad()` 或其他适当的方法中，可以通过代码修改 `lbl_counter` 的 `font` 属性。

    ```swift
    override func viewDidLoad() {
        super.viewDidLoad()
        lbl_counter.text = String(counter)

        // 方法一：使用系统字体并指定大小
        lbl_counter.font = UIFont.systemFont(ofSize: 24.0) // 将字体大小设置为 24 points

        // 方法二：使用特定名称的字体并指定大小
        // lbl_counter.font = UIFont(name: "Helvetica-Bold", size: 20.0)

        // 方法三：获取当前字体，然后创建一个具有新大小的字体副本
        // if let currentFont = lbl_counter.font {
        //     lbl_counter.font = currentFont.withSize(22.0)
        // }
    }
    ```
    选择其中一种代码方式即可。最常用的是 `UIFont.systemFont(ofSize: DESIRED_SIZE)` 或 `UIFont(name: FONT_NAME, size: DESIRED_SIZE)`。

**(e) 下面给出了2个 Swift 函数的定义。假设我们要将参数 7506 和 2022 传递给它们。请写下函数调用语句。(4%)**

**(i) `func compute(num1 n1: Int, n2: Int) { … }`**

*   **函数定义分析**：
    *   第一个参数有一个外部参数名 `num1` 和一个内部参数名 `n1`。
    *   第二个参数只有一个内部参数名 `n2`，这意味着在调用时，它的外部参数名与内部参数名相同，即 `n2`。

*   **函数调用语句**：
    ```swift
    compute(num1: 7506, n2: 2022)
    ```

**(ii) `func compute(_ n1: Int, _ num2: Int) { … }`**

*   **函数定义分析**：
    *   第一个参数的外部参数名是下划线 `_`，表示在调用时**省略外部参数名**。内部参数名是 `n1`。
    *   第二个参数的外部参数名也是下划线 `_`，表示在调用时**省略外部参数名**。内部参数名是 `num2`。

*   **函数调用语句**：
    ```swift
    compute(7506, 2022)
    ```

**知识点回顾**：
*   **外部参数名 (Argument Label)**：在函数调用时使用的名称。
*   **内部参数名 (Parameter Name)**：在函数实现内部使用的名称。
*   如果只提供一个名称（如 `n2: Int`），它既是外部参数名也是内部参数名。
*   如果提供了两个名称（如 `num1 n1: Int`），第一个是外部参数名，第二个是内部参数名。
*   如果使用下划线 `_` 作为外部参数名，则在调用函数时不需要写出该参数的标签。

## Question 4: 移动应用开发通用知识

这部分考察的是关于应用商店、应用签名、版本控制、第三方 SDK 以及移动设备传感器的一些常识。

**(a) 根据一些统计数据，Google Play 商店约有287万个应用程序可供下载，而苹果 App Store 约有196万个应用程序可供下载。Google Play 商店的应用程序数量多于苹果 App Store 的原因之一是，发布到 Google Play 商店的成本低于发布到苹果 App Store。请解释。(4%)**

发布到 Google Play 商店的成本低于苹果 App Store 主要体现在以下几个方面：

1.  **开发者账户注册费用 (Developer Account Registration Fee)**：
    *   **Google Play Store**: 开发者需要支付一次性的注册费用，通常是 **25美元**。支付后，开发者可以发布多个应用，并且该账户长期有效。
    *   **Apple App Store**: 开发者需要加入苹果开发者计划 (Apple Developer Program)，年费为 **99美元/年** (对于个人或公司)。如果想加入苹果开发者企业计划 (Apple Developer Enterprise Program)，年费更高，为 **299美元/年**。这个费用是每年都需要支付的，如果停止支付，已上架的应用虽然可能不受影响，但将无法提交新的应用或更新。

2.  **审核过程和政策 (Review Process and Policies)**：
    *   **Google Play Store**:
        *   **审核相对宽松和快速**：Google Play 的审核过程通常更快，自动化程度更高。虽然也有人工审核，但整体上对应用的技术实现、设计和内容限制相对较少。
        *   **迭代更快**：开发者可以更频繁地发布更新。
    *   **Apple App Store**:
        *   **审核严格且耗时较长**：苹果的审核过程以严格著称，有详细的《App Store 审核指南》(App Store Review Guidelines)，对应用的质量、设计、内容、隐私、安全等方面都有较高要求。人工审核更为细致，因此审核周期可能较长（尽管近年来有所改善）。
        *   **被拒风险**：由于审核严格，应用被拒绝的风险相对更高，这可能导致开发者需要花费额外的时间和精力进行修改和重新提交，间接增加了成本。

3.  **硬件要求 (Hardware Requirements for Development)**：
    *   **Android (Google Play)**: Android 开发可以在多种操作系统上进行（Windows, macOS, Linux），对开发硬件的要求相对灵活，可以使用普通的 PC。
    *   **iOS (Apple App Store)**: iOS 应用开发**必须使用 macOS 操作系统的 Mac 电脑**。这意味着开发者必须拥有一台 Mac，这本身就是一项硬件成本。虽然有虚拟机或黑苹果等方式，但官方支持且最稳定的是在真实 Mac 硬件上开发。

**总结**:
最直接的成本差异在于**注册费**：Google Play 是一次性的25美元，而 Apple App Store 是每年99美元（或更高）。此外，苹果更严格的审核流程和对特定硬件的依赖也间接增加了 iOS 应用的开发和发布成本。这些因素综合起来，使得发布到 Google Play 商店的门槛和持续成本相对较低，这可能是其应用数量更多的原因之一。

**(b) 对于 Android 和 iOS 应用开发，开发者都可以维护用于签名的私钥和数字证书。请说明 Android Studio 和 Xcode 在签名过程中的主要区别。(4%)**

Android Studio 和 Xcode 在应用签名过程中的主要区别体现在**密钥管理、证书来源和签名机制**上：

1.  **密钥/证书的生成和管理**：
    *   **Android Studio (Android)**:
        *   **开发者自行生成和管理密钥库 (Keystore)**：开发者使用 Java Keytool (通常通过 Android Studio 的界面操作) 生成一个密钥库文件 (`.jks` 或 `.keystore`)。这个密钥库包含一个或多个私钥/公钥对以及对应的证书。
        *   **密钥库的保管责任在于开发者**：开发者必须妥善保管好自己的密钥库文件和密码。如果丢失，将无法更新已发布的应用（因为新版本的签名必须与旧版本一致）。
        *   **自签名证书通常用于发布**：生成的证书通常是自签名的（即由开发者自己签发），Google Play 接受这种自签名证书用于应用发布。
    *   **Xcode (iOS)**:
        *   **依赖 Apple 的开发者门户和证书颁发机构 (CA)**：开发者通过 Xcode 或 Apple Developer 网站请求证书。这些证书是由 Apple 的证书颁发机构 (CA) 签发的，而不是开发者自签名的（除了开发证书在某些本地场景）。
        *   **证书和配置文件 (Provisioning Profiles) 由 Apple 管理**：Xcode 会与 Apple Developer 账户集成，帮助管理开发证书 (Development Certificates)、分发证书 (Distribution Certificates) 和相应的配置文件。配置文件将证书、App ID 和设备（用于开发和 Ad Hoc 分发）关联起来。
        *   **私钥存储在本地钥匙串 (Keychain) 中**：生成证书请求 (CSR) 时会在本地 Mac 的钥匙串中创建私钥，证书下载后与私钥配对。

2.  **签名过程的集成度**：
    *   **Android Studio**:
        *   在构建发布版本的 APK 或 App Bundle 时，Android Studio 会引导开发者选择或创建密钥库，并输入密钥库和密钥的密码来对应用进行签名。这个过程相对独立于 Google Play 的账户体系（直到上传时才验证）。
    *   **Xcode**:
        *   签名过程与 Apple Developer 账户紧密集成。Xcode 需要配置正确的开发者团队、Bundle Identifier，并自动或手动管理签名证书和配置文件。Xcode 会在构建和归档 (Archive) 应用时使用这些证书和配置文件进行签名。
        *   对于发布到 App Store，需要使用 **App Store Distribution Certificate** 和相应的 **App Store Provisioning Profile**。

3.  **证书类型和用途**：
    *   **Android**: 通常一个发布密钥可以用于签署多个应用，并且长期使用。没有明确的“开发证书”和“分发证书”的严格区分（虽然可以创建不同的密钥用于不同目的）。
    *   **iOS**: 有明确区分的证书类型：
        *   **Development Certificates**: 用于在开发和测试期间将应用安装到注册的测试设备上。
        *   **Distribution Certificates**:
            *   **App Store**: 用于签署提交到 App Store 的应用。
            *   **Ad Hoc**: 用于在有限数量的注册设备上分发测试版本（不通过 App Store）。
            *   **Enterprise (In-House)**: 用于企业内部分发应用（不通过 App Store）。

4.  **签名的目的和验证**：
    *   **Android**: 签名主要用于**验证应用的作者身份**和**确保应用的完整性**（自首次安装后未被篡改）。Google Play 在应用上传时会验证签名，后续更新也必须使用相同的密钥签名。
    *   **iOS**: 签名除了验证作者身份和完整性外，还与 **Apple 的信任链和权限控制**紧密相关。Apple 的设备只会运行由受信任的证书（最终可追溯到 Apple Root CA）签名的代码。配置文件进一步限制了应用可以在哪些设备上运行以及可以使用哪些服务 (App Services)。

**总结主要区别**:
*   **Android**: 开发者自己生成和管理密钥库（通常是自签名），签名过程相对独立。
*   **iOS**: 依赖 Apple 的 CA 签发证书，签名过程与 Apple Developer 账户和配置文件系统紧密集成，证书类型区分更细致。

**(c) 要发布到 Google Play 商店，我们需要为我们的应用程序提供 `versionCode` 和 `versionName`。它们之间有什么区别？(2%)**

*   **`versionCode`**:
    *   **用途**: 主要供**程序内部和 Google Play 商店判断应用版本的新旧**。它是一个**整数值**。
    *   **规则**: 每次发布新版本的应用时，`versionCode` **必须递增**。Google Play 商店使用它来确定一个版本是否比另一个版本新，从而允许用户更新。如果新上传的 APK/App Bundle 的 `versionCode` 不大于当前商店中的版本，上传会被拒绝。
    *   **用户不可见**: 这个值通常不直接显示给用户。
    *   **示例**: `1`, `2`, `10`, `101` (例如，可以对应主版本号.次版本号.修订号，如 1.0.1 -> 10001)。

*   **`versionName`**:
    *   **用途**: 主要用于**向用户展示的版本号**。它是一个**字符串值**。
    *   **规则**: 这个字符串可以是你希望用户看到的任何格式，例如 `1.0`, `1.2.5`, `2.0-beta`, `Christmas Edition`。它可以不严格递增，但通常会反映应用的迭代。
    *   **用户可见**: 这个值会显示在 Google Play 商店的应用详情页面、用户设备上的“应用信息”等处。
    *   **示例**: `"1.0"`, `"2.1.3-alpha"`, `"Version 3 Release Candidate"`。

**主要区别总结**:
| 特性         | `versionCode`                                  | `versionName`                                   |
| :----------- | :--------------------------------------------- | :---------------------------------------------- |
| **数据类型** | 整数 (Integer)                                 | 字符串 (String)                                 |
| **主要用途** | 程序判断版本新旧，Google Play 用于更新控制       | 向用户展示版本信息                              |
| **更新规则** | 必须严格递增                                   | 格式灵活，通常反映版本迭代，但无强制递增要求    |
| **可见性**   | 通常对用户不可见                               | 对用户可见                                      |

一个常见的做法是，`versionName` 是用户友好的版本号 (如 "1.2.3")，而 `versionCode` 是一个内部递增的整数 (如，如果 `versionName` 是 `Major.Minor.Patch`，`versionCode` 可以是 `Major * 10000 + Minor * 100 + Patch`，或者只是一个简单的序列号)。

**(d) 为了方便 HarmonyOS 应用的开发，华为为开发者提供了几个工具包。请写出其中任意两个并解释其用途。(4%)**

华为为其 HarmonyOS (鸿蒙操作系统) 应用开发提供了多个 **DevEco Kits** (开发套件，也常称为 "Kits")，这些 Kits 封装了 HarmonyOS 的核心能力，以 API 的形式提供给开发者。以下是其中两个例子及其用途：

1.  **Account Kit (帐号服务)**:
    *   **用途**: Account Kit 提供了一套简单、安全、可信的帐号授权和管理服务。它允许开发者在自己的应用中集成华为帐号的快速登录功能。
    *   **主要功能**:
        *   **华为帐号一键授权登录**: 用户可以使用已登录的华为帐号快速、安全地登录第三方应用，无需重新注册或输入密码。
        *   **获取用户信息**: 在用户授权后，应用可以获取用户的基本信息（如昵称、头像）。
        *   **管理授权**: 用户可以查看和管理对第三方应用的授权。
    *   **益处**: 简化了用户的登录流程，提高了用户转化率和安全性。

2.  **Push Kit (推送服务)**:
    *   **用途**: Push Kit 是华为提供的消息推送平台，帮助开发者向其应用的用户实时推送消息。它建立了一条从云端到设备的稳定、可靠的消息推送通道。
    *   **主要功能**:
        *   **消息推送**: 开发者可以通过 Push Kit 向其应用的用户发送通知消息或透传消息（自定义消息）。
        *   **多种推送方式**: 支持按设备、按用户标签、按主题等多种方式进行精准推送。
        *   **消息回执和统计**: 提供消息送达状态的跟踪和推送效果的统计分析。
    *   **益处**: 帮助应用开发者与用户保持互动，提高用户活跃度和粘性，例如发送促销信息、内容更新提醒、即时通讯消息等。

**其他常见的 HarmonyOS Kits (供参考)**:
*   **Map Kit (地图服务)**: 提供地图展示、定位、路径规划等功能。
*   **Location Kit (定位服务)**: 提供混合定位能力，融合 GPS、Wi-Fi、基站等多种定位方式。
*   **IAP Kit (In-App Purchases, 应用内支付服务)**: 允许应用销售数字商品和服务。
*   **Ads Kit (广告服务)**: 帮助开发者在应用中集成广告，实现流量变现。
*   **ML Kit (机器学习服务)**: 提供文本识别、图像识别、人脸检测等预置的机器学习能力。

**(e) 移动设备上的硬件传感器和软件传感器有什么区别？(2%) 请各举一个例子。(2%)**

*   **区别**:
    *   **硬件传感器 (Hardware Sensors)**:
        *   定义：硬件传感器是**物理集成在移动设备中的电子元件或芯片**，它们直接测量设备周围环境的物理量或设备自身的状态。
        *   数据来源：直接从物理世界或设备硬件获取原始数据。
        *   特点：通常提供原始的、未经处理或较少处理的数据。
    *   **软件传感器 (Software Sensors / Synthetic Sensors / Virtual Sensors)**:
        *   定义：软件传感器**不是独立的物理设备**。它们通过**处理一个或多个硬件传感器的数据，或者通过算法模拟，来推断出更高级别的信息或虚拟的传感器读数**。它们依赖于底层硬件传感器的存在和数据。
        *   数据来源：数据来源于一个或多个硬件传感器，或者通过算法逻辑生成。
        *   特点：提供的是经过处理、融合或推断出的信息，通常更具语义性或特定用途。

*   **例子**:
    *   **硬件传感器示例**:
        *   **加速度计 (Accelerometer)**: 测量设备在三个物理轴上的加速度（包括重力）。这是一个直接测量物理运动的硬件组件。
        *   其他例子：陀螺仪 (Gyroscope)、磁力计 (Magnetometer)、光线传感器 (Light Sensor)、距离传感器 (Proximity Sensor)、GPS芯片、温度计、气压计。
    *   **软件传感器示例**:
        *   **线性加速度传感器 (Linear Acceleration Sensor)**: 这个传感器提供的是设备在三个轴上的加速度，但**排除了重力的影响**。它通常是通过加速度计的数据减去通过重力传感器（或加速度计和磁力计融合计算出的重力分量）获得的数据来计算得到的。它本身没有一个独立的物理元件，而是基于加速度计数据的软件处理结果。
        *   其他例子：重力传感器 (Gravity Sensor - 通常由加速度计和可选的陀螺仪/磁力计融合得到)、旋转矢量传感器 (Rotation Vector Sensor - 融合加速度计、陀螺仪、磁力计数据得到设备姿态)、计步器 (Step Counter - 基于加速度计数据通过算法分析步态)。

**(f) 接近传感器 (proximity sensor) 的用途是什么？(1%) 请举一个它的应用例子。(1%)**

*   **用途**:
    *   接近传感器 (Proximity Sensor) 的主要用途是**检测物体是否靠近设备的某个特定区域（通常是屏幕附近），而无需物理接触**。它通常使用红外线或其他技术来感应近距离的物体。

*   **应用例子**:
    *   **通话时自动关闭屏幕**: 当你把手机靠近耳朵接听电话时，接近传感器会检测到你的脸部靠近屏幕。为了防止脸部误触屏幕上的按钮（如挂断、静音等）并节省电量，手机会自动关闭屏幕的显示和触摸功能。当你把手机从耳朵旁移开时，屏幕会自动重新亮起。这是接近传感器最常见和典型的应用。
    *   其他例子：某些手机的手势控制（例如，手掌在屏幕上方挥过以静音来电或翻页）、智能保护套（盖上盖子时锁屏）。


