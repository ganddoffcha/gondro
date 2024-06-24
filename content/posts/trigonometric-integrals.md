+++
title = 'Trigonometric Integrals'
date = 2024-06-24T19:54:40+08:00
tags = ['calculus','integrals']
summary = 'Evaluating a few trigo integrals by defining sine and cosine to be complex function.'
+++

# Identities

Define $$\begin{cases}
    \sin z=\frac{e^{iz}-e^{-iz}}{2i}\\
    \cos z=\frac{e^{iz}+e^{-iz}}2\\
    \tan x=\frac{\sin x}{\cos x}\\
    \sec x=\frac{1}{\cos x}\\
    \csc x=\frac{1}{\sin x}\\
    \cot x=\frac{\cos x}{\sin x}\\
\end{cases}$$

## Pythagorean Identity

$$\begin{aligned}
    \sin^2z+\cos^2z
    &=\left(\frac{e^{iz}-e^{-iz}}{2i}\right)^2+\left(\frac{e^{iz}+e^{-iz}}2\right)^2\\
    &=\frac{e^{2iz}-2+e^{-2iz}}{-4}+\frac{e^{2iz}+2+e^{-2iz}}4\\
    &=\frac{-e^{2iz}+2-e^{-2iz}}4+\frac{e^{2iz}+2+e^{-2iz}}4\\
    &=\frac44\\
    &=1
\end{aligned}$$ $$\begin{aligned}
    \sin^2x+\cos^2x&=1\\
    1+\cot^2x&=\csc^2x\\
    \tan^2x+1&=\sec^2x\\
\end{aligned}$$

## Euler's Formula

$$\begin{aligned}
    \cos\theta+i\sin\theta
    &=\frac{e^{i\theta}+e^{-i\theta}}2+i\frac{e^{i\theta}-e^{-i\theta}}{2i}\\
    &=\frac{e^{i\theta}+e^{-i\theta}}2+\frac{e^{i\theta}-e^{-i\theta}}2\\
    &=\frac{2e^{i\theta}}2\\
    &=e^{i\theta}
\end{aligned}$$

## Double Angle Identity

$$\begin{aligned}
    &\cos2\theta+i\sin2\theta\\
    &=e^{i2\theta}\\
    &=\left(e^{i\theta}\right)^2\\
    &=(\cos\theta+i\sin\theta)^2\\
    &=\cos^2\theta+2i\cos\theta\sin\theta+i^2\sin^2\theta\\
    &=\cos^2\theta-\sin^2\theta+i2\cos\theta\sin\theta
\end{aligned}
\implies
\begin{cases}
    \cos2\theta=\cos^2\theta-\sin^2\theta\\
    \sin2\theta=2\cos\theta\sin\theta
\end{cases}$$

# Derivatives

## Derivative of $\sin x$

$$\begin{aligned}
    \sin^\prime x&=\left(\frac{e^{ix}-e^{-ix}}{2i}\right)^\prime\\
    &=\frac1{2i}\left(e^{ix}-e^{-ix}\right)^\prime\\
    &=\frac1{2i}\left(ie^{ix}+ie^{-ix}\right)\\
    &=\frac i{2i}\left(e^{ix}+e^{-ix}\right)\\
    &=\frac{e^{ix}+e^{-ix}}2\\
    &=\cos x
\end{aligned}$$

## Derivative of $\cos x$

$$\begin{aligned}
    \cos^\prime x&=\left(\frac{e^{ix}+e^{-ix}}2\right)^\prime\\
    &=\frac12\left(e^{ix}+e^{-ix}\right)^\prime\\
    &=\frac12\left(ie^{ix}-ie^{-ix}\right)\\
    &=\frac i2\left(e^{ix}-e^{-ix}\right)\\
    &=\frac{-1}{2i}\left(e^{ix}-e^{-ix}\right)\\
    &=-\frac{e^{ix}-e^{-ix}}{2i}\\
    &=-\sin x
\end{aligned}$$

## Derivavtive of $\tan x$

$$\begin{aligned}
    \tan^\prime x&=\left(\frac{\sin x}{\cos x}\right)^\prime\\
    &=\frac{\cos x\sin^\prime x-\sin x\cos^\prime x}{(\cos x)^2}\\
    &=\frac{\cos x\cos x+\sin x\sin x}{\cos^2x}\\
    &=\frac{\cos^2x+\sin^2x}{\cos^2x}\\
    &=1+\tan^2x\\
    &=\sec^2x
\end{aligned}$$

## Derivavtive of $\sec x$

$$\begin{aligned}
    \sec^\prime x&=\left((\cos x)^{-1}\right)^\prime\\
    &=-(\cos x)^{-2}\cos^\prime x\\
    &=-(\sec^2 x)(-\sin x)\\
    &=\sec x\tan x\\
\end{aligned}$$

## Derivavtive of $\csc x$

$$\begin{aligned}
    \csc^\prime x&=\left((\sin x)^{-1}\right)^\prime\\
    &=-(\sin x)^{-2}\sin^\prime x\\
    &=-(\csc^2 x)\cos x\\
    &=-\csc x\cot x\\
\end{aligned}$$

## Derivavtive of $\cot x$

