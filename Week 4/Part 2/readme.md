Now that we've successfully made a neural network that can identify handwritten digits, let's try to do the same with alphabets.
For handwritten alphabets classifier, we'll be using the EMNIST(extended MNIST) dataset.
- This dataset contains 372450 handwritten alphabets!
- Labelled from 0 (for A) to 25 (for Z)
- Pixel values are stored in the same form as the MNIST dataset (ie. 784 pixels of a single 28x28 image stored as a row of a 2D matrix)
- EMNIST's similarity to MNIST will make the task of implementing our MNIST model to EMNIST model much simpler, requiring only a few minor changes (can you figure them out?).

You can download the EMNIST dataset from [here](https://drive.google.com/file/d/19pLVDMwag_FIftNdwMBtbUbAuDUtnhgf/view?usp=sharing), and complete the code in [this](https://colab.research.google.com/drive/17cbhaP5hoci-8mYiXxBThBMZqs3hceAn?usp=sharing) colab notebook
