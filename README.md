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
</p>

## Implementation Results
The model was given 106 views of the scene in the training step. The collections of training images cannot contain each and every angle of the scene. A trained model can represent the entire 3-D scene with a sparse set of training images. Here we provide different poses to the model and ask for it to give us the 2-D image corresponding to that camera view. If we infer the model for all the 360-degree views, it should provide an overview of the entire scenery from all around.
<p align="center">
  <img src="https://github.com/EssamMohamedAbo-ElMkarem/Neural-Radiance-Field-NeRF-/blob/main/impres.png" style="width:600px;"/>
</p>

## Conclusion
There is no doubt that there has been a great deal of research on 3d imaging and all other computer vision applications that would enhance our lives in the very near future. That's why I've put an effort here trying to wrap the implementation provided by Aritra Roy Gosthipaty wiith Tensorflow up with a quick explanation of the paper itself to put it as a milestone for anyone trying to dig into the topic from an applicable prespective. I've also modified the architecture of the neural network a little bit to improve the performance of the model. I really appretiate the great work done here in this paper by the researchers and of course there has been many improvements in the field when it comes to NeRFs but this paper is considered a really good entrance to the topic.
