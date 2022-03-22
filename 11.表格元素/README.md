浏览器会调整其他单元格，让它们宽度一致。

处理列：
```html
<colgroup>
  <col span="2">
  <col>
</colgroup>
```

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
