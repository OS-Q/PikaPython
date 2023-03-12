
<h1 align="center" style="margin: 30px 0 30px; font-weight: bold;">PikaPython</h1>
<h4 align="center">跨平台的超轻量级嵌入式 Python 引擎</h4>
<p align="center">
	<a href="https://gitee.com/lyon1998/pikapython/stargazers"><img src="https://gitee.com/lyon1998/pikapython/badge/star.svg?theme=gvp"></a>
	<a href="https://gitee.com/lyon1998/pikapython/members"><img src="https://gitee.com/lyon1998/pikapython/badge/fork.svg?theme=gvp"></a>
	<a href="https://github.com/OS-Q/PikaPython/stargazers"><img src="https://img.shields.io/github/stars/OS-Q/PikaPython?style=flat-square&logo=GitHub"></a>
	<a href="https://github.com/OS-Q/PikaPython/network/members"><img src="https://img.shields.io/github/forks/OS-Q/PikaPython?style=flat-square&logo=GitHub"></a>
	<a href="https://github.com/OS-Q/PikaPython/blob/master/LICENSE"><img src="https://img.shields.io/github/license/OS-Q/PikaPython.svg?style=flat-square"></a>
        <a href="https://github.com/OS-Q/PikaPython/actions/workflows/CI.yml"><img src="https://github.com/OS-Q/PikaPython/actions/workflows/CI.yml/badge.svg"> </a>
</p>

<p align="center">
	<a href="https://whycan.com/f_55.html" >论坛</a> |
	<a href="http://pikascript.com/doc" >文档中心</a> |
	<a href="https://space.bilibili.com/5365336/channel/seriesdetail?sid=1034902">视频</a> |
        <a href="https://item.taobao.com/item.htm?spm=a21dvs.23580594.0.0.52de3d0dt7rqAx&ft=t&id=654947372034">开发板</a> |
        <a href="https://pikadoc.readthedocs.io/zh/latest/%E4%BD%BF%E7%94%A8%20BSP%20%E5%B7%A5%E7%A8%8B.html">BSP</a> |
	<a href="https://pikadoc.readthedocs.io/zh/latest/%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8%E4%B8%8E%E6%A8%A1%E5%9D%97%E7%AE%A1%E7%90%86.html">包管理器</a> |
	<a href="https://pikadoc.readthedocs.io/zh/latest/%E4%BB%8E%20RT-Thread%20%E8%BD%AF%E4%BB%B6%E5%8C%85%E5%BC%80%E5%A7%8B.html" >RT-Thread 软件包</a>
</p>


# 1.简介

PikaPython 是一个完全重写的超轻量级 python 引擎，零依赖，零配置，可以在  **Flash ≤ 64KB，RAM≤ 4KB**  的平台下运行(如 stm32g030c8 和 stm32f103c8)，极易部署和扩展，具有大量的中文文档和视频资料。

PikaPython 也称 PikaScript、PikaPy。

<img src="document/image/147799764-5db2cb30-ee74-4cde-a2bd-b91c358ae3d9.png" width="500"/>

PikaPython 具有框架式 C 模块开发工具，只要用 Python 写好调用 API ，就能够自动连接到 C 模块，非常方便快捷。不用手动处理任何全局表、宏定义、等等。

所有的工具也是全部开源的，在 tools 目录下。

![image-20220520233540245](document/image/image-20220520233540245.png)

PikaPython 也支持 MDK、iar、RT-studio 等常见 ide 开发，能够轻松地调试 C 模块。

# 获取 PikaPython:

## 使用在线图形化工程生成器
生成器地址:
http://pikascript.com

