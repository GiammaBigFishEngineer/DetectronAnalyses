# Test sui vari modelli di Detectron2

Nel seguente file vengono testati i modelli pre addestrati di detectron su immagini del validation set di COCO in base alla classe etichettata sull'immagine.

### Modelli testati:
1 - Mask RCNN 50


2 - Mask RCNN 101


3 - R 50 Panoptic


4 - R 101 Panoptic

Le mask RCNN vengono testate sulle tre tipologie di backbone che i modelli mettono a disposizione come **FPN**, **DC5**, **C4**
Le segmentazioni semantiche sono messe a disposizione solo su bakbone con **FPN**.

Per calcolare l'errore sulla predizione delle immagini viene usata la distanza di Hausdorff
```math
d_h(X,Y) =  max(h(X,Y),h(Y,X))
```
```math
h(X,Y) = sup(inf(d(x,y): y \in Y): x \in X)
```

