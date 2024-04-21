# Statistical Mechanics for Equilibrium States

Japanese version is [here](README.md).

## General Description

### Overview

- As an introduction to statistical physics, the course will cover **Statistical Mechanics of Equilibrium States**.
  - The overall concept is statistical mechanics of equilibrium states, statistical physics involving equilibrium fluctuations, non-equilibrium statistical physics, and complex systems science.
- The repository includes MATLAB® Live Scripts to help students understand the fundamentals of statistical mechanics.
- The goal is to provide students new to statistical mechanics with an understanding of the basic concepts and theoretical background of statistical mechanics through numerical calculations and numerical simulations using MATLAB.
  - In particular, it provides intuitive explanations to help beginners smoothly enter the world of statistical physics.

- The contents are positioned as complementary materials to statistical mechanics taught in classroom (lecture notes), using numerical calculations and numerical simulations.

- The contents will be updated as needed.


### Learning Objectives

- To understand the basic concepts that link the macroscopic hierarchy to the microscopic hierarchy
- To unify and understand phenomena through statistical mechanics
  - Develop a sense of unity and understanding by linking very different phenomena through simple models
- Learn the fundamentals of statistical mechanics through numerical simulations based on random numbers
- Deepen understanding of the theory using lecture notes and be able to model and numerically simulate phenomena using Live Scripts

### Lecture Notes (In Japanese)

- [draft(240309)](https://waseda.box.com/s/xozrws2nlrkb0iuim7ylyg5xiv3fqwmh)

### Collection of MATLAB Live Scripts
- Part I <a href="#part01">Fundamentals</a>
  - Chapter 1 Probability Distribution
  - Chapter 2: Canonical Distribution
  - Chapter 3 Microcanonical Distribution and Boltzmann's Relative Equation
  - Chapter 4 Grand Canonical Distribution
- Part II <a href="#part02">Fluctuations and Transitions of Microscopic States</a>.
  - Chapter 5 Fluctuations of equilibrium states
  - Chapter 6: Transitions of Microscopic States
- Part III <a href="#part03">Applications of canonical distributions</a> [in preparation]
  - Chapter 7 Systems with external fields
  - Chapter 8 Harmonic oscillator systems
  - Chapter 9 Particle number distribution
- Part IV <a href="#part04">Quantum Statistics</a>[in preparation]
  - Chapter 10 Basics of Quantum Statistics
  - Chapter 11 Quantum many-body systems
  - Chapter 12 Fermi free particle systems
  - Chapter 13 Bose Free Particle Systems
<!-- Part V <a href="#part05">Appendix</a>
  - A. Mathematical Preparation
  - B. Other (related content). -->

(As of Mar/2024. Contents will be added/updated as needed)

### How to use this contents

- Read the lecture Notes
- Execute the code based on instruction written in the each Live Script.

### Prerequisite Knowledge

- Thermodynamics
- Classical and quantum mechanics. In particular, content related to energy

### Target Grades and Target Audience

- University 3rd and 4th year students (Motivated high school students and 2nd year university students are also welcome)

- Not limited to physics students, but more generally, those interested in statistical mechanics.

---

## <p id="part01">Part I: Fundamentals</p>


<!-- ### ===== Overview =====

- will be updated later

### ===== Live Script ===== -->

| Section.Chapter | Content | Livescript Link| Open with MATLAB Online |
| --- | -------------- | -------------- | -------------- |
| 1.1 | (1) [Empirical Probability and the Law of Large Numbers](Livescripts/empirical_probability_statA_240205_en.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/empirical_probability_statA_240205_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/empirical_probability_statA_240205_en.mlx) |
| 1.1 | (2) [Fundamental probability distribution](Livescripts/probability_distribution_statA_240205_en.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/probability_distribution_statA_240205_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/probability_distribution_statA_240205_en.mlx) |
| 1.2 | (3) [Coin Toss Problem and Verification of Approximations](Livescripts/coin_toss_statA_240229_en.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_toss_statA_240229_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_toss_statA_240229_en.mlx) |
| 1.2 | (4) [Galton board: binomial and normal distributions](Livescripts/galton_board_statA_240304_en.md)  | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/galton_board_statA_240304_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/galton_board_statA_240304_en.mlx)|
| 1.2 | (5) [Central Limit Theorem](Livescripts/central_limit_theorem_statA_240205_en.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/central_limit_theorem_statA_240205_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/central_limit_theorem_statA_240205_en.mlx) |
| 2.1 | (6) [Coin distribution model and canonical distribution](Livescripts/coin_canonical_statA_240304_en.md)  | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_canonical_statA_240304_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_canonical_statA_240304_en.mlx)|
| 3.1 | (7) [Coin exchange model and equilibrium state](Livescripts/coin_exchange_statA_240304_en.md)  | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_exchange_statA_240304_en.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_exchange_statA_240304_en.mlx)|



