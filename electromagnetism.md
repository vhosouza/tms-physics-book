---
description: The background for magnetic stimulation
---

# Electromagnetism

Everything starts with the four Maxwell's equations:

$$
\bf{\nabla}\times\bf{B} = \mu_0\bf{J} + \mu_0\varepsilon_0\frac{ \partial \bf{E}}{\partial t} \qquad \text{(Ampère's Law)}
$$

$$
\bf{\nabla}\times\bf{E} = - \frac{\partial \bf{B}}{\partial t} \qquad \text{(Faraday's Law)}
$$

$$
\bf{\nabla}\cdot\bf{B} = 0 \qquad \text{(Gauss's Law)}
$$

$$
\bf{\nabla}\cdot\bf{E} = \frac{\rho}{{\varepsilon}_0} \qquad \text{(Colomb's Law)}
$$

To know the effects of TMS we have to compute the induced electric field in the brain tissue. Consider an electric current  $I(t)$ changing over time and running in a coil away in free space. The changing current will generate a magnetic field that also changes in time. According to Faraday's law of induction, the changing magnetic field will induce an associated primary electric field ($\bf{E}_1$) in space.	

However, as we insert a conducting medium close to the coil, the primary $\bf{E}_1$ will cause a separation of charges in the conducting medium that will in turn generate a secondary electric field ($\bf{E}_2$). Therefore, if we consider that the brain is a conductive and is close enough to the stimulation coil, the total electric field induced in the tissue is the sum of the primary and secondary electric fields.
$$
\bf{E}_{total} = \bf{E}_1 + \bf{E}_2
$$
To compute the total electric field in the brain we can compute separately the $\bf{E}_1$ and $\bf{E}_2$ using similar approximations but different methods. First of all we have to consider that TMS is a quasi-static problem.

For the quasi static approximation we consider:

1. No charge accumulation;
2. For the given distance between coil and head there is no retarded time, in other words no phase difference between magnetic and electric fields;
3. Other reasons that Aino knows.

Also we separate the solutions of $\bf{E}_1$ and $\bf{E}_2$ in two. First, for $\bf{E}_1$ we use Faraday's law, with the definition of magnetic vector potential:
$$
\bf{E}_1(\bf{r}, t) = - \frac{\partial \bf{A}(\bf{r}, t)}{\partial t}
$$
For $\bf{E}_2$ the interpretation is a little bit more complicated.