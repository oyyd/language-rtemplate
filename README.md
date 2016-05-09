# language-rtemplate

用于atom的rtemplate高亮package。当前版本可能包含各种各样的问题和没有涉及到的地方，请发issue或pr来帮助我们解决。

## 注意

1. 当前rtemplate同时支持: `{}`、`""`的声明方式，而在language-rtemplate中只支持高亮`{}`中的内容。其原因是rtemplate的语法规则在[TextMate的grammar规则](https://manual.macromates.com/en/language_grammars)中，表达式中表示字符串开头的`"`和作为rtemplate界定符结尾的`"`会以完全相同的规则捕获文本内容，导致无法区分这二者（同样的情况对于`{}`而言，表达式开头的`{`和界定符结尾的`}`由于符号不同可以区分）。只有通过js（或其他语言）才能区分这种情况，而TextMate grammar的json形式不能。因此`""`中的内容将保持默认字符串的高亮。

2. 代码以[language-babel](https://github.com/gandm/language-babel)为基础构建，详情见`grammars/rtemplate.json`文件中的`repository`部分，稍有修改。

## 安装

```
apm install language-rtemplate
```

## 反馈

请发到issue上。