---

## <p id="part02">Part 2: Fluctuations and Transitions of Microscopic States</p>

<!-- ### ===== Overview =====

- Will be updated later

#### ===== Live Script ===== -->

| Section.Chapter | Content | Livescript Link| Open with MATLAB Online |
| --- | -------------- | -------------- | -------------- |
| 6.1 | (1) [Exponential relaxation of the coin exchange model](Livescripts/coin_exchange_2_statA_240304.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/coin_exchange_2_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/coin_exchange_2_statA_240304.mlx)|
| 6.2 | (2)  [Free particile system in 1D：Reproduction of equilibrium state by detailed balance](Livescripts/detailed_balance_statA_240304.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/detailed_balance_statA_240304.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/detailed_balance_statA_240304.mlx)|


---

## Part 3: Applications of Canonical Distributions [in preparation]
<!-- ### ===== Overview =====

- will be updated later

### ===== Live Script ===== -->

| Section.Chapter | Content | Livescript Link| Open with MATLAB Online |
| --- | -------------- | -------------- | -------------- |
| *** | *** | *** | *** |


---

## Part 4: Quantum Statistics [in preparation]

<!-- ### ===== Overview =====

- will be updated later

### ===== Live Script ===== -->

| Section.Chapter | Content | Livescript Link| Open with MATLAB Online |
| --- | -------------- | -------------- | -------------- |
| *** | *** | *** | *** |




## Part 5: Appendix

<!-- ### ===== Overview =====

- will be updated later

### ===== Live Script ===== 

| Section.Chapter | Content | Livescript Link| Open with MATLAB Online |
| --- | -------------- | -------------- | -------------- |
| *** | (1) [Validity of Approximate Continuous Representation for Discrete Distributions](Livescripts/approx_dis_con.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/approx_dis_con.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/approx_dis_con.mlx) |
| *** |(2) [Stirling's Formula: Proof and Approximation Accuracy](Livescripts/Stirling_formula_statA_240207.md) | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/Stirling_formula_statA_240207.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Stirling_formula_statA_240207.mlx)|
| *** | (3) Random Walks and Diffusion  | In Preparation | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/random_walk_lec_21v1.mlx)  |
| *** |(4) Monte Carlo Methods and Area Estimates | *** | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Monte_Carlo_lec_21v1.mlx)|
| *** |(5) Ising Model | *** | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=Livescripts/Monte_Carlo_lec_21v1.mlx)|
| *** | (1) [Generating uniform random numbers and plotting frequency distributions](Livescripts/uniform_random_number_histogram_lec_23.md)  | [download](https://github.com/yoshy2003/StatMech_A/raw/main/Livescripts/uniform_random_number_histogram_lec_23.mlx) | [![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=yoshy2003/StatMech_A&file=/Livescripts/uniform_random_number_histogram_lec_23.mlx)  | -->


---

## References

- 今田正俊　「統計物理学」（丸善出版）
- 大沢文夫　「大沢流　手づくり統計力学」（名古屋大学出版会）
- 久保亮五　「統計力学」（共立出版）
- 田崎晴明　「統計力学　Ⅰ・Ⅱ」（培風館）
- 松下貢　「物理学講義　統計力学入門」（裳華房）

<!-- - [その他のreferences](refs.md) -->

---

## Related to MALTAB

### Recommended Online Courses

- [MATLAB Onramp](https://matlabacademy.mathworks.com/jp/details/matlab-onramp/gettingstarted)
- [MATLAB Fundamentals](https://matlabacademy.mathworks.com/jp/details/matlab-fundamentals/mlbe)

### Requires
- MATLAB
- Statistics and Machine Learning Toolbox

## License

Copyright (C) 2023- Yoshihiro Yamazaki

Software code is subject to the MIT License (LICENCE), and documentation and images are subject to CC-BY 4.0 (LICENCE_CC_BY).




