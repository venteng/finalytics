# Introductino to Gibbs sampling


**Prior:**
- $\mu \sim N(\mu_0, \sigma_0^2)$
- $\sigma^2 \sim \text{InverseGamma}(\alpha, \beta)$

**Likelihood:**
- $X_i, \ldots, X_n \sim N(\mu, \sigma^2)$.

**Tasks:**
1. Write down the density of $\mu$ and $\sigma^2$.
2. Write down the likelihood.
3. Write down the full conditional density of $\mu$ and $\sigma^2$.
4. Provide the Gibbs sampling algorithm to understand the posterior distribution of $\mu$ and $\sigma^2$.

### Detailed Answers

#### 1. Prior Densities

**Density of $\mu$:**
The prior for $\mu$ is a normal distribution:
$\[ p(\mu) = \frac{1}{\sqrt{2\pi \sigma_0^2}} \exp\left(-\frac{(\mu - \mu_0)^2}{2\sigma_0^2}\right) \]$
where $\mu_0$ is the mean and $\sigma_0^2$ is the variance of the prior distribution for $\mu$.

**Density of $\sigma^2$:**
The prior for $\sigma^2$ is an inverse gamma distribution:
$\[ p(\sigma^2) = \frac{\beta^\alpha}{\Gamma(\alpha)} (\sigma^2)^{-\alpha - 1} \exp\left(-\frac{\beta}{\sigma^2}\right) \]$
where $\alpha$ and $\beta$ are the shape and scale parameters, respectively.

#### 2. Likelihood Function

