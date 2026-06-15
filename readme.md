# VSCode, html, md

memoをとるにはvscode + mdが決め手です．
vscodeには，mdをpreviewする機能があります．
文字，絵，数式などを簡単に編集することが可能です．

- MarkDown \<-\> html (WYSIWYG)
- [Markdown記法一覧](https://qiita.com/oreo/items/82183bfbaac69971917f)
- [Markdownチートシート](https://gist.github.com/higeknuckle/c9b2dac43fffa3ae0774e148a69a2e6b)

# レポート

「report == 正しい引用 + format(体裁) 」です．

## 剽窃と引用

- [理科系の作文技術(木下是雄)，「意見と事実」](https://kwanseio365-my.sharepoint.com/:b:/g/personal/cru32369_nuc_kwansei_ac_jp/Edel35ir5tVHur-rJt3hN58BIueXisBxrCVOCY9rssOM9g?e=xgz38W)
- [剽窃と引用(理工学部からの通達)](https://kwanseio365-my.sharepoint.com/:b:/g/personal/cru32369_nuc_kwansei_ac_jp/ETxjRkWsYitBqGPqWY88mYEB-fS_lY82o-7oyY4ljGF_8Q?e=UG78dg)

## [レポートの体裁](https://qiita.com/daddygongon/items/3373e54f1538036d0cf4)

# 題材 :: 双曲性ってなに？

## [池田の日経記事](https://kwanseio365-my.sharepoint.com/:b:/g/personal/cru32369_nuc_kwansei_ac_jp/EYhd0TQqO3hItmsrQWkKYb4BqOFOrVws_XWWJusX4AZJ_Q?e=7a62NY)

## OSSの便利ツールpandoc

Markdownからdocxへの変換ツールpandocのinstallと使用例です．

``` shell
> sudo apt install pandoc
> pandoc hyperbolic_discount.md --from=markdown --to=docx --output=hyperbolic_discount.docx
> open hyperbolic_discount.docx
```

さらにreference.docxという書式フォーマットを提供するdocxを
作っておいてそれに合わせるやり方です(付録参照)．

    > pandoc hyperbolic_discount.md --from=markdown --to=docx --standalone --reference-doc=reference.docx --output=sample.docx

# 課題

1.  題目 : 双曲割引についてのレポートをdocxで仕上げてください．
2.  議論 : 自分の「続ける工夫」を書き加えて，
3.  体裁 : Reportの体裁にしてLUNAへpdfで提出してください．