$$\begin{aligned}
    \cot^\prime x&=\left((\tan x)^{-1}\right)^\prime\\
    &=-(\tan x)^{-2}\tan^\prime x\\
    &=-(\cot^2x)\sec^2x\\
    &=-\csc^2x
\end{aligned}$$

# Integrals

## $\int_{}^{}{\frac 1{x^2+1}}\,\mathrm dx$

$$\begin{aligned}
    \int_{}^{}{\frac 1{x^2+1}}\,\mathrm dx
    &=\int_{}^{}{\frac{\sec^2\theta}{\tan^2\theta+1}}\,\mathrm d\theta\\
    &=\int_{}^{}{\frac{\sec^2\theta}{\sec^2\theta}}\,\mathrm d\theta\\
    &=\int_{}^{}{}\,\mathrm d\theta\\
    &=\theta+C\\
    &=\tan^{-1}x+C\\
\end{aligned}$$

## $\int_{}^{}{\frac 1{1-x^2}}\,\mathrm dx$

$$\begin{aligned}
    \int_{}^{}{\frac 1{1-x^2}}\,\mathrm dx
    &=\int_{}^{}{\frac 1{(1+x)(1-x)}}\,\mathrm dx\\
    &=\int_{}^{}{\left(\frac{1/2}{1+x}+\frac{1/2}{1-x}\right)}\,\mathrm dx\\
    &=\frac{\ln|1+x|+\ln|1-x|}2+C\\
    &=\frac12\ln\left|\frac{1+x}{1-x}\right|+C\\
\end{aligned}$$

## $\int_{}^{}{\sec x}\,\mathrm dx$

$$\begin{aligned}
    \int_{}^{}{\sec x}\,\mathrm dx
    &=\int_{}^{}{\frac 1{\cos x}}\,\mathrm dx\\
    &=\int_{}^{}{\frac{\cos x}{\cos^2x}}\,\mathrm dx\\
    &=\int_{}^{}{\frac{\cos x}{1-\sin^2x}}\,\mathrm dx\\
    &=\int_{}^{}{\frac 1{1-u^2}}\,\mathrm du\\
    &=\frac12\ln\left|\frac{1+u}{1-u}\right|+C\\
    &=\frac12\ln\left|\frac{(1+u)(1+u)}{(1-u)(1+u)}\right|+C\\
    &=\frac12\ln\left|\frac{(1+u)^2}{1-u^2}\right|+C\\
    &=\frac12\ln\left|\frac{(1+\sin x)^2}{\cos^2x}\right|+C\\
    &=\frac12\ln\left|\frac{1+\sin x}{\cos x}\right|^2+C\\
    &=\ln|\sec x+\tan x|+C\\
\end{aligned}$$

## $\int_{}^{}{\sin^2x}\,\mathrm dx$

$$\begin{aligned}
    \cos2x&=\cos^2x-\sin^2x\\
    \cos2x-1&=\cos^2x-\sin^2x-\sin^2x-\cos^2x\\
    \cos2x-1&=-2\sin^2x\\
    \sin^2x&=\frac{1-\cos2x}2\\
\end{aligned}$$ $$\begin{aligned}
    \int_{}^{}{\sin^2x}\,\mathrm dx
    &=\frac12\int_{}^{}{(1-\cos 2x)}\,\mathrm dx\\
    &=\frac12\left(x-\frac{\sin2x}2\right)+C\\
    &=\frac x2-\frac{\sin2x}4+C
\end{aligned}$$

## $\int_{}^{}{\cos^2x}\,\mathrm dx$

$$\cos^2x=1-\sin^2x=\frac22-\frac{1-\cos2x}2=\frac{1+\cos2x}2\\
$$ $$\begin{aligned}
    \int_{}^{}{\cos^2x}\,\mathrm dx
    &=\frac12\int_{}^{}{(1+\cos 2x)}\,\mathrm dx\\
    &=\frac12\left(x+\frac{\sin2x}2\right)+C\\
    &=\frac x2+\frac{\sin2x}4+C
\end{aligned}$$

## $\int_{}^{}{\sqrt{1-x^2}}\,\mathrm dx$

$$\begin{aligned}
    \int_{}^{}{\sqrt{1-x^2}}\,\mathrm dx
    &=\int_{}^{}{\sqrt{1-(\sin\theta)^2}\cdot\cos\theta}\,\mathrm d\theta\\
    &=\int_{\alpha}^{\beta}{\sqrt{\sin^2\theta+\cos^2\theta-\sin^2\theta}\cdot\cos\theta}\,\mathrm d\theta\\
    &=\int_{}^{}{\sqrt{\cos^2\theta}\cdot\cos\theta}\,\mathrm d\theta\\
    &=\int_{}^{}{\cos\theta\cos\theta}\,\mathrm d\theta\\
    &=\int_{}^{}{\cos^2\theta}\,\mathrm d\theta\\
    &=\frac{\theta}2+\frac{\sin2\theta}4+C\\
    &=\frac{\theta}2+\frac{2\cos\theta\sin\theta}4+C\\
    &=\frac12\left(\sin^{-1}x+x\sqrt{1-x^2}\right)+C\\
\end{aligned}$$
