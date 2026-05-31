# Statistical Mechanics Notes (Pages 18â43)

---

## The Power Spectrum

Suppose we have a random process which goes on from $t=0$ to $t=T$ ($T$ is assumed to be large). Observe that this necessarily implies that the process is not stationary though it may appear almost stationary for times sufficiently different from $0$ and $T$. Let $j(t)$ be a function which characterizes the process. For example, the current in a resistor. We may Fourier analyze $j(t)$. We will use a Fourier series for the present.

$$j(t) = \sum_{n=0}^{\infty} \left( a_n \cos\frac{2\pi n t}{T} + b_n \sin\frac{2\pi n t}{T} \right). \tag{66}$$

Since the process is random, the $a$'s and $b$'s will be different each time the process is repeated or for each member of an ensemble of systems undergoing the process. For many types of noise the $a$'s and $b$'s have Gaussian distributions, and thus the process is said to be a Gaussian random process. This means that if $N(a_n)\,da_n$ is the number of members of an ensemble of systems with $a_n$ between $a_n$ and $a_n + da_n$, $N(a_n)$ will be Gaussian.

Some properties which are quite often found are the following:

**(1)** $a_n$ and $b_m$ are statistically independent:

$$\overline{a_n b_m} = 0 \quad \text{all } n \text{ and } m. \tag{67}$$

**(2)** $a_n$ and $a_m$, and $b_n$ and $b_m$, are statistically independent:

$$\overline{a_n a_m} = 0 \quad m \ne n, \tag{68}$$

$$\overline{b_n b_m} = 0 \quad m \ne n. \tag{69}$$

**(3)** $\overline{a_n^2}$ is equal to $\overline{b_n^2}$.

These are assumptions about the process and don't have to be true. However, they quite often are true and we will assume this unless otherwise stated.

Returning to $j$,

$$j(t) = \sum_{n=1}^{\infty} \left( a_n \cos\frac{2\pi n t}{T} + b_n \sin\frac{2\pi n t}{T} \right). \tag{70}$$

Here I have assumed $j(t)$ has no D.C. value so that the sum can be started at 1. To make things concrete, let us imagine $j$ is a current flowing in a unit resistor. Then $j^2(t)$ would be the instantaneous power being dissipated. The time average of the power dissipated is

$$\langle j^2 \rangle = \frac{1}{T}\int_0^T j^2(t)\,dt = \frac{1}{T}\int_0^T \sum_{n=1}^{\infty}\sum_{m=1}^{\infty} \left\{ \left(a_n\cos\frac{2\pi n t}{T}+b_n\sin\frac{2\pi n t}{T}\right) \left(a_m\cos\frac{2\pi m t}{T}+b_m\sin\frac{2\pi m t}{T}\right) \right\}dt. \tag{71}$$

Interchanging integration and summation we find

$$\langle P \rangle = \langle j^2 \rangle = \sum_n \frac{a_n^2 + b_n^2}{2}. \tag{72}$$

If instead of taking the time average we take the ensemble average with the assumptions just made, all cross terms go out again.

$$\bar{P} = \overline{j^2(t)} = \sum_n \left(\overline{a_n^2}\cos^2\frac{2\pi n t}{T} + \overline{b_n^2}\sin^2\frac{2\pi n t}{T}\right), \tag{73}$$

$$\overline{a_n^2} = \overline{b_n^2} = \overline{\sigma^2}.$$

Thus,

$$\bar{P} = \sum_n \overline{\sigma_n^2}. \tag{74}$$

If we take the ensemble average of $\langle P \rangle$ we also get

$$\langle \bar{P} \rangle = \sum_n \frac{\overline{a_n^2} + \overline{b_n^2}}{2} = \sum_n \overline{\sigma_n^2}. \tag{75}$$

We now define the **power spectrum** or **spectral density** as the ensemble average of the time average of $j^2$ per unit frequency bandwidth. We denote it by $G(f)$. We have

$$f = \frac{n}{T}, \tag{76}$$

$$\Delta f = \frac{\Delta n}{T} \quad\text{or}\quad \frac{\Delta f}{\Delta n} = \frac{1}{T}. \tag{77}$$

$$G(f)\,\Delta f = \overline{\sigma_n^2}\,\Delta n \tag{78}$$

$$\sum_n \overline{\sigma_n^2} = \sum_n \frac{G(f)}{T} \approx \int \overline{\sigma_n^2}\,dn = \int \frac{G(f)\,dn}{T} = \int G(f)\,df. \tag{79}$$

The correlation function and the power spectrum are related, for stationary processes. We have

$$C(\tau) = \langle x(t)\,x(t+\tau)\rangle = \overline{\,\overline{x(t)\,x(t+\tau)}\,} \tag{80}$$

for time-independent processes.

