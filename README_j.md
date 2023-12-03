# 統計力学

## 全体の説明

- このカリキュラムモジュールには、統計力学の基礎を理解するための対話型のMATLAB®ライブスクリプトが含まれています。
- 内容は随時、追加・更新されます。
- 目次（2023年12月1日現在）
  1. 準備（乱数・確率・分布・統計）
      - 乱数生成と分布の描画
      - 確率分布
      - スターリングの公式
  2. カノニカル分布
      - コイン分配モデル
      - コイン交換モデル

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
  3. 演習に取り組む（理解度確認）

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

### 2.1 コイン分配モデル

#### ＊＊＊　概要　＊＊＊

カノニカル分布を理解するために、コインの分配モデルを用いた系の定常状態に着目しよう。
まず、$M$人が$N$個のコインをやりとりする状況を想定する。
ここでのコイン交換ルールは、$M$人の中からランダムに2人を選び、コインを持つ者から持たない者へコインを一つ渡すというものである。
このプロセスを繰り返すことによって、特定の人が持つコインの枚数の分布がどのように形成されるかを考える。

なお物理的には、このコイン分配モデルはエネルギー量子の交換と解釈することができる。
つまり、系全体を$M$個の部分系に分け、各部分系がコイン（エネルギー量子）を所持していると考えるわけである。
いま、全体系のエネルギーを$A$、エネルギーの最小単位を$\varepsilon$とし、全体系に含まれる単位エネルギーの総数を$N$とする$(N = A / \varepsilon)$。

このコイン分配モデルで、ある部分系（特定の人）が所持するコイン（エネルギー量子）の枚数分布を問題としよう。
物理的には、$N$個のエネルギー量子をランダムに交換した際に、一つの部分系に分配される単位エネルギーの数 $(E/\varepsilon = \eta)$ の確率分布$p(\eta)$を求める問題に相当する。
そしてこの問題は、「系」と「環境」との間でエネルギー交換が行われる際に、「系」のエネルギーが$E$となる確率$p(E)$を求める問いとして再定義することができる。

実際にこのコイン分配のルールを適用すると、コイン（エネルギー量子）の枚数のばらつきが増え、少ない枚数を持つ人の数が多くなる傾向が観察されます。
これは、コイン交換（エネルギー量子の交換）がランダムに行われるため、所持するコインの枚数が少ない状態が出現しやすくなることを意味します。
これはミクロな状態が同じ確率で出現するという等重率の原理に対応しており、最終的なコイン分布（エネルギー分布）は指数分布となります。

#### ＊＊＊　ライブスクリプト　＊＊＊

| 項目 | リンク |
| -------------- | -------------- |
| (1) コイン分配モデルとカノニカル分布  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Coin_canonical.mlx)|

---

### 2.1 コイン交換モデル

#### ＊＊＊　概要　＊＊＊

このセクションでは、ボルツマンの関係式の物理的意味と熱力学との関連を、コイン交換モデルを用いて説明する。
コイン交換モデルでは、2つの系AとBが存在し、それぞれの系にあるコインを交換するプロセスを考慮する。
物理的には、この設定は2つの系AとBが熱的に接触し、エネルギーをやり取りしている状況に相当する。
このエネルギー交換は、ランダムなコイン交換でモデル化されている。
初期状態では、系Aのコインは全て表でエネルギーが $+N$、系Bのコインは全て裏でエネルギーが $-N$となっている。
この状態から、それぞれの系からランダムにコインを選び、得点を交換していき、コイン交換を繰り返すと、各系のエネルギーは急速に0に近づき、その後は0の周りでランダムに揺らぐことが分かる。
なお、熱力学的には、この交換モデルは、系全体のエネルギーが変化しない孤立系としてモデル化されている。
また、特にコイン枚数が大きい場合、マクロな状態変化はなめらかに見なせ、ランダムなミクロ状態変化にもかかわらず、マクロな状態変化を連続的に記述できることが示唆される。


#### ＊＊＊　ライブスクリプト　＊＊＊

| 項目 | リンク |
| -------------- | -------------- |
| (1) コイン交換モデルと平衡状態  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Coin_exchange_23.mlx)|
| (2) コイン交換モデルによる緩和過程  | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=coin_exchange_lec_21v1.mlx)|

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



