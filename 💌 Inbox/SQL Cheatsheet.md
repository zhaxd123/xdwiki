## 1️⃣ 查询所有列

```sql
SELECT * FROM users;
```

### 含义：

从 `users` 表中查询 **所有行的所有列**，包括列名和数据。

### 假设 `users` 表内容：

|id|name|age|
|---|---|---|
|1|Alice|22|
|2|Bob|25|

### 查询结果：

|id|name|age|
|---|---|---|
|1|Alice|22|
|2|Bob|25|

---

## 2️⃣ 查询指定列

```sql
SELECT name, age FROM users;
```

### 含义：

从 `users` 表中查询所有行的 `name` 和 `age` 两列（不包含 id 列）。

### 查询结果：

|name|age|
|---|---|
|Alice|22|
|Bob|25|

---

## 3️⃣ 去重查询

```sql
SELECT DISTINCT age FROM users;
```

### 含义：

从 `users` 表中查询所有唯一的 `age` 值，重复值只保留一个。

### 假设数据：

|id|name|age|
|---|---|---|
|1|Alice|22|
|2|Bob|25|
|3|Carl|25|

### 查询结果：

|age|
|---|
|22|
|25|

---

## 4️⃣ 条件筛选（WHERE）

```sql
SELECT * FROM users WHERE age > 23;
```

### 含义：

只返回 `age > 23` 的行。

### 查询结果：

|id|name|age|
|---|---|---|
|2|Bob|25|
|3|Carl|25|

---

## 5️⃣ 模糊匹配（LIKE）

```sql
SELECT * FROM users WHERE name LIKE 'A%';
```

### 含义：

返回 name 以 "A" 开头的所有行。

### 查询结果：

|id|name|age|
|---|---|---|
|1|Alice|22|

---

## 6️⃣ 排序（ORDER BY）

```sql
SELECT * FROM users ORDER BY age DESC;
```

### 含义：

按照 `age` 从高到低排序返回所有行。

### 查询结果：

|id|name|age|
|---|---|---|
|2|Bob|25|
|1|Alice|22|

---

## 7️⃣ 计数（COUNT）

```sql
SELECT COUNT(*) FROM users;
```

### 含义：

返回 `users` 表中的总行数。

### 查询结果：

|COUNT(*)|
|---|
|3|

---

## 8️⃣ 分组（GROUP BY）

```sql
SELECT age, COUNT(*) FROM users GROUP BY age;
```

### 含义：

按 `age` 分组，并统计每组的行数。

### 查询结果：

|age|COUNT(*)|
|---|---|
|22|1|
|25|2|

---

## 9️⃣ 插入数据（INSERT）

```sql
INSERT INTO users (name, age) VALUES ('Diana', 30);
```

### 含义：

向 `users` 表插入一行数据，`name = 'Diana'`，`age = 30`。

---

## 🔟 更新数据（UPDATE）

```sql
UPDATE users SET age = 26 WHERE name = 'Bob';
```

### 含义：

将 `name = 'Bob'` 的那一行的 `age` 更新为 26。

---

## 1️⃣1️⃣ 删除数据（DELETE）

```sql
DELETE FROM users WHERE age < 23;
```

### 含义：

删除 `age` 小于 23 的所有行。

---

以上就是详细注释和示例的 SQL 语法速查表。如你有特定数据库（MySQL / PostgreSQL / SQLite）环境，我可以进一步为你优化语法示例。