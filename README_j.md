# 統計力学

## 全体の説明

- このカリキュラムモジュールには、統計力学の基礎を理解するための対話型のMATLAB®ライブスクリプトが含まれています。
- 内容は随時、追加・更新されます。
- 2023年12月1日現在
  - 確率と統計
  - カノニカル分布

### 前提となる知識

- 熱力学・古典力学・量子力学
  - 特に、エネルギーに関連する内容

### 対象学年

- 大学３年・４年

### 学習目標

- マクロな系の平衡状態における熱力学量を、分子や原子など系を構成するミクロな粒子の状態に対する分布の平均値・偏差として導出する手法 （平衡統計力学）を学ぶ。
- ボルツマンの関係式・カノニカル分布の意味を理解し、具体的な問題に適用して種々の熱力学的量が計算できるようになることを目標とする。

### 学習の流れ

- 各ライブスクリプトにある
  1. 理論的背景を確認する
  2. コードを実行する
  3. 演習に取り組む

---

## 1. 準備（乱数・確率・分布・統計）


### 1.1 乱数生成と分布の描画

#### ＊＊＊　概要　＊＊＊

乱数（random number）は、ランダム（無規則に）選択された数値を指す。計算機上で完全なランダム性を実現することは困難であるため、線形合同法やメルセンヌツイスター法といった擬似乱数として知られるアルゴリズムに基づいた数値が使用される。
乱数は等確率に生成されるだけでなく、特定の確率分布に従うように生成される場合もある。例えば、1次元ランダムウォークの結果として得られる位置を再現したい場合には、二項分布または正規分布に従った乱数を生成することになる。このように、特定の確率分布に従う乱数を生成することで、物理現象の数値的模擬が可能となる。
MATLABには一様乱数や正規乱数を生成する関数が標準で提供されており、これらを利用して乱数列を生成することができる。また、生成された乱数列の頻度分布を可視化するために、ヒストグラムを描画する関数を利用することができる。

#### ＊＊＊　ライブスクリプト　＊＊＊

| 項目 | リンク |
| -------------- | -------------- |
| (1) 乱数生成  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/random_number_lec_21v1.mlx)  |
| (2) 乱数列の頻度分布とフィッティング | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=plot_distribution_lec_21v1.mlx) |


---

### 1.2 確率分布

#### ＊＊＊　概要　＊＊＊

ここでは、MATLABを用いて、２項分布と正規分布を学ぶ

#### ＊＊＊　ライブスクリプト　＊＊＊

| 項目 | リンク |
| -------------- | -------------- |
| (1) ２講分布と正規分布 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=binomial_distribution_lec.mlx) |
| (2) 和と積分について | 準備中 |


---

### 1.3 スターリングの公式

#### ＊＊＊　概要　＊＊＊

Stirlingの公式： $\ln N! \approx N\ln N - N$に関する説明

学習ポイント
  - 公式の証明を視覚的に理解する
  - $N$が大きくなるにつれて、近似の精度がどのように変化するかを把握する
<img width="300" src="./Images/Stirling_1.png" style="margin:10px" >


#### ＊＊＊　ライブスクリプト　＊＊＊


| 項目 | リンク |
| -------------- | -------------- |
|(1) スターリングの公式 | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Stirling_formula_lec.mlx)|

---

## 2. カノニカル分布

- Coin_canonical.mlx
  - [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Coin_canonical.mlx)


### micro-canonical distribution

- coin_exchange_21v1.mlx
- coin_exchange_lec_21v1.mlx


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



