# hello-world
A place where I store my ideas, something I want to achieve.

I like to find something new and meaningful in my daily life and try to do something to improve myself.

2016.3.14 

* 拼音索引

其实这个理解起来也是很简单的，就是我现在有一个文本输入框，我输入中文会有提示，输入拼音也有提示，现在的浏览器都有这样的功能实现：

比如说输入北京：

![](./beijing-0.png)

同样，输入拼音也应给出提示：

![](./beijing-1.png)

这个还可以划分出一个刚小的任务，就是先写一个简单的爬虫程序，得到浏览器可能的智能提示，这个我之前写过，但基本忘了，可以再琢磨琢磨。

* 快速字符串匹配

这个应该是女票经常给我说的一个问题，去年年末我俩都换了 6S，她总是给我抱怨 iPhone 没有小米好用，其中的一个原因就是：

在搜索手机中的联系人时候，会有以下两种需求：

1. 我们都是学生党，同一个学校的手机号码基本短号，而我的手机里面存的是那个人的电话号码完整的11位，短号呢，前两位基本固定61、67此类，现在当我输入后四位，我希望能在我输入数字的时候给出匹配的联系人，以帮助我想起这是谁的短号，这样更方便，而不是要求我去将短号补全称完整的11位再去查询；
2. 在联系人页面，有一个搜索框，例如现在我一个同学找我要另一个同学 `令狐冲（linghuchong）` 的电话号码，我一般使用拼音输入法输入中文汉字，现在通讯录也一般有了我输入拼音 `linghuchong` 它就会给出一些匹配的联系人，我现在有另一个需求，就是希望我输入拼音首字母 `lhc` 也能给出我智能提示。

- 这些天一直在关注着这个问题 [Python 的练手项目有哪些值得推荐？](https://www.zhihu.com/question/29372574) ,看到了下面 [陈清扬](https://www.zhihu.com/people/chenqingyang) 的回答，觉得这个自己应该是行有余力，遂记在这里。

写一个计算器的解释器是很好的开始， 不要写那种基本上没有任何算法完全就是堆砌一些乱七八糟的第三方库的程序，写点真正有助于自己掌握计算机科学精髓的程序，譬如解释（1+2）*3 这样一个简单的算式，其实已经包含了计算机的本质——计算，计算的本质其实就是解释。你可以先用Dijkstra的中缀转后缀表达式算法（运算符压栈）来解释一个算式，进而 研究下如何对算术表达式进行语法分析，试着用上下文无关文法来表示一个计算器的语法，然后构造语法分析树来解释一个算式。

写一个brainfuck语言的解释器也很好，brainfuck据说是唯一一种写它的解释器比看懂它的hello world程序还要容易的语言（其实还有许多这种类似的蛋疼的语言，譬如whitespace），用Python实现的代码量大概是50行左右， 之后你回头再看brainfuck的语法，会恍然大悟，图灵机的本质原来就是读写存储器和条件跳转！

计算器写熟练了可以进一步写一个正则表达式转NFA的Thompson算法，思路完全一样，只是对运算符的解释不同，然后可以再练练NFA转DFA子集构造法、或正则表达式直接直接构造DFA，然后顺便学学最小化NFA的算法。

再进一步可以写一个递归下降分析来分析算术表达式的语法，C++的parser就是用的递归下降分析。

再进一步你可以扩展已有的计算器解释器，譬如加入声明、赋值与运算、循环、流程控制， 这就可以搞一个简易同时又图灵完备的玩具语言出来了。

