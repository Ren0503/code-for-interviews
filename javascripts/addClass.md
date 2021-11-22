# Thêm lớp

Thêm một lớp vào phần tử HTML.

- Sử dụng `Element.classList` và `DOMTokenList.add()` để thêm lớp được chỉ định vào phần tử.

```js
const addClass = (el, className) => el.classList.add(className);
```

```js
addClass(document.querySelector('p'), 'special');
// The paragraph will now have the 'special' class
```