$$C(\tau) = \left\langle \sum_{nm}\left(a_n\cos\frac{2\pi n t}{T}+b_n\sin\frac{2\pi n t}{T}\right) \left(a_m\cos\frac{2\pi m(t+\tau)}{T}+b_m\sin\frac{2\pi m(t+\tau)}{T}\right) \right\rangle$$

$$= \sum_n \left\{ \overline{a_n^2}\left\langle\cos\frac{2\pi n t}{T}\cos\frac{2\pi n(t+\tau)}{T}\right\rangle +\overline{b_n^2}\left\langle\sin\frac{2\pi n t}{T}\sin\frac{2\pi n(t+\tau)}{T}\right\rangle \right\} \tag{81}$$

$$\left\langle\cos\frac{2\pi n t}{T}\cos\frac{2\pi n(t+\tau)}{T}\right\rangle = \frac{1}{T}\int_0^T \cos\frac{2\pi n t}{T} \left(\cos\frac{2\pi n t}{T}\cos\frac{2\pi n\tau}{T} - \sin\frac{2\pi n t}{T}\sin\frac{2\pi n\tau}{T}\right)dt = \tfrac{1}{2}\cos\frac{2\pi n\tau}{T} \tag{82}$$

$$\left\langle\sin\frac{2\pi n t}{T}\sin\frac{2\pi n(t+\tau)}{T}\right\rangle = \frac{1}{T}\int_0^T \sin\frac{2\pi n t}{T} \left(\sin\frac{2\pi n t}{T}\cos\frac{2\pi n\tau}{T} + \cos\frac{2\pi n t}{T}\sin\frac{2\pi n\tau}{T}\right)dt = \tfrac{1}{2}\cos\frac{2\pi n\tau}{T} \tag{83}$$

$$C(\tau) = \tfrac{1}{2}\sum_n \left(\overline{a_n^2}+\overline{b_n^2}\right)\cos\frac{2\pi n\tau}{T} = \sum_n \overline{\sigma_n^2}\cos\frac{2\pi n\tau}{T} \tag{84}$$

$$C(\tau) = \int_0^\infty \overline{\sigma_n^2}\cos\frac{2\pi n\tau}{T}\,dn = \int_0^\infty G(f)\cos 2\pi f\tau\,df. \tag{85}$$

So far $G(f)$ has been defined only for positive $f$. We may, however, extend the definition by setting $G(-f)=G(f)$ or $\tilde{a}_{-n}=\tilde{a}_n$, $\tilde{b}_{-n}=+\tilde{b}_n=\frac{1}{2}b_n$. Then we may write

$$C(\tau) = \tfrac{1}{2}\int_{-\infty}^{\infty} G(f)\cos 2\pi f\tau\,df. \tag{86}$$

We may find $G(f)$ in terms of $C(\tau)$. Multiply both sides of (86) by $\cos 2\pi f'\tau$ and integrate from $0$ to $T$:

$$\int_0^T C(\tau)\cos 2\pi f'\tau\,d\tau = \tfrac{1}{2}\int_{-\infty}^{\infty}df\int_0^T d\tau\, G(f)\cos 2\pi f\tau\cos 2\pi f'\tau \tag{87}$$

$$\int_0^T C(\tau)\cos 2\pi f'\tau\,d\tau = \tfrac{1}{4}\int_{-\infty}^{\infty}\int_0^T d\tau\,df\, G(f) \left[\cos 2\pi(f+f')\tau + \cos 2\pi(f-f')\tau\right]d\tau$$

$$= \tfrac{1}{4}\int_{-\infty}^{\infty}G(f)\,df \left\{ \frac{\sin 2\pi(f+f')T}{2\pi(f+f')} + \frac{\sin 2\pi(f-f')T}{2\pi(f-f')} \right\}. \tag{88}$$

In the limit as $T\to\infty$ the first term integrates to $\frac{1}{2}G(-f')=\frac{1}{2}G(f')$ and the second term integrates to $\frac{1}{2}G(f')$ so that we find

$$4\int_0^T C(\tau)\cos 2\pi f'\tau\,d\tau = G(f'). \tag{89}$$

Equations (86) and (89) constitute the **WienerâKhintchine Theorem**.

---

## Insert II: Spectral Density and Correlations in Terms of Fourier Integrals

$j(t)$ is a random variable. Assume the process goes on from $t=0$ to $t=T$.

$$j(t) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}A(\omega)\,e^{i\omega t}\,d\omega. \tag{II.1}$$

Making use of Parseval's theorem the time average of $j^2(t)$ is given by

$$\langle j^2(t)\rangle = \frac{1}{T}\int_{-\infty}^{\infty}|A(\omega)|^2\,d\omega = \frac{2}{T}\int_0^{\infty}|A(\omega)|^2\,d\omega. \tag{II.2}$$

Define

$$G(\omega) = \frac{2\,\overline{|A(\omega)|^2}}{T} \quad \text{where overline represents ensemble average.} \tag{II.3}$$

Alternatively we may write

