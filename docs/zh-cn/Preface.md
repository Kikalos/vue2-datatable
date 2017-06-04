# § 前言

> 本 Datatable 仅支持 Vue 2.x

任何开源的 Datatable 都未必能满足所有的业务需求（否则也不会有这个项目了）  
本文档致力于让您在理解组件设计以及源码的基础上，可自行定制出最适合的 Datatable 

本 Datatable 的依赖如下：

* BootStrap 3.x + Font Awesome 4.x（全局引入）
* [lodash.orderBy](https://lodash.com/docs/4.17.4#orderBy)
* [replace-with](https://github.com/kenberkeley/replace-with)

注：BootStrap 以及 Font Awesome 的可替换性极强，您完全可以使用其他库替代（一般就是改一下类名即可）