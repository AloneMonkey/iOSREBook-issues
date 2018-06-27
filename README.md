# iOSREBook-issues

提交格式:

* 印次: 第x次印刷
* 位置: xxx页xxx行
* 问题: 发现问题
* 修改: 修改建议

范例:

* 印次: 第1次印刷
* 位置: 100页3行
* 问题: macho文件
* 修改: 建议统一写成Mach-O文件

### 勘误内容:

#### 第一次印刷(2018年6月)

|提交人|位置|内容|问题|修改|备注|
|---|---|---|---|---|---|
|Lucifer|10页|`iproxy 22 2222`|[issue12](https://github.com/AloneMonkey/iOSREBook-issues/issues/12)|`iproxy 2222 22`|端口写反了，是映射本地端口2222到设备的22端口|
|piaoyunsoft|14页10行|开发者关心的只有沙盒里面的Document、Library、tmp等。|[issue16](https://github.com/AloneMonkey/iOSREBook-issues/issues/16)|开发者关心的只有沙盒里面的Documents、Library、tmp等。|少了个s|
|pcccccc|41页|CocosPod|[issue8](https://github.com/AloneMonkey/iOSREBook-issues/issues/8)|CocoaPods|单词写错|
|AloneMonkey|目录和45页|3.4.2 使用Cycript越狱|[issue7](https://github.com/AloneMonkey/iOSREBook-issues/issues/7)|3.4.2 越狱使用Cycript|语义有误，不是使用Cycript越狱，而是在越狱环境下使用Cycript|
|mail2chensh|60页|网卡会过滤目标地址而不是自己的数据包|[issue10](https://github.com/AloneMonkey/iOSREBook-issues/issues/10)|网卡会过滤目标地址不是自己的数据包|多了个字|
|NSLogxiaoyu3|113页|(不知道这是不是Hopper解析64位`__objc_ivar`的bug，Hopper对32位和IDA的解析结果都是正常的。)|[issue9](https://github.com/AloneMonkey/iOSREBook-issues/issues/9)|(经验证，在用 Hopper 打开文件时取消勾选“Start automatic analysis after the file is loaded”复选框即可正常显示)|见issue。|
|ko1o|115页12行|经分析，0x10002bbcc处久是Block函数的实现。|[issue5](https://github.com/AloneMonkey/iOSREBook-issues/issues/5)|经分析，0x10002bbcc处就是Block函数的实现。|错别字|
|piaoyunsoft|117页倒数第6行|在这里可以以选择直接地址或者文件偏移的方式进行跳转|[issue17](https://github.com/AloneMonkey/iOSREBook-issues/issues/17)|在这里可以直接选择地址或者文件偏移的方式进行跳转|语句不通|
| NSLogxiaoyu3 |175页第8行|要将文件目录放到 /Library/Application\Support/TweakDemo/ 文件夹下面|[issue14](https://github.com/AloneMonkey/iOSREBook-issues/issues/14)|要将文件目录放到 /Library/Application\ Support/TweakDemo/ 文件夹下面|目录路径中少个空格|
|NSLogxiaoyu3|179页|Logs.xm: 和Theos中的文件一样，直接写Logs语法即可，在编译时会通过logos.pl转换成Logs.mm。|[issue13](https://github.com/AloneMonkey/iOSREBook-issues/issues/13)|Logos.xm: 和Theos中的文件一样，直接写Logos语法即可，在编译时会通过logos.pl转换成Logos.mm。|Logs改成成Logos|
|ko1o|224页倒数第6行|如图6-13所示|[issue4](https://github.com/AloneMonkey/iOSREBook-issues/issues/4)|如图6-14所示|图的编号写错了|
|piaoyunsoft|226页14行|也就是 0x54+0x34=0x88处|[issue15](https://github.com/AloneMonkey/iOSREBook-issues/issues/15)|也就是 0x2D054+0x34=0x2D088处|地址写全|
|yh8577|235页表6-7|表里ADR和ADRP指令对应的例子|[issue6](https://github.com/AloneMonkey/iOSREBook-issues/issues/6)|ADR指令的例子修改为`ADR x1, #0x1234`，<br>ADRP指令的例子修改为`ADRP x1, #0x1234`，<br>ADRP指令对应的含义修改为`base=PC[];base<11:0> = Zeros(12);x1 = base + 0x1234;`|指令的例子写错了，ADRP的含义优化一下。|
|Sometimes Naive|288页，倒数3行|分析WahtsApp的消息收发函数|[issue11](https://github.com/AloneMonkey/iOSREBook-issues/issues/11)|分析WhatsApp的消息收发函数|错别字|
|piaoyunsoft|309页，第8行|Windows、maxOS、Linux<br>需要在Mac OS和iOS上分别安装Frida。<br>在Mac OS中通过如下命令安装Frida。|[issue18](https://github.com/AloneMonkey/iOSREBook-issues/issues/18)|Windows、macOS、Linux<br>需要在macOS和iOS上分别安装Frida。<br>在macOS中通过如下命令安装Frida。|统一使用macOS|
|piaoyunsoft|341页，第3行|加密后进行静态分析和的结果|[issue19](https://github.com/AloneMonkey/iOSREBook-issues/issues/19)|加密后进行静态分析的结果|多了个 和|
|Naville|363页|可以选择不同的编译器作为LLVM的前端，例如gcc、Clang。|[issue3](https://github.com/AloneMonkey/iOSREBook-issues/issues/3)|LLVM-GCC和Clang都可以作为LLVM的前端。|这里使用编译器不太恰当，gcc其实指的是LLVM-GCC，早期的LLVM没有一个完整的前端，社区使用GCC的前端去生成LLVM IR，这个修改后的GCC前端被称为["DragonEgg"](https://dragonegg.llvm.org/)，但是在LLVM 3之后就不再维护开发了，使用LLVM自己的前端[Clang](http://clang.llvm.org/)。|
|Naville|385-388页|关于BCF代码的分析|[issue1](https://github.com/AloneMonkey/iOSREBook-issues/issues/1)|暂时不修改|1. 在最后直接遍历删除DebugIntrinsics也是一种方法。 <br> 2. EHPad过滤问题，其实解释都是说明同一个问题。 <br> 3. c++ 头文件没找到的问题，笔者暂时没有带libcxx试过，不过目前把头文件加上include search path就行。 <br> 4. 这里通过opt加载只是一个例子，后面的内容也说明可以直接加到PassManager编译成静态库。|


