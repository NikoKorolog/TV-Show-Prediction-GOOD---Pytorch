This is a personal project where I trained a pytorch neural net on metadata from my own personal music library to predict which tracks would be used on TV shows. This is a real-world dataset of
metadata from music that I actually wrote, and published, and pitched to TV shows. I kept a record of which tracks ended up on TV and used that positive indicator as target variable. I did all 
of this work in jupyter lab over the course of a few hours so I didn't actually commit any of the updates to the code which I promise to do on future projects - I just have a lot of stuff I need to 
upload to git from the past few weeks and wasn't really thinking about version control because I didn't think I was going to share it with anybody.
All of the features in the dataset were pulled from metadata on each of the tracks I had collected for personal use, and encoded to numerals according to a legend for each categorical variable.
I had anticipated using Tensorflow / Keras for this project and it turns out that Pytorch will accept categorical variables in string form so I spent a lot of time needlessly encoding features.
I ran this project with an 80/20 train test split and the resulting neural net gives me a 70% accuracy at predicting whether or not a track will get used by a TV show based upon metadata alone
which is better than I expected but still not totally useful for testing tracks in the real world, I think I need a bigger dataset and this dataset took me a week to clean up and format.
I experimented with different layer / neuron architectures but the model seemed to max out in accuracy at 69 or 70% regardless of the architecture or training epochs. I don't think it was
overfitted because none of the test data matched verbatim and I still got a 70% accuracy. Next steps might be figuring out how to build a complimentary generative model to generate metadata 
that fits this model or creating a new model that takes actual audio files as input instead of metadata.
