---
title: 회귀분석 - 1 단순회귀분석
use_math: true
---

### 단순회귀분석
회귀분석이란 ?
변수간 관계를 알기 위한 방법이다.

다음은 단순회귀모형의 식으로 $$x$$가 변할 때 $$y$$가 얼마나 변하는 지 나타내는 직선이다..

$$  y = \beta_0+\beta_1x + \epsilon $$

$$x$$  -독립변수

$$y$$ - 반응변수

$$\beta_0$$ - 절편

$$\beta_1$$ - 기울기

$$\epsilon$$ - 오차 $$\epsilon_i$$ ~ $$N(0,\sigma^2)$$

회귀분석의 가정으로 $$x$$의 값과 관계 없이 $$y$$값은 일정하다(등분산성)는 것과, 오차의 측정값은 독립이라는 것이 있다. 

$$y \sim N(\beta _0 + \beta _1 x, \sigma ^2$$

$$\epsilon \sim N(0,\sigma ^2)$$

가 성립하게 되는 이유가 회귀분석의 가정 때문이다.

회귀 직선의 식은 다음과 같다.

$$ \hat{y} = b_0 + b_1 x $$

여기서 $$b_0, b_1, \hat{y}$$ 는 각각 $$\beta_0, \beta_1, y$$의 추정값이다.

이 직선이 데이터에 얼마나 적합한지는 어떻게 판단해야 할까?

### 최소제곱법

$$y_i = \beta_0 + \beta_1 x_1 + \epsilon_i$$ 일때 오차 제곱합 $$S$$를

$$S = \Sigma \epsilon_i = \Sigma(y_i-\beta_0-\beta_1 x_i)^2$$

라고 하면, $$S$$를 최소화시키는 $$B_0$$과 $$B_1$$을 구해야한다.

이를 위해 $$B_0, B_1$$에 대해 $$S$$를 각각 편미분하면

$$\frac{\partial S}{\partial \beta_0} = -2\Sigma(y_i-\beta_0-\beta_1 x_i)$$

$$\frac{\partial S}{\partial \beta_1} = -2\Sigma x_i(y_i-\beta_0-\beta_1 x_i)$$

두 식의 값을 0으로 하는 값을 $$b_0, b_1$$이라고 하면,

$$b_0n + b_1\Sigma x_i = \Sigma y_i$$

$$b_0\Sigma x_i + b_1 \Sigma x_i^2 = \Sigma x_i y_i$$

위 식을 정규방정식이라고 한다.  이 연립방정식의 해를 풀면

$$ b_0 = \frac{\Sigma y_i}{n} - b_1 \frac{\Sigma x_i}{n} = y_bar - b_1 \bar{x}$$

$$b_1 = \frac{\Sigma x_i y_i - \frac {\Sigma x_i y_i}{n}} {\Sigma x^2_i - \frac{\Sigma (x_i)^2}{n}} = \frac{(x_i-\bar{x})(y_i-\bar{y})}{\Sigma (x_i-\bar{x})^2} = \frac{S_{xy}}{S_{xx}}$$

여기서 

$$S_{xx} = \Sigma(x_i-\bar{x})^2$$

$$S_{yy} = \Sigma(y_i-\bar{y})^2$$

$$S_{xy} = \Sigma(x_i-\bar{x})(y_i-\bar{y})$$
