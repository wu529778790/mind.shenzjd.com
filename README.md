# mind.shenzjd.com

> 中文名：思绪思维导图。一个简单&强大的 Web 思维导图。

本项目包含两部分：

1.一个 js 思维导图库，不依赖任何框架，可以使用它来快速完成 Web 思维导图产品的开发。

开发文档：[https://wanglin2.github.io/mind-map-docs/](https://wanglin2.github.io/mind-map-docs/)。

2.一个 Web 思维导图，基于思维导图库、Vue2.x、ElementUI 开发，可以操作电脑本地文件，可以当做一个在线版思维导图应用使用，也可以自部署和二次开发。

在线地址：[https://wanglin2.github.io/mind-map/](https://wanglin2.github.io/mind-map/)。

此外也提供了客户端可供下载使用，支持`Windows`、`Mac`及`Linux`，下载地址：

Github：[releases](https://github.com/wanglin2/mind-map/releases)。百度云盘：[地址](https://pan.baidu.com/s/1huasEbKsGNH2Af68dvWiOg?pwd=3bp3)。

> 客户端版本会落后于在线版本，尝试最新功能请优先使用在线版。

【云存储版本】如果你需要带后端的云存储版本，可以尝试我们开发的另一个项目[理想文档](https://github.com/wanglin2/lx-doc)。

## 特性

- [x] 插件化架构，除核心功能外，其他功能作为插件提供，按需使用，减小打包体积
- [x] 支持逻辑结构图（向左、向右逻辑结构图）、思维导图、组织结构图、目录组织图、时间轴（横向、竖向）、鱼骨图等结构
- [x] 内置多种主题，允许高度自定义样式，支持注册新主题
- [x] 节点内容支持文本（普通文本、富文本）、图片、图标、超链接、备注、标签、概要、数学公式
- [x] 节点支持拖拽（拖拽移动、自由调整）、多种节点形状；支持扩展节点内容、支持使用 DDM 完全自定义节点内容
- [x] 支持画布拖动、缩放
- [x] 支持鼠标按键拖动选择和 Ctrl+左键两种多选节点方式
- [x] 支持导出为`json`、`png`、`svg`、`pdf`、`markdown`、`xmind`、`txt`，支持从`json`、`xmind`、`markdown`导入
- [x] 支持快捷键、前进后退、关联线、搜索替换、小地图、水印、滚动条、手绘风格、彩虹线条、标记、外框
- [x] 提供丰富的配置，满足各种场景各种使用习惯
- [x] 支持协同编辑
- [x] 支持演示模式

官方提供了如下插件，可根据需求按需引入（某个功能不生效大概率是因为你没有引入对应的插件），具体使用方式请查看文档：

> RichText（节点富文本插件）、Select（鼠标多选节点插件）、Drag（节点拖拽插件）、AssociativeLine（关联线插件）、Export（导出插件）、KeyboardNavigation（键盘导航插件）、MiniMap（小地图插件）、Watermark（水印插件）、TouchEvent（移动端触摸事件支持插件）、NodeImgAdjust（拖拽调整节点图片大小插件）、Search（搜索插件）、Painter（节点格式刷插件）、Scrollbar（滚动条插件）、Formula（数学公式插件）、Cooperate（协同编辑插件）、RainbowLines（彩虹线条插件）、Demonstrate（演示模式插件）、OuterFrame（外框插件）、HandDrawnLikeStyle（手绘风格插件）[收费]、Notation（节点标记插件）[收费]、Numbers（节点编号插件）[收费]、Freemind（Freemind格式导入导出插件）[收费]、Excel（Excel格式导入导出插件）[收费]、Checkbox（待办插件）[收费]

本项目不会实现的特性：

> 1.自由节点，即多个根节点；
>
> 2.概要节点后面继续添加节点；
>
> 如果你需要以上特性，那么本库可能无法满足你的需求。

## 安装

```bash
npm i simple-mind-map
```

## 使用

提供一个宽高不为 0 的容器元素：

```html
<div id="mindMapContainer"></div>
```

另外再设置一下`css`样式：

```css
#mindMapContainer * {
  margin: 0;
  padding: 0;
}
```

然后创建一个实例：

```js
import MindMap from "simple-mind-map";

const mindMap = new MindMap({
  el: document.getElementById("mindMapContainer"),
  data: {
    data: {
      text: "根节点",
    },
    children: [],
  },
});
```

即可得到一个思维导图。

想要实现更多功能？可以查看[开发文档](https://wanglin2.github.io/mind-map-docs/)。
