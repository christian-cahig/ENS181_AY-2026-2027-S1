<!-- omit in toc -->
# Solutions to Quiz 02

- [Scenario 01](#scenario-01)
- [Scenario 02](#scenario-02)
- [Scenario 03](#scenario-03)
- [Scenario 04](#scenario-04)
- [Scenario 05](#scenario-05)
- [Scenario 06](#scenario-06)

## Scenario 01

The equation is nonlinear, non-homogeneous, and separable.

A suitable integrating factor is
$$\mu = y^{2} e^{y}$$
whence
$$u \left(x,y\right) = y^{2} e^{y} \sin x$$
Thus, the general solution is
$$y^{2} e^{y} \sin x = C$$

## Scenario 02

The equation is nonlinear, non-homogeneous, and non-separable.

A suitable integrating factor is
$$\mu = \left(x + 1 \right)^{-3}$$
whence
$$u \left(x,y\right) = -\frac{y^{2}}{\left(x + 1\right)^{2}} + 2\ln|x + 1| + \frac{4}{x + 1} + \frac{4}{\left(x + 1\right)^{2}}$$
Thus, the general solution is
$$-\frac{y^{2}}{\left(x + 1\right)^{2}} + 2\ln|x + 1| + \frac{4}{x + 1} + \frac{4}{\left(x + 1\right)^{2}} = C$$

## Scenario 03

The equation is nonlinear, homogeneous, and non-separable.

A suitable integrating factor is
$$\mu = x^{2}y$$
whence
$$u \left(x,y\right) = x^{3} y^{3} \left( x + y \right)$$
Thus, the general solution is
$$x^{3} y^{3} \left( x + y \right) = C$$

## Scenario 04

The equation is linear, exact, and non-separable.
The general solution is
$$tx - \frac{t}{\sqrt{1 + t^{2}}} = C$$
or, alternatively,
$$x\left(t\right) = \frac{C}{t} + \frac{t}{\sqrt{1 + t^{2}}}$$

## Scenario 05

The given equation is linear in $s$.

The "reduced" linear first-order equation is
$$t \dot{u} - 2u = t^{3}e^{t}$$
from which one can solve for $u\left(t\right)$.
Integrating $u\left(t\right)$ would then give $s\left(t\right)$.

The general solution is
$$s\left(t\right) = \left(t^{2} - 2t + 2\right)e^{t} + C_{1} t^{3} + C_{2}$$
The constants of integration $C_{1}$ and $C_{2}$ can be determined
using two conditions
(either
$s$-values at different $t$-values,
or
$s$- and $\dot{s}$values at one $t$-value).

## Scenario 06

The differential equation modelling the time rate of change is
$$\dot{w} = 2w = tw^{5}$$
which is a Bernoulli equation
and thus nonlinear in $w$.
This can be reduced to a linear equation by the substitution
$u = w^{-4}$.
The general solution is
$$w\left(t\right) = \frac{2}{\left(1 - 8t + Ce^{-8t}\right)^{0.25}}$$

Question 2 translates to
determining $w\left(-0.5\right)$
if $w\left(0\right) = 2$.
Similarly, Question 3 means
determining $w\left(-0.75\right)$
if $w\left(0\right) = 1$.
