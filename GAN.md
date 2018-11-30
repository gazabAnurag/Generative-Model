## GAN key points
WGAN->BigGan->CapsuleNet
### Discriminator
- Requires discriminator as CNN, uses Leaky ReLU after each layer, stride not MaxPool(why), 0.4 and 0.7 dropout at each layer
> Strided conv, 
- Output is a sigmoid yielding a probability 
  #### Model
  - Use RMSProp/Adam optimizer, Cross Entropy loss measure
 
 ### Generator
 - Generate image using random sample using [-1,1] and transposed Conv (could be fractionally or upsampling )
 - Batch Normalization
 - Use ReLU, dropout of 0.3 and 0.5 in the first layer 
 
 ### Training 
 - Test the discriminative first, train the discriminative and adversal then
 - if images do not improve set the drop out to 0.3/0.6
 - discriminator converges quickly, increase the LR and train the adversial first 
 - if images still like noise check the dropout activation batch normalization and dropout 
 - create the baseline and tweak one HP at a time , run few epochs (Where???)
 
 