For the model where $X_1, \ldots, X_n \sim N(\$






### 1. Prior Densities

#### Density of $\mu$
Given the prior for $\mu$ is a normal distribution, the density function is:
$
p(\mu) = \frac{1}{\sqrt{2\pi \sigma_0^2}} \exp\left(-\frac{(\mu - \mu_0)^2}{2\sigma_0^2}\right)
$
where $\mu_0$ is the mean and $\sigma_0^2$ is the variance of the prior distribution for $\mu$.

#### Density of $\sigma^2$
Given the prior for $\sigma^2$ is an inverse gamma distribution, the density function is:
$p(\sigma^2) = \frac{\beta^\alpha}{\Gamma(\alpha)} (\sigma^2)^{-\alpha - 1} \exp\left(-\frac{\beta}{\sigma^2}\right)$
where $\alpha$ and $\beta$ are the shape and scale parameters, respectively.

### 2. Likelihood Function

For the given model, where $X_1, \ldots, X_n \sim N(\mu, \sigma^2)$ independently, the likelihood function $L(\mu, \sigma^2)$ is:
$L(\mu, \sigma^2) = \prod_{i=1}^n \frac{1}{\sqrt{2\pi \sigma^2}} \exp\left(-\frac{(X_i - \mu)^2}{2\sigma^2}\right)$
which simplifies to:
$L(\mu, \sigma^2) = (2\pi \sigma^2)^{-n/2} \exp\left(-\frac{\sum_{i=1}^n (X_i - \mu)^2}{2\sigma^2}\right)$

### 3. Full Conditional Densities

#### Full Conditional for $\mu$
Given $\sigma^2$, $\mu$ follows a normal distribution:
$\mu | \sigma^2, X \sim N\left(\mu_n, \sigma_n^2\right)$
where:
$\sigma_n^2 = \left(\frac{1}{\sigma_0^2} + \frac{n}{\sigma^2}\right)^{-1}$
$\mu_n = \sigma_n^2 \left(\frac{\mu_0}{\sigma_0^2} + \frac{\sum_{i=1}^n X_i}{\sigma^2}\right)$

#### Full Conditional for $\sigma^2$
Given $\mu$, $\sigma^2$ follows an inverse gamma distribution:
$\sigma^2 | \mu, X \sim \text{InverseGamma}\left(\alpha_n, \beta_n\right)$
where:
$\alpha_n = \alpha + \frac{n}{2}$
$\beta_n = \beta + \frac{1}{2}\sum_{i=1}^n (X_i - \mu)^2$

### 4. Gibbs Sampling Algorithm

Here's a basic Gibbs sampling algorithm to sample from the posterior distribution of $\mu$ and $\sigma^2$:

1. **Initialize** $\mu$ and $\sigma^2$.
2. For each iteration:
   a. Sample $\mu$ from $N(\mu_n, \sigma_n^2)$ using the full conditional density for $\mu$.
   b. Sample $\sigma^2$ from $\text{InverseGamma}(\alpha_n, \beta_n)$ using the full conditional density for $\sigma^2$.
3. Repeat step 2 for a large number of iterations to approximate the posterior distribution.

Ensure that sufficient iterations are performed to allow for convergence of the Markov chain, and consider discarding an initial set of samples as burn-in.



Certainly! To find the full conditional density of $\mu$, given $\sigma^2$ and data $X_1, \ldots, X_n$, we need to consider both the likelihood function and the prior distribution of $\mu$.

Given that $\mu \sim N(\mu_0, \sigma_0^2)$ and $X_i | \mu, \sigma^2 \sim N(\mu, \sigma^2)$ for $i = 1, \ldots, n$, we can use the properties of the normal distribution to derive the full conditional distribution. The process combines these two distributions by treating the likelihood as a pseudo-prior and applying the formula for the posterior distribution in a conjugate setting.

### Prior Distribution:
$p(\mu) = \frac{1}{\sqrt{2\pi \sigma_0^2}} \exp\left(-\frac{(\mu - \mu_0)^2}{2\sigma_0^2}\right)$

### Likelihood (given $\sigma^2$):
$p(X|\mu, \sigma^2) = \prod_{i=1}^n \frac{1}{\sqrt{2\pi \sigma^2}} \exp\left(-\frac{(X_i - \mu)^2}{2\sigma^2}\right)$
$= (2\pi \sigma^2)^{-n/2} \exp\left(-\frac{\sum_{i=1}^n (X_i - \mu)^2}{2\sigma^2}\right)$

### Combining the Prior and Likelihood:

To find the full conditional for $\mu$, we treat the above as a product of two exponentials and simplify. First, rewrite the likelihood:
$\exp\left(-\frac{\sum_{i=1}^n (X_i - \mu)^2}{2\sigma^2}\right) = \exp\left(-\frac{\sum_{i=1}^n X_i^2 - 2\mu \sum_{i=1}^n X_i + n\mu^2}{2\sigma^2}\right)$

By completing the square for $\mu$, we get:
$-\frac{\sum_{i=1}^n X_i^2 - 2\mu \sum_{i=1}^n X_i + n\mu^2 + \frac{(\mu - \mu_0)^2 \sigma^2}{\sigma_0^2}}{2\sigma^2} = -\frac{\left(\mu - \frac{\frac{\sum_{i=1}^n X_i}{\sigma^2} + \frac{\mu_0}{\sigma_0^2}}{\frac{n}{\sigma^2} + \frac{1}{\sigma_0^2}}\right)^2 \left(\frac{n}{\sigma^2} + \frac{1}{\sigma_0^2}\right)}{2}$

### Full Conditional for $\mu$ (given $\sigma^2$):
Thus, the full conditional density for $\mu$ is a normal distribution:
$\mu | \sigma^2, X \sim N\left(\mu_n, \sigma_n^2\right)$
where:
$\sigma_n^2 = \left(\frac{n}{\sigma^2} + \frac{1}{\sigma_0^2}\right)^{-1}$
$\mu_n = \sigma_n^2 \left(\frac{\sum_{i=1}^n X_i}{\sigma^2} + \frac{\mu_0}{\sigma_0^2}\right)$

This is the exact full conditional density for $\mu$ given $\sigma^2$ and the data, combining Bayesian updating of the mean based on the observed data and the prior mean, appropriately weighted by their respective variances.