$$j(t) = \int_{-\infty}^{\infty}B(f)\,e^{2\pi i f t}\,df, \quad f = \omega/2\pi \tag{II.4}$$

$$B(f) = \sqrt{2\pi}\,A(\omega), \qquad \frac{2\,\overline{|A(\omega)|^2}}{T}\,d\omega = \frac{2\,\overline{|B(f)|^2}}{T}\,df.$$

The spectral density $G(f)$ is defined as

$$G(f) = \frac{2\,\overline{|B(f)|^2}}{T}, \tag{II.5}$$

which is the time average of the ensemble average of the power per unit frequency interval.

The autocorrelation function $C(\tau)$ given by

$$C(\tau) = \frac{1}{T}\int_0^T j(t)\,j(t+\tau)\,dt \tag{II.6}$$

is related to $G(f)$ by the relations

$$C(\tau) = \int_0^{\infty}G(f)\cos 2\pi f\tau\,df = \int_0^{\infty}G(\omega)\cos\omega\tau\,d\omega, \tag{II.7}$$

$$G(f) = 4\int_0^T c(\tau)\cos 2\pi f\tau\,d\tau = 2\pi G(\omega). \tag{II.8}$$

In most cases $C(\tau)$ goes to $0$ rapidly for large $\tau$ and $T$ may be replaced by $\infty$ as the upper limit for the integral appearing in (II.8).

---

## The Central Limit Theorem

Let $x$ be a random variable. Then the sum of $n$ $x$'s is also a random variable.

$$S_n = \sum_{i=1}^n x_i. \tag{90}$$

We will imagine that $x$ takes on only a discrete set of values although everything goes through if $x$ can take on a continuous set of values. Let $P(x)$ be the probability that the variable takes on the value $x$. We will assume that

$$\bar{x} = 0. \tag{91}$$

If this is not true, we can define a new variable $y = x - \bar{x}$ for which it is true. We also assume that $\overline{x^2}$ is finite.

Now the sum of $n$ $x$'s can take on a definite number of values and there is a definite probability that it will take on each of these values. We let $P_n(S)$ be the probability that the sum of $n$ $x$'s adds up to $S$. The central limit theorem states that the limit of $P_n(S)$ as $n$ goes to $\infty$ is a Gaussian.

**Proof**

Let us compute $P_{n+1}(S)$. We have

$$S_{n+1} = S_n + x_{n+1}, \tag{92}$$
$$S_n = S_{n+1} - x_{n+1}.$$

Further

$$P_{n+1}(S) = \sum_x P_n(S-x)\,P_1(x). \tag{93}$$

If $n$ is very large, we expect that

$$S \gg x. \tag{94}$$

We will therefore expand $P_n(S-x)$ about $S$:

$$P_{n+1}(S) = \sum_x \left\{ P_n(S) - x P_n'(S) + \frac{x^2}{2}P_n''(S) + \cdots \right\}P_1(x) \tag{95}$$

or

$$P_{n+1}(S) = P_n(S) + \frac{\overline{x^2}}{2}\,P_n''(S) \tag{96}$$

since $\bar{x}$ is zero.

$$P_{n+1}(S) - P_n(S) - \frac{\overline{x^2}}{2}\frac{\partial^2 P_n(S)}{\partial S^2} = 0,$$

or approximately

$$\frac{\partial P(S)}{\partial n} - \frac{\overline{x^2}}{2}\frac{\partial^2 P_n(S)}{\partial S^2} = 0. \tag{97}$$

Equation (97) is a diffusion equation of the usual type and may be solved in the usual manner. We write

$$P = N(n)\,S(s). \tag{98}$$

From (97) we have

$$\frac{N'}{N} - \frac{\overline{x^2}}{2}\frac{S''}{S} = 0, \tag{99}$$

$$\frac{S''}{S} = -k^2, \tag{100}$$

$$S = e^{iks}, \tag{101}$$

$$\frac{N'}{N} = -\frac{k^2\overline{x^2}}{2}, \tag{102}$$

$$N = e^{-\frac{k^2\overline{x^2}}{2}n}. \tag{103}$$

$$P_n(S) = \int A(k)\,e^{-\frac{k^2\overline{x^2}}{2}n - iks}\,dk. \tag{104}$$

As $n\to\infty$, the exponential gets sharper and sharper about $k=0$ and only $A(0)$ matters.

$$P_n(S)\Big|_{n\to\infty} \to A(0)\int_{-\infty}^{\infty} \exp\!\left\{-\frac{k^2\overline{x^2}\,n}{2} - ikS\right\}dk$$

$$= A(0)\int_{-\infty}^{\infty} \exp\!\left\{ -\frac{n\overline{x^2}}{2}\!\left(k+\frac{iS}{n\overline{x^2}}\right)^2 -\frac{S^2}{2n\overline{x^2}} \right\}dk$$

$$= A(0)\sqrt{\frac{4\pi}{n\overline{x^2}}} \exp\!\left\{-\frac{S^2}{2n\overline{x^2}}\right\}. \tag{105}$$

$A(0)$ may be determined from the normalization of $P_n$. This verifies the Central Limit Theorem.

---

## Example of Power Spectrum: Shot Noise

For the problem of shot noise we have for the current,

$$j(t) = \sum_i \delta(t - t_i), \tag{106}$$

where the $t_i$ are the times of emission of the electrons. We have

$$a_n = \frac{2}{T}\int_0^T j(t)\cos\frac{2\pi n t}{T}\,dt = \frac{2}{T}\sum_\ell \cos\frac{2\pi n t_\ell}{T} = \frac{2}{T}\sum_\ell \cos\theta_\ell, \tag{107}$$

$$b_n = \frac{2}{T}\sum_\ell \sin\frac{2\pi n t_\ell}{T} = \frac{2}{T}\sum_\ell \sin\theta_\ell, \tag{108}$$

where $\theta_\ell = \dfrac{2\pi n t_\ell}{T}$ reduced modulo $2\pi$.

Consider a little element of arc $\Delta\theta$. What is the probability that we will find $k$ electrons emitted in $\Delta\theta$? If the average number of electrons emitted is $N$, then the average number emitted in $\Delta\theta$ is $\dfrac{N\,\Delta\theta}{2\pi}$.

The electrons are emitted completely at random and will be distributed uniformly in $\theta$. The probability of finding $k$ electrons emitted in $\Delta\theta$ is a Poisson distribution as we have already seen. Thus

$$P(k,\Delta\theta) = \left(\frac{N}{2\pi}\Delta\theta\right)^k \frac{e^{-\frac{N\Delta\theta}{2\pi}}}{k!}. \tag{109}$$

If $\Delta\theta$ is large enough so that $k$ is on average large, then (109) can be approximated by

$$P(k,\Delta\theta) \cong C\,\exp\!\left\{ -\frac{\pi}{N\Delta\theta}\!\left(k - \frac{N\Delta\theta}{2\pi}\right)^2 \right\}. \tag{110}$$

If $T$ is large, $k$ will be large even for small $\Delta\theta$.

If the circle is divided into $M$ equal sections, then the probability that we find $k_1$ electrons in $\Delta\theta_1$, $k_2$ in $\Delta\theta_2$, âŠ, $k_M$ in $\Delta\theta_M$ is given by (111) since these are independent probabilities.

$$P(k_1,k_2,\ldots,k_M) \propto e^{-\frac{\pi}{N\Delta\theta}\sum_j\left(k_j-\frac{N\Delta\theta}{2\pi}\right)^2} = e^{-\frac{\pi}{N\Delta\theta}\sum_j x_j^2}, \tag{111}$$

$$x_j = k_j - \frac{N\Delta\theta}{2\pi} = k_j - N/M, \quad \Delta\theta = 2\pi/M.$$

Now for large $M$ we may approximate $a_n$ and $b_n$ by

$$\begin{pmatrix}a_n\\b_n\end{pmatrix} = \frac{2}{T}\sum_\ell \begin{pmatrix}\cos\theta_\ell\\\sin\theta_\ell\end{pmatrix} = \frac{2}{T}\sum_{j=1}^{M}k_j \begin{pmatrix}\cos\theta_j\\\sin\theta_j\end{pmatrix}, \tag{112}$$

where $k_j$ is the number of electrons emitted during the $j$th $\theta$ interval and $\theta_j = j\,\Delta\theta = j\cdot 2\pi/M$. We wish to know the probabilities that $a_n$ be between $a_n$ and $a_n + da_n$ and $b_n$ between $b_n$ and $b_n + db_n$. These are given by the sum of the probability $P(k_1,k_2,\ldots,k_M)$ over all $k_i$ such that $a_n$ or $b_n$ is in the desired region. We will imagine that we can treat $k_j$ or $x_j$ as continuous variables.

$$P\!\begin{pmatrix}a_n\\b_n\end{pmatrix}da_n\,db_n \propto \int\!\cdots\!\int P(x_1,\ldots,x_M)\,dx_1\cdots dx_M \tag{113}$$

over all $x_i$ such that $\begin{pmatrix}a_n\\b_n\end{pmatrix}$ is in the desired region.

Now Eqs. (112) are linear equations for $a_n$ and $b_n$ in terms of the $x_j$'s. They represent hyperplanes in $x_j$ space and the integration is to be carried out over these planes. $P(x_1,\ldots,x_M)$ is spherically symmetric so that integrating it over a hyperplane cannot depend on the orientation of the plane, and must depend only on the distance of the plane from the origin. Now $x_j = \text{constant}$ is also a hyperplane at a distance $x_j$ from the origin and the probability of finding $x_j$ in $dx_j$ is given by

$$P(x_j)\,dx_j \propto e^{-\frac{M}{2N}x_j^2}\,dx_j. \tag{114}$$

To find the probability that $a_n$ or $b_n$ lies in $da_n$ or $db_n$ we need only find the distance of the appropriate hyperplanes given by (112) from the origin and substitute this distance for $x_j$ in (114).

The distance squared of a point from the origin, $S^2$, is

$$S^2 = \sum_j x_j^2. \tag{115}$$

We have for the minimum distance to the plane

$$S\,dS = \sum_j x_j\cdot dx_j = 0. \tag{116}$$

Further, the $x_j$ must satisfy (112) so the $dx_j$ must satisfy

$$\sum_j dx_j\begin{pmatrix}\cos\theta_j\\\sin\theta_j\end{pmatrix} = 0. \tag{117}$$

Multiplying (117) by the Lagrange multiplier $\lambda$ and subtracting from (116) gives

$$\sum_j\left\{x_j - \lambda\begin{pmatrix}\cos\theta_j\\\sin\theta_j\end{pmatrix}\right\}dx_j = 0. \tag{118}$$

This must be zero for every $dx_j$. Thus

$$x_j = \lambda\begin{pmatrix}\cos\theta_j\\\sin\theta_j\end{pmatrix}. \tag{119}$$

Substituting (119) in (112) gives

$$\begin{pmatrix}a_n\\b_n\end{pmatrix} = \frac{2}{T}\sum_{j=1}^{M} \left\{ \lambda\begin{pmatrix}\cos\theta_j\\\sin\theta_j\end{pmatrix} + \frac{N}{M}\begin{pmatrix}\cos\theta_j\\\sin\theta_j\end{pmatrix} \right\}, \tag{120}$$

$$\begin{pmatrix}a_n\\b_n\end{pmatrix} = \frac{\lambda}{T}M, \tag{121}$$

$$\lambda = \frac{T}{M}\begin{pmatrix}a_n\\b_n\end{pmatrix}. \tag{122}$$

Substituting (122) in (119) and (119) in (115) gives for $S^2$

$$S^2 = \frac{1}{2}\frac{T^2}{M}\begin{pmatrix}a_n\\b_n\end{pmatrix}^2. \tag{123}$$

Substituting $S$ for $x_j$ in (114) we find,

$$P(a_n)\,da_n \propto e^{-\frac{T^2}{4N}a_n^2}\,da_n, \tag{124}$$

$$P(b_n)\,db_n \propto e^{-\frac{T^2}{4N}b_n^2}\,db_n. \tag{125}$$

This result is independent of $M$ as it should be. From (124) and (125) $\overline{a_n^2}$ and $\overline{b_n^2}$ can be computed and are found to be equal to,

$$\overline{a_n^2} = \frac{2N}{T^2} = \frac{2\bar{n}}{T}, \tag{126}$$

$$\overline{b_n^2} = \frac{2N}{T^2} = \frac{2\bar{n}}{T}. \tag{127}$$

We can also obtain this result from the central limit theorem. First we have for $\bar{a}_n$:

$$\bar{a}_n = \frac{2}{T}\sum_j\overline{\cos\frac{2\pi n t_j}{T}} = \frac{2}{T}\int\overline{\sum_j\delta(t-t_j)}\cos\frac{2\pi n t}{T}\,dt = \frac{2}{T}\int \bar{n}\,dt\cos\frac{2\pi n t}{T} = 0. \tag{128}$$

Likewise $\bar{b}_n = 0$.

For $\overline{a_n^2}$ we have

$$\overline{a_n^2} = \frac{4}{T^2}\sum_{j\ell}\overline{\cos\frac{2\pi n t_j}{T}\cos\frac{2\pi n t_\ell}{T}}$$

$$= \frac{4}{T^2}\iint dt_1\,dt_2 \sum_{\substack{j,\ell\\j\neq\ell}} \delta(t_1-t_j)\delta(t_2-t_\ell) \cos\frac{2\pi n t_1}{T}\cos\frac{2\pi n t_2}{T} + \frac{4}{T^2}\int\overline{\sum_j\delta(t-t_j)}\,dt\cos^2\frac{2\pi n t}{T}$$

$$= \frac{4}{T^2}\iint \bar{n}^2\,dt_1\,dt_2\cos\frac{2\pi n t_1}{T}\cos\frac{2\pi n t_2}{T} + \frac{4}{T^2}\int \bar{n}\,dt_1\cos^2\frac{2\pi n t_1}{T} = \frac{2\bar{n}}{T}. \tag{129}$$

Likewise

$$\overline{b_n^2} = \frac{2\bar{n}}{T}. \tag{130}$$

For $\overline{a_n b_n}$ we find

$$\overline{a_n b_n} = \frac{4}{T^2}\sum_{j\ell}\overline{\cos\frac{2\pi n t_j}{T}\sin\frac{2\pi n t_\ell}{T}}$$

$$= \frac{4}{T^2}\iint dt_1\,dt_2 \sum_{\substack{j,\ell\\j\neq\ell}} \delta(t_1-t_j)\delta(t_2-t_\ell) \cos\frac{2\pi n t_1}{T}\sin\frac{2\pi n t_2}{T} + \frac{4}{T^2}\int\overline{\sum_j\delta(t-t_j)}\,dt \cos\frac{2\pi n t}{T}\sin\frac{2\pi n t}{T}$$

$$= \frac{4\bar{n}^2}{T^2}\iint dt_1\,dt_2 \cos\frac{2\pi n t_1}{T}\sin\frac{2\pi n t_2}{T} + \frac{4\bar{n}}{2T^2}\int dt\,\sin\frac{4\pi n t}{T} = 0. \tag{131}$$

For $\overline{a_n a_m}$ we find

$$\overline{a_n a_m} = \frac{4}{T^2}\sum_{j\ell} \overline{\cos\frac{2\pi n t_j}{T}\cos\frac{2\pi m t_\ell}{T}}$$

$$= \frac{4}{T^2}\iint dt_1\,dt_2 \sum_{\substack{j,\ell\\j\neq\ell}} \delta(t_1-t_j)\delta(t_2-t_\ell) \cos\frac{2\pi n t_1}{T}\cos\frac{2\pi m t_2}{T} + \frac{4}{T^2}\int\overline{\sum_j\delta(t-t_j)}\,dt \cos\frac{2\pi n t}{T}\cos\frac{2\pi m t}{T}. \tag{132}$$

$$\overline{a_n a_m} = \frac{4}{T^2}\bar{n}^2\iint dt_1\,dt_2 \cos\frac{2\pi n t_1}{T}\cos\frac{2\pi m t_2}{T} + \frac{4}{T^2}\bar{n}\int dt\cos\frac{2\pi n t}{T}\cos\frac{2\pi m t}{T} = 0. \tag{133}$$

Likewise

$$\overline{a_n b_m} = 0, \tag{134}$$

$$\overline{b_n b_m} = 0. \tag{135}$$

Finally, for $n=0$ we have,

$$a_0 = \frac{N}{T}, \tag{136}$$

$$\bar{a}_0 = \frac{\bar{N}}{T}, \tag{137}$$

$$P(N)\,dN = P(Ta_0)\,T\,da_0, \tag{138}$$

$$P(N)\,dN = \frac{(\bar{n}T)^N e^{-\bar{n}T}}{N!}\,dN \cong C\,e^{-\frac{(N-\bar{n}T)^2}{2\bar{n}T}}\,dN = C\exp\!\left\{-\frac{T(a_0 - \bar{n})^2}{2\bar{n}}\right\}da_0, \tag{139}$$

$$\bar{a}_0 = \bar{n}, \tag{140}$$

$$\overline{a_0^2} - \bar{a}_0^2 = \frac{\bar{n}}{T}. \tag{141}$$

---

## Problem II

Consider the following system consisting of a vacuum tube connected to an $RC$ circuit through a battery. The battery is to simply supply enough voltage so that all the emitted electrons go from the cathode to the anode. The equation for the charge on the condenser is

$$\frac{dQ}{dt} = -j + j_r(t),$$

where $j_r$ is the random current emitted by the cathode and $j$ is the current through the resistor.

$$j = \frac{V}{R}, \qquad V = \frac{Q}{C},$$

$$\frac{dQ}{dt} = -\frac{Q}{RC} + j_r(t),$$

$$j_r(t) = \sum_i \delta(t-t_i), \quad \text{the particles are emitted at a uniform rate.}$$

*Find for $Q$:* $\quad\bar{a}_n,\ \bar{b}_n,\ \overline{a_n^2},\ \overline{b_n^2},\ G(f),\ C(\tau)$.

---

## Fluctuation Dissipation Theory

### Brownian Motion

We shall now look at the problem of Brownian Motion. Consider a particle suspended in a fluid. Its equation of motion is

$$m\ddot{x} = F(t), \tag{142}$$

where $F(t)$ is the force exerted on the particle by the fluid. Now if the particle is macroscopic and moving through the fluid, we know that the primary force on the particle is a drag which tends to stop the motion. The equation of motion for such a particle is, in general,

$$m\ddot{x} = f(\dot{x}), \tag{143}$$

and more specifically for slowly moving particles

$$m\ddot{x} = -R\dot{x}. \tag{144}$$

Now we know that the drag force is not the only force acting on a particle. The particle is being randomly bombarded by the molecules of the fluid and so there is also a random force acting on the particle. Of course the drag also comes from the bombardment of the particle by the fluid molecules. It is the systematic part of the force on the particle due to this bombardment. It arises because the motion of the particle causes it to be struck more often and more violently in the front than in the rear.

We will divide the force into two parts, a systematic drag and a random force.

$$\overline{F(t)} = \text{systematic force} = -R\dot{x}, \tag{145}$$

$$f(t) = \text{random force} = F(t) - \overline{F(t)}, \tag{146}$$

$$\overline{f(t)} = 0.$$

We imagine that $f(t)$ is a rapidly fluctuating force compared to the time scale for the stopping of the particle. For bodies of macroscopic size the systematic force is the only important one and equation (143) is valid. For very light particles, the fluctuating force is also important and equation (142) takes the form

$$m\ddot{x} = -R\dot{x} + f(t). \tag{147}$$

Now we do not know the details of $f(t)$; in fact it will be different for different particles in an ensemble, so that we cannot determine the motion of the particle. Nevertheless, we can obtain a formal solution to (147). Equation (147) has an integrating factor $\exp\!\left(\frac{R}{m}t\right)$. Therefore, we can write (147) in the form,

$$\frac{d}{dt}\left(\dot{x}\,e^{t/\tau}\right) = e^{t/\tau}a(t), \quad \tau = R/m, \quad a(t) = f(t)/m. \tag{148}$$

Integrating equation (148) we find,

$$\dot{x} = e^{-t/\tau}\left\{\int_0^t e^{t'/\tau}a(t')\,dt' + \dot{x}_0\right\}, \tag{149}$$

or

$$\dot{x} = \int_0^t e^{(t'-t)/\tau}a(t')\,dt' + \dot{x}_0\,e^{-t/\tau}. \tag{150}$$

Equation (150) can be integrated once more. We have

$$x = \int_0^t dt_1\int_0^{t_1} e^{(t'-t_1)/\tau}a(t')\,dt' + \dot{x}_0\,\tau(1-e^{-t/\tau}) + x_0. \tag{151}$$

Observe that the double integral is to be taken over the triangular region. The integration is first over $t'$ going from $0$ to $t_1$ and then over $t_1$ going from $0$ to $t$. We can alternatively write this integral as first being over $t_1$, going from $t'$ to $t$, and then over $t'$ going from $0$ to $t$.

$$\int_0^t dt'\int_{t'}^t e^{(t'-t_1)/\tau}a(t')\,dt_1 = \int_0^t \tau\,a(t')\bigl(1-e^{(t'-t)/\tau}\bigr)\,dt'. \tag{152}$$

Thus equation (151) may be written as

$$x = \int_0^t \tau\,a(t')\bigl(1-e^{(t'-t)/\tau}\bigr)\,dt' + \dot{x}_0\,\tau(1-e^{-t/\tau}) + x_0. \tag{153}$$

We could have found this solution in another way. The random force imparts to the particle a velocity $a(t')\,dt'$ in the time interval $dt'$. Between $t'$ and $t$ the particle travels a distance $\tau\,a(t')(1-e^{(t'-t)/\tau})$ due to this velocity. Since the equation is linear, the displacement at $t$ is the sum of all the displacements due to all the little impulses and hence we get the integral appearing in (153).

Let us now compute $\bar{\dot{x}}$. From (149) we have

$$\bar{\dot{x}} = \int_0^t e^{(t'-t)/\tau}\overline{a(t')}\,dt' + \dot{x}_0\,e^{-t/\tau} = \bar{\dot{x}}_0\,e^{-t/\tau} \tag{154}$$

since $\overline{a(t')} = 0$.

For $\overline{\dot{x}^2}$ we have

$$\overline{\dot{x}^2} = \int_0^t\int_0^t \overline{a(t')\,a(t'')} \,e^{(t'+t''-2t)/\tau}\,dt'\,dt'' + 2\dot{x}_0\,e^{-t/\tau}\int_0^t \overline{a(t')}\,e^{(t'-t)/\tau}\,dt' + \dot{x}_0^2\,e^{-2t/\tau}. \tag{155}$$

Now $a(t')$ is to be the nonsystematic acceleration so that it cannot be related to $\dot{x}_0$ and hence $\overline{\dot{x}_0\,a(t')} = 0$.

Thus the middle term goes out. The last term averages to

$$\overline{\dot{x}_0^2}\,e^{-2t/\tau}. \tag{156}$$

Let us now look at the double integral in (155):

$$\int_0^t\int_0^t \overline{a(t')\,a(t'')}\,e^{(t'+t''-2t)/\tau}\,dt'\,dt''. \tag{157}$$

Now the double integral is over the square. We assume that $a(t')$ is a very rapidly fluctuating acceleration and that $a(t'')$ is uncorrelated with $a(t')$ except for $t''$ very near to $t'$; that is, the random accelerations produced by different fluid molecules are uncorrelated. Thus

$$\overline{a(t')\,a(t'')} = 0 \quad\text{unless}\quad |t'-t''| < \delta t, \tag{158}$$

where $\delta t$ is a very short time. Let $t'' = t' + x$, then $dt'' = dx$ if $t'$ is kept constant. We may write the above integral as follows:

$$\int_0^t dt'\int_{-t'}^{t-t'} \overline{a(t')\,a(t'+x)}\,e^{(2t'+x-2t)/\tau}\,dx. \tag{159}$$

Now the ensemble average is zero unless $x$ is very small so that we can neglect the $x$ variation in the exponential and carry out the integration over $x$. We write

$$\int_{-\infty}^{\infty}\overline{f(t')\,f(t'+x)}\,dx = m^2\int_{-\infty}^{\infty}\overline{a(t')\,a(t'+x)}\,dx \equiv I, \tag{160}$$

where the infinite limits can be introduced since large values of $x$ make no contribution to the integral. Expression (159) becomes

$$\frac{I}{m^2}\int_0^t e^{2(t'-t)/\tau}\,dt' = \frac{\tau}{2}\frac{I}{m^2}\bigl(1-e^{-2t/\tau}\bigr). \tag{170}$$

> **Note:** equation numbers (161) through (169) have been omitted.

Thus we find for $\overline{\dot{x}^2}$ from (155):

$$\overline{\dot{x}^2} = \frac{\tau I}{2m^2}\bigl(1-e^{-2t/\tau}\bigr) + \overline{\dot{x}_0^2}\,e^{-2t/\tau}. \tag{171}$$

As $t\to\infty$,

$$\overline{\dot{x}^2} \to \frac{I\tau}{2m^2}. \tag{172}$$

Now we know that if the fluid and Brownian particles are in thermal equilibrium, then the average kinetic energy per particle is $kT/2$ for a group of particles. Thus

$$\overline{\dot{x}^2} = \frac{kT}{m}. \tag{173}$$

Combining (172) and (173) gives,

$$\frac{\tau I}{2m^2} = \frac{kT}{m},$$

or

$$I = \frac{2kTm}{\tau} = 2kTR. \tag{174}$$

Now $I$ is a measure of the random fluctuating force on a particle and $R$ is a measure of the resistance of the fluid to the motion of the particle. Thus we see that the fluctuating force is related to the resistance, the relation being such as to maintain thermal equilibrium.

We may also compute the average value of $x$ and $x^2$. From (153) we have

$$\bar{x} = \bar{\dot{x}}_0\,\tau(1-e^{-t/\tau}) + \bar{x}_0, \tag{175}$$

and

$$\overline{x^2} = \tau^2\int_0^t\int_0^t \overline{a(t')\,a(t'')} \bigl(1-e^{(t'-t)/\tau}\bigr)\bigl(1-e^{(t''-t)/\tau}\bigr) \,dt'\,dt''$$

$$+ 2\dot{x}_0\,\tau^2(1-e^{-t/\tau}) \int_0^t a(t')\bigl(1-e^{(t'-t)/\tau}\bigr)\,dt'$$

$$+ 2x_0\tau\int_0^t a(t')\bigl(1-e^{(t'-t)/\tau}\bigr)\,dt'$$

