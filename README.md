屏幕适配方案和生成适配文件工具
------------------
### 原因
    在安卓app开发过程中屏幕适配是我们需要做的重点工作之一，而我们需要考虑的重我的开发经验来看有两点
        1、安卓碎片化导致显示效果不一致
        2、UI设计给的尺寸和我们手机上的不匹配（比如我们手机屏幕宽是360dp的，但是UI给的设计稿件是基于750px屏幕宽度进行设计的）
### 目的
    所以考虑一个方案，既能很好的解决安卓碎片化的问题又能解决在实际开发中因为UI设计稿件不匹配导致的问题
### 解决方案
    现在屏幕适配方案我知道的大致有三种
        1、今日头条适配方案：通过动态的修改设备的density值来达到不同手机上的宽度dp值和我们UI设计稿件的达到一致，
          但是在开发过程中可能会遇到一些问题，如有些平板无法适配，如果项目中引用了其它控件类框架并且控件的宽高无法
          进行修改导致的问题等
        2、百分比适配方案：这个是官方提供的一套适配方案，之前也用过，但是在实际使用过程中不是那么方便，在开发过程
          中使用这种方案的并不多（以往同事和朋友）
        3、高宽限位符适配方案：这个也是官方提供的一套适配方案，根据手机屏幕高宽dp值建立不同的布局，在运行的时候根
          据手机具体值取对应的布局，如果没有合适的，会取大于并接近手机dp值的布局，如果大于手机dp值的找不到则会找
          小于手机dp值的布局文件，这中方案会导致app的文件增大
    本项目采用的是方案3并且通过将手机屏幕宽dp值根据UI设计稿件宽度px值进行换算（如UI设计稿件宽度750px，手机宽度360dp
    目录下资源没一份就是 750/360）来解决碎片化和实际开发中的问题，当然在不同手机上会有一些差异，可以通过增加屏幕适配dp
    值进行处理
### 使用方法
    
    


