---
title: DropMenu
preview: https://didi.github.io/mand-mobile/examples/#/drop-menu
---

Drop-down menu for list filtering

### Import

```javascript
import { DropMenu } from 'mand-mobile'

Vue.component(DropMenu.name, DropMenu)
```

### Code Examples
<!-- DEMO -->

### API

#### DropMenu Props
|Props | Description | Type | Default | Note|
|----|-----|------|------|------|
|data|data source|Array<{text, disabled, options, ...}>|`[]`|type of `options` is `Array<{text, disabled, ...}>`|
|defaultValue|initial value|Array<String>|`[]`|-|
|option-render|return options rendering content|Function({text, disabled, ...}):String|-|`vue 2.1.0+` can use `slot-scope`，refer to `Radio`|

#### DropMenu Methods

##### getSelectedValue(index): listItem
获取某菜单项选中值

|参数 | 说明 | 类型 | 默认值|
|----|-----|------|------|
|index|菜单项索引值|Number|-|

返回

|属性 | 说明 | 类型|
|----|-----|------|
|listItem|选项数据|Object: {text, disabled, options, ...}|

##### getSelectedValues(): listItems
获取所有菜单项选中值

返回

|属性 | 说明 | 类型|
|----|-----|------|
|listItems|选项数据|Array<{text, disabled, options, ...}>|

#### DropMenu Events

##### @change(barItem, listItem)
选中某项事件

|属性 | 说明 | 类型|
|----|-----|------|
|barItem|菜单项数据|Object: {text, disabled, options, ...}|
|listItem|选项数据|Object: {text, disabled, ...}|

##### @show()
下拉菜单展示事件

##### @hide()
下拉菜单隐藏事件
