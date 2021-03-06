## Block容器

通过Block容器进行页面的分区域布局

### 无title模式
:::demo
```html
<tc-block style="height:100px;">
test
</tc-block>

<tc-block style="padding: 5px;">
<div style="height:120px;background-color:#eee;"></div>
</tc-block>
```
:::

### title模式
:::demo
```html
<tc-block title="我是一个block" show-minimum style="height:100px;" content-style="color:red;padding:10px;">
test
</tc-block>
```
:::

### 自定义title模式
:::demo
```html
<tc-block style="height:100px;" show-maximum>
  <div slot="title" style="color:red;">我是自定义title</div>
  <div style="font-size:18px;">test</div>
</tc-block>
```
:::


### 无高度模式
:::demo
```html
<tc-block title="我是title" show-minimum show-maximum full-mode="document">
  <div style="font-size:18px;height:200px;">test</div>
</tc-block>
```
:::

### 阴影模式
:::demo
```html
<el-row :gutter="12">
  <el-col :span="8">
    <tc-block style="height:100px;">
    test
    </tc-block>
  </el-col>
  <el-col :span="8">
    <tc-block shadow="hover" style="height:100px;">
    test
    </tc-block>
  </el-col>
  <el-col :span="8">
    <tc-block shadow="never" style="height:100px;">
    test
    </tc-block>
  </el-col>
</el-row>
```
:::

### Slots
| name | 说明 |
|------|--------|
| default | 默认标签正文内容 |
| title | 标题栏 |
| rightTool | 右边工具栏 |

### Attributes

| 参数          | 说明            | 类型            | 可选值                 | 默认值   |
|-------------  |---------------- |---------------- |---------------------- |-------- |
| title   | 标题文本   | String | — | — |
| show-minimum   | 显示最小化   | Boolean | — | false |
| show-maximum   | 显示最大化   | Boolean | — | false |
| full-mode   | 全屏模式   | String | `window`,`document` | `window` |
| content-style   | 正文的样式   | String | — | — |
| content-class   | 正文的class样式名   | String | — | — |
| shadow   | 阴影模式   | String | `always`, `hover`, `never` | `always` |
