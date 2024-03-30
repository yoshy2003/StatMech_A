# 平衡状態の統計力学

## 全体の説明

### 概要

- 統計物理学入門として、**平衡状態の統計力学**を学ぶ。
  - 全体の構想は、平衡状態の統計力学・平衡ゆらぎの関わる統計物理学・非平衡統計物理学・複雑系科学
- このリポジトリには、統計力学の基礎を理解するためのMATLAB®ライブスクリプトが含まれている。
- 統計力学を初めて学ぶ学生を対象に、MATLABを用いた数値計算・数値シミュレーションを通して、統計力学の基本的な概念や理論の背景を理解することを目的とする。
  - 特に、初学者が統計物理学の世界にスムーズに入門できるような直感的な説明を提供する。
- 数値計算・数値シミュレーションを用いた、座学（講義ノート）で学ぶ統計力学に対する相補的な位置づけとなっている。
- 内容は随時更新されます。


### 学習目標

- マクロな階層とミクロな階層とを結びつける基本的な概念を理解する
- 統計力学を通して現象を束ねて理解する
  - 全く異なる現象を単純なモデルによって結びつけることによって統一して理解できる感覚を身につける
- 乱数に基づく数値シミュレーションを通して、統計力学の基礎を学ぶ
- 講義ノートを用いて理論の理解を深め、ライブスクリプトを用いて現象をモデル化し、数値シミュレーションできるようになる


### 講義ノート

- [draft版・随時更新中](https://waseda.box.com/s/xozrws2nlrkb0iuim7ylyg5xiv3fqwmh)


### ライブスクリプト集

- 第Ⅰ部 <a href="#part01">基礎</a>
  - 第１章 確率分布
  - 第２章 カノニカル分布
  - 第３章 ミクロカノニカル分布とボルツマンの関係式
  - 第４章 グランドカノニカル分布
- 第Ⅱ部 <a href="#part02">ミクロな状態のゆらぎと遷移</a>
  - 第５章 平衡状態のゆらぎ
  - 第６章 ミクロな状態の遷移
- 第Ⅲ部 <a href="#part03">カノニカル分布の応用</a>【準備中】
  - 第７章 外場がはたらく系
  - 第８章 調和振動子系
  - 第９章 粒子数分布
- 第Ⅳ部 <a href="#part04">量子統計</a>【準備中】
  - 第１０章 量子統計の基礎
  - 第１１章 量子多体系
  - 第１２章 フェルミ自由粒子系
  - 第１３章 ボーズ自由粒子系
- 第Ⅴ部 <a href="#part05">付録</a>
  - 第１４章 物理数学
  <!-- - A. 数学的準備
  - B. その他（関連内容） -->

（2024年03月現在。内容は随時、追加・更新されます。）

### 学習の流れ

- 講義テキストを読む
- ライブスクリプトの内容に従って、コードを実行する

### 前提となる知識

- 熱力学
- 古典力学・量子力学の特に、エネルギーに関連する内容

### 対象学年・対象者

- 大学３年・４年（＋意欲的な高校生～大学２年生）
- 物理系の学生に限らず、より一般に、統計力学に興味のある方々

---

## <p id="part01">第Ⅰ部 基礎</p>


<!-- ### ===== 概要 =====

- ライブスクリプトに合わせた概要に

### ===== ライブスクリプト ===== -->

| 章.節 | 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| --- | -------------- | -------------- | -------------- |
| 1.1 | (1) [経験的確率と大数の法則](Livescripts/empirical_probability_statA_240205.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/empirical_probability_statA_240205.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/empirical_probability_statA_240205.mlx) |
| 1.1 | (2) [基本的な確率分布](Livescripts/probability_distribution_statA_240205.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/probability_distribution_statA_240205.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/probabilityl_distributions_lec_v23.mlx) |
| 1.2 | (3) [コイン投げ問題と近似の確認](Livescripts/coin_toss_statA_240229.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_toss_statA_240229.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_toss_statA_240229.mlx) |
| 1.2 | (4) [Galton board: 二項分布と正規分布](Livescripts/galton_board_statA_240304.md)  | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/galton_board_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/galton_board_statA_240304.mlx)|| 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/binomial_distribution_lec.mlx) |
| 1.2 | (5) [中心極限定理の確認](Livescripts/central_limit_theorem_statA_240205.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/central_limit_theorem_statA_240205.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/central_limit_theorem_statA_240205.mlx) |
| 2.1 | (6) [コイン分配モデルとカノニカル分布](Livescripts/coin_canonical_statA_240304.md)  | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_canonical_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_canonical_statA_240304.mlx)|
| 3.1 | (7) [コイン交換モデルと平衡状態](Livescripts/coin_exchange_statA_240304.md)  | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_exchange_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_exchange_statA_240304.mlx)|



