<!-- omit in toc -->
# Solutions to Quiz 03

*Last updated 28 September 2026*

For the computations,
see [`oqz-03-soln.ipynb`](./oqz-03-soln.ipynb).

- [Part I](#part-i)
  - [Scenario 01](#scenario-01)
  - [Scenario 02](#scenario-02)
- [Part II](#part-ii)
  - [Scenario 03](#scenario-03)
  - [Scenario 04](#scenario-04)

## Part I

Infer from the given information that:

- $\dot{Q}_{c} = 100$
- $\dot{Q}_{s} = \dot{Q}_{h} = 0$
- $T_{a} \left(t\right) = 25$
- $T_{c} \left(0\right) = T_{s} \left(0\right) = T_{h} \left(0\right) = 25$

### Scenario 01

The ODE is

$$ \frac{dT_{c}}{dt} = \frac{\dot{Q_{c}}}{C_{c}}
+ \frac{1}{R_{c,s} C_{c}} \left(T_{s} - T_{c}\right)$$

or, in standard form,

$$ \frac{dT_{c}}{dt} + \frac{1}{R_{c,s} C_{c}} T_{c} = \frac{\dot{Q_{c}}}{C_{c}} + \frac{T_{s}}{R_{c,s} C_{c}} $$

### Scenario 02

The ODE is

$$ \frac{dT_{h}}{dt} = \frac{\dot{Q_{h}}}{C_{h}} + \frac{1}{R_{s,h} C_{h}} \left(T_{s} - T_{h}\right) + \frac{1}{R_{h,a} C_{h}} \left(T_{a} - T_{h}\right) $$

which simplifies to the standard form

$$ \frac{dT_{h}}{dt} + \frac{1}{C_{h}} \left(\frac{1}{R_{s,h}} + \frac{1}{R_{h,a}}\right) T_{c} = \frac{1}{C_{h}} \left(\frac{T_s}{R_{s,h}} + \frac{T_{a}}{R_{h,a}}\right) $$

## Part II

### Scenario 03

By KVL,

$$v_{E} + 2 i_{E} - 1 = 0$$

Since $v_{E}$ and $i_{E}$ are capacitor voltage and current, respectively,
we have:

- $i_{E} = 0.001 \dot{v}_{E}$,
  and
- by continuity, $v_{E} \left(0\right) = 2$.

So the KVL equation becomes

$$v_{E} + 0.002 \dot{v}_{E} - 1 = 0$$

which is linear in $v_{E}$.
Eventually,

$$v_{E} \left(t\right) = 1 + \operatorname{exp}\left(-\frac{t}{0.002}\right)$$

$$ i_{E} \left(t\right) = -0.5 \operatorname{exp}\left(-\frac{t}{0.002}\right) $$

The voltage across the 1-ohm resistor is 1 V,
and, by Ohm's law, its current is 1 A.
By KCL,

$$i_{s} \left(t\right) = 1 + i_{E} \left(t\right) = 1 - 0.5 \operatorname{exp}\left(-\frac{t}{0.002}\right)$$

### Scenario 04

By KVL,

$$v_{E} + 2 i_{E}  - 1 = 0$$

Since $v_{E}$ and $i_{E}$ are now inductor voltage and current, respectively,
we have:

- $v_{E} = 0.001 \dot{i}_{E}$,
  and
- by continuity, $i_{E} \left(0\right) = 2$.

So the KVL equation becomes

$$0.001 \dot{i}_{E} + 2 i_{E} - 1 = 0$$

which is linear in $i_{E}$.
Eventually,

$$i_{E} \left(t\right) = 0.5 + 1.5 \operatorname{exp}\left(-\frac{t}{0.0005}\right)$$

$$v_{E} \left(t\right) = - 3 \operatorname{exp}\left(-\frac{t}{0.0005}\right)$$

The voltage across the 1-ohm resistor is 1 V,
and, by Ohm's law, its current is 1 A.
By KCL,

$$i_{s} \left(t\right) = 1 + i_{E} \left(t\right) = 1.5 + 1.5 \operatorname{exp}\left(-\frac{t}{0.0005}\right)$$
