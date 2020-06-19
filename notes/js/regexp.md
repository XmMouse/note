## 正则表达式
### 模式
#### 贪婪模式&懒惰模式
 - 贪婪模式-尽量多的匹配
    - 开启方式 * + {}
 - 懒惰模式尽量少地匹配
    - 开启方式 -
#### 全局模式&局部模式
 - 全局模式
    - 开启方式-/something/g 
    - 还有i(忽略大小写) m(多行模式)
    - m影响^和$二者默认受到\n的影响
 - 局部模式
    - 不加G
### 使用接口
- exec - 最本质用法
    - exec和没有g的方法完全一致只是多了个lastIndex
- match
    - g 返回全局匹配内容不包括子匹配
    - !g 第一项为全部匹配内容-依次为子匹配
- search
- test
- replace
- split
### 特殊字符
略
### 子模式和非获取
- 子模式
    ()
- 非获取模式
    - (!:) -非获取
### []
匹配单个字符
### 代表多个字符的方式
- \* +
- (abc)
- .{1,3}
- \w