# Ddpai technical documentation {#ddpai-technical-documentation}

**一、布局XML静态检查**

一、XML 类型：

（1）未使用的命名空间-----可直接删除命名空间

（2）空标记-----直接使用结束符&lt;/&gt;

二、Android lint类型：

（1）id重复------------ 暂不修改

（2）未使用merge标签--------使用merge：

（3）字符串硬编码----暂不修改，建议后续的布局 不再这么调试

（4）语音提示---不用修改

（5）按比重的布局---使用0dp

**（6）布局视图过多----看能否精简（重点）**

（7）嵌套层级过深---精简

（8）Set android:baselineAligned=&quot;false&quot; on this element for better performance

如果LinearLayout被用于嵌套的layout空间计算，它的android:baselineAligned属性应该设置成false，以加速layout计算

android:baselineAligned=&quot;false&quot;

（9）输入类型---暂不修改

（10）内嵌权重无效---适配父布局

（11）内嵌可滑动视图---暂不修改

（12）文字与背景控件合一--------------textview提供了一个属性来给它设置image需设置位置 android:drawable=&quot;@drawable/resource&quot;

（13）无效参数----删除

（14）根布局背景重绘 -----是不是考虑不用主题背景

（15）界面重叠----性能不影响，但是 海外的兼容性，最好能考虑----暂不修改

（16）缩进对称---暂不修改

（17）无效id属性 ---删除对于的id属性

（18）字体大小---暂不修改

（20）未使用的布局---暂不修改

（21）未使用的字节点 ----部分需要删除

（22）无用的父布局---部分需要删除

（23）字体单位-- 换成sp

（24）缩进的对称性 ---暂不修改

1.  代码JAVA静态检查
2.  Android类型
3.  在子线程中对view的操作----将操作view的代码移到子线程外
4.  使用资源不建议使用id-----不修改
5.  Android Lint类型
6.  Android Lint Correctness

1、api版本不匹配-----修改为判断版本号

2、无空的构造方法-----不修改

1.  字符串格式化时，需要国际化-----不修改，已修改字符串
2.  格式化日期需要绑定语言------不修改
3.  Android Lint Internationalization 国际化-----暂时不修改
4.  Android Lint Performance -------性能

1、提示handler处理时，需要加static------------检查是否调用handler.destroy（）即可

2、HashMap改成SparseArray-----修改

3、在ondraw方法中new对象------修改，ondraw频繁调用，不建议new对象

4、获取TypedArray属性需要recycle()-----修改

5、使用Double.valueOf代替new-----修改

6、使用adapter使用view holder-----修改

（4）Android Lint Security----暂时不修改

（5）Android Lint Usability----暂时不修改

1.  其他（以下都是根据修改的）

1、

2、

3、

4、