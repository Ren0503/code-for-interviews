# Thêm phút vào ngày

Tính ngày của `n` phút từ ngày được cho, trả về biểu diễn chuỗi của nó.

- Sử dụng `new Date()` để tạo đối tượng ngày từ tham số đầu tiên.
- Sử dụng `Date.prototype.getTime()` và `Date.prototype.setTime()` để thêm `n` phút từ ngày được cho.
- Sử dụng `Date.prototype.toISOString()`, `String.prototype.split()` và `String.prototype.replace()` để trả về định dạng chuỗi `yyyy-mm-dd HH:MM:SS`.


```js
const addMinutesToDate = (date, n) => {
  const d = new Date(date);
  d.setTime(d.getTime() + n * 60000);
  return d.toISOString().split('.')[0].replace('T',' ');
};
```

```js
addMinutesToDate('2020-10-19 12:00:00', 10); // '2020-10-19 12:10:00'
addMinutesToDate('2020-10-19', -10); // '2020-10-18 23:50:00'
```
