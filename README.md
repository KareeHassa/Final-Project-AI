# VAE-GAN with U-Net Discriminator

![Generated Faces](Grid.png)

## Key Features
- **U-Net Discriminator**: Skip connections enable multi-scale feedback for fine facial details  
- **L1 + Perceptual Loss**: Combines edge preservation (L1) and semantic coherence (VGG19)  
- **25-Epoch Training**: Achieves stable results on CelebA (64×64)  

## Architecture
### Hybrid Framework
1. **VAE Encoder**: Structured latent space with KL-divergence  
2. **U-Net Discriminator**: Pixel-wise realism maps via skip connections  
3. **Balanced Losses**:  
   - Adversarial loss (GAN)  
   - L1 reconstruction (λ=100)  
   - Perceptual loss (λ=0.3)  

*(See report Figure 2 for detailed encoder/decoder diagrams)*  

## Results
### Reconstruction Comparison
| Original | Reconstructed |  
|----------|---------------|  
| ![Original]([images\Original.png](https://github.com/KareeHassa/Final-Project-AI/blob/main/images/Original.png?raw=true)) | ![Reconstructed](Reconstructed.png) |  


### Generated Samples
![Generated Faces](Grid.png)  
- High diversity with minimal artifacts  
- Stable training (no mode collapse)  

