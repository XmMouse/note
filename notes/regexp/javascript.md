# 正则表达式
## 使用的地方
### Regexp
1. exec => [] | null
2. test => Bean
### String
1. match => [] | null
## 正则匹配模式
### 贪婪模式
1. 尽可能多的匹配匹配不成功会回溯
2. 开启方法
启用? + {}  * 默认开启
### 懒惰模式
1. 一旦匹配后就不再匹配
2. 启用模式字符加上? 例如 ?? +? {}? *?
### 独占模式
2. 尽可能多的匹配匹配不成功不会回溯
## 全局匹配
1. 将g标志或者global标志设置为true启用lastIndex属性不启用lastIndex则无法匹配多个结果(只是返回第一个)
## test match 和 exec的区别
1. test只是返回存不存在
2. match返回的是exec的包装(全局配置)阉割(子匹配，全局配置)版
3. 需要手动循环
4. 在非全局匹配下2，3差不多
5. 3比2多一个功能返回子匹配
## 非获取匹配
(?:...)
## 正则引擎
>正则引擎主要可以分为基本不同的两大类：一种是DFA（确定型有穷自动机），另一种是NFA（不确定型有穷自动机）。简单来讲，NFA 对应的是正则表达式主导的匹配，而 DFA 对应的是文本主导的匹配。
## 特殊字符
1. . not \r \n
2. \b 单词边界 \B非单词边界
3. \d 数字 \D非数字
4. \s 不可见字符[\n\r\t] \S可见字符
5. \w 包括下划线的任何单词字符