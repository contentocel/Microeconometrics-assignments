# Microeconometrics-assignments

This study utilizes data from the Medical Expenditure Panel Survey (MEPS) from 2017, which is conducted annually by the U.S. Department of Health and Human Services to collect information about health insurance, medical expenditures, and health status for a representative sample of the US population. The survey gathers data from individuals, families, and healthcare providers, and is recognized as one of the most thorough sources of healthcare data in the country. 

Two reports are included in this folder. The first one aims in researching the influence factors of the number of visits to a physician, which assumed to be Poisson distributed, the estimation is obtained by Maximum Likelihood Estimation (MLE) and Newton-Raphson method.
The second report is about determining several variables that influence the amount of healthcare expenditures people have. Previous studies have already shown that being insured or not is an important determining factor for healthcare expenditures, whereas there is no evidence that it can be treated as exogenous in the healthcare expenditure equation. Hence, there could be self-selection problem, which would cause the endogeneity. To check this, Ordinary Least Squares, the Heckman Selectivity Model, and Polynomial Logit with Newey’s selection correction are compared.

\section{Method and Model}
\subsection{Poisson Model}
The Poisson distribution with parameter $\lambda$ is given by:
\[P(Y=k)=\frac{\lambda^{k}e^{-\lambda}}{k!}\]
where
\[E[Y]=Var[Y]=\lambda.\]
In order to use the Maximum Likelihood framework, $Y_{i}$ is applied to be conditional on $x_{i}$, which implies
\[E[Y_{i}|x_{i}]=\lambda_{i}=\exp(x_{i}'\beta).\]
Follows the Poisson distribution with parameter $\lambda_{i}$, the model can be described as
\[P(Y_{i}=y_{i}|x_{i})=\frac{\lambda_{i}^{y_{i}}e^{-\lambda_{i}}}{y_{i}!}\]

\subsection{Estimation of the Parameters}
Based on the Maximum Likelihood Estimation, the log-likelihood function of the Poisson model is given by:
\begin{align*}
    \mathcal{L}(\beta)=\log\Bigg[\prod^{i=1}_{n}\frac{\lambda_{i}^{y_{i}}e^{-\lambda_{i}}}{y_{i}!}\Bigg]&=\sum_{i=1}^{n}\log\Bigg[\frac{\lambda_{i}^{y_{i}}e^{-\lambda_{i}}}{y_{i}!}\Bigg]\\
    &=\sum_{i=1}^{n}\Big[\log(\lambda_{i}^{y_{i
