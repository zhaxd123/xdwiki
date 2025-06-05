`std::string_view` 是 C++17 引入的一个轻量级、**不可变的字符串“视图”类型**，可以看作是对一段字符串（例如 `std::string`、C 字符串、字面量字符串等）的**只读引用**，避免了不必要的内存拷贝。

---

## 🔍 一句话总结

> `std::string_view` 是一个只读的、非拥有的字符串片段引用，不会复制字符串内容，非常适合高性能场景下的只读字符串处理。

---

## ✅ 用法示例

```cpp
#include <iostream>
#include <string_view>

void print(std::string_view sv) {
    std::cout << sv << '\n';
}

int main() {
    std::string s = "Hello World";
    const char* cstr = "Hello C-String";
    print(s);           // std::string
    print(cstr);        // const char*
    print("Hello view"); // string literal
}
```

你可以传入各种字符串类型，`std::string_view` 都能无缝接收。

---

## ⚙️ 构造方式

```cpp
std::string_view sv1 = "Hello";                   // 来自字符串字面量
std::string s = "Hello";
std::string_view sv2 = s;                         // 来自 std::string（不复制数据）
std::string_view sv3 = s.substr(0, 3);            // 错误❌！这是临时对象的视图，容易悬垂！
std::string_view sv4(s.c_str(), 3);               // 安全✅
```

---

## 🔧 常用函数（和 std::string 类似）

|函数名|功能说明|
|---|---|
|`.size()` / `.length()`|获取长度|
|`.empty()`|是否为空|
|`.data()`|获取原始指针|
|`.substr(pos, len)`|获取子视图|
|`.remove_prefix(n)`|去掉前缀|
|`.remove_suffix(n)`|去掉后缀|
|`.starts_with(...)` / `.ends_with(...)`|检查前缀/后缀（C++20）|
|`.find(...)`|查找子串|

---

## 🎯 应用场景

### ✅ 优点：

- 避免重复分配和拷贝字符串（适合**高性能**场景）
    
- 可以用于函数参数接收各种字符串类型
    
- 快速截取、操作字符串片段
    

### ⚠️ 注意事项：

1. `std::string_view` **不拥有数据**，使用时要确保原始字符串**不会被销毁**：
    
    ```cpp
    std::string_view sv = std::string("hello").substr(0, 3); // ❌ 悬垂引用！
    ```
    
2. 用于接口时，**读操作没问题，但不能修改内容**：
    
    ```cpp
    void bad(std::string_view sv) {
        // sv[0] = 'x'; // ❌ 错误
    }
    ```
    
3. 如果你需要将 `std::string_view` 的内容保存下来，请复制：
    
    ```cpp
    std::string s_copy = std::string(sv);
    ```
    

---

## 🧠 总结对比

|类型|拥有字符串数据？|拷贝开销|可修改？|是否 null 结尾|
|---|---|---|---|---|
|`std::string`|✅ 是|中等|✅|❓ 可变|
|`const char*`|❌ 否|小|❌|✅ 必须 null|
|`std::string_view`|❌ 否|极小|❌|❌ 不保证 null 结尾|

---

如果你在处理日志、解析文本、零拷贝处理协议等场景中，`std::string_view` 是非常值得使用的工具。

如果你想了解它和 `std::span<char>` 的区别，或 `constexpr` 中的用法，我也可以继续展开。