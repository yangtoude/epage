# Epage

一款基于schema的可视化页面配置工具。可基于流行的前端组件库配置表单、页面等。

[English Introduction](./README_EN.md) | 中文介绍

## 文档

官网：[http://epage.didichuxing.com](http://epage.didichuxing.com)

- [快速起步](http://epage.didichuxing.com/usage/#快速起步)
- [开发文档](http://epage.didichuxing.com/developer/)
- [设计器API](http://epage.didichuxing.com/developer/epage.html)
- [如何开发widget?](http://epage.didichuxing.com/developer/widget.html)
- [在线示例](http://epage.didichuxing.com/examples/)


## 演示地址

- **[Demo](http://epage.didichuxing.com/examples/epage.html)**

## 安装

```sh
# 需提前安装vue vuex iview vuedragable
npm install epage -S
# 或者 yarn add epage
```

## 仓库更新说明

本仓库为`Epage渲染器`及`Epage设计器`核心依赖，更新日志查看[CHANGLOG](./CHANGELOG.md)。更多`Epage渲染器`及相关工具参见：[https://github.com/epage-team](https://github.com/epage-team)。

## 设计器及渲染器示例

```js
import Epage from 'epage'
import 'epage/src/style/main.less'

const el = document.getElementById('root')
// 实例化设计器，Render为渲染器，widgets为待注册的页面部件
// 关于 Render 和 widgets，可以访问 https://github.com/epage-team/epage-iview
new Epage({ el, Render, widgets })
```

## 设计理念

通过[schema](http://epage.didichuxing.com/developer/schema.html)方式描述页面功能、展示及交互，以可视化方式配置生成schema，最终生成页面。

项目起源于流程表单场景，定制开发每一个表单成本太高且维护性差，最主要是实施人员希望通过可视化方式配置生成表单。基于此场景，在开发中我们发现，表单场景与其他一些页面（如列表页、详情页、图表报表等）场景非常相似，都应该可以通过可视化方式配置出来，从而达到组件复用、灵活配置、方便维护等效果。在使用过程中，业务的复杂远不是基础组件能覆盖的，于是要求需要具备很强的扩展性，以便定制业务组件，有些项目甚至还使用了不同前端框架。

[epage](http://epage.didichuxing.com/)的设计器及渲染器分别基于原生dom节点设计，使得设计器及渲染器分离，结合统一的[schema](http://epage.didichuxing.com/developer/schema.html)规范，实现一次设计多处渲染。关于如何定制开发widget可以访问 [如何开发widget?](http://epage.didichuxing.com/developer/widget.html)

## 交流群

微信群

![](http://img-hxy021.didistatic.com/static/star/epage-qrcode.jpg)

## License

[MIT](http://opensource.org/licenses/MIT)
