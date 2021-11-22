# Thêm ngày

Tính ngày thứ `n` từ ngày được cho, trả về biểu diễn chuỗi của nó.

- Sử dụng `new Date()` tạo đối tượng ngày từ tham số đầu tiên.
- Sử dụng `Date.prototype.getDate()` và `Date.prototype.setDate()` để thêm `n` ngày từ ngày được cho.
- Sử dụng `Date.prototype.toISOString()` để trả về định dạng chuỗi `yyyy-mm-dd`.

```js
const addDaysToDate = (date, n) => {
  const d = new Date(date);
  d.setDate(d.getDate() + n);
  return d.toISOString().split('T')[0];
};
```

```js
addDaysToDate('2020-10-15', 10); // '2020-10-25'
addDaysToDate('2020-10-15', -10); // '2020-10-05'
```
