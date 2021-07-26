# Dimension-Modified

本项目是在Hugo theme: [Dimension](https://github.com/your-identity/hugo-theme-dimension.git)基础上的修改。

使用方法可参见原项目ReadMe，此处不再赘述。

---

- [Dimension-Modified](#dimension-modified)
  - [新增特性](#新增特性)
  - [如何配置](#如何配置)
    - [导航分页](#导航分页)
    - [显示备案号](#显示备案号)
    - [浏览器标签显示logo](#浏览器标签显示logo)
  - [License](#license)

---

## 新增特性 

本项目目前主要做了以下修改：
  - 将Page的URL生成方法由**urlize**修改为**md5**，以解决部分title为中文的文章无法显示的问题
  - 增加导航列表的分页功能，以解决文章或目录较多时超出界面或者显示错乱的问题
  - 可配置备案号的显示
  - 浏览器标签显示logo

---

## 如何配置

### 导航分页

该导航按照文章或目录的**title**以及**date**进行排序分页。

在`/your_site/config.toml`下配置：
```toml
paginate = 9
```
即可按照配置在导航显示对应的最多为paginate数量的导航按钮，此处示例即表示每页导航最多显示9个导航按钮。

> 该配置项在Hugo中默认为10。

### 显示备案号

首先需要在`/your_site/data`目录下创建`custom.toml`以进行个性化配置。

在`custom.toml`下配置
```toml
ICPRecordText = "XICP备XXXXXXXX号-X"
```

未配置、或配置为空字符串时时不会显示任何内容。

### 浏览器标签显示logo

在相应目录下的`_index.md`中配置`logo`属性，即可将该logo设为浏览器标签上显示的logo

```markdown
---
title: example
description: "example description."
logo: "/path/to/your/logo"
---
```

---

## License

Copyright © 2021 Atient

The theme is released under the CC BY 3.0 License. Check the [original theme license](https://github.com/Atient/hugo-theme-dimension-modified/blob/master/LICENSE.md) for additional licensing information.