---

## <p id="part02">第２部 ミクロな状態のゆらぎと遷移</p>

<!-- ### ===== 概要 =====

- ライブスクリプトに合わせた概要に

#### ===== ライブスクリプト ===== -->

| 章.節 | 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| --- | -------------- | -------------- | -------------- |
| 6.1 | (1) [コイン交換モデルの指数緩和](Livescripts/coin_exchange_2_statA_240304.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_exchange_2_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_exchange_2_statA_240304.mlx)|
| 6.2 | (2)  [1次元自由粒子系：詳細つりあいによる平衡状態の再現](Livescripts/detailed_balance_statA_240304.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/detailed_balance_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/detailed_balance_statA_240304.mlx)|


---

## 第３部 カノニカル分布の応用【準備中】

<!-- ### ===== 概要 =====

- ライブスクリプトに合わせた概要に

#### ===== ライブスクリプト ===== -->

| 章.節 | 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| --- | -------------- | -------------- | -------------- |
| *** | *** | *** | *** |


---

## 第４部 量子統計【準備中】

<!-- ### ===== 概要 =====

- ライブスクリプトに合わせた概要に

#### ===== ライブスクリプト ===== -->

| 章.節 | 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| --- | -------------- | -------------- | -------------- |
| *** | *** | *** | *** |


---

## <p id="part05">第５部 付録</p>


<!-- ### ===== 概要 =====

- ライブスクリプトに合わせた概要に

#### ===== ライブスクリプト ===== -->

| 章.節 | 項目(markdownによるレビュー) | Livescript | MATLAB Online での実行 |
| --- | -------------- | -------------- | -------------- |
| 14.4 |(1) [スターリングの公式：証明と近似精度](Livescripts/Stirling_formula_statA_240207.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/Stirling_formula_statA_240207.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Stirling_formula_statA_240207.mlx)|
<!-- | *** | (1) [離散分布に対する近似的な連続表現の妥当性](Livescripts/approx_dis_con.md) | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/approx_dis_con.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/approx_dis_con.mlx) |
| *** | (3) ランダムウォークと拡散  | 準備中 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/random_walk_lec_21v1.mlx)  |
| *** |(4) モンテカルロ法による面積計算 | *** | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Monte_Carlo_lec_21v1.mlx)|
| *** |(5) イジングモデル | *** | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Monte_Carlo_lec_21v1.mlx)|
| *** | (1) [一様乱数の生成と頻度分布の描画](Livescripts/uniform_random_number_histogram_lec_23.md)  | [ダウンロード](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/uniform_random_number_histogram_lec_23.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/uniform_random_number_histogram_lec_23.mlx)  | -->


---

## 参考図書

- 今田正俊　「統計物理学」（丸善出版）
- 大沢文夫　「大沢流　手づくり統計力学」（名古屋大学出版会）
- 久保亮五　「統計力学」（共立出版）
- 田崎晴明　「統計力学　Ⅰ・Ⅱ」（培風館）
- 松下貢　　「物理学講義　統計力学入門」（裳華房）
- 小田垣孝　「統計力学」（裳華房）
- ファインマン　「ファインマン 統計力学」（丸善出版）


<!-- - [その他のreferences](refs.md) -->

---

## MATLABに関して

### 推奨のオンラインコース

- [MATLAB入門](https://matlabacademy.mathworks.com/jp/details/matlab-onramp/gettingstarted)
- [MATLAB基礎](https://matlabacademy.mathworks.com/jp/details/matlab-fundamentals/mlbe)

### 使用する製品
- MATLAB
- Statistics and Machine Learning Toolbox

## ライセンス

Copyright (C) 2023- Yoshihiro Yamazaki

ソフトウェアコードはMITライセンス(LICENCE)に従い、ドキュメンテーションや画像はCC-BY 4.0(LICENCE_CC_BY)に従う。



