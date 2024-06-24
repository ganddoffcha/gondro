+++
title = '$(\mathbf{AB})^{\mathrm T}=\mathbf B^{\mathrm T}\mathbf A^{\mathrm T}$'
date = 2024-06-23T18:23:07+08:00
summary = 'Deriving a propety of matrix tranpose.'
+++

## Notation
$[\mathbf M]_{ij}$ denotes the entry at the $i^\text{th}$ row, $j^\text{th}$ column of matrix $\mathbf M$.

## Matrix Product and Transpose
The product between generic matrices $\mathbf X$ and $\mathbf Y$ can be written concisely as such:
$$
[\mathbf X\mathbf Y]_{ij}=\sum_{k=1}^n[\mathbf X]_{ik}[\mathbf Y]_{kj}
$$
Likewise, transpose of $\mathbf X$ is written as such:
$$
\left[\mathbf X^{\mathrm T}\right]_{ij}=[\mathbf X]_{ji}
$$

## Proving the Theorem
$$
\begin{aligned}
\left[(\mathbf A\mathbf B)^{\mathrm T}\right]_{ij}&=[\mathbf A\mathbf B]_{ji}\\
&=\sum_{k=1}^n[\mathbf A]_{jk}[\mathbf B]_{ki}\\
&=\sum_{k=1}^n[\mathbf B]_{ki}[\mathbf A]_{jk}\\
&=\sum_{k=1}^n\left[\mathbf B^{\mathrm T}\right]_{ik}\left[\mathbf A^{\mathrm T}\right]_{kj}\\
&=\left[\mathbf B^{\mathrm T}\mathbf A^{\mathrm T}\right]_{ij}\qquad\square
\end{aligned}
$$

## Extension
$$
\begin{aligned}
(\mathbf A_1\mathbf A_2\mathbf A_3\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N)^{\mathrm T}&=(\mathbf A_1(\mathbf A_2\mathbf A_3\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N))^{\mathrm T}\\
&=(\mathbf A_2\mathbf A_3\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N)^{\mathrm T}\mathbf A_1^{\mathrm T}\\
&=(\mathbf A_2(\mathbf A_3\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N))^{\mathrm T}\mathbf A_1^{\mathrm T}\\
&=(\mathbf A_3\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N)^{\mathrm T}\mathbf A_2^{\mathrm T}\mathbf A_1^{\mathrm T}\\
&=(\mathbf A_3(\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N))^{\mathrm T}\mathbf A_2^{\mathrm T}\mathbf A_1^{\mathrm T}\\
&=(\dots\mathbf A_{N-2}\mathbf A_{N-1}\mathbf A_N))^{\mathrm T}\mathbf A_3^{\mathrm T}\mathbf A_2^{\mathrm T}\mathbf A_1^{\mathrm T}\\
&=\cdots\\
&=(\mathbf A_{N-1}\mathbf A_N)^{\mathrm T}\mathbf A_{N-2}^{\mathrm T}\dots\mathbf A_3^{\mathrm T}\mathbf A_2^{\mathrm T}\mathbf A_1^{\mathrm T}\\
&=\mathbf A_N^{\mathrm T}\mathbf A_{N-2}^{\mathrm T}\mathbf A_{N-1}^{\mathrm T}\dots\mathbf A_3^{\mathrm T}\mathbf A_2^{\mathrm T}\mathbf A_1^{\mathrm T}\\
\end{aligned}
$$
