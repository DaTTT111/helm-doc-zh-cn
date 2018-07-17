# 附录 2：Go 数据类型和模板

Helm 模板语言是用强类型的 Go 编程语言实现的。出于这个原因，模板中的变量是强类型的。大多数情况下，变量为以下类型之一：

- 字符串：一串文本
- 布尔：`true` 或 `false`
- 整数：整数值（也有 8,16,32 和 64 位有符号和无符号变体）
- float64：一个 64 位浮点值（也有 8,16 和 32 位的变体）
- 一个字节 slice（`[]byte`），通常用于保存（可能）二进制数据
- 结构题：具有属性和方法的对象
- 一个上面类型的片段（索引列表）
- 一个字符串键映射（`map[string]interface{}`），其中的值是上面的类型之一

Go中还有很多其他类型，有时需要在模板中进行转换。调试对象类型的最简单方法是用`printf "%t"`在模板中传递它，该模板将打印类型。另请参阅`typeOf`和`kindOf`函数。