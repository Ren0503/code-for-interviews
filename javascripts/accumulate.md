# Tích luỹ

Cách để tạo một mảng tổng phần tử:

- Sử dụng `Array.prototype.reduce()`, khởi tạo một bộ tích luỹ là một mảng trống để lặp qua `numbers`.
- Sử dụng `Array.prototype.slice(-1)`, toán tử (`...`) và toán tử một ngôi `+` để thêm từng giá trị vào mảng tích luỹ bao gồm cả tổng trước đó.

```js
const accumulate = (...numbers) =>
  numbers.reduce((acc, n) => [...acc, n + +acc.slice(-1)], []);
```

```js
accumulate(1, 2, 3, 4); // [1, 3, 6, 10]
accumulate(...[1, 2, 3, 4]); // [1, 3, 6, 10]
```