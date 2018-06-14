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
|Naville|385-388页|关于BCF代码的分析|[issue1](https://github.com/AloneMonkey/iOSREBook-issues/issues/1)|暂时不修改|1. 在最后直接遍历删除DebugIntrinsics也是一种方法。 <br> 2. EHPad过滤问题，其实解释都是说明同一个问题。 <br> 3. c++ 头文件没找到的问题，笔者暂时没有带libcxx试过，不过目前把头文件加上include search path就行。 <br> 4. 这里通过opt加载只是一个例子，后面的内容也说明可以直接加到PassManager编译成静态库。|
|Naville|363页|可以选择不同的编译器作为LLVM的前端，例如gcc、Clang。|[issue3](https://github.com/AloneMonkey/iOSREBook-issues/issues/3)|LLVM-GCC和Clang都可以作为LLVM的前端。|这里使用编译器不太恰当，gcc其实指的是LLVM-GCC，早期的LLVM没有一个完整的前端，社区使用GCC的前端去生成LLVM IR，这个修改后的GCC前端被称为["DragonEgg"](https://dragonegg.llvm.org/)，但是在LLVM 3之后就不再维护开发了，使用LLVM自己的前端[Clang](http://clang.llvm.org/)。|

