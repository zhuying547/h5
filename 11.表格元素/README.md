浏览器会调整其他单元格，让它们宽度一致。

处理列：
```html
<colgroup>
  <col span="2">
  <col>
</colgroup>
```
table 元素的宽度带来的问题：在不设置表格宽度的情况下对列宽进行固定值输入，如果列宽的值整体值不超过表格所在容器宽度，那就能正常显示，如果超出整体值的话就会对列宽进行相应的缩放，请问如何解决这个问题呢？
`table { width: 100%; table-layout: fixed }` 设置这个属性就能解决上述问题。
为什么需要同时设置这两个值才算真正的固定列表的宽度呢？原因未知To be continue。


这时候只需再设置外部容器 `overflow: auto` 就能实现表格 x 轴滚动。

border 属性必须设置为 `"1"` 或 `""`，如果没有设置 border 属性，那么浏览器可能会认为表格是用于布局的，可能会导致显示表格的方式和预期的不同。

```css
table {
  display: table;
  border-collapse: separate;
  border-spacing: 2px;
  border-color: gray; 
}
tr {
  display: table-row;
  vertical-align: inherit;
  border-color: inherit;
}
td {
  display: table-cell;
  vertical-align: inherit;
}
th {
  display: table-cell;
  vertical-align: inherit;
  font-weight: bold;
  text-align: center;
}
tbody {
  display: table-row-group;
  vertical-align: middle;
  border-color: inherit;
}
thead {
  display: table-header-group;
  vertical-align: middle;
  border-color: inherit;
}
tfoot {
  display: table-footer-group;
  vertical-align: middle;
  border-color: inherit;
}
caption {
  display: table-caption;
  text-align: center;
}
colgroup {
  display: table-column-group;
}
col {
  display: table-column;
}
```
