# これはなに
これは私のために私が作成したLaTeXのスタイルファイルとそのテストです。

# 目指すもの
(u)pLaTeXとLuaLaTeX+LuaTeX-jaで通るものを目指します。
XeLaTeXで通るものに関してはまだ考えていません。

自分がLaTeXを使う時に必要なものがこれですべて指定できるようにします。

クラスファイルはBXjsclassとjsclassを想定していますが、将来的にはjlreqにも対応したいと思っています。
しかし、maketitleの変更のせいでjlreqに対応できなくなっているので、分離させて上で読み込もうかと考えています。

# このパッケージで追加するもの
普段よく使うパッケージを読み込みます。TeXLive2018以降に標準で追加されるパッケージのみを読み込みます（読み込むパッケージを下にあげておきます）。
また、パッケージを利用するためにいくつかコマンドを追加しました（これも使い方等を書きます）。

---
- expl3
- xparse
- ifthen
- ifluatex
- ifuptex
- luatexja
- luatexja-ruby
- luatexja-otf
- graphicx
- xcolor
- luatexja-fontspec
- tikz
- longtable
- hyperref
- arydshln
- pxrubrica
- otf
- pxchfon
- ltjp-geometry
- geometry
- *scsnowman*
- float
- *musikui*
- url
- amsmath
- amssymb
- wrapfig
- overpic
- ascmac
- tcolorbox
- mdframed
- enumitem
- makeidx
- bxtexlogo
- fontenc
- titlesec
- fancyhdr
---

追加コマンドです。

---
- `\purizw`
LuaLaTeXと(u)pLaTeXの両方で通る全角幅です。

- `\purizh`
LuaLaTeXと(u)pLaTeXの両方で通る全角の高さです。

- `\purijafont`
日本語のフォントを変えるコマンドです。引数が2つで、1つ目は明朝体のフォントで2つ目がゴチック体のフォントを入れます。

- `\purimcdefault`
明朝体のデフォルトのフォントです。規定は小塚明朝Pr6Nです。

- `\purigtdefault`
ゴチック体のデフォルトのフォントです。規定は小塚ゴシックPr6Nです。

- `\purigeometry`
オプション引数にgeometryパッケージで使うオプションを入れてください。
何も入力しないと`pass`になります。

- `\purihypersetup`
必須引数は2つで、オプション引数があります。
必須引数の1つ目にはpdftitleを、2つ目にはpdfauthorを入れてください。
オプション引数には`\hypersetup`で使うオプションを入れてください。

- `\purichead`
fancyhdrパッケージで使うコマンドである`\chead`を決めます。
既定は`\chead[]{}`です。

- `\purilhead`
`\purichead`の`\lhead`版です。規定は`\lhead[]{}`です。

- `\purirhead`
`\purichead`の`\rhead`版です。規定は`\rhead[]{}`です。

- `\puricfoot`
fancyhdrパッケージで使うコマンドである`\cfoot`を決めます。
既定は`\cfoot[--- {\thepage} ---]{--- {\thepage} ---}`です。

- `\purilfoot`
`\puricfoot`の`\lfoot`版です。規定は`\lfoot[]{}`です。

- `\purirfoot`
`\puricfoot`の`\rfoot`版です。規定は`\rfoot[]{}`です。
---

titleとsectionのデザインを変更します（本来はパッケージではなく、クラスファイルの方で行うべきなのでしょうが）。
また、title関係でいくつかコマンドを追加します（下にあげます）。

---
- `\puritoday`
今日の日付を出します。
形式は <年>/<月>/<日>となります。

- `\subtitle`
サブタイトルをタイトルの下に出します。

- `\nonsubtitle`
サブタイトルを出したくない時に`\subtitle`の前に書いておきます。

- `\nonauthor`
著者を出したくない時に`\author`の前に書いておきます。

- `\nondate`
日付を出したくない時に`\date`の前に書いておきます。

- `\purimaketitle`
上記の`\subtitle`や`\nonauthor`等がきちんと通り、デザインを変更させるためのコマンドです。
`\maketitle`を使うときちんとしたいつもどおりのタイトルデザインになります（当然ながら`\subtitle`は使えません）。
---

# 使用・LICENSE等に関して
改変・再配布等は自由に行って構いません。また、その際に著作権の明記は一切必要ありません。

しかし、これはあくまでも自分のために作成するものなので、これを使用することによる被害等に関しては一切責任を負いません。