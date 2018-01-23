# Transfer-Learning

This is a code showing transfer learning in Keras for the Kaggle competition Dogs vs Cats redux - https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition/leaderboard. I use inceptionv3 and add two more layers at the end of it. For the transfer learning part I train only the last two layers while for fine tuning I unfreeze the last two residual blocks. Submitting to Kaggle I get  non clipped - 0.09480, clipped @ 0.05-0.08616, 0.03 -0.06928, 0.01 - 0.05569, 0.005 - 0.05440, 0.0005 - 0.05978. This shows how important it is to clip the values to get a high log loss value. The best value of 0.05440 would be in the top 7% for this Kaggle competition hich show just how good transfer learning is. 

## Future Directions

Try different sorts of data augmentation as in Sample pairing (https://arxiv.org/pdf/1801.02929.pdf) this would require training it for more epochs (at least 10). A dropout layer should be inserted for regularization if it will be trained for that long. 