[![](assets/1644129110261-049ad5bb-21af-40e2-9533-a1c8c86790f1.jpg)](http://pikascript.com)

## 使用 Pika 包管理器[PikaPackage.exe](https://pikadoc.readthedocs.io/zh/latest/%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8%E4%B8%8E%E6%A8%A1%E5%9D%97%E7%AE%A1%E7%90%86.html)

1. 直接运行[PikaPackage.exe](https://pikadoc.readthedocs.io/en/latest/%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8%E4%B8%8E%E6%A8%A1%E5%9D%97%E7%AE%A1%E7%90%86.html), 自动下载并更新pikapython主仓库(文件在当前磁盘的/tmp/pikapython文件夹)

2. 将[requestment.txt](/bsp/stm32g070cb/pikapython/requestment.txt)放在[PikaPackage.exe](https://pikadoc.readthedocs.io/en/latest/%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8%E4%B8%8E%E6%A8%A1%E5%9D%97%E7%AE%A1%E7%90%86.html)同一文件夹下, 运行[pikaPackage.exe](https://pikadoc.readthedocs.io/en/latest/%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8%E4%B8%8E%E6%A8%A1%E5%9D%97%E7%AE%A1%E7%90%86.html), 自动在当前目录下安装[内核](../../tree/master/src)、[预编译器](../../tree/master/tools/pikaCompiler)与[模块](../../tree/master/package)。

3. 已发布的模块列表：[packages.toml](/packages.toml)

# 开发手册

### [点此进入文档中心](http://pikascript.com/doc)

![image](document/image/144693400-99f9c038-76fd-4d95-b3d2-137bd972d580.png)


# 交流论坛

### [点此进入论坛](https://whycan.com/f_55.html)

![image](document/image/144693543-4aee46c8-b6c8-4282-99c4-e07271a4ba5f.png)

## 文件目录
[src](../../tree/master/src) - 内核源码

[bsp](../../tree/master/bsp) - 裸机芯片/板卡支持

[port](../../tree/master/port) - 操作系统和包管理器支持

[test](../../tree/master/port/linux/test) - 单元测试

[document](../../tree/master/document) - 开发文档

[examples](../../tree/master/examples) - 示例脚本

[package](../../tree/master/package) - 模块目录

[pikaCompiler](../../tree/master/tools/pikaCompiler) - 使用 rust 编写的预编译器

[pikaPackageManager](../../tree/master/tools/pikaPackageManager) - 使用 go 编写的模块管理器

# 2.平台支持列表

## MCU support
|MCU               |bsp|gpio|time|uart|pwm|adc|i2c|dac|
|---               |---|--- |--- |--- |---|---|---|---|
|stm32g030c8       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32g070cB       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f103c8       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f103rb       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f103ze       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f103rc       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f401cc       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f411ce       |√  |√   |√   |√   |√  |√  |√  |   |
|stm32f407ze       |√  |    |    |    |   |   |   |   |
|stm32f407zg       |√  |    |    |    |   |   |   |   |
|stm32h750vb       |√  |    |    |    |   |   |   |   |
|stm32f051r8       |√  |    |    |    |   |   |   |   |
|air32f103cb       |√  |√   |√   |    |   |   |   |   |
|ch582             |√  |√   |√   |√   |   |√  |√  |   |
|ch32v103r8t6      |√  |√   |√   |    |   |   |   |   |
|cm32m101a         |√  |    |    |    |   |   |   |   |
|w806              |√  |√   |√   |√   |√  |√  |√  |   |
|apm32f030r8       |√  |    |    |    |   |   |   |   |
|apm32e103vb       |√  |    |    |    |   |   |   |   |
|bl-602            |√  |√   |    |    |√  |√  |   |√  |
|bl-706            |√  |    |    |    |   |   |   |   |
|Raspberry Pico    |√  |    |    |    |   |   |   |   |
|ESP32C3           |√  |√   |√   |    |   |   |   |   |
|TC264D            |√  |    |    |    |   |   |   |   |
|devc              |√  |    |    |    |   |   |   |   |
|visual-studio     |√  |    |    |    |   |   |   |   |
|EC600N            |√  |    |    |    |   |   |   |   |
|mm32f5277e9p      |√  |√   |    |    |   |   |   |   |
|xr806(openharmony)|√  |    |    |    |   |   |   |   |


## Board support
|Board|bsp|gpio|uart|pwm|adc|i2c|rgb|lcd|arm-2d|
|---|---|---|---|---|---|---|---|---|---|
|[Pika-Pi-Zero](https://item.taobao.com/item.htm?spm=a230r.1.14.1.4f2e27a8R0qWJn&id=654947372034&ns=1&abbucket=15#detail)|√|√|√|√|√|√|√|√|√|

|Board|bsp|pika_lvgl|
|---|---|---|
|lvgl-vs-simu|√|√|
|swm320|√|√|

|Board|bsp|arm-2d|
|---|---|---|
|QEMU-arm2d|√|√|

|Board|bsp|LED|KEY|
|---|---|---|---|
|SmartLoong|√|√|√|√|

## OS support
|OS|port|GPIO|TIME|PWM|
|---|---|---|---|---|
|RT-Thread|√|√|√|√|
|vsf|√|√| | |

|OS|port|Google Test|Benchmark|
|---|---|---|---|
|linux|√|√|√|

## 相关开源项目

- ▶️ [pikapython Binding For LVGL](https://github.com/lvgl/lv_binding_pikascript)

- ⭐ [pikapython Bluepill Demo In PlatformIO — Python-like REPL 🐍🔌](https://github.com/maxgerhardt/pikascript-pio-bluepill)

- ⭐ [pikapython Bluepill Demo In GCC 🐍](https://github.com/Chandler-Kluser/pikascript_gcc_bluepill)

# 3.特性
### (1)运行环境

支持裸机运行，可运行于 **RAM ≥ 4kB** ，**FLASH ≥ 64kB** 的mcu中，如stm32g030, stm32f103c8t6，esp8266。

### (2)开发环境
支持串口下载 Python 脚本。

<img src="document/image/134841230-85de6734-8467-4245-93a5-d452b5022b42.gif" width="400" alt="微信交流群"/><br/>

支持 Keil、IAR、rt-thread studio、segger embedded studio 等IDE开发。

支持 CMake、makeFile、Scons 等构建工具

零依赖，零配置，开箱即用，极易集成进已有的C工程。

极易拓展自定义的C原生函数。

支持跨平台，可在 linux 环境开发内核。

### (3)语法特性

使用 python3 标准语法的子集。

在编译时支持 python 类和方法定义，完整支持封装、继承、多态、模块功能 - 基于 [Pika 预编译器](../../tree/master/tools/pikaCompiler)。

在运行时支持 python 方法调用、变量定义、对象构造、对象释放、控制流(if\while) - 基于 [Pika 运行时内核](../../tree/master/src)。

<details><summary>更多语法特性细节</summary>

|语法|编译时|运行时|Shell|
|---|---|---|---|
|模块定义   |√|-|-|
|模块导入   |√|√|√|
|类定义    |√|√|√|
|类继承    |√|√|√|
|方法定义   |√|√|√|
|方法重载   |√|√|√|
|方法调用   |√|√|√|
|参数定义   |√|√|√|
|参数赋值   |√|√|√|
|对象新建   |√|√|√|
|对象销毁   |√|√|√|
|对象嵌套   |√|√|√|
|控制流     |√|√|√|

#### Operator

| + | - | * | / | == | > | < | >= | <= | % | ** | // | != | & | >> | << | and | or | not | in | += | -= | *= | /= |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|√|

#### Control flow

| Syntax | State |
| --- | --- |
| if | √ |
| while | √ |
| for in [list] | √ |
| for in range(a, b) | √ |
| for in [dict] | √ |
| if elif else | √ |
| for break/continue | √ |
| while break/continue | √ |

#### Module

| Syntax | Python Module | C Module |
| --- | --- | --- |
| import [module] | √ | √ |
| import [module] as | √ | - |
| from [module] import [class/function>]| √ | - |
| from [module] import [class/function>] as | √ | - |
| from [module] import * | - | PikaObj Module Only |

#### List/Dict
| Syntax | State |
| --- | --- |
| l = list() | √  |
| l = [a, b, c] | √ |
| d = dict() | √ |
| d = {'a':x, 'b':y, 'c':z} | √ |

#### Exception

| Syntax | State |
| --- | --- |
|try:| √ |
|except:| √ |
|except [Exception]:| - |
|except [Exception] as [err]: | - |
|except: ... else:| - |
|raise:| √ |
|raise [Exception]:| - |
|finally:| - |

#### Slice

| Syntax | str | bytes | list |
| --- | --- | --- | --- |
| test[i] | √ | √ | √ |
| test[a : b] | √ | √ | √ |
| test[a :] | √ | √ | √ |

#### Other keywords/Syntax

| yield | is | comprehensions |
| --- | --- | --- |
| - | √ | - |
</details>

### (4)源码规范

注重源码可读性，命名规范，标准统一，完全不使用宏，几乎不使用全局变量。

完整的 googletest 单元测试。

# 4.交流与技术支持：

## Tencent QQ Group:

<img src="document/image/136304186-e49610e4-ce01-4524-99b6-b56842d56411.png" width="300" alt="微信交流群"/><br/>

## E-mail: liang6516@outlook.com

# 5.Demo展示

## Demo 01 GPIO

<details><summary>查看代码</summary>

``` python
import PikaStdLib
import STM32G0

mem = PikaStdLib.MemChecker()
io1 = STM32G0.GPIO()
time = STM32G0.Time()

io1.setPin('PA8')
io1.setMode('out')
io1.enable()
io1.low()

print('hello pikapython')
print('mem.max :')
mem.max()
print('mem.now :')
mem.now()

while True:
    io1.low()
    time.sleep_ms(500)
    io1.high()
    time.sleep_ms(500)

```

</details>

![Hnet-image (2)](document/image/132943428-f2b365ca-140e-42f4-936c-db6a7d9f8dee.gif)

## Demo 02 USART

<details><summary>查看代码</summary>

``` python
import PikaStdLib
import STM32G0

time = STM32G0.Time()
uart = STM32G0.UART()
uart.setId(1)
uart.setBaudRate(115200)
uart.enable()

while True:
    time.sleep_ms(500)
    readBuff = uart.read(2)
    print('read 2 char:')
    print(readBuff)

```

</details>

![Hnet-image (3)](document/image/132943365-0f7059b3-4f9d-4989-a5ec-2cce72b0cc96.gif)


## Demo 03 ADC

<details><summary>查看代码</summary>

``` python
import PikaStdLib
import STM32G0

time = STM32G0.Time()
adc1 = STM32G0.ADC()

adc1.setPin('PA1')
adc1.enable()

while True:
    val = adc1.read()
    print('adc1 value:')
    print(val)
    time.sleep_ms(500)

```

</details>

![mmexport1631351523907](document/image/132944185-0a01b1ba-8cf7-4f9f-9d73-fe9cbcd52f0b.png)

## Demo 04 PWM output

<details><summary>查看代码</summary>

``` python
import PikaStdLib
import STM32G0

time = STM32G0.Time()
pwm = STM32G0.PWM()
pwm.setPin('PA8')
pwm.setFrequency(2000)
pwm.setDuty(0.5)
pwm.enable()

while True:
    time.sleep_ms(500)
    pwm.setDuty(0.5)
    time.sleep_ms(500)
    pwm.setDuty(0.001)

```

</details>

## Demo 05 RGB

<details><summary>查看代码</summary>

``` python
import STM32G0
import PikaPiZero
import PikaStdLib

rgb = PikaPiZero.RGB()
mem = PikaStdLib.MemChecker()

rgb.init()
rgb.enable()

print('hello 2')
print('mem used max:')
mem.max()

while True:
    print('flowing')
    rgb.flow()

```

</details>

## Demo 06 Snake(Need LCD)

<details><summary>查看代码</summary>

``` python
from PikaObj import *
import PikaStdLib
import PikaPiZero
import STM32G0

# hardware init
lcd = PikaPiZero.LCD()
lcd.init()
lcd.clear('white')
key = PikaPiZero.KEY()
key.init()
time = STM32G0.Time()
x_max = 120
y_max = 150

# snake init
s = PikaPiZero.Point()
w = 9
h = 9
s.x = 50
s.y = 10
len = 0
while len < 3:
    b = s
    i = 0
    while i < len:
        b = b.next
        i = i + 1
    b.next = PikaPiZero.Point()
    b.next.x = b.x - 10
    b.next.y = b.y
    b.next.prev = b
    len = len + 1
# ring link
b.next = s
s.prev = b

i = 0
b = s
while i < len:
    lcd.fill(b.x, b.y, w, h, 'blue')
    b = b.next
    i = i + 1

print('snake lengh')
print(len)

# fruit init
f = PikaPiZero.Point()
f.x = 30
f.y = 20
lcd.fill(f.x, f.y, w, h, 'green')

# memory check
mem = PikaStdLib.MemChecker()
print('mem used max:')
mem.max()

# main loop
d = 0
isUpdate = 1
isEat = 0
while True:
    if isUpdate:
        # isUpdate = 0
        # check eat fruit
        if f.x == s.x and f.y == s.y:
            # have eat fruit
            isEat = 1
            f.x = f.x + 30
            if f.x > x_max:
                f.x = f.x - x_max
            f.y = f.y + 30
            if f.y > y_max:
                f.y = f.y - y_max
            lcd.fill(f.x, f.y, w, h, 'green')
        # move snake by the direction
        if d == 0:
            x_new = s.x + 10
            y_new = s.y
            if x_new > x_max:
                x_new = 0
        elif d == 1:
            x_new = s.x
            y_new = s.y - 10
            if y_new < 0:
                y_new = y_max
        elif d == 2:
            x_new = s.x
            y_new = s.y + 10
            if y_new > y_max:
                y_new = 0
        elif d == 3:
            x_new = s.x - 10
            y_new = s.y
            if x_new < 0:
                x_new = x_max
        if isEat:
            isEat = 0
            b_new = PikaPiZero.Point()
            b_new.x = x_new
            b_new.y = y_new
            b_new.prev = s.prev
            b_new.next = s
            s.prev.next = b_new
            s.prev = b_new
            s = b_new
            len = len + 1
            print('snake lengh')
            print(len)
            print('mem used max:')
            mem.max()
        # drow the snake and fruit
        # clear last body
        lcd.fill(s.prev.x, s.prev.y, w, h, 'white')
        # new body
        s.prev.x = x_new
        s.prev.y = y_new
        # head is last body
        s = s.prev
        lcd.fill(s.x, s.y, w, h, 'blue')
        b = s
        i = 0
    # scan key
    key_val = key.get()
    if key_val == 0:
        d = 0
        isUpdate = 1
    elif key_val == 1:
        d = 1
        isUpdate = 1
    elif key_val == 2:
        d = 2
        isUpdate = 1
    elif key_val == 3:
        d = 3
        isUpdate = 1

```

</details>

![输入图片说明](document/image/imagefwef.png)

这几个 Demo 占用的 RAM 最大值只有3.56K，把1K的堆栈也算上就是4.56K，Flash 最大占用是30.4K，以 STM32F103C8T6 的 20K RAM 和 64K Flash 为标准，RAM 才用掉不到25%，Flash 才用掉不到50%。

我们可以简单对比一下 micropython 的常用芯片 STM32F405RG 和这次跑 pikapython 的芯片STM32G070CB

## RAM资源对比
![image](document/image/132944731-a55ece1d-061f-4b91-ba87-bd6547be96a7.png)

## Flash资源对比
![image](document/image/132944745-e9cf598d-e75f-40bb-873e-911819d535b7.png)

## 参考价对比(以2021年9月11日立创商城10片售价为参考)
![image](document/image/132944757-2b5cfda8-f93f-4456-8d7f-4e4767954056.png)

## 拓展能力如何呢？

除了设备驱动之外，为 mcu 开发自定义的 python 脚本绑定在 pikapython 的开发框架下非常轻松，下面两个 Demo 就是自定义的C模块拓展，这个 Demo 基于 ARM-2D 图像驱动库开发了一些 python 脚本接口。

## 几个小方块~
![Hnet-image (7)](document/image/132945282-bfd310df-8063-456d-b90c-6b798a2c8ed5.gif)

## 几个旋转太阳~
![Hnet-image (6)](document/image/132945107-e473a2cc-9fbc-47f9-aaed-a28d3ad1048c.gif)

# 6.内核测试与开发

## 在 Docker 中测试 (recommend)
[ Docker 开发环境搭建指南 ](https://pikadoc.readthedocs.io/zh/latest/get-start_linux.html)

