# XAI-Evolving-Binary-Masks
Explaining Image Classification by evolving Binary Masks

Most of us are familiar with the deep neural networks like CNN and their efficiency in image classification tasks. But one might wonder how is the CNN able to make such decisions as the way the image gets percieved by a computer is very different compared to our vision. That being said, algorithms like eXplainable Arificial Intelligence or XAI algorithms can actually help us in deciphering how black-box models like CNNs really work. Some of the notable XAI algorithms include Grad-Cam, LIME, SHAP etc. This is an algorithm created by me during my Mtech Final year as part of the dissertation. This novel method is inspired by the Evolutionary Algorithms, EA, and has been used for explaining the image classification. The contributions of this algorithm encompass the following:

- A model-agnostic evolutionary eXplainable Artificial Intelligence (XAI) algorithm offering local explanations for image classification tasks.
- A representation strategy to mitigate the sparsity of genetic chromosomes, eliminating the need for additional tools like image segmentation. 
- A gradient-free approach for quantifying the contributions of contributing pixels. 
- A hierarchical approach integrated with EA to address the sparsity of image attributes.
- Implementation of negative reinforcement to enforce consistency in prediction between the original and masked image.

So what does a sample explanation look like ? 
For eg, If we take some samples from the CIFAR 10 images and we want to understand which patches of a particular image got it classfied into a particular label such as dog, frog cat etc. We can pass this image and the CNN model to the algorithm. The result is basically a binary mask which reveals the important regions when superimposed on the original image and a score matrix is also produced which mentions the correspoding contributions of the pixels. 

<img width="600" alt="cifar" src="https://github.com/rudra-99/XAI-Evolving-Binary-Masks/assets/107755049/6c321dae-0dc6-4a62-95fb-59071d999745">

On the left we have the original images with the predicitions provided by the CNN. In the middle our proposed algorithm retrieves the essential regions which are contributing to the prediciton. Additonally we also have a score matrix which provides a visualisation of the contribution provided by these essesntial image attributes.

We have also proposed a metric for quantifying the quality of explanation. Now in an image explantion, we are looking for a set of pixels for which the prediciton confidence is maximised. An XAI algorithm can just bypass this whole image and say all the pixels are important and thus achieve the highest confidence. To overcome this fault we have introduced a metric called Confidence per pixel or CP score. CP score is simply the `confidence * total number of pixels in the original image / total number of pixels used for explantions`. So we are looking for a good localisation of image attributes as well as the selected pixels having a relatively high confidence from the other pixels. Here is a comparitive analysis amongst the results obtained from other XAI algorithms against our proposed algorithm. 


<img width="800" alt="cifar" src="https://github.com/rudra-99/XAI-Evolving-Binary-Masks/assets/107755049/ddab34f1-c178-415c-97e7-2ca4e0620f77">



