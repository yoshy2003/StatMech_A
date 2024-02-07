# 統計力学

## 全体の説明

- このリポジトリには、統計力学の基礎を理解するためのMATLAB®ライブスクリプトが含まれている。
- 統計力学を初めて学ぶ学生を対象に、MATLABを用いた数値計算・数値シミュレーションを通して、統計力学の基本的な概念や理論の背景を理解することを目的とする。
  - 特に、初学者が統計物理学の世界にスムーズに入門できるよう、直感的な説明と演習問題を提供する。
- このサイトの内容は、数値計算・数値シミュレーションを用いた、座学で学ぶ統計力学講義に対する補助的な位置づけとなっている。

### 目次
[マインドマップ](https://github.com/yoshy2003/StatMech_A/blob/main/Images/mindmap.png)
- pdf で一覧表を作成する

- 第Ⅰ部 基礎
  - 第１章 <a href="#chap01">確率分布</a>
  - 第２章 <a href="#chap02">カノニカル分布</a>
  - 第３章 <a href="#chap03">ミクロカノニカル分布とボルツマンの関係式</a>
- 第Ⅱ部 カノニカル分布の応用
  - 第４章 外場がはたらく系
  - 第５章 調和振動子系
  - 第６章 粒子数分布
  - 第７章 グランドカノニカル分布
- 第Ⅲ部 量子統計
  - 第８章 量子統計の基礎
  - 第９章 量子多体系
  - 第１０章 フェルミ自由粒子系
  - 第１１章 ボーズ自由粒子系
- 第Ⅳ部 状態の遷移・ゆらぎ
  - 第１２章 <a href="#chap12">ミクロな状態の遷移</a>
  - 第１３章 平衡状態のゆらぎ
- 第Ⅴ部 付録
  - A. <a href="#appA">数学的準備</a>
  - B. <a href="#appB">その他（関連内容）</a>

（2024年02月現在。内容は随時、追加・更新されます。）

### 前提となる知識

- 熱力学
- 古典力学・量子力学
  - 特に、エネルギーに関連する内容

### 対象学年

- 大学３年・４年（＋意欲的な高校生～大学２年生）

### 学習目標

- マクロな状態とミクロな状態との関係に関する基本的な概念を理解する。
- 乱数に基づく数値シミュレーションを通して、統計力学の基礎を学ぶ。
- ライブスクリプトを用いて理論の理解を深め、実際の物理現象をモデル化しシミュレーションできるようになる。

### 学習の流れ

1. 概要を読み、各節の目的を確認する
2. ライブスクリプトの内容に従って、コードを実行する
3. ライブスクリプトにある例題に取り組む

---

## <p id="chap01">第１章： 確率分布</p>

#### ===== 概要 =====

- 統計力学において基本的な以下の確率分布を紹介する。
  - 一様分布・指数分布・二項分布・ポアソン分布・正規分布
- 乱数は等確率に生成される（一様乱数の場合）だけでなく、特定の確率分布に従うように生成することもできる。
  - 例えば、1次元ランダムウォークの結果として得られる位置を再現したい場合には、二項分布または正規分布に従った乱数を生成することになる。
  - MATLABには一様乱数や正規乱数を生成する関数が標準で提供されており、これらを利用して乱数列を生成することができる。
- 確率分布に従って生成した乱数列の頻度分布を描画し、関数でフィッティングすることにより確認する。
  - 確率分布乱数に対する基本的な統計量（平均・分散・偏差）を求める。
- 確率分布は離散的にも連続的にも表すことができる。
  - 例えば、コインの状態は離散的（表か裏）、粒子の位置は連続的に分布する。
  - 連続変数で表される場合は、確率密度 $p(x)$を用いて、区間 $x$から $x+dx$までの確率が $p(x)dx$で与えられる。
  - 確率の総和が1であることに注意して、離散と連続との変換を行うことができる。


#### ===== ライブスクリプト =====

| 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| -------------- | -------------- | -------------- |
| (1) [経験的確率と大数の法則](Livescripts/empirical_probability_statA_240205.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/empirical_probability_statA_240205.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/empirical_probability_statA_240205.mlx) |
| (2) [基本的な確率分布](Livescripts/probability_distribution_statA_240205.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/probability_distribution_statA_240205.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/probabilityl_distributions_lec_v23.mlx) |
| (3) コイン投げと大数の法則 | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/binomial_distribution_lec.mlx) |
| (4) 二項分布から正規分布へ | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/binomial_distribution_lec.mlx) |
| (5) [中心極限定理の確認](Livescripts/central_limit_theorem_statA_240205.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/central_limit_theorem_statA_240205.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/central_limit_theorem_statA_240205.mlx) |



---

## <p id="chap02">第２章： カノニカル分布</p>

#### ===== 概要 =====

- カノニカル分布を理解するために、コインの分配モデルを用いた系の定常状態に着目しよう。


#### ===== ライブスクリプト =====

| 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| -------------- | -------------- | -------------- |
| (1) コイン分配モデルとカノニカル分布  | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Coin_canonical.mlx)|
| (1) コイン交換モデルと平衡状態  | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Coin_exchange_23.mlx)|
| (2) コイン交換モデルによる緩和過程 | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=coin_exchange_lec_21v1.mlx)|



---

## <p id="chap03">第３章： ミクロカノニカル分布とボルツマンの関係式</p>

#### ===== 概要 =====

