# Introduction

# CJK Support

当到处本文档为pdf的时候，可能出现乱码。参考 https://github.com/epsilonant/asciidoctor-pdf-for-chinese
部分的解决方案，使用如下命令来编译pdf:

    asciidoctor-pdf \
-a scripts=cjk \
-d book \
-a pdf-theme=pdf-theme.yml \
-a pdf-fontsdir="fonts;GEM_FONTS_DIR" \
systemc-code-review.adoc

其中，pdf-theme.yml在本仓库内已经提供，这里仍然需要一个fonts目录来存放 pdf-theme.yml
中所指定的中文字体。这些字体可以从
https://github.com/bruinspaw/asciidoctor-pdf-for-chinese/releases/download/0.1.0/themes-and-fonts-0.1.0.zip
下载之后，解压，并将解压得到的 fonts 目录软链接到本目录来实现中文支持。

# Validation

本文档用到了大量的交叉引用。为了避免交叉引用的拼写错误，请使用如下命令行检查：

    asciidoctor -d book -v systemc-code-review.adoc

并根据生成的warning信息，修正文档中的交叉引用拼写错误。

此外，根据经验，交叉引用的定义不能连着放在一起，否则asciidoctor会丢失这部分的定义。
