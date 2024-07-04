# Computer-Vision: Detecting if the red coral polyp is open or close

As currently I do not have permission to share the data, I am only putting some rudamentory results.

## Annotaed Data

62 images were annotated and marked as open, close or partial (open/close).
Here is some initial information on the annotated data.
As the transition is for very small amount of time, we don't really have a lot of data.
However, enough data was available for the other two states of the coral.
Howver, in ths particular sub-set of annotated data open annotations are more than close.

![image](./model_info/labels.jpg)

Here we see the correlation between the annotations:

![image](./model_info/labels_correlogram.jpg)

## Model Results

The model was trained in `yolo5x.pt`.
Here are the results of the traingin for 50 epochs.

![image](./model_info/results.png)


## Predictions on unseen photos

Below we see the predictions for never before seen mages of red coral. 
Additionally, the training data was not augmented to have rotations.
Hence, the first image seen where corals are growing downwards, the model hasn't seen at all, and hence has difficulty Detecting.

![image](./results/redcoraleffe.jpg)

For the other two, the results are ok.

![image](./results/CORAIL_large.jpg)

![image](./results/demo4-corallium-rubrum-demo4-corallium-rubrum-ambiance-corail.jpg)


## Net Steps

- Train the model for longer
- augment data through mirror, rotations, color adjustments
- add more annotated data
- may be drop the annotation for partial