- カノニカル分布を理解するために、コインの分配モデルを用いた系の定常状態に着目しよう。


#### ===== ライブスクリプト =====

| 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| -------------- | -------------- | -------------- |


---

## <p id="chap12">第１２章： ミクロな状態遷移とゆらぎ</p>

#### ===== 概要 =====

- カノニカル分布を理解するために、コインの分配モデルを用いた系の定常状態に着目しよう。
ミクロな状態の遷移に基づいて平衡状態の実現を考察するため、ここでは、1次元理想気体のモデルを例とする。
実際、以下のような問題を設定しよう。
いま、系内には $N$個の粒子が存在し、初期状態では全粒子が同一の速度 $v_0$を持っているとする、
この系が温度 $T$の熱浴に接している状況を考え、系がどのように平衡状態に緩和するかを調べる。
特に、平衡状態における粒子の速度分布に着目しよう。
統計力学に基づけば、平衡状態での速度分布はマクスウェル分布に従うことになる。
初期条件では、速度分布は $v = v_0$でデルタ関数となっているが、このデルタ関数的な分布が、どのようにマクスウェル分布へと緩和していくかを観察する。


#### ===== ライブスクリプト =====

| 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| -------------- | -------------- | -------------- |
| (1) 詳細つりあいと平衡状態  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/Detailed_balance_21v1.mlx)  |
| (1) ２準位系  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/Detailed_balance_21v1.mlx)  |
| (2) イジングモデル  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/Detailed_balance_21v1.mlx)  |



---

## <p id="appA">付録Ａ： 数学的準備</p>

#### ===== 概要 =====



#### ===== ライブスクリプト =====

| 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| -------------- | -------------- | -------------- |
| (1) [離散分布に対する近似的な連続表現](Livescripts/approx_dis_con.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/approx_dis_con.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/approx_dis_con.mlx) |
|(2) [スターリングの公式：証明と近似精度](Livescripts/Stirling_formula_statA_240207.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/Stirling_formula_statA_240207.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Stirling_formula_statA_240207.mlx)|


---

## <p id="appB">付録Ｂ： その他</p>

#### ===== 概要 =====



#### ===== ライブスクリプト =====

| 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| -------------- | -------------- | -------------- |
| (1) [一様乱数の生成と頻度分布の描画](Livescripts/uniform_random_number_histogram_lec_23.md)  | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/uniform_random_number_histogram_lec_23.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/uniform_random_number_histogram_lec_23.mlx)  |
| (2) ランダムウォークと拡散  | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/random_walk_lec_21v1.mlx)  |


### 1.4 乱数を用いた数値計算

#### ===== 概要 =====

- 乱数を利用した数値計算は一般に、モンテカルロ法と呼ばれている。
- 一例として、乱数を利用して、特定の領域に対する面積を求める方法を紹介する。
  - 例えば、正方形の領域内に特定の領域が存在するとして、正方形の面積を $S$、特定の領域の面積を $S_1$とする。
  - なお、$S$は既知として、 $S_1$を求めることにしよう。
  - この計算は以下の次のステップで進めることができる。
    1. 全領域にランダムに $N$個の点を打つ。なおこの際、乱数を用いて点をランダムに打つ。
    2. 特定領域に入った点の数 $N_1$を数える。
    3. 打たれた点が全領域に均一に分布していると仮定すれば、 $N$が大きくなるにつれて、面積比と点の数の割合が等しくなると期待される。<br>つまり、全領域に対する特定の領域の面積比は、全点に対する特定領域内の点の割合に近似されることになる。
    4. 従って、 $S_1$は、 $S_1 \approx S \times \frac{N_1}{N}$で求められる。
  - モンテカルロ法による面積計算は、特に複雑な形状の領域や解析的に積分が困難な場合に有効である。
    - 乱数を使用することで、従来の数値積分手法では難しい問題に対しても、近似的な解を効率的に求めることが可能となる。
  - draw now を用いた動画生成
- 二項分布の生成モデル
- Galton Board が知られている。MALTABでアニメーションを作成する。


#### ===== ライブスクリプト =====

| 項目 | リンク |
| -------------- | -------------- |
|(1) モンテカルロ法による面積計算 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Monte_Carlo_lec_21v1.mlx)|
| (3) コイン投げモデル | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=plot_distribution_lec_21v1.mlx) |
| (3) Galton Board シミュレーション | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=plot_distribution_lec_21v1.mlx) |




---

## 参考図書

- 今田正俊　「統計物理学」（丸善出版）
- 大沢文夫　「大沢流　手づくり統計力学」（名古屋大学出版会）
- 久保亮五　「統計力学」（共立出版）
- 田崎晴明　「統計力学　Ⅰ・Ⅱ」（培風館）
- 松下貢　「物理学講義　統計力学入門」（裳華房）
- [その他のreferences](refs.md)

---

## MATLABに関して

### 推奨のオンラインコース

- [MATLAB入門](https://matlabacademy.mathworks.com/jp/details/matlab-onramp/gettingstarted)
- [MATLAB基礎](https://matlabacademy.mathworks.com/jp/details/matlab-fundamentals/mlbe)

### 使用する製品
- MATLAB

## ライセンス

Copyright (C) 2023- Yoshihiro Yamazaki

ソフトウェアコードはMITライセンス(LICENCE)に従い、ドキュメンテーションや画像はCC-BY 4.0(LICENCE_CC_BY)に従う。



