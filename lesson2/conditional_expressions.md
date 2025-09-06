# Python 條件表達式 (Conditional Expressions)

## 什麼是條件表達式？

條件表達式是一種簡潔的語法，用來根據條件選擇不同的值。它也被稱為「三元運算子」。

## 基本語法

```python
值1 if 條件 else 值2
```

- 如果**條件為真**，回傳 `值1`
- 如果**條件為假**，回傳 `值2`

## 實際範例

### 範例 1：判斷年齡
```python
age = 18
status = "成年人" if age >= 18 else "未成年人"
print(status)  # 輸出：成年人
```

### 範例 2：判斷成績等級
```python
score = 85
grade = "及格" if score >= 60 else "不及格"
print(grade)  # 輸出：及格
```

### 範例 3：判斷數字正負
```python
number = -5
result = "正數" if number > 0 else "負數或零"
print(result)  # 輸出：負數或零
```

## 與 if-else 語句的比較

### 使用 if-else 語句：
```python
age = 18
if age >= 18:
    status = "成年人"
else:
    status = "未成年人"
```

### 使用條件表達式：
```python
age = 18
status = "成年人" if age >= 18 else "未成年人"
```

**優點：**
- 程式碼更簡潔
- 一行就能完成條件判斷
- 適合簡單的條件選擇

## 注意事項

1. **只適用於簡單的條件判斷**
2. **條件表達式必須有 else 部分**
3. **避免過度複雜的條件表達式**

## 練習題

試著用條件表達式完成以下練習：

1. 判斷一個數字是否為偶數
2. 根據溫度判斷天氣狀況
3. 判斷字串是否為空

---

*記住：條件表達式讓程式碼更簡潔，但不要為了簡潔而犧牲可讀性！*

---

# Python 迴圈 (Loops)

## 什麼是迴圈？

迴圈是一種控制結構，讓程式可以重複執行一段程式碼，直到滿足特定條件為止。

## 迴圈類型

### 1. for 迴圈

用於**已知次數**的重複執行。

#### 基本語法
```python
for 變數 in 序列:
    # 要執行的程式碼
```

#### 範例 1：遍歷數字範圍
```python
# 印出 1 到 5
for i in range(1, 6):
    print(i)
```
輸出：
```
1
2
3
4
5
```

#### 範例 2：遍歷字串
```python
# 印出每個字元
name = "Python"
for char in name:
    print(char)
```
輸出：
```
P
y
t
h
o
n
```

#### 範例 3：遍歷列表
```python
# 印出列表中的每個元素
fruits = ["蘋果", "香蕉", "橘子"]
for fruit in fruits:
    print(f"我喜歡{fruit}")
```
輸出：
```
我喜歡蘋果
我喜歡香蕉
我喜歡橘子
```

### 2. while 迴圈

用於**未知次數**的重複執行，直到條件不滿足為止。

#### 基本語法
```python
while 條件:
    # 要執行的程式碼
```

#### 範例 1：計數器
```python
# 從 1 數到 5
count = 1
while count <= 5:
    print(count)
    count += 1  # 等同於 count = count + 1
```
輸出：
```
1
2
3
4
5
```

#### 範例 2：使用者輸入
```python
# 持續詢問直到輸入正確答案
answer = ""
while answer != "Python":
    answer = input("請輸入最喜歡的程式語言：")
print("答對了！")
```

## 迴圈控制語句

### break - 跳出迴圈
```python
# 找到第一個偶數就停止
numbers = [1, 3, 4, 7, 8, 9]
for num in numbers:
    if num % 2 == 0:
        print(f"找到第一個偶數：{num}")
        break
```

### continue - 跳過本次迴圈
```python
# 只印出奇數
for i in range(1, 6):
    if i % 2 == 0:
        continue  # 跳過偶數
    print(i)
```
輸出：
```
1
3
5
```

## 實用技巧

### 1. 使用 enumerate() 取得索引
```python
fruits = ["蘋果", "香蕉", "橘子"]
for index, fruit in enumerate(fruits):
    print(f"{index + 1}. {fruit}")
```
輸出：
```
1. 蘋果
2. 香蕉
3. 橘子
```

### 2. 巢狀迴圈
```python
# 九九乘法表
for i in range(1, 4):  # 1, 2, 3
    for j in range(1, 4):  # 1, 2, 3
        print(f"{i} × {j} = {i * j}")
```

### 3. 列表推導式 (List Comprehension)
```python
# 傳統寫法
squares = []
for i in range(1, 6):
    squares.append(i ** 2)

# 列表推導式寫法
squares = [i ** 2 for i in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]
```

## 迴圈練習題

1. **計算 1 到 100 的總和**
2. **印出所有小於 50 的偶數**
3. **計算字串中每個字母出現的次數**
4. **使用迴圈建立一個簡單的猜數字遊戲**

## 注意事項

⚠️ **避免無限迴圈**
- 確保 while 迴圈的條件最終會變為 False
- 在迴圈內部要有改變條件的程式碼

⚠️ **效能考量**
- 避免不必要的巢狀迴圈
- 使用適當的資料結構

---

*迴圈是程式設計的重要概念，掌握好迴圈能讓你的程式更強大！*
