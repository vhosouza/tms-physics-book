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

To know the effects of TMS we have to compute the induced electric field in the brain tissue. Consider an electric current $$I(t)$$ changing over time and running in a coil away in free space. The changing current will generate a magnetic field that also changes in time. According to Faraday's law of induction, the changing magnetic field will induce an associated primary electric field $$\bf{E}_1$$ in space.

However, as we insert a conducting medium close to the coil, the primary $$\bf{E}_1​$$ will cause a separation of charges in the conducting medium that will in turn generate a secondary electric field ($$\bf{E}_2​$$). Therefore, if we consider that the brain is a conductive and is close enough to the stimulation coil, the total electric field induced in the tissue is the sum of the primary and secondary electric fields.

$$
\bf{E}_{total} = \bf{E}_1 + \bf{E}_2
$$

To compute the total electric field in the brain we can compute separately the $$\bf{E}_1$$ and $$\bf{E}_2$$ using similar approximations but different methods. First of all we have to consider that TMS is a quasi-static problem.

For the quasi static approximation we consider:

1. No charge accumulation;
2. For the given distance between coil and head there is no retarded time, in other words no phase difference between magnetic and electric fields;
3. Other reasons that Aino knows.

Also we separate the solutions of $$\bf{E}_1$$ and  $$\bf{E}_2$$ in two. First, for  $$\bf{E}_1$$ we use Faraday's law, with the definition of magnetic vector potential:

$$
\bf{E}_1(\bf{r}, t) = - \frac{\partial \bf{A}(\bf{r}, t)}{\partial t}
$$

For $$\bf{E}_2$$ the interpretation is a little bit more complicated. The $$\bf{E}_2$$ exists only in the conductive medium and is associated also with a secondary magnetic field $$\bf{B}_2$$.

$$
\bf{\nabla}\times\bf{E}_2 = - \frac{\partial \bf{B}_2}{\partial t}
$$

$$
\bf{\nabla}\cdot\bf{E}_2 = \frac{\rho}{{\varepsilon_0}} \qquad \text{This holds everywhere in the brain}
$$

However, considering the quasi-static approximation and that the conductivity of the medium is too low, the $$\bf{B}_2$$ is negligible and therefore we have that:

$$
\bf{\nabla}\times\bf{E}_2 \approx 0
$$

But also, we know that:

$$
\bf{J}=\sigma\bf{E}
$$

and than we can substitute to the equation of $$\bf{\nabla}\cdot\bf{E}_2$$ and get:

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

According to the conservation of currents in a system in which there is no electric current \(or charges\) being added to the conducting media, we have that:

$$
\bf{\nabla}\cdot\bf{J} + \frac{\partial \rho }{\partial t} = 0
$$

If we combine the two latter equations we get:

$$
-\frac{\sigma}{{\varepsilon_0}} \rho = \frac{\partial\rho}{\partial t}
$$

The solution than is the exponential function of the form:

$$
\rho(t) = e^{-\omega_0 t}
$$

And from that follows:

$$
\omega_0 \equiv \frac{\sigma}{\varepsilon_0}
$$

Which is than:

$$
\omega_0 \approx 1.8 \times10^{-9} \text s
$$

And thus, the equation $$\nabla \cdot {\bf{J}} = \frac{\sigma} \rho$$ becomes:

$$
\nabla \cdot {\bf{J}} = 0
$$

Which means that the total current in the system is the divergent of the current density added to the change in time of the charge density. And also, if $$\rho$$ goes to zero, we have that:

$$
\bf{\nabla}\cdot\bf{E}_2 = 0
$$

And from the fact that:

$$
\bf{\nabla}\times\bf{E}_2 = 0
$$

Then $$\bf{E}_2$$ can be written as the gradient of a scalar potential, which in turn is:

$$
\bf{E}_2 = - \nabla V
$$

If we replace to the divergent of $$\bf{E}_2$$ we have two possible cases:

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

For both cases we have possible ways to solve for the potential and then get to the secondary electric field $$\bf{E}_2$$.

Another parameter to consider in the quasi-static approximation is the skin depth $$\delta$$ . The skin depth is the amount in which the electric field decays with the depth of the conductor by a factor of $$1/e$$ . This definition can be found in Chapter 9.4 in Griffiths Introduction to Electrodynamics where it deals with electromagnetic waves in conductors (4th edition page 417). In our case the diameter $$D$$ of the head is much bigger than the skin depth. Consider the two Maxwell's Equations:
$$
\bf{\nabla}\times\bf{E} = - \frac{\partial \bf{B}}{\partial t} \qquad \text{(i)}
$$

$$
\bf{\nabla}\times\bf{B} = \mu_0\bf{J} + \mu_0\varepsilon_0\frac{ \partial \bf{E}}{\partial t} \qquad \text{(ii)}
$$

If one applies the curl to $$\text{i}$$ and $$\text{ii}$$ , following the mathematical identity that:
$$
\bf{\nabla}\times(\bf{\nabla}\times\bf{A}) = \bf{\nabla}(\bf{\nabla}\dot\bf{A}) + \nabla^2\bf{A}
$$
We get to:
$$
\nabla^2\bf{E}=\mu\epsilon \frac{\partial^2\bf{E}}{\partial^2 t} +\mu\sigma \frac{\partial\bf{E}}{\partial t}
$$
Which admit the plane-wave solution:
$$
\tilde{E}(z,t) = \tilde{E}_0e^{i(\tilde{k}z-\omega t)}
$$
where $$\tilde{k}$$ is the complex wave number written as:
$$
\tilde{k}^2=\mu\epsilon\omega^2 + i\mu\sigma\omega
$$
By taking the square root:
$$
\tilde{k}=k + i\kappa
$$

$$
k=\omega\sqrt{\frac{\epsilon\mu}{2}}\Bigg[\sqrt{1+\Big(\frac{\sigma}{\epsilon\omega}\Big)^2}+1\Bigg]^{1/2} \quad, \quad \kappa\equiv\omega\sqrt{\frac{\epsilon\mu}{2}}\Bigg[\sqrt{1+\Big(\frac{\sigma}{\epsilon\omega}\Big)^2}-1\Bigg]^{1/2}
$$

The attenuation comes from the imaginary part of $$\tilde{k}$$, in which reduces $$\tilde{E}(z,t)$$ with the increase in $$z$$ . Then:
$$
\tilde{E}(z,t) = \tilde{E}_0e^{-\kappa z}e^{i(kz-\omega t)}
$$
Finally, the skin depth $$\delta$$ comes from the amount in which the electric field decays with the depth of the conductor by a factor of $$1/e$$ , and is:
$$
\delta=\frac{1}{\kappa}
$$
Finally, taking that:
$$
\omega_0 \equiv \frac{\sigma}{\varepsilon_0}
$$
And $$\omega/\omega_0\ll1$$, we get:
$$
\delta \equiv \frac{1}{2}\mu_0\sigma\omega
$$
And we can also write $$E(z,t)$$ as:
$$
\nabla^2{\bf{E}}= -(i\mu_0\sigma\omega + \mu_0\epsilon\omega^2)\bf{E}
$$
If we take the conductivity of the brain as $$\sigma=0.4 / \Omega\text{-m}$$ and for $$\omega=10^5 \text{Hz}$$ , $$\delta^2=4.0 \times 10^5 \text{cm}^2$$, and thus $$(D/\delta)^2\ll1$$. According to Heller et al. (1992), this is the essence of the quasi-static approximation and leads to:
$$
\nabla^2{\bf{E}}= 0
$$

Therefore, a static electric field cannot penetrate a conductor.