# Thêm style

Thêm style được cung cấp đến phần tử.

- Sử dụng `Object.assign()` và `ElementCSSInlineStyle.style` để hợp với đối tượng `styles` được cung cấp vào styles của phần tử.

```js
const addStyles = (el, styles) => Object.assign(el.style, styles);
```

```js
addStyles(document.getElementById('my-element'), {
  background: 'red',
  color: '#ffff00',
  fontSize: '3rem'
});
```