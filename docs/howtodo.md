# 常用功能的实现 {#howtodo}

## 如何插入参考文献

1. 插入参考文献时，需要创建.bib格式的参考文献数据库。
2. 在合适的地方插入引用[@xie2015]，语法如下：

   ```
   引用[@xie2015]
   ```
3. 单独创建一个显示全部参考文献的.Rmd文件，内容如下：
   ```
   # References {-}
   ```

按照上述步骤，将在章节末尾和全书末尾生成参考文献。

## 如何将参考文献格式调整为国标格式

在首页文件`index.Rmd`中，用户可以通过`biblio-style`指定参考文献的格式，例如：

```yaml
---
bibliography: ["one.bib", "another.bib", "yet-another.bib"]
biblio-style: "GBT7714-2005"
link-citations: true
---
```

与此同时，还需要将上述文件复制到项目目录中，不过上述设定，仅对PDF和word输出时起作用，对于gitbook格式，则没有效果。

## 如何设置索引

在一些书的后面，我们可以看到一些人名、术语的索引\index{索引}（index），在bookdown中，可以通过`\index{}`实现。

但目前而言，只支持PDF格式的输出。需要在latex的导言区文件`preamble.tex`中，加入：

```tex
\usepackage{makeidx}
\makeindex
```

然后在配置文件`after_body.tex`中，加入：

```tex
\printindex
```

如果使用 bookdown 提供的模板，上述设置已被默认。

