# VAE-GAN with U-Net Discriminator

![Generated Faces](images/Final2.png)

## Key Features
- **U-Net Discriminator**: Skip connections enable multi-scale feedback for fine facial details  
- **L1 + Perceptual Loss**: Combines edge preservation (L1) and semantic coherence (VGG19)  
- **25-Epoch Training**: Achieves stable results on CelebA (64×64)  

## Architecture
### Hybrid Framework
1. **Encoder**: Structured latent space with KL-divergence  
![Encoder](images/Enc.png)
2. **Decoder**
![Decoder](images/Dec.png)
3. **U-Net Discriminator**: Pixel-wise realism maps via skip connections  
![Discriminator](images/Disc.png)
4. **Balanced Losses**:  
   - Adversarial loss (GAN)  
   - L1 reconstruction (λ=100)  
   - Perceptual loss (λ=0.3)  

## Results
### Reconstruction Comparison
### Original 
![Original](images/Original.png) 
### Reconstructed 
![Reconstructed](images/Reconstructed.png)   


### Generated Samples
![Generated Faces](images/Grid.png)  
- High diversity with minimal artifacts  
- Stable training (no mode collapse)  

