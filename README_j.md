# 統計力学

## 全体の説明

- このカリキュラムモジュールには、統計力学の基礎を理解するための対話型のMATLAB®ライブスクリプトが含まれています。
- 以下のトピックスが含まれています。
  - 確率と統計
  - カノニカル分布
  - 準備中
- 内容は随時追加されます。 


### 前提となる知識
- 熱力学
- 古典力学・量子力学の基礎

### 対象学年
- 大学３年・４年


### 学習目標
- マクロな系の平衡状態における熱力学量を、分子や原子など系を構成するミクロな粒子の状態に対する分布の平均値・偏差として導出する手法 （平衡統計力学）を学ぶ。
- 物理学を体系的に学び、現代物理学の基礎的知識の習得する。
- ボルツマンの関係式・カノニカル分布・グランドカノニカル分布の意味を理解し、具体的な問題に適用して種々の熱力学的量が計算できるようになることを目標とする。



---
## 各ライブスクリプトの概要

### 1. 準備

#### 1.1 確率と統計

(1) 乱数生成 [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/random_number_lec_21v1.mlx)

- 説明

- ライブスクリプト：　[random_number_lec_21v1.mlx](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/random_number_lec_21v1.mlx) 




(2) 確率分布 plot_distribution_lec_21v1.mlx [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=plot_distribution_lec_21v1.mlx)

- 説明

- binomial_distribution_lec.mlx
  - [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=binomial_distribution_lec.mlx)


#### 1.2 数学的準備

(1) スターリングの公式について [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Stirling_formula_lec.mlx)

- Stirlingの公式： $\ln N! \approx N\ln N - N$に関する説明
- 学習ポイント
  - 公式の証明を視覚的に理解する
  - $N$が大きくなるにつれて、近似の精度がどのように変化するかを把握する
<img width="300" src="./Images/Stirling_1.png" style="margin:10px" >
- ライブスクリプト： Stirling_formula_lec.mlx


(2) 和と積分
- sum-int.mlx


#### 1.3 その他

- draw_graphs_lec.mlx



---
### 2. カノニカル分布

- Coin_canonical.mlx
  - [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Coin_canonical.mlx)


#### micro-canonical distribution

- coin_exchange_21v1.mlx
- coin_exchange_lec_21v1.mlx

---
### 3. 量子統計

準備中


---
### 4. 状態の遷移とゆらぎ

- Monte_Carlo_lec_21v1.mlx
- Detailed_balance_21v1.mlx



---
### 5. 相互作用と相転移


- Ising_heatbath_1.mlapp

---
### 6. ゆらぎと緩和

- random_walk_lec_21v1.mlx


---
### 7. 臨界現象

- power_law_211228.mlx


---
## MATLABに関して

### 推奨のオンラインコース

- [MATLAB入門](https://matlabacademy.mathworks.com/jp/details/matlab-onramp/gettingstarted)
- [MATLAB基礎](https://matlabacademy.mathworks.com/jp/details/matlab-fundamentals/mlbe)

### 使用する製品
- MATLAB

## ライセンス
- LICENSE ファイルを参照


