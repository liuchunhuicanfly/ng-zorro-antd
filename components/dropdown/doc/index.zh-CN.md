---
category: Components
subtitle: 下拉菜单
type: 导航
title: Dropdown
---

向下弹出的列表。

## 何时使用

当页面上的操作命令过多时，用此组件可以收纳操作元素。点击或移入触点，会出现一个下拉菜单。可在列表中进行选择，并执行相应的命令。

## API

### 单独引入此组件

想要了解更多关于单独引入组件的内容，可以在[快速上手](/docs/getting-started/zh#单独引入某个组件)页面进行查看。

```ts
import { NzDropDownModule } from 'ng-zorro-antd';
```

### nz-dropdown

> 需要在触发下拉菜单的元素上加入 `[nz-dropdown]` 标记用于定位元素位置

| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| `[nzDisabled]` | 菜单是否禁用 | `boolean` | - |
| `[nzPlacement]` | 菜单弹出位置 | `'bottomLeft'｜'bottomCenter'｜'bottomRight'｜'topLeft'｜'topCenter'｜'topRight'` | `'bottomLeft'` |
| `[nzTrigger]` | 触发下拉的行为 | `'click'｜'hover'` | `'hover'` |
| `[nzClickHide]` | 点击后是否隐藏菜单 | `boolean` | `true` |
| `[nzVisible]` | 菜单是否显示，可双向绑定 | `boolean` | - |
| `[nzOverlayClassName]` | 下拉根元素的类名称 | `string` | - |
| `[nzOverlayStyle]` | 下拉根元素的样式 | `object` | - |
| `(nzVisibleChange)` | 菜单显示状态改变时调用，参数为 nzVisible | `EventEmitter<boolean>` | - |

菜单使用 [nz-menu](/components/menu/zh)，还包括菜单项 `[nz-menu-item]`，分割线 `[nz-menu-divider]`。

> nz-dropdown 下的 nz-menu 默认不可选中。如果需要菜单可选中，可以指定 `<ul nz-menu nzSelectable>`.

### [nz-dropdown]

用于标定下拉菜单定位元素

### nz-dropdown-button

| 参数 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| `[nzDisabled]` | 菜单是否禁用 | `boolean` | - |
| `[nzPlacement]` | 菜单弹出位置 | `'bottomLeft'｜'bottomCenter'｜'bottomRight'｜'topLeft'｜'topCenter'｜'topRight'` | `'bottomLeft'` |
| `[nzSize]` | 按钮大小，和 [nz-button](/components/button/zh) 一致 | `'large'｜'small'｜'default'` | `'default'` |
| `[nzType]` | 按钮类型，和 [nz-button](/components/button/zh) 一致 | `'primary'｜'ghost'｜'dashed'｜'danger'｜'default'` | `'default'` |
| `[nzTrigger]` | 触发下拉的行为 | `'click'｜'hover'` | `'hover'` |
| `[nzClickHide]` | 点击后是否隐藏菜单 | `boolean` | `true` |
| `[nzVisible]` | 菜单是否显示 | `boolean` | - |
| `[nzIcon]` | 右侧的 icon  | `string｜TemplateRef<void>` | `'ellipsis'` |
| `(nzVisibleChange)` | 菜单显示状态改变时调用，参数为 nzVisible | `EventEmitter<boolean>` | - |
| `(nzClick)` | 点击左侧按钮的回调 | `EventEmitter<MouseEvent>` | - |

### NzDropdownService

用于右键弹出下拉菜单，具体参见示例

| 参数 | 说明 | 参数 | 返回 |
| --- | --- | --- | --- |
| create | 创建右键菜单 | `($event:MouseEvent, template:TemplateRef<void>)` | `NzDropdownContextComponent` |
| close | 关闭右键菜单 | - | - |