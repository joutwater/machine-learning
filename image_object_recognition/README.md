## Using object recognition to find airplanes in a set of images
### Feature creation : Historgram of Oriented Gradients
### Current model : Multilayer Perceptron (Neural Network)

I've been looking forward to the image recognition project this semester in ML because of my background in photogrammetry and remote sensing. I think the application of these skills can be useful in a wide varitey of imagery anaylses.

The first part of this iteration was focused on feature building and parameter tweaking. I started with the canny method which is used to detect edges of an object in an image. I played with the sensitivity of canny by changing values in sigma, low threshold, and high threshold to see how the highly pixelated image output was affected. I would occassionally run my features through the perceptron and multilayer perceptron models to see how the edge choices were changing the recall of the model. I was only getting up to about 0.5 recall in these efforts. I then tried the hog method which returned a jump in recall. The parameters I used were : orientations=12, pixels_per_cell=(10, 10), cells_per_block=(4, 4), block_norm='L2-Hys', transform_sqrt=True, feature_vector=True). I was not able to print out images of the hog while changing parameters so I would check changes in the model output occassionally.

The model I chose was the multilayer perceptron aka neural netowrk (NN). NN and the perceptron were producing similar recalls throughout experimentation, but I heard the NN would be the best model to use in this task so I focused on its parameters. The hidden_layers parameter was giving me the best results as I increased neurons and layers to a certain point.

Next steps will be fine-tuning the HOG method and NN model parameters.
