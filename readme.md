```{=org}
#+qiita_private: bf2689a40f6e2816d606
```
```{=org}
#+STARTUP: indent nolineimages overview num
```
```{=org}
#+TAG: Pandoc, report, 双曲割引
```
```{=org}
#+SETUPFILE: https://fniessen.github.io/org-html-themes/org/html-theme-readtheorg.setup
```
# init(initialize:初期化)

``` shell
> open .         # explorerで'.'(current dir)を開く
```

Explorerの表示をいじります(appendix 1)．

``` shell
> ls             # ls:list ('.'が省略, current dir)
aoyama_type_data.zip  bin/  comp_a_25s/
> mkdir my_comp_a #mkdir: make directory [dir]
> cd comp_a_25s/ # cd : change directory [dir]
> git stash      # gitで隠す(stash)
> git pull origin main
> cd ../my_comp_a/
                 # cd [to_dir]: '..'は一つ上のdirを指す
> cp -rf ../comp_a_25s/lectures/d4_docx_discount/ .
                 # cp: copy --options [from_dir] [to_dir]
                 # -r: recursively(再帰的に)
                 # -f: force(強制的に)
> cd d4_docx_discount/
> open .
```

# AoyamaType

``` shell
> pipx install --force git+https://github.com/daddygongon/aoyamatype.git
> sudo apt install python3-tk
> pipx install PyQt6 #が必要かも．．．
> aoyamatype -r
```

で出てきたグラフをpngで保存．

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

「AoyamaTypeによる双曲性の評価」と題するレポートを作成してください．

## GUIで

1.  結果 : グラフの貼り付け

        aoyamatype -rのグラフ

    を貼り付けて，

2.  分析 : 初回と比較

        > aoyamatype -c

    の結果を初回と比較して，寸評を加え

3.  議論 : 自分の「続ける工夫」を書き加えて，

4.  体裁 : Reportの体裁にしてLUNAへpdfで提出してください．

## CUIで

aoyamatype -rのプロットをmy_comp_a/d4\_.../aoyama_reportに保存

    > pandoc aoyama.md --from=markdown --to=docx --output=aoyama.docx
    あるいは
    > pandoc aoyama.md --from=markdown --to=docx --standalone --reference-doc=reference.docx --output=aoyama.docx

# appendix(付録)

## explorerのデフォルト変更

Explorerの表示を見やすいようにデフォルトを変更します

1.  並べ替え-\>グループ化-\>更新日時を選択
2.  ミツぼたん(...これが詳しい設定のアイコン)-\> オプション選択
3.  表示タブを選択
4.  「フォルダーに適用」ボタンを押して，「はい」を選んで，「OK」を押す
5.  再openしてデフォルトで適用されているのを確認

[![](../figs/ss_change_default_explorer_disp_marked.png)](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151211/ab0207af-c626-4bff-96bb-6de052771300.png)

## reference.docxの作り方

これには，

    > pandoc --print-default-data-file reference.docx > reference.docx

としてreference.docsという雛形を作っておいて，
書式をそれぞれのパーツで調整して，保存しておきます．

[![](./figs/screen_shot_word_style.png)](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/151211/342d7a5a-07db-4aa6-a2c1-f9a8cb91d15f.png)

## VSCode, html, md

markdownからdocxを作るのが速いです．
markdownの編集には，code編集ソフトのVSCodeが便利です．
このソフトの操作は， ３回ほど後のPythonコーディングで詳しく紹介します．
時間がある人は，自分で調べて使ってみてください．

- [vscodeのインストール](https://cs.kwansei.ac.jp/junbi/?%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E7%92%B0%E5%A2%83%E8%A8%AD%E5%AE%9A/VSCode/%E6%9C%AC%E4%BD%93)

- Get Started with VS Code(Welcome画面でStartの下にあるOpen a
  Walkthrough...をクリック)

- MarkDown \<-\> html (WYSIWYG)

- [Markdown記法一覧](https://qiita.com/oreo/items/82183bfbaac69971917f)

- [Markdownチートシート](https://gist.github.com/higeknuckle/c9b2dac43fffa3ae0774e148a69a2e6b)
