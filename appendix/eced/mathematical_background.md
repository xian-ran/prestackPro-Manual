### Mathematical background {#mathematical-background}

Edge- and coherence-enhancing anisotropic diffusion filtering (ECED) performs structure-adaptive smoothing. Let $$\Omega\subset R^3$$  denote a three-dimensional image domain and $$f:\Omega\rightarrow R$$ be a scalar-valued image. Then a filtered version $$u(x,y,z,z)$$ of $$f(x,y,z)$$  is computed by regarding $$f$$ as initial state of a diffusion equation


$$
\partial_tu = \nabla ^T(D(J_\rho(\nabla u_\sigma ))\nabla u)
$$



with homogeneous Neumann boundary conditions. Here denotes the spatial nabla operator, and is the diffusion time.

The diffusion tensor is a positive semidefinite 3x3 matrix that is chosen as a function of the so-called structure tensor

where denotes convolution, is a Gaussian with standard deviation , and . The parameter is called noise scale, and is the integration scale.

The structure tensor is a well-established tool for describing local image structure: Let denote the eigenvalues of this positive semidefinite 3x3 matrix, and be the corresponding eigenvalues. Then the orthogonal eigenvectors specify the preferred local orientations, and the eigenvalues characterise the contrast in these directions.

In order to adapt the diffusion process to the local image structure, the diffusion tensor uses the same eigenvectors as the structure tensor , and its eigenvalues are given by

with a so-called contrast parameter . This strategy allows to reduce diffusion across the dominant structure (in the direction of ), while diffusing with full strength along these structures (the local plane spanned by and ). The contrast parameter is automatically determined, given the amplitude scale of the seismic data, in order to obtain very low values for for relevant seismic amplitudes.