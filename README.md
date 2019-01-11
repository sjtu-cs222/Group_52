# 52
Hierarchical Relation Extraction with Encoder-Decoder model
report is in "report.pdf"
LaTeX code is in "LaTeX code.zip"
program code is in "code.zip"

Make sure you have the following packages installed:
Python (2.7)
Tensorflow (1.12)
scikit-learn (>=0.18)
Matplotlib (>=2.0.0)

There are two model in the zip, for the GRU+ATT you can first put your dataset in the folder "origin_data".
For training, you need to type the following command:
python train_GRU.py
The training model file will be saved in folder model/

You can lauch the tensorboard to see the softmax_loss, l2_loss and final_loss curve by typing the following command: tensorboard --logdir=./train_loss

For testing, you need to run the test_GRU.py to get all results on test dataset. BUT before you run it, you should change the pathname and modeliters you want to perform testing on in the test_GRU.py. We have add 'ATTENTION' to the code in test_GRU.py where you have to change before you test your own models.

As an example, we provide our best model in the model/ directory. You just need to type the following command:
python test_GRU.py
The testing results will be printed(mainly the P@N results and the area of PR curve) and the all results on test dataset will be saved in out/ directory with the prefix "sample"

To draw the PR curve for the sample model, you just need to type the following command:
python plot_pr.py
