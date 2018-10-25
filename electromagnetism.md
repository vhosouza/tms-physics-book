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
\bf{\nabla}\cdot\bf{E} = \frac{\rho}{{\varepsilon_0}} \qquad \text{(Colomb's Law)}
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
For $\bf{E}_2$ the interpretation is a little bit more complicated. The $\bf{E}_2$ exists only in the conductive medium and is associated also with a secondary magnetic field $\bf{B}_2$.
$$
\bf{\nabla}\times\bf{E}_2 = - \frac{\partial \bf{B}_2}{\partial t}
$$

$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{\rho}{{\varepsilon_0}} \qquad \text{This holds everywhere in the brain}
$$

However, considering the quasi-static approximation and that the conductivity of the medium is too low, the $\bf{B}_2$ is negligible and therefore we have that:
$$
\bf{\nabla}\times\bf{E}_2 \approx 0
$$
But also, we know that:
$$
\bf{J}=\sigma\bf{E}
$$
and than we can substitute to the equation of $\bf{\nabla}\cdot\bf{E}_2$ and get:
$$
\bf{\nabla}\cdot\bf{E}_2 = \nabla \cdot {(\frac{\bf{J}}{\sigma})}
$$
If we consider that the conductivity is the same everywhere for a homogeneous medium, then it is constant, and:
$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{1}{\sigma} \nabla \cdot {\bf{J}}
$$
Than we can also get to:
$$
\frac{\rho}{{\varepsilon_0}} = \frac{1}{\sigma} \nabla \cdot {\bf{J}}
$$
And finally:
$$
\nabla \cdot {\bf{J}} = \frac{\sigma}{{\varepsilon_0}} \rho
$$


According to the conservation of currents in a system in which there is no electric current (or charges) being added to the conducting media, we have that:
$$
\bf{\nabla}\cdot\bf{J} + \frac{\part\rho}{\part t} = 0
$$
If we combine the two latter equations we get:
$$
-\frac{\sigma}{{\varepsilon_0}} \rho = \frac{\part\rho}{\part t}
$$
The solution than is the exponential function of the form:
$$
\rho(t) = e^{-\omega_0 t}
$$
And from that follows:
$$
\omega_0 = \frac{\sigma}{\varepsilon_0}
$$
Which is than:
$$
\omega_0 \approx 1.8 \times10^{-9} \text s
$$


And thus, the equation $\nabla \cdot {\bf{J}} = \frac{\sigma}{{\varepsilon_0}} \rho$ becomes:
$$
\nabla \cdot {\bf{J}} = 0
$$


Which means that the total current in the system is the divergent of the current density added to the change in time of the charge density. And also, if $\rho$ goes to zero, we have that:
$$
\bf{\nabla}\cdot\bf{E}_2 = 0
$$
And from the fact that:
$$
\bf{\nabla}\times\bf{E}_2 = 0
$$
Then $\bf{E}_2$ can be written as the gradient of a scalar potential, which in turn is:
$$
\bf{E}_2 = - \nabla V
$$
If we replace to the divergent of $\bf{E}_2$ we have two possible cases:
$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{\rho}{\varepsilon_0} = - \nabla^2V
$$

$$
\nabla^2V = - \frac{\rho}{\varepsilon_0} \qquad \text{Poisson's equation}
$$

And second case:
$$
\bf{\nabla}\cdot\bf{E}_2 = 0 = - \nabla^2V
$$

$$
\nabla^2V = 0 \qquad \text{Laplace's equation}
$$



For both cases we have possible ways to solve for the potential and then get to the secondary electric field $\bf{E}_2$.

