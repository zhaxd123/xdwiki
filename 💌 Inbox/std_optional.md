

`std::optional` 是 C++17 引入的类模板，用于表示一个**可能存在或不存在**的值。它适用于需要明确处理“无值”场景的情况，替代传统方法（如特殊标记值、布尔状态+输出参数等），提升代码安全性和可读性。

---

### **核心用法**

#### 1. **基本定义**
```cpp
#include <optional>

std::optional<int> maybeNumber;    // 默认无值
std::optional<std::string> name = "DeepSeek"; // 直接初始化有值
std::optional<float> invalid = std::nullopt;  // 显式表示无值
```

#### 2. **检查值是否存在**
```cpp
if (maybeNumber.has_value()) { /* 有值 */ }
// 或直接转换为 bool
if (name) { /* 有值 */ }
```

#### 3. **安全访问值**
```cpp
// 方法 1: value()（有值则返回，否则抛 std::bad_optional_access）
int num = maybeNumber.value();

// 方法 2: value_or(default)（无值时返回默认值）
std::string nameValue = name.value_or("Unknown");

// 方法 3: 运算符 * 或 ->（直接访问，需确保有值！）
int numDirect = *maybeNumber;
size_t len = name->length();
```

#### 4. **修改值或重置**
```cpp
maybeNumber = 42;          // 赋新值
maybeNumber = std::nullopt; // 重置为无值
maybeNumber.reset();        // 同上
```

---

### **典型场景示例**

#### 1. **函数可能返回无效结果**
```cpp
// 查找元素索引，未找到返回 std::nullopt
std::optional<size_t> findIndex(const std::vector<int>& vec, int target) {
    auto it = std::find(vec.begin(), vec.end(), target);
    if (it != vec.end()) return std::distance(vec.begin(), it);
    return std::nullopt;
}

// 调用方处理
auto idx = findIndex({1,2,3}, 2);
if (idx) std::cout << "Found at: " << *idx;
```

#### 2. **替代指针或特殊标记值**
传统方式（易出错）：
```cpp
int* findPtr(int* arr, int size, int target) {
    for (int i=0; i<size; ++i) 
        if (arr[i] == target) return &arr[i];
    return nullptr; // 特殊标记
}
```
改用 `optional`（更安全）：
```cpp
std::optional<int> findValue(const std::vector<int>& arr, int target) {
    for (auto val : arr)
        if (val == target) return val;
    return std::nullopt;
}
```

---

### **注意事项**
- **避免未检查访问**：直接使用 `value()` 或 `operator*` 前务必确认有值，否则可能导致未定义行为或异常。
- **性能**：`std::optional` 会引入少量存储开销（通常多一个布尔值大小），但无额外动态分配。
- **与 `std::variant` 对比**：若需在多个类型间选择，而非“有/无值”，应使用 `std::variant`。

通过合理使用 `std::optional`，可以显著提升代码的健壮性和表达力。