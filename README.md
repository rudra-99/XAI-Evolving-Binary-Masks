# XAI-Evolving-Binary-Masks
Explaining Image Classification by evolving Binary Masks

A novel method inspired by the Evolutionary Algorithms, EA, has been used for explaining the image classification. The contributions of this algorithm encompass the following:

- A model-agnostic evolutionary eXplainable Artificial Intelligence (XAI) algorithm offering local explanations for image classification tasks.
- A representation strategy to mitigate the sparsity of genetic chromosomes, eliminating the need for additional tools like image segmentation. 
- A gradient-free approach for quantifying the contributions of contributing pixels. 
- A hierarchical approach integrated with EA to address the sparsity of image attributes.
- Implementation of negative reinforcement to enforce consistency in prediction between the original and masked image.

Results from CIFAR10 dataset
<img width="800" alt="cifar" src="https://github.com/rudra-99/XAI-Evolving-Binary-Masks/assets/107755049/ad45320b-f930-441b-88fb-18407bc71ab4">

Results from Imagenette dataset
<img width="800" alt="imgnet" src="https://github.com/rudra-99/XAI-Evolving-Binary-Masks/assets/107755049/78866698-fd63-4c9b-b9f1-f4773070749e">

Results from Caltech101 dataset
<img width="800" alt="caltech" src="https://github.com/rudra-99/XAI-Evolving-Binary-Masks/assets/107755049/50cf5959-2bfb-44ec-908b-985dcd38eebb">



