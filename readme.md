# Introduction

# Validation

本文档用到了大量的交叉引用。为了避免交叉引用的拼写错误，请使用如下命令行检查：

    asciidoctor -d book -v systemc-code-review.adoc

并根据生成的warning信息，修正文档中的交叉引用拼写错误。

此外，根据经验，交叉引用的定义不能连着放在一起，否则asciidoctor会丢失这部分的定义。
