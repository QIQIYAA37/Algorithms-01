# 修改记录

## Grades.java 的修改

### reverse 方法
- 原始代码：循环条件为 `i <= grades.length/2`，使用 `int temp`。
- 问题：对于偶数长度数组，会多执行一次无用的交换；未使用对象类型。
- 修复：将循环条件改为 `i < grades.length/2`，使用 `Integer temp` 以匹配数组类型。
- 最终：调用泛型方法 `Algorithms.reverse(grades)`。

### sort 方法
- 原始代码：单遍循环，仅比较相邻元素并交换一次，无法正确排序。
- 问题：不是完整的排序算法。
- 修复：实现插入排序，使用 `compareTo` 方法进行比较。
- 最终：调用泛型方法 `Algorithms.sort(grades)`。

## 新增文件 Algorithms.java
- 实现泛型反转和排序方法。
- `reverse` 方法：泛型反转数组。
- `sort` 方法：泛型插入排序，要求元素实现 `Comparable` 接口。

这些修改确保了算法的正确性，并符合 README 的要求，使代码更通用和可重用。