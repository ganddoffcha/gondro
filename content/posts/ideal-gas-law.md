+++
title = 'Ideal Gas Law'
date = 2024-06-23T18:47:09+08:00
tags = ['kinetic particle theory']
+++

## Boyle's law

At constant temperature and number of particles, $$p\propto V^{-1}$$
where $p$ is the pressure of a gas, and $V$ is the volume of it.

## Charles's law

At constant pressure and number of particles, $$V\propto T$$ where $V$
is the volume of a gas, and $T$ is the temperature of it.

## Avogadro's law

At constant pressure and temperature of particles, $$V\propto N$$ where
$V$ is the pressure of a gas, and $N$ is the number of particles.

## Ideal gas law

Suppose we have ideal gas with pressure, volume, and temperature of
$p_1$, $V_1$, and $T_1$ respectively, with $N_1$ particles. Firstly,
only the pressure and volume is changed:
$$(p_1,V_1,N_1,T_1)\to(p_2,V_2,N_1,T_1)$$ By Boyle's law,
$$p_1V_1=p_2V_2$$ Secondly, only the volume and temperature is changed:
$$(p_2,V_2,N_1,T_1)\to(p_2,V_3,N_1,T_2)$$ By Charles's law,
$$V_2T_2=V_3T_1$$ Thirdly, only the volume and number of particles is
changed: $$(p_2,V_3,N_1,T_2)\to(p_2,V_4,N_2,T_2)$$ By Avogadro's law,
$$V_3N_2=V_4N_1$$ Now since $V_4$ can be changed to any value, let
$V_4=V_2$. Thus, $$V_3N_2=V_2N_1$$ $$\begin{aligned}
    p_1V_1&=p_2V_2\\
    p_1V_1T_2&=p_2V_2T_2\\
    p_1V_1T_2&=p_2V_3T_1\\
    p_1V_1N_2T_2&=p_2V_3N_2T_1\\
    p_1V_1N_2T_2&=p_2V_2N_1T_1\\
    \frac{p_1V_1}{N_1T_1}&=\frac{p_2V_2}{N_2T_2}\\
    \frac{pV}{NT}&=k_B\\
\end{aligned}$$ Given an ideal gas, $$\boxed{pV=Nk_BT}$$ where $p$, $V$,
and $T$ are the pressure, volume, and temperature of the gas
respectively, with $N$ being the number of particles, and
$$\boxed{k_B=\pu{1.38E-23 J K-1}}$$ being the Boltzmann
constant.
