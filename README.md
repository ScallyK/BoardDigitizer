#####################################################################################################
#####################################################################################################
#####################################################################################################


# Board Digitizer:

Script that uses FastRCNN model to determine if a tile on a chess board is occupied and if so, determine what piece it is. Results are then stored in image, string, and array form.


#####################################################################################################
#####################################################################################################
#####################################################################################################


# Breakdown:

1) Splits an image of a chessboard into 64 separate segments. (each image represents a tile on the chessboard)

2) Model is applied to each image to determine if a piece is present on the tile. 

3) Images with completed model evaluations are stored in outputs/inference/res*

4) Text output of each completed evaluation is stored in a text file named classes.txt

5) Results of classes.txt are appended to an array named piece_array



#####################################################################################################
#####################################################################################################
#####################################################################################################


# Requirements:

1) See requiremnts.txt

2) Code was developed/tested in AWS Sagemaker with a GPU instance. When running this code, ensure you have an NVIDIA GPU and >=PyTorch 1.8 as well as >= Python 3.6 

3) CPU-Only versions of PyTorch may still run this, but it has not been tested. Changes to requirements.txt may be necessary and the --device 'cpu' flag will need to be appended as a parameter when running inference.py.


#####################################################################################################
#####################################################################################################
#####################################################################################################


# Original code (excepting Board_Digitizer.py) is from sovit-123 on GitHub. 

# See here for details:https://github.com/sovit-123/fasterrcnn-pytorch-training-pipeline

# Edits made to inference.py and requirements.txt to attain proper board evaluation.



#####################################################################################################
#####################################################################################################
#####################################################################################################
