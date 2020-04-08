# 《offer来了》设计模式篇--工厂模式

**工厂模式（FactoryPattern）** 是最常见的设计模式，该模式设属于创建型模式，它提供了简单、快速、高效且安全地创建对象的方式。工厂模式在接口中定义了创建对象的方法，而将具体的创建对象的过程在子类中实现，用户只需通过接口创建需要的对象即可，不用关注对象的具体创建过程。同时，不同的子类可根据灵活实现创建对象的方法。

通俗的讲，工厂模式的本质就是用工厂方法代替new操作创建一个实例化对象的方法，以提供一种方便的创建有同种类型接口的产品的复杂对象。

如果代码通过初始化参数直接通过new关键字来创建实例化对象会增加代码的耦合度，不利于维护，因此需要通过工厂模式将创建实例和使用实例分来，将创建实例化对象的过程封装到工厂的方法中，我们在使用时直接通过调用工厂来获取，不需要关心具体实现过程。

**区别**
```c++
int main() {
    HuaWei huawei = new HuaWei();
    Phone iphone = new Phone();
}
```

```c++
#工厂模式
int main() {
    Factory factory = new Factory();
    Phone huawei = factory.createPhone("HuaWei");
    Phone iphone = factory.createPhone("Apple");
}
```
[有道笔记-工厂模式](http://note.youdao.com/noteshare?id=e989bc2fc615627c5979cbba639557cc)