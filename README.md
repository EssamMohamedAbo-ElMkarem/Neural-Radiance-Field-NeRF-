# Neural Radiance Field(NeRF)
A neural radiance field (NeRF) is a fully-connected neural network that can generate novel views of complex 3D scenes, based on a partial set of 2D images.
<p align="center">
  <img src="https://github.com/EssamMohamedAbo-ElMkarem/Neural-Radiance-Field-NeRF-/blob/main/Images/image1.png" style="width:800px;"/>
</p>
## Problem set up
The representation here is a continuous scene as a 5D vector-valued function whose input is
a 3D location x = (x, y, z) and 2D viewing direction (θ, φ), and whose output
is an emitted color c = (r, g, b) and volume density σ. 
<p align="center">
  <img src="https://github.com/EssamMohamedAbo-ElMkarem/Neural-Radiance-Field-NeRF-/blob/main/Images/image2.png" style="width:800px;"/>
</p>In practice, we express direction as a 3D Cartesian unit vector d. We approximate this continuous 5D
scene representation with an MLP network F Θ : (x, d) → (c, σ) and optimize its
weights Θ to map from each input 5D coordinate to its corresponding volume
density and directional emitted color.
The paper encourages the representation to be multiview consistent by restricting
the network to predict the volume density σ as a function of only the location
x, while allowing the RGB color c to be predicted as a function of both location
and viewing direction. To accomplish this, the MLP F Θ first processes the input
3D coordinate x with 8 fully-connected layers (using ReLU activations and 256
channels per layer), and outputs σ and a 256-dimensional feature vector. This
feature vector is then concatenated with the camera ray’s viewing direction and
passed to one additional fully-connected layer (using a ReLU activation and 128
channels) that output the view-dependent RGB color.
There is no doubt that there has been a great deal of research on 3d imaging and all other computer vision applications that would enhance our lives in the very near future. That's why I've put an effort here trying to wrap the implementation provided by Aritra Roy Gosthipaty up with a quick explanation of the paper itself to put it as a milestone for anyone trying to dig into the topic from an applicable prespective. I've also modified the architecture of the neural network a little bit to improve the performance of the model. I really appretiate the great work done here in this paper by the researchers as actually the preliminary results are really promising and of course there has been many improvements in the field when it comes to NeRFs but this paper is considered a really good start to dig deeper into the topic.
###### Credits for the researchers behind this work
- Ben Mildenhall 
- Pratul P. Srinivasan
- Matthew Tancik 
- Jonathan T. Barron 
- Ravi Ramamoorthi 
- Ren Ng 
- UC Berkeley
- Google Research
- UC San Diego
