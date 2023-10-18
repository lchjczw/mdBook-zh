# build 命令

构建命令,用于渲染您的 md,并输出静态 html:

```bash
mdbook build
```

它会尝试解析你的`SUMMARY.md`文件，以了解您的图书的结构并获取相应的文件。
要注意的是，如果你写在`SUMMARY.md`里面的文件链接不存在，它会帮你创建文件。

为方便起见，渲染的输出将保持与源目录结构相同。因此，大型书籍在渲染时能保持结构化。

#### 指定目录

`build`命令可以将目录作为参数，用作本书的根目录，而不是当前工作目录.

```bash
mdbook build path/to/book
```

#### --open

当你使用`--open`(`-o`)，mdbook 将在构建之后，在默认 Web 浏览器中打开网页书.

#### --dest-dir

`--dest-dir`(`-d`)选项允许您更改书籍的输出目录。为相对路径，（相对于书籍的根目录）。如果未指定，则默认为`book.toml`配置的`build.build-dir`字段， 或者`./book`目录.

---

**_注意:_** _build 命令会复制源目录的所有文件(除了`.md`后缀)，到构建目录_