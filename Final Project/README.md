## SNN for detecting static object <br>
Spiking Neural Networks (SNNs) offer a biologically inspired approach to object detection, yet their application to static images remains underexplored compared to dynamic inputs. This project investigates the use of SNNs for
static object detection, leveraging the SpikingJelly framework
to build and evaluate models on augmented datasets, including
MNIST, Fashion-MNIST, and Animal Faces. To address challenges such as angle variation, noise, and adversarial attacks, we integrate data augmentation, convolutional self-attention
auto-encoders (CSAAEs), and hardware optimizations. Our
results demonstrate that SNNs achieve 92.75% accuracy on MNIST and 87.21% on Fashion-MNIST with augmentation, while CSAAEs enhance robustness against adversarial
perturbations (e.g., 80.27% accuracy on Animal Faces under FGSM attacks). Additionally, a custom C-based SNN framework
reduces latency by replacing floating-point operations with fixed- point arithmetic and bit-shift optimizations, achieving significant
performance gains. This work highlights the potential of SNNs
for efficient, noise-resilient static object detection in real-world
applications.
