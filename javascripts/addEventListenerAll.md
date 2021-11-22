# Trình lắng nghe sự kiện

Gắn một trình lắng nghe sự kiện (event listener) cho tất cả đối tượng được cung cấp.

- Sử dụng `Array.prototype.forEach()` và `EventTarget.addEventListener()` để gắn `listener` được cung cấp với sự kiện `type` cho tất cả `targets`.


```js
const addEventListenerAll = (targets, type, listener, options, useCapture) => {
  targets.forEach(target =>
    target.addEventListener(type, listener, options, useCapture)
  );
};
```

```js
addEventListenerAll(document.querySelectorAll('a'), 'click', () =>
  console.log('Clicked a link')
);
// Log hiển thị 'Clicked a link' bất cứ khi nào phần tử được click.
```
