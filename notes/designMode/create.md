## 抽象工厂模式（小米自己的工厂生产小米所有的产品-pc-mobile）
- 类模式
- 目的
    - 创建一系列的产品
    - 
- 原则: 依赖倒置-里氏替换
## 工厂模式
- 类模式
- 目的
    - 根据条件创建合格的子类
- 类型
    - 简单工厂模式 - 一个工厂创建所有（大外包工厂只要有需要就生产-工厂具有所有生产线）
    - 工厂方法模板 - 多个工厂-每个工厂都创建自己的单一产品（小米自己的手机工厂，苹果自己的手机工厂）
## 单例模式（搭建平台出租）
- 类模式
- 核心
    - 使用静态方法-getInstance-静态属性-instance
    - 构造函数是私有的
    - 全局只能有一个
    - 有就返回无就创建
    - 自己创建自己
## 原型模式（卖软件直接复制）
- 类模式
- 目的
    - 快速地复制对象
        - 深度复制
        - 浅度复制
    - 重用大消耗的步骤（数据库连接等）
## 建造者模式（零件外包公司还是自己组装）
- 类模式
- 目的
    - 用一种方式表示对象的创建过程
    - 创建过程的绝大多数都是固定的否着没有必要
    - 用于装配config等等复杂的对象