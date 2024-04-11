# Watrmark

> watrmark 是一个用于在网页中创建水印的 npm 包。它提供了一个简单易用的接口，让你可以轻松地添加自定义水印到网页内容中。无论是在保护敏感信息还是在展示品牌标识时，这个包都能帮助你快速生成具有专业外观的水印效果。

<img src="./public/demo.jpg" />


## ✨ 特性

- 支持TS
- 丰富的配置项
- 使用简单

## 安装

使用 npm:
```
npm install watrmark --save
```

使用 pnpm:
```
pnpm install watrmark --save
```

## 基础使用

```js
import { generate } from "watrmark"
generate("水印文本 9311")
```

## 清除水印

```js
import { generate, clearWatrmark } from "watrmark"
const watrmarkId = generate("水印文本 9311")
clearWatrmark(watrmarkId)
```

## API

### generate(text: string, options?: WatrmarkOptions)

对当前网页生成一个水印，并返回一个唯一标识，预留传递给 clearWatrmark 用于清除水印。

- **WatrmarkOptions**

| 参数 | 类型 | 描述 | 默认值 |
| --- | --- | --- | --- |
| width | `number` | 水印宽度 | 200 |
| height | `number` | 水印高度 | 200 |
| fontSize | `string` | 水印文字大小 | `24px` |
| fontFamily | `string` | 水印字体 | `微软雅黑` |
| color | `string` | 水印文字颜色 | `#333` |
| rotate | `number` | 水印旋转角度 | 330 |
| opacity | `number` | 水印透明度 | 0.1 |


- **返回值**

  - `string`

- **示例**

```js
import { generate } from "watrmark"
const watrmarkId = generate("水印文本 9311")
```
  
### clearWatrmark(watrmarkId?: string)
清除当前网页的水印, 如果不传入 watrmarkId，则清除所有.

- **示例**

```js
import { clearWatrmark } from "watrmark"
clearWatrmark("watrmarkId")
```


## Issues

https://github.com/Belen-Luo/watrmark/issues

## 更新日志

### 发布周期

- 修订版本号：日常bugfix更新。
- 次版本号：发布带有新特性的向下兼容的版本。
- 主版本号：含有破坏性更新和新特性。

#### v1.0.0

- 网页水印创建

#### v1.1.0

- 添加水印清除功能
  
#### v1.2.0

- 添加防修改和注入功能