$$+ \overline{\dot{x}_0^2}\,\tau^2(1-e^{-t/\tau})^2 + 2\overline{x_0\dot{x}_0}\,\tau(1-e^{-t/\tau}) + \overline{x_0^2}. \tag{176}$$

Proceeding as before gives

$$\overline{x^2} = \frac{\tau^2}{m^2}I\int_0^t\bigl(1-e^{(t'-t)/\tau}\bigr)^2\,dt' + \overline{\dot{x}_0^2}\,\tau^2(1-e^{-t/\tau})^2 + 2\overline{\dot{x}_0 x_0}\,\tau(1-e^{-t/\tau}) + \overline{x_0^2}$$

$$= \frac{\tau^2}{m^2}I\left[t - 2\tau(1-e^{-t/\tau}) + \frac{\tau}{2}(1-e^{-2t/\tau})\right]$$

$$+ \overline{\dot{x}_0^2}\,\tau^2(1-e^{-t/\tau})^2 + 2\overline{\dot{x}_0 x_0}\,\tau(1-e^{-t/\tau}) + \overline{x_0^2}. \tag{177}$$

As $t\to\infty$ this gives

$$\overline{x^2} \xrightarrow{t\to\infty} \frac{\tau^2}{m^2}I\,t = 2\frac{kT}{m}\tau\,t = 2\frac{kT}{m}\tau^2\frac{t}{\tau} = 2V_T^2\tau^2\frac{t}{\tau}, \tag{178}$$

where $V_T$ is the thermal velocity of a particle.

We see that for large $t$, $\overline{x^2}$ increases linearly with $t$. This is a diffusion-like behavior. Equation (178) has a simple physical interpretation. The distance a thermal particle will go in a stopping time is $V_T\tau$. If the particle makes $t/\tau$ random steps of size $V_T\tau$, then $\overline{x^2} \sim (V_T\tau)^2(t/\tau)$, consistent with (178).
