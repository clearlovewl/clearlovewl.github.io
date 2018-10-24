class: center, middle



---
# ABSTRCT

Convolutional networks are powerful visual models that yield  hierarchies  of  features.FCN show  that  convolutional networks by themselves, trained end-to-end, pixels-to-pixels,  exceed  the  state-of-the-art  in  semantic  segmentation.

---

# Adapting classifiers for dense prediction

typical recognition nets, including lenet [21], alexnet[19],  and  its  deeper  successors  [31,  32],  ostensibly  takefixed-sized inputs and produce nonspatial outputs. the fullyconnected layers of these nets have fixed dimensions andthrow away spatial coordinates.  however, these fully con-nected layers can also be viewed as convolutions with ker-nels  that  cover  their  entire  input  regions.   doing  so  caststhem  into  fully  convolutional  networks  that  take  input  ofany size and output classification maps.

---

![fcn](https://clearlovewl.github.io/2018/10/22/fcn/fcn.png)

---

# Segmentation Architecture

![fcn2](https://clearlovewl.github.io/2018/10/22/fcn/fcn2.png)

---

we address this by adding links that combine the finalprediction layer with lower layers with finer strides.  this turns a line topology into a dag, with edges that skip aheadfrom lower layers to higher ones (figure 3).   as they seefewer pixels, the finer scale predictions should need fewerlayers, so it makes sense to make them from shallower netoutputs.   combining fine layers and coarse layers lets the model make local predictions that respect global structure.by analogy to the multiscale local jet of floracket al. [10],we call our nonlinear local feature hierarchy the deep jet

---

![vgg](https://clearlovewl.github.io/2018/10/22/fcn/vgg.png)

---

![fcn2](https://clearlovewl.github.io/2018/10/22/fcn/fcn8.png)

---

# Transpose Convolution

![tconv](https://clearlovewl.github.io/2018/10/22/fcn/tconv.png)

---

# Results

table 3 gives the performance of ourfcn-8s on the test sets of pascal voc 2011 and 2012,and compares it to the previous state-of-the-art, sds [16],and the well-known r-cnn [12].  we achieve the best re-sults on mean iu by a relative margin of 20%.  inferencetime is reduced114×(convnet only, ignoring proposals andrefinement) or286×(overall)

Mean Intersection over Union(MIoU，均交并比)

![xiaoguo](https://clearlovewl.github.io/2018/10/22/fcn/xiaoguo.png)

---