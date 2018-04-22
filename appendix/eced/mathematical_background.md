### Mathematical background {#mathematical-background}

Edge- and coherence-enhancing anisotropic diffusion filtering (ECED) performs structure-adaptive smoothing. Let $$\Omega\subset R^3$$  denote a three-dimensional image domain and $$f:\Omega\rightarrow R$$ be a scalar-valued image. Then a filtered version $$u(x,y,z,z)$$ of $$f(x,y,z)$$  is computed by regarding $$f$$ as initial state of a diffusion equation


$$
\partial_tu = \nabla ^T(D(J_\rho(\nabla u_\sigma ))\nabla u)
$$



with homogeneous Neumann boundary conditions. Here $$\nabla:=(\partial_x, \partial_y, \partial_z)^T$$ denotes the spatial nabla operator, and   is the diffusion time.

The diffusion tensor $$D$$ is a positive semidefinite 3x3 matrix that is chosen as a function of the so-called structure tensor


$$
J_\rho(\nabla u_\sigma) = K_\rho *(\nabla u_\sigma \nabla u_\sigma^T)
$$



where  $$*$$ denotes convolution, $$K_p$$  is a Gaussian with standard deviation $$\rho$$ , and $$u_\sigma := K_\sigma*u$$ . The parameter $$\sigma$$ is called noise scale, and  $$\rho$$ is the integration scale.

The structure tensor is a well-established tool for describing local image structure: Let $$\mu_1\geq\mu_2\geq\mu_3$$ denote the eigenvalues of this positive semidefinite 3x3 matrix, and $$\nu_1,\nu_2,\nu_3$$ be the corresponding eigenvalues. Then the orthogonal eigenvectors $$\nu_1,\nu_2,\nu_3$$ specify the preferred local orientations, and the eigenvalues $$\mu_1,\mu_2,\mu_3$$ characterize the contrast in these directions.

In order to adapt the diffusion process to the local image structure, the diffusion tensor $$D$$ uses the same eigenvectors $$\nu_1,\nu_2,\nu_3$$  as the structure tensor $$J_\rho(\nabla u_\sigma)$$ , and its eigenvalues are given by


$$
\lambda_1 = \{1-exp\lgroup \frac{-3.31488}{\mu_1^4/\lambda^8} \rgroup  ( \mu_1> 0)
$$


$$
\lambda_2 = 1
$$


$$
\lambda_3 = 1

$$




with a so-called contrast parameter $$\lambda> 0$$ . This strategy allows to reduce diffusion across the dominant structure (in the direction of $$\nu_1$$), while diffusing with full strength along these structures (the local plane spanned by $$\nu_2$$  and $$\nu_3$$ ). The contrast parameter $$\lambda$$ is automatically determined, given the amplitude scale of the seismic data, in order to obtain very low values for $$\lambda_1$$  for relevant seismic amplitudes.