# Thêm nhiều trình lắng nghe sự kiện

Thêm nhiều trình lắng nghe sự kiện với cùng handler cho một phần tử.

- Sử dụng `Array.prototype.forEach()` và `EventTarget.addEventListener()` để thêm nhiều trình lắng nghe sự kiện với hàm callback chuyển đến phần tử.

```js
const addMultipleListeners = (el, types, listener, options, useCapture) => {
  types.forEach(type =>
    el.addEventListener(type, listener, options, useCapture)
  );
};
```

```js
addMultipleListeners(
  document.querySelector('.my-element'),
  ['click', 'mousedown'],
  () => { console.log('hello!') }
);